---
description: Propriedade LocationDisp.CivicAddressReportFactory.Status – o status atual do relatório.
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: Propriedade LocationDisp.CivicAddressReportFactory.Status
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
ms.openlocfilehash: 8ba7d9e26a9741f80caed84d2a4ee4198eae05736aa8dee91019452cc3345ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693116"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a>Propriedade LocationDisp.CivicAddressReportFactory.Status

\[O modelo de objeto da API de Localização está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de Geolocalização do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo da área de trabalho, use o [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

O status atual do relatório.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade é um Número somente **leitura** (sem assinatura longa).



| Status                                                                                               | Significado                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Não há suporte para o relatório.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Erro.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Acesso negado<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Inicializando.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Running.<br/>              |



 

## <a name="examples"></a>Exemplos

Para ver um exemplo de como usar essa propriedade, consulte [Escutando eventos de relatório de endereço civil.](/uwp/api/Windows.Devices.Geolocation)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

