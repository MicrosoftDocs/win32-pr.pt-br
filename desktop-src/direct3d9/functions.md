---
description: Uma função é o bloco de construção para um sombreador criado no idioma de alto nível. Se você preferir escrever sombreadores em uma linguagem de estilo C em vez de na linguagem de assembly, será melhor escrever funções.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintaxe da função Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9de680f2f892e59f49e1dfd0850a128ca9ba34e2588e416059251d5058c44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297104"
---
# <a name="effect-function-syntax-direct3d-9"></a>Sintaxe da função Effect (Direct3D 9)

Uma função é o bloco de construção para um sombreador criado no idioma de alto nível. Se você preferir escrever sombreadores em uma linguagem de estilo C em vez de na linguagem de assembly, será melhor escrever funções.

## <a name="syntax"></a>Sintaxe


```
type id ( [ parameters ] )  
    { body }
```



As funções não alteram os valores de parâmetro em um efeito.

-   type – qualquer [Referência válida para o tipo HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)
-   id – um nome exclusivo.
-   parâmetros – parâmetros de função.
-   corpo – o corpo da função.

As funções são criadas com base na linguagem de alto nível. Consulte [Referência para HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
