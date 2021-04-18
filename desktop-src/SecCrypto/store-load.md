---
description: Importa certificados de um arquivo para o repositório.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Método Store. Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783227"
---
# <a name="storeload-method"></a><span data-ttu-id="019d2-103">Método Store. Load</span><span class="sxs-lookup"><span data-stu-id="019d2-103">Store.Load method</span></span>

<span data-ttu-id="019d2-104">\[O método **Load** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="019d2-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="019d2-105">Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="019d2-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="019d2-106">O método **Load** importa certificados de um arquivo para o repositório.</span><span class="sxs-lookup"><span data-stu-id="019d2-106">The **Load** method imports certificates from a file into the store.</span></span>

## <a name="syntax"></a><span data-ttu-id="019d2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="019d2-107">Syntax</span></span>


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="019d2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="019d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="019d2-109">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="019d2-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="019d2-110">A cadeia de caracteres que contém o caminho para um arquivo. cer,. SST,. SPC,. p7s ou. pfx ou qualquer arquivo assinado por Authenticode.</span><span class="sxs-lookup"><span data-stu-id="019d2-110">The string that contains the path to a .cer, .sst, .spc, .p7s, or .pfx file, or any Authenticode signed file.</span></span>

</dd> <dt>

<span data-ttu-id="019d2-111">*Senha* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="019d2-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="019d2-112">A cadeia de caracteres que contém a senha de texto sem formatação para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="019d2-112">The string that contains the plaintext password to the file.</span></span> <span data-ttu-id="019d2-113">Até 32 caracteres Unicode, incluindo um caractere nulo de terminação, podem ser usados para a senha.</span><span class="sxs-lookup"><span data-stu-id="019d2-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="019d2-114">Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="019d2-114">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="019d2-115">*KeyStorageFlag* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="019d2-115">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="019d2-116">Um valor da enumeração [**de \_ \_ \_ sinalizador de armazenamento de chave capicor**](capicom-key-storage-flag.md) que define os sinalizadores de armazenamento de chaves.</span><span class="sxs-lookup"><span data-stu-id="019d2-116">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="019d2-117">O padrão é o padrão de armazenamento de chave CAPICOM \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="019d2-117">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="019d2-118">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="019d2-118">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="019d2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="019d2-119">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="019d2-120">Significado</span><span class="sxs-lookup"><span data-stu-id="019d2-120">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="019d2-121"><dt>**\_padrão de \_ armazenamento de chave CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="019d2-121"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="019d2-122">Armazenamento de chaves padrão.</span><span class="sxs-lookup"><span data-stu-id="019d2-122">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="019d2-123"><dt>**o armazenamento de chaves capicor é \_ \_ \_ exportável**</dt></span><span class="sxs-lookup"><span data-stu-id="019d2-123"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="019d2-124">A chave é exportável.</span><span class="sxs-lookup"><span data-stu-id="019d2-124">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="019d2-125"><dt>**CAPICOM de \_ armazenamento de chave \_ \_ \_ protegido pelo usuário**</dt></span><span class="sxs-lookup"><span data-stu-id="019d2-125"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="019d2-126">A chave é protegida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="019d2-126">The key is user protected.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="019d2-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="019d2-127">Return value</span></span>

<span data-ttu-id="019d2-128">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="019d2-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="019d2-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="019d2-129">Remarks</span></span>

<span data-ttu-id="019d2-130">Se o método **Load** for chamado em um repositório de memória, os contêineres de chave criados serão excluídos quando o armazenamento de memória for excluído.</span><span class="sxs-lookup"><span data-stu-id="019d2-130">If the **Load** method is called on a memory store, any key containers that are created will be deleted when the memory store is deleted.</span></span> <span data-ttu-id="019d2-131">Por exemplo, se um arquivo. pfx for carregado em um repositório de memória e adicionado posteriormente a um repositório do sistema (como o meu repositório) do armazenamento de memória, o certificado no meu repositório não conterá uma chave.</span><span class="sxs-lookup"><span data-stu-id="019d2-131">For example, if a .pfx file is loaded into a memory store and later added to a system store (such as the My store) from the memory store, the certificate in the My store will not contain a key.</span></span> <span data-ttu-id="019d2-132">Nesse caso, o arquivo. pfx deve ser carregado diretamente no meu repositório.</span><span class="sxs-lookup"><span data-stu-id="019d2-132">In this case, the .pfx file should be loaded directly into the My store.</span></span>

<span data-ttu-id="019d2-133">Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="019d2-133">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="019d2-134">Se a senha falhar ao descriptografar o arquivo de chave privada, o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) padrão deverá ser consultado.</span><span class="sxs-lookup"><span data-stu-id="019d2-134">If the password fails to decrypt the private key file, then the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) should be queried.</span></span> <span data-ttu-id="019d2-135">Se o CSP padrão for o provedor criptográfico base da Microsoft e a operação de descriptografia falhar, a operação de descriptografia deverá ser tentada novamente com o provedor de criptografia forte da Microsoft ou com o provedor criptográfico avançado da Microsoft, o que estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="019d2-135">If the default CSP is the Microsoft Base Cryptographic Provider and the decrypt operation fails, then the decrypt operation should be tried again with the Microsoft Strong Cryptographic Provider or Microsoft Enhanced Cryptographic Provider, whichever is available.</span></span>

<span data-ttu-id="019d2-136">Se o certificado que está sendo carregado no repositório for o mesmo que já existe, o método **Load** excluirá o certificado existente do repositório e, em seguida, adicionará o novo certificado.</span><span class="sxs-lookup"><span data-stu-id="019d2-136">If the certificate being loaded into the store is the same as one that is already there, the **Load** method will delete the existing certificate from the store and then add the new certificate.</span></span> <span data-ttu-id="019d2-137">O novo certificado herdará as propriedades do certificado existente.</span><span class="sxs-lookup"><span data-stu-id="019d2-137">The new certificate will inherit properties from the existing certificate.</span></span> <span data-ttu-id="019d2-138">O contêiner de chave privada existente é substituído pelo novo contêiner de chave privada.</span><span class="sxs-lookup"><span data-stu-id="019d2-138">The existing private key container is replaced by the new private key container.</span></span>

## <a name="requirements"></a><span data-ttu-id="019d2-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="019d2-139">Requirements</span></span>



| <span data-ttu-id="019d2-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="019d2-140">Requirement</span></span> | <span data-ttu-id="019d2-141">Valor</span><span class="sxs-lookup"><span data-stu-id="019d2-141">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="019d2-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="019d2-142">Redistributable</span></span><br/> | <span data-ttu-id="019d2-143">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="019d2-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="019d2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="019d2-144">DLL</span></span><br/>             | <dl> <span data-ttu-id="019d2-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="019d2-145"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="019d2-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="019d2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="019d2-147">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="019d2-147">**Store**</span></span>](store.md)
</dt> </dl>

 

 
