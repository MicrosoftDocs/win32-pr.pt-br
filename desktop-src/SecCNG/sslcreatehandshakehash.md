---
description: Obtém um identificador de hash que é usado para mensagens de handshake de hash.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Função SslCreateHandshakeHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770354"
---
# <a name="sslcreatehandshakehash-function"></a><span data-ttu-id="3bfc1-103">Função SslCreateHandshakeHash</span><span class="sxs-lookup"><span data-stu-id="3bfc1-103">SslCreateHandshakeHash function</span></span>

<span data-ttu-id="3bfc1-104">A função **SslCreateHandshakeHash** Obtém um identificador de hash que é usado para mensagens de handshake de hash.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-104">The **SslCreateHandshakeHash** function obtains a hash handle that is used to hash handshake messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bfc1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bfc1-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3bfc1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bfc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bfc1-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bfc1-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfc1-108">O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="3bfc1-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3bfc1-109">*phHandshakeHash* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3bfc1-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfc1-110">Um identificador de hash que pode ser passado para outras funções de provedor de SSL.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-110">A hash handle that can be passed to other SSL provider functions.</span></span>

</dd> <dt>

<span data-ttu-id="3bfc1-111">*dwProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bfc1-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfc1-112">Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="3bfc1-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

> [!Note]  
> <span data-ttu-id="3bfc1-113">Essa função não é usada com o protocolo SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-113">This function is not used with the SSL 2.0 protocol.</span></span>

 

</dd> <dt>

<span data-ttu-id="3bfc1-114">*dwCipherSuite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bfc1-114">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfc1-115">Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="3bfc1-115">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="3bfc1-116">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bfc1-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bfc1-117">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-117">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bfc1-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bfc1-118">Return value</span></span>

<span data-ttu-id="3bfc1-119">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-119">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3bfc1-120">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-120">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="3bfc1-121">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-121">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3bfc1-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3bfc1-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="3bfc1-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="3bfc1-123">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="3bfc1-124"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="3bfc1-124"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="3bfc1-125">Memória insuficiente para alocar o buffer de hash.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-125">There is insufficient memory to allocate the hash buffer.</span></span><br/> |
| <dl> <span data-ttu-id="3bfc1-126"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="3bfc1-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="3bfc1-127">O identificador *hSslProvider* não é válido.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-127">The *hSslProvider* handle is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="3bfc1-128"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="3bfc1-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="3bfc1-129">O *phHandshakeHash* é nulo.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-129">The *phHandshakeHash* is null.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="3bfc1-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bfc1-130">Remarks</span></span>

<span data-ttu-id="3bfc1-131">A função **SslCreateHandshakeHash** é uma das três funções usadas para gerar um hash a ser usado durante o HANDSHAKE de SSL.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-131">The **SslCreateHandshakeHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="3bfc1-132">A função **SslCreateHandshakeHash** é chamada para obter um identificador de hash.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-132">The **SslCreateHandshakeHash** function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="3bfc1-133">A função [**SslHashHandshake**](sslhashhandshake.md) é chamada qualquer número de vezes com o identificador de hash para adicionar dados ao hash.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-133">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="3bfc1-134">A função [**SslComputeFinishedHash**](sslcomputefinishedhash.md) é chamada com o identificador de hash para obter o resumo dos dados com hash.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-134">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bfc1-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bfc1-135">Requirements</span></span>



| <span data-ttu-id="3bfc1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bfc1-136">Requirement</span></span> | <span data-ttu-id="3bfc1-137">Valor</span><span class="sxs-lookup"><span data-stu-id="3bfc1-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bfc1-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bfc1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3bfc1-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3bfc1-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3bfc1-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bfc1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3bfc1-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3bfc1-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3bfc1-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bfc1-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bfc1-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bfc1-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3bfc1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3bfc1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bfc1-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bfc1-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

