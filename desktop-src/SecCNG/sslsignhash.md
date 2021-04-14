---
description: Assina um hash usando a chave privada especificada.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Função SslSignHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461036"
---
# <a name="sslsignhash-function"></a><span data-ttu-id="fd2f7-103">Função SslSignHash</span><span class="sxs-lookup"><span data-stu-id="fd2f7-103">SslSignHash function</span></span>

<span data-ttu-id="fd2f7-104">A função **SslSignHash** assina um [*hash*](/windows/desktop/SecGloss/h-gly) usando a [*chave privada*](/windows/desktop/SecGloss/p-gly)especificada.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-104">The **SslSignHash** function signs a [*hash*](/windows/desktop/SecGloss/h-gly) by using the specified [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="fd2f7-105">O processo de assinatura é executado no servidor.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-105">The signing process is performed on the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2f7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd2f7-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fd2f7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd2f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd2f7-108">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2f7-109">O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="fd2f7-109">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="fd2f7-110">*hPrivateKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-110">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2f7-111">O identificador para a chave privada a ser usada para assinar o hash.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-111">The handle to the private key to use to sign the hash.</span></span>

</dd> <dt>

<span data-ttu-id="fd2f7-112">*pbHashValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-112">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2f7-113">Um ponteiro para um buffer que contém o hash a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-113">A pointer to a buffer that contains the hash to sign.</span></span>

</dd> <dt>

<span data-ttu-id="fd2f7-114">*cbHashValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-114">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2f7-115">O tamanho, em bytes, do buffer *pbHashValue* .</span><span class="sxs-lookup"><span data-stu-id="fd2f7-115">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fd2f7-116">*pbSignature* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-116">*pbSignature* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2f7-117">O endereço de um buffer que recebe a assinatura do hash.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-117">The address of a buffer that receives the signature of the hash.</span></span> <span data-ttu-id="fd2f7-118">O parâmetro *cbSignature* contém o tamanho desse buffer.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-118">The *cbSignature* parameter contains the size of this buffer.</span></span> <span data-ttu-id="fd2f7-119">Para determinar o tamanho de dimensionamento necessário do buffer, defina o parâmetro *pbSignature* como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-119">To determine the required sized size of the buffer, set the *pbSignature* parameter to **NULL**.</span></span> <span data-ttu-id="fd2f7-120">O tamanho necessário do buffer será retornado no parâmetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="fd2f7-120">The required size of the buffer will be returned in the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fd2f7-121">*cbSignature* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-121">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2f7-122">O tamanho, em bytes, do buffer *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="fd2f7-122">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fd2f7-123">*pcbResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-123">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2f7-124">Um ponteiro para um valor que, após a conclusão, contém o número real de bytes gravados no buffer *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="fd2f7-124">A pointer to a value that, upon completion, contains the actual number of bytes written to the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fd2f7-125">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2f7-126">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd2f7-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd2f7-127">Return value</span></span>

<span data-ttu-id="fd2f7-128">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="fd2f7-129">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="fd2f7-130">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="fd2f7-131">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fd2f7-131">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="fd2f7-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd2f7-132">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="fd2f7-133"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="fd2f7-133"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="fd2f7-134">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-134">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fd2f7-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd2f7-135">Requirements</span></span>



| <span data-ttu-id="fd2f7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd2f7-136">Requirement</span></span> | <span data-ttu-id="fd2f7-137">Valor</span><span class="sxs-lookup"><span data-stu-id="fd2f7-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2f7-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd2f7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fd2f7-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fd2f7-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd2f7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fd2f7-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd2f7-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fd2f7-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd2f7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd2f7-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd2f7-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="fd2f7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fd2f7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd2f7-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd2f7-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

