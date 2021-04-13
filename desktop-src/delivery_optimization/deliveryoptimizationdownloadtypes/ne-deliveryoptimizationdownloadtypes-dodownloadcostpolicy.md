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
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369286"
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
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | DeliveryOptimizationDownloadTypes. h |
