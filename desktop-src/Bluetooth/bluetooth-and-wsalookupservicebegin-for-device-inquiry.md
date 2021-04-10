---
title: Bluetooth e WSALookupServiceBegin para consulta de dispositivo
description: Este tópico descreve como usar a função WSALookupServiceBegin para executar uma consulta de dispositivos visíveis e fantasmas. Para obter mais informações, consulte descobrindo dispositivos e serviços Bluetooth.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth e WSALookupServiceBegin para consulta de dispositivo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104084960"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a><span data-ttu-id="2cf91-105">Bluetooth e WSALookupServiceBegin para consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2cf91-105">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>

<span data-ttu-id="2cf91-106">Este tópico descreve como usar a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para executar uma consulta de dispositivos visíveis e fantasmas.</span><span class="sxs-lookup"><span data-stu-id="2cf91-106">This topic describes how to use the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function to perform an inquiry of both visible and ghosted devices.</span></span> <span data-ttu-id="2cf91-107">Para obter mais informações, consulte [descobrindo dispositivos e serviços Bluetooth](discovering-bluetooth-devices-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="2cf91-107">For more information, see [Discovering Bluetooth Devices and Services](discovering-bluetooth-devices-and-services.md).</span></span>

<span data-ttu-id="2cf91-108">A função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) em seu primeiro parâmetro, *lpqsRestrictions*, para definir critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="2cf91-108">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function uses a [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure in its first parameter, *lpqsRestrictions*, to define search criteria.</span></span> <span data-ttu-id="2cf91-109">O Bluetooth fornece diretrizes específicas para o uso da função **WSALookupServiceBegin** e do **WSAQUERYSET**.</span><span class="sxs-lookup"><span data-stu-id="2cf91-109">Bluetooth provides specific guidelines for use of the **WSALookupServiceBegin** function and **WSAQUERYSET**.</span></span>

<span data-ttu-id="2cf91-110">A tabela a seguir lista as restrições que se aplicam à estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passada para o parâmetro *lpqsRestrictions* ao consultar dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2cf91-110">The following table lists restrictions that apply to the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed to the *lpqsRestrictions* parameter when querying for devices.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2cf91-111">Membro WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="2cf91-111">WSAQUERYSET member</span></span></th>
<th><span data-ttu-id="2cf91-112">Restrição</span><span class="sxs-lookup"><span data-stu-id="2cf91-112">Restriction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2cf91-113"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="2cf91-113"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="2cf91-114">Defina como <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="2cf91-114">Set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cf91-115"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="2cf91-115"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="2cf91-116">Esse membro contém um ponteiro opcional para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2cf91-116">This member contains an optional pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure.</span></span> <span data-ttu-id="2cf91-117">Se esse membro for especificado, os parâmetros de consulta do dispositivo válidos para <strong>LUP_FLUSHCACHE</strong> serão os seguintes:</span><span class="sxs-lookup"><span data-stu-id="2cf91-117">If this member is specified, the valid device inquire parameters for <strong>LUP_FLUSHCACHE</strong> are as follows:</span></span>
<ul>
<li><span data-ttu-id="2cf91-118">O membro <strong>cbSize</strong> da estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> deve ser <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span><span class="sxs-lookup"><span data-stu-id="2cf91-118">The <strong>cbSize</strong> member of the <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure must be <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span></span></li>
<li><span data-ttu-id="2cf91-119">O membro <strong>pBlobData</strong> é um ponteiro para uma estrutura de <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , para o qual o membro de <strong>LAP</strong> é o código de acesso de consulta Bluetooth, e <strong>o comprimento do membro é</strong> o comprimento, em segundos, da consulta.</span><span class="sxs-lookup"><span data-stu-id="2cf91-119">The <strong>pBlobData</strong> member is a pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> structure, for which the <strong>LAP</strong> member is the Bluetooth inquiry access code, and the <strong>length</strong> member is the length, in seconds, of the inquiry.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cf91-120"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="2cf91-120"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="2cf91-121">Defina como <strong>NS_BTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="2cf91-121">Set to <strong>NS_BTH</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cf91-122">Outros membros</span><span class="sxs-lookup"><span data-stu-id="2cf91-122">Other members</span></span></td>
<td><span data-ttu-id="2cf91-123">Outros membros da estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> são ignorados.</span><span class="sxs-lookup"><span data-stu-id="2cf91-123">Other members of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure are ignored.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2cf91-124">Os sinalizadores listados na tabela a seguir são usados no parâmetro *dwControlFlags* para controlar os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="2cf91-124">The flags listed in the following table are used in the *dwControlFlags* parameter to control the query results.</span></span> <span data-ttu-id="2cf91-125">Os **\_ contêineres Lup** e sinalizadores **Lup \_ FLUSHCACHE** são usados pela função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ; o restante dos sinalizadores é usado em chamadas para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="2cf91-125">The **LUP\_CONTAINERS** and **LUP\_FLUSHCACHE** flags are used by the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function; the rest of the flags are used in calls to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span>

| <span data-ttu-id="2cf91-126">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="2cf91-126">Flag</span></span>               | <span data-ttu-id="2cf91-127">Resultado</span><span class="sxs-lookup"><span data-stu-id="2cf91-127">Result</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf91-128">\_contêineres de Lup</span><span class="sxs-lookup"><span data-stu-id="2cf91-128">LUP\_CONTAINERS</span></span>    | <span data-ttu-id="2cf91-129">Especifica que a finalidade da consulta é obter uma lista de dispositivos Bluetooth e não uma lista de serviços.</span><span class="sxs-lookup"><span data-stu-id="2cf91-129">Specifies that the query purpose is to obtain a list of Bluetooth devices and not a list of services.</span></span> <span data-ttu-id="2cf91-130">Esse sinalizador deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="2cf91-130">This flag must be set.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2cf91-131">LUP \_ FLUSHCACHE</span><span class="sxs-lookup"><span data-stu-id="2cf91-131">LUP\_FLUSHCACHE</span></span>    | <span data-ttu-id="2cf91-132">Dispara uma consulta de dispositivos locais ou faz com que os resultados em cache de consultas anteriores sejam retornados.</span><span class="sxs-lookup"><span data-stu-id="2cf91-132">Triggers an inquiry of local devices or causes cached results from previous queries to be returned.</span></span>                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="2cf91-133">\_tipo de retorno Lup \_</span><span class="sxs-lookup"><span data-stu-id="2cf91-133">LUP\_RETURN\_TYPE</span></span>  | <span data-ttu-id="2cf91-134">Retorne o Bluetooth COD (classe de bits de dispositivo) diretamente no membro **lpServiceClassId** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="2cf91-134">Return the Bluetooth COD (class of device bits) directly in the **lpServiceClassId** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="2cf91-135">O COD é mapeado para o membro **dados1** do GUID.</span><span class="sxs-lookup"><span data-stu-id="2cf91-135">The COD is mapped to the **Data1** member of the GUID.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="2cf91-136">\_serviço Lup res \_</span><span class="sxs-lookup"><span data-stu-id="2cf91-136">LUP\_RES\_SERVICE</span></span>  | <span data-ttu-id="2cf91-137">Retornar informações para o endereço local do Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="2cf91-137">Return information for the local Bluetooth address.</span></span> <span data-ttu-id="2cf91-138">Esse sinalizador terá efeito somente se o **\_ \_ endereço de retorno de Lup** também for especificado.</span><span class="sxs-lookup"><span data-stu-id="2cf91-138">This flag has an effect only if **LUP\_RETURN\_ADDR** is also specified.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2cf91-139">LUP \_ nome de retorno \_</span><span class="sxs-lookup"><span data-stu-id="2cf91-139">LUP\_RETURN\_NAME</span></span>  | <span data-ttu-id="2cf91-140">Retorne o nome de exibição do dispositivo no membro **lpszServiceInstanceName** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada chamada para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="2cf91-140">Return the display name of the device in the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="2cf91-141">Esse sinalizador também deve ser especificado para recuperar o **nome** membro da estrutura [**de \_ \_ informações do dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) ao especificar o sinalizador de **retorno de \_ \_ blob Lup** .</span><span class="sxs-lookup"><span data-stu-id="2cf91-141">This flag must also be specified to retrieve the **name** member of the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure when specifying the **LUP\_RETURN\_BLOB** flag.</span></span> |
| <span data-ttu-id="2cf91-142">\_endereço de retorno de Lup \_</span><span class="sxs-lookup"><span data-stu-id="2cf91-142">LUP\_RETURN\_ADDR</span></span>  | <span data-ttu-id="2cf91-143">Retorne uma estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) que contém o endereço de 48 bits do par no membro **lpcsaBuffer** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada chamada para a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="2cf91-143">Return a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure that contains the 48-bit address of the peer in the **lpcsaBuffer** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="2cf91-144">Outros membros na estrutura **SOCKADDR \_ BTH** estarão vazios.</span><span class="sxs-lookup"><span data-stu-id="2cf91-144">Other members in the **SOCKADDR\_BTH** structure will be empty.</span></span>                                                            |
| <span data-ttu-id="2cf91-145">\_blob de retorno de Lup \_</span><span class="sxs-lookup"><span data-stu-id="2cf91-145">LUP\_RETURN\_BLOB</span></span>  | <span data-ttu-id="2cf91-146">Retorne a estrutura de [**\_ \_ informações do dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) em cada chamada subsequente para [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="2cf91-146">Return the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure on each subsequent call to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2cf91-147">LUP \_ FLUSHPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="2cf91-147">LUP\_FLUSHPREVIOUS</span></span> | <span data-ttu-id="2cf91-148">Ignore o próximo dispositivo disponível e retorne o dispositivo que o segue.</span><span class="sxs-lookup"><span data-stu-id="2cf91-148">Skip the next available device, and return the device that follows it.</span></span>                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="2cf91-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2cf91-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cf91-150">Bluetooth e WSALookupServiceBegin para descoberta de serviço</span><span class="sxs-lookup"><span data-stu-id="2cf91-150">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="2cf91-151">Bluetooth e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="2cf91-151">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="2cf91-152">Bluetooth e WSAQUERYSET para consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2cf91-152">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="2cf91-153">Descobrir dispositivos e serviços Bluetooth</span><span class="sxs-lookup"><span data-stu-id="2cf91-153">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="2cf91-154">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="2cf91-154">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="2cf91-155">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="2cf91-155">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="2cf91-156">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="2cf91-156">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="2cf91-157">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="2cf91-157">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="2cf91-158">**\_dispositivo de consulta BTH \_**</span><span class="sxs-lookup"><span data-stu-id="2cf91-158">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="2cf91-159">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="2cf91-159">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="2cf91-160">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="2cf91-160">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="2cf91-161">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="2cf91-161">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 