---
description: Retorna protocolo SSL uma chave de sessão de protocolo SSL ou uma chave efêmera pública para um BLOB serializado.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Função SslExportKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921409"
---
# <a name="sslexportkey-function"></a><span data-ttu-id="635b5-103">Função SslExportKey</span><span class="sxs-lookup"><span data-stu-id="635b5-103">SslExportKey function</span></span>

<span data-ttu-id="635b5-104">A função **SslExportKey** retorna uma [*chave de sessão*](/windows/desktop/SecGloss/s-gly) de protocolo SSL ou [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) uma chave efêmera pública para um [*blob*](/windows/desktop/SecGloss/b-gly)serializado.</span><span class="sxs-lookup"><span data-stu-id="635b5-104">The **SslExportKey** function returns an [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) [*session key*](/windows/desktop/SecGloss/s-gly) or public ephemeral key into a serialized [*BLOB*](/windows/desktop/SecGloss/b-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="635b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="635b5-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="635b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="635b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="635b5-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="635b5-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="635b5-108">O identificador da instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="635b5-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="635b5-109">*HKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="635b5-109">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="635b5-110">O identificador da chave a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="635b5-110">The handle of the key to export.</span></span>

<span data-ttu-id="635b5-111">Quando você não estiver especificando uma chave, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="635b5-111">When you are not specifying a key, set this parameter to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="635b5-112">Um identificador *HKEY* é obtido chamando a função [**SslOpenPrivateKey**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="635b5-112">A *hKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="635b5-113">Não há suporte para identificadores obtidos da função [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) .</span><span class="sxs-lookup"><span data-stu-id="635b5-113">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="635b5-114">*pszBlobType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="635b5-114">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="635b5-115">Uma cadeia de caracteres Unicode terminada em nulo que contém um identificador que especifica o tipo de BLOB a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="635b5-115">A null-terminated Unicode string that contains an identifier that specifies the type of BLOB to export.</span></span> <span data-ttu-id="635b5-116">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="635b5-116">This can be one of the following values.</span></span>



| <span data-ttu-id="635b5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="635b5-117">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="635b5-118">Significado</span><span class="sxs-lookup"><span data-stu-id="635b5-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="635b5-119"><dt>**\_ \_ blob público do BCRYPT DH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="635b5-119"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="635b5-120">Exportar uma [*chave pública*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="635b5-120">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="635b5-121">O buffer *pbOutput* recebe uma estrutura de [**\_ \_ \_ blob de chave DH BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) imediatamente seguida pelos dados de chave.</span><span class="sxs-lookup"><span data-stu-id="635b5-121">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="635b5-122"><dt>**BLOB de BCRYPT \_ ECCPUBLIC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="635b5-122"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="635b5-123">Exportar uma chave pública de [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="635b5-123">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) public key.</span></span> <span data-ttu-id="635b5-124">O buffer *pbOutput* recebe uma estrutura de [**blob de BCRYPT \_ ECCKEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) imediatamente seguida pelos dados de chave.</span><span class="sxs-lookup"><span data-stu-id="635b5-124">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="635b5-125"><dt>**\_blob de \_ chave \_ opaco de BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="635b5-125"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="635b5-126">Exporte uma chave simétrica em um formato específico para um único CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ).</span><span class="sxs-lookup"><span data-stu-id="635b5-126">Export a symmetric key in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="635b5-127">BLOBs opacos não são transferível e devem ser importados usando o mesmo CSP ( *provedor de serviços de criptografia* ) que gerou o blob.</span><span class="sxs-lookup"><span data-stu-id="635b5-127">Opaque BLOBs are not transferable and must be imported by using the same *cryptographic service provider* (CSP) that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="635b5-128"><dt>**BLOB de BCRYPT \_ RSAPUBLIC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="635b5-128"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="635b5-129">Exportar uma chave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="635b5-129">Export an RSA public key.</span></span> <span data-ttu-id="635b5-130">O buffer *pbOutput* recebe uma estrutura de [**blob de BCRYPT \_ RSAKEY \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) imediatamente seguida pelos dados de chave.</span><span class="sxs-lookup"><span data-stu-id="635b5-130">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="635b5-131">*pbOutput* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="635b5-131">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="635b5-132">O endereço de um buffer que recebe o [*blob de chave*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="635b5-132">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="635b5-133">O parâmetro *cbOutput* contém o tamanho desse buffer.</span><span class="sxs-lookup"><span data-stu-id="635b5-133">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="635b5-134">Se esse parâmetro for **NULL**, essa função coloca o tamanho necessário, em bytes, no **DWORD** apontado pelo parâmetro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="635b5-134">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="635b5-135">*cbOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="635b5-135">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="635b5-136">O tamanho, em bytes, do buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="635b5-136">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="635b5-137">*pcbResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="635b5-137">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="635b5-138">O endereço de uma variável **DWORD** que recebe o número de bytes copiados para o buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="635b5-138">The address of a **DWORD** variable that receives the number of bytes copied to the *pbOutput* buffer.</span></span> <span data-ttu-id="635b5-139">Se o parâmetro *pbOutput* for definido como **NULL** quando a função for chamada, o tamanho necessário para o buffer *pbOutput* , em bytes, será retornado no **DWORD** apontado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="635b5-139">If the *pbOutput* parameter is set to **NULL** when the function is called, the required size for the *pbOutput* buffer, in bytes, is returned in the **DWORD** pointed to by this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="635b5-140">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="635b5-140">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="635b5-141">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="635b5-141">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="635b5-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="635b5-142">Return value</span></span>

<span data-ttu-id="635b5-143">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="635b5-143">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="635b5-144">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="635b5-144">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="635b5-145">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="635b5-145">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="635b5-146">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="635b5-146">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="635b5-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="635b5-147">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="635b5-148"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="635b5-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="635b5-149">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="635b5-149">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="635b5-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="635b5-150">Remarks</span></span>

<span data-ttu-id="635b5-151">A função **SslExportKey** facilita o transporte de chaves de sessão de um processo para outro, bem como a exportação da parte pública uma chave efêmera.</span><span class="sxs-lookup"><span data-stu-id="635b5-151">The **SslExportKey** function facilitates transporting session keys from one process to another as well as exporting the public portion an ephemeral key.</span></span>

<span data-ttu-id="635b5-152">Ao exportar chaves de sessão, o tipo de BLOB é opaco, o que significa que o formato do BLOB é irrelevante, desde que as funções **SslExportKey** e [**SslImportKey**](sslimportkey.md) possam interpretá-la.</span><span class="sxs-lookup"><span data-stu-id="635b5-152">When exporting session keys, the BLOB type is opaque, meaning that the format of the BLOB is irrelevant as long as both the **SslExportKey** and [**SslImportKey**](sslimportkey.md) functions can interpret it.</span></span>

<span data-ttu-id="635b5-153">Ao exportar a parte pública de uma chave efêmera, o tipo de BLOB deve ser o tipo apropriado, como **NCrypt do blob público de \_ DH \_ \_** ou do **\_ \_ blob ECCPUBLIC de NCrypt**.</span><span class="sxs-lookup"><span data-stu-id="635b5-153">When exporting the public portion of an ephemeral key the BLOB type must be the appropriate type, such as **NCRYPT\_DH\_PUBLIC\_BLOB** or **NCRYPT\_ECCPUBLIC\_BLOB**.</span></span>

## <a name="requirements"></a><span data-ttu-id="635b5-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="635b5-154">Requirements</span></span>



| <span data-ttu-id="635b5-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="635b5-155">Requirement</span></span> | <span data-ttu-id="635b5-156">Valor</span><span class="sxs-lookup"><span data-stu-id="635b5-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="635b5-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="635b5-157">Minimum supported client</span></span><br/> | <span data-ttu-id="635b5-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="635b5-158">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="635b5-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="635b5-159">Minimum supported server</span></span><br/> | <span data-ttu-id="635b5-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="635b5-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="635b5-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="635b5-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="635b5-162"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="635b5-162"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="635b5-163">DLL</span><span class="sxs-lookup"><span data-stu-id="635b5-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="635b5-164"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="635b5-164"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

