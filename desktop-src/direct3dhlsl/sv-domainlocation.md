---
title: SV_DomainLocation
description: Define o local no envoltória do ponto de domínio atual que está sendo avaliado.
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb9265734663881981f1626db6e23c6b7dd9415a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996503"
---
# <a name="sv_domainlocation"></a>\_DOMAINLOCATION VA

Define o local no envoltória do ponto de domínio atual que está sendo avaliado.

## <a name="type"></a>Digite



|        |                |
|--------|----------------|
| Digite   | Topologia de entrada |
| float2 | patch quádruplo     |
| float3 | Tri patch      |
| float2 | isoline        |



 

## <a name="remarks"></a>Comentários

Esse valor do sistema é necessário.

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domain | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      | x      |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Semântica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




