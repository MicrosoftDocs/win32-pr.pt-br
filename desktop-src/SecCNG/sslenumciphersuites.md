---
description: Enumera os conjuntos de codificação com suporte de um provedor de protocolo SSL (protocolo SSL Protocol).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Função SslEnumCipherSuites (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296657"
---
# <a name="sslenumciphersuites-function"></a><span data-ttu-id="29767-103">Função SslEnumCipherSuites</span><span class="sxs-lookup"><span data-stu-id="29767-103">SslEnumCipherSuites function</span></span>

<span data-ttu-id="29767-104">A função **SslEnumCipherSuites** enumera os conjuntos de codificação com suporte de um provedor de protocolo SSL ( [*protocolo SSL Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="29767-104">The **SslEnumCipherSuites** function enumerates the cipher suites supported by a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="29767-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29767-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="29767-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29767-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29767-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29767-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29767-108">O identificador da instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="29767-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="29767-109">*hPrivateKey* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="29767-109">*hPrivateKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29767-110">O identificador de uma [*chave privada*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="29767-110">The handle of a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="29767-111">Quando uma chave privada é especificada, o **SslEnumCipherSuites** enumera os conjuntos de codificação que são compatíveis com a chave privada.</span><span class="sxs-lookup"><span data-stu-id="29767-111">When a private key is specified, **SslEnumCipherSuites** enumerates the cipher suites that are compatible with the private key.</span></span> <span data-ttu-id="29767-112">Por exemplo, se a chave privada for uma chave DSS, somente os pacotes de \_ codificação DSS DHE serão retornados.</span><span class="sxs-lookup"><span data-stu-id="29767-112">For example, if the private key is a DSS key, then only the DSS\_DHE cipher suites are returned.</span></span> <span data-ttu-id="29767-113">Se a chave privada for uma chave RSA, mas não der suporte a operações de descriptografia brutas, os conjuntos de codificação SSL2 não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="29767-113">If the private key is an RSA key, but it does not support raw decryption operations, then the SSL2 cipher suites are not returned.</span></span>

<span data-ttu-id="29767-114">Defina esse parâmetro como **NULL** quando você não estiver especificando uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="29767-114">Set this parameter to **NULL** when you are not specifying a private key.</span></span>

> [!Note]  
> <span data-ttu-id="29767-115">Um identificador *hPrivateKey* é obtido chamando a função [**SslOpenPrivateKey**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="29767-115">A *hPrivateKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="29767-116">Não há suporte para identificadores obtidos da função [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) .</span><span class="sxs-lookup"><span data-stu-id="29767-116">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="29767-117">*ppCipherSuite* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="29767-117">*ppCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29767-118">Um ponteiro para uma estrutura [**NCRYPT do \_ \_ \_ pacote de criptografia SSL**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) para receber o endereço do próximo conjunto de codificação na lista.</span><span class="sxs-lookup"><span data-stu-id="29767-118">A pointer to a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure to receive the address of the next cipher suite in the list.</span></span>

</dd> <dt>

<span data-ttu-id="29767-119">*ppEnumState* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="29767-119">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="29767-120">Um ponteiro para um buffer que indica a posição atual na lista de conjuntos de codificação.</span><span class="sxs-lookup"><span data-stu-id="29767-120">A pointer to a buffer that indicates the current position in the list of cipher suites.</span></span>

<span data-ttu-id="29767-121">Defina o ponteiro como **nulo** na primeira chamada para **SslEnumCipherSuites**.</span><span class="sxs-lookup"><span data-stu-id="29767-121">Set the pointer to **NULL** on the first call to **SslEnumCipherSuites**.</span></span> <span data-ttu-id="29767-122">Em cada chamada subsequente, passe o valor não modificado de volta para **SslEnumCipherSuites**.</span><span class="sxs-lookup"><span data-stu-id="29767-122">On each subsequent call, pass the unmodified value back to **SslEnumCipherSuites**.</span></span>

<span data-ttu-id="29767-123">Quando não houver mais conjuntos de codificação disponíveis, você deverá liberar *ppEnumState* chamando a função [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="29767-123">When there are no more cipher suites available, you should free *ppEnumState* by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="29767-124">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29767-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29767-125">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="29767-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29767-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29767-126">Return value</span></span>

<span data-ttu-id="29767-127">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="29767-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="29767-128">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="29767-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="29767-129">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="29767-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="29767-130">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="29767-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="29767-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="29767-131">Description</span></span>                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="29767-132"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="29767-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>      | <span data-ttu-id="29767-133">Não há memória suficiente disponível para alocar os buffers necessários.</span><span class="sxs-lookup"><span data-stu-id="29767-133">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="29767-134"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="29767-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="29767-135">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="29767-135">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="29767-136"><dt>**Nte \_ Não há \_ mais \_ itens**</dt> <dt>0x8009002AL</dt></span><span class="sxs-lookup"><span data-stu-id="29767-136"><dt>**NTE\_NO\_MORE\_ITEMS**</dt> <dt>0x8009002AL</dt></span></span> </dl> | <span data-ttu-id="29767-137">Não há suporte para conjuntos de codificação adicionais.</span><span class="sxs-lookup"><span data-stu-id="29767-137">No additional cipher suites are supported.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="29767-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="29767-138">Remarks</span></span>

<span data-ttu-id="29767-139">Para enumerar todos os conjuntos de codificação com suporte pelo provedor SSL, chame a função **SslEnumCipherSuites** em um loop até que o **nte não seja retornado \_ \_ mais \_ itens** .</span><span class="sxs-lookup"><span data-stu-id="29767-139">To enumerate all cipher suites supported by the SSL provider, call the **SslEnumCipherSuites** function in a loop until **NTE\_NO\_MORE\_ITEMS** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="29767-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29767-140">Requirements</span></span>



| <span data-ttu-id="29767-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="29767-141">Requirement</span></span> | <span data-ttu-id="29767-142">Valor</span><span class="sxs-lookup"><span data-stu-id="29767-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29767-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29767-143">Minimum supported client</span></span><br/> | <span data-ttu-id="29767-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29767-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="29767-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29767-145">Minimum supported server</span></span><br/> | <span data-ttu-id="29767-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29767-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="29767-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29767-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="29767-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="29767-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="29767-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29767-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="29767-150"><dt>NCrypt. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29767-150"><dt>Ncrypt.lib</dt></span></span> </dl>    |
| <span data-ttu-id="29767-151">DLL</span><span class="sxs-lookup"><span data-stu-id="29767-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29767-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29767-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="29767-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="29767-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29767-154">**\_pacote de \_ codificação \_ SSL NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="29767-154">**NCRYPT\_SSL\_CIPHER\_SUITE**</span></span>](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

