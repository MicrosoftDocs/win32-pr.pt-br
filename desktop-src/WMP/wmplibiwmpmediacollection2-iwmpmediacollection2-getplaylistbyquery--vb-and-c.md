---
title: Método IWMPMediaCollection2 getPlaylistByQuery
description: O método getPlaylistByQuery retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia que correspondem às condições de consulta.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- método getPlaylistByQuery Windows Media Player
- método getPlaylistByQuery Windows Media Player, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 Windows Media Player, método getPlaylistByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747471"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a><span data-ttu-id="990f5-106">Método IWMPMediaCollection2:: getPlaylistByQuery</span><span class="sxs-lookup"><span data-stu-id="990f5-106">IWMPMediaCollection2::getPlaylistByQuery method</span></span>

<span data-ttu-id="990f5-107">O `getPlaylistByQuery` método retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia que correspondem às condições de consulta.</span><span class="sxs-lookup"><span data-stu-id="990f5-107">The `getPlaylistByQuery` method returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="990f5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="990f5-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a><span data-ttu-id="990f5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="990f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="990f5-110">*pQuery* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="990f5-110">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="990f5-111">A interface **WMPLib. IWMPQuery** que representa a consulta.</span><span class="sxs-lookup"><span data-stu-id="990f5-111">The **WMPLib.IWMPQuery** interface that represents the query.</span></span>

</dd> <dt>

<span data-ttu-id="990f5-112">*bstrMediaType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="990f5-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="990f5-113">O **System. String** que é o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="990f5-113">The **System.String** that is the media type.</span></span> <span data-ttu-id="990f5-114">Deve conter um dos seguintes valores: "áudio", "vídeo", "foto", "playlist" ou "outros".</span><span class="sxs-lookup"><span data-stu-id="990f5-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="990f5-115">*bstrSortAttribute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="990f5-115">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="990f5-116">O **System. String** que é o nome do atributo usado para classificação.</span><span class="sxs-lookup"><span data-stu-id="990f5-116">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="990f5-117">Uma cadeia de caracteres de comprimento zero ("") significa que nenhuma classificação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="990f5-117">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="990f5-118">*fSortAscending* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="990f5-118">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="990f5-119">O valor **System. Boolean** que indica se a playlist deve ser classificada em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="990f5-119">The **System.Boolean** value that indicates whether the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="990f5-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="990f5-120">Return value</span></span>

<span data-ttu-id="990f5-121">Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução recuperada.</span><span class="sxs-lookup"><span data-stu-id="990f5-121">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="990f5-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="990f5-122">Remarks</span></span>

<span data-ttu-id="990f5-123">As consultas compostas usando **IWMPQuery** não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="990f5-123">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="990f5-124">Quando a consulta composta especificada pelo parâmetro *pQuery* contém uma condição criada no atributo **MediaType** , essa condição é ignorada.</span><span class="sxs-lookup"><span data-stu-id="990f5-124">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="990f5-125">O valor para o parâmetro *bstrMediaType* é sempre usado.</span><span class="sxs-lookup"><span data-stu-id="990f5-125">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="990f5-126">Por exemplo, se a consulta composta contiver a condição "MediaType igual a áudio" e o valor do parâmetro *bstrMediaType* for "vídeo", a lista de reprodução resultante conterá apenas itens de vídeo.</span><span class="sxs-lookup"><span data-stu-id="990f5-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="990f5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="990f5-127">Requirements</span></span>



| <span data-ttu-id="990f5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="990f5-128">Requirement</span></span> | <span data-ttu-id="990f5-129">Valor</span><span class="sxs-lookup"><span data-stu-id="990f5-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="990f5-130">Versão</span><span class="sxs-lookup"><span data-stu-id="990f5-130">Version</span></span><br/>   | <span data-ttu-id="990f5-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="990f5-131">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="990f5-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="990f5-132">Namespace</span></span><br/> | <span data-ttu-id="990f5-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="990f5-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="990f5-134">Assembly</span><span class="sxs-lookup"><span data-stu-id="990f5-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="990f5-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="990f5-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="990f5-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="990f5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="990f5-137">**Interface IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="990f5-137">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="990f5-138">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="990f5-138">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="990f5-139">**Interface IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="990f5-139">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="990f5-140">**Atributo MediaType**</span><span class="sxs-lookup"><span data-stu-id="990f5-140">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





