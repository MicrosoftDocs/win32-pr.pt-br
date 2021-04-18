---
title: Propriedade IWMPControls3 currentAudioLanguageIndex
description: A propriedade currentAudioLanguageIndex Obtém ou define o índice com base em um que corresponde ao idioma de áudio para reprodução.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- Propriedade currentAudioLanguageIndex Windows Media Player
- Propriedade currentAudioLanguageIndex Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, Propriedade currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751565"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a><span data-ttu-id="b9238-106">Propriedade IWMPControls3:: currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="b9238-106">IWMPControls3::currentAudioLanguageIndex property</span></span>

<span data-ttu-id="b9238-107">A propriedade **currentAudioLanguageIndex** Obtém ou define o índice com base em um que corresponde ao idioma de áudio para reprodução.</span><span class="sxs-lookup"><span data-stu-id="b9238-107">The **currentAudioLanguageIndex** property gets or sets the one-based index that corresponds to the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9238-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9238-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="b9238-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b9238-109">Property value</span></span>

<span data-ttu-id="b9238-110">Um **System. Int32** que é o índice baseado em um da linguagem.</span><span class="sxs-lookup"><span data-stu-id="b9238-110">A **System.Int32** that is the one-based index of the language.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9238-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9238-111">Remarks</span></span>

<span data-ttu-id="b9238-112">Para conteúdo baseado no Windows, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.</span><span class="sxs-lookup"><span data-stu-id="b9238-112">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="b9238-113">Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte.</span><span class="sxs-lookup"><span data-stu-id="b9238-113">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9238-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9238-114">Requirements</span></span>



| <span data-ttu-id="b9238-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9238-115">Requirement</span></span> | <span data-ttu-id="b9238-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b9238-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9238-117">Versão</span><span class="sxs-lookup"><span data-stu-id="b9238-117">Version</span></span><br/>   | <span data-ttu-id="b9238-118">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b9238-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b9238-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9238-119">Namespace</span></span><br/> | <span data-ttu-id="b9238-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b9238-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b9238-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="b9238-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b9238-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b9238-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9238-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9238-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9238-124">**Interface IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b9238-124">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9238-125">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b9238-125">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9238-126">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b9238-126">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9238-127">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b9238-127">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9238-128">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b9238-128">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9238-129">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b9238-129">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





