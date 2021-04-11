---
description: Abre um identificador para uma chave privada.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Função SslOpenPrivateKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090198"
---
# <a name="sslopenprivatekey-function"></a><span data-ttu-id="bba37-103">Função SslOpenPrivateKey</span><span class="sxs-lookup"><span data-stu-id="bba37-103">SslOpenPrivateKey function</span></span>

<span data-ttu-id="bba37-104">A função **SslOpenPrivateKey** abre um identificador para uma [*chave privada*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="bba37-104">The **SslOpenPrivateKey** function opens a handle to a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="bba37-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bba37-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="bba37-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bba37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba37-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba37-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba37-108">O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="bba37-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="bba37-109">*phPrivateKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bba37-109">*phPrivateKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bba37-110">O endereço de um buffer no qual gravar o identificador para a chave privada.</span><span class="sxs-lookup"><span data-stu-id="bba37-110">The address of a buffer in which to write the handle to the private key.</span></span>

<span data-ttu-id="bba37-111">Quando terminar de usar a chave, você deverá liberar *phPrivateKey* chamando a função [**SslFreeObject**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="bba37-111">When you have finished using the key, you should free *phPrivateKey* by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bba37-112">*pCertContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba37-112">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba37-113">O endereço do certificado do qual obter a chave privada.</span><span class="sxs-lookup"><span data-stu-id="bba37-113">The address of the certificate from which to obtain the private key.</span></span>

</dd> <dt>

<span data-ttu-id="bba37-114">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba37-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba37-115">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bba37-115">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba37-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bba37-116">Return value</span></span>

<span data-ttu-id="bba37-117">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="bba37-117">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="bba37-118">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="bba37-118">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="bba37-119">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="bba37-119">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="bba37-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bba37-120">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="bba37-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="bba37-121">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bba37-122"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="bba37-122"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="bba37-123">Não há memória suficiente disponível para alocar os buffers necessários.</span><span class="sxs-lookup"><span data-stu-id="bba37-123">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="bba37-124"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="bba37-124"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="bba37-125">O identificador *hSslProvider* não é válido.</span><span class="sxs-lookup"><span data-stu-id="bba37-125">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="bba37-126"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="bba37-126"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="bba37-127">O parâmetro *phPrivateKey* ou *pCertContext* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bba37-127">The *phPrivateKey* or *pCertContext* parameter is **NULL**.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="bba37-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="bba37-128">Remarks</span></span>

<span data-ttu-id="bba37-129">A chave privada obtida faz parte de um [*par de chaves pública/privada*](/windows/desktop/SecGloss/p-gly) dentro de um [*certificado*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="bba37-129">The private key obtained is part of a [*public/private key pair*](/windows/desktop/SecGloss/p-gly) within a [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="bba37-130">Essa função simplesmente extrai a chave privada do certificado especificado pelo parâmetro *pCertContext* .</span><span class="sxs-lookup"><span data-stu-id="bba37-130">This function merely extracts the private key from the certificate specified by the *pCertContext* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba37-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bba37-131">Requirements</span></span>



| <span data-ttu-id="bba37-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba37-132">Requirement</span></span> | <span data-ttu-id="bba37-133">Valor</span><span class="sxs-lookup"><span data-stu-id="bba37-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba37-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bba37-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bba37-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bba37-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bba37-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bba37-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bba37-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bba37-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bba37-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bba37-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bba37-139"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="bba37-139"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="bba37-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bba37-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bba37-141"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bba37-141"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

