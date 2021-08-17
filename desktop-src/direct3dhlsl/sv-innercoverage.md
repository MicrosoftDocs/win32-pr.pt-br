---
title: SV_InnerCoverage
description: SV InputCoverage representa informações de rasterização falsas (ou seja, se um pixel tem garantia de \_ ser totalmente coberto).
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172ee60cb85e69568c8cb226aa19fa325686726f42fc27c7aa21231b1a55ef28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724374"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

SV InputCoverage representa informações de rasterização falsas (ou seja, se um pixel tem garantia de \_ ser totalmente coberto).

## <a name="type"></a>Tipo



| Tipo     |
|------|
| uint |



 

## <a name="remarks"></a>Comentários

Esse valor gerado pelo sistema é necessário para suporte de camada 3 e só está disponível nessa camada. Essa entrada é mutuamente exclusiva com a Cobertura SV \_ – ambas não podem ser usadas.

Para acessar o InnerCoverage SV, ele deve ser declarado como um único componente de um dos registros de entrada \_ do sombreador de pixel. O modo de interpolação na declaração deve ser constante (a interpolação não se aplica).

A rasterização conservadora está disponível em D3D11.3 e D3D12. Consulte:

-   [D3D11.3 Rasterização conservadora](/windows/desktop/direct3d11/conservative-rasterization)
-   [D3D12 Rasterização conservadora](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Valores do sistema do Modelo de Sombreador 5.1](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
