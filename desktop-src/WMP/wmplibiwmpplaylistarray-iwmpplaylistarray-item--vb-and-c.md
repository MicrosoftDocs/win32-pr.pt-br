---
title: Método de item IWMPPlaylistArray
description: O método Item retorna uma interface IWMPPlaylist que representa a playlist no índice especificado.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Método de item Windows Media Player
- Método de item Windows Media Player, interface IWMPPlaylistArray
- Interface IWMPPlaylistArray do Windows Media Player, método de item
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771371"
---
# <a name="iwmpplaylistarrayitem-method"></a><span data-ttu-id="53e63-106">Método IWMPPlaylistArray:: item</span><span class="sxs-lookup"><span data-stu-id="53e63-106">IWMPPlaylistArray::Item method</span></span>

<span data-ttu-id="53e63-107">O método **Item** retorna uma interface **IWMPPlaylist** que representa a playlist no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="53e63-107">The **Item** method returns an **IWMPPlaylist** interface representing the playlist at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e63-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53e63-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a><span data-ttu-id="53e63-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53e63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53e63-110">*Lindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53e63-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53e63-111">Um **System. Int32** que contém o índice que identifica a lista de reprodução que o método deve recuperar.</span><span class="sxs-lookup"><span data-stu-id="53e63-111">A **System.Int32** containing the index that identifies the playlist that the method should retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53e63-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53e63-112">Return value</span></span>

<span data-ttu-id="53e63-113">Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução recuperada.</span><span class="sxs-lookup"><span data-stu-id="53e63-113">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="53e63-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="53e63-114">Remarks</span></span>

<span data-ttu-id="53e63-115">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="53e63-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="53e63-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="53e63-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53e63-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53e63-117">Requirements</span></span>



| <span data-ttu-id="53e63-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="53e63-118">Requirement</span></span> | <span data-ttu-id="53e63-119">Valor</span><span class="sxs-lookup"><span data-stu-id="53e63-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53e63-120">Versão</span><span class="sxs-lookup"><span data-stu-id="53e63-120">Version</span></span><br/>   | <span data-ttu-id="53e63-121">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="53e63-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="53e63-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="53e63-122">Namespace</span></span><br/> | <span data-ttu-id="53e63-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="53e63-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="53e63-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="53e63-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="53e63-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="53e63-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53e63-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="53e63-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e63-127">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="53e63-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="53e63-128">**Interface IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="53e63-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





