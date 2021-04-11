---
title: Constantes de TF_MOD_ (msctf. h)
description: O TF \_ mod \_ \ Constants especifica os modificadores de chave na \_ estrutura TF PRESERVEDKEY.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009329"
---
# <a name="tf_mod_-constants"></a>Constantes de TF \_ mod \_ \*

As \_ constantes TF mod \_ \* especificam modificadores de chave na estrutura [TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .



| Constante/valor                                                                                                                                                                                                                                                      | Descrição                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <dt>**TF \_ MOD \_ ALT**</dt> <dt>0x0001</dt> </dl>                                                   | Uma das teclas ALT é pressionada<br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <dt>**TF \_ 0x0002 de \_ controle mod**</dt> <dt></dt> </dl>                                       | Uma das teclas CTRL é pressionada<br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <dt>**TF \_ MOD \_ Shift**</dt> <dt>0x0004</dt> </dl>                                             | Uma das teclas SHIFT é pressionada<br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <dt>**TF \_ MOD \_ Ralt**</dt> <dt>0x0008</dt> </dl>                                                | A tecla ALT direita é pressionada<br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <dt>**TF \_ MOD \_ RCONTROL**</dt> <dt>0x0010</dt> </dl>                                    | A tecla CTRL direita é pressionada<br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <dt>**TF \_ MOD \_ RSHIFT**</dt> <dt>0x0020</dt> </dl>                                          | A tecla SHIFT direita é pressionada<br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <dt>**TF \_ MOD \_ LALT**</dt> <dt>0x0040</dt> </dl>                                                | A tecla ALT esquerda é pressionada<br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <dt>**TF \_ MOD \_ LCONTROL**</dt> <dt>0x0080</dt> </dl>                                    | A tecla CTRL esquerda é pressionada<br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <dt>**TF \_ MOD \_ LSHIFT**</dt> <dt>0x0100</dt> </dl>                                          | A tecla SHIFT esquerda é pressionada<br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <dt>**TF \_ MOD \_ em \_**</dt> <dt>0x0200</dt> KEYUP </dl>                                   | O evento será acionado quando a chave for liberada. Sem esse sinalizador, o evento é acionado quando a tecla é pressionada.<br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <dt>**TF \_ MOD \_ ignorar \_ todos os 0x0400 \_ modificadores**</dt> <dt></dt> </dl> | O estado das teclas ALT, CTRL e SHIFT é ignorado. Isso significa que o evento será acionado quando a tecla virtual for pressionada, independentemente de quais teclas modificadoras forem pressionadas.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





