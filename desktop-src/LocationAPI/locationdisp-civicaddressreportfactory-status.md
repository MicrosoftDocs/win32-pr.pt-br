---
description: O status atual do relatório.
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: Propriedade LocationDisp. CivicAddressReportFactory. status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: ff937b11fbb64e0ec1596f9b3b9d85b33528eb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812923"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a>Propriedade LocationDisp. CivicAddressReportFactory. status

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

O status atual do relatório.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a>Valor da propriedade

Esta propriedade é um **número** somente leitura (sem sinal).



| Status                                                                                               | Significado                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Relatório sem suporte.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Erro.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Acesso negado.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Inicializando.<br/>         |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | Running.<br/>              |



 

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar essa propriedade, consulte [escutando eventos de relatório de endereço cívico](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

