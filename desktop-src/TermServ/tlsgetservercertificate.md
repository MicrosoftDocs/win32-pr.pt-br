---
title: Função TLSGetServerCertificate
description: Retorna o certificado do servidor de licença Área de Trabalho Remota.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Função TLSGetServerCertificate Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755152"
---
# <a name="tlsgetservercertificate-function"></a><span data-ttu-id="6dcca-104">Função TLSGetServerCertificate</span><span class="sxs-lookup"><span data-stu-id="6dcca-104">TLSGetServerCertificate function</span></span>

<span data-ttu-id="6dcca-105">Retorna o certificado do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="6dcca-105">Returns the certificate of the Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="6dcca-106">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="6dcca-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="6dcca-107">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="6dcca-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6dcca-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6dcca-108">Syntax</span></span>


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="6dcca-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dcca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dcca-110">*hHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6dcca-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dcca-111">Identificador para um Área de Trabalho Remota servidor de licença que é aberto por uma chamada para a função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="6dcca-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="6dcca-112">*bSignCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6dcca-112">*bSignCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dcca-113">**Verdadeiro** se o certificado de assinatura, **falso** , se o certificado do Exchange.</span><span class="sxs-lookup"><span data-stu-id="6dcca-113">**TRUE** if signature certificate, **FALSE** if exchange certificate.</span></span>

</dd> <dt>

<span data-ttu-id="6dcca-114">*ppbCertBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6dcca-114">*ppbCertBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dcca-115">Ponteiro para uma variável que recebe um ponteiro para um buffer que contém o certificado.</span><span class="sxs-lookup"><span data-stu-id="6dcca-115">Pointer to a variable that receives a pointer to a buffer that contains the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="6dcca-116">*lpdwCertBlobLen* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6dcca-116">*lpdwCertBlobLen* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dcca-117">Ponteiro para uma variável que recebe o tamanho do certificado retornado.</span><span class="sxs-lookup"><span data-stu-id="6dcca-117">Pointer to a variable that receives the size of the certificate that is returned.</span></span>

</dd> <dt>

<span data-ttu-id="6dcca-118">*pdwErrCode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6dcca-118">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dcca-119">Ponteiro para uma variável que recebe o código de erro.</span><span class="sxs-lookup"><span data-stu-id="6dcca-119">Pointer to a variable that receives the error code.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="6dcca-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S com \_ êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="6dcca-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6dcca-121">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6dcca-121">Call is successful.</span></span>

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span data-ttu-id="6dcca-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_ \_ \_ Certificado W SELFSIGN** (4007)</span><span class="sxs-lookup"><span data-stu-id="6dcca-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS\_W\_SELFSIGN\_CERTIFICATE** (4007)</span></span>


</dt> <dd>

<span data-ttu-id="6dcca-123">O certificado retornado é um certificado autoassinado.</span><span class="sxs-lookup"><span data-stu-id="6dcca-123">Certificate returned is a self-signed certificate.</span></span>

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span data-ttu-id="6dcca-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_ \_Certificado de \_ SELFSIGN \_ temporário W** (4009)</span><span class="sxs-lookup"><span data-stu-id="6dcca-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS\_W\_TEMP\_SELFSIGN\_CERT** (4009)</span></span>


</dt> <dd>

<span data-ttu-id="6dcca-125">O certificado retornado é temporário.</span><span class="sxs-lookup"><span data-stu-id="6dcca-125">Certificate returned is temporary.</span></span>

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span data-ttu-id="6dcca-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_ E \_ acesso \_ negado** (5003)</span><span class="sxs-lookup"><span data-stu-id="6dcca-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS\_E\_ACCESS\_DENIED** (5003)</span></span>


</dt> <dd>

<span data-ttu-id="6dcca-127">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="6dcca-127">Access denied.</span></span>

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span data-ttu-id="6dcca-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_ \_ \_ Identificador E alocado** (5007)</span><span class="sxs-lookup"><span data-stu-id="6dcca-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS\_E\_ALLOCATE\_HANDLE** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="6dcca-129">O servidor está muito ocupado para processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6dcca-129">Server is too busy to process the request.</span></span>

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span data-ttu-id="6dcca-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_ E \_ nenhum \_ certificado** (5022)</span><span class="sxs-lookup"><span data-stu-id="6dcca-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS\_E\_NO\_CERTIFICATE** (5022)</span></span>


</dt> <dd>

<span data-ttu-id="6dcca-131">Não é possível recuperar um certificado.</span><span class="sxs-lookup"><span data-stu-id="6dcca-131">Cannot retrieve a certificate.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dcca-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6dcca-132">Return value</span></span>

<span data-ttu-id="6dcca-133">Essa função retorna os seguintes valores de retorno possíveis.</span><span class="sxs-lookup"><span data-stu-id="6dcca-133">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="6dcca-134">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="6dcca-134">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="6dcca-135">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6dcca-135">The call succeeded.</span></span> <span data-ttu-id="6dcca-136">Verifique o valor do parâmetro *pdwErrCode* para obter o código de retorno para a chamada.</span><span class="sxs-lookup"><span data-stu-id="6dcca-136">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="6dcca-137">**ARG. de RPC \_ \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="6dcca-137">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="6dcca-138">O argumento era inválido.</span><span class="sxs-lookup"><span data-stu-id="6dcca-138">The argument was invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dcca-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dcca-139">Requirements</span></span>



| <span data-ttu-id="6dcca-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dcca-140">Requirement</span></span> | <span data-ttu-id="6dcca-141">Valor</span><span class="sxs-lookup"><span data-stu-id="6dcca-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dcca-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dcca-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6dcca-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dcca-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6dcca-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dcca-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6dcca-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6dcca-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6dcca-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6dcca-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dcca-147"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dcca-147"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dcca-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dcca-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dcca-149">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="6dcca-149">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

