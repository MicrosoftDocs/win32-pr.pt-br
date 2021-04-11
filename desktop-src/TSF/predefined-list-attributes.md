---
title: Atributos de lista predefinidos (TsAttrid. h)
description: Os valores a seguir identificam os atributos de lista obtidos com o método ITfContext GetAppProperty. O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Atributos de lista predefinidos estrutura de serviços de texto
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086124"
---
# <a name="predefined-list-attributes"></a><span data-ttu-id="658b5-105">Atributos de lista predefinidos</span><span class="sxs-lookup"><span data-stu-id="658b5-105">Predefined List Attributes</span></span>

<span data-ttu-id="658b5-106">Os valores a seguir identificam os atributos de lista obtidos com o método [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="658b5-106">The following values identify list attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="658b5-107">O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.</span><span class="sxs-lookup"><span data-stu-id="658b5-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="658b5-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="658b5-108">Properties</span></span>



| <span data-ttu-id="658b5-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="658b5-109">Property</span></span>                          | <span data-ttu-id="658b5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="658b5-110">Description</span></span>                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="658b5-111">Lista de TSATTRID \_</span><span class="sxs-lookup"><span data-stu-id="658b5-111">TSATTRID\_List</span></span>                    | <span data-ttu-id="658b5-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="658b5-112">Not used.</span></span>                                                                                       |
| <span data-ttu-id="658b5-113">TSATTRID \_ lista \_ LevelIndel</span><span class="sxs-lookup"><span data-stu-id="658b5-113">TSATTRID\_List\_LevelIndel</span></span>        | <span data-ttu-id="658b5-114">Contém o nível de índice da lista.</span><span class="sxs-lookup"><span data-stu-id="658b5-114">Contains the index level of the list.</span></span> <span data-ttu-id="658b5-115">1 é o nível mais externo, 2 é o próximo nível e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="658b5-115">1 is the outermost level, 2 is the next level, and so on.</span></span> |
| <span data-ttu-id="658b5-116">\_Tipo de lista TSATTRID \_</span><span class="sxs-lookup"><span data-stu-id="658b5-116">TSATTRID\_List\_Type</span></span>              | <span data-ttu-id="658b5-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="658b5-117">Not used.</span></span>                                                                                       |
| <span data-ttu-id="658b5-118">\_Tipo de lista TSATTRID \_ \_ árabe</span><span class="sxs-lookup"><span data-stu-id="658b5-118">TSATTRID\_List\_Type\_Arabic</span></span>      | <span data-ttu-id="658b5-119">Contém um valor diferente de zero se a lista for uma lista de algarismos árabes ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="658b5-119">Contains a nonzero value if the list is an arabic numeral list or zero otherwise.</span></span>               |
| <span data-ttu-id="658b5-120">\_Marcador de \_ tipo de lista de TSATTRID \_</span><span class="sxs-lookup"><span data-stu-id="658b5-120">TSATTRID\_List\_Type\_Bullet</span></span>      | <span data-ttu-id="658b5-121">Contém um valor diferente de zero se a lista for uma lista com marcadores ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="658b5-121">Contains a nonzero value if the list is a bulleted list or zero otherwise.</span></span>                      |
| <span data-ttu-id="658b5-122">TSATTRID \_ tipo de lista \_ \_ LowerLetter</span><span class="sxs-lookup"><span data-stu-id="658b5-122">TSATTRID\_List\_Type\_LowerLetter</span></span> | <span data-ttu-id="658b5-123">Contém um valor diferente de zero se a lista for uma lista de letras minúsculas ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="658b5-123">Contains a nonzero value if the list is a lowercase lettered list or zero otherwise.</span></span>            |
| <span data-ttu-id="658b5-124">TSATTRID \_ tipo de lista \_ \_ LowerRoman</span><span class="sxs-lookup"><span data-stu-id="658b5-124">TSATTRID\_List\_Type\_LowerRoman</span></span>  | <span data-ttu-id="658b5-125">Contém um valor diferente de zero se a lista for uma lista de algarismos romanos minúsculos ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="658b5-125">Contains a nonzero value if the list is a lowercase roman numeral list or zero otherwise.</span></span>       |
| <span data-ttu-id="658b5-126">TSATTRID \_ tipo de lista \_ \_ UpperLetter</span><span class="sxs-lookup"><span data-stu-id="658b5-126">TSATTRID\_List\_Type\_UpperLetter</span></span> | <span data-ttu-id="658b5-127">Contém um valor diferente de zero se a lista for uma lista com letras maiúsculas ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="658b5-127">Contains a nonzero value if the list is an upper-case lettered list or zero otherwise.</span></span>          |
| <span data-ttu-id="658b5-128">TSATTRID \_ tipo de lista \_ \_ UpperRoman</span><span class="sxs-lookup"><span data-stu-id="658b5-128">TSATTRID\_List\_Type\_UpperRoman</span></span>  | <span data-ttu-id="658b5-129">Contém um valor diferente de zero se a lista for uma lista de algarismos romanos maiúsculos ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="658b5-129">Contains a nonzero value if the list is an uppercase roman numeral list or zero otherwise.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="658b5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="658b5-130">Requirements</span></span>



| <span data-ttu-id="658b5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="658b5-131">Requirement</span></span> | <span data-ttu-id="658b5-132">Valor</span><span class="sxs-lookup"><span data-stu-id="658b5-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="658b5-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="658b5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="658b5-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="658b5-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="658b5-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="658b5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="658b5-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="658b5-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="658b5-137">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="658b5-137">Redistributable</span></span><br/>          | <span data-ttu-id="658b5-138">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="658b5-138">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="658b5-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="658b5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="658b5-140"><dt>TsAttrid. h</dt></span><span class="sxs-lookup"><span data-stu-id="658b5-140"><dt>TsAttrid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="658b5-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="658b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658b5-142">ITfContext:: GetAppProperty</span><span class="sxs-lookup"><span data-stu-id="658b5-142">ITfContext::GetAppProperty</span></span>](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

