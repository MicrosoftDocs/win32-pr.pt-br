---
description: As constantes de sinalizadores globais são usadas para habilitar ou desabilitar as opções de política de energia do usuário.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Constantes de sinalizadores globais (PowrProf.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2dfd23559959bee72e8572cc700a948df1e92dcdb37a03c41b52cdca4d578c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143520"
---
# <a name="global-flags-constants"></a>Constantes de sinalizadores globais

As constantes de sinalizadores globais são usadas para habilitar ou desabilitar as opções de política de energia do usuário.



| Constante/valor                                                                                                                                                                                                                                                                                         | Descrição                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt> </dl> | Habilita ou desabilita a exibição de várias bateria no Power Meter do sistema.<br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <dt>**EnablePasswordLogon**</dt> <dt>0x04</dt> </dl>                         | Habilita ou desabilita a necessidade de logon de senha quando o sistema é retomado do modo de espera ou hibernação.<br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt> </dl> | Habilita ou desabilita o ícone de medidor de bateria na bandeja do sistema. Quando esse sinalizador é limpo, o ícone de medidor de bateria não é exibido.<br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt> </dl>                 | Habilita ou desabilita o suporte para esmaecimento da exibição de vídeo quando o sistema muda de execução na energia ac para em execução na energia da bateria.<br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <dt>**EnableWakeOnRing**</dt> <dt>0x08</dt> </dl>                                     | Habilita ou desabilita o suporte de a wake on ring.<br/>                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>PowrProf.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**POLÍTICA DE \_ \_ ENERGIA DO USUÁRIO \_ GLOBAL**](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




