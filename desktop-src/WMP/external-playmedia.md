---
title: Método external. playMedia
description: Esta página documenta um recurso do SDK do Windows Media Player 9 Series e do SDK do Windows Media Player 10. Ele pode não estar disponível em versões subsequentes.
ms.assetid: 48071318-e853-4139-8fe4-17d1cdbef8f5
keywords:
- método playMedia Windows Media Player
- método playMedia Windows Media Player, classe externa
- Classe externa Windows Media Player, método playMedia
topic_type:
- apiref
api_name:
- External.playMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0330e7e68d8b4e3747c019e0841f872d279c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789540"
---
# <a name="externalplaymedia-method"></a><span data-ttu-id="497dd-107">Método external. playMedia</span><span class="sxs-lookup"><span data-stu-id="497dd-107">External.playMedia method</span></span>

<span data-ttu-id="497dd-108">Esta página documenta um recurso do SDK do Windows Media Player 9 Series e do SDK do Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="497dd-108">This page documents a feature of the Windows Media Player 9 Series SDK and the Windows Media Player 10 SDK.</span></span> <span data-ttu-id="497dd-109">Ele pode não estar disponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="497dd-109">It may be unavailable in subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="497dd-110">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="497dd-110">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="497dd-111">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="497dd-111">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="497dd-112">O método **playMedia** especifica a URL de um item de mídia digital a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="497dd-112">The **playMedia** method specifies the URL of a digital media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="497dd-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="497dd-113">Syntax</span></span>


```JScript
External.playMedia(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="497dd-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="497dd-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="497dd-115">*URL* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="497dd-115">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="497dd-116">**Cadeia de caracteres** que especifica a URL do item de mídia digital a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="497dd-116">**String** specifying the URL of the digital media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="497dd-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="497dd-117">Return value</span></span>

<span data-ttu-id="497dd-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="497dd-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="497dd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="497dd-119">Remarks</span></span>

<span data-ttu-id="497dd-120">Esse método só está disponível para páginas da Web hospedadas no recurso de **guia** .</span><span class="sxs-lookup"><span data-stu-id="497dd-120">This method is only available to webpages hosted in the **Guide** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="497dd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="497dd-121">Requirements</span></span>



| <span data-ttu-id="497dd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="497dd-122">Requirement</span></span> | <span data-ttu-id="497dd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="497dd-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="497dd-124">Versão</span><span class="sxs-lookup"><span data-stu-id="497dd-124">Version</span></span><br/> | <span data-ttu-id="497dd-125">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="497dd-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="497dd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="497dd-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="497dd-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="497dd-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="497dd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="497dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="497dd-129">**Objeto externo para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="497dd-129">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





