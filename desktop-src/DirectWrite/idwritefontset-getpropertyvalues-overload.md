---
title: Métodos getvalordapropriedades IDWriteFontSet (Dwrite \_ 3. h)
description: Retorna valores de propriedade para o conjunto de fontes.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Métodos getvalordapropriedades Direct Write
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755129"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a><span data-ttu-id="b2e53-104">Métodos IDWriteFontSet:: getvalordapropriedades</span><span class="sxs-lookup"><span data-stu-id="b2e53-104">IDWriteFontSet::GetPropertyValues methods</span></span>

<span data-ttu-id="b2e53-105">Retorna valores de propriedade para o conjunto de fontes.</span><span class="sxs-lookup"><span data-stu-id="b2e53-105">Returns property values for the font set.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b2e53-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="b2e53-106">Overload list</span></span>



| <span data-ttu-id="b2e53-107">Método</span><span class="sxs-lookup"><span data-stu-id="b2e53-107">Method</span></span>                                                                                                                                   | <span data-ttu-id="b2e53-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2e53-108">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e53-109">[**Getvalordapropriedades ( \_ ID da propriedade da fonte DWRITE \_ \_ , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="b2e53-109">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span>                       | <span data-ttu-id="b2e53-110">Retorna todos os valores de propriedade exclusivos no conjunto, que pode ser usado para fins como exibir uma lista de família ou uma nuvem de marca.</span><span class="sxs-lookup"><span data-stu-id="b2e53-110">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="b2e53-111">Todos os valores são retornados independentemente do idioma, incluindo todos os nomes localizados.</span><span class="sxs-lookup"><span data-stu-id="b2e53-111">All values are returned regardless of language, including all localized names.</span></span> <br/>                                                                                       |
| <span data-ttu-id="b2e53-112">[**Getvalordapropriedades ( \_ ID da propriedade da fonte DWRITE \_ \_ , const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="b2e53-112">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, const WCHAR\*, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span></span>        | <span data-ttu-id="b2e53-113">Retorna todos os valores de propriedade exclusivos no conjunto, que pode ser usado para fins como exibir uma lista de família ou uma nuvem de marca.</span><span class="sxs-lookup"><span data-stu-id="b2e53-113">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="b2e53-114">Os valores são retornados em ordem de prioridade de acordo com a lista de idiomas, de modo que, se uma fonte contiver mais de um nome localizado, o preferencial será retornado.</span><span class="sxs-lookup"><span data-stu-id="b2e53-114">Values are returned in priority order according to the language list, such that if a font contains more than one localized name, the preferred one will be returned.</span></span> <br/> |
| <span data-ttu-id="b2e53-115">[**Getvalordapropriedades (UINT32, \_ ID de \_ propriedade de fonte DWRITE \_ , bool \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="b2e53-115">[**GetPropertyValues(UINT32, DWRITE\_FONT\_PROPERTY\_ID, BOOL\*, IDWriteLocalizedStrings\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span> | <span data-ttu-id="b2e53-116">Retorna os valores de propriedade de um índice de item de fonte específico.</span><span class="sxs-lookup"><span data-stu-id="b2e53-116">Returns the property values of a specific font item index.</span></span><br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="b2e53-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2e53-117">Requirements</span></span>



| <span data-ttu-id="b2e53-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2e53-118">Requirement</span></span> | <span data-ttu-id="b2e53-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b2e53-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e53-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2e53-120">Header</span></span><br/> | <dl> <span data-ttu-id="b2e53-121"><dt>Dwrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2e53-121"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e53-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2e53-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e53-123">**IDWriteFontSet**</span><span class="sxs-lookup"><span data-stu-id="b2e53-123">**IDWriteFontSet**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

<span data-ttu-id="b2e53-124">�</span><span class="sxs-lookup"><span data-stu-id="b2e53-124">�</span></span>

<span data-ttu-id="b2e53-125">�</span><span class="sxs-lookup"><span data-stu-id="b2e53-125">�</span></span>
