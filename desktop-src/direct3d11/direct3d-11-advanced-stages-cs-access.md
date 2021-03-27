---
title: Acessando recursos
description: Há várias maneiras de acessar os recursos.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988687"
---
# <a name="accessing-resources"></a>Acessando recursos

Há várias maneiras de acessar os [recursos](overviews-direct3d-11-resources-types.md). Independentemente, as garantias de Direct3D retornarão zero para qualquer recurso que seja acessado fora dos limites.

-   [Acesso por deslocamento de byte](#access-by-byte-offset)
-   [Acesso por índice](#access-by-index)
-   [Acesso por método MIPS](#access-by-mips-method)
-   [Tópicos relacionados](#related-topics)

## <a name="access-by-byte-offset"></a>Acesso por deslocamento de byte

Dois novos tipos de buffer podem ser acessados usando um deslocamento de byte:

-   [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) é um buffer somente leitura.
-   [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) é um buffer de leitura ou gravação.

## <a name="access-by-index"></a>Acesso por índice

Os tipos de recursos podem usar um índice para fazer referência a um local específico no recurso. Considere este exemplo:


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



Este exemplo atribui os 4 valores float que são armazenados no Texel localizado na posição *pos* no recurso de textura 2D *MyTexture* para a variável *myvar* .

> [!Note]  
> O padrão para acessar uma textura dessa maneira é o nível de mipmap zero (o nível mais detalhado).

 

> [!Note]  
> A linha "FLOAT4 myVar = MyTexture \[ pos \] ;" é equivalente a "FLOAT4 myvar = mytextura. Load (uint3 (POS, 0));". O acesso por índice é um novo aprimoramento de sintaxe de HLSL.

 

> [!Note]  
> O compilador na versão de junho de 2010 do SDK do DirectX e posterior permite que você Indexe todos os tipos de recursos, exceto os [buffers de endereço de byte](direct3d-11-advanced-stages-cs-resources.md).

 

> [!Note]  
> O compilador de junho de 2010 e posterior permite que você declare variáveis de recurso locais. Você pode atribuir recursos definidos globalmente (como *MyTexture*) a essas variáveis e usá-las da mesma maneira que suas contrapartes globais.

 

## <a name="access-by-mips-method"></a>Acesso por método MIPS

Os objetos de textura têm um método **MIPS** (por exemplo, [**Texture2D. MIPS**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), que pode ser usado para especificar o nível de mipmap. Este exemplo lê a cor armazenada em (7, 16) no mipmap nível 2 em uma textura 2D:


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



Esse é um aprimoramento do compilador de junho de 2010 e posterior. A expressão "MyTexture. MIPS \[ 2 \] \[ uint2 (x, y) \] " é equivalente a "mytextura. Load (uint3 (x, y, 2))".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do sombreador de computação](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 