---
title: Outros atributos predefinidos (TsAttrid. h)
description: Os valores a seguir identificam os atributos diversos obtidos com o método ITfContext GetAppProperty. O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.
ms.assetid: 8536938b-98a1-415b-b5f2-45b90215c270
keywords:
- Outros atributos predefinidos estrutura de serviços de texto
topic_type:
- apiref
api_name:
- Other Predefined Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d0a3ff72a5ea84a6b9e5b47106012a945dbf45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800041"
---
# <a name="other-predefined-attributes"></a><span data-ttu-id="99a0b-105">Outros atributos predefinidos</span><span class="sxs-lookup"><span data-stu-id="99a0b-105">Other Predefined Attributes</span></span>

<span data-ttu-id="99a0b-106">Os valores a seguir identificam os atributos diversos obtidos com o método [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="99a0b-106">The following values identify miscellaneous attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="99a0b-107">O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.</span><span class="sxs-lookup"><span data-stu-id="99a0b-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="99a0b-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="99a0b-108">Properties</span></span>



| <span data-ttu-id="99a0b-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="99a0b-109">Property</span></span>                             | <span data-ttu-id="99a0b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="99a0b-110">Description</span></span>                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="99a0b-111">**\_Aplicativo TSATTRID**</span><span class="sxs-lookup"><span data-stu-id="99a0b-111">**TSATTRID\_App**</span></span>                    | <span data-ttu-id="99a0b-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="99a0b-112">Not used.</span></span>                                                                         |
| <span data-ttu-id="99a0b-113">**\_IncorrectGrammar do aplicativo TSATTRID \_**</span><span class="sxs-lookup"><span data-stu-id="99a0b-113">**TSATTRID\_App\_IncorrectGrammar**</span></span>  | <span data-ttu-id="99a0b-114">Contém um valor diferente de zero se o texto contiver um erro de gramática ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="99a0b-114">Contains a nonzero value if the text contains a grammar error or zero otherwise.</span></span>  |
| <span data-ttu-id="99a0b-115">**\_IncorrectSpelling do aplicativo TSATTRID \_**</span><span class="sxs-lookup"><span data-stu-id="99a0b-115">**TSATTRID\_App\_IncorrectSpelling**</span></span> | <span data-ttu-id="99a0b-116">Contém um valor diferente de zero se o texto contiver um erro de ortografia ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="99a0b-116">Contains a nonzero value if the text contains a spelling error or zero otherwise.</span></span> |
| <span data-ttu-id="99a0b-117">**TSATTRID \_ outros**</span><span class="sxs-lookup"><span data-stu-id="99a0b-117">**TSATTRID\_OTHERS**</span></span>                 | <span data-ttu-id="99a0b-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="99a0b-118">Not used.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="99a0b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99a0b-119">Requirements</span></span>



| <span data-ttu-id="99a0b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="99a0b-120">Requirement</span></span> | <span data-ttu-id="99a0b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="99a0b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99a0b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99a0b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="99a0b-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99a0b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="99a0b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99a0b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="99a0b-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99a0b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99a0b-126">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="99a0b-126">Redistributable</span></span><br/>          | <span data-ttu-id="99a0b-127">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="99a0b-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="99a0b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99a0b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="99a0b-129"><dt>TsAttrid. h</dt></span><span class="sxs-lookup"><span data-stu-id="99a0b-129"><dt>TsAttrid.h</dt></span></span> </dl> |



 

