---
title: Método PlaylistArray. Item
description: O método item recupera a lista de reprodução no índice fornecido.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe PlaylistArray
- Classe PlaylistArray do Windows Media Player, método de item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771650"
---
# <a name="playlistarrayitem-method"></a><span data-ttu-id="bdb14-106">Método PlaylistArray. Item</span><span class="sxs-lookup"><span data-stu-id="bdb14-106">PlaylistArray.item method</span></span>

<span data-ttu-id="bdb14-107">O método **Item** recupera a lista de reprodução no índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="bdb14-107">The **item** method retrieves the playlist at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb14-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdb14-108">Syntax</span></span>


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="bdb14-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdb14-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb14-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="bdb14-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdb14-111">**Número** (**longo**) que contém o índice da lista de reprodução a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="bdb14-111">**Number** (**long**) containing the index of the playlist to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb14-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdb14-112">Return value</span></span>

<span data-ttu-id="bdb14-113">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="bdb14-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb14-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdb14-114">Remarks</span></span>

<span data-ttu-id="bdb14-115">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bdb14-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="bdb14-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bdb14-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb14-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdb14-117">Requirements</span></span>



| <span data-ttu-id="bdb14-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdb14-118">Requirement</span></span> | <span data-ttu-id="bdb14-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bdb14-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb14-120">Versão</span><span class="sxs-lookup"><span data-stu-id="bdb14-120">Version</span></span><br/> | <span data-ttu-id="bdb14-121">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bdb14-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bdb14-122">DLL</span><span class="sxs-lookup"><span data-stu-id="bdb14-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="bdb14-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdb14-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdb14-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdb14-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb14-125">**Objeto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="bdb14-125">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="bdb14-126">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bdb14-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="bdb14-127">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bdb14-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





