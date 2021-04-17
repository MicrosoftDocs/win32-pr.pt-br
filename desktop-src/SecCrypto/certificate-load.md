---
description: Importa um certificado de um arquivo.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'Método ICertificate2:: Load'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755316"
---
# <a name="icertificate2load-method"></a><span data-ttu-id="e7325-103">Método ICertificate2:: Load</span><span class="sxs-lookup"><span data-stu-id="e7325-103">ICertificate2::Load method</span></span>

<span data-ttu-id="e7325-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e7325-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e7325-105">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e7325-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e7325-106">O método **Load** importa um certificado de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e7325-106">The **Load** method imports a certificate from a file.</span></span> <span data-ttu-id="e7325-107">Esse método foi introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e7325-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7325-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7325-108">Syntax</span></span>


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e7325-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7325-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7325-110">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7325-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7325-111">Uma cadeia de caracteres que contém o caminho para um arquivo. cer ou. pfx que contém os dados do certificado.</span><span class="sxs-lookup"><span data-stu-id="e7325-111">A string that contains the path to a .cer or .pfx file that contains the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="e7325-112">*Senha* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e7325-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e7325-113">Uma cadeia de caracteres que contém a senha de [*texto sem formatação*](../secgloss/p-gly.md) para o arquivo de [*chave privada*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e7325-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password to the [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="e7325-114">A senha pode conter até 32 caracteres Unicode, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="e7325-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="e7325-115">Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="e7325-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7325-116">*KeyStorageFlag* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e7325-116">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e7325-117">Um valor da enumeração [**de \_ \_ \_ sinalizador de armazenamento de chave capicor**](capicom-key-storage-flag.md) que define os sinalizadores de armazenamento de chaves.</span><span class="sxs-lookup"><span data-stu-id="e7325-117">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="e7325-118">O padrão é o padrão de armazenamento de chave CAPICOM \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e7325-118">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="e7325-119">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="e7325-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="e7325-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e7325-120">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="e7325-121">Significado</span><span class="sxs-lookup"><span data-stu-id="e7325-121">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="e7325-122"><dt>**\_padrão de \_ armazenamento de chave CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7325-122"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="e7325-123">Armazenamento de chaves padrão.</span><span class="sxs-lookup"><span data-stu-id="e7325-123">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="e7325-124"><dt>**o armazenamento de chaves capicor é \_ \_ \_ exportável**</dt></span><span class="sxs-lookup"><span data-stu-id="e7325-124"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="e7325-125">A chave é exportável.</span><span class="sxs-lookup"><span data-stu-id="e7325-125">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="e7325-126"><dt>**CAPICOM de \_ armazenamento de chave \_ \_ \_ protegido pelo usuário**</dt></span><span class="sxs-lookup"><span data-stu-id="e7325-126"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="e7325-127">A chave é protegida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e7325-127">The key is user protected.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e7325-128">*Keylocation* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e7325-128">*KeyLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e7325-129">Um valor da enumeração [**do \_ \_ local da chave CAPICOM**](capicom-key-location.md) que define os tipos de local de chave.</span><span class="sxs-lookup"><span data-stu-id="e7325-129">A value of the [**CAPICOM\_KEY\_LOCATION**](capicom-key-location.md) enumeration that defines key location types.</span></span> <span data-ttu-id="e7325-130">O valor padrão é capicor a \_ \_ chave de usuário atual \_ .</span><span class="sxs-lookup"><span data-stu-id="e7325-130">The default value is CAPICOM\_CURRENT\_USER\_KEY.</span></span> <span data-ttu-id="e7325-131">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="e7325-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="e7325-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e7325-132">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="e7325-133">Significado</span><span class="sxs-lookup"><span data-stu-id="e7325-133">Meaning</span></span>                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <span data-ttu-id="e7325-134"><dt>**CAPICOM da \_ \_ chave de usuário atual \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7325-134"><dt>**CAPICOM\_CURRENT\_USER\_KEY**</dt></span></span> </dl>    | <span data-ttu-id="e7325-135">A chave é uma chave de usuário.</span><span class="sxs-lookup"><span data-stu-id="e7325-135">The key is a user key.</span></span><br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <span data-ttu-id="e7325-136"><dt>**\_chave do \_ computador \_ local CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="e7325-136"><dt>**CAPICOM\_LOCAL\_MACHINE\_KEY**</dt></span></span> </dl> | <span data-ttu-id="e7325-137">A chave é uma chave de computador.</span><span class="sxs-lookup"><span data-stu-id="e7325-137">The key is a machine key.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7325-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7325-138">Return value</span></span>

<span data-ttu-id="e7325-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e7325-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7325-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7325-140">Remarks</span></span>

<span data-ttu-id="e7325-141">Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="e7325-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7325-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7325-142">Requirements</span></span>



| <span data-ttu-id="e7325-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7325-143">Requirement</span></span> | <span data-ttu-id="e7325-144">Valor</span><span class="sxs-lookup"><span data-stu-id="e7325-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7325-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e7325-145">End of client support</span></span><br/> | <span data-ttu-id="e7325-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7325-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e7325-147">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e7325-147">End of server support</span></span><br/> | <span data-ttu-id="e7325-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7325-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e7325-149">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e7325-149">Redistributable</span></span><br/>       | <span data-ttu-id="e7325-150">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e7325-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e7325-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e7325-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e7325-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7325-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
