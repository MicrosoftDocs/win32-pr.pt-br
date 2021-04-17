---
description: 'Retorna o identificador de algoritmo da API de criptografia: próxima geração (CNG) do algoritmo de hash que é usado para a função pseudo aleatória (TLS) do protocolo de segurança da camada de transporte (PRF) para o protocolo de entrada, o conjunto de codificação e o tipo de chave.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Função SslGetCipherSuitePRFHashAlgorithm (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783245"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a><span data-ttu-id="7a786-103">Função SslGetCipherSuitePRFHashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7a786-103">SslGetCipherSuitePRFHashAlgorithm function</span></span>

<span data-ttu-id="7a786-104">A função **SslGetCipherSuitePRFHashAlgorithm** retorna o identificador de algoritmo CNG (Cryptography API: Next Generation) do [*algoritmo de hash*](/windows/desktop/SecGloss/h-gly) que é usado para a [*função pseudo-aleatória*](/windows/desktop/SecGloss/p-gly) do [*protocolo*](/windows/desktop/SecGloss/t-gly) TLS para o protocolo de entrada, o conjunto de codificação e o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="7a786-104">The **SslGetCipherSuitePRFHashAlgorithm** function returns the Cryptography API: Next Generation (CNG) Algorithm Identifier of the [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that is used for the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) [*pseudo-random function*](/windows/desktop/SecGloss/p-gly) (PRF) for the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a786-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a786-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7a786-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a786-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a786-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a786-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a786-108">O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="7a786-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="7a786-109">*dwProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a786-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a786-110">Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7a786-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="7a786-111">*dwCipherSuite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a786-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a786-112">Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7a786-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="7a786-113">*dwKeyType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a786-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a786-114">Um dos valores do [**identificador do tipo de chave do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7a786-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="7a786-115">Para tipos de chave que não são ECC ( [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) ), defina esse parâmetro como zero.</span><span class="sxs-lookup"><span data-stu-id="7a786-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7a786-116">*szPRFHash* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7a786-116">*szPRFHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a786-117">Um dos [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) para o hash que será usado para o TLS PRF.</span><span class="sxs-lookup"><span data-stu-id="7a786-117">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) for the hash that will be used for the TLS PRF.</span></span>

</dd> <dt>

<span data-ttu-id="7a786-118">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a786-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a786-119">Esse parâmetro é reservado para uso futuro e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="7a786-119">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a786-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a786-120">Return value</span></span>

<span data-ttu-id="7a786-121">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7a786-121">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="7a786-122">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7a786-122">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="7a786-123">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="7a786-123">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="7a786-124">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7a786-124">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="7a786-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a786-125">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a786-126"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="7a786-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="7a786-127">O parâmetro *hSslProvider* contém um ponteiro que não é válido.</span><span class="sxs-lookup"><span data-stu-id="7a786-127">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="7a786-128"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="7a786-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="7a786-129">O parâmetro *szPRFHash* está definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7a786-129">The *szPRFHash* parameter is set to **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="7a786-130"><dt>**Nte \_ 0x80090029L sem \_ suporte**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7a786-130"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="7a786-131">A função selecionada não tem suporte na versão especificada da interface.</span><span class="sxs-lookup"><span data-stu-id="7a786-131">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="7a786-132"><dt>**Nte \_ \_Sinalizadores INválidos**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="7a786-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="7a786-133">O parâmetro *dwFlags* deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="7a786-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="7a786-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a786-134">Remarks</span></span>

<span data-ttu-id="7a786-135">Essa função **SslGetCipherSuitePRFHashAlgorithm** é chamada para conversações TLS 1,2 ou posteriores para consultar o algoritmo de hash que será usado no TLS PRF.</span><span class="sxs-lookup"><span data-stu-id="7a786-135">This **SslGetCipherSuitePRFHashAlgorithm** function is called for TLS 1.2 or later conversations to query the hashing algorithm that will be used in the TLS PRF.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a786-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a786-136">Requirements</span></span>



| <span data-ttu-id="7a786-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a786-137">Requirement</span></span> | <span data-ttu-id="7a786-138">Valor</span><span class="sxs-lookup"><span data-stu-id="7a786-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a786-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a786-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7a786-140">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7a786-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7a786-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a786-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7a786-142">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="7a786-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a786-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a786-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a786-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a786-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="7a786-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7a786-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a786-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a786-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

