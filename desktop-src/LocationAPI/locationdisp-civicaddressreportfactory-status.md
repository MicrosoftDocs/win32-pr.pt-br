---
description: Propriedade LocationDisp. CivicAddressReportFactory. status-o status atual do relatório.
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
ms.openlocfilehash: acb5bcfa589139e2c69e75124253f9d9a7b53a87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118494"
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
| <span id="3"></span><dl> <dt>**Beta**</dt> </dl> | Inicializando.<br/>         |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | Running.<br/>              |



 

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar essa propriedade, consulte [escutando eventos de relatório de endereço cívico](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

