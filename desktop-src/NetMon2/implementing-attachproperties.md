---
description: Chama a função Attachproperties para mapear as propriedades que existem em uma parte dos dados reconhecidos.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implementando Anexaproperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787046"
---
# <a name="implementing-attachproperties"></a><span data-ttu-id="a8513-103">Implementando Anexaproperties</span><span class="sxs-lookup"><span data-stu-id="a8513-103">Implementing AttachProperties</span></span>

<span data-ttu-id="a8513-104">Monitor de Rede chama a função [**attachproperties**](attachproperties.md) para mapear as propriedades que existem em uma parte dos dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="a8513-104">Network Monitor calls the [**AttachProperties**](attachproperties.md) function to map the properties that exist in a piece of recognized data.</span></span> <span data-ttu-id="a8513-105">A função [**attachproperties**](attachproperties.md) mapeia as propriedades para um local específico.</span><span class="sxs-lookup"><span data-stu-id="a8513-105">The [**AttachProperties**](attachproperties.md) function maps the properties to a specific location.</span></span>

<span data-ttu-id="a8513-106">Monitor de Rede usa o processo a seguir para analisar os dados em um quadro.</span><span class="sxs-lookup"><span data-stu-id="a8513-106">Network Monitor uses the following process to parse the data in a frame.</span></span>

-   <span data-ttu-id="a8513-107">Primeiro, Monitor de Rede chama [RecognizeFrame](recognizeframe.md) para reconhecer todos os protocolos existentes em um quadro.</span><span class="sxs-lookup"><span data-stu-id="a8513-107">First, Network Monitor calls [RecognizeFrame](recognizeframe.md) to recognize all the protocols that exist in a frame.</span></span>
-   <span data-ttu-id="a8513-108">Em seguida, Monitor de Rede chama [**anexaproperties**](attachproperties.md) para cada analisador que reconhece uma parte dos dados.</span><span class="sxs-lookup"><span data-stu-id="a8513-108">Then, Network Monitor calls [**AttachProperties**](attachproperties.md) for each parser that recognizes a piece of data.</span></span>

<span data-ttu-id="a8513-109">Quando Monitor de Rede chama a função [attachproperties](attachproperties.md) para os dados reconhecidos, o analisador que é chamado deve analisar os dados e, em seguida, mapear cada propriedade existente para um local nos dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="a8513-109">When Network Monitor calls the [AttachProperties](attachproperties.md) function for the recognized data, the parser that is called must parse the data, and then map each existing property to a location in the recognized data.</span></span> <span data-ttu-id="a8513-110">O analisador determina quais propriedades existem e onde cada propriedade está localizada nos dados.</span><span class="sxs-lookup"><span data-stu-id="a8513-110">The parser determines which properties exist, and where each property is located in the data.</span></span> <span data-ttu-id="a8513-111">A figura a seguir mostra dados reconhecidos pelo analisador.</span><span class="sxs-lookup"><span data-stu-id="a8513-111">The following figure shows parser-recognized data.</span></span>

![dados reconhecidos do analisador](images/attachproperties1.png)

<span data-ttu-id="a8513-113">Durante a implementação de [**attachproperties**](attachproperties.md), você deve chamar uma das funções a seguir para cada propriedade existente em um quadro de dados.</span><span class="sxs-lookup"><span data-stu-id="a8513-113">During the implementation of [**AttachProperties**](attachproperties.md), you must call one of the following functions for each property that exists in a data frame.</span></span>

-   <span data-ttu-id="a8513-114">Chame a função [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) quando desejar modificar os dados de propriedade em um quadro.</span><span class="sxs-lookup"><span data-stu-id="a8513-114">Call the [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function when you want to modify the property data in a frame.</span></span>
-   <span data-ttu-id="a8513-115">Chame a função [**AttachPropertyInstance**](attachpropertyinstance.md) quando não quiser modificar os dados de propriedade em um quadro.</span><span class="sxs-lookup"><span data-stu-id="a8513-115">Call the [**AttachPropertyInstance**](attachpropertyinstance.md) function when you do not want to modify the property data in a frame.</span></span>

> [!Note]  
> <span data-ttu-id="a8513-116">É recomendável que você use os dados como eles existem na captura.</span><span class="sxs-lookup"><span data-stu-id="a8513-116">It is recommended that you use the data as it exists in the capture.</span></span>

 

<span data-ttu-id="a8513-117">O procedimento a seguir identifica as etapas necessárias para implementar [**anexaproperties**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="a8513-117">The following procedure identifies the steps necessary to implement [**AttachProperties**](attachproperties.md).</span></span>

<span data-ttu-id="a8513-118">**Para implementar Anexaproperties**</span><span class="sxs-lookup"><span data-stu-id="a8513-118">**To implement AttachProperties**</span></span>

1.  <span data-ttu-id="a8513-119">Determine quais propriedades existem e o local da propriedade nos dados.</span><span class="sxs-lookup"><span data-stu-id="a8513-119">Determine which properties exist, and the property location in the data.</span></span>
2.  <span data-ttu-id="a8513-120">Chame [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) para cada propriedade com um valor que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="a8513-120">Call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) for each property with a value that you want to modify.</span></span>
3.  <span data-ttu-id="a8513-121">Chame [**AttachPropertyInstance**](attachpropertyinstance.md) para cada propriedade com um valor que você não deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="a8513-121">Call [**AttachPropertyInstance**](attachpropertyinstance.md) for each property with a value that you do not want to modify.</span></span> <span data-ttu-id="a8513-122">Normalmente, essa é a única função que você precisa chamar.</span><span class="sxs-lookup"><span data-stu-id="a8513-122">Typically, this is the only function that you need to call.</span></span>

<span data-ttu-id="a8513-123">A seguir está uma implementação básica de [**attachproperties**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="a8513-123">The following is a basic implementation of [**AttachProperties**](attachproperties.md).</span></span> <span data-ttu-id="a8513-124">Lembre-se de que o exemplo não inclui o código para determinar quais propriedades existem ou o código para localizar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="a8513-124">Be aware that the example does not include either the code to determine which properties exist, or the code to locate the properties.</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



