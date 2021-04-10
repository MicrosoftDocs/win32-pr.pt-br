---
title: Constantes de reconhecimento de fala (Ctffunc. h)
description: Os valores a seguir são usados com o serviço de texto de reconhecimento de fala.
ms.assetid: ac433d15-738a-46ab-8f69-0fbfb6a8b654
topic_type:
- apiref
api_name:
- TF_DICTATION_ON
- TF_DICTATION_ENABLED
- TF_COMMANDING_ENABLED
- TF_COMMANDING_ON
- TF_SPEECHUI_SHOWN
- TF_SHOW_BALLOON
- TF_DISABLE_BALLOON
- TF_DISABLE_SPEECH
- TF_DISABLE_DICTATION
- TF_DISABLE_COMMANDING
api_location:
- Ctffunc.h
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04c9cfd340e79415d12202765a8db1578abba74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085231"
---
# <a name="speech-recognition-constants"></a>Constantes de reconhecimento de fala

Os valores a seguir são usados com o serviço de texto de reconhecimento de fala.



| Constante/valor                                                                                                                                                                                                                                         | Descrição                                                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DICTATION_ON"></span><span id="tf_dictation_on"></span><dl> <dt>**TF \_ DITAdo \_ em**</dt> <dt>0x00000001</dt> </dl>                   | Se esse bit for 1, o ditado de fala estará ativo. Caso contrário, o ditado de fala ficará inativo. Esse valor não pode ser combinado com o \_ comando TF \_ em. Usado com o compartimento de [ \_ DICTATIONSTAT de \_ fala \_ do compartimento GUID](predefined-compartments.md) .<br/> |
| <span id="TF_DICTATION_ENABLED"></span><span id="tf_dictation_enabled"></span><dl> <dt>**TF \_ DITAdo \_ habilitado**</dt> , <dt>0x00000002</dt> </dl>    | Se esse bit for 1, o ditado de fala será habilitado. Caso contrário, o ditado de fala será desabilitado. Usado com o compartimento de [ \_ DICTATIONSTAT de \_ fala \_ do compartimento GUID](predefined-compartments.md) .<br/>                                                       |
| <span id="TF_COMMANDING_ENABLED"></span><span id="tf_commanding_enabled"></span><dl> <dt>**TF \_ COMANDO \_ habilitado**</dt> <dt>0x00000004</dt> </dl> | Se esse bit for 1, o comando de fala estará habilitado. Caso contrário, o comando de fala será desabilitado. Usado com o compartimento de [ \_ DICTATIONSTAT de \_ fala \_ do compartimento GUID](predefined-compartments.md) .<br/>                                                           |
| <span id="TF_COMMANDING_ON"></span><span id="tf_commanding_on"></span><dl> <dt>**TF \_ COMANDO \_ em**</dt> <dt>0x00000008</dt> </dl>                | Se esse bit for 1, o comando de fala estará ativo. Caso contrário, o comando de fala ficará inativo. Esse valor não pode ser combinado com o \_ ditado \_ de TF ativado. Usado com o compartimento de [ \_ DICTATIONSTAT de \_ fala \_ do compartimento GUID](predefined-compartments.md) .<br/>      |
| <span id="TF_SPEECHUI_SHOWN"></span><span id="tf_speechui_shown"></span><dl> <dt>**TF \_ SPEECHUI \_ mostrado**</dt> <dt>0x00000010</dt> </dl>             | Não usado no momento.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SHOW_BALLOON"></span><span id="tf_show_balloon"></span><dl> <dt>**TF \_ Mostrar \_ balão**</dt> <dt>0x00000001</dt> </dl>                   | Não usado no momento. Usado com o compartimento de [ \_ \_ \_ \_ status da interface do usuário de fala do compartimento GUID](predefined-compartments.md) .<br/>                                                                                                                              |
| <span id="TF_DISABLE_BALLOON"></span><span id="tf_disable_balloon"></span><dl> <dt>**TF \_ DESABILITAR \_ balão**</dt> <dt>0x00000002</dt> </dl>          | Se esse bit for 1, a exibição de balão para o modo de fala atual será desabilitada. Caso contrário, a exibição de balão para o modo de fala atual será habilitada. Usado com o compartimento de [ \_ \_ \_ \_ status da interface do usuário de fala do compartimento GUID](predefined-compartments.md) .<br/>    |
| <span id="TF_DISABLE_SPEECH"></span><span id="tf_disable_speech"></span><dl> <dt>**TF \_ DESABILITAR a \_ fala**</dt> <dt>0x00000001</dt> </dl>             | Se esse bit for 1, a entrada de fala será desabilitada. Caso contrário, a entrada de fala será habilitada. Usado com o compartimento de [ \_ \_ fala \_ desabilitada do compartimento de GUID](predefined-compartments.md) .<br/>                                                                    |
| <span id="TF_DISABLE_DICTATION"></span><span id="tf_disable_dictation"></span><dl> <dt>**TF \_ DESABILITAR \_ ditado**</dt> <dt>0x00000002</dt> </dl>    | Se esse bit for 1, o ditado de fala será desabilitado. Caso contrário, o ditado de fala será habilitado. Usado com o compartimento de [ \_ \_ fala \_ desabilitada do compartimento de GUID](predefined-compartments.md) .<br/>                                                            |
| <span id="TF_DISABLE_COMMANDING"></span><span id="tf_disable_commanding"></span><dl> <dt>**TF \_ DESABILITAR \_ comando**</dt> <dt>0x00000004</dt> </dl> | Se esse bit for 1, o comando de fala será desabilitado. Caso contrário, o comando de fala estará habilitado. Usado com o compartimento de [ \_ \_ fala \_ desabilitada do compartimento de GUID](predefined-compartments.md) .<br/>                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                    |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                                                                                         |
| parâmetro<br/>                   | <dl> <dt>Ctffunc. h; </dt> <dt>Msctf. h</dt> </dl>     |
| INSERI<br/>                      | <dl> <dt>Ctffunc. idl; </dt> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Compartimentos predefinidos](predefined-compartments.md)
</dt> </dl>

 

 





