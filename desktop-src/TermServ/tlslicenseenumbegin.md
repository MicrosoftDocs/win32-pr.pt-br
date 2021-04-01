---
title: Função TLSLicenseEnumBegin
description: Inicia a enumeração de licenças emitidas pelo servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Função TLSLicenseEnumBegin Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645176"
---
# <a name="tlslicenseenumbegin-function"></a><span data-ttu-id="ea78c-104">Função TLSLicenseEnumBegin</span><span class="sxs-lookup"><span data-stu-id="ea78c-104">TLSLicenseEnumBegin function</span></span>

<span data-ttu-id="ea78c-105">Inicia a enumeração de licenças emitidas pelo servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea78c-105">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="ea78c-106">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="ea78c-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="ea78c-107">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="ea78c-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ea78c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea78c-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="ea78c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea78c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea78c-110">*hHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea78c-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea78c-111">Identificador para um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ea78c-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="ea78c-112">Especifique um identificador que é aberto pela função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="ea78c-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ea78c-113">*dwSearchParm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea78c-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea78c-114">Especifica os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea78c-114">Specifies the search criteria.</span></span> <span data-ttu-id="ea78c-115">O parâmetro pode ser um ou uma combinação dos valores descritos na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea78c-115">The parameter can be one or a combination of the values that are described in the following list.</span></span> <span data-ttu-id="ea78c-116">O parâmetro especifica o tipo de pacote de chaves e o pacote de chaves a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="ea78c-116">The parameter specifies the type of key pack and which key pack to search.</span></span>

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span data-ttu-id="ea78c-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ \_Licença de pesquisa** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="ea78c-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE\_SEARCH\_LICENSEID** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-118">Pesquisar por ID da licença.</span><span class="sxs-lookup"><span data-stu-id="ea78c-118">Search by license ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span data-ttu-id="ea78c-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ SEARCH \_ Packid** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="ea78c-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE\_SEARCH\_KEYPACKID** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-120">Pesquise por ID do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="ea78c-120">Search by key pack ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span data-ttu-id="ea78c-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ Pesquisar \_ MachineName** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="ea78c-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE\_SEARCH\_MACHINENAME** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-122">Pesquisar por nome do computador.</span><span class="sxs-lookup"><span data-stu-id="ea78c-122">Search by machine name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span data-ttu-id="ea78c-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ \_Nome de usuário da pesquisa** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="ea78c-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE\_SEARCH\_USERNAME** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-124">Pesquisar por nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="ea78c-124">Search by user name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span data-ttu-id="ea78c-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ PESQUISA \_ emitida** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="ea78c-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE\_SEARCH\_ISSUEDATE** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-126">Pesquisar por data de emissão.</span><span class="sxs-lookup"><span data-stu-id="ea78c-126">Search by issue date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span data-ttu-id="ea78c-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ PESQUISA \_ expirada** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="ea78c-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE\_SEARCH\_EXPIREDATE** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-128">Pesquisar por data de validade.</span><span class="sxs-lookup"><span data-stu-id="ea78c-128">Search by expiration date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span data-ttu-id="ea78c-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ Pesquisar \_ NUMLICENSES** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="ea78c-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE\_SEARCH\_ NUMLICENSES** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-130">Pesquisar por número de licenças.</span><span class="sxs-lookup"><span data-stu-id="ea78c-130">Search by number of licenses.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span data-ttu-id="ea78c-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ \_ \_ Status de entrada de pesquisa** (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="ea78c-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE\_SEARCH\_ ENTRY\_STATUS** (0x20000000)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-132">Pesquisar por status de entrada.</span><span class="sxs-lookup"><span data-stu-id="ea78c-132">Search by entry status.</span></span>

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span data-ttu-id="ea78c-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ \_LICENSESTATUS do exsearch** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="ea78c-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE\_EXSEARCH\_LICENSESTATUS** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-134">Pesquisar por status da licença.</span><span class="sxs-lookup"><span data-stu-id="ea78c-134">Search by license status.</span></span>

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span data-ttu-id="ea78c-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ Pesquisar \_ tudo** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="ea78c-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK\_SEARCH\_ALL** (0xFFFFFFFF)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-136">Pesquisar todas as licenças.</span><span class="sxs-lookup"><span data-stu-id="ea78c-136">Search all licenses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ea78c-137">*bMatchAll* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea78c-137">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea78c-138">Especifica se é para corresponder a todos os valores de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea78c-138">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="ea78c-139">*lpSearchParm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea78c-139">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea78c-140">Ponteiro para uma estrutura [**LSLicense**](lslicense.md) que especifica os parâmetros de pesquisa a serem procurados.</span><span class="sxs-lookup"><span data-stu-id="ea78c-140">Pointer to a [**LSLicense**](lslicense.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="ea78c-141">*pdwErrCode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ea78c-141">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea78c-142">Ponteiro para uma variável que recebe um dos seguintes códigos de erro no retorno.</span><span class="sxs-lookup"><span data-stu-id="ea78c-142">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="ea78c-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S com \_ êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="ea78c-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-144">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ea78c-144">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="ea78c-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ \_ \_ Erro interno E** (5001)</span><span class="sxs-lookup"><span data-stu-id="ea78c-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-146">Erro interno no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ea78c-146">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="ea78c-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ \_ \_ Sequência inválida E** (5006)</span><span class="sxs-lookup"><span data-stu-id="ea78c-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-148">A sequência de chamada não era válida.</span><span class="sxs-lookup"><span data-stu-id="ea78c-148">The calling sequence was not valid.</span></span> <span data-ttu-id="ea78c-149">Provavelmente, uma enumeração anterior não terminou.</span><span class="sxs-lookup"><span data-stu-id="ea78c-149">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="ea78c-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ \_Servidor E \_ ocupado** (5007)</span><span class="sxs-lookup"><span data-stu-id="ea78c-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-151">O servidor de licenças está muito ocupado para processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ea78c-151">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="ea78c-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="ea78c-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-153">Não é possível processar a solicitação devido à memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="ea78c-153">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="ea78c-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ dados inválidos** (5009)</span><span class="sxs-lookup"><span data-stu-id="ea78c-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="ea78c-155">Os dados no parâmetro de pesquisa não são válidos.</span><span class="sxs-lookup"><span data-stu-id="ea78c-155">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea78c-156">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea78c-156">Return value</span></span>

<span data-ttu-id="ea78c-157">Essa função retorna os seguintes valores de retorno possíveis.</span><span class="sxs-lookup"><span data-stu-id="ea78c-157">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="ea78c-158">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="ea78c-158">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="ea78c-159">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ea78c-159">The call succeeded.</span></span> <span data-ttu-id="ea78c-160">Verifique o valor do parâmetro *pdwErrCode* para obter o código de retorno para a chamada.</span><span class="sxs-lookup"><span data-stu-id="ea78c-160">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="ea78c-161">**ARG. de RPC \_ \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="ea78c-161">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="ea78c-162">O argumento não era válido.</span><span class="sxs-lookup"><span data-stu-id="ea78c-162">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea78c-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea78c-163">Requirements</span></span>



| <span data-ttu-id="ea78c-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea78c-164">Requirement</span></span> | <span data-ttu-id="ea78c-165">Valor</span><span class="sxs-lookup"><span data-stu-id="ea78c-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea78c-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea78c-166">Minimum supported client</span></span><br/> | <span data-ttu-id="ea78c-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea78c-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea78c-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea78c-168">Minimum supported server</span></span><br/> | <span data-ttu-id="ea78c-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea78c-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea78c-170">DLL</span><span class="sxs-lookup"><span data-stu-id="ea78c-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea78c-171"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea78c-171"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea78c-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea78c-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea78c-173">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="ea78c-173">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="ea78c-174">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="ea78c-174">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="ea78c-175">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="ea78c-175">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="ea78c-176">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="ea78c-176">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

