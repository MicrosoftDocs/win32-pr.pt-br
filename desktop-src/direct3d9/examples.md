---
description: Seguem dois exemplos de definições de modelo binário e um exemplo de objeto de dados binários.
ms.assetid: vs|directx_sdk|~\examples.htm
title: Exemplos (gráficos do Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fbb8cbe45881243e17f80fd302c0fb4640685
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087596"
---
# <a name="examples-direct3d-9-graphics"></a><span data-ttu-id="0d888-103">Exemplos (gráficos do Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0d888-103">Examples (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="0d888-104">Seguem dois exemplos de definições de modelo binário e um exemplo de objeto de dados binários.</span><span class="sxs-lookup"><span data-stu-id="0d888-104">Two example binary template definitions and an example of a binary data object follow.</span></span>

> [!Note]  
> <span data-ttu-id="0d888-105">Os dados são armazenados no formato little-endian, que não é mostrado nesses exemplos.</span><span class="sxs-lookup"><span data-stu-id="0d888-105">Data is stored in little-endian format, which is not shown in these examples.</span></span>

 

<span data-ttu-id="0d888-106">O modelo fechado RGB é identificado pelo UUID {55b6d780-37ec-11D0-AB39-0020af71e433} e tem três membros-r, g e b-cada do tipo float.</span><span class="sxs-lookup"><span data-stu-id="0d888-106">The closed template RGB is identified by the UUID {55b6d780-37ec-11d0-ab39-0020af71e433} and has three members - r, g, and b - each of type float.</span></span>


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



<span data-ttu-id="0d888-107">O modelo fechado Matrix4x4 é identificado pelo UUID {55b6d781-37ec-11D0-AB39-0020af71e433} e tem um membro-uma matriz bidimensional chamada Matrix-do tipo float.</span><span class="sxs-lookup"><span data-stu-id="0d888-107">The closed template Matrix4x4 is identified by the UUID {55b6d781-37ec-11d0-ab39-0020af71e433} and has one member - a two-dimensional array named matrix - of type float.</span></span>


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



<span data-ttu-id="0d888-108">O objeto de dados binários a seguir mostra uma instância do modelo RGB definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0d888-108">The binary data object that follows shows an instance of the RGB template defined earlier.</span></span> <span data-ttu-id="0d888-109">O objeto de exemplo é denominado Blue e seus três membros-r, g e b-têm os valores 0,0, 0,0 e 1,0, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0d888-109">The example object is named blue, and its three members - r, g, and b - have the values 0.0, 0.0, and 1.0, respectively.</span></span>


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a><span data-ttu-id="0d888-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d888-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d888-111">Codificação binária</span><span class="sxs-lookup"><span data-stu-id="0d888-111">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



