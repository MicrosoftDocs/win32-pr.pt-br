---
description: Importa uma chave para o provedor de protocolo de protocolo SSL protocolo (SSL).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Função SslImportKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780481"
---
# <a name="sslimportkey-function"></a><span data-ttu-id="9e84b-103">Função SslImportKey</span><span class="sxs-lookup"><span data-stu-id="9e84b-103">SslImportKey function</span></span>

<span data-ttu-id="9e84b-104">A função **SslImportKey** importa uma chave para o provedor de protocolo de [*protocolo SSL protocolo*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="9e84b-104">The **SslImportKey** function imports a key into the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e84b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e84b-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9e84b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e84b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e84b-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e84b-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e84b-108">O identificador para a instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="9e84b-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="9e84b-109">*phKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9e84b-109">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e84b-110">Um ponteiro para o identificador da [*chave de criptografia*](/windows/desktop/SecGloss/c-gly) para receber a chave importada.</span><span class="sxs-lookup"><span data-stu-id="9e84b-110">A pointer to the handle of the [*cryptographic key*](/windows/desktop/SecGloss/c-gly) to receive the imported key.</span></span>

</dd> <dt>

<span data-ttu-id="9e84b-111">*pszBlobType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e84b-111">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e84b-112">Uma cadeia de caracteres Unicode terminada em nulo que contém um identificador que especifica o tipo de [*blob*](/windows/desktop/SecGloss/b-gly) que está contido no buffer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="9e84b-112">A null-terminated Unicode string that contains an identifier that specifies the type of [*BLOB*](/windows/desktop/SecGloss/b-gly) that is contained in the *pbInput* buffer.</span></span> <span data-ttu-id="9e84b-113">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9e84b-113">This can be one of the following values.</span></span>



| <span data-ttu-id="9e84b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9e84b-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="9e84b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="9e84b-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="9e84b-116"><dt>**\_ \_ blob público do BCRYPT DH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e84b-116"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="9e84b-117">Exportar uma [*chave pública*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="9e84b-117">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="9e84b-118">O buffer *pbOutput* recebe uma estrutura de [**\_ \_ \_ blob de chave DH BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) imediatamente seguida pelos dados de chave.</span><span class="sxs-lookup"><span data-stu-id="9e84b-118">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="9e84b-119"><dt>**BLOB de BCRYPT \_ ECCPUBLIC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e84b-119"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="9e84b-120">Exportar uma [*chave pública*](/windows/desktop/SecGloss/p-gly)de [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="9e84b-120">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="9e84b-121">O buffer *pbOutput* recebe uma estrutura de [**blob de BCRYPT \_ ECCKEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) imediatamente seguida pelos dados de chave.</span><span class="sxs-lookup"><span data-stu-id="9e84b-121">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="9e84b-122"><dt>**\_blob de \_ chave \_ opaco de BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="9e84b-122"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="9e84b-123">Exporte uma [*chave simétrica*](/windows/desktop/SecGloss/s-gly) em um formato específico para um único CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ).</span><span class="sxs-lookup"><span data-stu-id="9e84b-123">Export a [*symmetric key*](/windows/desktop/SecGloss/s-gly) in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="9e84b-124">BLOBs opacos não são transferível e devem ser importados usando o mesmo CSP que gerou o BLOB.</span><span class="sxs-lookup"><span data-stu-id="9e84b-124">Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="9e84b-125"><dt>**BLOB de BCRYPT \_ RSAPUBLIC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e84b-125"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="9e84b-126">Exportar uma chave pública [*RSA*](/windows/desktop/SecGloss/r-gly) .</span><span class="sxs-lookup"><span data-stu-id="9e84b-126">Export an [*RSA*](/windows/desktop/SecGloss/r-gly) public key.</span></span> <span data-ttu-id="9e84b-127">O buffer *pbOutput* recebe uma estrutura de [**blob de BCRYPT \_ RSAKEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) imediatamente seguida pelos dados de chave.</span><span class="sxs-lookup"><span data-stu-id="9e84b-127">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="9e84b-128">*pbKeyBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e84b-128">*pbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e84b-129">Um ponteiro para o buffer que contém o [*blob de chave*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="9e84b-129">A pointer to the buffer that contains the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span>

</dd> <dt>

<span data-ttu-id="9e84b-130">*cbKeyBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e84b-130">*cbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e84b-131">O tamanho, em bytes, do buffer *pbKeyBlob* .</span><span class="sxs-lookup"><span data-stu-id="9e84b-131">The size, in bytes, of the *pbKeyBlob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9e84b-132">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e84b-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e84b-133">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9e84b-133">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e84b-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e84b-134">Return value</span></span>

<span data-ttu-id="9e84b-135">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="9e84b-135">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="9e84b-136">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9e84b-136">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="9e84b-137">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="9e84b-137">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="9e84b-138">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9e84b-138">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="9e84b-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e84b-139">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e84b-140"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="9e84b-140"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="9e84b-141">Não há memória suficiente disponível para alocar os buffers necessários.</span><span class="sxs-lookup"><span data-stu-id="9e84b-141">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="9e84b-142"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="9e84b-142"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="9e84b-143">O identificador *hSslProvider* não é válido.</span><span class="sxs-lookup"><span data-stu-id="9e84b-143">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="9e84b-144"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="9e84b-144"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="9e84b-145">O parâmetro *phKey* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9e84b-145">The *phKey* parameter is **NULL**.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="9e84b-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e84b-146">Remarks</span></span>

<span data-ttu-id="9e84b-147">Você pode usar a função **SslImportKey** para importar chaves de sessão como parte do processo de transferência de chaves de sessão de um processo para outro.</span><span class="sxs-lookup"><span data-stu-id="9e84b-147">You can use the **SslImportKey** function to import session keys as a part of the process of transferring session keys from one process to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e84b-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e84b-148">Requirements</span></span>



| <span data-ttu-id="9e84b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e84b-149">Requirement</span></span> | <span data-ttu-id="9e84b-150">Valor</span><span class="sxs-lookup"><span data-stu-id="9e84b-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e84b-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e84b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9e84b-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e84b-152">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9e84b-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e84b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9e84b-154">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e84b-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9e84b-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e84b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e84b-156"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e84b-156"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="9e84b-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9e84b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e84b-158"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e84b-158"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

