---
description: O método de menu de exibição exibe o menu especificado na tela.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Método de menu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645971"
---
# <a name="showmenu-method"></a><span data-ttu-id="1610e-103">Método de menu</span><span class="sxs-lookup"><span data-stu-id="1610e-103">ShowMenu Method</span></span>

> [!Note]  
> <span data-ttu-id="1610e-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1610e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1610e-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1610e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1610e-106">O `ShowMenu` método exibe o menu especificado na tela.</span><span class="sxs-lookup"><span data-stu-id="1610e-106">The `ShowMenu` method displays the specified menu on the screen.</span></span>

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a><span data-ttu-id="1610e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1610e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1610e-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span><span class="sxs-lookup"><span data-stu-id="1610e-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span></span>
</dt> <dd>

<span data-ttu-id="1610e-109">Especifica a ID do menu como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="1610e-109">Specifies the menu ID as an Integer.</span></span>



| <span data-ttu-id="1610e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1610e-110">Value</span></span> | <span data-ttu-id="1610e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1610e-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="1610e-112">2</span><span class="sxs-lookup"><span data-stu-id="1610e-112">2</span></span>     | <span data-ttu-id="1610e-113">Título (superior)</span><span class="sxs-lookup"><span data-stu-id="1610e-113">Title (Top)</span></span> |
| <span data-ttu-id="1610e-114">3</span><span class="sxs-lookup"><span data-stu-id="1610e-114">3</span></span>     | <span data-ttu-id="1610e-115">Root</span><span class="sxs-lookup"><span data-stu-id="1610e-115">Root</span></span>        |
| <span data-ttu-id="1610e-116">4</span><span class="sxs-lookup"><span data-stu-id="1610e-116">4</span></span>     | <span data-ttu-id="1610e-117">Subimagem</span><span class="sxs-lookup"><span data-stu-id="1610e-117">Subpicture</span></span>  |
| <span data-ttu-id="1610e-118">5</span><span class="sxs-lookup"><span data-stu-id="1610e-118">5</span></span>     | <span data-ttu-id="1610e-119">Áudio</span><span class="sxs-lookup"><span data-stu-id="1610e-119">Audio</span></span>       |
| <span data-ttu-id="1610e-120">6</span><span class="sxs-lookup"><span data-stu-id="1610e-120">6</span></span>     | <span data-ttu-id="1610e-121">Ângulo</span><span class="sxs-lookup"><span data-stu-id="1610e-121">Angle</span></span>       |
| <span data-ttu-id="1610e-122">7</span><span class="sxs-lookup"><span data-stu-id="1610e-122">7</span></span>     | <span data-ttu-id="1610e-123">Capítulo</span><span class="sxs-lookup"><span data-stu-id="1610e-123">Chapter</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1610e-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1610e-124">Return Value</span></span>

<span data-ttu-id="1610e-125">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1610e-125">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1610e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1610e-126">Remarks</span></span>

<span data-ttu-id="1610e-127">Os nomes de menu de DVD podem ser um pouco confusos.</span><span class="sxs-lookup"><span data-stu-id="1610e-127">DVD menu names can be somewhat confusing.</span></span> <span data-ttu-id="1610e-128">O menu título é outro nome para o menu Gerenciador de vídeo, o menu principal do disco inteiro; em geral, ele lista todos os conjuntos de títulos de vídeo disponíveis no disco. O menu raiz é o menu de um conjunto de título de vídeo, que pode conter um título ou um grupo de títulos.</span><span class="sxs-lookup"><span data-stu-id="1610e-128">The title menu is another name for the Video Manager Menu, the main menu for the entire disc; it generally lists all the video title sets available on the disc. The root menu is the menu for one video title set, which can contain one title or a group of titles.</span></span> <span data-ttu-id="1610e-129">Todos os títulos em um conjunto de título compartilham os mesmos menus de subimagem, áudio e ângulo.</span><span class="sxs-lookup"><span data-stu-id="1610e-129">All the titles in a title set share the same Subpicture, Audio, and Angle menus.</span></span>

 

 



