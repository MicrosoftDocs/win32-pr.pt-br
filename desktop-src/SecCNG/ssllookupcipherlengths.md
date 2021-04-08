---
description: Retorna uma \_ estrutura de \_ comprimentos de criptografia de SSL NCRYPT \_ que contém o cabeçalho e os comprimentos do trailer do protocolo de entrada, do conjunto de codificação e do tipo de chave.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Função SslLookupCipherLengths (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921362"
---
# <a name="ssllookupcipherlengths-function"></a><span data-ttu-id="b1dff-103">Função SslLookupCipherLengths</span><span class="sxs-lookup"><span data-stu-id="b1dff-103">SslLookupCipherLengths function</span></span>

<span data-ttu-id="b1dff-104">A função **SslLookupCipherLengths** retorna uma estrutura de [**\_ \_ \_ comprimentos de criptografia de SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) que contém o cabeçalho e os comprimentos do trailer do protocolo de entrada, do conjunto de codificação e do tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="b1dff-104">The **SslLookupCipherLengths** function returns an [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure that contains the header and trailer lengths of the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1dff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1dff-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b1dff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1dff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1dff-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1dff-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dff-108">O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="b1dff-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="b1dff-109">*dwProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1dff-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dff-110">Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b1dff-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="b1dff-111">*dwCipherSuite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1dff-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dff-112">Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b1dff-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="b1dff-113">*dwKeyType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1dff-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dff-114">Um dos valores do [**identificador do tipo de chave do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b1dff-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="b1dff-115">Para tipos de chave que não são ECC ( [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) ), defina esse parâmetro como zero.</span><span class="sxs-lookup"><span data-stu-id="b1dff-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b1dff-116">*pCipherLengths* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b1dff-116">*pCipherLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dff-117">Um ponteiro para um buffer para receber a estrutura de [**\_ \_ \_ comprimentos de criptografia de SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) .</span><span class="sxs-lookup"><span data-stu-id="b1dff-117">A pointer to a buffer to receive the [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b1dff-118">*cbCipherLengths* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1dff-118">*cbCipherLengths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dff-119">O comprimento, em bytes, do buffer apontado pelo parâmetro *pCipherLengths* .</span><span class="sxs-lookup"><span data-stu-id="b1dff-119">The length, in bytes, of the buffer pointed to by the *pCipherLengths* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b1dff-120">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1dff-120">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dff-121">Esse parâmetro é reservado para uso futuro e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="b1dff-121">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1dff-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1dff-122">Return value</span></span>

<span data-ttu-id="b1dff-123">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b1dff-123">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="b1dff-124">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b1dff-124">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="b1dff-125">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="b1dff-125">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="b1dff-126">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b1dff-126">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="b1dff-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1dff-127">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1dff-128"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="b1dff-128"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="b1dff-129">O parâmetro *hSslProvider* contém um ponteiro que não é válido.</span><span class="sxs-lookup"><span data-stu-id="b1dff-129">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="b1dff-130"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="b1dff-130"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="b1dff-131">O parâmetro *pCipherLengths* está definido como **NULL** ou o comprimento do buffer especificado pelo *cbCipherLengths* é muito curto.</span><span class="sxs-lookup"><span data-stu-id="b1dff-131">The *pCipherLengths* parameter is set to **NULL** or the buffer length specified by the *cbCipherLengths* is too short.</span></span><br/> |
| <dl> <span data-ttu-id="b1dff-132"><dt>**Nte \_ \_Sinalizadores INválidos**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="b1dff-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="b1dff-133">O parâmetro *dwFlags* deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="b1dff-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="b1dff-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1dff-134">Remarks</span></span>

<span data-ttu-id="b1dff-135">A função **SslLookupCipherLengths** é chamada para as conversas do [*protocolo*](/windows/desktop/SecGloss/t-gly) TLS 1,1 ou posterior para consultar o cabeçalho e os comprimentos do trailer para o protocolo solicitado, o conjunto de codificação e o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="b1dff-135">The **SslLookupCipherLengths** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.1 or later conversations to query the header and trailer lengths for the requested protocol, cipher suite, and key type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1dff-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1dff-136">Requirements</span></span>



| <span data-ttu-id="b1dff-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1dff-137">Requirement</span></span> | <span data-ttu-id="b1dff-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b1dff-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1dff-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1dff-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b1dff-140">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b1dff-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1dff-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1dff-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b1dff-142">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b1dff-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1dff-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1dff-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1dff-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1dff-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="b1dff-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b1dff-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1dff-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1dff-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

