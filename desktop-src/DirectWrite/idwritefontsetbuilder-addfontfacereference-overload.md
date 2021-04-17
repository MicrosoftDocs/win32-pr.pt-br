---
title: Métodos IDWriteFontSetBuilder AddFontFaceReference (Dwrite \_ 3. h)
description: Adiciona uma referência a uma fonte para o conjunto que está sendo compilado.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Gravação direta de métodos AddFontFaceReference
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3c20ca2832bfce3696a98c22730580442f621469
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770239"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a><span data-ttu-id="68c25-104">Métodos IDWriteFontSetBuilder:: AddFontFaceReference</span><span class="sxs-lookup"><span data-stu-id="68c25-104">IDWriteFontSetBuilder::AddFontFaceReference methods</span></span>

<span data-ttu-id="68c25-105">Adiciona uma referência a uma fonte para o conjunto que está sendo compilado.</span><span class="sxs-lookup"><span data-stu-id="68c25-105">Adds a reference to a font to the set being built.</span></span>

### <a name="overload-list"></a><span data-ttu-id="68c25-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="68c25-106">Overload list</span></span>



| <span data-ttu-id="68c25-107">Método</span><span class="sxs-lookup"><span data-stu-id="68c25-107">Method</span></span>                                                                                                                                           | <span data-ttu-id="68c25-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="68c25-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c25-109">[**AddFontFaceReference (IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span><span class="sxs-lookup"><span data-stu-id="68c25-109">[**AddFontFaceReference(IDWriteFontFaceReference\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span></span>                                         | <span data-ttu-id="68c25-110">Adiciona uma referência a uma fonte para o conjunto que está sendo compilado.</span><span class="sxs-lookup"><span data-stu-id="68c25-110">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="68c25-111">Os metadados necessários serão extraídos automaticamente da fonte ao chamar createfontset.</span><span class="sxs-lookup"><span data-stu-id="68c25-111">The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="68c25-112">[**AddFontFaceReference (IDWriteFontFaceReference \* , const DWRITE \_ propriedade da fonte \_ \* , UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span><span class="sxs-lookup"><span data-stu-id="68c25-112">[**AddFontFaceReference(IDWriteFontFaceReference\*, const DWRITE\_FONT\_PROPERTY\*, UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span></span> | <span data-ttu-id="68c25-113">Adiciona uma referência a uma fonte para o conjunto que está sendo compilado.</span><span class="sxs-lookup"><span data-stu-id="68c25-113">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="68c25-114">O chamador fornece informações suficientes para pesquisar, evitando a necessidade de abrir a fonte potencialmente não local.</span><span class="sxs-lookup"><span data-stu-id="68c25-114">The caller supplies enough information to search on, avoiding the need to open the potentially non-local font.</span></span> <span data-ttu-id="68c25-115">Todas as propriedades não fornecidas pelo chamador estarão ausentes e essas propriedades não estarão disponíveis como filtros em GetMatchingFonts.</span><span class="sxs-lookup"><span data-stu-id="68c25-115">Any properties not supplied by the caller will be missing, and those properties will not be available as filters in GetMatchingFonts.</span></span> <span data-ttu-id="68c25-116">Getvalordapropriedades para propriedades ausentes retornará uma lista de cadeias de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="68c25-116">GetPropertyValues for missing properties will return an empty string list.</span></span> <span data-ttu-id="68c25-117">As propriedades passadas devem geralmente ser consistentes com o conteúdo da fonte real, mas não precisam ser.</span><span class="sxs-lookup"><span data-stu-id="68c25-117">The properties passed should generally be consistent with the actual font contents, but they need not be.</span></span> <span data-ttu-id="68c25-118">Você poderia, por exemplo, alias de uma fonte usando um nome diferente ou identificador exclusivo, ou pode definir marcas personalizadas que não estão presentes na fonte real.</span><span class="sxs-lookup"><span data-stu-id="68c25-118">You could, for example, alias a font using a different name or unique identifier, or you could set custom tags not present in the actual font.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="68c25-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68c25-119">Requirements</span></span>



| <span data-ttu-id="68c25-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c25-120">Requirement</span></span> | <span data-ttu-id="68c25-121">Valor</span><span class="sxs-lookup"><span data-stu-id="68c25-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68c25-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68c25-122">Header</span></span><br/> | <dl> <span data-ttu-id="68c25-123"><dt>Dwrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="68c25-123"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68c25-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="68c25-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c25-125">**IDWriteFontSetBuilder**</span><span class="sxs-lookup"><span data-stu-id="68c25-125">**IDWriteFontSetBuilder**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

<span data-ttu-id="68c25-126">�</span><span class="sxs-lookup"><span data-stu-id="68c25-126">�</span></span>

<span data-ttu-id="68c25-127">�</span><span class="sxs-lookup"><span data-stu-id="68c25-127">�</span></span>
