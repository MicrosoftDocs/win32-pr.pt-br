---
title: GetSamplePosition (objeto de textura DirectX HLSL)
description: Obtém a posição do exemplo especificado.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365189"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (objeto de textura DirectX HLSL)

Obtém a posição do exemplo especificado.



|                                        |
|----------------------------------------|
| Objeto Ret. GetSamplePosition (int s); |



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                           | Descrição                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*<br/> | Um Texture2DMS ou um tipo de [objeto de textura](dx-graphics-hlsl-to-type.md) Texture2DMSArray.<br/> |
| <span id="s"></span><span id="S"></span>*&*<br/>                                         | \[no \] índice de exemplo baseado em zero.<br/>                                                      |



 

## <a name="return-value"></a>Valor Retornado

Retorna a posição de exemplo (x, y), um vetor de ponto flutuante de dois componentes.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.

## <a name="remarks"></a>Comentários

Um sombreador de pixel pode ser avaliado com frequência de exemplo (execute um sombreador de pixel uma vez por amostra) ou em frequência de pixel (execute um sombreador de pixel uma vez por pixel). Anexe a semântica de SampleIndex da VA \_ a uma entrada de sombreador de pixel para invocar um sombreador de pixel na frequência de exemplo, o valor de entrada é usado como um índice de exemplo ao fazer amostragem do destino de renderização.

Você pode interpolar uma entrada de sombreador de pixel de várias maneiras. Para interpolar em:

-   Um pixel Center, não use nenhuma semântica.
-   Um exemplo, use a \_ semântica SampleIndex de VA.
-   Um local de centróide, use o modificador de [ \_ centróide](dx-graphics-hlsl-struct.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Textura-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





