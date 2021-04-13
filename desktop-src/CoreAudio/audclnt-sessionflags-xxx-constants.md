---
description: As \_ constantes AUDCLNT SESSIONFLAGS \_ xxx indicam as características de uma sessão de áudio associada ao fluxo.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: Constantes de AUDCLNT_SESSIONFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457175"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>\_Constantes AUDCLNT SESSIONFLAGS \_ xxx

As \_ constantes AUDCLNT SESSIONFLAGS \_ xxx indicam as características de uma sessão de áudio associada ao fluxo. Um cliente pode especificar essas opções durante a inicialização do fluxo por meio do parâmetro *StreamFlags* do método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .



| Constante/valor                                                                                                                                                                                                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt> </dl>                       | A sessão expira quando não há fluxos associados e proprietário de objetos de controle de sessão que contêm referências.<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ Exibir \_ ocultar**</dt> <dt>0x20000000</dt> </dl>                                     | O controle de volume fica oculto na interface do usuário do mixer de volume quando a sessão de áudio é criada. Se a sessão associada ao fluxo já existir antes de [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) abrir o fluxo, o controle de volume será exibido no mixer de volume.<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **AUDCLNT \_ SESSIONFLAGS \_ exibição \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt> </dl> | O controle de volume fica oculto na interface do usuário do mixer de volume depois que a sessão expira. <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Principais constantes de áudio](core-audio-constants.md)
</dt> <dt>

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




