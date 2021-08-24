---
title: Enumeração DODownloadCostPolicy
description: Especifica a ID das opções de políticas de custo associadas à propriedade **DODownloadProperty_CostPolicy** .
keywords:
- Enumeração DODownloadCostPolicy, DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 763042ed6d0df6fa287fbe66d23528a199a73041cb3500c6a2812e6db86cb698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677876"
---
# <a name="dodownloadcostpolicy-enumeration"></a>Enumeração DODownloadCostPolicy

A enumeração **DODownloadCostPolicy** especifica a ID das opções de políticas de custo associadas à propriedade **DODownloadProperty_CostPolicy** .

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a>Constantes

| Requisito | Valor |
|-|-|
| DODownloadCostPolicy_Always | O download é executado independentemente do custo. |
| DODownloadCostPolicy_Unrestricted | O download é executado, a menos que o impõe custos ou limites de tráfego. |
| DODownloadCostPolicy_Standard | O download é executado, a menos que não esteja sujeito a uma sobretaxa ou ao próximo esgotamento. |
| DODownloadCostPolicy_NoRoaming | O download é executado, a menos que a conectividade esteja sujeita a sobretaxas de roaming. |
| DODownloadCostPolicy_NoSurcharge | O download é executado, a menos que sujeito a uma sobretaxa. |
| DODownloadCostPolicy_NoCellular | O download é executado, a menos que a rede esteja em celular. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | DeliveryOptimizationDownloadTypes. h |
