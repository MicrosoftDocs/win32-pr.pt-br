---
description: Um metarquivo avançado é uma matriz de registros.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Registros de metarquivo avançados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967667"
---
# <a name="enhanced-metafile-records"></a><span data-ttu-id="aa050-103">Registros de metarquivo avançados</span><span class="sxs-lookup"><span data-stu-id="aa050-103">Enhanced Metafile Records</span></span>

<span data-ttu-id="aa050-104">Um metarquivo avançado é uma matriz de registros.</span><span class="sxs-lookup"><span data-stu-id="aa050-104">An enhanced metafile is an array of records.</span></span> <span data-ttu-id="aa050-105">Um registro de metarquivo é uma estrutura de [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="aa050-105">A metafile record is a variable-length [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) structure.</span></span> <span data-ttu-id="aa050-106">No início de cada registro de metarquivo avançado está uma estrutura [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) , que contém dois membros.</span><span class="sxs-lookup"><span data-stu-id="aa050-106">At the beginning of every enhanced metafile record is an [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) structure, which contains two members.</span></span> <span data-ttu-id="aa050-107">O primeiro membro, iType, identifica o tipo de registro que é, a função GDI cujos parâmetros estão contidos no registro.</span><span class="sxs-lookup"><span data-stu-id="aa050-107">The first member, iType, identifies the record type that is, the GDI function whose parameters are contained in the record.</span></span> <span data-ttu-id="aa050-108">Como as estruturas são variáveis de comprimento, o outro membro, nSize, contém o tamanho do registro.</span><span class="sxs-lookup"><span data-stu-id="aa050-108">Because the structures are variable in length, the other member, nSize, contains the size of the record.</span></span> <span data-ttu-id="aa050-109">Imediatamente após o membro nSize estão os parâmetros restantes, se houver, da função GDI.</span><span class="sxs-lookup"><span data-stu-id="aa050-109">Immediately following the nSize member are the remaining parameters, if any, of the GDI function.</span></span> <span data-ttu-id="aa050-110">O restante da estrutura contém dados adicionais que dependem do tipo de registro.</span><span class="sxs-lookup"><span data-stu-id="aa050-110">The remainder of the structure contains additional data that is dependent on the record type.</span></span>

<span data-ttu-id="aa050-111">O primeiro registro em um metarquivo avançado é sempre a estrutura [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) , que é o cabeçalho Enhanced-Metafile.</span><span class="sxs-lookup"><span data-stu-id="aa050-111">The first record in an enhanced metafile is always the [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) structure, which is the enhanced-metafile header.</span></span> <span data-ttu-id="aa050-112">O cabeçalho especifica as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="aa050-112">The header specifies the following information:</span></span>

-   <span data-ttu-id="aa050-113">Tamanho do metarquivo, em bytes</span><span class="sxs-lookup"><span data-stu-id="aa050-113">Size of the metafile, in bytes</span></span>
-   <span data-ttu-id="aa050-114">Dimensões do quadro de imagem, em unidades de dispositivo</span><span class="sxs-lookup"><span data-stu-id="aa050-114">Dimensions of the picture frame, in device units</span></span>
-   <span data-ttu-id="aa050-115">Dimensões do quadro de imagem, em unidades de 01 a milímetros</span><span class="sxs-lookup"><span data-stu-id="aa050-115">Dimensions of the picture frame, in .01-millimeter units</span></span>
-   <span data-ttu-id="aa050-116">Número de registros no metarquivo</span><span class="sxs-lookup"><span data-stu-id="aa050-116">Number of records in the metafile</span></span>
-   <span data-ttu-id="aa050-117">Deslocamento para uma descrição de texto opcional</span><span class="sxs-lookup"><span data-stu-id="aa050-117">Offset to an optional text description</span></span>
-   <span data-ttu-id="aa050-118">Tamanho da paleta opcional</span><span class="sxs-lookup"><span data-stu-id="aa050-118">Size of the optional palette</span></span>
-   <span data-ttu-id="aa050-119">Resolução do dispositivo original, em pixels</span><span class="sxs-lookup"><span data-stu-id="aa050-119">Resolution of the original device, in pixels</span></span>
-   <span data-ttu-id="aa050-120">Resolução do dispositivo original, em milímetros</span><span class="sxs-lookup"><span data-stu-id="aa050-120">Resolution of the original device, in millimeters</span></span>

<span data-ttu-id="aa050-121">Uma descrição de texto opcional pode seguir o registro de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="aa050-121">An optional text description can follow the header record.</span></span> <span data-ttu-id="aa050-122">A descrição do texto descreve a imagem e o nome do autor.</span><span class="sxs-lookup"><span data-stu-id="aa050-122">The text description describes the picture and the author's name.</span></span> <span data-ttu-id="aa050-123">A paleta opcional especifica as cores usadas para criar o metarquivo avançado.</span><span class="sxs-lookup"><span data-stu-id="aa050-123">The optional palette specifies the colors used to create the enhanced metafile.</span></span> <span data-ttu-id="aa050-124">Os registros restantes identificam as funções GDI usadas para criar a imagem.</span><span class="sxs-lookup"><span data-stu-id="aa050-124">The remaining records identify the GDI functions used to create the picture.</span></span> <span data-ttu-id="aa050-125">A seguinte saída hexadecimal corresponde a um registro gerado para uma chamada para a função [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) .</span><span class="sxs-lookup"><span data-stu-id="aa050-125">The following hexadecimal output corresponds to a record generated for a call to the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function.</span></span>


```C++
00000011 0000000C 00000004 
```



<span data-ttu-id="aa050-126">O valor 0x00000011 especifica o tipo de registro (corresponde à \_ constante EMR SETMAPMODE definida no arquivo WinGDI. h).</span><span class="sxs-lookup"><span data-stu-id="aa050-126">The value 0x00000011 specifies the record type (corresponds to the EMR\_SETMAPMODE constant defined in the file Wingdi.h).</span></span> <span data-ttu-id="aa050-127">O valor 0x0000000C especifica o comprimento do registro, em bytes.</span><span class="sxs-lookup"><span data-stu-id="aa050-127">The value 0x0000000C specifies the length of the record, in bytes.</span></span> <span data-ttu-id="aa050-128">O valor 0x00000004 identifica o modo de mapeamento (corresponde à \_ constante mm LOENGLISH definida na função [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) ).</span><span class="sxs-lookup"><span data-stu-id="aa050-128">The value 0x00000004 identifies the mapping mode (corresponds to the MM\_LOENGLISH constant defined in the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function).</span></span>

<span data-ttu-id="aa050-129">Para obter uma lista de tipos de registro adicionais, consulte [estruturas de metarquivo](metafile-structures.md).</span><span class="sxs-lookup"><span data-stu-id="aa050-129">For a list of additional record types, see [Metafile Structures](metafile-structures.md).</span></span>

 

 



