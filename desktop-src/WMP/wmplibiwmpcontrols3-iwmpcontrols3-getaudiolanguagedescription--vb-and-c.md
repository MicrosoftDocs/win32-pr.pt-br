---
title: Método IWMPControls3 getAudioLanguageDescription
description: O método getAudioLanguageDescription retorna a descrição para o idioma de áudio correspondente ao índice baseado em um especificado.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- método getAudioLanguageDescription Windows Media Player
- método getAudioLanguageDescription Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, método getAudioLanguageDescription
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749519"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a><span data-ttu-id="49a23-106">Método IWMPControls3:: getAudioLanguageDescription</span><span class="sxs-lookup"><span data-stu-id="49a23-106">IWMPControls3::getAudioLanguageDescription method</span></span>

<span data-ttu-id="49a23-107">O método **getAudioLanguageDescription** retorna a descrição para o idioma de áudio correspondente ao índice baseado em um especificado.</span><span class="sxs-lookup"><span data-stu-id="49a23-107">The **getAudioLanguageDescription** method returns the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a23-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49a23-108">Syntax</span></span>


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a><span data-ttu-id="49a23-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49a23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a23-110">*Lindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49a23-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a23-111">Um **System. Int32** que é o índice de idioma de áudio baseado em um.</span><span class="sxs-lookup"><span data-stu-id="49a23-111">A **System.Int32** that is the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a23-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49a23-112">Return value</span></span>

<span data-ttu-id="49a23-113">Um **System. String** que é a descrição do idioma de áudio.</span><span class="sxs-lookup"><span data-stu-id="49a23-113">A **System.String** that is the description of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="49a23-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="49a23-114">Remarks</span></span>

<span data-ttu-id="49a23-115">Para conteúdo baseado no Windows, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.</span><span class="sxs-lookup"><span data-stu-id="49a23-115">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="49a23-116">Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte e, em seguida, acesse um idioma de áudio individualmente usando um índice com base em um.</span><span class="sxs-lookup"><span data-stu-id="49a23-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="49a23-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49a23-117">Requirements</span></span>



| <span data-ttu-id="49a23-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="49a23-118">Requirement</span></span> | <span data-ttu-id="49a23-119">Valor</span><span class="sxs-lookup"><span data-stu-id="49a23-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49a23-120">Versão</span><span class="sxs-lookup"><span data-stu-id="49a23-120">Version</span></span><br/>   | <span data-ttu-id="49a23-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="49a23-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="49a23-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="49a23-122">Namespace</span></span><br/> | <span data-ttu-id="49a23-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="49a23-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="49a23-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="49a23-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="49a23-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="49a23-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49a23-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="49a23-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a23-127">**Interface IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49a23-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49a23-128">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49a23-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49a23-129">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49a23-129">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49a23-130">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49a23-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49a23-131">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49a23-131">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49a23-132">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49a23-132">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





