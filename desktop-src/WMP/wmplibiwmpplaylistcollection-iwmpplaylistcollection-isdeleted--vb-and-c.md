---
title: Método IsDeleted IWMPPlaylistCollection
description: O método IsDeleted retorna um valor que indica se a playlist especificada está na pasta itens excluídos.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- método IsDeleted Windows Media Player
- método IsDeleted Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection do Windows Media Player, método IsDeleted
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782544"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a><span data-ttu-id="f539a-106">Método IWMPPlaylistCollection:: IsDeleted</span><span class="sxs-lookup"><span data-stu-id="f539a-106">IWMPPlaylistCollection::isDeleted method</span></span>

<span data-ttu-id="f539a-107">O método **IsDeleted** retorna um valor que indica se a playlist especificada está na pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="f539a-107">The **isDeleted** method returns a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="f539a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f539a-108">Syntax</span></span>


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a><span data-ttu-id="f539a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f539a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f539a-110">*pItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f539a-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f539a-111">Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução consultada.</span><span class="sxs-lookup"><span data-stu-id="f539a-111">A **WMPLib.IWMPPlaylist** interface for the queried playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f539a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f539a-112">Return value</span></span>

<span data-ttu-id="f539a-113">Um **System. Boolean** que especifica se a playlist foi excluída.</span><span class="sxs-lookup"><span data-stu-id="f539a-113">A **System.Boolean** that specifies whether the playlist was deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="f539a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f539a-114">Requirements</span></span>



| <span data-ttu-id="f539a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f539a-115">Requirement</span></span> | <span data-ttu-id="f539a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f539a-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f539a-117">Versão</span><span class="sxs-lookup"><span data-stu-id="f539a-117">Version</span></span><br/>   | <span data-ttu-id="f539a-118">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f539a-118">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="f539a-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="f539a-119">Namespace</span></span><br/> | <span data-ttu-id="f539a-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f539a-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f539a-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="f539a-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f539a-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f539a-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f539a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f539a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f539a-124">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f539a-124">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f539a-125">**Interface IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f539a-125">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





