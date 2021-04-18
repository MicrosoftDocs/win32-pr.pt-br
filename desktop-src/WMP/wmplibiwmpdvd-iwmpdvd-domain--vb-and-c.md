---
title: Propriedade de domínio IWMPDVD
description: A propriedade Domain Obtém o domínio atual do DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Propriedade de domínio Windows Media Player
- Propriedade de domínio Windows Media Player, interface IWMPDVD
- Interface IWMPDVD do Windows Media Player, propriedade de domínio
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749553"
---
# <a name="iwmpdvddomain-property"></a><span data-ttu-id="5794a-106">IWMPDVD: Propriedade omain de:d</span><span class="sxs-lookup"><span data-stu-id="5794a-106">IWMPDVD::domain property</span></span>

<span data-ttu-id="5794a-107">A propriedade **Domain** Obtém o domínio atual do DVD.</span><span class="sxs-lookup"><span data-stu-id="5794a-107">The **domain** property gets the current domain of the DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="5794a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5794a-108">Syntax</span></span>


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a><span data-ttu-id="5794a-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5794a-109">Property value</span></span>

<span data-ttu-id="5794a-110">Um **System. String** que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5794a-110">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="5794a-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5794a-111">Value</span></span>                                                                                        | <span data-ttu-id="5794a-112">Significado</span><span class="sxs-lookup"><span data-stu-id="5794a-112">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5794a-113"><dt>firstPlay</dt></span><span class="sxs-lookup"><span data-stu-id="5794a-113"><dt>firstPlay</dt></span></span> </dl>         | <span data-ttu-id="5794a-114">Executando a inicialização padrão de um disco de DVD.</span><span class="sxs-lookup"><span data-stu-id="5794a-114">Performing default initialization of a DVD disc.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="5794a-115"><dt>videoManagerMenu</dt></span><span class="sxs-lookup"><span data-stu-id="5794a-115"><dt>videoManagerMenu</dt></span></span> </dl>  | <span data-ttu-id="5794a-116">Exibindo menus para todo o disco. Também conhecido como topMenu para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5794a-116">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="5794a-117">Normalmente chamado de menu de título ou do menu superior.</span><span class="sxs-lookup"><span data-stu-id="5794a-117">Commonly called the title menu or the top menu.</span></span><br/> |
| <dl> <span data-ttu-id="5794a-118"><dt>videoTitleSetMenu</dt></span><span class="sxs-lookup"><span data-stu-id="5794a-118"><dt>videoTitleSetMenu</dt></span></span> </dl> | <span data-ttu-id="5794a-119">Exibindo menus para o conjunto de títulos atual.</span><span class="sxs-lookup"><span data-stu-id="5794a-119">Displaying menus for the current title set.</span></span> <span data-ttu-id="5794a-120">Também conhecido como titleMenu para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5794a-120">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="5794a-121">Normalmente chamado de menu raiz.</span><span class="sxs-lookup"><span data-stu-id="5794a-121">Commonly called the root menu.</span></span><br/>          |
| <dl> <span data-ttu-id="5794a-122"><dt>title</dt></span><span class="sxs-lookup"><span data-stu-id="5794a-122"><dt>title</dt></span></span> </dl>             | <span data-ttu-id="5794a-123">Normalmente, exibindo o título atual.</span><span class="sxs-lookup"><span data-stu-id="5794a-123">Usually, displaying the current title.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="5794a-124"><dt>stop</dt></span><span class="sxs-lookup"><span data-stu-id="5794a-124"><dt>stop</dt></span></span> </dl>              | <span data-ttu-id="5794a-125">O navegador de DVD está no domínio de parada de DVD.</span><span class="sxs-lookup"><span data-stu-id="5794a-125">The DVD Navigator is in the DVD Stop domain.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="5794a-126"><dt>indefinido</dt></span><span class="sxs-lookup"><span data-stu-id="5794a-126"><dt>undefined</dt></span></span> </dl>         | <span data-ttu-id="5794a-127">O Windows Media Player não está em nenhum domínio de DVD.</span><span class="sxs-lookup"><span data-stu-id="5794a-127">Windows Media Player is not in any DVD domain.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="5794a-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="5794a-128">Remarks</span></span>

<span data-ttu-id="5794a-129">Cada DVD é criado de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="5794a-129">Every DVD is authored differently.</span></span> <span data-ttu-id="5794a-130">Alguns DVDs não contêm os domínios firstPlay, videoManagerMenu ou videoTitleSetMenu.</span><span class="sxs-lookup"><span data-stu-id="5794a-130">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="5794a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5794a-131">Requirements</span></span>



| <span data-ttu-id="5794a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5794a-132">Requirement</span></span> | <span data-ttu-id="5794a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5794a-133">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5794a-134">Versão</span><span class="sxs-lookup"><span data-stu-id="5794a-134">Version</span></span><br/>   | <span data-ttu-id="5794a-135">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5794a-135">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5794a-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="5794a-136">Namespace</span></span><br/> | <span data-ttu-id="5794a-137">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5794a-137">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5794a-138">Assembly</span><span class="sxs-lookup"><span data-stu-id="5794a-138">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5794a-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5794a-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5794a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="5794a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5794a-141">**Interface IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5794a-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





