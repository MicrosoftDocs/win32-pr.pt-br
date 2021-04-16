---
description: Executa uma operação de troca de chaves do protocolo SSL (protocolo SSL do servidor).
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Função SslImportMasterKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750500"
---
# <a name="sslimportmasterkey-function"></a><span data-ttu-id="ace40-103">Função SslImportMasterKey</span><span class="sxs-lookup"><span data-stu-id="ace40-103">SslImportMasterKey function</span></span>

<span data-ttu-id="ace40-104">A função **SslImportMasterKey** executa uma operação de troca de chaves de protocolo SSL ( [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) do servidor).</span><span class="sxs-lookup"><span data-stu-id="ace40-104">The **SslImportMasterKey** function performs a server-side [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) key exchange operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace40-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ace40-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ace40-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ace40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace40-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace40-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace40-108">O identificador para a instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="ace40-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ace40-109">*hPrivateKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace40-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace40-110">O identificador para a [*chave privada*](/windows/desktop/SecGloss/p-gly) usada na troca.</span><span class="sxs-lookup"><span data-stu-id="ace40-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="ace40-111">*phMasterKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ace40-111">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ace40-112">Um ponteiro para o identificador para receber a [*chave mestra*](/windows/desktop/SecGloss/m-gly).</span><span class="sxs-lookup"><span data-stu-id="ace40-112">A pointer to the handle to receive the [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="ace40-113">*dwProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace40-113">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace40-114">Um dos valores do [**identificador do protocolo do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="ace40-114">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="ace40-115">*dwCipherSuite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace40-115">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace40-116">Um dos valores dos [**identificadores do pacote de codificação do provedor de SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="ace40-116">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="ace40-117">*pParameterList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace40-117">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace40-118">Um ponteiro para uma matriz de buffers [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contém informações usadas como parte da operação de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="ace40-118">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="ace40-119">O conjunto preciso de buffers depende do protocolo e do pacote de codificação usado.</span><span class="sxs-lookup"><span data-stu-id="ace40-119">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="ace40-120">No mínimo, a lista conterá buffers que contêm os valores aleatórios de cliente e servidor fornecidos.</span><span class="sxs-lookup"><span data-stu-id="ace40-120">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="ace40-121">*pbEncryptedKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace40-121">*pbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace40-122">Um ponteiro para um buffer que contém a chave secreta criptografada do mestre criptografada com a [*chave pública*](/windows/desktop/SecGloss/p-gly) do servidor.</span><span class="sxs-lookup"><span data-stu-id="ace40-122">A pointer to a buffer that contains the encrypted premaster secret key encrypted with the [*public key*](/windows/desktop/SecGloss/p-gly) of the server.</span></span>

</dd> <dt>

<span data-ttu-id="ace40-123">*cbEncryptedKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace40-123">*cbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace40-124">O tamanho, em bytes, do buffer *pbEncryptedKey* .</span><span class="sxs-lookup"><span data-stu-id="ace40-124">The size, in bytes, of the *pbEncryptedKey* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ace40-125">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace40-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace40-126">Defina esse parâmetro como **o \_ \_ \_ sinalizador de servidor SSL NCRYPT** para indicar que esta é uma chamada de servidor.</span><span class="sxs-lookup"><span data-stu-id="ace40-126">Set this parameter to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace40-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ace40-127">Return value</span></span>

<span data-ttu-id="ace40-128">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ace40-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ace40-129">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ace40-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="ace40-130">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ace40-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="ace40-131">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ace40-131">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="ace40-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="ace40-132">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ace40-133"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="ace40-133"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="ace40-134">Não há memória suficiente disponível para alocar os buffers necessários.</span><span class="sxs-lookup"><span data-stu-id="ace40-134">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="ace40-135"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="ace40-135"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="ace40-136">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="ace40-136">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="ace40-137"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="ace40-137"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="ace40-138">O parâmetro *phMasterKey* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ace40-138">The *phMasterKey* parameter is **NULL**.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="ace40-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="ace40-139">Remarks</span></span>

<span data-ttu-id="ace40-140">Essa função descriptografa o segredo de mestre, computa o segredo mestre do SSL e retorna um identificador para esse objeto para o chamador.</span><span class="sxs-lookup"><span data-stu-id="ace40-140">This function decrypts the premaster secret, computes the SSL master secret, and returns a handle to this object to the caller.</span></span> <span data-ttu-id="ace40-141">Essa chave mestra pode então ser usada para derivar a chave de sessão SSL e concluir o handshake de SSL.</span><span class="sxs-lookup"><span data-stu-id="ace40-141">This master key can then be used to derive the SSL session key and finish the SSL handshake.</span></span>

> [!Note]  
> <span data-ttu-id="ace40-142">Essa função é usada quando o algoritmo de troca de chave [*RSA*](/windows/desktop/SecGloss/r-gly) está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="ace40-142">This function is used when the [*RSA*](/windows/desktop/SecGloss/r-gly) key exchange algorithm is being used.</span></span> <span data-ttu-id="ace40-143">Quando [*DH*](/windows/desktop/SecGloss/d-gly) é usado, o código do servidor chama [**SslGenerateMasterKey**](sslgeneratemasterkey.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ace40-143">When [*DH*](/windows/desktop/SecGloss/d-gly) is used, then the server code calls [**SslGenerateMasterKey**](sslgeneratemasterkey.md) instead.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ace40-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ace40-144">Requirements</span></span>



| <span data-ttu-id="ace40-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="ace40-145">Requirement</span></span> | <span data-ttu-id="ace40-146">Valor</span><span class="sxs-lookup"><span data-stu-id="ace40-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace40-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ace40-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ace40-148">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ace40-148">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ace40-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ace40-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ace40-150">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ace40-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ace40-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ace40-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="ace40-152"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="ace40-152"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ace40-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ace40-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace40-154"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace40-154"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

