---
title: Método DownloadItem. getItemInfo
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método getItemInfo recupera o valor de um atributo para o item de download.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, classe DownloadItem
- Classe DownloadItem Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783614"
---
# <a name="downloaditemgetiteminfo-method"></a><span data-ttu-id="81097-108">Método DownloadItem. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="81097-108">DownloadItem.getItemInfo method</span></span>

> [!Note]  
> <span data-ttu-id="81097-109">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="81097-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="81097-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="81097-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="81097-111">O método **getItemInfo** recupera o valor de um atributo para o item de download.</span><span class="sxs-lookup"><span data-stu-id="81097-111">The **getItemInfo** method retrieves the value of an attribute for the download item.</span></span>

## <a name="syntax"></a><span data-ttu-id="81097-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81097-112">Syntax</span></span>


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a><span data-ttu-id="81097-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81097-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81097-114">*ItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81097-114">*itemname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81097-115">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="81097-115">**String** containing the attribute name.</span></span> <span data-ttu-id="81097-116">Os valores com suporte são AlbumArtist, álbum, Duration, WM/provedor, title, userrating e WM/TrackNumber.</span><span class="sxs-lookup"><span data-stu-id="81097-116">Supported values are AlbumArtist, Album, Duration, WM/Provider, Title, UserRating, and WM/TrackNumber.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81097-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81097-117">Return value</span></span>

<span data-ttu-id="81097-118">Esse método retorna uma **cadeia de caracteres** que contém o valor do atributo especificado por *ItemName*.</span><span class="sxs-lookup"><span data-stu-id="81097-118">This method returns a **String** containing the value of the attribute specified by *itemname*.</span></span>

## <a name="remarks"></a><span data-ttu-id="81097-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="81097-119">Remarks</span></span>

<span data-ttu-id="81097-120">Esse método recupera atributos especificados usando a cadeia de caracteres de descrição BITS.</span><span class="sxs-lookup"><span data-stu-id="81097-120">This method retrieves attributes specified using the BITS description string.</span></span> <span data-ttu-id="81097-121">Consulte a [Convenção de trabalho bits do Windows Media Player](windows-media-player-bits-job-convention.md).</span><span class="sxs-lookup"><span data-stu-id="81097-121">See [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md).</span></span>

<span data-ttu-id="81097-122">Esse método tem suporte para download em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="81097-122">This method is supported for background downloading.</span></span> <span data-ttu-id="81097-123">Seu código não deve chamar esse método ao usar o download em tempo real.</span><span class="sxs-lookup"><span data-stu-id="81097-123">Your code should not call this method when using real-time downloading.</span></span>

<span data-ttu-id="81097-124">Esse método pode recuperar informações para trabalhos BITS adicionados somente durante a sessão atual do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="81097-124">This method can retrieve information for BITS jobs added during the current Windows Media Player session only.</span></span>

## <a name="requirements"></a><span data-ttu-id="81097-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81097-125">Requirements</span></span>



| <span data-ttu-id="81097-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="81097-126">Requirement</span></span> | <span data-ttu-id="81097-127">Valor</span><span class="sxs-lookup"><span data-stu-id="81097-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81097-128">Versão</span><span class="sxs-lookup"><span data-stu-id="81097-128">Version</span></span><br/> | <span data-ttu-id="81097-129">Windows Media Player 10 ou posterior</span><span class="sxs-lookup"><span data-stu-id="81097-129">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="81097-130">DLL</span><span class="sxs-lookup"><span data-stu-id="81097-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="81097-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81097-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81097-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="81097-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81097-133">**DownloadItem. Type**</span><span class="sxs-lookup"><span data-stu-id="81097-133">**DownloadItem.type**</span></span>](downloaditem-type.md)
</dt> <dt>

[<span data-ttu-id="81097-134">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="81097-134">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





