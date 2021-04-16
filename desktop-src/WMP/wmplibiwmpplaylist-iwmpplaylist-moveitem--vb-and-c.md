---
title: Método IWMPPlaylist moveItem
description: O método moveItem altera o local de um item de mídia na lista de reprodução.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- método moveItem Windows Media Player
- método moveItem Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, método moveItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765266"
---
# <a name="iwmpplaylistmoveitem-method"></a><span data-ttu-id="3eed4-106">Método IWMPPlaylist:: moveItem</span><span class="sxs-lookup"><span data-stu-id="3eed4-106">IWMPPlaylist::moveItem method</span></span>

<span data-ttu-id="3eed4-107">O método **moveItem** altera o local de um item de mídia na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="3eed4-107">The **moveItem** method changes the location of a media item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eed4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3eed4-108">Syntax</span></span>


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a><span data-ttu-id="3eed4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3eed4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eed4-110">*lIndexOld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3eed4-110">*lIndexOld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eed4-111">Um **System. Int32** que é o índice original.</span><span class="sxs-lookup"><span data-stu-id="3eed4-111">A **System.Int32** that is the original index.</span></span>

</dd> <dt>

<span data-ttu-id="3eed4-112">*lIndexNew* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3eed4-112">*lIndexNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eed4-113">Um **System. Int32** que é o novo índice.</span><span class="sxs-lookup"><span data-stu-id="3eed4-113">A **System.Int32** that is the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eed4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3eed4-114">Return value</span></span>

<span data-ttu-id="3eed4-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3eed4-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eed4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3eed4-116">Remarks</span></span>

<span data-ttu-id="3eed4-117">Todos os itens após o item inserido terão seus números de índice aumentados em um.</span><span class="sxs-lookup"><span data-stu-id="3eed4-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="3eed4-118">Antes de chamar esse método, você deve ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3eed4-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="3eed4-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3eed4-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3eed4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3eed4-120">Requirements</span></span>



| <span data-ttu-id="3eed4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eed4-121">Requirement</span></span> | <span data-ttu-id="3eed4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3eed4-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eed4-123">Versão</span><span class="sxs-lookup"><span data-stu-id="3eed4-123">Version</span></span><br/>   | <span data-ttu-id="3eed4-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="3eed4-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3eed4-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="3eed4-125">Namespace</span></span><br/> | <span data-ttu-id="3eed4-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3eed4-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3eed4-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="3eed4-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3eed4-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3eed4-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eed4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3eed4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eed4-130">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3eed4-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3eed4-131">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3eed4-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3eed4-132">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3eed4-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





