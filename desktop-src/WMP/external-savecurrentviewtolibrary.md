---
title: Método external. saveCurrentViewToLibrary
description: O método saveCurrentViewToLibrary cria uma lista de reprodução a partir dos itens de mídia na exibição atual e salva a lista de reprodução na biblioteca local.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- método saveCurrentViewToLibrary Windows Media Player
- método saveCurrentViewToLibrary Windows Media Player, classe externa
- Classe externa Windows Media Player, método saveCurrentViewToLibrary
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762069"
---
# <a name="externalsavecurrentviewtolibrary-method"></a><span data-ttu-id="948be-106">Método external. saveCurrentViewToLibrary</span><span class="sxs-lookup"><span data-stu-id="948be-106">External.saveCurrentViewToLibrary method</span></span>

<span data-ttu-id="948be-107">O método **saveCurrentViewToLibrary** cria uma lista de reprodução a partir dos itens de mídia na exibição atual e salva a lista de reprodução na biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="948be-107">The **saveCurrentViewToLibrary** method creates a playlist from the media items in the current view and saves the playlist in the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="948be-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="948be-108">Syntax</span></span>


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a><span data-ttu-id="948be-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="948be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="948be-110">*FriendlyListName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="948be-110">*FriendlyListName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="948be-111">**Cadeia de caracteres** que especifica um nome amigável para a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="948be-111">**String** that specifies a friendly name for the playlist.</span></span> <span data-ttu-id="948be-112">O Windows Media Player exibe esse nome na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="948be-112">Windows Media Player displays this name in its user interface.</span></span>

</dd> <dt>

<span data-ttu-id="948be-113">*Local* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="948be-113">*Local* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="948be-114">**Booliano** que especifica se a playlist é dinâmica ou estática.</span><span class="sxs-lookup"><span data-stu-id="948be-114">**Boolean** that specifies whether the playlist is dynamic or static.</span></span> <span data-ttu-id="948be-115">**True** especifica dinâmico e **false** especifica estático.</span><span class="sxs-lookup"><span data-stu-id="948be-115">**TRUE** specifies dynamic, and **FALSE** specifies static.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="948be-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="948be-116">Return value</span></span>

<span data-ttu-id="948be-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="948be-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="948be-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="948be-118">Requirements</span></span>



| <span data-ttu-id="948be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="948be-119">Requirement</span></span> | <span data-ttu-id="948be-120">Valor</span><span class="sxs-lookup"><span data-stu-id="948be-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="948be-121">Versão</span><span class="sxs-lookup"><span data-stu-id="948be-121">Version</span></span><br/> | <span data-ttu-id="948be-122">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="948be-122">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="948be-123">DLL</span><span class="sxs-lookup"><span data-stu-id="948be-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="948be-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="948be-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="948be-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="948be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="948be-126">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="948be-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





