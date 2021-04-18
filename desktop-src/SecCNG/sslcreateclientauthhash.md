---
description: Recupera um identificador para o hash de handshake que é usado para autenticação de cliente.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Função SslCreateClientAuthHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778696"
---
# <a name="sslcreateclientauthhash-function"></a><span data-ttu-id="43faf-103">Função SslCreateClientAuthHash</span><span class="sxs-lookup"><span data-stu-id="43faf-103">SslCreateClientAuthHash function</span></span>

<span data-ttu-id="43faf-104">A função **SslCreateClientAuthHash** recupera um identificador para o [*hash*](/windows/desktop/SecGloss/h-gly) de handshake que é usado para autenticação de cliente.</span><span class="sxs-lookup"><span data-stu-id="43faf-104">The **SslCreateClientAuthHash** function retrieves a handle to the handshake [*hash*](/windows/desktop/SecGloss/h-gly) that is used for client authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="43faf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43faf-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="43faf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43faf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43faf-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43faf-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43faf-108">O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="43faf-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="43faf-109">*phHandshakeHash* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43faf-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43faf-110">Um ponteiro para uma variável de **\_ \_ identificador de hash NCRYPT** para receber o identificador de hash.</span><span class="sxs-lookup"><span data-stu-id="43faf-110">A pointer to an **NCRYPT\_HASH\_HANDLE** variable to receive the hash handle.</span></span>

</dd> <dt>

<span data-ttu-id="43faf-111">*dwProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43faf-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43faf-112">Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="43faf-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="43faf-113">*dwCipherSuite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43faf-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43faf-114">Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="43faf-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="43faf-115">*pszHashAlgId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43faf-115">*pszHashAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43faf-116">Um dos valores de [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="43faf-116">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) values.</span></span>

</dd> <dt>

<span data-ttu-id="43faf-117">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43faf-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43faf-118">Esse parâmetro é reservado para uso futuro e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="43faf-118">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43faf-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43faf-119">Return value</span></span>

<span data-ttu-id="43faf-120">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="43faf-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="43faf-121">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="43faf-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="43faf-122">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="43faf-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="43faf-123">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="43faf-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="43faf-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="43faf-124">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43faf-125"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="43faf-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="43faf-126">O parâmetro *hSslProvider* contém um ponteiro que não é válido.</span><span class="sxs-lookup"><span data-stu-id="43faf-126">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="43faf-127"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="43faf-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="43faf-128">O parâmetro *phHandshakeHash* está definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="43faf-128">The *phHandshakeHash* parameter is set to **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="43faf-129"><dt>**Nte \_ 0x80090029L sem \_ suporte**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="43faf-129"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="43faf-130">A função selecionada não tem suporte na versão especificada da interface.</span><span class="sxs-lookup"><span data-stu-id="43faf-130">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="43faf-131"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="43faf-131"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="43faf-132">Memória insuficiente para alocar buffers.</span><span class="sxs-lookup"><span data-stu-id="43faf-132">Insufficient memory to allocate buffers.</span></span><br/>                                          |
| <dl> <span data-ttu-id="43faf-133"><dt>**Nte \_ \_Sinalizadores INválidos**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="43faf-133"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="43faf-134">O parâmetro *dwFlags* deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="43faf-134">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="43faf-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="43faf-135">Remarks</span></span>

<span data-ttu-id="43faf-136">A função **SslCreateClientAuthHash** é chamada para o [*protocolo*](/windows/desktop/SecGloss/t-gly) TLS 1,2 ou conversas posteriores para criar objetos hash que são usados para mensagens de handshake de hash.</span><span class="sxs-lookup"><span data-stu-id="43faf-136">The **SslCreateClientAuthHash** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.2 or later conversations to create hash objects that are used to hash handshake messages.</span></span> <span data-ttu-id="43faf-137">Ele é chamado uma vez para cada [*algoritmo de hash*](/windows/desktop/SecGloss/h-gly) possível que pode ser usado na assinatura de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="43faf-137">It is called once for each possible [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that can be used in the client authentication signature.</span></span>

## <a name="requirements"></a><span data-ttu-id="43faf-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43faf-138">Requirements</span></span>



| <span data-ttu-id="43faf-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="43faf-139">Requirement</span></span> | <span data-ttu-id="43faf-140">Valor</span><span class="sxs-lookup"><span data-stu-id="43faf-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43faf-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43faf-141">Minimum supported client</span></span><br/> | <span data-ttu-id="43faf-142">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="43faf-142">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="43faf-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43faf-143">Minimum supported server</span></span><br/> | <span data-ttu-id="43faf-144">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="43faf-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43faf-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43faf-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="43faf-146"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="43faf-146"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="43faf-147">DLL</span><span class="sxs-lookup"><span data-stu-id="43faf-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43faf-148"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43faf-148"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

