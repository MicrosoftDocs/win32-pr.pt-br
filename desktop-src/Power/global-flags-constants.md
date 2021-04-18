---
description: As constantes de sinalizadores globais são usadas para habilitar ou desabilitar opções de política de energia de usuário.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Constantes de sinalizadores globais (PowrProf. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783247"
---
# <a name="global-flags-constants"></a>Constantes de sinalizadores globais

As constantes de sinalizadores globais são usadas para habilitar ou desabilitar opções de política de energia de usuário.



| Constante/valor                                                                                                                                                                                                                                                                                         | Descrição                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt> </dl> | Habilita ou desabilita várias exibições de bateria no medidor de energia do sistema.<br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <dt>**EnablePasswordLogon**</dt> <dt>0x04</dt> </dl>                         | Habilita ou desabilita a exigência de logon de senha quando o sistema é retomado do modo de espera ou hibernação.<br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt> </dl> | Habilita ou desabilita o ícone de medidor de bateria na bandeja do sistema. Quando esse sinalizador é removido, o ícone de medidor de bateria não é exibido.<br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt> </dl>                 | Habilita ou desabilita o suporte para o esmaecimento da tela de vídeo quando o sistema muda de execução em energia CA para em execução com energia da bateria.<br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <dt>**EnableWakeOnRing**</dt> <dt>0x08</dt> </dl>                                     | Habilita ou desabilita o suporte a Wake on Ring.<br/>                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>PowrProf. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_política de \_ energia de usuário global \_**](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




