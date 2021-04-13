---
description: Computa a chave de segredo mestre do protocolo de protocolo SSL (SSL).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Função SslGenerateMasterKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370794"
---
# <a name="sslgeneratemasterkey-function"></a><span data-ttu-id="63f1c-103">Função SslGenerateMasterKey</span><span class="sxs-lookup"><span data-stu-id="63f1c-103">SslGenerateMasterKey function</span></span>

<span data-ttu-id="63f1c-104">A função **SslGenerateMasterKey** computa a chave de segredo mestre do protocolo SSL ( [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="63f1c-104">The **SslGenerateMasterKey** function computes the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) master secret key.</span></span>

## <a name="syntax"></a><span data-ttu-id="63f1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63f1c-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="63f1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63f1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63f1c-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-108">O identificador para a instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="63f1c-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="63f1c-109">*hPrivateKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-110">O identificador para a [*chave privada*](/windows/desktop/SecGloss/p-gly) usada na troca.</span><span class="sxs-lookup"><span data-stu-id="63f1c-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="63f1c-111">*hPublicKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-111">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-112">O identificador para a [*chave pública*](/windows/desktop/SecGloss/p-gly) usada na troca.</span><span class="sxs-lookup"><span data-stu-id="63f1c-112">The handle to the [*public key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="63f1c-113">*phMasterKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-113">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-114">Um ponteiro para o identificador para a [*chave mestra*](/windows/desktop/SecGloss/m-gly)gerada.</span><span class="sxs-lookup"><span data-stu-id="63f1c-114">A pointer to the handle to the generated [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="63f1c-115">*dwProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-115">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-116">Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="63f1c-116">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="63f1c-117">*dwCipherSuite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-117">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-118">Um dos valores do [**identificador do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="63f1c-118">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="63f1c-119">*pParameterList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-119">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-120">Um ponteiro para uma matriz de buffers [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contém informações usadas como parte da operação de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="63f1c-120">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="63f1c-121">O conjunto preciso de buffers depende do protocolo e do pacote de codificação usado.</span><span class="sxs-lookup"><span data-stu-id="63f1c-121">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="63f1c-122">No mínimo, a lista conterá buffers que contêm os valores aleatórios de cliente e servidor fornecidos.</span><span class="sxs-lookup"><span data-stu-id="63f1c-122">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="63f1c-123">*pbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-123">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-124">O endereço de um buffer que recebe o segredo mestre criptografado com a chave pública do servidor.</span><span class="sxs-lookup"><span data-stu-id="63f1c-124">The address of a buffer that receives the premaster secret encrypted with the public key of the server.</span></span> <span data-ttu-id="63f1c-125">O parâmetro *cbOutput* contém o tamanho desse buffer.</span><span class="sxs-lookup"><span data-stu-id="63f1c-125">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="63f1c-126">Se esse parâmetro for **NULL**, essa função retornará o tamanho necessário, em bytes, no **DWORD** apontado pelo parâmetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="63f1c-126">If this parameter is **NULL**, this function returns the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="63f1c-127">Esse buffer é usado ao executar uma troca de chaves RSA.</span><span class="sxs-lookup"><span data-stu-id="63f1c-127">This buffer is used when performing a RSA key exchange.</span></span>

 

</dd> <dt>

<span data-ttu-id="63f1c-128">*cbOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-128">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-129">O tamanho, em bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="63f1c-129">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="63f1c-130">*pcbResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-130">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-131">Um ponteiro para um valor **DWORD** no qual posicionar o número de bytes gravados no buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="63f1c-131">A pointer to a **DWORD** value in which to place number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="63f1c-132">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f1c-133">Especifica se essa função está sendo usada para troca de chaves do lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="63f1c-133">Specifies whether this function is being used for client-side or server-side key exchange.</span></span>



| <span data-ttu-id="63f1c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="63f1c-134">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="63f1c-135">Significado</span><span class="sxs-lookup"><span data-stu-id="63f1c-135">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="63f1c-136"><dt>**NCRYPT \_ \_ \_ Sinalizador de cliente SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="63f1c-136"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="63f1c-137">Especifica uma troca de chaves do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="63f1c-137">Specifies a client-side key exchange.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="63f1c-138"><dt>**NCRYPT \_ \_ \_ Sinalizador de servidor SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="63f1c-138"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="63f1c-139">Especifica uma troca de chaves do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="63f1c-139">Specifies a server-side key exchange.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63f1c-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63f1c-140">Return value</span></span>

<span data-ttu-id="63f1c-141">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="63f1c-141">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="63f1c-142">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="63f1c-142">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="63f1c-143">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="63f1c-143">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="63f1c-144">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="63f1c-144">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="63f1c-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="63f1c-145">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63f1c-146"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="63f1c-146"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="63f1c-147">Não há memória suficiente disponível para alocar os buffers necessários.</span><span class="sxs-lookup"><span data-stu-id="63f1c-147">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="63f1c-148"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="63f1c-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="63f1c-149">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="63f1c-149">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="63f1c-150"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="63f1c-150"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="63f1c-151">O parâmetro *phMasterKey* ou *hPublicKey* não é válido.</span><span class="sxs-lookup"><span data-stu-id="63f1c-151">The *phMasterKey* or *hPublicKey* parameter is not valid.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="63f1c-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63f1c-152">Requirements</span></span>



| <span data-ttu-id="63f1c-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="63f1c-153">Requirement</span></span> | <span data-ttu-id="63f1c-154">Valor</span><span class="sxs-lookup"><span data-stu-id="63f1c-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63f1c-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63f1c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="63f1c-156">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-156">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="63f1c-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63f1c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="63f1c-158">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63f1c-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63f1c-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63f1c-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="63f1c-160"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="63f1c-160"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="63f1c-161">DLL</span><span class="sxs-lookup"><span data-stu-id="63f1c-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63f1c-162"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63f1c-162"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

