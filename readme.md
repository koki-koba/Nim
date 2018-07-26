# <img src="https://raw.githubusercontent.com/nim-lang/assets/master/Art/logo-crown.png" height="28px"/> Nim [![Build Status][badge-nim-travisci]][nim-travisci]

���̃��|�W�g���ɂ� Nim�R���p�C��, Nim��stdlib, �c�[������уh�L�������g���܂܂�Ă��܂��B
������Nim�ɂ��Ēm�肽���Ƃ���, �h�L�������g���܂ލŐV�����[�X���_�E�����[�h���Ă��������B [Nim�̃T�C�g][nim-site].

## �R�~���j�e�B(�p��)
[![Join the IRC chat][badge-nim-irc]][nim-irc]
[![Join the Gitter chat][badge-nim-gitter]][nim-gitter]
[![Get help][badge-nim-forum-gethelp]][nim-forum]
[![View Nim posts on Stack Overflow][badge-nim-stackoverflow]][nim-stackoverflow-newest]
[![Follow @nim_lang on Twitter][badge-nim-twitter]][nim-twitter]

* [Nim�̃t�H�[����][nim-forum] - Nim�ɂ��Ď��₵����, �c�_����ɂ͍ō��̏ꏊ�ł�
* [#nim IRC�`�����l��(Freenode)][nim-irc] - Nim�ɂ��ă��A���^�C���ŋc�_����ꏊ�ł��B
  �܂��A�قƂ�ǂ̊J�������IRC�ōs���܂��B
* [Gitter][nim-gitter] - Nim�ɂ��ă��A���^�C���ŋc�_���邽�߂̕⏕�I�ȏ�ł��B
  Gitter��IRC�̊Ԃɂ̓u���b�W������܂��B
* [Telegram][nim-telegram] - Nim�ɂ��ă��A���^�C���ŋc�_���邽�߂̕⏕�I�ȏ�ł��B
  �����Nim�̌���Telegram�`�����l���ł��B
* [Stack Overflow][nim-stackoverflow] - �v���O���~���O�֘A�̈�ʓI��Q&A�T�C�g�B
  Nim�ɂ��Ẵg�s�b�N������܂��B
* [Github Wiki][nim-wiki] - ���̑��̃��[�U�[�ɂ��R���e���c�B

## �R���p�C��
�R���p�C���͌��݁A�ȉ��̃v���b�g�t�H�[����
�A�[�L�e�N�`���̑g�ݍ��킹�������ɃT�|�[�g���Ă��܂�:

  * Windows (Windows XP�ȍ~) - x86 �� x86_64
  * Linux (���ׂĂł͂Ȃ����A�قƂ�ǂ��T�|�[�g) - x86, x86_64, ppc64 �� armv6l
  * Mac OS X (10.04�ȍ~) - x86, x86_64 �� ppc64

��葽���̃v���b�g�t�H�[�����T�|�[�g����Ă��܂����A����I�Ƀe�X�g����Ă��炸�A��L��
�v���b�g�t�H�[���قǈ��肵�Ă��Ȃ��\��������܂��B

���̎菇�ʂ�Ɏ��s�����Nim�̃R���p�C���͔��ɊȒP�ł�:

Nim�R���p�C�����̂�Nim�𗘗p���ď�����Ă��邽�߁ANim�R���p�C����C�ŏ����ꂽ�Â��o�[�W�����̃\�[�X���K�v�ł��B
�����͂����炩�����ł��܂��B[``nim-lang/csources``][csources-repo]���|�W�g��


���ɁA�r���h�ɕK�v�Ȃ��̂�p�ӂ��܂�:

  * ``gcc`` 3.x/�ȍ~, ``clang``, ``Visual C++`` �� ``Intel C++``�Ȃǂ̃R���p�C���B
    ���� ``gcc`` 3.x �ȍ~���g�����Ƃ������߂��܂��B
  * ``git`` �������� ``wget`` �\�[�X�����|�W�g������_�E�����[�h���邽�߂ɗ��p���܂��B
  * Ubuntu��``gcc``�𗘗p����Ƃ���``build-essential``�p�b�P�[�W���g���܂��B
    (����Ubuntu�f�B�X�g���r���[�V�����ł����l�ł��B) 

���� \*nix �V�X�e�� �܂��� Windows �𗘗p���Ă���ꍇ�́A�ȉ��̎菇�ŃR���p�C������K�v������܂��B
Nim���\�[�X���� ``gcc``, ``git`` �� ``koch`` �𗘗p���ăr���h����B
(``sh build.sh`` �̑����x86 Windows�ł� ``build.bat`` ���Ax86_64 Windows�ł� ``build64.bat`` �𗘗p���Ă��������B):

**����: �ȉ��̃R�}���h�͊J���ŃR���p�C���̃r���h�菇�ł�**
��ʃ��[�U�[�����̈���ł͂�����ł�: https://nim-lang.org/install.html.

```
git clone https://github.com/nim-lang/Nim.git
cd Nim
git clone --depth 1 https://github.com/nim-lang/csources.git
cd csources
sh build.sh
cd ../
bin/nim c koch
./koch boot -d:release
./koch tools # Compile Nimble and other tools.
```

�Ō�ɁA �C���X�g�[�������������� (Windows, Mac  Linux�̏ꍇ��) 
�p�X�� ``bin`` �f�B���N�g����ʂ����Ƃ������߂��܂��B

## Koch
``koch``��Nim�̗l�X�ȕ�����h�L�������g�AWeb�T�C�g�����\�z���邽�߂Ɏg�p�����r���h�c�[���ł��B
``koch``���g�p����Nim�̃e�X�g�����\�z���邱�Ƃ��\�ł��B

Nim��``bin``�f�B���N�g�����p�X�ɒǉ����Ă���Ȃ�A
``./koch tests``�Ńe�X�g�����s�ł��܂��B�e�X�g�ɂ͎��Ԃ�������܂����A
�J�e�S�����w�肵�ăe�X�g���s�����Ƃ��ł��܂��B``./koch tests cat async``

``koch``�ɂ��ďڂ�����[doc/koch.rst](doc/koch.rst) ���Q�Ƃ��Ă��������B

## Nimble

``nimble`` ��Nim�̃p�b�P�[�W�}�l�W���[�ł��B �ڂ�����
[``nim-lang/nimble``][nimble-repo]���Q�Ƃ��Ă�������

## �v����

���̃v���W�F�N�g�́A�v�����邷�ׂĂ̕��X�̂������Ő��藧���Ă��܂��B [Read on to find out how to contribute](#contributing).
<a href="https://github.com/nim-lang/Nim/graphs/contributors"><img src="https://opencollective.com/Nim/contributors.svg?width=890" /></a>

## �v������
[![Backers on Open Collective](https://opencollective.com/nim/backers/badge.svg)](#backers) [![Sponsors on Open Collective](https://opencollective.com/nim/sponsors/badge.svg)](#sponsors)
[![Setup a bounty via Bountysource][badge-nim-bountysource]][nim-bountysource]
[![Donate Bitcoins][badge-nim-bitcoin]][nim-bitcoin]
[![Open Source Helpers](https://www.codetriage.com/nim-lang/nim/badges/users.svg)](https://www.codetriage.com/nim-lang/nim)

�������͂ǂ�ȏ����ȏC���ł����}���܂��B
�W�����C�u�����̃X�y���C������V���ȃ��W���[���̒ǉ��܂ł��ׂĂ����}����A�]������܂��B
�v�����J�n����O�ɁA�ȉ��̃��|�W�g���\���ɂ��ė������Ă����Ă�������:

* ``bin/``, ``build/`` - �����̃f�B���N�g����Nim���r���h����܂ł͋�ł��B
* ``compiler/`` - �R���p�C���̃\�[�X�R�[�h�A�܂�``compiler/nimfix``��``compiler/plugins``�̃R�[�h���܂܂�܂��B
* ``nimsuggest`` - �ȑO�� [``nim-lang/nimsuggest``][nimsuggest-repo] ���|�W�g���ɂ����� nimsuggest �c�[���ł��B 
* ``config/`` - �R���p�C���ƃh�L�������g�W�F�l���[�^�̐ݒ�B
* ``doc/`` - ReStructuredText�`���̃h�L�������g���i�[����Ă��܂��B
* ``lib/`` - �W�����C�u�����A���e:
    * ``pure/`` - Nim�����ŏ����ꂽ���C�u�����B
    * ``impure/`` - Nim�ŏ����ꂽ���̌���Ɉˑ����郉�C�u�����B
    * ``wrappers/`` - �ˑ�����ق��̌���ɂ���ď����ꂽ���C�u�����B
* ``tests/`` - �R���p�C���ƕW�����C�u�����̂��߂̃e�X�g�B
* ``tools/`` - ``niminst`` �� ``nimweb`` ���܂�(���``koch``�o�R�ŌĂяo�����)�B
* ``web/`` - [Nim website][nim-site].
* ``koch.nim`` - Nim��������������c�[���AC�\�[�X�AWeb�T�C�g�A�h�L�������g�𐶐�����c�[���B

�������Ȃ���GitHub��git���g�����v�����N�G�X�g�Ɋ���Ă��Ȃ��Ȃ�:
[������][pull-request-instructions].

�v�����N�G�X�g�𑗐M����O�ɂ��ׂẴe�X�g�ɍ��i���邱�Ƃ����z�I�ł����A���Ԃ�����Ȃ��ꍇ�ɂ�
�ύX�ӏ��ɑΉ������e�X�g���s�������ł��\���܂���B
Travis CI���v�����N�G�X�g���󂯓����O�Ƀe�X�g���܂��B
�����e�X�g�� ``tests/untestable``�ł��B

�v��������@�����T���̏ꍇ��[issue tracker][nim-issues]���������������B
 [``Easy``][nim-issues-easy]���x���̖��͂������񂠂�܂��B
������Nim�ւ̍v���̗ǂ��o���_�ƂȂ�͂��ł��B

��t������Nim�̊J���̎菕�������邱�Ƃ��ł��܂��B��t�͈ȉ�����s�����Ƃ��ł��܂�:

* [Open Collective](https://opencollective.com/nim)
* [Bountysource][nim-bountysource]
* [Bitcoin][nim-bitcoin]

�����₪����܂�����A[Nim�t�H�[����][nim-forum]��IRC[the \#nim channel][nim-irc]�ɂ��񂹂��������B


## �x����

���ӂ��܂�! [[Become a backer](https://opencollective.com/Nim#backer)]

<a href="https://opencollective.com/Nim#backers" target="_blank"><img src="https://opencollective.com/Nim/backers.svg?width=890"></a>


## �X�|���T�[

�X�|���T�[�ɂȂ邱�Ƃł��̃v���W�F�N�g���T�|�[�g���Ă��������B ���S�����Ȃ��̃E�F�u�T�C�g�ւ̃����N�ƂƂ��ɂ����ɕ\������܂��B[[Become a sponsor](https://opencollective.com/Nim#sponsor)]

<a href="https://opencollective.com/Nim/sponsor/0/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/1/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/2/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/3/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/4/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/5/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/6/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/7/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/8/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/9/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/9/avatar.svg"></a>

���E�F�u�T�C�g��[�X�|���T�[�y�[�W](https://nim-lang.org/sponsors.html)�ɂ́A�l�X�Ȏx�����T�[�r�X�̃X�|���T�[/�x���҂̃��X�g���\������܂��B

## ���C�Z���X
�R���p�C���ƕW�����C�u�����́AMIT���C�Z���X�̉��Ń��C�Z���X����Ă��܂��B
���Ȃ킿�ANim�ŊJ�������Ǝ��̃v���O�����Ɍ݊����̂��郉�C�Z���X���g�p���邱�Ƃ��ł��܂��B
Nim���g�p���ď��p�A�v���P�[�V�������J�����邱�Ƃ͖����I�ɋ�����Ă��܂��B

���C�Z���X�ɂ��Ă̏ڍׂ� [copying.txt](copying.txt) �����ǂ݂��������B

Copyright c 2006-2018 Andreas Rumpf, all rights reserved.

Translated by koki Kobayashi 2018.

[nim-site]: https://nim-lang.org
[nim-forum]: https://forum.nim-lang.org
[nim-issues]: https://github.com/nim-lang/Nim/issues
[nim-issues-easy]: https://github.com/nim-lang/Nim/labels/Easy
[nim-irc]: https://webchat.freenode.net/?channels=nim
[nim-travisci]: https://travis-ci.org/nim-lang/Nim
[nim-twitter]: https://twitter.com/nim_lang
[nim-stackoverflow]: https://stackoverflow.com/questions/tagged/nim
[nim-stackoverflow-newest]: https://stackoverflow.com/questions/tagged/nim?sort=newest&pageSize=15
[nim-gitter]: https://gitter.im/nim-lang/Nim
[nim-telegram]: https://t.me/nim_lang
[nim-bountysource]: https://www.bountysource.com/teams/nim
[nim-bitcoin]: https://blockchain.info/address/1BXfuKM2uvoD6mbx4g5xM3eQhLzkCK77tJ
[nimble-repo]: https://github.com/nim-lang/nimble
[nimsuggest-repo]: https://github.com/nim-lang/nimsuggest
[csources-repo]: https://github.com/nim-lang/csources
[badge-nim-travisci]: https://img.shields.io/travis/nim-lang/Nim/devel.svg?style=flat-square
[badge-nim-irc]: https://img.shields.io/badge/chat-on_irc-blue.svg?style=flat-square
[badge-nim-gitter]: https://img.shields.io/badge/chat-on_gitter-blue.svg?style=flat-square
[badge-nim-forum-gethelp]: https://img.shields.io/badge/Forum-get%20help-4eb899.svg?style=flat-square
[badge-nim-twitter]: https://img.shields.io/twitter/follow/nim_lang.svg?style=social
[badge-nim-stackoverflow]: https://img.shields.io/badge/stackoverflow-nim_tag-yellow.svg?style=flat-square
[badge-nim-bountysource]: https://img.shields.io/bountysource/team/nim/activity.svg?style=flat-square
[badge-nim-bitcoin]: https://img.shields.io/badge/bitcoin-1BXfuKM2uvoD6mbx4g5xM3eQhLzkCK77tJ-D69134.svg?style=flat-square
[pull-request-instructions]: https://help.github.com/articles/using-pull-requests/
[nim-wiki]: https://github.com/nim-lang/Nim/wiki
