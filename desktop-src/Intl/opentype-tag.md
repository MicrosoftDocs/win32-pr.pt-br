---
description: Define uma matriz de 4 bytes que contém valores ASCII de 4 8 bits de espaço, A-Z ou a-z para identificar marcas de recurso de fonte, idioma e script OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810332"
---
# <a name="opentype_tag"></a><span data-ttu-id="a373c-103">\_marca OPENTYPE</span><span class="sxs-lookup"><span data-stu-id="a373c-103">OPENTYPE\_TAG</span></span>

<span data-ttu-id="a373c-104">Define uma matriz de 4 bytes que contém valores ASCII de 4 8 bits de espaço, A-Z ou a-z para identificar marcas de recurso de fonte, idioma e script OpenType.</span><span class="sxs-lookup"><span data-stu-id="a373c-104">Defines a 4-byte array that contains four 8-bit ASCII values of space, A-Z, or a-z to identify OpenType script, language, and font feature tags.</span></span>


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a><span data-ttu-id="a373c-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a373c-105">Remarks</span></span>

<span data-ttu-id="a373c-106">Os exemplos a seguir definem representações de marcas de recurso OpenType.</span><span class="sxs-lookup"><span data-stu-id="a373c-106">The following examples define representations of OpenType feature tags.</span></span>

-   <span data-ttu-id="a373c-107">A marca de recurso para o recurso ligadura é "liga".</span><span class="sxs-lookup"><span data-stu-id="a373c-107">The feature tag for the ligature feature is "liga".</span></span>
-   <span data-ttu-id="a373c-108">As marcas de idioma para romeno, urdu e persa são "ROM", "URD" e "distante", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a373c-108">The language tags for Romanian, Urdu, and Persian are "ROM ", "URD ", and "FAR ", respectively.</span></span> <span data-ttu-id="a373c-109">Observe que cada uma dessas marcas termina com um espaço.</span><span class="sxs-lookup"><span data-stu-id="a373c-109">Note that each of these tags ends with a space.</span></span>
-   <span data-ttu-id="a373c-110">As marcas de script para scripts latinos e árabes são "Latn" e "árabe", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a373c-110">The script tags for Latin and Arabic scripts are "latn" and "arab", respectively.</span></span>

<span data-ttu-id="a373c-111">Para obter mais informações sobre marcas de recurso OpenType e a especificação OpenType, consulte <https://www.microsoft.com/typography/otspec/featuretags.htm> .</span><span class="sxs-lookup"><span data-stu-id="a373c-111">For more information on OpenType feature tags and the OpenType specification, see <https://www.microsoft.com/typography/otspec/featuretags.htm>.</span></span>

## <a name="requirements"></a><span data-ttu-id="a373c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a373c-112">Requirements</span></span>



| <span data-ttu-id="a373c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a373c-113">Requirement</span></span> | <span data-ttu-id="a373c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a373c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a373c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a373c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a373c-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a373c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a373c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a373c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a373c-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a373c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a373c-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a373c-119">Redistributable</span></span><br/>          | <span data-ttu-id="a373c-120">Usp10.dll versão 1,600 ou superior, o Windows xpandir mais tarde</span><span class="sxs-lookup"><span data-stu-id="a373c-120">Usp10.dll version 1.600 or greater onWindows XPand later</span></span><br/>                |
| <span data-ttu-id="a373c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a373c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a373c-122"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a373c-122"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a373c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a373c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a373c-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="a373c-124">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="a373c-125">Estruturas do Uniscribe</span><span class="sxs-lookup"><span data-stu-id="a373c-125">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="a373c-126">**ScriptGetFontAlternateGlyphs**</span><span class="sxs-lookup"><span data-stu-id="a373c-126">**ScriptGetFontAlternateGlyphs**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[<span data-ttu-id="a373c-127">**ScriptGetFontFeatureTags**</span><span class="sxs-lookup"><span data-stu-id="a373c-127">**ScriptGetFontFeatureTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[<span data-ttu-id="a373c-128">**ScriptGetFontLanguageTags**</span><span class="sxs-lookup"><span data-stu-id="a373c-128">**ScriptGetFontLanguageTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[<span data-ttu-id="a373c-129">**ScriptGetFontScriptTags**</span><span class="sxs-lookup"><span data-stu-id="a373c-129">**ScriptGetFontScriptTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[<span data-ttu-id="a373c-130">**ScriptItemizeOpenType**</span><span class="sxs-lookup"><span data-stu-id="a373c-130">**ScriptItemizeOpenType**</span></span>](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[<span data-ttu-id="a373c-131">**ScriptPlaceOpenType**</span><span class="sxs-lookup"><span data-stu-id="a373c-131">**ScriptPlaceOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[<span data-ttu-id="a373c-132">**ScriptPositionSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="a373c-132">**ScriptPositionSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[<span data-ttu-id="a373c-133">**ScriptShapeOpenType**</span><span class="sxs-lookup"><span data-stu-id="a373c-133">**ScriptShapeOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[<span data-ttu-id="a373c-134">**ScriptSubstituteSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="a373c-134">**ScriptSubstituteSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




