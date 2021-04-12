---
title: Funções do Windows Defender
description: Funções chamadas por aplicativos para solicitar verificações, atualizações de assinatura ou informações do Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365485"
---
# <a name="windows-defender-functions"></a><span data-ttu-id="523b2-103">Funções do Windows Defender</span><span class="sxs-lookup"><span data-stu-id="523b2-103">Windows Defender Functions</span></span>

<span data-ttu-id="523b2-104">Funções chamadas por aplicativos para solicitar verificações, atualizações de assinatura ou informações do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="523b2-104">Functions called by apps to request scans, signature updates, or information from Windows Defender.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="523b2-105">Função</span><span class="sxs-lookup"><span data-stu-id="523b2-105">Function</span></span></th>
<th><span data-ttu-id="523b2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="523b2-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="523b2-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span></span></td>
<td><span data-ttu-id="523b2-108">Retorna uma mensagem de erro formatada com base em um código de erro.</span><span class="sxs-lookup"><span data-stu-id="523b2-108">Returns a formatted error message based on an error code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523b2-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span></span></td>
<td><span data-ttu-id="523b2-110">Libera memória para o Gerenciador de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="523b2-110">Frees memory for the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="523b2-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span></span></td>
<td><span data-ttu-id="523b2-112">Fecha o identificador retornado por <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>ou <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="523b2-112">Closes the handle returned by <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>, or <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523b2-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span></span></td>
<td><span data-ttu-id="523b2-114">Estabelece uma conexão com o Malware Protection Manager no computador local.</span><span class="sxs-lookup"><span data-stu-id="523b2-114">Establishes a connection to the malware protection manager on the local computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="523b2-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span></span></td>
<td><span data-ttu-id="523b2-116"><strong>Sem suporte.</strong></span><span class="sxs-lookup"><span data-stu-id="523b2-116"><strong>Not supported.</strong></span></span> <span data-ttu-id="523b2-117">Retorna informações de status sobre vários componentes do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="523b2-117">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523b2-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span></span></td>
<td><span data-ttu-id="523b2-119">Retorna informações de status sobre vários componentes do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="523b2-119">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="523b2-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span></span></td>
<td><span data-ttu-id="523b2-121">Retorna informações de versão sobre vários componentes do Gerenciador de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="523b2-121">Returns version information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523b2-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span></span></td>
<td><span data-ttu-id="523b2-123">Permite o controle de uma verificação que foi iniciada de forma assíncrona via <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="523b2-123">Allows the control of a scan that was asynchronously initiated via <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="523b2-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span></span></td>
<td><span data-ttu-id="523b2-125">Inicia uma operação de verificação.</span><span class="sxs-lookup"><span data-stu-id="523b2-125">Starts a scanning operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523b2-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span></span></td>
<td><span data-ttu-id="523b2-127">Retorna informações sobre a próxima ameaça na lista de enumeração.</span><span class="sxs-lookup"><span data-stu-id="523b2-127">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="523b2-128">Essa função pode ser chamada repetidamente até que a enumeração de todas as ameaças seja concluída.</span><span class="sxs-lookup"><span data-stu-id="523b2-128">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="523b2-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span></span></td>
<td><span data-ttu-id="523b2-130">Retorna um identificador de enumeração para a finalidade de recuperar ameaças.</span><span class="sxs-lookup"><span data-stu-id="523b2-130">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="523b2-131">Essa função pode ser usada para abrir ameaças detectadas por uma verificação específica, todas as ameaças ativas no sistema, o histórico de desinfecção de ameaças ou todas as ameaças presentes no banco de dados de assinatura.</span><span class="sxs-lookup"><span data-stu-id="523b2-131">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523b2-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span></span></td>
<td><span data-ttu-id="523b2-133">Usado para consultar informações estáticas (como severidade e categoria) ou localizadas (como descrição da categoria e conselhos) sobre uma determinada ameaça.</span><span class="sxs-lookup"><span data-stu-id="523b2-133">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="523b2-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span></span></td>
<td><span data-ttu-id="523b2-135">Permite o controle de uma operação de atualização de assinatura que foi iniciada de forma assíncrona via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="523b2-135">Allows the control of a signature update operation that was asynchronously initiated via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523b2-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span></span></td>
<td><span data-ttu-id="523b2-137">Inicia uma operação de atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="523b2-137">Starts a signature update operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="523b2-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span></span></td>
<td><span data-ttu-id="523b2-139">Altera o status do Windows Defender para ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="523b2-139">Changes Windows Defender status to on or off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="523b2-140">A partir do Windows 10, versão 1607 e Windows Server 2016, a função <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> sempre retorna <strong>E_NOTIMPL</strong>.</span><span class="sxs-lookup"><span data-stu-id="523b2-140">Beginning in Windows 10, version 1607 and Windows Server 2016, the <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> function always returns <strong>E_NOTIMPL</strong>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523b2-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="523b2-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span></span></td>
<td><span data-ttu-id="523b2-142">Retorna o status atual do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="523b2-142">Returns the current status of Windows Defender.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





