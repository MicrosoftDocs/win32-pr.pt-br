---
description: Os sinalizadores na tabela a seguir especificam o status de uma sessão do Gerenciador de proteção de saída (OPM).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Sinalizadores de status OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502262"
---
# <a name="opm-status-flags"></a><span data-ttu-id="f61ad-103">Sinalizadores de status OPM</span><span class="sxs-lookup"><span data-stu-id="f61ad-103">OPM Status Flags</span></span>

<span data-ttu-id="f61ad-104">Os sinalizadores na tabela a seguir especificam o status de uma sessão do Gerenciador de proteção de saída (OPM).</span><span class="sxs-lookup"><span data-stu-id="f61ad-104">The flags in the following table specify the status of an Output Protection Manager (OPM) session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f61ad-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="f61ad-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f61ad-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f61ad-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <span data-ttu-id="f61ad-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span><span class="sxs-lookup"><span data-stu-id="f61ad-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f61ad-108">Status normal.</span><span class="sxs-lookup"><span data-stu-id="f61ad-108">Normal status.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <span data-ttu-id="f61ad-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span><span class="sxs-lookup"><span data-stu-id="f61ad-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f61ad-110">A integridade da conexão foi comprometida.</span><span class="sxs-lookup"><span data-stu-id="f61ad-110">The integrity of the connection has been compromised.</span></span> <span data-ttu-id="f61ad-111">Exemplos de eventos que fazem com que o driver defina esse sinalizador incluem:</span><span class="sxs-lookup"><span data-stu-id="f61ad-111">Examples of events that cause the driver to set this flag include:</span></span><br/>
<ul>
<li><span data-ttu-id="f61ad-112">O driver não pode mais impor o nível de proteção atual.</span><span class="sxs-lookup"><span data-stu-id="f61ad-112">The driver can no longer enforce the current protection level.</span></span></li>
<li><span data-ttu-id="f61ad-113">O driver detectou um erro de integridade interno.</span><span class="sxs-lookup"><span data-stu-id="f61ad-113">The driver detected an internal integrity error.</span></span></li>
<li><span data-ttu-id="f61ad-114">O conector entre o computador e o dispositivo de vídeo foi desconectado.</span><span class="sxs-lookup"><span data-stu-id="f61ad-114">The connector between the computer and the display device was unplugged.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <span data-ttu-id="f61ad-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span><span class="sxs-lookup"><span data-stu-id="f61ad-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f61ad-116">A configuração de conexão foi alterada.</span><span class="sxs-lookup"><span data-stu-id="f61ad-116">The connection configuration has changed.</span></span> <span data-ttu-id="f61ad-117">Por exemplo, o usuário alterou o modo de exibição da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f61ad-117">For example, the user has changed the desktop display mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <span data-ttu-id="f61ad-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span><span class="sxs-lookup"><span data-stu-id="f61ad-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f61ad-119">O adaptador gráfico ou o driver foi adulterado.</span><span class="sxs-lookup"><span data-stu-id="f61ad-119">The graphics adapter or the driver has been tampered with.</span></span><br/> <span data-ttu-id="f61ad-120">Esse sinalizador não é usado no <em>modo de emulação Copp</em>.</span><span class="sxs-lookup"><span data-stu-id="f61ad-120">This flag is not used in <em>COPP emulation mode</em>.</span></span> <span data-ttu-id="f61ad-121">Em vez disso, a saída de vídeo definirá o sinalizador OPM_STATUS_LINK_LOST se detectar violação.</span><span class="sxs-lookup"><span data-stu-id="f61ad-121">Instead, the video output will set the OPM_STATUS_LINK_LOST flag if it detects tampering.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <span data-ttu-id="f61ad-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span><span class="sxs-lookup"><span data-stu-id="f61ad-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f61ad-123">Um dispositivo de Proteção de Conteúdo Digital High-Bandwidth revogado (HDCP) é anexado à saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f61ad-123">A revoked High-Bandwidth Digital Content Protection (HDCP) device is attached to the video output.</span></span><br/> <span data-ttu-id="f61ad-124">Esse sinalizador de status pode ser retornado de uma consulta <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> ou <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> .</span><span class="sxs-lookup"><span data-stu-id="f61ad-124">This status flag can be returned from an <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> or <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> query.</span></span> <br/> <span data-ttu-id="f61ad-125">O dispositivo revogado pode ser anexado diretamente à saída de vídeo ou indiretamente por meio de um repetidor HDCP.</span><span class="sxs-lookup"><span data-stu-id="f61ad-125">The revoked device might be attached directly to the video output, or indirectly through an HDCP repeater.</span></span> <span data-ttu-id="f61ad-126">Uma saída de vídeo é necessária para detectar essa condição enquanto a HDCP está habilitada, mas não de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f61ad-126">A video output is required to detect this condition while HDCP is enabled, but not otherwise.</span></span><br/> <span data-ttu-id="f61ad-127">Esse sinalizador não é usado no <em>modo de emulação de Copp</em>, pois a saída de vídeo não detecta dispositivos revogados nesse modo.</span><span class="sxs-lookup"><span data-stu-id="f61ad-127">This flag is not used in <em>COPP emulation mode</em>, because the video output does not detect revoked devices in that mode.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="f61ad-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="f61ad-128">Remarks</span></span>

<span data-ttu-id="f61ad-129">Algumas dessas constantes são equivalentes aos valores da enumeração **Copp \_ StatusFlags** usada no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="f61ad-129">Some of these constants are equivalent to values from the **COPP\_StatusFlags** enumeration used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="f61ad-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f61ad-130">Requirements</span></span>



| <span data-ttu-id="f61ad-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f61ad-131">Requirement</span></span> | <span data-ttu-id="f61ad-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f61ad-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f61ad-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f61ad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f61ad-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f61ad-134">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f61ad-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f61ad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f61ad-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f61ad-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f61ad-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f61ad-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f61ad-138"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f61ad-138"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f61ad-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f61ad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61ad-140">Enumerações de OPM</span><span class="sxs-lookup"><span data-stu-id="f61ad-140">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




