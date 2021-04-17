---
title: Método getLanguageName de IWMPControls3
description: O método getLanguageName retorna o nome do idioma de áudio com o LCID (identificador de localidade) especificado.
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- método getLanguageName do Windows Media Player
- método getLanguageName Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, método getLanguageName
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93bf97c7b5213e3d196897de1c3ebcfa6e6d2c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749482"
---
# <a name="iwmpcontrols3getlanguagename-method"></a><span data-ttu-id="3b151-106">Método IWMPControls3:: getLanguageName</span><span class="sxs-lookup"><span data-stu-id="3b151-106">IWMPControls3::getLanguageName method</span></span>

<span data-ttu-id="3b151-107">O método **getLanguageName** retorna o nome do idioma de áudio com o LCID (identificador de localidade) especificado.</span><span class="sxs-lookup"><span data-stu-id="3b151-107">The **getLanguageName** method returns the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b151-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b151-108">Syntax</span></span>


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a><span data-ttu-id="3b151-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b151-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b151-110">*lLangID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b151-110">*lLangID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b151-111">Um **System. Int32** que é o LCID.</span><span class="sxs-lookup"><span data-stu-id="3b151-111">A **System.Int32** that is the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b151-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b151-112">Return value</span></span>

<span data-ttu-id="3b151-113">Um **System. String** que é o nome do idioma de áudio.</span><span class="sxs-lookup"><span data-stu-id="3b151-113">A **System.String** that is the name of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b151-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b151-114">Remarks</span></span>

<span data-ttu-id="3b151-115">Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.</span><span class="sxs-lookup"><span data-stu-id="3b151-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="3b151-116">Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.</span><span class="sxs-lookup"><span data-stu-id="3b151-116">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b151-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b151-117">Requirements</span></span>



| <span data-ttu-id="3b151-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b151-118">Requirement</span></span> | <span data-ttu-id="3b151-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3b151-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b151-120">Versão</span><span class="sxs-lookup"><span data-stu-id="3b151-120">Version</span></span><br/>   | <span data-ttu-id="3b151-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="3b151-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3b151-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b151-122">Namespace</span></span><br/> | <span data-ttu-id="3b151-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3b151-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3b151-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="3b151-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3b151-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3b151-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b151-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b151-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b151-127">**Interface IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b151-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b151-128">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b151-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b151-129">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b151-129">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b151-130">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b151-130">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b151-131">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b151-131">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b151-132">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b151-132">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





