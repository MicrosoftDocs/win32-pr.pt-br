---
title: Propriedade AxWindowsMediaPlayer. cdromCollection
description: A propriedade cdromCollection Obtém uma interface IWMPCdromCollection que fornece acesso a uma coleção de unidades de CD ou DVD.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- Propriedade cdromCollection Windows Media Player
- Propriedade cdromCollection Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, Propriedade cdromCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800169"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a><span data-ttu-id="94c90-106">Propriedade AxWindowsMediaPlayer. cdromCollection</span><span class="sxs-lookup"><span data-stu-id="94c90-106">AxWindowsMediaPlayer.cdromCollection property</span></span>

<span data-ttu-id="94c90-107">A propriedade cdromCollection Obtém uma interface **IWMPCdromCollection** que fornece acesso a uma coleção de unidades de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="94c90-107">The cdromCollection property gets an **IWMPCdromCollection** interface that provides access to a collection of CD or DVD drives.</span></span>

<span data-ttu-id="94c90-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="94c90-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="94c90-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94c90-109">Syntax</span></span>


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a><span data-ttu-id="94c90-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="94c90-110">Property value</span></span>

<span data-ttu-id="94c90-111">Uma interface WMPLib. IWMPCdromCollection.</span><span class="sxs-lookup"><span data-stu-id="94c90-111">A WMPLib.IWMPCdromCollection interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="94c90-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="94c90-112">Remarks</span></span>

<span data-ttu-id="94c90-113">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="94c90-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="94c90-114">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="94c90-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94c90-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94c90-115">Requirements</span></span>



| <span data-ttu-id="94c90-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="94c90-116">Requirement</span></span> | <span data-ttu-id="94c90-117">Valor</span><span class="sxs-lookup"><span data-stu-id="94c90-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94c90-118">Versão</span><span class="sxs-lookup"><span data-stu-id="94c90-118">Version</span></span><br/>   | <span data-ttu-id="94c90-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="94c90-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="94c90-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="94c90-120">Namespace</span></span><br/> | <span data-ttu-id="94c90-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="94c90-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="94c90-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="94c90-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="94c90-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="94c90-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94c90-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="94c90-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c90-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c90-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="94c90-126">**Interface IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c90-126">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="94c90-127">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c90-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="94c90-128">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c90-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





