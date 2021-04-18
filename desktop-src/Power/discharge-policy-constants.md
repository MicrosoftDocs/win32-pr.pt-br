---
description: A lista a seguir descreve as constantes da política de descarga.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Constantes da política de descarga (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764627"
---
# <a name="discharge-policy-constants"></a>Constantes da política de descarga

A lista a seguir descreve as constantes da política de descarga.



| Constante/valor                                                                                                                                                                                                                                            | Descrição                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <dt>**Descarga \_ POLÍTICA \_ crítica**</dt> <dt>0</dt> </dl> | Quais das configurações de política de descarga da bateria (estruturas do [**\_ \_ nível de energia do sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) são usadas quando a bateria é descarregada abaixo do limite crítico.<br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <dt>**Descarga \_ POLÍTICA \_ baixa**</dt> <dt>1</dt> </dl>                | Qual das configurações de política de descarga da bateria (estruturas do [**\_ \_ nível de energia do sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) é usada quando a bateria é descarregada abaixo do limite baixo.<br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <dt>**Número \_ de \_Políticas de descarga**</dt> <dt>4</dt> </dl>          | Número de configurações de política de descarga da bateria (estruturas de [**\_ \_ nível de energia do sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) especificadas.<br/>                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>WinNT. h (incluir Windows. h)</dt> </dl> |



 

 




