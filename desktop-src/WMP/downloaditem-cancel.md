---
title: Método DownloadItem. Cancel
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método Cancel cancela o download.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- cancelar método Windows Media Player
- método Cancel Windows Media Player, classe DownloadItem
- Classe DownloadItem do Windows Media Player, método Cancel
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760455"
---
# <a name="downloaditemcancel-method"></a><span data-ttu-id="7da10-108">Método DownloadItem. Cancel</span><span class="sxs-lookup"><span data-stu-id="7da10-108">DownloadItem.cancel method</span></span>

> [!Note]  
> <span data-ttu-id="7da10-109">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="7da10-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7da10-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="7da10-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7da10-111">O método **Cancel** cancela o download.</span><span class="sxs-lookup"><span data-stu-id="7da10-111">The **cancel** method cancels the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da10-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7da10-112">Syntax</span></span>


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a><span data-ttu-id="7da10-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7da10-113">Parameters</span></span>

<span data-ttu-id="7da10-114">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7da10-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7da10-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7da10-115">Return value</span></span>

<span data-ttu-id="7da10-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7da10-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7da10-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7da10-117">Remarks</span></span>

<span data-ttu-id="7da10-118">Os itens cancelados não são removidos da coleção de download.</span><span class="sxs-lookup"><span data-stu-id="7da10-118">Cancelled items are not removed from the download collection.</span></span> <span data-ttu-id="7da10-119">Os itens cancelados retornam um valor de **downloadstate** de 4 (cancelado).</span><span class="sxs-lookup"><span data-stu-id="7da10-119">Cancelled items return a **downloadState** value of 4 (canceled).</span></span>

## <a name="requirements"></a><span data-ttu-id="7da10-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7da10-120">Requirements</span></span>



| <span data-ttu-id="7da10-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7da10-121">Requirement</span></span> | <span data-ttu-id="7da10-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7da10-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7da10-123">Versão</span><span class="sxs-lookup"><span data-stu-id="7da10-123">Version</span></span><br/> | <span data-ttu-id="7da10-124">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7da10-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="7da10-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7da10-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7da10-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7da10-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7da10-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7da10-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da10-128">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="7da10-128">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="7da10-129">**DownloadItem. downloadstate**</span><span class="sxs-lookup"><span data-stu-id="7da10-129">**DownloadItem.downloadState**</span></span>](downloaditem-downloadstate.md)
</dt> </dl>

 

 





