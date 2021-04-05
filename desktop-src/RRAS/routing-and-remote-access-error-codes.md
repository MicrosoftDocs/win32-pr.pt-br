---
title: Códigos de erro de roteamento e acesso remoto
description: Os códigos de erro da API RRAS (roteamento e acesso remoto) a seguir são definidos em Raserror. h.
ms.assetid: 1fa41438-7c93-4e9c-851c-652fba23da4f
topic_type:
- apiref
api_name:
- Routing and Remote Access Error Codes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15966d009f0690a1db24c21460da5b9e08a38347
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009049"
---
# <a name="routing-and-remote-access-error-codes"></a><span data-ttu-id="870d7-103">Códigos de erro de roteamento e acesso remoto</span><span class="sxs-lookup"><span data-stu-id="870d7-103">Routing and Remote Access Error Codes</span></span>

<span data-ttu-id="870d7-104">Os códigos de erro da API RRAS (roteamento e acesso remoto) a seguir são definidos em Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="870d7-104">The following Routing and Remote Access (RRAS) API error codes are defined in raserror.h.</span></span> <span data-ttu-id="870d7-105">Todos os códigos de erro têm suporte no Windows 2000 ou em versões posteriores do Windows, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="870d7-105">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="870d7-106">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="870d7-106">Return code/value</span></span></th>
<th><span data-ttu-id="870d7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="870d7-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="PENDING"></span><span id="pending"></span><dl> <span data-ttu-id="870d7-108"><dt><strong></strong></dt> <dt>600</dt> pendente </span><span class="sxs-lookup"><span data-stu-id="870d7-108"><dt><strong>PENDING</strong></dt> <dt>600</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-109">Uma operação está pendente.</span><span class="sxs-lookup"><span data-stu-id="870d7-109">An operation is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PORT_HANDLE"></span><span id="error_invalid_port_handle"></span><dl> <span data-ttu-id="870d7-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-111">O identificador de porta fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-111">The port handle supplied is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_ALREADY_OPEN"></span><span id="error_port_already_open"></span><dl> <span data-ttu-id="870d7-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-113">A porta especificada já está aberta.</span><span class="sxs-lookup"><span data-stu-id="870d7-113">The specified port is already open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BUFFER_TOO_SMALL"></span><span id="error_buffer_too_small"></span><dl> <span data-ttu-id="870d7-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-115">O buffer fornecido é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="870d7-115">The buffer supplied is too small.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_INFO_SPECIFIED"></span><span id="error_wrong_info_specified"></span><dl> <span data-ttu-id="870d7-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-117">As informações de porta especificadas estão incorretas.</span><span class="sxs-lookup"><span data-stu-id="870d7-117">The port information specified is incorrect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SET_PORT_INFO"></span><span id="error_cannot_set_port_info"></span><dl> <span data-ttu-id="870d7-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-119">Não é possível definir as informações de porta especificadas.</span><span class="sxs-lookup"><span data-stu-id="870d7-119">The port information specified cannot be set.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-120">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-120">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_CONNECTED"></span><span id="error_port_not_connected"></span><dl> <span data-ttu-id="870d7-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-122">A porta especificada não está conectada.</span><span class="sxs-lookup"><span data-stu-id="870d7-122">The port specified is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EVENT_INVALID"></span><span id="error_event_invalid"></span><dl> <span data-ttu-id="870d7-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-124">Foi detectado um evento inválido.</span><span class="sxs-lookup"><span data-stu-id="870d7-124">An event that is not valid was detected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-125">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-125">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_DOES_NOT_EXIST"></span><span id="error_device_does_not_exist"></span><dl> <span data-ttu-id="870d7-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-127">O dispositivo especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="870d7-127">The specified device does not exist.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICETYPE_DOES_NOT_EXIST"></span><span id="error_devicetype_does_not_exist"></span><dl> <span data-ttu-id="870d7-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-129">O tipo de dispositivo especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="870d7-129">The specified device type does not exist.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUFFER_INVALID"></span><span id="error_buffer_invalid"></span><dl> <span data-ttu-id="870d7-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-131">O buffer fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-131">The buffer supplied is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTE_NOT_AVAILABLE"></span><span id="error_route_not_available"></span><dl> <span data-ttu-id="870d7-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-133">Foi especificada uma rota que não está disponível.</span><span class="sxs-lookup"><span data-stu-id="870d7-133">A route was specified that is not available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-134">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-134">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ROUTE_NOT_ALLOCATED"></span><span id="error_route_not_allocated"></span><dl> <span data-ttu-id="870d7-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-136">A rota especificada não está alocada.</span><span class="sxs-lookup"><span data-stu-id="870d7-136">The specified route is not allocated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERRERROR_INVALID_COMPRESSION_SPECIFIED"></span><span id="errerror_invalid_compression_specified"></span><dl> <span data-ttu-id="870d7-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-138">A compactação especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="870d7-138">The specified compression is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-139">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-139">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OUT_OF_BUFFERS"></span><span id="error_out_of_buffers"></span><dl> <span data-ttu-id="870d7-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-141">Havia buffers insuficientes disponíveis.</span><span class="sxs-lookup"><span data-stu-id="870d7-141">There were insufficient buffers available.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_FOUND_"></span><span id="error_port_not_found_"></span><dl> <span data-ttu-id="870d7-142"><dt> <strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-142"><dt><strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-143">A porta especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="870d7-143">The specified port was not found.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ASYNC_REQUEST_PENDING"></span><span id="error_async_request_pending"></span><dl> <span data-ttu-id="870d7-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-145">Uma solicitação assíncrona está pendente.</span><span class="sxs-lookup"><span data-stu-id="870d7-145">An asynchronous request is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_DISCONNECTING"></span><span id="error_already_disconnecting"></span><dl> <span data-ttu-id="870d7-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-147">A porta ou o dispositivo especificado já está se desconectando.</span><span class="sxs-lookup"><span data-stu-id="870d7-147">The specified port or device is already disconnecting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_OPEN"></span><span id="error_port_not_open"></span><dl> <span data-ttu-id="870d7-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-149">A porta especificada não está aberta.</span><span class="sxs-lookup"><span data-stu-id="870d7-149">The specified port is not open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_DISCONNECTED"></span><span id="error_port_disconnected"></span><dl> <span data-ttu-id="870d7-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-151">A porta especificada está desconectada.</span><span class="sxs-lookup"><span data-stu-id="870d7-151">The specified port is disconnected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ENDPOINTS"></span><span id="error_no_endpoints"></span><dl> <span data-ttu-id="870d7-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-153">Não foi possível determinar nenhum ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="870d7-153">No endpoints could be determined.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-154">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-154">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_OPEN_PHONEBOOK"></span><span id="error_cannot_open_phonebook"></span><dl> <span data-ttu-id="870d7-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-156">Não é possível abrir o arquivo de catálogo telefônico especificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-156">Cannot open the specified phone book file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_PHONEBOOK"></span><span id="error_cannot_load_phonebook"></span><dl> <span data-ttu-id="870d7-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-158">Não é possível carregar o arquivo de catálogo telefônico especificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-158">Cannot load the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_FIND_PHONEBOOK_ENTRY"></span><span id="error_cannot_find_phonebook_entry"></span><dl> <span data-ttu-id="870d7-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-160">Não é possível localizar a entrada do catálogo telefônico especificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-160">Cannot find the specified phone book entry.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_WRITE_PHONEBOOK"></span><span id="error_cannot_write_phonebook"></span><dl> <span data-ttu-id="870d7-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-162">Não é possível gravar no arquivo de catálogo telefônico especificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-162">Cannot write to the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CORRUPT_PHONEBOOK"></span><span id="error_corrupt_phonebook"></span><dl> <span data-ttu-id="870d7-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-164">As informações encontradas no catálogo telefônico especificado não são válidas.</span><span class="sxs-lookup"><span data-stu-id="870d7-164">Information found in the specified phone book is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_STRING"></span><span id="error_cannot_load_string"></span><dl> <span data-ttu-id="870d7-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-166">Não foi possível carregar uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="870d7-166">A string could not be loaded.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-167">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-167">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_KEY_NOT_FOUND"></span><span id="error_key_not_found"></span><dl> <span data-ttu-id="870d7-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-169">Não é possível localizar a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="870d7-169">Cannot find the specified key.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DISCONNECTION"></span><span id="error_disconnection"></span><dl> <span data-ttu-id="870d7-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-171">A porta especificada foi desconectada.</span><span class="sxs-lookup"><span data-stu-id="870d7-171">The specified port was disconnected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_DISCONNECTION"></span><span id="error_remote_disconnection"></span><dl> <span data-ttu-id="870d7-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-173">A porta especificada foi desconectada pelo computador remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-173">The specified port was disconnected by the remote computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HARDWARE_FAILURE"></span><span id="error_hardware_failure"></span><dl> <span data-ttu-id="870d7-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-175">A porta especificada foi desconectada devido a uma falha de hardware.</span><span class="sxs-lookup"><span data-stu-id="870d7-175">The specified port was disconnected due to hardware failure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_DISCONNECTION"></span><span id="error_user_disconnection"></span><dl> <span data-ttu-id="870d7-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-177">A porta especificada foi desconectada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="870d7-177">The specified port was disconnected by the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIZE"></span><span id="error_invalid_size"></span><dl> <span data-ttu-id="870d7-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-179">Tamanho de estrutura incorreto.</span><span class="sxs-lookup"><span data-stu-id="870d7-179">Incorrect structure size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_AVAILABLE"></span><span id="error_port_not_available"></span><dl> <span data-ttu-id="870d7-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-181">A porta especificada já está em uso ou não está configurada para acesso remoto dial-out.</span><span class="sxs-lookup"><span data-stu-id="870d7-181">The specified port is already in use or is not configured for remote access dial-out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_PROJECT_CLIENT"></span><span id="error_cannot_project_client"></span><dl> <span data-ttu-id="870d7-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-183">Seu computador não pôde ser registrado na rede remota.</span><span class="sxs-lookup"><span data-stu-id="870d7-183">Your computer could not be registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-184">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-184">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN"></span><span id="error_unknown"></span><dl> <span data-ttu-id="870d7-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-186">Ocorreu um erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="870d7-186">An unknown error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_DEVICE_ATTACHED"></span><span id="error_wrong_device_attached"></span><dl> <span data-ttu-id="870d7-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-188">O dispositivo errado está conectado à porta especificada.</span><span class="sxs-lookup"><span data-stu-id="870d7-188">The wrong device is attached to the specified port.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_STRING"></span><span id="error_bad_string"></span><dl> <span data-ttu-id="870d7-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-190">Foi detectada uma cadeia de caracteres que não pôde ser convertida.</span><span class="sxs-lookup"><span data-stu-id="870d7-190">A string was detected that could not be converted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-191">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-191">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REQUEST_TIMEOUT"></span><span id="error_request_timeout"></span><dl> <span data-ttu-id="870d7-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-193">O tempo limite da solicitação foi atingido.</span><span class="sxs-lookup"><span data-stu-id="870d7-193">The request has timed out.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_GET_LANA"></span><span id="error_cannot_get_lana"></span><dl> <span data-ttu-id="870d7-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-195">Nenhuma rede assíncrona está disponível.</span><span class="sxs-lookup"><span data-stu-id="870d7-195">No asynchronous net is available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-196">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-196">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NETBIOS_ERROR"></span><span id="error_netbios_error"></span><dl> <span data-ttu-id="870d7-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-198">Ocorreu um erro envolvendo o NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="870d7-198">An error has occurred involving NetBIOS.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-199">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-199">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_OUT_OF_RESOURCES"></span><span id="error_server_out_of_resources"></span><dl> <span data-ttu-id="870d7-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-201">o servidor de ti não pode alocar os recursos de NetBIOS necessários para dar suporte ao cliente.</span><span class="sxs-lookup"><span data-stu-id="870d7-201">he server cannot allocate NetBIOS resources needed to support the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-202">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-202">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NAME_EXISTS_ON_NET"></span><span id="error_name_exists_on_net"></span><dl> <span data-ttu-id="870d7-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-204">Um dos nomes NetBIOS do seu computador já está registrado na rede remota.</span><span class="sxs-lookup"><span data-stu-id="870d7-204">One of your computer's NetBIOS names is already registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-205">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-205">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_GENERAL_NET_FAILURE"></span><span id="error_server_general_net_failure"></span><dl> <span data-ttu-id="870d7-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-207">Falha em um adaptador de rede no servidor.</span><span class="sxs-lookup"><span data-stu-id="870d7-207">A network adapter at the server failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-208">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-208">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_MSG_ALIAS_NOT_ADDED"></span><span id="warning_msg_alias_not_added"></span><dl> <span data-ttu-id="870d7-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-210">Você não receberá pop-ups de mensagem de rede.</span><span class="sxs-lookup"><span data-stu-id="870d7-210">You will not receive network message popups.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-211">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-211">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_INTERNAL"></span><span id="error_auth_internal"></span><dl> <span data-ttu-id="870d7-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-213">Ocorreu um erro interno de autenticação.</span><span class="sxs-lookup"><span data-stu-id="870d7-213">An internal authentication error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RESTRICTED_LOGON_HOURS"></span><span id="error_restricted_logon_hours"></span><dl> <span data-ttu-id="870d7-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-215">A conta especificada não tem permissão para fazer logon nesta hora do dia.</span><span class="sxs-lookup"><span data-stu-id="870d7-215">The specified account is not permitted to log in at this time of day.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCT_DISABLED"></span><span id="error_acct_disabled"></span><dl> <span data-ttu-id="870d7-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-217">A conta especificada está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="870d7-217">The specified account is disabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PASSWD_EXPIRED"></span><span id="error_passwd_expired"></span><dl> <span data-ttu-id="870d7-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-219">A senha especificada expirou.</span><span class="sxs-lookup"><span data-stu-id="870d7-219">The specified password has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_DIALIN_PERMISSION"></span><span id="error_no_dialin_permission"></span><dl> <span data-ttu-id="870d7-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-221">A conta especificada não tem permissões de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-221">The specified account does not have remote access permissions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_NOT_RESPONDING"></span><span id="error_server_not_responding"></span><dl> <span data-ttu-id="870d7-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-223">O servidor de acesso remoto não está respondendo.</span><span class="sxs-lookup"><span data-stu-id="870d7-223">The remote access server is not responding.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-224">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-224">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FROM_DEVICE"></span><span id="error_from_device"></span><dl> <span data-ttu-id="870d7-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-226">O modem ou outro dispositivo de conexão relatou um erro.</span><span class="sxs-lookup"><span data-stu-id="870d7-226">Your modem or other connection device has reported an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNRECOGNIZED_RESPONSE"></span><span id="error_unrecognized_response"></span><dl> <span data-ttu-id="870d7-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-228">Uma resposta não reconhecida foi retornada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="870d7-228">An unrecognized response was returned by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MACRO_NOT_FOUND"></span><span id="error_macro_not_found"></span><dl> <span data-ttu-id="870d7-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-230">Uma macro exigida pelo dispositivo não foi encontrada no dispositivo. Seção de arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="870d7-230">A macro required by the device was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MACRO_NOT_DEFINED"></span><span id="error_macro_not_defined"></span><dl> <span data-ttu-id="870d7-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-232">Um comando ou resposta no dispositivo. A seção arquivo INF refere-se a uma macro indefinida.</span><span class="sxs-lookup"><span data-stu-id="870d7-232">A command or response in the device .INF file section refers to an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MESSAGE_MACRO_NOT_FOUND"></span><span id="error_message_macro_not_found"></span><dl> <span data-ttu-id="870d7-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-234">A <message> macro não foi encontrada no dispositivo. Seção de arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="870d7-234">The <message> macro was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEFAULTOFF_MACRO_NOT_FOUND"></span><span id="error_defaultoff_macro_not_found"></span><dl> <span data-ttu-id="870d7-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-236">A <defaultoff> macro no dispositivo. A seção arquivo INF contém uma macro indefinida.</span><span class="sxs-lookup"><span data-stu-id="870d7-236">The <defaultoff> macro in the device .INF file section contains an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FILE_COULD_NOT_BE_OPENED"></span><span id="error_file_could_not_be_opened"></span><dl> <span data-ttu-id="870d7-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-238">O dispositivo. Não foi possível abrir o arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="870d7-238">The device .INF file could not be opened.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICENAME_TOO_LONG"></span><span id="error_devicename_too_long"></span><dl> <span data-ttu-id="870d7-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-240">O nome do dispositivo no dispositivo. INF ou mídia. O arquivo INI é muito longo.</span><span class="sxs-lookup"><span data-stu-id="870d7-240">The device name in the device .INF or media .INI file is too long.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICENAME_NOT_FOUND"></span><span id="error_devicename_not_found"></span><dl> <span data-ttu-id="870d7-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-242">A mídia. O arquivo INI refere-se a um nome de dispositivo desconhecido.</span><span class="sxs-lookup"><span data-stu-id="870d7-242">The media .INI file refers to an unknown device name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RESPONSES"></span><span id="error_no_responses"></span><dl> <span data-ttu-id="870d7-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-244">O dispositivo. O arquivo INF não contém nenhuma resposta para o comando.</span><span class="sxs-lookup"><span data-stu-id="870d7-244">The device .INF file contains no responses for the command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_COMMAND_FOUND"></span><span id="error_no_command_found"></span><dl> <span data-ttu-id="870d7-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-246">O dispositivo. O arquivo INF não tem um comando.</span><span class="sxs-lookup"><span data-stu-id="870d7-246">The device .INF file is missing a command.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_KEY_SPECIFIED"></span><span id="error_wrong_key_specified"></span><dl> <span data-ttu-id="870d7-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-248">Tentativa de definir uma macro não listada no dispositivo. Seção de arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="870d7-248">Attempted to set a macro not listed in device .INF file section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN_DEVICE_TYPE"></span><span id="error_unknown_device_type"></span><dl> <span data-ttu-id="870d7-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-250">A mídia. O arquivo INI refere-se a um tipo de dispositivo desconhecido.</span><span class="sxs-lookup"><span data-stu-id="870d7-250">The media .INI file refers to an unknown device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALLOCATING_MEMORY"></span><span id="error_allocating_memory"></span><dl> <span data-ttu-id="870d7-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-252">Não é possível alocar memória.</span><span class="sxs-lookup"><span data-stu-id="870d7-252">Cannot allocate memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_CONFIGURED"></span><span id="error_port_not_configured"></span><dl> <span data-ttu-id="870d7-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-254">A porta não está configurada para acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-254">The port is not configured for remote access.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_NOT_READY"></span><span id="error_device_not_ready"></span><dl> <span data-ttu-id="870d7-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-256">Seu modem ou outro dispositivo de conexão não está funcionando.</span><span class="sxs-lookup"><span data-stu-id="870d7-256">Your modem or other connection device is not functioning.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_INI_FILE"></span><span id="error_reading_ini_file"></span><dl> <span data-ttu-id="870d7-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-258">Não é possível ler a mídia. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="870d7-258">Cannot read the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CONNECTION"></span><span id="error_no_connection"></span><dl> <span data-ttu-id="870d7-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-260">A conexão foi eliminada.</span><span class="sxs-lookup"><span data-stu-id="870d7-260">The connection was dropped.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_USAGE_IN_INI_FILE"></span><span id="error_bad_usage_in_ini_file"></span><dl> <span data-ttu-id="870d7-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-262">O parâmetro de uso no arquivo Media. ini não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-262">The usage parameter in the media .ini file is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SECTIONNAME"></span><span id="error_reading_sectionname"></span><dl> <span data-ttu-id="870d7-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-264">Não é possível ler o nome da seção da mídia. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="870d7-264">Cannot read the section name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEVICETYPE"></span><span id="error_reading_devicetype"></span><dl> <span data-ttu-id="870d7-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-266">Não é possível ler o tipo de dispositivo da mídia. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="870d7-266">Cannot read the device type from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_DEVICENAME"></span><span id="error_reading_devicename"></span><dl> <span data-ttu-id="870d7-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-268">Não é possível ler o nome do dispositivo da mídia. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="870d7-268">Cannot read the device name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_USAGE"></span><span id="error_reading_usage"></span><dl> <span data-ttu-id="870d7-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-270">Não é possível ler o uso da mídia. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="870d7-270">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_MAXCONNECTBPS"></span><span id="error_reading_maxconnectbps"></span><dl> <span data-ttu-id="870d7-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-272">O sistema não pôde ler a velocidade máxima de conexão da operadora da mídia. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="870d7-272">The system was unable to read the maximum carrier connection speed from the media .INI file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-273">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-273">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_MAXCARRIERBPS"></span><span id="error_reading_maxcarrierbps"></span><dl> <span data-ttu-id="870d7-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-275">Não é possível ler o uso da mídia. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="870d7-275">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_LINE_BUSY"></span><span id="error_line_busy"></span><dl> <span data-ttu-id="870d7-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-277">A linha está ocupada.</span><span class="sxs-lookup"><span data-stu-id="870d7-277">The line is busy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VOICE_ANSWER"></span><span id="error_voice_answer"></span><dl> <span data-ttu-id="870d7-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-279">Uma pessoa respondeu em vez de um modem.</span><span class="sxs-lookup"><span data-stu-id="870d7-279">A person answered instead of a modem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ANSWER"></span><span id="error_no_answer"></span><dl> <span data-ttu-id="870d7-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-281">Não há resposta.</span><span class="sxs-lookup"><span data-stu-id="870d7-281">There is no answer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_CARRIER"></span><span id="error_no_carrier"></span><dl> <span data-ttu-id="870d7-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-283">Não é possível detectar um sinal de operador.</span><span class="sxs-lookup"><span data-stu-id="870d7-283">Cannot detect a carrier signal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIALTONE"></span><span id="error_no_dialtone"></span><dl> <span data-ttu-id="870d7-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-285">Não há nenhum tom de discagem.</span><span class="sxs-lookup"><span data-stu-id="870d7-285">There is no dial tone.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IN_COMMAND"></span><span id="error_in_command"></span><dl> <span data-ttu-id="870d7-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-287">O modem (ou outro dispositivo de conexão) relatou um erro geral.</span><span class="sxs-lookup"><span data-stu-id="870d7-287">The modem (or other connecting device) reported a general error.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-288">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-288">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_SECTIONNAME"></span><span id="error_writing_sectionname"></span><dl> <span data-ttu-id="870d7-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-290">Erro ao gravar o nome da seção.</span><span class="sxs-lookup"><span data-stu-id="870d7-290">There was an error in writing the section name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_DEVICETYPE"></span><span id="error_writing_devicetype"></span><dl> <span data-ttu-id="870d7-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-292">Erro ao gravar o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="870d7-292">There was an error in writing the device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEVICENAME"></span><span id="error_writing_devicename"></span><dl> <span data-ttu-id="870d7-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-294">Erro ao gravar o nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="870d7-294">There was an error in writing the device name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_MAXCONNECTBPS"></span><span id="error_writing_maxconnectbps"></span><dl> <span data-ttu-id="870d7-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-296">Erro ao gravar a velocidade de conexão máxima.</span><span class="sxs-lookup"><span data-stu-id="870d7-296">There was an error in writing the maximum connection speed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_MAXCARRIERBPS"></span><span id="error_writing_maxcarrierbps"></span><dl> <span data-ttu-id="870d7-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-298">Erro ao gravar a velocidade máxima da operadora.</span><span class="sxs-lookup"><span data-stu-id="870d7-298">There was an error in writing the maximum carrier speed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_USAGE"></span><span id="error_writing_usage"></span><dl> <span data-ttu-id="870d7-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-300">Ocorreu um erro ao gravar o uso.</span><span class="sxs-lookup"><span data-stu-id="870d7-300">There was an error in writing the usage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEFAULTOFF"></span><span id="error_writing_defaultoff"></span><dl> <span data-ttu-id="870d7-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-302">Ocorreu um erro ao gravar o padrão.</span><span class="sxs-lookup"><span data-stu-id="870d7-302">There was an error in writing the default-off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEFAULTOFF"></span><span id="error_reading_defaultoff"></span><dl> <span data-ttu-id="870d7-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span></span></dl></td>

