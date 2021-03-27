---
title: SV_InnerCoverage
description: '\_A InputCoverage de VA representa informações de rasterização conservadora subestimadas (ou seja, se um pixel é garantido para ser totalmente coberto).'
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
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988700"
---
# <a name="sv_innercoverage"></a>\_INNERCOVERAGE VA

\_A InputCoverage de VA representa informações de rasterização conservadora subestimadas (ou seja, se um pixel é garantido para ser totalmente coberto).

## <a name="type"></a>Tipo



|      |
|------|
| Tipo |
| uint |



 

## <a name="remarks"></a>Comentários

Esse valor gerado pelo sistema é necessário para o suporte de camada 3 e só está disponível nessa camada. Essa entrada é mutuamente exclusiva com \_ cobertura de VA-ambas não podem ser usadas.

Para acessar a \_ InnerCoverage de VA, ela deve ser declarada como um único componente de um dos registros de entrada do sombreador de pixel. O modo de interpolação na declaração deve ser constante (interpolação não se aplica).

A rasterização conservadora está disponível no D3D 11.3 e no D3D12. Consulte:

-   [Rasterização conservadora de D3D 11.3](/windows/desktop/direct3d11/conservative-rasterization)
-   [Rasterização D3D12 conservadora](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Valores de sistema do modelo do sombreador 5,1](shader-model-5-1-system-values.md)
</dt> </dl>

 

 