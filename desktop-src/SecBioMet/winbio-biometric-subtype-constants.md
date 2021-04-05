---
title: Constantes de WINBIO_BIOMETRIC_SUBTYPE (WinBio \_ Types. h)
description: Forneça informações sobre uma medição biométrica.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918671"
---
# <a name="winbio_biometric_subtype-constants"></a><span data-ttu-id="f7f98-103">\_Constantes de SUBtipo de biometria WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="f7f98-103">WINBIO\_BIOMETRIC\_SUBTYPE Constants</span></span>

<span data-ttu-id="f7f98-104">**WINBIO \_ As constantes de \_ SUBtipo biométrica** são usadas em todo o Windows Biometric Framework para fornecer informações adicionais sobre uma medição biométrica.</span><span class="sxs-lookup"><span data-stu-id="f7f98-104">**WINBIO\_BIOMETRIC\_SUBTYPE** constants are used throughout the Windows Biometric Framework to provide additional information about a biometric measurement.</span></span> <span data-ttu-id="f7f98-105">As constantes a seguir podem ser usadas quando nenhum subtipo é necessário ou quando qualquer subtipo é necessário.</span><span class="sxs-lookup"><span data-stu-id="f7f98-105">The following constants can be used when no subtype is required or when any subtype is required.</span></span>



| <span data-ttu-id="f7f98-106">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="f7f98-106">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="f7f98-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7f98-107">Description</span></span>                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <span data-ttu-id="f7f98-108"><dt>**WINBIO \_ Subtipo \_ nenhuma \_ informação**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="f7f98-108"><dt>**WINBIO\_SUBTYPE\_NO\_INFORMATION**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="f7f98-109">Nenhuma informação de subtipo.</span><span class="sxs-lookup"><span data-stu-id="f7f98-109">No subtype information.</span></span><br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <span data-ttu-id="f7f98-110"><dt>**WINBIO \_ Subtipo \_ qualquer**</dt> <dt>0xFF</dt></span><span class="sxs-lookup"><span data-stu-id="f7f98-110"><dt>**WINBIO\_SUBTYPE\_ANY**</dt> <dt>0xFF</dt></span></span> </dl>                                   | <span data-ttu-id="f7f98-111">Qualquer subtipo.</span><span class="sxs-lookup"><span data-stu-id="f7f98-111">Any subtype.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="f7f98-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7f98-112">Remarks</span></span>

<span data-ttu-id="f7f98-113">Para localizar os subtipos de biometria disponíveis para um tipo biométrico específico, use a seguinte tabela:</span><span class="sxs-lookup"><span data-stu-id="f7f98-113">To find the available biometric subtypes for a particular biometric type, use the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f7f98-114">Valor <strong>WINBIO_BIOMETRIC_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="f7f98-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> value</span></span></th>
<th><span data-ttu-id="f7f98-115">Tópico (s) para localizar <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> valores</span><span class="sxs-lookup"><span data-stu-id="f7f98-115">Topic(s) to find <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f7f98-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span><span class="sxs-lookup"><span data-stu-id="f7f98-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span></span></td>
<td><span data-ttu-id="f7f98-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE constantes</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="f7f98-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="f7f98-118">Esses valores se aplicam somente ao Windows 10 e posterior.</span><span class="sxs-lookup"><span data-stu-id="f7f98-118">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7f98-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span><span class="sxs-lookup"><span data-stu-id="f7f98-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span></span></td>
<td><span data-ttu-id="f7f98-120">Um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f7f98-120">One of the following topics:</span></span>
<ul>
<li><span data-ttu-id="f7f98-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT constantes</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7f98-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT Constants</strong></a></span></span></li>
<li><span data-ttu-id="f7f98-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG constantes</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7f98-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG Constants</strong></a></span></span></li>
<li><span data-ttu-id="f7f98-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ constantes</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7f98-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ Constants</strong></a></span></span></li>
<li><span data-ttu-id="f7f98-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE constantes</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7f98-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE Constants</strong></a></span></span></li>
<li><span data-ttu-id="f7f98-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS constantes</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7f98-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS Constants</strong></a></span></span></li>
<li><span data-ttu-id="f7f98-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS constantes de impressão digital</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7f98-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerprint Constants</strong></a></span></span></li>
<li><span data-ttu-id="f7f98-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm constantes</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7f98-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm Constants</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7f98-128"><strong>WINBIO_TYPE_IRIS</strong></span><span class="sxs-lookup"><span data-stu-id="f7f98-128"><strong>WINBIO_TYPE_IRIS</strong></span></span></td>
<td><span data-ttu-id="f7f98-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS constantes</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="f7f98-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="f7f98-130">Esses valores se aplicam somente ao Windows 10 e posterior.</span><span class="sxs-lookup"><span data-stu-id="f7f98-130">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7f98-131"><strong>WINBIO_TYPE_VOICE</strong></span><span class="sxs-lookup"><span data-stu-id="f7f98-131"><strong>WINBIO_TYPE_VOICE</strong></span></span></td>
<td><span data-ttu-id="f7f98-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE constantes</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="f7f98-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="f7f98-133">Esses valores se aplicam somente ao Windows 10 e posterior.</span><span class="sxs-lookup"><span data-stu-id="f7f98-133">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f7f98-134">Para obter mais informações, consulte [constantes do aplicativo cliente](client-application-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f7f98-134">For more information, see [Client Application Constants](client-application-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7f98-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7f98-135">Requirements</span></span>



| <span data-ttu-id="f7f98-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7f98-136">Requirement</span></span> | <span data-ttu-id="f7f98-137">Valor</span><span class="sxs-lookup"><span data-stu-id="f7f98-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f98-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7f98-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f7f98-139">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f7f98-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f7f98-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7f98-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f7f98-141">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f7f98-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f7f98-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7f98-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7f98-143"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7f98-143"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





