---
title: DVD. Domain
description: A propriedade Domain recupera o domínio atual do DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. Domain do Windows Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295767"
---
# <a name="dvddomain"></a><span data-ttu-id="258af-104">DVD. Domain</span><span class="sxs-lookup"><span data-stu-id="258af-104">DVD.domain</span></span>

<span data-ttu-id="258af-105">A propriedade **Domain** recupera o domínio atual do DVD.</span><span class="sxs-lookup"><span data-stu-id="258af-105">The **domain** property retrieves the current domain of the DVD.</span></span>

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a><span data-ttu-id="258af-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="258af-106">Possible Values</span></span>

<span data-ttu-id="258af-107">Essa propriedade é uma **cadeia de caracteres** somente leitura que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="258af-107">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="258af-108">String</span><span class="sxs-lookup"><span data-stu-id="258af-108">String</span></span>            | <span data-ttu-id="258af-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="258af-109">Description</span></span>                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="258af-110">firstPlay</span><span class="sxs-lookup"><span data-stu-id="258af-110">firstPlay</span></span>         | <span data-ttu-id="258af-111">Executando a inicialização padrão de um disco de DVD.</span><span class="sxs-lookup"><span data-stu-id="258af-111">Performing default initialization of a DVD disc.</span></span>                                                                                      |
| <span data-ttu-id="258af-112">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="258af-112">videoManagerMenu</span></span>  | <span data-ttu-id="258af-113">Exibindo menus para todo o disco. Também conhecido como topMenu para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="258af-113">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="258af-114">Normalmente chamado de menu de título ou do menu superior.</span><span class="sxs-lookup"><span data-stu-id="258af-114">Commonly called the title menu or the top menu.</span></span> |
| <span data-ttu-id="258af-115">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="258af-115">videoTitleSetMenu</span></span> | <span data-ttu-id="258af-116">Exibindo menus para o conjunto de títulos atual.</span><span class="sxs-lookup"><span data-stu-id="258af-116">Displaying menus for current title set.</span></span> <span data-ttu-id="258af-117">Também conhecido como titleMenu para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="258af-117">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="258af-118">Normalmente chamado de menu raiz.</span><span class="sxs-lookup"><span data-stu-id="258af-118">Commonly called the root menu.</span></span>              |
| <span data-ttu-id="258af-119">título</span><span class="sxs-lookup"><span data-stu-id="258af-119">title</span></span>             | <span data-ttu-id="258af-120">Geralmente exibindo o título atual.</span><span class="sxs-lookup"><span data-stu-id="258af-120">Usually displaying the current title.</span></span>                                                                                                 |
| <span data-ttu-id="258af-121">parar</span><span class="sxs-lookup"><span data-stu-id="258af-121">stop</span></span>              | <span data-ttu-id="258af-122">O navegador de DVD está no domínio de parada de DVD.</span><span class="sxs-lookup"><span data-stu-id="258af-122">The DVD Navigator is in the DVD Stop domain.</span></span>                                                                                          |
| <span data-ttu-id="258af-123">não definido</span><span class="sxs-lookup"><span data-stu-id="258af-123">undefined</span></span>         | <span data-ttu-id="258af-124">O Player não está em nenhum domínio de DVD.</span><span class="sxs-lookup"><span data-stu-id="258af-124">Player is not in any DVD domain.</span></span>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="258af-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="258af-125">Remarks</span></span>

<span data-ttu-id="258af-126">Cada DVD é criado de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="258af-126">Every DVD is authored differently.</span></span> <span data-ttu-id="258af-127">Alguns DVDs não contêm os domínios firstPlay, videoManagerMenu ou videoTitleSetMenu.</span><span class="sxs-lookup"><span data-stu-id="258af-127">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

<span data-ttu-id="258af-128">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="258af-128">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="258af-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="258af-129">Requirements</span></span>



| <span data-ttu-id="258af-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="258af-130">Requirement</span></span> | <span data-ttu-id="258af-131">Valor</span><span class="sxs-lookup"><span data-stu-id="258af-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="258af-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="258af-132">Minimum supported client</span></span><br/> | <span data-ttu-id="258af-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="258af-133">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="258af-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="258af-134">Minimum supported server</span></span><br/> | <span data-ttu-id="258af-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="258af-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="258af-136">Versão</span><span class="sxs-lookup"><span data-stu-id="258af-136">Version</span></span><br/>                  | <span data-ttu-id="258af-137">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="258af-137">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="258af-138">DLL</span><span class="sxs-lookup"><span data-stu-id="258af-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="258af-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="258af-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="258af-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="258af-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="258af-141">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="258af-141">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





