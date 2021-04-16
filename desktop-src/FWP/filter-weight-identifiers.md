---
title: Identificadores de peso de filtro (Fwpmu. h)
description: Filtre os identificadores de peso usados pelo BFE (mecanismo de filtragem base) para computar os pesos de filtro gerados automaticamente.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761739"
---
# <a name="filter-weight-identifiers"></a>Identificadores de peso de filtro

Os identificadores de peso de filtro usados pelo BFE (mecanismo de filtragem base) para computar os pesos de filtro gerados automaticamente são listados abaixo.

Consulte [atribuição de peso de filtro](filter-weight-assignment.md) para obter mais informações sobre a geração de peso de filtro.

<dl> <dt>

<span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**\_bits de \_ peso \_ automático FWPM**
</dt> <dd> <dl> <dt>

(60)
</dt> <dt>



Número de bits usados para pesos de filtro gerados automaticamente.


</dt> </dl> </dd> <dt>

<span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**\_ \_ peso \_ máximo de FWPM**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 4)
</dt> <dt>



Peso máximo de filtro gerado automaticamente.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**
</dt> <dd> <dl> <dt>

(0xC)
</dt> <dt>



O BFE atribui um peso com esse valor de intervalo aos filtros IKE e AuthIP.

Consulte [isenções de Ike/AuthIP](ike-exemptions.md) para obter mais informações sobre filtros Ike/AuthIP.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**\_IPSec de \_ intervalo de peso FWPM \_**
</dt> <dd> <dl> <dt>

(0x0)
</dt> <dt>



O BFE atribui um peso com esse valor de intervalo aos filtros de política IPsec.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**\_intervalo de peso FWPM \_ \_ máximo**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 60)
</dt> <dt>



Valor de intervalo de peso de filtro máximo permitido.


</dt> </dl> </dd> </dl>

> [!Note]  
> **MAXUINT64** representa o maior valor possível de **UINT64**. O valor dessa constante é 0xFFFFFFFFFFFFFFFF.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





