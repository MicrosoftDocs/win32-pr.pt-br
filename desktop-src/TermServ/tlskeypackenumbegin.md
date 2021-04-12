---
title: Função TLSKeyPackEnumBegin
description: Inicia a enumeração por meio de todos os pacotes de chaves instalados em um servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- Função TLSKeyPackEnumBegin Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f61197e3c08f5608be954a9288ea54cad5586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295899"
---
# <a name="tlskeypackenumbegin-function"></a><span data-ttu-id="26d2d-104">Função TLSKeyPackEnumBegin</span><span class="sxs-lookup"><span data-stu-id="26d2d-104">TLSKeyPackEnumBegin function</span></span>

<span data-ttu-id="26d2d-105">Inicia a enumeração por meio de todos os pacotes de chaves instalados em um servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="26d2d-105">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="26d2d-106">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="26d2d-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="26d2d-107">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="26d2d-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="26d2d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26d2d-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="26d2d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26d2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d2d-110">*hHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26d2d-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d2d-111">Identificador para um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="26d2d-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="26d2d-112">Especifique um identificador que é aberto pela função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="26d2d-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="26d2d-113">*dwSearchParm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26d2d-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d2d-114">Especifica os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="26d2d-114">Specifies the search criteria.</span></span> <span data-ttu-id="26d2d-115">Esse parâmetro é reservado para uso futuro e deve conter 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="26d2d-115">This parameter is reserved for future use and must contain 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="26d2d-116">*bMatchAll* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26d2d-116">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d2d-117">Especifica se é para corresponder a todos os valores de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="26d2d-117">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="26d2d-118">*lpSearchParm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26d2d-118">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d2d-119">Ponteiro para uma estrutura [**LSKeyPack**](lskeypack.md) que especifica os parâmetros de pesquisa a serem procurados.</span><span class="sxs-lookup"><span data-stu-id="26d2d-119">Pointer to a [**LSKeyPack**](lskeypack.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="26d2d-120">*pdwErrCode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="26d2d-120">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26d2d-121">Ponteiro para uma variável que recebe um dos seguintes códigos de erro no retorno.</span><span class="sxs-lookup"><span data-stu-id="26d2d-121">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="26d2d-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S com \_ êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="26d2d-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="26d2d-123">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="26d2d-123">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="26d2d-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ \_ \_ Erro interno E** (5001)</span><span class="sxs-lookup"><span data-stu-id="26d2d-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="26d2d-125">Erro interno no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="26d2d-125">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="26d2d-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ \_ \_ Sequência inválida E** (5006)</span><span class="sxs-lookup"><span data-stu-id="26d2d-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="26d2d-127">A sequência de chamada não era válida.</span><span class="sxs-lookup"><span data-stu-id="26d2d-127">The calling sequence was not valid.</span></span> <span data-ttu-id="26d2d-128">Provavelmente, uma enumeração anterior não terminou.</span><span class="sxs-lookup"><span data-stu-id="26d2d-128">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="26d2d-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ \_Servidor E \_ ocupado** (5007)</span><span class="sxs-lookup"><span data-stu-id="26d2d-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="26d2d-130">O servidor de licenças está muito ocupado para processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="26d2d-130">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="26d2d-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="26d2d-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="26d2d-132">Não é possível processar a solicitação devido à memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="26d2d-132">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="26d2d-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ dados inválidos** (5009)</span><span class="sxs-lookup"><span data-stu-id="26d2d-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="26d2d-134">Os dados no parâmetro de pesquisa não são válidos.</span><span class="sxs-lookup"><span data-stu-id="26d2d-134">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26d2d-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26d2d-135">Return value</span></span>

<span data-ttu-id="26d2d-136">Essa função retorna os seguintes valores de retorno possíveis.</span><span class="sxs-lookup"><span data-stu-id="26d2d-136">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="26d2d-137">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="26d2d-137">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="26d2d-138">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="26d2d-138">The call succeeded.</span></span> <span data-ttu-id="26d2d-139">Verifique o valor do parâmetro *pdwErrCode* para obter o código de retorno para a chamada.</span><span class="sxs-lookup"><span data-stu-id="26d2d-139">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="26d2d-140">**ARG. de RPC \_ \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="26d2d-140">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="26d2d-141">O argumento não era válido.</span><span class="sxs-lookup"><span data-stu-id="26d2d-141">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26d2d-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26d2d-142">Requirements</span></span>



| <span data-ttu-id="26d2d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d2d-143">Requirement</span></span> | <span data-ttu-id="26d2d-144">Valor</span><span class="sxs-lookup"><span data-stu-id="26d2d-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26d2d-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26d2d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="26d2d-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26d2d-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26d2d-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26d2d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="26d2d-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26d2d-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26d2d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="26d2d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d2d-150"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d2d-150"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26d2d-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="26d2d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d2d-152">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="26d2d-152">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="26d2d-153">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="26d2d-153">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="26d2d-154">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="26d2d-154">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="26d2d-155">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="26d2d-155">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

