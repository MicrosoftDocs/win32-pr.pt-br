---
title: Propriedade de erro IWMPMedia2
description: A Propriedade Error obterá uma interface IWMPErrorItem se o item de mídia tiver uma condição de erro.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Propriedade de erro Windows Media Player
- Propriedade de erro Windows Media Player, interface IWMPMedia2
- Interface IWMPMedia2 Windows Media Player, Propriedade Error
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811778"
---
# <a name="iwmpmedia2error-property"></a><span data-ttu-id="b145c-106">Propriedade IWMPMedia2:: Error</span><span class="sxs-lookup"><span data-stu-id="b145c-106">IWMPMedia2::Error property</span></span>

<span data-ttu-id="b145c-107">A propriedade **Error** obterá uma interface **IWMPErrorItem** se o item de mídia tiver uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="b145c-107">The **Error** property gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span>

<span data-ttu-id="b145c-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b145c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b145c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b145c-109">Syntax</span></span>


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a><span data-ttu-id="b145c-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b145c-110">Property value</span></span>

<span data-ttu-id="b145c-111">Uma interface **WMPLib. IWMPErrorItem** que fornece acesso a informações sobre a condição de erro.</span><span class="sxs-lookup"><span data-stu-id="b145c-111">A **WMPLib.IWMPErrorItem** interface that provides access to information about the error condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="b145c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b145c-112">Remarks</span></span>

<span data-ttu-id="b145c-113">Se o item de mídia não puder ser reproduzido, essa propriedade obterá uma interface **IWMPErrorItem** que contém informações sobre o problema encontrado.</span><span class="sxs-lookup"><span data-stu-id="b145c-113">If the media item cannot be played, this property gets an **IWMPErrorItem** interface that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="b145c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b145c-114">Requirements</span></span>



| <span data-ttu-id="b145c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b145c-115">Requirement</span></span> | <span data-ttu-id="b145c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b145c-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b145c-117">Versão</span><span class="sxs-lookup"><span data-stu-id="b145c-117">Version</span></span><br/>   | <span data-ttu-id="b145c-118">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b145c-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b145c-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="b145c-119">Namespace</span></span><br/> | <span data-ttu-id="b145c-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b145c-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b145c-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="b145c-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b145c-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b145c-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b145c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b145c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b145c-124">**IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b145c-124">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b145c-125">**Interface IWMPMedia2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b145c-125">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





