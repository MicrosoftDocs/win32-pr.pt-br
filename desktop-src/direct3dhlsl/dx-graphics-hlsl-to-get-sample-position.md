---
title: GetSamplePosition (objeto de textura directX HLSL)
description: Obtém a posição do exemplo especificado.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a1e5f4dc71d5af2e7973ef180c919a49e65ef81
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118581"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (objeto de textura directX HLSL)

Obtém a posição do exemplo especificado.

ret Object.GetSamplePosition( int s );



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                           | Descrição                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*<br/> | Um tipo de objeto de textura Texture2DMS ou Texture2DMSArray. [](dx-graphics-hlsl-to-type.md)<br/> |
| <span id="s"></span><span id="S"></span>*s*<br/>                                         | \[em \] O índice de exemplo baseado em zero.<br/>                                                      |



 

## <a name="return-value"></a>Valor Retornado

Retorna a posição de exemplo (x,y), um vetor de ponto flutuante de dois componentes.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   O Modelo de Sombreador 4.1 está disponível no Direct3D 10.1 ou superior.

## <a name="remarks"></a>Comentários

Um sombreador de pixel pode ser avaliado na frequência de exemplo (execute um sombreador de pixel uma vez por amostra) ou na frequência de pixel (execute um sombreador de pixel uma vez por pixel). Anexe a semântica SV SampleIndex a uma entrada de sombreador de pixel para invocar um sombreador de pixel na frequência de exemplo. Em seguida, o valor de entrada é usado como um índice de exemplo ao amostragem do destino de \_ renderização.

Você pode interpolar uma entrada de sombreador de pixel de várias maneiras. Para interpolar em:

-   Um centro de pixels, não use nenhuma semântica.
-   Um exemplo, use a semântica \_ SV SampleIndex.
-   Um local de centroide, use o [ \_ modificador centroide.](dx-graphics-hlsl-struct.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto de textura](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