</tr>
<tr class="odd">
<td><span id="ERROR_EMPTY_INI_FILE"></span><span id="error_empty_ini_file"></span><dl> <span data-ttu-id="870d7-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-305">A mídia. O arquivo INI está vazio.</span><span class="sxs-lookup"><span data-stu-id="870d7-305">The media .INI file is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTHENTICATION_FAILURE"></span><span id="error_authentication_failure"></span><dl> <span data-ttu-id="870d7-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-307">Acesso negado porque o nome de usuário, a senha ou ambos não são válidos no domínio.</span><span class="sxs-lookup"><span data-stu-id="870d7-307">Access denied because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_OR_DEVICE"></span><span id="error_port_or_device"></span><dl> <span data-ttu-id="870d7-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-309">Ocorreu uma falha de hardware na porta ou no dispositivo conectado</span><span class="sxs-lookup"><span data-stu-id="870d7-309">A hardware failure has occurred in the port or attached device</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_BINARY_MACRO"></span><span id="error_not_binary_macro"></span><dl> <span data-ttu-id="870d7-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-311">A macro não é uma macro binária.</span><span class="sxs-lookup"><span data-stu-id="870d7-311">The macro is not a binary macro.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DCB_NOT_FOUND"></span><span id="error_dcb_not_found"></span><dl> <span data-ttu-id="870d7-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-313">DCB não encontrado.</span><span class="sxs-lookup"><span data-stu-id="870d7-313">DCB not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_STATE_MACHINES_NOT_STARTED"></span><span id="error_state_machines_not_started"></span><dl> <span data-ttu-id="870d7-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-315">Os computadores de estado não foram iniciados.</span><span class="sxs-lookup"><span data-stu-id="870d7-315">State machines are not started.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_STATE_MACHINES_ALREADY_STARTED"></span><span id="error_state_machines_already_started"></span><dl> <span data-ttu-id="870d7-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-317">As máquinas de estado já foram iniciadas.</span><span class="sxs-lookup"><span data-stu-id="870d7-317">State machines are already started.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PARTIAL_RESPONSE_LOOPING"></span><span id="error_partial_response_looping"></span><dl> <span data-ttu-id="870d7-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-319">Loop de resposta parcial.</span><span class="sxs-lookup"><span data-stu-id="870d7-319">Partial response looping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_RESPONSE_KEY"></span><span id="error_unknown_response_key"></span><dl> <span data-ttu-id="870d7-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-321">Um nome de chave de resposta no dispositivo. O arquivo INF não está no formato esperado.</span><span class="sxs-lookup"><span data-stu-id="870d7-321">A response key name in the device .INF file is not in the expected format.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RECV_BUF_FULL"></span><span id="error_recv_buf_full"></span><dl> <span data-ttu-id="870d7-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-323">A resposta do dispositivo causou um estouro de buffer.</span><span class="sxs-lookup"><span data-stu-id="870d7-323">The device response caused a buffer overflow.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CMD_TOO_LONG"></span><span id="error_cmd_too_long"></span><dl> <span data-ttu-id="870d7-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-325">O comando expandido no dispositivo. O arquivo INF é muito longo.</span><span class="sxs-lookup"><span data-stu-id="870d7-325">The expanded command in the device .INF file is too long.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNSUPPORTED_BPS"></span><span id="error_unsupported_bps"></span><dl> <span data-ttu-id="870d7-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-327">O dispositivo foi movido para uma velocidade de conexão que não é suportada pelo driver COM.</span><span class="sxs-lookup"><span data-stu-id="870d7-327">The device moved to a connection speed that is not supported by the COM driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNEXPECTED_RESPONSE"></span><span id="error_unexpected_response"></span><dl> <span data-ttu-id="870d7-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-329">Resposta do dispositivo recebida quando nenhuma era esperada.</span><span class="sxs-lookup"><span data-stu-id="870d7-329">Device response received when none expected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERACTIVE_MODE"></span><span id="error_interactive_mode"></span><dl> <span data-ttu-id="870d7-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-331">Ocorreu um erro porque o modo interativo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="870d7-331">An error occurred because the interactive mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAD_CALLBACK_NUMBER"></span><span id="error_bad_callback_number"></span><dl> <span data-ttu-id="870d7-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-333">Foi especificado um número de retorno de chamada inadequado.</span><span class="sxs-lookup"><span data-stu-id="870d7-333">A bad callback number was specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_AUTH_STATE"></span><span id="error_invalid_auth_state"></span><dl> <span data-ttu-id="870d7-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-335">O estado de autenticação especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-335">The specified authentication state is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_INITBPS"></span><span id="error_writing_initbps"></span><dl> <span data-ttu-id="870d7-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-337">Ocorreu um erro ao gravar a velocidade de conexão inicial.</span><span class="sxs-lookup"><span data-stu-id="870d7-337">An error occurred when writing the initial connection speed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-338">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-338">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_X25_DIAGNOSTIC"></span><span id="error_x25_diagnostic"></span><dl> <span data-ttu-id="870d7-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-340">Foi recebida uma indicação de diagnóstico X. 25.</span><span class="sxs-lookup"><span data-stu-id="870d7-340">An X.25 diagnostic indication was received.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ACCT_EXPIRED"></span><span id="error_acct_expired"></span><dl> <span data-ttu-id="870d7-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-342">A conta especificada expirou.</span><span class="sxs-lookup"><span data-stu-id="870d7-342">The specified account has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CHANGING_PASSWORD"></span><span id="error_changing_password"></span><dl> <span data-ttu-id="870d7-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-344">Ocorreu um erro ao tentar alterar a senha no domínio.</span><span class="sxs-lookup"><span data-stu-id="870d7-344">An error occurred while attempting to change the password on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OVERRUN"></span><span id="error_overrun"></span><dl> <span data-ttu-id="870d7-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-346">Foram detectados erros de saturação de série durante a comunicação com o modem.</span><span class="sxs-lookup"><span data-stu-id="870d7-346">Serial overrun errors were detected while communicating with your modem.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASMAN_CANNOT_INITIALIZE"></span><span id="error_rasman_cannot_initialize"></span><dl> <span data-ttu-id="870d7-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-348">Falha na inicialização de RasMan.</span><span class="sxs-lookup"><span data-stu-id="870d7-348">RasMan initialization failure.</span></span> <span data-ttu-id="870d7-349">Verifique o log de eventos.</span><span class="sxs-lookup"><span data-stu-id="870d7-349">Check the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BIPLEX_PORT_NOT_AVAILABLE"></span><span id="error_biplex_port_not_available"></span><dl> <span data-ttu-id="870d7-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-351">A porta bidirecional está sendo inicializada.</span><span class="sxs-lookup"><span data-stu-id="870d7-351">The two-way port is initializing.</span></span> <span data-ttu-id="870d7-352">Aguarde alguns segundos e disque novamente.</span><span class="sxs-lookup"><span data-stu-id="870d7-352">Wait a few seconds and redial.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-353">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-353">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_ACTIVE_ISDN_LINES"></span><span id="error_no_active_isdn_lines"></span><dl> <span data-ttu-id="870d7-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-355">Não há linhas ISDN ativas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="870d7-355">No active ISDN lines are available.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ISDN_CHANNELS_AVAILABLE"></span><span id="error_no_isdn_channels_available"></span><dl> <span data-ttu-id="870d7-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-357">Não há canais ISDN disponíveis para fazer a chamada.</span><span class="sxs-lookup"><span data-stu-id="870d7-357">No ISDN channels are available to make the call.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-358">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-358">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_TOO_MANY_LINE_ERRORS"></span><span id="error_too_many_line_errors"></span><dl> <span data-ttu-id="870d7-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-360">Muitos erros ocorreram devido à baixa qualidade da linha telefônica.</span><span class="sxs-lookup"><span data-stu-id="870d7-360">Too many errors occurred because of poor phone line quality.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-361">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-361">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IP_CONFIGURATION"></span><span id="error_ip_configuration"></span><dl> <span data-ttu-id="870d7-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-363">A configuração de IP de acesso remoto é inutilizável.</span><span class="sxs-lookup"><span data-stu-id="870d7-363">The remote access IP configuration is unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_IP_ADDRESSES"></span><span id="error_no_ip_addresses"></span><dl> <span data-ttu-id="870d7-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-365">Nenhum endereço IP está disponível no pool estático de endereços IP de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-365">No IP addresses are available in the static pool of remote access IP addresses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_TIMEOUT"></span><span id="error_ppp_timeout"></span><dl> <span data-ttu-id="870d7-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-367">Ocorreu um tempo limite de PPP.</span><span class="sxs-lookup"><span data-stu-id="870d7-367">A PPP timeout occurred.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REMOTE_TERMINATED"></span><span id="error_ppp_remote_terminated"></span><dl> <span data-ttu-id="870d7-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-369">A conexão foi encerrada pelo computador remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-369">The connection was terminated by the remote computer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-370">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-370">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_PROTOCOLS_CONFIGURED"></span><span id="error_ppp_no_protocols_configured"></span><dl> <span data-ttu-id="870d7-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-372">Não há protocolos de controle de PPP configurados.</span><span class="sxs-lookup"><span data-stu-id="870d7-372">No PPP control protocols are configured.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_NO_RESPONSE"></span><span id="error_ppp_no_response"></span><dl> <span data-ttu-id="870d7-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-374">O ponto PPP remoto não está respondendo.</span><span class="sxs-lookup"><span data-stu-id="870d7-374">The remote PPP peer is not responding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_INVALID_PACKET"></span><span id="error_ppp_invalid_packet"></span><dl> <span data-ttu-id="870d7-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-376">O pacote PPP não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-376">The PPP packet is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PHONE_NUMBER_TOO_LONG"></span><span id="error_phone_number_too_long"></span><dl> <span data-ttu-id="870d7-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-378">O número de telefone, incluindo o prefixo e o sufixo, é muito longo.</span><span class="sxs-lookup"><span data-stu-id="870d7-378">The phone number, including the prefix and suffix, is too long.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NO_DIALOUT_CONFIGURED"></span><span id="error_ipxcp_no_dialout_configured"></span><dl> <span data-ttu-id="870d7-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-380">O protocolo IPX não pode se conectar ao modem (ou a outro dispositivo de conexão) porque este computador não está configurado para discagem (é um roteador IPX).</span><span class="sxs-lookup"><span data-stu-id="870d7-380">The IPX protocol cannot dial out on the modem (or other connecting device) because this computer is not configured for dialing out (it is an IPX router).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-381">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-381">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPXCP_NO_DIALIN_CONFIGURED"></span><span id="error_ipxcp_no_dialin_configured"></span><dl> <span data-ttu-id="870d7-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-383">O protocolo IPX não pode discar no modem (ou em outro dispositivo de conexão) porque este computador não está configurado para discagem (o roteador IPX não está instalado).</span><span class="sxs-lookup"><span data-stu-id="870d7-383">The IPX protocol cannot dial in on the modem (or other connecting device) because this computer is not configured for dialing in (the IPX router is not installed).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-384">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-384">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE"></span><span id="error_ipxcp_dialout_already_active"></span><dl> <span data-ttu-id="870d7-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-386">O protocolo IPX não pode ser usado para discagem em mais de uma porta por vez.</span><span class="sxs-lookup"><span data-stu-id="870d7-386">The IPX protocol cannot be used for dial-out on more than one port at a time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCESSING_TCPCFGDLL"></span><span id="error_accessing_tcpcfgdll"></span><dl> <span data-ttu-id="870d7-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-388">Não é possível acessar o TCPCFG.DLL.</span><span class="sxs-lookup"><span data-stu-id="870d7-388">Cannot access TCPCFG.DLL.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-389">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-389">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_IP_RAS_ADAPTER"></span><span id="error_no_ip_ras_adapter"></span><dl> <span data-ttu-id="870d7-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-391">Não é possível encontrar um adaptador IP associado ao acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-391">Cannot find an IP adapter bound to remote access.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SLIP_REQUIRES_IP"></span><span id="error_slip_requires_ip"></span><dl> <span data-ttu-id="870d7-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-393">A lista não pode ser usada a menos que o protocolo IP esteja instalado.</span><span class="sxs-lookup"><span data-stu-id="870d7-393">SLIP cannot be used unless the IP protocol is installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PROJECTION_NOT_COMPLETE"></span><span id="error_projection_not_complete"></span><dl> <span data-ttu-id="870d7-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-395">O registro do computador não está concluído.</span><span class="sxs-lookup"><span data-stu-id="870d7-395">Computer registration is not complete.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-396">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-396">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_NOT_CONFIGURED"></span><span id="error_protocol_not_configured"></span><dl> <span data-ttu-id="870d7-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-398">O protocolo especificado não está configurado.</span><span class="sxs-lookup"><span data-stu-id="870d7-398">The specified protocol is not configured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NOT_CONVERGING"></span><span id="error_ppp_not_converging"></span><dl> <span data-ttu-id="870d7-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-400">A negociação PPP não está convergindo.</span><span class="sxs-lookup"><span data-stu-id="870d7-400">The PPP negotiation is not converging.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_CP_REJECTED"></span><span id="error_ppp_cp_rejected"></span><dl> <span data-ttu-id="870d7-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-402">o protocolo de controle PPP para o protocolo de rede especificado não está disponível no servidor.</span><span class="sxs-lookup"><span data-stu-id="870d7-402">the PPP control protocol for the specified network protocol is not available on the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_LCP_TERMINATED"></span><span id="error_ppp_lcp_terminated"></span><dl> <span data-ttu-id="870d7-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-404">O protocolo de controle de link PPP foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="870d7-404">The PPP link control protocol was terminated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REQUIRED_ADDRESS_REJECTED"></span><span id="error_ppp_required_address_rejected"></span><dl> <span data-ttu-id="870d7-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-406">O endereço solicitado foi rejeitado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="870d7-406">The requested address was rejected by the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NCP_TERMINATED"></span><span id="error_ppp_ncp_terminated"></span><dl> <span data-ttu-id="870d7-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-408">O computador remoto terminou o protocolo de controle.</span><span class="sxs-lookup"><span data-stu-id="870d7-408">The remote computer terminated the control protocol.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_LOOPBACK_DETECTED"></span><span id="error_ppp_loopback_detected"></span><dl> <span data-ttu-id="870d7-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-410">Loopback detectado.</span><span class="sxs-lookup"><span data-stu-id="870d7-410">Loopback detected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_ADDRESS_ASSIGNED"></span><span id="error_ppp_no_address_assigned"></span><dl> <span data-ttu-id="870d7-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-412">O servidor não atribuiu um endereço.</span><span class="sxs-lookup"><span data-stu-id="870d7-412">The server did not assign an address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_USE_LOGON_CREDENTIALS"></span><span id="error_cannot_use_logon_credentials"></span><dl> <span data-ttu-id="870d7-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-414">O servidor remoto não pode usar a senha criptografada do Windows NT.</span><span class="sxs-lookup"><span data-stu-id="870d7-414">The remote server cannot use the Windows NT encrypted password.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TAPI_CONFIGURATION"></span><span id="error_tapi_configuration"></span><dl> <span data-ttu-id="870d7-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-416">Os dispositivos TAPI configurados para acesso remoto falharam ao inicializar ou não foram instalados corretamente.</span><span class="sxs-lookup"><span data-stu-id="870d7-416">The TAPI devices configured for remote access failed to initialize or were not installed correctly.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_LOCAL_ENCRYPTION"></span><span id="error_no_local_encryption"></span><dl> <span data-ttu-id="870d7-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-418">O computador local não dá suporte à criptografia.</span><span class="sxs-lookup"><span data-stu-id="870d7-418">The local computer does not support encryption.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_REMOTE_ENCRYPTION"></span><span id="error_no_remote_encryption"></span><dl> <span data-ttu-id="870d7-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-420">O servidor remoto não dá suporte à criptografia.</span><span class="sxs-lookup"><span data-stu-id="870d7-420">The remote server does not support encryption.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_REQUIRES_ENCRYPTION"></span><span id="error_remote_requires_encryption"></span><dl> <span data-ttu-id="870d7-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-422">O computador remoto requer criptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="870d7-422">The remote computer requires data encryption.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-423">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-423">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NET_NUMBER_CONFLICT"></span><span id="error_ipxcp_net_number_conflict"></span><dl> <span data-ttu-id="870d7-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-425">O sistema não pode usar o número de rede IPX atribuído pelo computador remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-425">The system cannot use the IPX network number assigned by the remote computer.</span></span> <span data-ttu-id="870d7-426">Informações adicionais são fornecidas no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="870d7-426">Additional information is provided in the event log.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-427">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-427">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SMM"></span><span id="error_invalid_smm"></span><dl> <span data-ttu-id="870d7-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-429">O módulo de gerenciamento de sessão (SMM) não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-429">The Session Management Module (SMM) is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-430">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-430">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_UNINITIALIZED"></span><span id="error_smm_uninitialized"></span><dl> <span data-ttu-id="870d7-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-432">O SMM não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="870d7-432">The SMM is uninitialized.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-433">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-433">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_MAC_FOR_PORT"></span><span id="error_no_mac_for_port"></span><dl> <span data-ttu-id="870d7-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-435">Sem MAC para a porta.</span><span class="sxs-lookup"><span data-stu-id="870d7-435">No MAC for port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-436">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-436">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_TIMEOUT"></span><span id="error_smm_timeout"></span><dl> <span data-ttu-id="870d7-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-438">O SMM atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="870d7-438">The SMM timed out.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-439">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-439">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_PHONE_NUMBER"></span><span id="error_bad_phone_number"></span><dl> <span data-ttu-id="870d7-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-441">Foi especificado um número de telefone insatisfatório.</span><span class="sxs-lookup"><span data-stu-id="870d7-441">A bad phone number was specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_MODULE"></span><span id="error_wrong_module"></span><dl> <span data-ttu-id="870d7-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-443">O SMM errado foi especificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-443">The wrong SMM was specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-444">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-444">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_CALLBACK_NUMBER"></span><span id="error_invalid_callback_number"></span><dl> <span data-ttu-id="870d7-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-446">O número de retorno de chamada contém um caractere que não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-446">The callback number contains a character that is not valid.</span></span> <span data-ttu-id="870d7-447">Somente os 18 caracteres a seguir são permitidos: 0 a 9, T, P, W, (,),-, @ e espaço.</span><span class="sxs-lookup"><span data-stu-id="870d7-447">Only the following 18 characters are allowed: 0 to 9, T, P, W, (, ), -, @, and space.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-448">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-448">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SCRIPT_SYNTAX"></span><span id="error_script_syntax"></span><dl> <span data-ttu-id="870d7-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-450">Foi encontrado um erro de sintaxe durante o processamento de um script.</span><span class="sxs-lookup"><span data-stu-id="870d7-450">A syntax error was encountered while processing a script.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_HANGUP_FAILED"></span><span id="error_hangup_failed"></span><dl> <span data-ttu-id="870d7-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-452">Não foi possível desconectar a conexão porque ela foi criada pelo roteador de vários protocolos.</span><span class="sxs-lookup"><span data-stu-id="870d7-452">The connection could not be disconnected because it was created by the multi-protocol router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUNDLE_NOT_FOUND"></span><span id="error_bundle_not_found"></span><dl> <span data-ttu-id="870d7-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-454">O sistema não pôde localizar o pacote de vários vínculos.</span><span class="sxs-lookup"><span data-stu-id="870d7-454">The system could not find the multi-link bundle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DO_CUSTOMDIAL"></span><span id="error_cannot_do_customdial"></span><dl> <span data-ttu-id="870d7-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-456">O sistema não pode executar a discagem automática porque essa conexão tem um discador personalizado especificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-456">The system cannot perform automated dial because this connection has a custom dialer specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIAL_ALREADY_IN_PROGRESS"></span><span id="error_dial_already_in_progress"></span><dl> <span data-ttu-id="870d7-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-458">Esta conexão já está sendo discada.</span><span class="sxs-lookup"><span data-stu-id="870d7-458">This connection is already being dialed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASAUTO_CANNOT_INITIALIZE"></span><span id="error_rasauto_cannot_initialize"></span><dl> <span data-ttu-id="870d7-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-460">Não foi possível iniciar o RAS automaticamente.</span><span class="sxs-lookup"><span data-stu-id="870d7-460">RAS could not be started automatically.</span></span> <span data-ttu-id="870d7-461">Informações adicionais são fornecidas no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="870d7-461">Additional information is provided in the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_ALREADY_SHARED"></span><span id="error_connection_already_shared"></span><dl> <span data-ttu-id="870d7-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-463">O ICS (compartilhamento de conexão com a Internet) já está habilitado na conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-463">Internet Connection Sharing (ICS) is already enabled on the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-464">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-464">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_CHANGE_FAILED"></span><span id="error_sharing_change_failed"></span><dl> <span data-ttu-id="870d7-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-466">Ocorreu um erro enquanto as configurações de compartilhamento de conexão com a Internet existentes estavam sendo alteradas.</span><span class="sxs-lookup"><span data-stu-id="870d7-466">An error occurred while the existing Internet Connection Sharing settings were being changed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-467">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-467">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_ROUTER_INSTALL"></span><span id="error_sharing_router_install"></span><dl> <span data-ttu-id="870d7-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-469">Ocorreu um erro enquanto os recursos de roteamento estavam sendo habilitados.</span><span class="sxs-lookup"><span data-stu-id="870d7-469">An error occurred while routing capabilities were being enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-470">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-470">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARE_CONNECTION_FAILED"></span><span id="error_share_connection_failed"></span><dl> <span data-ttu-id="870d7-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-472">Ocorreu um erro enquanto o compartilhamento de conexão com a Internet estava sendo habilitado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-472">An error occurred while Internet Connection Sharing was being enabled for the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-473">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-473">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="7ERROR_SHARING_PRIVATE_INSTALL64"></span><span id="7error_sharing_private_install64"></span><dl> <span data-ttu-id="870d7-474"><dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-474"><dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-475">Ocorreu um erro enquanto a rede local estava sendo configurada para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="870d7-475">An error occurred while the local network was being configured for sharing.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-476">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-476">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SHARE_CONNECTION"></span><span id="error_cannot_share_connection"></span><dl> <span data-ttu-id="870d7-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-478">O compartilhamento de conexão com a Internet não pode ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="870d7-478">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="870d7-479">Há mais de uma conexão de LAN diferente da conexão a ser compartilhada.</span><span class="sxs-lookup"><span data-stu-id="870d7-479">There is more than one LAN connection other than the connection to be shared.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-480">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-480">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SMART_CARD_READER"></span><span id="error_no_smart_card_reader"></span><dl> <span data-ttu-id="870d7-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-482">Nenhum leitor de cartão inteligente está instalado.</span><span class="sxs-lookup"><span data-stu-id="870d7-482">No smart card reader is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_ADDRESS_EXISTS"></span><span id="error_sharing_address_exists"></span><dl> <span data-ttu-id="870d7-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-484">O compartilhamento de conexão com a Internet não pode ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="870d7-484">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="870d7-485">Uma conexão de LAN já está configurada com o endereço IP necessário para o endereçamento IP automático.</span><span class="sxs-lookup"><span data-stu-id="870d7-485">A LAN connection is already configured with the IP address that is required for automatic IP addressing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CERTIFICATE"></span><span id="error_no_certificate"></span><dl> <span data-ttu-id="870d7-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-487">Não foi possível encontrar um certificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-487">A certificate could not be found.</span></span> <span data-ttu-id="870d7-488">As conexões que usam o protocolo L2TP sobre IPSec exigem a instalação de um certificado de máquina, também conhecido como certificado de computador.</span><span class="sxs-lookup"><span data-stu-id="870d7-488">Connections that use the L2TP protocol over IPSec require the installation of a machine certificate, also known as a computer certificate.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_MULTIPLE_ADDRESSES"></span><span id="error_sharing_multiple_addresses"></span><dl> <span data-ttu-id="870d7-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-490">O compartilhamento de conexão com a Internet não pode ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="870d7-490">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="870d7-491">A conexão LAN selecionada como a rede privada tem mais de um endereço IP configurado.</span><span class="sxs-lookup"><span data-stu-id="870d7-491">The LAN connection selected as the private network has more than one IP address configured.</span></span> <span data-ttu-id="870d7-492">Reconfigure a conexão LAN com um único endereço IP antes de habilitar o compartilhamento de conexão com a Internet.</span><span class="sxs-lookup"><span data-stu-id="870d7-492">Please reconfigure the LAN connection with a single IP address before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FAILED_TO_ENCRYPT"></span><span id="error_failed_to_encrypt"></span><dl> <span data-ttu-id="870d7-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-494">Falha na tentativa de conexão devido à falha na criptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="870d7-494">The connection attempt failed because of failure to encrypt data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_ADDRESS_SPECIFIED"></span><span id="error_bad_address_specified"></span><dl> <span data-ttu-id="870d7-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-496">O destino especificado não está acessível.</span><span class="sxs-lookup"><span data-stu-id="870d7-496">The specified destination is not reachable.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_REJECT"></span><span id="error_connection_reject"></span><dl> <span data-ttu-id="870d7-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-498">O computador remoto rejeitou a tentativa de conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-498">The remote computer rejected the connection attempt.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONGESTION"></span><span id="error_congestion"></span><dl> <span data-ttu-id="870d7-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-500">Falha na tentativa de conexão porque a rede está ocupada.</span><span class="sxs-lookup"><span data-stu-id="870d7-500">The connection attempt failed because the network is busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INCOMPATIBLE"></span><span id="error_incompatible"></span><dl> <span data-ttu-id="870d7-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-502">O hardware de rede do computador remoto é incompatível com o tipo de chamada solicitada.</span><span class="sxs-lookup"><span data-stu-id="870d7-502">The remote computer's network hardware is incompatible with the type of call requested.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NUMBERCHANGED"></span><span id="error_numberchanged"></span><dl> <span data-ttu-id="870d7-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-504">Falha na tentativa de conexão porque o número de destino foi alterado.</span><span class="sxs-lookup"><span data-stu-id="870d7-504">The connection attempt failed because the destination number has changed.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TEMPFAILURE"></span><span id="error_tempfailure"></span><dl> <span data-ttu-id="870d7-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-506">Falha na tentativa de conexão devido a uma falha temporária.</span><span class="sxs-lookup"><span data-stu-id="870d7-506">The connection attempt failed because of a temporary failure.</span></span> <span data-ttu-id="870d7-507">Tente se conectar novamente.</span><span class="sxs-lookup"><span data-stu-id="870d7-507">Try connecting again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BLOCKED"></span><span id="error_blocked"></span><dl> <span data-ttu-id="870d7-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-509">A chamada foi bloqueada pelo computador remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-509">The call was blocked by the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DONOTDISTURB"></span><span id="error_donotdisturb"></span><dl> <span data-ttu-id="870d7-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-511">Não foi possível conectar a chamada porque o computador remoto invocou o recurso não incomodar.</span><span class="sxs-lookup"><span data-stu-id="870d7-511">The call could not be connected because the remote computer has invoked the Do Not Disturb feature.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OUTOFORDER"></span><span id="error_outoforder"></span><dl> <span data-ttu-id="870d7-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-513">Falha na tentativa de conexão porque o modem ou outro dispositivo de conexão no computador remoto está fora de ordem.</span><span class="sxs-lookup"><span data-stu-id="870d7-513">The connection attempt failed because the modem or other connection device on the remote computer is out of order.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNABLE_TO_AUTHENTICATE_SERVER"></span><span id="error_unable_to_authenticate_server"></span><dl> <span data-ttu-id="870d7-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-515">Não foi possível verificar a identidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="870d7-515">It was not possible to verify the identity of the server.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SMART_CARD_REQUIRED"></span><span id="error_smart_card_required"></span><dl> <span data-ttu-id="870d7-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-517">Para discar usando essa conexão, você deve usar um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="870d7-517">To dial out using this connection you must use a smart card.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-518">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-518">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_FUNCTION_FOR_ENTRY"></span><span id="error_invalid_function_for_entry"></span><dl> <span data-ttu-id="870d7-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-520">Uma função tentada não é válida para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-520">An attempted function is not valid for this connection.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND"></span><span id="error_cert_for_encryption_not_found"></span><dl> <span data-ttu-id="870d7-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-522">Falha na tentativa de criptografia porque nenhum certificado válido foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="870d7-522">The encryption attempt failed because no valid certificate was found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-523">Preterido no Windows Vista e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-523">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_RRAS_CONFLICT"></span><span id="error_sharing_rras_conflict"></span><dl> <span data-ttu-id="870d7-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-525">O compartilhamento de conexão (NAT) está instalado atualmente como um protocolo de roteamento e deve ser removido antes de habilitar o compartilhamento de conexão com a Internet.</span><span class="sxs-lookup"><span data-stu-id="870d7-525">Connection Sharing (NAT) is currently installed as a routing protocol, and must be removed before enabling Internet Connection Sharing.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_NO_PRIVATE_LAN"></span><span id="error_sharing_no_private_lan"></span><dl> <span data-ttu-id="870d7-526"><dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-526"><dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-527">O compartilhamento de conexão com a Internet não pode ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="870d7-527">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="870d7-528">A conexão LAN selecionada como a rede privada não está presente ou está desconectada da rede.</span><span class="sxs-lookup"><span data-stu-id="870d7-528">The LAN connection selected as the private network is either not present, or is disconnected from the network.</span></span> <span data-ttu-id="870d7-529">Verifique se o adaptador de LAN está conectado antes de habilitar o compartilhamento de conexão com a Internet.</span><span class="sxs-lookup"><span data-stu-id="870d7-529">Please ensure that the LAN adapter is connected before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIFF_USER_AT_LOGON"></span><span id="error_no_diff_user_at_logon"></span><dl> <span data-ttu-id="870d7-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-531">Não é possível discar usando essa conexão no momento do logon porque ela está configurada para usar um nome de usuário diferente daquele no cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="870d7-531">You cannot dial using this connection at login time because it is configured to use a user name different than the one on the smart card.</span></span> <span data-ttu-id="870d7-532">Se você quiser usar essa conexão no momento do logon, deverá configurá-la para usar o nome de usuário no cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="870d7-532">If you want to use this connection at login time, you must configure it to use the user name on the smart card.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_REG_CERT_AT_LOGON"></span><span id="error_no_reg_cert_at_logon"></span><dl> <span data-ttu-id="870d7-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-534">Não é possível discar usando essa conexão no momento do logon porque ela não está configurada para usar um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="870d7-534">You cannot dial using this connection at login time because it is not configured to use a smart card.</span></span> <span data-ttu-id="870d7-535">Se você quiser usá-lo no momento do logon, deverá editar as propriedades dessa conexão para que ele use um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="870d7-535">If you want to use it at login time, you must edit the properties of this connection so that it uses a smart card.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_CERT"></span><span id="error_oakley_no_cert"></span><dl> <span data-ttu-id="870d7-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-537">A tentativa de conexão L2TP falhou porque não há um certificado de máquina válido no computador para autenticação de segurança.</span><span class="sxs-lookup"><span data-stu-id="870d7-537">The L2TP connection attempt failed because there is no valid machine certificate on your computer for security authentication.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_AUTH_FAIL"></span><span id="error_oakley_auth_fail"></span><dl> <span data-ttu-id="870d7-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-539">A tentativa de conexão L2TP falhou porque a camada de segurança não pôde autenticar o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-539">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_ATTRIB_FAIL"></span><span id="error_oakley_attrib_fail"></span><dl> <span data-ttu-id="870d7-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-541">A tentativa de conexão L2TP falhou porque a camada de segurança não pôde negociar parâmetros compatíveis com o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-541">The L2TP connection attempt failed because the security layer could not negotiate compatible parameters with the remote computer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_GENERAL_PROCESSING"></span><span id="error_oakley_general_processing"></span><dl> <span data-ttu-id="870d7-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-543">A tentativa de conexão L2TP falhou porque a camada de segurança encontrou um erro de processamento durante as negociações iniciais com o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-543">The L2TP connection attempt failed because the security layer encountered a processing error during initial negotiations with the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_PEER_CERT"></span><span id="error_oakley_no_peer_cert"></span><dl> <span data-ttu-id="870d7-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-545">Falha na tentativa de conexão L2TP porque a validação de certificado no computador remoto falhou.</span><span class="sxs-lookup"><span data-stu-id="870d7-545">The L2TP connection attempt failed because certificate validation on the remote computer failed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_NO_POLICY"></span><span id="error_oakley_no_policy"></span><dl> <span data-ttu-id="870d7-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-547">Falha na tentativa de conexão L2TP porque a política de segurança para a conexão não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="870d7-547">The L2TP connection attempt failed because security policy for the connection was not found.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_TIMED_OUT"></span><span id="error_oakley_timed_out"></span><dl> <span data-ttu-id="870d7-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-549">Falha na tentativa de conexão L2TP porque a negociação de segurança atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="870d7-549">The L2TP connection attempt failed because security negotiation timed out.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_ERROR"></span><span id="error_oakley_error"></span><dl> <span data-ttu-id="870d7-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-551">A tentativa de conexão L2TP falhou porque ocorreu um erro ao negociar a segurança.</span><span class="sxs-lookup"><span data-stu-id="870d7-551">The L2TP connection attempt failed because an error occurred while negotiating security.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_FRAMED_PROTOCOL"></span><span id="error_unknown_framed_protocol"></span><dl> <span data-ttu-id="870d7-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-553">O atributo de raio do protocolo Framed para este usuário não é PPP.</span><span class="sxs-lookup"><span data-stu-id="870d7-553">The Framed Protocol RADIUS attribute for this user is not PPP.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRONG_TUNNEL_TYPE"></span><span id="error_wrong_tunnel_type"></span><dl> <span data-ttu-id="870d7-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-555">O atributo RADIUS do tipo de túnel para este usuário não está correto.</span><span class="sxs-lookup"><span data-stu-id="870d7-555">The Tunnel Type RADIUS attribute for this user is not correct.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_SERVICE_TYPE"></span><span id="error_unknown_service_type"></span><dl> <span data-ttu-id="870d7-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-557">O atributo RADIUS do tipo de serviço para este usuário não é Framed nem retorno de chamada Framed.</span><span class="sxs-lookup"><span data-stu-id="870d7-557">The Service Type RADIUS attribute for this user is neither Framed nor Callback Framed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONNECTING_DEVICE_NOT_FOUND"></span><span id="error_connecting_device_not_found"></span><dl> <span data-ttu-id="870d7-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-559">Não foi possível estabelecer uma conexão com o computador remoto porque o modem não foi encontrado ou estava ocupado.</span><span class="sxs-lookup"><span data-stu-id="870d7-559">A connection to the remote computer could not be established because the modem was not found or was busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_EAPTLS_CERTIFICATE"></span><span id="error_no_eaptls_certificate"></span><dl> <span data-ttu-id="870d7-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-561">Não foi possível encontrar um certificado que possa ser usado com o EAP (Extensible Authentication Protocol).</span><span class="sxs-lookup"><span data-stu-id="870d7-561">A certificate could not be found that can be used with the Extensible Authentication Protocol (EAP).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_HOST_ADDRESS_CONFLICT"></span><span id="error_sharing_host_address_conflict"></span><dl> <span data-ttu-id="870d7-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-563">O ICS (compartilhamento de conexão com a Internet) não pode ser habilitado devido a um conflito de endereço IP na rede.</span><span class="sxs-lookup"><span data-stu-id="870d7-563">Internet Connection Sharing (ICS) cannot be enabled due to an IP address conflict on the network.</span></span> <span data-ttu-id="870d7-564">O ICS requer que o host seja configurado para usar <strong>192.168.0.1</strong>.</span><span class="sxs-lookup"><span data-stu-id="870d7-564">ICS requires the host be configured to use <strong>192.168.0.1</strong>.</span></span> <span data-ttu-id="870d7-565">Certifique-se de que nenhum outro cliente na rede esteja configurado para usar <strong>192.168.0.1</strong>.</span><span class="sxs-lookup"><span data-stu-id="870d7-565">Ensure that no other client on the network is configured to use <strong>192.168.0.1</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-566">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-566">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-567">Windows 7 e posterior: o host deve ser configurado para usar o <strong>192.168.137.1</strong>
</span><span class="sxs-lookup"><span data-stu-id="870d7-567">Windows 7 and later: The host must be configured to use <strong>192.168.137.1</strong>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTOMATIC_VPN_FAILED"></span><span id="error_automatic_vpn_failed"></span><dl> <span data-ttu-id="870d7-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-569">Não é possível estabelecer a conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="870d7-569">Unable to establish the VPN connection.</span></span> <span data-ttu-id="870d7-570">O servidor VPN pode estar inacessível ou os parâmetros de segurança podem não estar configurados corretamente para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-570">The VPN server may be unreachable, or security parameters may not be configured properly for this connection.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-571">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-571">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VALIDATING_SERVER_CERT"></span><span id="error_validating_server_cert"></span><dl> <span data-ttu-id="870d7-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-573">Essa conexão é configurada para validar a identidade do servidor de acesso, mas o Windows não pode verificar o certificado digital enviado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="870d7-573">This connection is configured to validate the identity of the access server, but Windows cannot verify the digital certificate sent by the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-574">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-574">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SCARD"></span><span id="error_reading_scard"></span><dl> <span data-ttu-id="870d7-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-576">O cartão fornecido não foi reconhecido.</span><span class="sxs-lookup"><span data-stu-id="870d7-576">The card supplied was not recognized.</span></span> <span data-ttu-id="870d7-577">Verifique se o cartão foi inserido corretamente e se adapta com segurança.</span><span class="sxs-lookup"><span data-stu-id="870d7-577">Please check that the card is inserted correctly, and fits securely.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-578">Com suporte no Windows XP com SP1 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-578">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_CONFIG"></span><span id="error_invalid_peap_cookie_config"></span><dl> <span data-ttu-id="870d7-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-580">A configuração de PEAP armazenada no cookie de sessão não corresponde à configuração de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="870d7-580">The PEAP configuration stored in the session cookie does not match the current session configuration.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-581">Com suporte no Windows XP com SP1 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-581">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PEAP_COOKIE_USER"></span><span id="error_invalid_peap_cookie_user"></span><dl> <span data-ttu-id="870d7-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-583">A identidade de PEAP armazenada no cookie de sessão não corresponde à identidade atual.</span><span class="sxs-lookup"><span data-stu-id="870d7-583">The PEAP identity stored in the session cookie does not match the current identity.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-584">Com suporte no Windows XP com SP1 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-584">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_MSCHAPV2_CONFIG"></span><span id="error_invalid_mschapv2_config"></span><dl> <span data-ttu-id="870d7-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-586">Não é possível discar usando essa conexão no momento do logon porque ela está configurada para usar as credenciais do usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="870d7-586">You cannot dial using this connection at login time because it is configured to use the currently-logged-in user's credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-587">Com suporte no Windows XP com SP1 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-587">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_GRE_BLOCKED"></span><span id="error_vpn_gre_blocked"></span><dl> <span data-ttu-id="870d7-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-589">Uma conexão entre o computador e o servidor VPN foi iniciada, mas a conexão VPN não pode ser concluída.</span><span class="sxs-lookup"><span data-stu-id="870d7-589">A connection between your computer and the VPN server has been started, but the VPN connection cannot be completed.</span></span> <span data-ttu-id="870d7-590">A causa mais comum para isso é que pelo menos um dispositivo de Internet (por exemplo, um firewall ou um roteador) entre o computador e o servidor VPN não está configurado para permitir pacotes de protocolo GRE (encapsulamento de roteamento genérico).</span><span class="sxs-lookup"><span data-stu-id="870d7-590">The most common cause for this is that at least one Internet device (for example, a firewall or a router) between your computer and the VPN server is not configured to allow Generic Routing Encapsulation (GRE) protocol packets.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-591">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-591">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_DISCONNECT"></span><span id="error_vpn_disconnect"></span><dl> <span data-ttu-id="870d7-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-593">A conexão de rede entre o computador e o servidor VPN foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="870d7-593">The network connection between your computer and the VPN server was interrupted.</span></span> <span data-ttu-id="870d7-594">Isso pode ser causado por um problema na transmissão de VPN e é normalmente o resultado da latência da Internet ou simplesmente que o servidor VPN atingiu a capacidade.</span><span class="sxs-lookup"><span data-stu-id="870d7-594">This can be caused by a problem in the VPN transmission and is commonly the result of internet latency or simply that your VPN server has reached capacity.</span></span> <span data-ttu-id="870d7-595">Tente se reconectar ao servidor VPN.</span><span class="sxs-lookup"><span data-stu-id="870d7-595">Try to reconnect to the VPN server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-596">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-596">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_REFUSED"></span><span id="error_vpn_refused"></span><dl> <span data-ttu-id="870d7-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-598">A conexão de rede entre o computador e o servidor VPN não pôde ser estabelecida porque o servidor remoto recusou a conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-598">The network connection between your computer and the VPN server could not be established because the remote server refused the connection.</span></span> <span data-ttu-id="870d7-599">Isso geralmente é causado por uma incompatibilidade entre a configuração do servidor e suas configurações de conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-599">This is typically caused by a mismatch between the server's configuration and your connection settings.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-600">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-600">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_TIMEOUT"></span><span id="error_vpn_timeout"></span><dl> <span data-ttu-id="870d7-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-602">Não foi possível estabelecer a conexão de rede entre o computador e o servidor VPN porque o servidor remoto não está respondendo.</span><span class="sxs-lookup"><span data-stu-id="870d7-602">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="870d7-603">Isso pode ocorrer porque um dos dispositivos de rede (por exemplo, firewalls, NAT, roteadores) entre o computador e o servidor remoto não está configurado para permitir conexões VPN.</span><span class="sxs-lookup"><span data-stu-id="870d7-603">This could be because one of the network devices (for example, firewalls, NAT, routers) between your computer and the remote server is not configured to allow VPN connections.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-604">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-604">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_BAD_CERT"></span><span id="error_vpn_bad_cert"></span><dl> <span data-ttu-id="870d7-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-606">Uma conexão de rede entre o computador e o servidor VPN foi iniciada, mas a conexão VPN não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="870d7-606">A network connection between your computer and the VPN server was started, but the VPN connection was not completed.</span></span> <span data-ttu-id="870d7-607">Isso geralmente é causado pelo uso de um certificado incorreto ou expirado para autenticação entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="870d7-607">This is typically caused by the use of an incorrect or expired certificate for authentication between the client and the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-608">Com suporte no Windows Vista e versões posteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="870d7-608">Supported in Windows Vista and later versions of Windows</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_BAD_PSK"></span><span id="error_vpn_bad_psk"></span><dl> <span data-ttu-id="870d7-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-610">Não foi possível estabelecer a conexão de rede entre o computador e o servidor VPN porque o servidor remoto não está respondendo.</span><span class="sxs-lookup"><span data-stu-id="870d7-610">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="870d7-611">Isso geralmente é causado por um problema de chave pré-compartilhada entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="870d7-611">This is typically caused by a pre-shared key problem between the client and server.</span></span> <span data-ttu-id="870d7-612">Uma chave pré-compartilhada é usada para garantir que você diga que está em um ciclo de comunicação de IPSec (segurança IP).</span><span class="sxs-lookup"><span data-stu-id="870d7-612">A pre-shared key is used to guarantee you are who you say you are in an IP Security (IPSec) communication cycle.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-613">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-613">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_POLICY"></span><span id="error_server_policy"></span><dl> <span data-ttu-id="870d7-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-615">a conexão foi impedida devido a uma política configurada no servidor RAS/VPN.</span><span class="sxs-lookup"><span data-stu-id="870d7-615">The connection was prevented because of a policy configured on your RAS/VPN server.</span></span> <span data-ttu-id="870d7-616">Especificamente, o método de autenticação usado pelo servidor para verificar seu nome de usuário e sua senha podem não corresponder ao método de autenticação configurado em seu perfil de conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-616">Specifically, the authentication method used by the server to verify your username and password may not match the authentication method configured in your connection profile.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-617">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-617">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_ACTIVE"></span><span id="error_broadband_active"></span><dl> <span data-ttu-id="870d7-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-619">Você tentou estabelecer uma segunda conexão de banda larga enquanto uma conexão de banda larga anterior já foi estabelecida usando o mesmo dispositivo ou porta.</span><span class="sxs-lookup"><span data-stu-id="870d7-619">You have attempted to establish a second broadband connection while a previous broadband connection is already established using the same device or port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-620">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-620">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BROADBAND_NO_NIC"></span><span id="error_broadband_no_nic"></span><dl> <span data-ttu-id="870d7-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-622">A conectividade Ethernet subjacente necessária para a conexão de banda larga não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="870d7-622">The underlying Ethernet connectivity required for the broadband connection was not found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-623">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-623">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_TIMEOUT"></span><span id="error_broadband_timeout"></span><dl> <span data-ttu-id="870d7-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-625">Não foi possível estabelecer a conexão de rede de banda larga no computador porque o servidor remoto não está respondendo.</span><span class="sxs-lookup"><span data-stu-id="870d7-625">The broadband network connection could not be established on your computer because the remote server is not responding.</span></span> <span data-ttu-id="870d7-626">Isso pode ser causado por um valor que não é válido para o campo ' nome do serviço ' para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-626">This could be caused by a value that is not valid for the 'Service Name' field for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-627">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-627">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FEATURE_DEPRECATED"></span><span id="error_feature_deprecated"></span><dl> <span data-ttu-id="870d7-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-629">Um recurso ou configuração que você tentou habilitar não é mais suportado pelo serviço de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-629">A feature or setting you have tried to enable is no longer supported by the remote access service.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-630">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-630">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DELETE"></span><span id="error_cannot_delete"></span><dl> <span data-ttu-id="870d7-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-632">Não é possível excluir uma conexão enquanto ela está conectada.</span><span class="sxs-lookup"><span data-stu-id="870d7-632">Cannot delete a connection while it is connected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-633">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-633">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_RESOURCE_CREATION_FAILED"></span><span id="error_rasqec_resource_creation_failed"></span><dl> <span data-ttu-id="870d7-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-635">O cliente de imposição de NAP (proteção de acesso à rede) não pôde criar recursos do sistema para conexões de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-635">The Network Access Protection (NAP) enforcement client could not create system resources for remote access connections.</span></span> <span data-ttu-id="870d7-636">Alguns serviços de rede ou recursos podem não estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="870d7-636">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-637">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-637">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_ENABLED"></span><span id="error_rasqec_napagent_not_enabled"></span><dl> <span data-ttu-id="870d7-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-639">O serviço de agente de proteção de acesso à rede (agente NAP) foi desabilitado ou não está instalado neste computador.</span><span class="sxs-lookup"><span data-stu-id="870d7-639">The Network Access Protection Agent (NAP Agent) service has been disabled or is not installed on this computer.</span></span> <span data-ttu-id="870d7-640">Alguns serviços de rede ou recursos podem não estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="870d7-640">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-641">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-641">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_CONNECTED"></span><span id="error_rasqec_napagent_not_connected"></span><dl> <span data-ttu-id="870d7-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-643">Falha do cliente de imposição de NAP (proteção de acesso à rede) ao registrar com o serviço de agente de proteção de acesso à rede (agente NAP).</span><span class="sxs-lookup"><span data-stu-id="870d7-643">The Network Access Protection (NAP) enforcement client failed to register with the Network Access Protection Agent (NAP Agent) service.</span></span> <span data-ttu-id="870d7-644">Alguns serviços de rede ou recursos podem não estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="870d7-644">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-645">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-645">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_CONN_DOESNOTEXIST"></span><span id="error_rasqec_conn_doesnotexist"></span><dl> <span data-ttu-id="870d7-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-647">O cliente de imposição de NAP (proteção de acesso à rede) não pôde processar a solicitação porque a conexão de acesso remoto não existe.</span><span class="sxs-lookup"><span data-stu-id="870d7-647">The Network Access Protection (NAP) enforcement client was unable to process the request because the remote access connection does not exist.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-648">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-648">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_TIMEOUT"></span><span id="error_rasqec_timeout"></span><dl> <span data-ttu-id="870d7-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-650">O cliente de imposição de NAP (proteção de acesso à rede) não respondeu.</span><span class="sxs-lookup"><span data-stu-id="870d7-650">The Network Access Protection (NAP) enforcement client did not respond.</span></span> <span data-ttu-id="870d7-651">Alguns serviços de rede ou recursos podem não estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="870d7-651">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-652">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-652">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_CRYPTOBINDING_INVALID"></span><span id="error_peap_cryptobinding_invalid"></span><dl> <span data-ttu-id="870d7-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-654">O TLV (tipo-tamanho-valor) de Crypto-Binding recebido não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-654">The Crypto-Binding type-length-value (TLV) received is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-655">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-655">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED"></span><span id="error_peap_cryptobinding_notreceived"></span><dl> <span data-ttu-id="870d7-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-657">O TLV de Crypto-Binding não foi recebido.</span><span class="sxs-lookup"><span data-stu-id="870d7-657">Crypto-Binding TLV was not received.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-658">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-658">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_VPNSTRATEGY"></span><span id="error_invalid_vpnstrategy"></span><dl> <span data-ttu-id="870d7-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-660">O PPTP (ponto a ponto de encapsulamento) é incompatível com o IPv6.</span><span class="sxs-lookup"><span data-stu-id="870d7-660">Point-to-Point Tunneling Protocol (PPTP) is incompatible with IPv6.</span></span> <span data-ttu-id="870d7-661">Altere o tipo de rede virtual privada para L2TP (protocolo de encapsulamento de camada dois).</span><span class="sxs-lookup"><span data-stu-id="870d7-661">Change the type of virtual private network to Layer Two Tunneling Protocol (L2TP).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-662">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-662">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_cache_credentials_invalid"></span><dl> <span data-ttu-id="870d7-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-664">Falha na validação de EAPTLS das credenciais armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="870d7-664">EAPTLS validation of the cached credentials failed.</span></span> <span data-ttu-id="870d7-665">Descartar credenciais em cache.</span><span class="sxs-lookup"><span data-stu-id="870d7-665">Discard cached credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-666">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-666">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPSEC_SERVICE_STOPPED"></span><span id="error_ipsec_service_stopped"></span><dl> <span data-ttu-id="870d7-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-668">A conexão L2TP/IPsec não pode ser concluída porque o serviço de módulos de criação de chaves IKE e AuthIP IPSec e/ou o serviço mecanismo de filtragem base não está em execução.</span><span class="sxs-lookup"><span data-stu-id="870d7-668">The L2TP/IPsec connection cannot be completed because the IKE and AuthIP IPSec Keying Modules service and/or the Base Filtering Engine service is not running.</span></span> <span data-ttu-id="870d7-669">Esses serviços são necessários para estabelecer uma conexão L2TP/IPSec.</span><span class="sxs-lookup"><span data-stu-id="870d7-669">These services are required to establish an L2TP/IPSec connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-670">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-670">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_TIMEOUT"></span><span id="error_idle_timeout"></span><dl> <span data-ttu-id="870d7-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-672">A conexão foi encerrada devido ao tempo limite de ociosidade.</span><span class="sxs-lookup"><span data-stu-id="870d7-672">The connection was terminated because of idle timeout.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-673">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-673">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_LINK_FAILURE"></span><span id="error_link_failure"></span><dl> <span data-ttu-id="870d7-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-675">O modem (ou outro dispositivo de conexão) foi desconectado devido a uma falha de link.</span><span class="sxs-lookup"><span data-stu-id="870d7-675">The modem (or other connecting device) was disconnected due to link failure.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-676">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-676">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_USER_LOGOFF"></span><span id="error_user_logoff"></span><dl> <span data-ttu-id="870d7-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-678">A conexão foi encerrada porque o usuário fez logoff.</span><span class="sxs-lookup"><span data-stu-id="870d7-678">The connection was terminated because user logged off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-679">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-679">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAST_USER_SWITCH"></span><span id="error_fast_user_switch"></span><dl> <span data-ttu-id="870d7-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-681">A conexão foi encerrada porque o comutador do usuário ocorreu.</span><span class="sxs-lookup"><span data-stu-id="870d7-681">The connection was terminated because user switch happened.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-682">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-682">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HIBERNATION"></span><span id="error_hibernation"></span><dl> <span data-ttu-id="870d7-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-684">A conexão foi encerrada devido à hibernação.</span><span class="sxs-lookup"><span data-stu-id="870d7-684">The connection was terminated because of hibernation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-685">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-685">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SYSTEM_SUSPENDED"></span><span id="error_system_suspended"></span><dl> <span data-ttu-id="870d7-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-687">A conexão foi encerrada porque o sistema foi suspenso.</span><span class="sxs-lookup"><span data-stu-id="870d7-687">The connection was terminated because the system got suspended.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-688">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-688">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASMAN_SERVICE_STOPPED"></span><span id="error_rasman_service_stopped"></span><dl> <span data-ttu-id="870d7-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-690">A conexão foi encerrada porque o Gerenciador de conexões de acesso remoto foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="870d7-690">The connection was terminated because Remote Access Connection manager stopped.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-691">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-691">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SERVER_CERT"></span><span id="error_invalid_server_cert"></span><dl> <span data-ttu-id="870d7-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-693">A tentativa de conexão L2TP falhou porque a camada de segurança não pôde autenticar o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-693">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <span data-ttu-id="870d7-694">Isso pode ocorrer porque um ou mais campos do certificado apresentados pelo servidor remoto não puderam ser validados como pertencentes ao destino de destino.</span><span class="sxs-lookup"><span data-stu-id="870d7-694">This could be because one or more fields of the certificate presented by the remote server could not be validated as belonging to the target destination.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-695">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-695">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_NAP_CAPABLE"></span><span id="error_not_nap_capable"></span><dl> <span data-ttu-id="870d7-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-697">O computador não é compatível com NAP.</span><span class="sxs-lookup"><span data-stu-id="870d7-697">The machine is not NAP capable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-698">Com suporte no Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-698">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_TUNNELID"></span><span id="error_invalid_tunnelid"></span><dl> <span data-ttu-id="870d7-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-700">ID de túnel inválida.</span><span class="sxs-lookup"><span data-stu-id="870d7-700">Invalid Tunnel ID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-701">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-701">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS"></span><span id="error_updateconnection_request_in_process"></span><dl> <span data-ttu-id="870d7-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-703">Outra solicitação de conexão de atualização está em andamento.</span><span class="sxs-lookup"><span data-stu-id="870d7-703">Another update connection request is in progress.</span></span> <span data-ttu-id="870d7-704">O RAS permite apenas uma solicitação de conexão de atualização por vez.</span><span class="sxs-lookup"><span data-stu-id="870d7-704">RAS allows only one update connection request at a time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-705">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-705">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ENGINE_DISABLED"></span><span id="error_protocol_engine_disabled"></span><dl> <span data-ttu-id="870d7-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-707">Negociar usando o protocolo configurado é desabilitar.</span><span class="sxs-lookup"><span data-stu-id="870d7-707">Negotiating using configured protocol is disable.</span></span> <span data-ttu-id="870d7-708">Edite as propriedades de conexão e selecione protocolo diferente para negociação e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="870d7-708">Edit connection properties and select different protocol for negotiation and try again.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-709">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-709">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERNAL_ADDRESS_FAILURE"></span><span id="error_internal_address_failure"></span><dl> <span data-ttu-id="870d7-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-711">Falha na negociação de endereço interno.</span><span class="sxs-lookup"><span data-stu-id="870d7-711">Internal address negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-712">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-712">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAILED_CP_REQUIRED"></span><span id="error_failed_cp_required"></span><dl> <span data-ttu-id="870d7-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-714">O cliente precisa solicitar um endereço IPv4 ou IPv6 interno.</span><span class="sxs-lookup"><span data-stu-id="870d7-714">Client has to request an Internal IPv4 or IPv6 address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-715">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-715">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TS_UNACCEPTABLE"></span><span id="error_ts_unacceptable"></span><dl> <span data-ttu-id="870d7-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-717">Falha na negociação de seletores de tráfego.</span><span class="sxs-lookup"><span data-stu-id="870d7-717">Traffic Selectors negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-718">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-718">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MOBIKE_DISABLED"></span><span id="error_mobike_disabled"></span><dl> <span data-ttu-id="870d7-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-720">A mobilidade está desabilitada para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-720">Mobility is disabled for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-721">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-721">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_INITIATE_MOBIKE_UPDATE"></span><span id="error_cannot_initiate_mobike_update"></span><dl> <span data-ttu-id="870d7-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-723">A conexão VPN ainda está se conectando ou autenticando novamente devido à alteração de estado de quarentena.</span><span class="sxs-lookup"><span data-stu-id="870d7-723">The VPN Connection is still connecting or re-authenticating because of Quarantine state change.</span></span> <span data-ttu-id="870d7-724">Inicie a atualização móvel somente quando o estado da conexão for ' conectado '.</span><span class="sxs-lookup"><span data-stu-id="870d7-724">Initiate mobile update only when connection state is 'Connected'.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-725">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-725">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV"></span><span id="error_peap_server_rejected_client_tlv"></span><dl> <span data-ttu-id="870d7-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-727">O servidor rejeitou a autenticação de cliente, devido à incompatibilidade de TLV ou valor inesperado para um TLV.</span><span class="sxs-lookup"><span data-stu-id="870d7-727">Server rejected client authentication, due to unexpected TLV or value mismatch for a TLV.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-728">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-728">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PREFERENCES"></span><span id="error_invalid_preferences"></span><dl> <span data-ttu-id="870d7-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-730">A preferência de destino VPN não está selecionada pelo usuário ou não é mais válida.</span><span class="sxs-lookup"><span data-stu-id="870d7-730">Either VPN destination preference is not selected by the user or it is no longer valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-731">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-731">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_scard_cache_credentials_invalid"></span><dl> <span data-ttu-id="870d7-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-733">A credencial de cartão inteligente armazenada em cache é inválida.</span><span class="sxs-lookup"><span data-stu-id="870d7-733">Cached smart card credential is invalid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-734">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-734">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SSTP_COOKIE_SET_FAILURE"></span><span id="error_sstp_cookie_set_failure"></span><dl> <span data-ttu-id="870d7-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-736">Falha na tentativa de conexão VPN devido a um erro interno ao adicionar cookies ao SSTP (Secure Socket encapsulating Protocol).</span><span class="sxs-lookup"><span data-stu-id="870d7-736">VPN connection attempt failed due to internal error occurred while adding cookies to the Secure Socket Tunneling Protocol (SSTP).</span></span> <span data-ttu-id="870d7-737">Consulte o log de eventos do sistema para obter as informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="870d7-737">Please see the System Event Log for the detailed information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES"></span><span id="error_invalid_peap_cookie_attributes"></span><dl> <span data-ttu-id="870d7-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-739">Os atributos do método interno PEAP armazenados no cookie são inválidos.</span><span class="sxs-lookup"><span data-stu-id="870d7-739">The PEAP inner method attribute(s) stored in the cookie is/are invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_NOT_INSTALLED"></span><span id="error_eap_method_not_installed"></span><dl> <span data-ttu-id="870d7-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-741">O tipo de protocolo de autenticação extensível necessário para autenticação da conexão de acesso remoto não está instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="870d7-741">The Extensible Authentication Protocol type required for authentication of the remote access connection is not installed on your computer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO"></span><span id="error_eap_method_does_not_support_sso"></span><dl> <span data-ttu-id="870d7-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-743">O tipo de protocolo de autenticação extensível configurado na conexão de acesso remoto não oferece suporte ao logon único.</span><span class="sxs-lookup"><span data-stu-id="870d7-743">The Extensible Authentication Protocol type configured on the remote access connection does not support single sign-on.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="error_eap_method_operation_not_supported"></span><dl> <span data-ttu-id="870d7-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-745">O tipo de protocolo de autenticação extensível configurado na conexão de acesso remoto não oferece suporte à operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="870d7-745">The Extensible Authentication Protocol type configured on the remote access connection does not support the requested operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_INVALID"></span><span id="error_eap_user_cert_invalid"></span><dl> <span data-ttu-id="870d7-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-747">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que autentica o cliente para o servidor não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-747">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is not valid.</span></span> <span data-ttu-id="870d7-748">Verifique se o certificado usado para autenticação é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-748">Ensure that the certificate used for authentication is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_EXPIRED"></span><span id="error_eap_user_cert_expired"></span><dl> <span data-ttu-id="870d7-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-750">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que autentica o cliente para o servidor expirou.</span><span class="sxs-lookup"><span data-stu-id="870d7-750">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is expired.</span></span> <span data-ttu-id="870d7-751">Renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-751">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_REVOKED"></span><span id="error_eap_user_cert_revoked"></span><dl> <span data-ttu-id="870d7-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-753">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que autentica o cliente para o servidor foi revogado.</span><span class="sxs-lookup"><span data-stu-id="870d7-753">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is revoked.</span></span> <span data-ttu-id="870d7-754">Use um certificado que não tenha sido revogado.</span><span class="sxs-lookup"><span data-stu-id="870d7-754">Use a certificate that has not been revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_OTHER_ERROR"></span><span id="error_eap_user_cert_other_error"></span><dl> <span data-ttu-id="870d7-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-756">A conexão de acesso remoto foi concluída, mas a autenticação falhou devido a um erro no certificado que autentica o cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="870d7-756">The remote access connection completed, but authentication failed because of an error in the certificate that authenticates the client to the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_INVALID"></span><span id="error_eap_server_cert_invalid"></span><dl> <span data-ttu-id="870d7-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-758">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que o cliente usa para autenticar o servidor não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-758">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_EXPIRED"></span><span id="error_eap_server_cert_expired"></span><dl> <span data-ttu-id="870d7-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-760">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que o cliente usa para autenticar o servidor expirou.</span><span class="sxs-lookup"><span data-stu-id="870d7-760">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_REVOKED"></span><span id="error_eap_server_cert_revoked"></span><dl> <span data-ttu-id="870d7-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-762">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que o cliente usa para autenticar o servidor foi revogado.</span><span class="sxs-lookup"><span data-stu-id="870d7-762">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_OTHER_ERROR"></span><span id="error_eap_server_cert_other_error"></span><dl> <span data-ttu-id="870d7-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-764">A conexão de acesso remoto foi concluída, mas a autenticação falhou devido a um erro no certificado que o cliente usa para autenticar o servidor.</span><span class="sxs-lookup"><span data-stu-id="870d7-764">The remote access connection completed, but authentication failed because of an error in the certificate that the client uses to authenticate the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_user_root_cert_not_found"></span><dl> <span data-ttu-id="870d7-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-766">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque um certificado raiz confiável que valida o certificado de usuário não foi encontrado no repositório de certificados de autoridades de certificação raiz confiáveis.</span><span class="sxs-lookup"><span data-stu-id="870d7-766">The remote access connection completed, but authentication failed because a trusted root certificate that validates the user certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_ROOT_CERT_INVALID"></span><span id="error_eap_user_root_cert_invalid"></span><dl> <span data-ttu-id="870d7-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-768">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado raiz confiável usado para validar o certificado do usuário não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-768">The remote access connection completed, but authentication failed because the trusted root certificate that is used to validate the user certificate is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_EXPIRED"></span><span id="error_eap_user_root_cert_expired"></span><dl> <span data-ttu-id="870d7-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-770">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado no repositório de certificados das autoridades de certificação raiz confiáveis que autentica o certificado do usuário expirou.</span><span class="sxs-lookup"><span data-stu-id="870d7-770">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that authenticates the user certificate is expired.</span></span> <span data-ttu-id="870d7-771">Renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-771">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_server_root_cert_not_found"></span><dl> <span data-ttu-id="870d7-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-773">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque um certificado que valida o certificado do servidor não foi encontrado no repositório de certificados das autoridades de certificação raiz confiáveis.</span><span class="sxs-lookup"><span data-stu-id="870d7-773">The remote access connection completed, but authentication failed because a certificate that validates the server certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_INVALID"></span><span id="error_eap_server_root_cert_invalid"></span><dl> <span data-ttu-id="870d7-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-775">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado no repositório de certificados de autoridades de certificação raiz confiáveis que valida o certificado do servidor não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-775">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that validates the server certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="error_eap_server_root_cert_name_required"></span><dl> <span data-ttu-id="870d7-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-777">A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado no computador servidor não tem um nome de servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="870d7-777">The remote access connection completed, but authentication failed because the certificate on the server computer does not have a server name specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_IDENTITY_MISMATCH"></span><span id="error_peap_identity_mismatch"></span><dl> <span data-ttu-id="870d7-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-779">A identidade externa de PEAP não é igual à identidade interna quando a privacidade de identidade está desativada.</span><span class="sxs-lookup"><span data-stu-id="870d7-779">The PEAP outer identity is not same as the inner identity when identity privacy is turned OFF.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DNSNAME_NOT_RESOLVABLE"></span><span id="error_dnsname_not_resolvable"></span><dl> <span data-ttu-id="870d7-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-781">A conexão remota não foi feita porque o nome do servidor de acesso remoto não foi resolvido.</span><span class="sxs-lookup"><span data-stu-id="870d7-781">The remote connection was not made because the name of the remote access server did not resolve.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_PASSWD_INVALID"></span><span id="error_eaptls_passwd_invalid"></span><dl> <span data-ttu-id="870d7-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-783">A senha fornecida para o certificado não é válida.</span><span class="sxs-lookup"><span data-stu-id="870d7-783">The password provided for the certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS"></span><span id="error_ikev2_psk_interface_already_exists"></span><dl> <span data-ttu-id="870d7-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-785">A interface não pôde ser habilitada porque mais de uma interface com o mesmo destino foi criada com o método de autenticação de chave pré-compartilhada.</span><span class="sxs-lookup"><span data-stu-id="870d7-785">The interface could not be enabled because more than one interface with the same destination has been created with the pre-shared key authentication method.</span></span> <span data-ttu-id="870d7-786">Altere o método de destino/autenticação e habilite a interface.</span><span class="sxs-lookup"><span data-stu-id="870d7-786">Change the destination/auth method and enable the interface.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="870d7-787">Os códigos de erro da API RRAS (roteamento e acesso remoto) a seguir são definidos em Mprerror. h.</span><span class="sxs-lookup"><span data-stu-id="870d7-787">The following Routing and Remote Access (RRAS) API error codes are defined in mprerror.h.</span></span> <span data-ttu-id="870d7-788">Todos os códigos de erro têm suporte no Windows 2000 ou em versões posteriores do Windows, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="870d7-788">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="870d7-789">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="870d7-789">Return code/value</span></span></th>
<th><span data-ttu-id="870d7-790">Descrição</span><span class="sxs-lookup"><span data-stu-id="870d7-790">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ERROR_ROUTER_STOPPED"></span><span id="error_router_stopped"></span><dl> <span data-ttu-id="870d7-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-792">O roteador não está em execução.</span><span class="sxs-lookup"><span data-stu-id="870d7-792">The router is not running.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_CONNECTED"></span><span id="error_already_connected"></span><dl> <span data-ttu-id="870d7-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-794">A interface já está conectada.</span><span class="sxs-lookup"><span data-stu-id="870d7-794">The interface is already connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_PROTOCOL_ID"></span><span id="error_unknown_protocol_id"></span><dl> <span data-ttu-id="870d7-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-796">O identificador de protocolo especificado não é conhecido pelo roteador.</span><span class="sxs-lookup"><span data-stu-id="870d7-796">The specified protocol identifier is not known to the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DDM_NOT_RUNNING"></span><span id="error_ddm_not_running"></span><dl> <span data-ttu-id="870d7-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-798">O DDM (Gerenciador de interface de discagem por demanda) não está em execução.</span><span class="sxs-lookup"><span data-stu-id="870d7-798">The Demand-dial Interface Manager (DDM) is not running.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_ALREADY_EXISTS"></span><span id="error_interface_already_exists"></span><dl> <span data-ttu-id="870d7-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-800">Uma interface com esse nome já está registrada com o roteador.</span><span class="sxs-lookup"><span data-stu-id="870d7-800">An interface with this name is already registered with the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_SUCH_INTERFACE"></span><span id="error_no_such_interface"></span><dl> <span data-ttu-id="870d7-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-802">Uma interface com esse nome não está registrada no roteador.</span><span class="sxs-lookup"><span data-stu-id="870d7-802">An interface with this name is not registered with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_NOT_CONNECTED"></span><span id="error_interface_not_connected"></span><dl> <span data-ttu-id="870d7-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-804">A interface não está conectada.</span><span class="sxs-lookup"><span data-stu-id="870d7-804">The interface is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_STOP_PENDING"></span><span id="error_protocol_stop_pending"></span><dl> <span data-ttu-id="870d7-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-806">O protocolo especificado está parando.</span><span class="sxs-lookup"><span data-stu-id="870d7-806">The specified protocol is stopping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONNECTED"></span><span id="error_interface_connected"></span><dl> <span data-ttu-id="870d7-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-808">A interface está conectada e, portanto, não pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="870d7-808">The interface is connected and hence cannot be deleted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_INTERFACE_CREDENTIALS_SET"></span><span id="error_no_interface_credentials_set"></span><dl> <span data-ttu-id="870d7-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-810">As credenciais da interface não foram definidas.</span><span class="sxs-lookup"><span data-stu-id="870d7-810">The interface credentials have not been set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALREADY_CONNECTING"></span><span id="error_already_connecting"></span><dl> <span data-ttu-id="870d7-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-812">Esta interface já está no processo de conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-812">This interface is already in the process of connecting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UPDATE_IN_PROGRESS"></span><span id="error_update_in_progress"></span><dl> <span data-ttu-id="870d7-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-814">Uma atualização das informações de roteamento nesta interface já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="870d7-814">An update of routing information on this interface is already in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONFIGURATION"></span><span id="error_interface_configuration"></span><dl> <span data-ttu-id="870d7-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-816">A interface de interfaces não é válida.</span><span class="sxs-lookup"><span data-stu-id="870d7-816">The interface configration is not valid.</span></span> <span data-ttu-id="870d7-817">Já existe outra interface que está conectada à mesma interface no roteador remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-817">There is already another interface that is connected to the same interface on the remote router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_CLIENT_PORT"></span><span id="error_not_client_port"></span><dl> <span data-ttu-id="870d7-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-819">Um cliente de acesso remoto tentou conectar-se por uma porta que foi reservada apenas para roteadores.</span><span class="sxs-lookup"><span data-stu-id="870d7-819">A Remote Access Client attempted to connect over a port that was reserved for routers only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_ROUTER_PORT"></span><span id="error_not_router_port"></span><dl> <span data-ttu-id="870d7-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-821">Um roteador de discagem por demanda tentou conectar-se por uma porta reservada somente para clientes de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-821">A Demand Dial Router attempted to connect over a port that was reserved for Remote Access Clients only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CLIENT_INTERFACE_ALREADY_EXISTS"></span><span id="error_client_interface_already_exists"></span><dl> <span data-ttu-id="870d7-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-823">A interface do cliente com esse nome já existe e está conectada no momento.</span><span class="sxs-lookup"><span data-stu-id="870d7-823">The client interface with this name already exists and is currently connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_DISABLED"></span><span id="error_interface_disabled"></span><dl> <span data-ttu-id="870d7-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-825">A interface está em um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="870d7-825">The interface is in a disabled state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_PROTOCOL_REJECTED"></span><span id="error_auth_protocol_rejected"></span><dl> <span data-ttu-id="870d7-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-827">O protocolo de autenticação foi rejeitado pelo par remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-827">The authentication protocol was rejected by the remote peer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_AUTH_PROTOCOL_AVAILABLE"></span><span id="error_no_auth_protocol_available"></span><dl> <span data-ttu-id="870d7-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-829">Não há protocolos de autenticação disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="870d7-829">There are no authentication protocols available for use.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEER_REFUSED_AUTH"></span><span id="error_peer_refused_auth"></span><dl> <span data-ttu-id="870d7-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-831">Não foi possível estabelecer a conexão porque o protocolo de autenticação usado pelo servidor RAS/VPN para verificar seu nome de usuário e senha não pôde ser correspondido com as configurações em seu perfil de conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-831">The connection could not be established because the authentication protocol used by the RAS/VPN server to verify your username and password could not be matched with the settings in your connection profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_NO_DIALIN_PERMISSION"></span><span id="error_remote_no_dialin_permission"></span><dl> <span data-ttu-id="870d7-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-833">A conta remota não tem permissão de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="870d7-833">The remote account does not have Remote Access permission.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_PASSWD_EXPIRED"></span><span id="error_remote_passwd_expired"></span><dl> <span data-ttu-id="870d7-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-835">A conta remota expirou.</span><span class="sxs-lookup"><span data-stu-id="870d7-835">The remote account has expired.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_ACCT_DISABLED"></span><span id="error_remote_acct_disabled"></span><dl> <span data-ttu-id="870d7-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-837">A conta remota está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="870d7-837">The remote account is disabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_RESTRICTED_LOGON_HOURS"></span><span id="error_remote_restricted_logon_hours"></span><dl> <span data-ttu-id="870d7-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-839">A conta remota não tem permissão para fazer logon no momento do dia.</span><span class="sxs-lookup"><span data-stu-id="870d7-839">The remote account is not permitted to logon at this time of day.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_AUTHENTICATION_FAILURE"></span><span id="error_remote_authentication_failure"></span><dl> <span data-ttu-id="870d7-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-841">O acesso foi negado ao par remoto porque o nome de usuário, a senha ou ambos não são válidos no domínio.</span><span class="sxs-lookup"><span data-stu-id="870d7-841">Access was denied to the remote peer because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_HAS_NO_DEVICES"></span><span id="error_interface_has_no_devices"></span><dl> <span data-ttu-id="870d7-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-843">Não há portas habilitadas para roteamento disponíveis para uso por esta interface de discagem por demanda.</span><span class="sxs-lookup"><span data-stu-id="870d7-843">There are no routing enabled ports available for use by this demand dial interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_DISCONNECTED"></span><span id="error_idle_disconnected"></span><dl> <span data-ttu-id="870d7-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-845">A porta foi desconectada devido a inatividade.</span><span class="sxs-lookup"><span data-stu-id="870d7-845">The port has been disconnected due to inactivity.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_UNREACHABLE"></span><span id="error_interface_unreachable"></span><dl> <span data-ttu-id="870d7-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-847">A interface não está acessível no momento.</span><span class="sxs-lookup"><span data-stu-id="870d7-847">The interface is not reachable at this time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVICE_IS_PAUSED"></span><span id="error_service_is_paused"></span><dl> <span data-ttu-id="870d7-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-849">O serviço de discagem por demanda está em um estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="870d7-849">The Demand Dial service is in a paused state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_DISCONNECTED"></span><span id="error_interface_disconnected"></span><dl> <span data-ttu-id="870d7-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-851">A interface foi desconectada pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="870d7-851">The interface has been disconnected by the administrator.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_SERVER_TIMEOUT"></span><span id="error_auth_server_timeout"></span><dl> <span data-ttu-id="870d7-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-853">O servidor de autenticação não respondeu às solicitações de autenticação em tempo hábil.</span><span class="sxs-lookup"><span data-stu-id="870d7-853">The authentication server did not respond to authentication requests in a timely fashion.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_LIMIT_REACHED"></span><span id="error_port_limit_reached"></span><dl> <span data-ttu-id="870d7-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-855">O número máximo de portas permitidas para uso na conexão de vários vínculos foi atingido.</span><span class="sxs-lookup"><span data-stu-id="870d7-855">The maximum number of ports allowed for use in the multi-linked connection has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_SESSION_TIMEOUT"></span><span id="error_ppp_session_timeout"></span><dl> <span data-ttu-id="870d7-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-857">O limite de tempo de conexão para o usuário foi atingido.</span><span class="sxs-lookup"><span data-stu-id="870d7-857">The connection time limit for the user has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_LAN_INTERFACE_LIMIT"></span><span id="error_max_lan_interface_limit"></span><dl> <span data-ttu-id="870d7-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-859">O limite máximo do número de interfaces de LAN com suporte foi atingido.</span><span class="sxs-lookup"><span data-stu-id="870d7-859">The maximum limit on the number of LAN interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MAX_WAN_INTERFACE_LIMIT"></span><span id="error_max_wan_interface_limit"></span><dl> <span data-ttu-id="870d7-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-861">O limite máximo no número de interfaces de discagem por demanda com suporte foi atingido.</span><span class="sxs-lookup"><span data-stu-id="870d7-861">The maximum limit on the number of Demand Dial interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_CLIENT_INTERFACE_LIMIT"></span><span id="error_max_client_interface_limit"></span><dl> <span data-ttu-id="870d7-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-863">O limite máximo do número de clientes de acesso remoto com suporte foi atingido.</span><span class="sxs-lookup"><span data-stu-id="870d7-863">The maximum limit on the number of Remote Access Clients supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAP_DISCONNECTED"></span><span id="error_bap_disconnected"></span><dl> <span data-ttu-id="870d7-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-865">A porta foi desconectada devido à política do Protocolo BAP (Bandwidth Allocation Protocol).</span><span class="sxs-lookup"><span data-stu-id="870d7-865">The port has been disconnected due to the Bandwidth Allocation Protocol (BAP) policy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_LIMIT"></span><span id="error_user_limit"></span><dl> <span data-ttu-id="870d7-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-867">Como outra conexão do seu tipo está em uso, a conexão de entrada não pode aceitar sua solicitação de conexão.</span><span class="sxs-lookup"><span data-stu-id="870d7-867">Because another connection of your type is in use, the incoming connection cannot accept your connection request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RADIUS_SERVERS"></span><span id="error_no_radius_servers"></span><dl> <span data-ttu-id="870d7-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-869">Nenhum servidor RADIUS estava localizado na rede.</span><span class="sxs-lookup"><span data-stu-id="870d7-869">No RADIUS servers were located on the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_RADIUS_RESPONSE"></span><span id="error_invalid_radius_response"></span><dl> <span data-ttu-id="870d7-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-871">A resposta recebida do servidor de autenticação RADIUS não era válida.</span><span class="sxs-lookup"><span data-stu-id="870d7-871">The response received from the RADIUS authentication server was not valid.</span></span> <span data-ttu-id="870d7-872">Verifique se a senha de segredo sensível ao caso do servidor RADIUS está definida corretamente.</span><span class="sxs-lookup"><span data-stu-id="870d7-872">Make sure that the case sensitive secret password for the RADIUS server is set correctly.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALIN_HOURS_RESTRICTION"></span><span id="error_dialin_hours_restriction"></span><dl> <span data-ttu-id="870d7-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-874">Você não tem permissão para se conectar neste momento.</span><span class="sxs-lookup"><span data-stu-id="870d7-874">You do not have permission to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALLOWED_PORT_TYPE_RESTRICTION"></span><span id="error_allowed_port_type_restriction"></span><dl> <span data-ttu-id="870d7-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-876">Você não tem permissão para se conectar usando o tipo de dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="870d7-876">You do not have permission to connect using the current device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_PROTOCOL_RESTRICTION"></span><span id="error_auth_protocol_restriction"></span><dl> <span data-ttu-id="870d7-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-878">Não foi possível estabelecer a conexão porque o método de autenticação usado pelo seu perfil de conexão não é permitido para uso por uma política de acesso configurada no servidor RAS/VPN.</span><span class="sxs-lookup"><span data-stu-id="870d7-878">The connection could not be established because the authentication method used by your connection profile is not permitted for use by an access policy configured on the RAS/VPN server.</span></span> <span data-ttu-id="870d7-879">Especificamente, isso pode ser devido a diferenças de configuração entre o método de autenticação selecionado no servidor RAS/VPN e a política de acesso configurada para ele.</span><span class="sxs-lookup"><span data-stu-id="870d7-879">Specifically, this could be due to configuration differences between the authentication method selected on the RAS/VPN server and the access policy configured for it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAP_REQUIRED"></span><span id="error_bap_required"></span><dl> <span data-ttu-id="870d7-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-881">BAP é necessário para este usuário.</span><span class="sxs-lookup"><span data-stu-id="870d7-881">BAP is required for this user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALOUT_HOURS_RESTRICTION"></span><span id="error_dialout_hours_restriction"></span><dl> <span data-ttu-id="870d7-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-883">A interface não tem permissão para se conectar neste momento.</span><span class="sxs-lookup"><span data-stu-id="870d7-883">The interface is not allowed to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTER_CONFIG_INCOMPATIBLE"></span><span id="error_router_config_incompatible"></span><dl> <span data-ttu-id="870d7-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-885">A configuração do roteador salva é incompatível com o roteador atual.</span><span class="sxs-lookup"><span data-stu-id="870d7-885">The saved router configuration is incompatible with the current router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_NO_MD5_MIGRATION"></span><span id="warning_no_md5_migration"></span><dl> <span data-ttu-id="870d7-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-887">O acesso remoto detectou contas de usuário de formato mais antigo que não serão migradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="870d7-887">Remote Access has detected older format user accounts that will not be migrated automatically.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ALREADY_INSTALLED"></span><span id="error_protocol_already_installed"></span><dl> <span data-ttu-id="870d7-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-889">O transporte já está instalado com o roteador.</span><span class="sxs-lookup"><span data-stu-id="870d7-889">The transport is already installed with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIGNATURE_LENGTH"></span><span id="error_invalid_signature_length"></span><dl> <span data-ttu-id="870d7-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-891">O tamanho da assinatura recebido em um pacote do servidor RADIUS não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-891">The signature length received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-892">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-892">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SIGNATURE"></span><span id="error_invalid_signature"></span><dl> <span data-ttu-id="870d7-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-894">A assinatura recebida em um pacote do servidor RADIUS não é válida.</span><span class="sxs-lookup"><span data-stu-id="870d7-894">The signature received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-895">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-895">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SIGNATURE"></span><span id="error_no_signature"></span><dl> <span data-ttu-id="870d7-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-897">Não recebeu assinatura junto com EAPMessage do servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="870d7-897">Did not receive signature along with EAPMessage from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-898">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-898">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET_LENGTH_OR_ID"></span><span id="error_invalid_packet_length_or_id"></span><dl> <span data-ttu-id="870d7-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-900">O comprimento ou a ID recebidos em um pacote do servidor RADIUS não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-900">The length or Id received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-901">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-901">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_ATTRIBUTE_LENGTH"></span><span id="error_invalid_attribute_length"></span><dl> <span data-ttu-id="870d7-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-903">O comprimento recebido em um pacote com o atributo do servidor RADIUS não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-903">The length received in a packet with attribute from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-904">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-904">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET"></span><span id="error_invalid_packet"></span><dl> <span data-ttu-id="870d7-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-906">O pacote recebido do servidor RADIUS não é válido.</span><span class="sxs-lookup"><span data-stu-id="870d7-906">The packet received from RADIUS server in not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-907">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-907">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTHENTICATOR_MISMATCH"></span><span id="error_authenticator_mismatch"></span><dl> <span data-ttu-id="870d7-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-909">O autenticador não corresponde ao pacote do servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="870d7-909">Authenticator does not match in packet from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-910">Com suporte no Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-910">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTEACCESS_NOT_CONFIGURED"></span><span id="error_remoteaccess_not_configured"></span><dl> <span data-ttu-id="870d7-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span><span class="sxs-lookup"><span data-stu-id="870d7-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span></span></dl></td>
<td><span data-ttu-id="870d7-912">O servidor de roteamento e acesso remoto não está configurado ou não está em execução.</span><span class="sxs-lookup"><span data-stu-id="870d7-912">Routing and Remote access server is either not configured or not running.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="870d7-913">Com suporte no Windows 7 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="870d7-913">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="870d7-914">Requisitos</span><span class="sxs-lookup"><span data-stu-id="870d7-914">Requirements</span></span>



| <span data-ttu-id="870d7-915">Requisito</span><span class="sxs-lookup"><span data-stu-id="870d7-915">Requirement</span></span> | <span data-ttu-id="870d7-916">Valor</span><span class="sxs-lookup"><span data-stu-id="870d7-916">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="870d7-917">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="870d7-917">Minimum supported client</span></span><br/> | <span data-ttu-id="870d7-918">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="870d7-918">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="870d7-919">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="870d7-919">Minimum supported server</span></span><br/> | <span data-ttu-id="870d7-920">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="870d7-920">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 





