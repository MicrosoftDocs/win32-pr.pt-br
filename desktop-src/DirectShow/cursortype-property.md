---
description: A propriedade CursorType define ou recupera o tipo de cursor atual.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Propriedade CursorType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825800"
---
# <a name="cursortype-property"></a><span data-ttu-id="5dedf-103">Propriedade CursorType</span><span class="sxs-lookup"><span data-stu-id="5dedf-103">CursorType Property</span></span>

> [!Note]  
> <span data-ttu-id="5dedf-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5dedf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5dedf-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5dedf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5dedf-106">A `CursorType` propriedade define ou recupera o tipo de cursor atual.</span><span class="sxs-lookup"><span data-stu-id="5dedf-106">The `CursorType` property sets or retrieves the current cursor type.</span></span>

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a><span data-ttu-id="5dedf-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5dedf-107">Return Value</span></span>

<span data-ttu-id="5dedf-108">Retorna um valor inteiro que representa o tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="5dedf-108">Returns an integer value representing the cursor type.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dedf-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dedf-109">Remarks</span></span>

<span data-ttu-id="5dedf-110">Os valores possíveis para essa propriedade são:</span><span class="sxs-lookup"><span data-stu-id="5dedf-110">The possible values for this property are:</span></span>



| <span data-ttu-id="5dedf-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5dedf-111">Value</span></span> | <span data-ttu-id="5dedf-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5dedf-112">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="5dedf-113">0</span><span class="sxs-lookup"><span data-stu-id="5dedf-113">0</span></span>     | <span data-ttu-id="5dedf-114">Seta</span><span class="sxs-lookup"><span data-stu-id="5dedf-114">Arrow</span></span>       |
| <span data-ttu-id="5dedf-115">1</span><span class="sxs-lookup"><span data-stu-id="5dedf-115">1</span></span>     | <span data-ttu-id="5dedf-116">Ampliar</span><span class="sxs-lookup"><span data-stu-id="5dedf-116">Zoom In</span></span>     |
| <span data-ttu-id="5dedf-117">2</span><span class="sxs-lookup"><span data-stu-id="5dedf-117">2</span></span>     | <span data-ttu-id="5dedf-118">Reduzir</span><span class="sxs-lookup"><span data-stu-id="5dedf-118">Zoom Out</span></span>    |
| <span data-ttu-id="5dedf-119">3</span><span class="sxs-lookup"><span data-stu-id="5dedf-119">3</span></span>     | <span data-ttu-id="5dedf-120">Existentes</span><span class="sxs-lookup"><span data-stu-id="5dedf-120">Hand</span></span>        |
| <span data-ttu-id="5dedf-121">-1</span><span class="sxs-lookup"><span data-stu-id="5dedf-121">-1</span></span>    | <span data-ttu-id="5dedf-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5dedf-122">None</span></span>        |



 

<span data-ttu-id="5dedf-123">Essa propriedade é de leitura/gravação com um valor padrão de zero.</span><span class="sxs-lookup"><span data-stu-id="5dedf-123">This property is read/write with a default value of zero.</span></span> <span data-ttu-id="5dedf-124">Quando a imagem é ampliada, definir `CursorType` como **mão** (0x3) coloca o aplicativo no modo de arrastar, permitindo que o usuário mova a imagem dentro da área de exibição do vídeo.</span><span class="sxs-lookup"><span data-stu-id="5dedf-124">When the picture is zoomed in, setting `CursorType` to **Hand** (0x3) puts the application into drag mode, enabling the user to move the image inside the video display area.</span></span>

 

 



