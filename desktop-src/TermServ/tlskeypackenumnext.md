---
title: Função TLSKeyPackEnumNext
description: Continua de uma chamada anterior para a função TLSKeyPackEnumBegin e retorna o próximo pacote de chaves instalado em um servidor de licença Área de Trabalho Remota que corresponde aos critérios de pesquisa.
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- Função TLSKeyPackEnumNext Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSKeyPackEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897874f333ed7933ea1616f7f5ba5f1686736d0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008962"
---
# <a name="tlskeypackenumnext-function"></a><span data-ttu-id="3cc8f-104">Função TLSKeyPackEnumNext</span><span class="sxs-lookup"><span data-stu-id="3cc8f-104">TLSKeyPackEnumNext function</span></span>

<span data-ttu-id="3cc8f-105">Continua de uma chamada anterior para a função [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e retorna o próximo pacote de chaves instalado em um servidor de licença área de trabalho remota que corresponde aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="3cc8f-106">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="3cc8f-107">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3cc8f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cc8f-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="3cc8f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cc8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cc8f-110">*hHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3cc8f-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc8f-111">Identificador para um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="3cc8f-112">Especifique um identificador que é aberto pela função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="3cc8f-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3cc8f-113">*lpKeyPack* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3cc8f-113">*lpKeyPack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc8f-114">Ponteiro para uma estrutura [**LSKeyPack**](lskeypack.md) que recebe o próximo pacote de chaves que corresponde aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-114">Pointer to a [**LSKeyPack**](lskeypack.md) structure that receives the next key pack that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="3cc8f-115">*pdwErrCode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3cc8f-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc8f-116">Ponteiro para uma variável que recebe um dos seguintes códigos de erro no retorno.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="3cc8f-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S com \_ êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="3cc8f-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3cc8f-118">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="3cc8f-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_ \_Não há \_ mais \_ dados** (4001)</span><span class="sxs-lookup"><span data-stu-id="3cc8f-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="3cc8f-120">Nenhum pacote de chaves corresponde aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-120">No more key packs match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="3cc8f-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ \_ \_ Erro interno E** (5001)</span><span class="sxs-lookup"><span data-stu-id="3cc8f-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="3cc8f-122">Erro interno no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="3cc8f-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ \_ \_ Sequência inválida E** (5006)</span><span class="sxs-lookup"><span data-stu-id="3cc8f-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="3cc8f-124">A sequência de chamada não era válida.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-124">The calling sequence was not valid.</span></span> <span data-ttu-id="3cc8f-125">Deve chamar a função [**TLSKeyPackEnumBegin ()**](tlskeypackenumbegin.md) antes disso.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-125">Must call the [**TLSKeyPackEnumBegin()**](tlskeypackenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="3cc8f-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ \_Servidor E \_ ocupado** (5007)</span><span class="sxs-lookup"><span data-stu-id="3cc8f-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="3cc8f-127">O servidor de licenças está muito ocupado para processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="3cc8f-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="3cc8f-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="3cc8f-129">Não é possível processar a solicitação devido à memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cc8f-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3cc8f-130">Return value</span></span>

<span data-ttu-id="3cc8f-131">Essa função retorna os seguintes valores de retorno possíveis.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="3cc8f-132">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="3cc8f-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="3cc8f-133">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-133">The call succeeded.</span></span> <span data-ttu-id="3cc8f-134">Verifique o valor do parâmetro *pdwErrCode* para obter o código de retorno para a chamada.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="3cc8f-135">**ARG. de RPC \_ \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="3cc8f-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="3cc8f-136">O argumento não era válido.</span><span class="sxs-lookup"><span data-stu-id="3cc8f-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3cc8f-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cc8f-137">Requirements</span></span>



| <span data-ttu-id="3cc8f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cc8f-138">Requirement</span></span> | <span data-ttu-id="3cc8f-139">Valor</span><span class="sxs-lookup"><span data-stu-id="3cc8f-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc8f-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cc8f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="3cc8f-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cc8f-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3cc8f-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cc8f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="3cc8f-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cc8f-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3cc8f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3cc8f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cc8f-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cc8f-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cc8f-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cc8f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc8f-147">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="3cc8f-147">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="3cc8f-148">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="3cc8f-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="3cc8f-149">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="3cc8f-149">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="3cc8f-150">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="3cc8f-150">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

