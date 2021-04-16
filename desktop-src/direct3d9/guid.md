---
description: Define um GUID que pode ser usado em outros modelos.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: GUID (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500395"
---
# <a name="guid-directx-9"></a><span data-ttu-id="46263-103">GUID (DirectX 9)</span><span class="sxs-lookup"><span data-stu-id="46263-103">Guid (DirectX 9)</span></span>

<span data-ttu-id="46263-104">Define um GUID que pode ser usado em outros modelos.</span><span class="sxs-lookup"><span data-stu-id="46263-104">Defines a GUID that can be used in other templates.</span></span>

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

<span data-ttu-id="46263-105">Onde os parâmetros formam o formato de armazenamento binário para um GUID:</span><span class="sxs-lookup"><span data-stu-id="46263-105">Where the parameters together form the binary storage format for a GUID:</span></span>

-   <span data-ttu-id="46263-106">valor de dados inteiros sem sinal de data1-32-bit</span><span class="sxs-lookup"><span data-stu-id="46263-106">data1 - 32-bit unsigned integer data value</span></span>
-   <span data-ttu-id="46263-107">o valor de dados inteiros sem sinal de data2 de 16 bits</span><span class="sxs-lookup"><span data-stu-id="46263-107">data2 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="46263-108">data3-valor de dados inteiros sem sinal de 16 bits</span><span class="sxs-lookup"><span data-stu-id="46263-108">data3 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="46263-109">data4-uma matriz de caracteres não assinados</span><span class="sxs-lookup"><span data-stu-id="46263-109">data4 - An array of unsigned characters</span></span>

## <a name="see-also"></a><span data-ttu-id="46263-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="46263-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46263-111">Modelos</span><span class="sxs-lookup"><span data-stu-id="46263-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



