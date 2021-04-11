---
description: Descreve o tipo de dados do valor associado a uma marca.
ms.assetid: 009ad522-35da-4053-a7f6-61d7d240b98c
title: Tipos de marca
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab53b9c3b85263ddcdbe80e3979d576685bd73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163944"
---
# <a name="tag-types"></a><span data-ttu-id="31671-103">Tipos de marca</span><span class="sxs-lookup"><span data-stu-id="31671-103">TAG Types</span></span>

<span data-ttu-id="31671-104">Descreve o tipo de dados do valor associado a uma marca.</span><span class="sxs-lookup"><span data-stu-id="31671-104">Describes the data type of the value associated with a TAG.</span></span>



| <span data-ttu-id="31671-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="31671-105">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="31671-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="31671-106">Description</span></span>                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span id="TAG_TYPE_NULL"></span><span id="tag_type_null"></span><dl> <span data-ttu-id="31671-107"><dt>**Marca \_ de Digite \_**</dt> o <dt>0x1000</dt> nulo</span><span class="sxs-lookup"><span data-stu-id="31671-107"><dt>**TAG\_TYPE\_NULL**</dt> <dt>0x1000</dt></span></span> </dl>                | <span data-ttu-id="31671-108">Não há nenhum valor associado à marca.</span><span class="sxs-lookup"><span data-stu-id="31671-108">There is no value associated with the TAG.</span></span><br/> |
| <span id="TAG_TYPE_BYTE"></span><span id="tag_type_byte"></span><dl> <span data-ttu-id="31671-109"><dt>**Marca \_ de 0x2000 de tipo \_ byte**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="31671-109"><dt>**TAG\_TYPE\_BYTE**</dt> <dt>0x2000</dt></span></span> </dl>                | <span data-ttu-id="31671-110">Um valor de **byte** .</span><span class="sxs-lookup"><span data-stu-id="31671-110">A **BYTE** value.</span></span><br/>                          |
| <span id="TAG_TYPE_WORD"></span><span id="tag_type_word"></span><dl> <span data-ttu-id="31671-111"><dt>**Marca \_ de Digite o \_ Word**</dt> <dt>0x3000</dt></span><span class="sxs-lookup"><span data-stu-id="31671-111"><dt>**TAG\_TYPE\_WORD**</dt> <dt>0x3000</dt></span></span> </dl>                | <span data-ttu-id="31671-112">Um valor de **palavra** .</span><span class="sxs-lookup"><span data-stu-id="31671-112">A **WORD** value.</span></span><br/>                          |
| <span id="TAG_TYPE_DWORD"></span><span id="tag_type_dword"></span><dl> <span data-ttu-id="31671-113"><dt>**Marca \_ de Digite \_ DWORD**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="31671-113"><dt>**TAG\_TYPE\_DWORD**</dt> <dt>0x4000</dt></span></span> </dl>             | <span data-ttu-id="31671-114">Um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="31671-114">A **DWORD** value.</span></span><br/>                         |
| <span id="TAG_TYPE_QWORD"></span><span id="tag_type_qword"></span><dl> <span data-ttu-id="31671-115"><dt>**Marca \_ de Digite \_ QWORD**</dt> <dt>0x5000</dt></span><span class="sxs-lookup"><span data-stu-id="31671-115"><dt>**TAG\_TYPE\_QWORD**</dt> <dt>0x5000</dt></span></span> </dl>             | <span data-ttu-id="31671-116">Um valor de **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="31671-116">A **ULONGLONG** value.</span></span><br/>                     |
| <span id="TAG_TYPE_STRINGREF"></span><span id="tag_type_stringref"></span><dl> <span data-ttu-id="31671-117"><dt>**Marca \_ de Digite \_ STRINGREF**</dt> <dt>0x6000</dt></span><span class="sxs-lookup"><span data-stu-id="31671-117"><dt>**TAG\_TYPE\_STRINGREF**</dt> <dt>0x6000</dt></span></span> </dl> | <span data-ttu-id="31671-118">Um valor de cadeia de caracteres com token.</span><span class="sxs-lookup"><span data-stu-id="31671-118">A tokenized string value.</span></span><br/>                  |
| <span id="TAG_TYPE_LIST"></span><span id="tag_type_list"></span><dl> <span data-ttu-id="31671-119"><dt>**Marca \_ de \_Lista de tipos**</dt> <dt>0x7000</dt></span><span class="sxs-lookup"><span data-stu-id="31671-119"><dt>**TAG\_TYPE\_LIST**</dt> <dt>0x7000</dt></span></span> </dl>                | <span data-ttu-id="31671-120">Uma lista de valores de marca.</span><span class="sxs-lookup"><span data-stu-id="31671-120">A list of TAG values.</span></span><br/>                      |
| <span id="TAG_TYPE_STRING"></span><span id="tag_type_string"></span><dl> <span data-ttu-id="31671-121"><dt>**Marca \_ de \_Cadeia de caracteres de tipo**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="31671-121"><dt>**TAG\_TYPE\_STRING**</dt> <dt>0x8000</dt></span></span> </dl>          | <span data-ttu-id="31671-122">Um valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="31671-122">A string value.</span></span><br/>                            |
| <span id="TAG_TYPE_BINARY"></span><span id="tag_type_binary"></span><dl> <span data-ttu-id="31671-123"><dt>**Marca \_ de TIPO \_**</dt> <dt>0x9000</dt> binário</span><span class="sxs-lookup"><span data-stu-id="31671-123"><dt>**TAG\_TYPE\_BINARY**</dt> <dt>0x9000</dt></span></span> </dl>          | <span data-ttu-id="31671-124">Um valor binário.</span><span class="sxs-lookup"><span data-stu-id="31671-124">A binary value.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="31671-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31671-125">Requirements</span></span>



| <span data-ttu-id="31671-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="31671-126">Requirement</span></span> | <span data-ttu-id="31671-127">Valor</span><span class="sxs-lookup"><span data-stu-id="31671-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31671-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31671-128">Minimum supported client</span></span><br/> | <span data-ttu-id="31671-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31671-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="31671-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31671-130">Minimum supported server</span></span><br/> | <span data-ttu-id="31671-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31671-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31671-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="31671-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31671-133">**Tags**</span><span class="sxs-lookup"><span data-stu-id="31671-133">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="31671-134">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="31671-134">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="31671-135">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="31671-135">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




