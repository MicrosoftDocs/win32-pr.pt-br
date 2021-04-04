---
title: Constantes de WINBIO_CAPABILITY (WinBio \_ Types. h)
description: Subtipos de sensor de impressão digital.
ms.assetid: D447273E-2A02-484E-B0E4-69FEADD15797
topic_type:
- apiref
api_name:
- WINBIO_CAPABILITY_SENSOR
- WINBIO_CAPABILITY_MATCHING
- WINBIO_CAPABILITY_DATABASE
- WINBIO_CAPABILITY_PROCESSING
- WINBIO_CAPABILITY_ENCRYPTION
- WINBIO_CAPABILITY_NAVIGATION
- WINBIO_CAPABILITY_INDICATOR
- WINBIO_CAPABILITY_VIRTUAL_SENSOR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16de3f496e5c3723722bb7aae22c81eb27c968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824432"
---
# <a name="winbio_capability-constants"></a><span data-ttu-id="4e04e-103">\_Constantes de recurso WINBIO</span><span class="sxs-lookup"><span data-stu-id="4e04e-103">WINBIO\_CAPABILITY Constants</span></span>

<span data-ttu-id="4e04e-104">Os seguintes subtipos de sensor de impressão digital são valores de **\_ recursos WINBIO** que podem ser usados como bitmask para o parâmetro *Capabilities* da estrutura de [**\_ \_ esquema de unidade WINBIO**](winbio-unit-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="4e04e-104">The following fingerprint sensor sub types are **WINBIO\_CAPABILITIES** values that can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="4e04e-105">Eles se referem aos recursos do sensor integrado.</span><span class="sxs-lookup"><span data-stu-id="4e04e-105">These refer to the onboard sensor capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4e04e-106">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="4e04e-106">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4e04e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e04e-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_SENSOR"></span><span id="winbio_capability_sensor"></span><dl> <span data-ttu-id="4e04e-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="4e04e-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e04e-109">O sensor pode capturar dados biométricos.</span><span class="sxs-lookup"><span data-stu-id="4e04e-109">The sensor can capture biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_MATCHING"></span><span id="winbio_capability_matching"></span><dl> <span data-ttu-id="4e04e-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="4e04e-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e04e-111">O sensor pode corresponder dados biométricos a uma identidade.</span><span class="sxs-lookup"><span data-stu-id="4e04e-111">The sensor can match biometric data to an identity.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_DATABASE"></span><span id="winbio_capability_database"></span><dl> <span data-ttu-id="4e04e-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="4e04e-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e04e-113">O sensor contém um banco de dados integrado.</span><span class="sxs-lookup"><span data-stu-id="4e04e-113">The sensor contains an onboard database.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_PROCESSING"></span><span id="winbio_capability_processing"></span><dl> <span data-ttu-id="4e04e-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="4e04e-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e04e-115">O sensor pode executar o processamento biométrico.</span><span class="sxs-lookup"><span data-stu-id="4e04e-115">The sensor can perform biometric processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_ENCRYPTION"></span><span id="winbio_capability_encryption"></span><dl> <span data-ttu-id="4e04e-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="4e04e-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e04e-117">O sensor pode criptografar dados biométricos.</span><span class="sxs-lookup"><span data-stu-id="4e04e-117">The sensor can encrypt biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_NAVIGATION"></span><span id="winbio_capability_navigation"></span><dl> <span data-ttu-id="4e04e-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="4e04e-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e04e-119">O sensor pode atuar como um mouse pad.</span><span class="sxs-lookup"><span data-stu-id="4e04e-119">The sensor can act as a mouse pad.</span></span> <span data-ttu-id="4e04e-120">Não há suporte para esse recurso no momento.</span><span class="sxs-lookup"><span data-stu-id="4e04e-120">This is currently not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_INDICATOR"></span><span id="winbio_capability_indicator"></span><dl> <span data-ttu-id="4e04e-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="4e04e-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e04e-122">O sensor contém uma luz do indicador.</span><span class="sxs-lookup"><span data-stu-id="4e04e-122">The sensor contains an indicator light.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_VIRTUAL_SENSOR"></span><span id="winbio_capability_virtual_sensor"></span><dl> <span data-ttu-id="4e04e-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="4e04e-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e04e-124">O adaptador do sensor gerencia sua própria conexão com o hardware biométrico.</span><span class="sxs-lookup"><span data-stu-id="4e04e-124">The sensor adapter manages its own connection to the biometric hardware.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e04e-125">Essa constante se aplica somente ao Windows 10 e posterior.</span><span class="sxs-lookup"><span data-stu-id="4e04e-125">This constant applies only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="4e04e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e04e-126">Requirements</span></span>



| <span data-ttu-id="4e04e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e04e-127">Requirement</span></span> | <span data-ttu-id="4e04e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4e04e-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e04e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e04e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4e04e-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e04e-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="4e04e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e04e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4e04e-132">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="4e04e-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                  |
| <span data-ttu-id="4e04e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e04e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e04e-134"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="4e04e-134"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e04e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e04e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e04e-136">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="4e04e-136">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="4e04e-137">**\_esquema de unidade WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4e04e-137">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





