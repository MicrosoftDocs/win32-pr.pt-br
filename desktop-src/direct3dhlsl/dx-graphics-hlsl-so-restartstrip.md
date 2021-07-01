---
title: RestartStrip (objeto Stream-Output DirectX HLSL)
description: Encerra a faixa primitiva atual e inicia uma nova faixa. Se a faixa atual não tiver vértices suficientes emitidos para preencher a topologia primitiva, o primitivo incompleto no final será Descartado.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120191"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a>RestartStrip (objeto Stream-Output DirectX HLSL)

Encerra a faixa primitiva atual e inicia uma nova faixa. Se a faixa atual não tiver vértices suficientes emitidos para preencher a topologia primitiva, o primitivo incompleto no final será Descartado.

RestartStrip();



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                     | Descrição |
|------------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>**None**<br/> |             |



 

## <a name="return-value"></a>Valor Retornado

Nenhum

## <a name="remarks"></a>Comentários

Um corte de faixa faz com que a faixa atual termine e uma nova faixa seja iniciada. Uma faixa de corte pode ser feita chamando explicitamente esse método ou apenas renderizando até o valor de índice máximo (1, que é 0xFFFFFFFF para índices de 32 bits ou 0xFFFF para índices de 16 bits). Cada instância de um desenho de instância indexada gera um corte automático de uma faixa. Isso é verdadeiro mesmo que a topologia não seja uma faixa de triângulo.

> [!Note]  
> O suporte para reinicialização e o 1 ' valor mágico ' para um recorte só está disponível no [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 ou dispositivos superiores.

 

A saída é sempre considerada uma faixa de triângulo. Para fazer a saída de uma lista de triângulos, você deve chamar RestartStrip entre cada triângulo. Não há suporte para ventiladores de triângulo.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | yes       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fluxo-objeto de saída](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

