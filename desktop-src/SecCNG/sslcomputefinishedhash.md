---
description: Computa o hash enviado na mensagem concluída do handshake do protocolo de protocolo SSL (SSL).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Função SslComputeFinishedHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921414"
---
# <a name="sslcomputefinishedhash-function"></a><span data-ttu-id="17bd5-103">Função SslComputeFinishedHash</span><span class="sxs-lookup"><span data-stu-id="17bd5-103">SslComputeFinishedHash function</span></span>

<span data-ttu-id="17bd5-104">A função **SslComputeFinishedHash** computa o [*hash*](/windows/desktop/SecGloss/h-gly) enviado na mensagem concluída do handshake do [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="17bd5-104">The **SslComputeFinishedHash** function computes the [*hash*](/windows/desktop/SecGloss/h-gly) sent in the finished message of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span> <span data-ttu-id="17bd5-105">Para obter mais informações sobre a sequência de handshake SSL, consulte [Descrição do handshake de protocolo SSL (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="17bd5-105">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

## <a name="syntax"></a><span data-ttu-id="17bd5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17bd5-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="17bd5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17bd5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17bd5-108">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17bd5-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17bd5-109">O identificador da instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="17bd5-109">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="17bd5-110">*hMasterKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17bd5-110">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17bd5-111">O identificador do objeto de [*chave mestra*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="17bd5-111">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="17bd5-112">*hHandshakeHash* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17bd5-112">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17bd5-113">O identificador do hash das mensagens de handshake.</span><span class="sxs-lookup"><span data-stu-id="17bd5-113">The handle of the hash of the handshake messages.</span></span>

</dd> <dt>

<span data-ttu-id="17bd5-114">*pbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="17bd5-114">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17bd5-115">Um ponteiro para um buffer que recebe o hash da mensagem de conclusão.</span><span class="sxs-lookup"><span data-stu-id="17bd5-115">A pointer to a buffer that receives the hash for the finish message.</span></span>

</dd> <dt>

<span data-ttu-id="17bd5-116">*cbOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17bd5-116">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17bd5-117">O comprimento, em bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="17bd5-117">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="17bd5-118">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17bd5-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17bd5-119">Uma das constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="17bd5-119">One of the following constants.</span></span>



| <span data-ttu-id="17bd5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="17bd5-120">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="17bd5-121">Significado</span><span class="sxs-lookup"><span data-stu-id="17bd5-121">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="17bd5-122"><dt>**NCRYPT \_ \_ \_ Sinalizador de cliente SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="17bd5-122"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="17bd5-123">Especifica que esta é uma chamada de cliente.</span><span class="sxs-lookup"><span data-stu-id="17bd5-123">Specifies that this is a client call.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="17bd5-124"><dt>**NCRYPT \_ \_ \_ Sinalizador de servidor SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="17bd5-124"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="17bd5-125">Especifica que esta é uma chamada de servidor.</span><span class="sxs-lookup"><span data-stu-id="17bd5-125">Specifies that this is a server call.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17bd5-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17bd5-126">Return value</span></span>

<span data-ttu-id="17bd5-127">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="17bd5-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="17bd5-128">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="17bd5-128">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="17bd5-129">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="17bd5-129">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="17bd5-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="17bd5-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="17bd5-131"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>2148073510 (0x80090026)</dt></span><span class="sxs-lookup"><span data-stu-id="17bd5-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>2148073510 (0x80090026)</dt></span></span> </dl> | <span data-ttu-id="17bd5-132">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="17bd5-132">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17bd5-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="17bd5-133">Remarks</span></span>

<span data-ttu-id="17bd5-134">A função **SslComputeFinishedHash** é uma das três funções usadas para gerar um hash a ser usado durante o HANDSHAKE de SSL.</span><span class="sxs-lookup"><span data-stu-id="17bd5-134">The **SslComputeFinishedHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="17bd5-135">A função [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) é chamada para obter um identificador de hash.</span><span class="sxs-lookup"><span data-stu-id="17bd5-135">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="17bd5-136">A função [**SslHashHandshake**](sslhashhandshake.md) é chamada qualquer número de vezes com o identificador de hash para adicionar dados ao hash.</span><span class="sxs-lookup"><span data-stu-id="17bd5-136">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="17bd5-137">A função **SslComputeFinishedHash** é chamada com o identificador de hash para obter o resumo dos dados com hash.</span><span class="sxs-lookup"><span data-stu-id="17bd5-137">The **SslComputeFinishedHash** function is called with the hash handle to obtain the digest of the hashed data.</span></span>

<span data-ttu-id="17bd5-138">O valor de hash é computado pelo hash do segredo mestre com um hash de todas as mensagens de handshake anteriores enviadas ou recebidas.</span><span class="sxs-lookup"><span data-stu-id="17bd5-138">The hash value is computed by hashing the master secret with a hash of all previous handshake messages sent or received.</span></span>

<span data-ttu-id="17bd5-139">O valor de *cbOutput* determina o comprimento dos dados de hash.</span><span class="sxs-lookup"><span data-stu-id="17bd5-139">The value of *cbOutput* determines the length of the hash data.</span></span> <span data-ttu-id="17bd5-140">Quando o protocolo TLS 1,0 é usado [*, ele deve*](/windows/desktop/SecGloss/t-gly) ser sempre 12 (bytes).</span><span class="sxs-lookup"><span data-stu-id="17bd5-140">When the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.0 protocol is used, this should always be 12 (bytes).</span></span> <span data-ttu-id="17bd5-141">Para obter mais informações, consulte [o protocolo TLS versão 1,0](https://www.ietf.org/rfc/rfc2246.txt).</span><span class="sxs-lookup"><span data-stu-id="17bd5-141">For more information, see [The TLS Protocol Version 1.0](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="requirements"></a><span data-ttu-id="17bd5-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17bd5-142">Requirements</span></span>



| <span data-ttu-id="17bd5-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="17bd5-143">Requirement</span></span> | <span data-ttu-id="17bd5-144">Valor</span><span class="sxs-lookup"><span data-stu-id="17bd5-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="17bd5-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17bd5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="17bd5-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17bd5-146">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="17bd5-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17bd5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="17bd5-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17bd5-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="17bd5-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17bd5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="17bd5-150"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="17bd5-150"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="17bd5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="17bd5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17bd5-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17bd5-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

