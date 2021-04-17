---
title: Método Controls. getLanguageName
description: O método getLanguageName recupera o nome do idioma de áudio com o LCID (identificador de localidade) especificado.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- método getLanguageName do Windows Media Player
- método getLanguageName Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método getLanguageName
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783619"
---
# <a name="controlsgetlanguagename-method"></a><span data-ttu-id="fe9ba-106">Método Controls. getLanguageName</span><span class="sxs-lookup"><span data-stu-id="fe9ba-106">Controls.getLanguageName method</span></span>

<span data-ttu-id="fe9ba-107">O método **getLanguageName** recupera o nome do idioma de áudio com o LCID (identificador de localidade) especificado.</span><span class="sxs-lookup"><span data-stu-id="fe9ba-107">The **getLanguageName** method retrieves the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe9ba-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe9ba-108">Syntax</span></span>


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a><span data-ttu-id="fe9ba-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe9ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe9ba-110">*LCID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="fe9ba-110">*LCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe9ba-111">**Número** (**longo**) que especifica o LCID.</span><span class="sxs-lookup"><span data-stu-id="fe9ba-111">**Number** (**long**) specifying the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe9ba-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe9ba-112">Return value</span></span>

<span data-ttu-id="fe9ba-113">Esse método retorna uma **cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="fe9ba-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe9ba-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe9ba-114">Remarks</span></span>

<span data-ttu-id="fe9ba-115">Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.</span><span class="sxs-lookup"><span data-stu-id="fe9ba-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="fe9ba-116">Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.</span><span class="sxs-lookup"><span data-stu-id="fe9ba-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe9ba-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe9ba-117">Requirements</span></span>



| <span data-ttu-id="fe9ba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe9ba-118">Requirement</span></span> | <span data-ttu-id="fe9ba-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fe9ba-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9ba-120">Versão</span><span class="sxs-lookup"><span data-stu-id="fe9ba-120">Version</span></span><br/> | <span data-ttu-id="fe9ba-121">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fe9ba-121">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="fe9ba-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fe9ba-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe9ba-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe9ba-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe9ba-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe9ba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe9ba-125">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="fe9ba-125">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="fe9ba-126">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="fe9ba-126">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="fe9ba-127">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="fe9ba-127">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="fe9ba-128">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="fe9ba-128">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="fe9ba-129">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="fe9ba-129">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="fe9ba-130">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="fe9ba-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





