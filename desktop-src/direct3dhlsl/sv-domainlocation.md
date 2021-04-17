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
ms.openlocfilehash: 3c5195881df438c94cdaed7de8484d0df65e4d54
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104365027"
---
# <a name="sv_domainlocation"></a>\_DOMAINLOCATION VA

Define o local no envoltória do ponto de domínio atual que está sendo avaliado.

## <a name="type"></a>Tipo



|        |                |
|--------|----------------|
| Tipo   | Topologia de entrada |
| float2 | patch quádruplo     |
| float3 | Tri patch      |
| float2 | isoline        |



 

## <a name="remarks"></a>Comentários

Esse valor do sistema é necessário.

Essa função tem suporte nos seguintes tipos de sombreadores:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|        |      | x      |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Semântica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




