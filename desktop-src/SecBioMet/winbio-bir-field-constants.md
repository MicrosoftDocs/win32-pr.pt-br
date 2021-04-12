---
title: Constantes de WINBIO_BIR_FIELD (WinBio \_ Types. h)
description: Especifique um bitmask.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295794"
---
# <a name="winbio_bir_field-constants"></a><span data-ttu-id="cc66c-103">\_Constantes do \_ campo WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="cc66c-103">WINBIO\_BIR\_FIELD Constants</span></span>

<span data-ttu-id="cc66c-104">As constantes a seguir são usadas para criar um bitmask para o membro **ValidFields** da estrutura de [**\_ \_ cabeçalho WINBIO Bir**](winbio-bir-header.md) .</span><span class="sxs-lookup"><span data-stu-id="cc66c-104">The following constants are used to create a bitmask for the **ValidFields** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="cc66c-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="cc66c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="cc66c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc66c-106">Description</span></span>                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <span data-ttu-id="cc66c-107"><dt>**WINBIO \_ 0x0001 \_ de \_ \_ contagem de subtítulos de campo Bir**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-107"><dt>**WINBIO\_BIR\_FIELD\_SUBHEAD\_COUNT**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="cc66c-108">Fornecido para conformidade com o NISTIR 6529-a, o formato de Patron da estrutura de formatos de intercâmbio biométrico comum (CBEFF), mas não é usado.</span><span class="sxs-lookup"><span data-stu-id="cc66c-108">Provided for conformity with NISTIR 6529-A, the Common Biometric Exchange Formats Framework (CBEFF) Patron Format A, but not used.</span></span><br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <span data-ttu-id="cc66c-109"><dt>**WINBIO \_ \_ID de \_ produto \_ do campo Bir**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-109"><dt>**WINBIO\_BIR\_FIELD\_PRODUCT\_ID**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="cc66c-110">O membro **ProductID** é válido.</span><span class="sxs-lookup"><span data-stu-id="cc66c-110">The **ProductId** member is valid.</span></span><br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <span data-ttu-id="cc66c-111"><dt>**WINBIO \_ BIR \_ campo \_ Patron \_ ID**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-111"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_ID**</dt> <dt>0x0004</dt></span></span> </dl>                                      | <span data-ttu-id="cc66c-112">Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.</span><span class="sxs-lookup"><span data-stu-id="cc66c-112">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <span data-ttu-id="cc66c-113"><dt>**WINBIO \_ \_ \_ Índice de campo Bir**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-113"><dt>**WINBIO\_BIR\_FIELD\_INDEX**</dt> <dt>0x0008</dt></span></span> </dl>                                                   | <span data-ttu-id="cc66c-114">Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.</span><span class="sxs-lookup"><span data-stu-id="cc66c-114">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <span data-ttu-id="cc66c-115"><dt>**WINBIO \_ 0x0010 \_ de \_ \_ data de criação do campo Bir**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-115"><dt>**WINBIO\_BIR\_FIELD\_CREATION\_DATE**</dt> <dt>0x0010</dt></span></span> </dl>                          | <span data-ttu-id="cc66c-116">O membro **CreationDate** é válido.</span><span class="sxs-lookup"><span data-stu-id="cc66c-116">The **CreationDate** member is valid.</span></span><br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <span data-ttu-id="cc66c-117"><dt>**WINBIO \_ \_Período de \_ validade \_ do campo Bir**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-117"><dt>**WINBIO\_BIR\_FIELD\_VALIDITY\_PERIOD**</dt> <dt>0x0020</dt></span></span> </dl>                    | <span data-ttu-id="cc66c-118">O membro **ValidityPeriod** é válido.</span><span class="sxs-lookup"><span data-stu-id="cc66c-118">The **ValidityPeriod** member is valid.</span></span><br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <span data-ttu-id="cc66c-119"><dt>**WINBIO \_ BIR \_ de \_ \_ tipo biométrico de campo**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-119"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_TYPE**</dt> <dt>0x0040</dt></span></span> </dl>                       | <span data-ttu-id="cc66c-120">O membro de **tipo** é válido.</span><span class="sxs-lookup"><span data-stu-id="cc66c-120">The **Type** member is valid.</span></span><br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <span data-ttu-id="cc66c-121"><dt>**WINBIO \_ BIR \_ de \_ \_ subtipo de campo biométrico**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-121"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_SUBTYPE**</dt> <dt>0x0080</dt></span></span> </dl>              | <span data-ttu-id="cc66c-122">O membro do **subtipo** é válido.</span><span class="sxs-lookup"><span data-stu-id="cc66c-122">The **Subtype** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <span data-ttu-id="cc66c-123"><dt>**WINBIO \_ BIR \_ Field \_ CBEFF \_ header \_ versão**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-123"><dt>**WINBIO\_BIR\_FIELD\_CBEFF\_HEADER\_VERSION**</dt> <dt>0x0100</dt></span></span> </dl>    | <span data-ttu-id="cc66c-124">O membro **HeaderVersion** é válido.</span><span class="sxs-lookup"><span data-stu-id="cc66c-124">The **HeaderVersion** member is valid.</span></span><br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <span data-ttu-id="cc66c-125"><dt>**WINBIO \_ BIR \_ Field \_ Patron \_ header \_ versão**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-125"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_HEADER\_VERSION**</dt> <dt>0x0200</dt></span></span> </dl> | <span data-ttu-id="cc66c-126">O membro **PatronHeaderVersion** é válido.</span><span class="sxs-lookup"><span data-stu-id="cc66c-126">The **PatronHeaderVersion** member is valid.</span></span><br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <span data-ttu-id="cc66c-127"><dt>**WINBIO \_ BIR \_ de \_ \_ finalidade biométrica**</dt> <dt>0x0400</dt> do campo</span><span class="sxs-lookup"><span data-stu-id="cc66c-127"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_PURPOSE**</dt> <dt>0x0400</dt></span></span> </dl>              | <span data-ttu-id="cc66c-128">O membro de **finalidade** é válido.</span><span class="sxs-lookup"><span data-stu-id="cc66c-128">The **Purpose** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <span data-ttu-id="cc66c-129"><dt>**WINBIO \_ BIR \_ \_ \_ condição biométrica do campo**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-129"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_CONDITION**</dt> <dt>0x0800</dt></span></span> </dl>        | <span data-ttu-id="cc66c-130">Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.</span><span class="sxs-lookup"><span data-stu-id="cc66c-130">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <span data-ttu-id="cc66c-131"><dt>**WINBIO \_ BIR \_ \_ qualidade do campo**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-131"><dt>**WINBIO\_BIR\_FIELD\_QUALITY**</dt> <dt>0x1000</dt></span></span> </dl>                                             | <span data-ttu-id="cc66c-132">O membro **dataquality** é válido.</span><span class="sxs-lookup"><span data-stu-id="cc66c-132">The **DataQuality** member is valid.</span></span><br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <span data-ttu-id="cc66c-133"><dt>**WINBIO \_ 0x2000 do BIR \_ Field \_ Creator**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-133"><dt>**WINBIO\_BIR\_FIELD\_CREATOR**</dt> <dt>0x2000</dt></span></span> </dl>                                             | <span data-ttu-id="cc66c-134">Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.</span><span class="sxs-lookup"><span data-stu-id="cc66c-134">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <span data-ttu-id="cc66c-135"><dt>**WINBIO \_ BIR \_ \_ desafio de campo**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-135"><dt>**WINBIO\_BIR\_FIELD\_CHALLENGE**</dt> <dt>0x4000</dt></span></span> </dl>                                       | <span data-ttu-id="cc66c-136">Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.</span><span class="sxs-lookup"><span data-stu-id="cc66c-136">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <span data-ttu-id="cc66c-137"><dt>**WINBIO \_ BIR \_ de \_ carga de campo**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-137"><dt>**WINBIO\_BIR\_FIELD\_PAYLOAD**</dt> <dt>0x8000</dt></span></span> </dl>                                             | <span data-ttu-id="cc66c-138">Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.</span><span class="sxs-lookup"><span data-stu-id="cc66c-138">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="cc66c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc66c-139">Requirements</span></span>



| <span data-ttu-id="cc66c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc66c-140">Requirement</span></span> | <span data-ttu-id="cc66c-141">Valor</span><span class="sxs-lookup"><span data-stu-id="cc66c-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc66c-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc66c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cc66c-143">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cc66c-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="cc66c-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc66c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cc66c-145">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="cc66c-145">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cc66c-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc66c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc66c-147"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc66c-147"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc66c-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc66c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc66c-149">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="cc66c-149">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





