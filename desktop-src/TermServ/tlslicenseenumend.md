---
title: Função TLSLicenseEnumEnd
description: Continua de uma chamada anterior para a função TLSLicenseEnumBegin e encerra a enumeração.
ms.assetid: b9cba03c-0f5a-41e8-ae13-bcdd0ac6dd99
ms.tgt_platform: multiple
keywords:
- Função TLSLicenseEnumEnd Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSLicenseEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bbd494ec539ee78008fa3df274282da1e9db6c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787575"
---
# <a name="tlslicenseenumend-function"></a><span data-ttu-id="2b8b0-104">Função TLSLicenseEnumEnd</span><span class="sxs-lookup"><span data-stu-id="2b8b0-104">TLSLicenseEnumEnd function</span></span>

<span data-ttu-id="2b8b0-105">Continua de uma chamada anterior para a função [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e encerra a enumeração.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="2b8b0-106">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="2b8b0-107">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2b8b0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b8b0-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="2b8b0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b8b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b8b0-110">*hHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b8b0-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b8b0-111">Identificador para um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="2b8b0-112">Especifique um identificador que é aberto pela função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="2b8b0-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2b8b0-113">*pdwErrCode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b8b0-113">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b8b0-114">Ponteiro para uma variável que recebe um dos seguintes códigos de erro no retorno.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-114">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="2b8b0-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S com \_ êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="2b8b0-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2b8b0-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-116">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span data-ttu-id="2b8b0-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_ \_ \_ Identificador inválido E** (5005)</span><span class="sxs-lookup"><span data-stu-id="2b8b0-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER\_E\_INVALID\_HANDLE** (5005)</span></span>


</dt> <dd>

<span data-ttu-id="2b8b0-118">O identificador não é válido.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-118">The handle is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b8b0-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b8b0-119">Return value</span></span>

<span data-ttu-id="2b8b0-120">Essa função retorna os seguintes valores de retorno possíveis.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-120">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="2b8b0-121">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="2b8b0-121">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="2b8b0-122">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-122">The call succeeded.</span></span> <span data-ttu-id="2b8b0-123">Verifique o valor do parâmetro *pdwErrCode* para obter o código de retorno para a chamada.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-123">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="2b8b0-124">**ARG. de RPC \_ \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="2b8b0-124">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="2b8b0-125">O argumento não era válido.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-125">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b8b0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b8b0-126">Requirements</span></span>



| <span data-ttu-id="2b8b0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b8b0-127">Requirement</span></span> | <span data-ttu-id="2b8b0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2b8b0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8b0-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b8b0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8b0-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b8b0-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b8b0-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b8b0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8b0-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b8b0-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b8b0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2b8b0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b8b0-134"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b8b0-134"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b8b0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b8b0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8b0-136">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="2b8b0-136">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="2b8b0-137">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="2b8b0-137">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="2b8b0-138">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="2b8b0-138">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="2b8b0-139">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="2b8b0-139">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> </dl>

 

