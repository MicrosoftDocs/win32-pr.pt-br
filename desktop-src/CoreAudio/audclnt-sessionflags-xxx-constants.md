---
description: As \_ constantes AUDCLNT SESSIONFLAGS XXX indicam características de uma sessão de áudio \_ associada ao fluxo.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: AUDCLNT_SESSIONFLAGS_XXX constantes (Audiosessiontypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15423d24d48a98b69c4ab1651941fba639885c03e27cf9df8b1834aab830bb6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018494"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>Constantes AUDCLNT \_ SESSIONFLAGS \_ XXX

As \_ constantes AUDCLNT SESSIONFLAGS XXX indicam características de uma sessão de áudio \_ associada ao fluxo. Um cliente pode especificar essas opções durante a inicialização do fluxo por meio do parâmetro *StreamFlags* do [**método IAudioClient::Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)



| Constante/valor                                                                                                                                                                                                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0X10000000</dt> </dl>                       | A sessão expira quando não há fluxos associados e objetos de controle de sessão que têm referências.<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <dt>**AUDCLNT \_ EXIBIÇÃO SESSIONFLAGS \_ \_ OCULTAR**</dt> <dt>0X20000000</dt> </dl>                                     | O controle de volume fica oculto na interface do usuário do mixer de volume quando a sessão de áudio é criada. Se a sessão associada ao fluxo já existir antes [**de IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) abrir o fluxo, o controle de volume será exibido no mixer de volume.<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **AUDCLNT \_ SESSIONFLAGS \_ DISPLAY \_ HIDEWHENEXPIRED**</dt> <dt>0X40000000</dt> </dl> | O controle de volume fica oculto na interface do usuário do mixer de volume depois que a sessão expira. <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Audiosessiontypes.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de áudio principais](core-audio-constants.md)
</dt> <dt>

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




