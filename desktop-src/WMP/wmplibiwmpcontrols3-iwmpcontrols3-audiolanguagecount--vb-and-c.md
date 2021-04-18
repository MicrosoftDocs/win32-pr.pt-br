---
title: Propriedade IWMPControls3 audioLanguageCount
description: A propriedade audioLanguageCount Obtém a contagem de idiomas de áudio com suporte.
ms.assetid: 92e2093f-435b-4427-9f85-8c8ae76e0e2d
keywords:
- Propriedade audioLanguageCount Windows Media Player
- Propriedade audioLanguageCount Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, Propriedade audioLanguageCount
topic_type:
- apiref
api_name:
- IWMPControls3.audioLanguageCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd397dec80a5ccb5f2085e3231782555efde8e39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780089"
---
# <a name="iwmpcontrols3audiolanguagecount-property"></a><span data-ttu-id="121f9-106">Propriedade IWMPControls3:: audioLanguageCount</span><span class="sxs-lookup"><span data-stu-id="121f9-106">IWMPControls3::audioLanguageCount property</span></span>

<span data-ttu-id="121f9-107">A propriedade **audioLanguageCount** Obtém a contagem de idiomas de áudio com suporte.</span><span class="sxs-lookup"><span data-stu-id="121f9-107">The **audioLanguageCount** property gets the count of supported audio languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="121f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="121f9-108">Syntax</span></span>


```CSharp
public System.Int32 audioLanguageCount {get; set;}
```


```VB

Public ReadOnly Property audioLanguageCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="121f9-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="121f9-109">Property value</span></span>

<span data-ttu-id="121f9-110">Um **System. Int32** que é a contagem de idiomas de áudio com suporte.</span><span class="sxs-lookup"><span data-stu-id="121f9-110">A **System.Int32** that is the count of supported audio languages.</span></span>

## <a name="remarks"></a><span data-ttu-id="121f9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="121f9-111">Remarks</span></span>

<span data-ttu-id="121f9-112">Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.</span><span class="sxs-lookup"><span data-stu-id="121f9-112">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="121f9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="121f9-113">Requirements</span></span>



| <span data-ttu-id="121f9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="121f9-114">Requirement</span></span> | <span data-ttu-id="121f9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="121f9-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="121f9-116">Versão</span><span class="sxs-lookup"><span data-stu-id="121f9-116">Version</span></span><br/>   | <span data-ttu-id="121f9-117">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="121f9-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="121f9-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="121f9-118">Namespace</span></span><br/> | <span data-ttu-id="121f9-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="121f9-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="121f9-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="121f9-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="121f9-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="121f9-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="121f9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="121f9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="121f9-123">**Interface IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="121f9-123">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="121f9-124">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="121f9-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="121f9-125">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="121f9-125">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="121f9-126">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="121f9-126">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="121f9-127">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="121f9-127">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="121f9-128">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="121f9-128">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





