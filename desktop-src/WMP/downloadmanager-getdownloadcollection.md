---
title: Método DownloadManager. getbaixecollection
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método getdownloadscollection recupera a coleção de download especificada.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- método getbaixecollection Windows Media Player
- método getbaixecollection Windows Media Player, classe DownloadManager
- Classe DownloadManager Windows Media Player, método getbaixecollection
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761467"
---
# <a name="downloadmanagergetdownloadcollection-method"></a><span data-ttu-id="7b7e1-108">Método DownloadManager. getbaixecollection</span><span class="sxs-lookup"><span data-stu-id="7b7e1-108">DownloadManager.getDownloadCollection method</span></span>

> [!Note]  
> <span data-ttu-id="7b7e1-109">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="7b7e1-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7b7e1-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="7b7e1-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7b7e1-111">O método **Getdownloadscollection** recupera a coleção de download especificada.</span><span class="sxs-lookup"><span data-stu-id="7b7e1-111">The **getDownloadCollection** method retrieves the specified download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b7e1-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b7e1-112">Syntax</span></span>


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a><span data-ttu-id="7b7e1-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b7e1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b7e1-114">*CollectionId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b7e1-114">*collectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b7e1-115">**Número** (**longo**) especificando a ID da coleção de download a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="7b7e1-115">**Number** (**long**) specifying the ID of the download collection to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b7e1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b7e1-116">Return value</span></span>

<span data-ttu-id="7b7e1-117">Esse método retorna um objeto **downloadcollection** .</span><span class="sxs-lookup"><span data-stu-id="7b7e1-117">This method returns a **DownloadCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b7e1-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b7e1-118">Remarks</span></span>

<span data-ttu-id="7b7e1-119">Você deve primeiro chamar *DownloadManager*. **Createbaixecollection** para criar uma nova coleção e recuperar seu valor de ID.</span><span class="sxs-lookup"><span data-stu-id="7b7e1-119">You must first call *DownloadManager*.**createDownloadCollection** to create a new collection and retrieve its ID value.</span></span>

<span data-ttu-id="7b7e1-120">Uma coleção de download existente pode conter itens que foram marcados como cancelados.</span><span class="sxs-lookup"><span data-stu-id="7b7e1-120">An existing download collection may contain items that have been marked as cancelled.</span></span>

<span data-ttu-id="7b7e1-121">Itens de download em tempo real não concluídos em uma sessão anterior não são recuperados como parte da coleção.</span><span class="sxs-lookup"><span data-stu-id="7b7e1-121">Real-time download items not completed in a prior session are not retrieved as part of the collection.</span></span> <span data-ttu-id="7b7e1-122">Os downloads em segundo plano que foram concluídos antes da sessão atual permanecem na coleção de download até serem removidos.</span><span class="sxs-lookup"><span data-stu-id="7b7e1-122">Background downloads that were completed prior to the current session remain in the download collection until removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b7e1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b7e1-123">Requirements</span></span>



| <span data-ttu-id="7b7e1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b7e1-124">Requirement</span></span> | <span data-ttu-id="7b7e1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7b7e1-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7e1-126">Versão</span><span class="sxs-lookup"><span data-stu-id="7b7e1-126">Version</span></span><br/> | <span data-ttu-id="7b7e1-127">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7b7e1-127">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="7b7e1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7b7e1-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b7e1-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b7e1-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b7e1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b7e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b7e1-131">**Objeto DownloadManager**</span><span class="sxs-lookup"><span data-stu-id="7b7e1-131">**DownloadManager Object**</span></span>](downloadmanager-object.md)
</dt> <dt>

[<span data-ttu-id="7b7e1-132">**DownloadManager. createbaixecollection**</span><span class="sxs-lookup"><span data-stu-id="7b7e1-132">**DownloadManager. createDownloadCollection**</span></span>](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="7b7e1-133">**Objeto downloadcollection**</span><span class="sxs-lookup"><span data-stu-id="7b7e1-133">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





