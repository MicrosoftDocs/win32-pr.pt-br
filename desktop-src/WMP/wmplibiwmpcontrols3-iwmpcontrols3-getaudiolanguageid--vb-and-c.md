---
title: Método IWMPControls3 getAudioLanguageID
description: O método getAudioLanguageID retorna o LCID (identificador de localidade) para um índice de idioma de áudio especificado.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- método getAudioLanguageID Windows Media Player
- método getAudioLanguageID Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, método getAudioLanguageID
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750110"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a><span data-ttu-id="3b310-106">Método IWMPControls3:: getAudioLanguageID</span><span class="sxs-lookup"><span data-stu-id="3b310-106">IWMPControls3::getAudioLanguageID method</span></span>

<span data-ttu-id="3b310-107">O método **getAudioLanguageID** retorna o LCID (identificador de localidade) para um índice de idioma de áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="3b310-107">The **getAudioLanguageID** method returns the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b310-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b310-108">Syntax</span></span>


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a><span data-ttu-id="3b310-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b310-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b310-110">*Lindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b310-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b310-111">Um **System. Int32** que é o índice baseado em um do idioma de áudio.</span><span class="sxs-lookup"><span data-stu-id="3b310-111">A **System.Int32** that is the one-based index of the audio language.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b310-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b310-112">Return value</span></span>

<span data-ttu-id="3b310-113">Um **System. Int32** que é o LCID.</span><span class="sxs-lookup"><span data-stu-id="3b310-113">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b310-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b310-114">Remarks</span></span>

<span data-ttu-id="3b310-115">Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.</span><span class="sxs-lookup"><span data-stu-id="3b310-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="3b310-116">Para conteúdo baseado no Windows, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.</span><span class="sxs-lookup"><span data-stu-id="3b310-116">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="3b310-117">Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte e, em seguida, acesse um idioma de áudio individualmente usando um índice com base em um.</span><span class="sxs-lookup"><span data-stu-id="3b310-117">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b310-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b310-118">Requirements</span></span>



| <span data-ttu-id="3b310-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b310-119">Requirement</span></span> | <span data-ttu-id="3b310-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3b310-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b310-121">Versão</span><span class="sxs-lookup"><span data-stu-id="3b310-121">Version</span></span><br/>   | <span data-ttu-id="3b310-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="3b310-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3b310-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b310-123">Namespace</span></span><br/> | <span data-ttu-id="3b310-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3b310-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3b310-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="3b310-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3b310-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3b310-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b310-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b310-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b310-128">**Interface IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b310-128">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b310-129">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b310-129">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b310-130">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b310-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b310-131">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b310-131">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b310-132">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b310-132">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b310-133">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b310-133">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





