---
description: Recupera as informações do pacote de codificação para um protocolo especificado, um conjunto de codificação e um conjunto de tipos de chave.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Função SslLookupCipherSuiteInfo (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837388"
---
# <a name="ssllookupciphersuiteinfo-function"></a><span data-ttu-id="5e3a9-103">Função SslLookupCipherSuiteInfo</span><span class="sxs-lookup"><span data-stu-id="5e3a9-103">SslLookupCipherSuiteInfo function</span></span>

<span data-ttu-id="5e3a9-104">A função **SslLookupCipherSuiteInfo** recupera as informações do pacote de codificação para um protocolo especificado, o conjunto de codificação e o conjunto de tipos de chave.</span><span class="sxs-lookup"><span data-stu-id="5e3a9-104">The **SslLookupCipherSuiteInfo** function retrieves the cipher suite information for a specified protocol, cipher suite, and key type set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e3a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e3a9-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5e3a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e3a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e3a9-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e3a9-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3a9-108">O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="5e3a9-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="5e3a9-109">*dwProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e3a9-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3a9-110">Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e3a9-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5e3a9-111">*dwCipherSuite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e3a9-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3a9-112">Um dos valores dos [**identificadores do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e3a9-112">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5e3a9-113">*dwKeyType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e3a9-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3a9-114">Um dos valores dos [**identificadores de tipo de chave do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e3a9-114">One of the [**CNG SSL Provider Key Type Identifiers**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5e3a9-115">*pCipherSuite* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5e3a9-115">*pCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3a9-116">O endereço de um buffer que contém uma estrutura de [**\_ pacote de \_ criptografia \_ de SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) na qual gravar as informações do pacote de codificação.</span><span class="sxs-lookup"><span data-stu-id="5e3a9-116">The address of a buffer that contains a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure in which to write the cipher suite information.</span></span>

</dd> <dt>

<span data-ttu-id="5e3a9-117">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e3a9-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3a9-118">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5e3a9-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e3a9-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e3a9-119">Return value</span></span>

<span data-ttu-id="5e3a9-120">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="5e3a9-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5e3a9-121">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="5e3a9-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5e3a9-122">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="5e3a9-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5e3a9-123">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5e3a9-123">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="5e3a9-124">Description</span><span class="sxs-lookup"><span data-stu-id="5e3a9-124">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="5e3a9-125"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="5e3a9-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="5e3a9-126">O identificador *hSslProvider* não é válido.</span><span class="sxs-lookup"><span data-stu-id="5e3a9-126">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5e3a9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e3a9-127">Requirements</span></span>



| <span data-ttu-id="5e3a9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e3a9-128">Requirement</span></span> | <span data-ttu-id="5e3a9-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5e3a9-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3a9-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e3a9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3a9-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e3a9-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5e3a9-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e3a9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3a9-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e3a9-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e3a9-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e3a9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e3a9-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e3a9-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5e3a9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5e3a9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e3a9-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e3a9-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

