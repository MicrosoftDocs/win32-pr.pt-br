---
description: Computa um hash a ser usado durante a autenticação do certificado.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Função SslComputeClientAuthHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165432"
---
# <a name="sslcomputeclientauthhash-function"></a><span data-ttu-id="35b1f-103">Função SslComputeClientAuthHash</span><span class="sxs-lookup"><span data-stu-id="35b1f-103">SslComputeClientAuthHash function</span></span>

<span data-ttu-id="35b1f-104">A função **SslComputeClientAuthHash** computa um [*hash*](/windows/desktop/SecGloss/h-gly) a ser usado durante a autenticação do [*certificado*](/windows/desktop/SecGloss/c-gly) .</span><span class="sxs-lookup"><span data-stu-id="35b1f-104">The **SslComputeClientAuthHash** function computes a [*hash*](/windows/desktop/SecGloss/h-gly) to use during [*certificate*](/windows/desktop/SecGloss/c-gly) authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="35b1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35b1f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="35b1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35b1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b1f-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35b1f-108">O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="35b1f-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="35b1f-109">*hMasterKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35b1f-110">O identificador do objeto de [*chave mestra*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="35b1f-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="35b1f-111">*hHandshakeHash* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-111">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35b1f-112">O identificador do hash do handshake calculado até o momento.</span><span class="sxs-lookup"><span data-stu-id="35b1f-112">The handle of the hash of the handshake computed so far.</span></span>

</dd> <dt>

<span data-ttu-id="35b1f-113">*pszAlgId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-113">*pszAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35b1f-114">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que identifica o [*algoritmo criptográfico*](/windows/desktop/SecGloss/c-gly)solicitado.</span><span class="sxs-lookup"><span data-stu-id="35b1f-114">A pointer to a null-terminated Unicode string that identifies the requested [*cryptographic algorithm*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="35b1f-115">Pode ser um dos [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) padrão ou o identificador para outro algoritmo registrado.</span><span class="sxs-lookup"><span data-stu-id="35b1f-115">This can be one of the standard [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or the identifier for another registered algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="35b1f-116">*pbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-116">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35b1f-117">O endereço de um buffer que recebe o [*blob de chave*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="35b1f-117">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="35b1f-118">O parâmetro *cbOutput* contém o tamanho desse buffer.</span><span class="sxs-lookup"><span data-stu-id="35b1f-118">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="35b1f-119">Se esse parâmetro for **NULL**, essa função coloca o tamanho necessário, em bytes, no **DWORD** apontado pelo parâmetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="35b1f-119">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="35b1f-120">*cbOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-120">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35b1f-121">O comprimento, em bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="35b1f-121">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="35b1f-122">*pcbResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-122">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35b1f-123">Um ponteiro para um valor **DWORD** que especifica o comprimento, em bytes, do hash gravado no buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="35b1f-123">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="35b1f-124">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35b1f-125">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="35b1f-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b1f-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35b1f-126">Return value</span></span>

<span data-ttu-id="35b1f-127">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="35b1f-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="35b1f-128">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="35b1f-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="35b1f-129">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="35b1f-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="35b1f-130">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="35b1f-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="35b1f-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="35b1f-131">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="35b1f-132"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="35b1f-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="35b1f-133">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="35b1f-133">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="35b1f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="35b1f-134">Remarks</span></span>

<span data-ttu-id="35b1f-135">A função **SslComputeClientAuthHash** computa o hash que é enviado na mensagem de verificação de certificado do handshake SSL.</span><span class="sxs-lookup"><span data-stu-id="35b1f-135">The **SslComputeClientAuthHash** function computes the hash that is sent in the certificate verification message of the SSL handshake.</span></span> <span data-ttu-id="35b1f-136">O valor de hash é calculado com a criação de um hash que contém o segredo mestre com um hash de todas as mensagens de handshake anteriores enviadas ou recebidas.</span><span class="sxs-lookup"><span data-stu-id="35b1f-136">The hash value is computed by creating a hash that contains the master secret with a hash of all previous handshake messages sent or received.</span></span> <span data-ttu-id="35b1f-137">Para obter mais informações sobre a sequência de handshake SSL, consulte [Descrição do handshake de protocolo SSL (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="35b1f-137">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

<span data-ttu-id="35b1f-138">A maneira como o hash é calculado depende do protocolo e do conjunto de codificação usado.</span><span class="sxs-lookup"><span data-stu-id="35b1f-138">The manner in which the hash is computed depends on the protocol and cipher suite used.</span></span> <span data-ttu-id="35b1f-139">Além disso, o hash depende do tipo de chave de autenticação de cliente usada; o parâmetro *pszAlgId* indica o tipo de chave usada para autenticação de cliente.</span><span class="sxs-lookup"><span data-stu-id="35b1f-139">In addition, the hash depends on the type of client authentication key used; the *pszAlgId* parameter indicates the type of key used for client authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="35b1f-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35b1f-140">Requirements</span></span>



| <span data-ttu-id="35b1f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="35b1f-141">Requirement</span></span> | <span data-ttu-id="35b1f-142">Valor</span><span class="sxs-lookup"><span data-stu-id="35b1f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b1f-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35b1f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="35b1f-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="35b1f-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35b1f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="35b1f-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35b1f-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="35b1f-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35b1f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="35b1f-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b1f-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="35b1f-149">DLL</span><span class="sxs-lookup"><span data-stu-id="35b1f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35b1f-150"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35b1f-150"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

