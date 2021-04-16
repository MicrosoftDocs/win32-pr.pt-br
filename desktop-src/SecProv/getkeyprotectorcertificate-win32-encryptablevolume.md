---
description: Recupera a chave pública e a impressão digital do certificado para um protetor de chave pública.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Método GetKeyProtectorCertificate da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757991"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="55976-103">Método GetKeyProtectorCertificate da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="55976-103">GetKeyProtectorCertificate method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="55976-104">O método **GetKeyProtectorCertificate** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera a [*chave pública*](../secgloss/p-gly.md) e a impressão digital do [*certificado*](../secgloss/c-gly.md) para um protetor de chave pública.</span><span class="sxs-lookup"><span data-stu-id="55976-104">The **GetKeyProtectorCertificate** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the [*public key*](../secgloss/p-gly.md) and [*certificate*](../secgloss/c-gly.md) thumbprint for a public key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="55976-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55976-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a><span data-ttu-id="55976-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55976-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55976-107">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55976-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55976-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55976-108">Type: **string**</span></span>

<span data-ttu-id="55976-109">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="55976-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="55976-110">*PublicKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="55976-110">*PublicKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55976-111">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="55976-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="55976-112">Uma matriz de bytes que especifica a chave pública.</span><span class="sxs-lookup"><span data-stu-id="55976-112">An array of bytes that specifies the public key.</span></span>

</dd> <dt>

<span data-ttu-id="55976-113">*CertThumbprint* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="55976-113">*CertThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55976-114">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55976-114">Type: **string**</span></span>

<span data-ttu-id="55976-115">Uma cadeia de caracteres que especifica a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="55976-115">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="55976-116">*Certtype* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="55976-116">*CertType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55976-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55976-117">Type: **uint32**</span></span>

<span data-ttu-id="55976-118">Um inteiro sem sinal que especifica o tipo do protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="55976-118">An unsigned integer that specifies the type of the key protector.</span></span> <span data-ttu-id="55976-119">Esse inteiro é usado para diferenciar entre o DRA (agente de recuperação de dados) e os certificados de usuário.</span><span class="sxs-lookup"><span data-stu-id="55976-119">This integer is used to differentiate between data recovery agent (DRA) and user certificates.</span></span>



| <span data-ttu-id="55976-120">Valor</span><span class="sxs-lookup"><span data-stu-id="55976-120">Value</span></span>                                                                        | <span data-ttu-id="55976-121">Significado</span><span class="sxs-lookup"><span data-stu-id="55976-121">Meaning</span></span>                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="55976-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="55976-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="55976-123">O certificado é um DRA.</span><span class="sxs-lookup"><span data-stu-id="55976-123">The certificate is a DRA.</span></span><br/>     |
| <dl> <span data-ttu-id="55976-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="55976-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="55976-125">O certificado não é um DRA.</span><span class="sxs-lookup"><span data-stu-id="55976-125">The certificate is not a DRA.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55976-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55976-126">Return value</span></span>

<span data-ttu-id="55976-127">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55976-127">Type: **uint32**</span></span>

<span data-ttu-id="55976-128">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="55976-128">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="55976-129">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="55976-129">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="55976-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="55976-130">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55976-131"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="55976-131"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="55976-132">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="55976-132">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="55976-133"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="55976-133"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                               | <span data-ttu-id="55976-134">O protetor de chave especificado não é um protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="55976-134">The specified key protector is not a key protector.</span></span> <span data-ttu-id="55976-135">Você deve inserir outro protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="55976-135">You must enter another key protector.</span></span><br/>            |
| <dl> <span data-ttu-id="55976-136"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="55976-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="55976-137">Esta unidade está bloqueada por Criptografia de Unidade de Disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="55976-137">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="55976-138">Você deve desbloquear este volume no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="55976-138">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="55976-139"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="55976-139"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="55976-140">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="55976-140">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="55976-141">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="55976-141">Add a key protector to enable BitLocker.</span></span> <br/>                    |
| <dl> <span data-ttu-id="55976-142"><dt>**FVE \_ \_Certificado de usuário de política E \_ \_ \_ necessário**</dt> <dt>2150695027 (0x80310073)</dt></span><span class="sxs-lookup"><span data-stu-id="55976-142"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt></span></span> </dl> | <span data-ttu-id="55976-143">Política de Grupo requer o uso de um certificado de usuário, como um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="55976-143">Group Policy requires the use of a user certificate, such as a smart card.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="55976-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="55976-144">Remarks</span></span>

<span data-ttu-id="55976-145">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="55976-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="55976-146">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="55976-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="55976-147">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="55976-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="55976-148">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="55976-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55976-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55976-149">Requirements</span></span>



| <span data-ttu-id="55976-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="55976-150">Requirement</span></span> | <span data-ttu-id="55976-151">Valor</span><span class="sxs-lookup"><span data-stu-id="55976-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55976-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55976-152">Minimum supported client</span></span><br/> | <span data-ttu-id="55976-153">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="55976-153">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="55976-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55976-154">Minimum supported server</span></span><br/> | <span data-ttu-id="55976-155">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="55976-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55976-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="55976-156">Namespace</span></span><br/>                | <span data-ttu-id="55976-157">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="55976-157">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="55976-158">MOF</span><span class="sxs-lookup"><span data-stu-id="55976-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55976-159"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55976-159"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55976-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="55976-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55976-161">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="55976-161">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
