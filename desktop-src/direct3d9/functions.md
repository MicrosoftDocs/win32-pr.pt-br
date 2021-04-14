---
description: Uma função é o bloco de construção de um sombreador criado na linguagem de alto nível. Se você preferir escrever sombreadores em uma linguagem em estilo C em vez de em linguagem de assembly, convém escrever funções.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintaxe da função de efeito (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500264"
---
# <a name="effect-function-syntax-direct3d-9"></a>Sintaxe da função de efeito (Direct3D 9)

Uma função é o bloco de construção de um sombreador criado na linguagem de alto nível. Se você preferir escrever sombreadores em uma linguagem em estilo C em vez de em linguagem de assembly, convém escrever funções.

## <a name="syntax"></a>Syntax


```
type id ( [ parameters ] )  
    { body }
```



As funções não alteram valores de parâmetro em um efeito.

-   tipo-qualquer [referência válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) o tipo HLSL.
-   ID-um nome exclusivo.
-   parâmetros-parâmetros de função.
-   corpo-o corpo da função.

As funções são criadas a partir da linguagem de alto nível. Consulte [a referência para HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
