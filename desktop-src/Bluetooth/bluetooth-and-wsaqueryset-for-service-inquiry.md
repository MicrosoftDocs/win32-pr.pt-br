---
title: Bluetooth e WSAQUERYSET para consulta de serviço
description: Usando a estrutura WSAQUERYSET com as funções WSALookupServiceBegin e WSALookupServiceNext para obter informações sobre o processo de consulta de serviço.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth e WSAQUERYSET para consulta de serviço Bluetooth
- WSAQUERYSET Bluetooth, para consulta de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642325"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a><span data-ttu-id="c09bd-105">Bluetooth e WSAQUERYSET para consulta de serviço</span><span class="sxs-lookup"><span data-stu-id="c09bd-105">Bluetooth and WSAQUERYSET for Service Inquiry</span></span>

<span data-ttu-id="c09bd-106">O Bluetooth usa a estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , com várias funções, para facilitar a descoberta de dispositivos e serviços no namespace do Bluetooth, NS \_ BTH.</span><span class="sxs-lookup"><span data-stu-id="c09bd-106">Bluetooth uses the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure, with various functions, to facilitate the discovery of devices and services in the Bluetooth namespace, NS\_BTH.</span></span>

<span data-ttu-id="c09bd-107">As funções [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usam a estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obter dados sobre o processo de consulta de serviço.</span><span class="sxs-lookup"><span data-stu-id="c09bd-107">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) and [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) functions use the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to obtain data about the service inquiry process.</span></span> <span data-ttu-id="c09bd-108">A tabela a seguir descreve como definir os valores de membro na estrutura **WSAQUERYSET** para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="c09bd-108">The following table describes how to set the member values in the **WSAQUERYSET** structure for this purpose.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c09bd-109">Membro</span><span class="sxs-lookup"><span data-stu-id="c09bd-109">Member</span></span></th>
<th><span data-ttu-id="c09bd-110">Entrada para WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="c09bd-110">Input to WSALookupServiceBegin</span></span></th>
<th><span data-ttu-id="c09bd-111">Valor retornado de WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="c09bd-111">Returned value from WSALookupServiceNext</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c09bd-112"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-112"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="c09bd-113">Deve ser definido como <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="c09bd-113">Must be set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
<td><span data-ttu-id="c09bd-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) retornado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="c09bd-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) returned by system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09bd-115"><strong>dwOutputFlags</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-115"><strong>dwOutputFlags</strong></span></span></td>
<td><span data-ttu-id="c09bd-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-116">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-117">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c09bd-118"><strong>lpszServiceInstanceName</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-118"><strong>lpszServiceInstanceName</strong></span></span></td>
<td><span data-ttu-id="c09bd-119">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-119">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-120">Nome de exibição do serviço, convertido como uma cadeia de caracteres codificada em UTF-8 da codificação de idioma padrão do atributo SDP do ServiceName do Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="c09bd-120">Display name of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceName SDP attribute.</span></span> <span data-ttu-id="c09bd-121">Retornado se LUP_RETURN_NAME for especificado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-121">Returned if LUP_RETURN_NAME is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09bd-122"><strong>lpServiceClassId</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-122"><strong>lpServiceClassId</strong></span></span></td>
<td><span data-ttu-id="c09bd-123">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c09bd-123">Required.</span></span> <span data-ttu-id="c09bd-124">O UUID de Bluetooth único mais específico para os serviços para os quais a pesquisa está sendo realizada.</span><span class="sxs-lookup"><span data-stu-id="c09bd-124">The most specific single Bluetooth UUID for the services for which the search is being conducted.</span></span> <span data-ttu-id="c09bd-125">Por exemplo, se esse valor for definido como o UUID do protocolo L2CAP, ele retornará todos os serviços usando o protocolo L2CAP no dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="c09bd-125">For example, if this value is set to the UUID of the L2CAP protocol, it returns all services using the L2CAP protocol on the target device.</span></span> <span data-ttu-id="c09bd-126">Se definido como o UUID de um serviço específico, ele retornará apenas as instâncias desse serviço.</span><span class="sxs-lookup"><span data-stu-id="c09bd-126">If set to the UUID of a specific service, it would return only the instances of that service.</span></span></td>
<td><span data-ttu-id="c09bd-127">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-127">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c09bd-128"><strong>lpVersion</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-128"><strong>lpVersion</strong></span></span></td>
<td><span data-ttu-id="c09bd-129">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-129">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-130">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-130">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09bd-131"><strong>lpszComment</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-131"><strong>lpszComment</strong></span></span></td>
<td><span data-ttu-id="c09bd-132">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-132">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-133">Descrição do serviço, convertido como uma cadeia de caracteres codificada em UTF-8 da codificação de idioma padrão do atributo SDP ServiceDescription do Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="c09bd-133">Description of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceDescription SDP attribute.</span></span> <span data-ttu-id="c09bd-134">Retornado se <strong>LUP_RETURN_COMMENT</strong> for especificado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-134">Returned if <strong>LUP_RETURN_COMMENT</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c09bd-135"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-135"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="c09bd-136">Deve ser NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="c09bd-136">Must be NS_BTH.</span></span></td>
<td><span data-ttu-id="c09bd-137">Retorna NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="c09bd-137">Returns NS_BTH.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09bd-138"><strong>lpNSProviderId</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-138"><strong>lpNSProviderId</strong></span></span></td>
<td><span data-ttu-id="c09bd-139">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-139">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-140">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-140">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c09bd-141"><strong>lpszContext</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-141"><strong>lpszContext</strong></span></span></td>
<td><span data-ttu-id="c09bd-142">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c09bd-142">Required.</span></span> <span data-ttu-id="c09bd-143">O endereço do dispositivo Bluetooth com o qual estabelecer uma conexão SDP e consultar serviços.</span><span class="sxs-lookup"><span data-stu-id="c09bd-143">The Bluetooth Device Address with which to establish an SDP connection and query for services.</span></span> <span data-ttu-id="c09bd-144">Esse valor deve ser uma cadeia de caracteres que foi convertida usando a chamada de função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c09bd-144">This value must be a string that was converted by using the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> function call.</span></span> <span data-ttu-id="c09bd-145">Se o endereço do dispositivo Bluetooth local for fornecido, o banco de dados SDP local será pesquisado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-145">If the local Bluetooth device address is provided, the local SDP database is searched.</span></span></td>
<td><span data-ttu-id="c09bd-146">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-146">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09bd-147"><strong>dwNumberOfProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-147"><strong>dwNumberOfProtocols</strong></span></span></td>
<td><span data-ttu-id="c09bd-148">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-148">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-149">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-149">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c09bd-150"><strong>lpafpProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-150"><strong>lpafpProtocols</strong></span></span></td>
<td><span data-ttu-id="c09bd-151">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-151">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-152">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-152">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09bd-153"><strong>lpszQueryString</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-153"><strong>lpszQueryString</strong></span></span></td>
<td><span data-ttu-id="c09bd-154">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-154">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-155">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-155">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c09bd-156"><strong>dwNumberOfCsAddrs</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-156"><strong>dwNumberOfCsAddrs</strong></span></span></td>
<td><span data-ttu-id="c09bd-157">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-157">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-158">Indica o número de elementos na matriz de estruturas de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c09bd-158">Indicates the number of elements in the array of <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09bd-159"><strong>lpcsaBuffer</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-159"><strong>lpcsaBuffer</strong></span></span></td>
<td><span data-ttu-id="c09bd-160">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-160">Not used.</span></span></td>
<td><span data-ttu-id="c09bd-161">Ponteiro para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> cujo membro <strong>localaddr. lpSockAddr</strong> aponta para uma <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> que contém o endereço de conexão completo do serviço remoto, convertido da primeira entrada do atributo de SDP de ProtocolDescriptorList do Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="c09bd-161">Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structure whose <strong>LocalAddr.lpSockaddr</strong> member points to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> that contains the complete connectable address of the remote service, converted from the first entry of the Bluetooth ProtocolDescriptorList SDP attribute.</span></span> <span data-ttu-id="c09bd-162">Retornado se <strong>LUP_RETURN_ADDR</strong> for especificado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-162">Returned if <strong>LUP_RETURN_ADDR</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c09bd-163"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="c09bd-163"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="c09bd-164">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c09bd-164">Optional.</span></span> <span data-ttu-id="c09bd-165">Ponteiro para uma estrutura de <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> que contém parâmetros avançados para limitar os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c09bd-165">Pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> structure that contains advanced parameters to limit the results of the search.</span></span> <span data-ttu-id="c09bd-166">Se fornecido, <strong>lpServiceClassId</strong> será ignorado e as consultas em cache não serão executadas com sucesso.</span><span class="sxs-lookup"><span data-stu-id="c09bd-166">If provided, <strong>lpServiceClassId</strong> is ignored and cached queries do not succeed.</span></span></td>
<td><ul>
<li><span data-ttu-id="c09bd-167">Se uma pesquisa de serviço for executada: ponteiro para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> que retorna os identificadores de serviço.</span><span class="sxs-lookup"><span data-stu-id="c09bd-167">If a service search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the service handles.</span></span> <span data-ttu-id="c09bd-168">(<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ULong) calcula o número de identificadores.</span><span class="sxs-lookup"><span data-stu-id="c09bd-168">(<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calculates the number of handles.</span></span> <span data-ttu-id="c09bd-169"><strong>BLOB. pBlobData</strong> é uma matriz de valores ULONG que representa os identificadores de serviço.</span><span class="sxs-lookup"><span data-stu-id="c09bd-169"><strong>BLOB.pBlobData</strong> is an array of ULONG values representing the service handles.</span></span></li>
<li><span data-ttu-id="c09bd-170">Se uma pesquisa de atributo ou ServiceAttribute for executada: ponteiro para uma estrutura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blob</strong></a> que retorna o registro SDP binário.</span><span class="sxs-lookup"><span data-stu-id="c09bd-170">If an attribute or serviceAttribute search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the binary SDP record.</span></span> <span data-ttu-id="c09bd-171"><strong>BLOB. cbSize</strong> é o tamanho do registro SDP binário.</span><span class="sxs-lookup"><span data-stu-id="c09bd-171"><strong>BLOB.cbSize</strong> is the size of the binary SDP record.</span></span> <span data-ttu-id="c09bd-172"><strong>BLOB. pBlobData</strong> aponta para o próprio registro.</span><span class="sxs-lookup"><span data-stu-id="c09bd-172"><strong>BLOB.pBlobData</strong> points to the record itself.</span></span> <span data-ttu-id="c09bd-173">O registro de SDP binário é necessário em muitos casos porque apenas um número limitado de atributos SDP pode ser convertido na estrutura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> e somente as cadeias de caracteres UTF-8 codificadas por padrão são convertidas.</span><span class="sxs-lookup"><span data-stu-id="c09bd-173">The binary SDP record is necessary in many cases because only a limited number of SDP attributes are able to be converted to the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure, and only default encoded UTF-8 strings are converted.</span></span> <span data-ttu-id="c09bd-174">As funções para auxiliar na análise do registro SDP binário são fornecidas na seção de <a href="bluetooth-reference.md">referência do Bluetooth</a> .</span><span class="sxs-lookup"><span data-stu-id="c09bd-174">Functions to assist in parsing the binary SDP record are provided in the <a href="bluetooth-reference.md">Bluetooth Reference</a> section.</span></span></li>
<li><span data-ttu-id="c09bd-175">Retornado se LUP_RETURN_BLOB for especificado.</span><span class="sxs-lookup"><span data-stu-id="c09bd-175">Returned if LUP_RETURN_BLOB is specified.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c09bd-176">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c09bd-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c09bd-177">Bluetooth e WSAQUERYSET para o serviço set</span><span class="sxs-lookup"><span data-stu-id="c09bd-177">Bluetooth and WSAQUERYSET for Set Service</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[<span data-ttu-id="c09bd-178">Bluetooth e WSAQUERYSET para consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c09bd-178">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="c09bd-179">Bluetooth e BLOB</span><span class="sxs-lookup"><span data-stu-id="c09bd-179">Bluetooth and BLOB</span></span>](bluetooth-and-blob.md)
</dt> <dt>

[<span data-ttu-id="c09bd-180">Bluetooth e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="c09bd-180">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

<span data-ttu-id="c09bd-181">Bluetooth e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="c09bd-181">Bluetooth and WSALookupServiceNext</span></span>
</dt> <dt>

[<span data-ttu-id="c09bd-182">Referência de Bluetooth</span><span class="sxs-lookup"><span data-stu-id="c09bd-182">Bluetooth Reference</span></span>](bluetooth-reference.md)
</dt> <dt>

[<span data-ttu-id="c09bd-183">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="c09bd-183">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="c09bd-184">**\_serviço de consulta do BTH \_**</span><span class="sxs-lookup"><span data-stu-id="c09bd-184">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="c09bd-185">**informações de CSADDR \_**</span><span class="sxs-lookup"><span data-stu-id="c09bd-185">**CSADDR\_INFO**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[<span data-ttu-id="c09bd-186">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="c09bd-186">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="c09bd-187">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="c09bd-187">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="c09bd-188">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="c09bd-188">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="c09bd-189">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="c09bd-189">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 