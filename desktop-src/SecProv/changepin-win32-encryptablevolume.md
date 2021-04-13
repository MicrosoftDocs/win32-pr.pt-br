---
description: Altera o PIN associado a um volume criptografado.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Método ChangePIN da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501536"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="12387-103">Método ChangePIN da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="12387-103">ChangePIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="12387-104">O método **ChangePIN** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) altera o PIN associado a um volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="12387-104">The **ChangePIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes the PIN associated with an encrypted volume.</span></span> <span data-ttu-id="12387-105">Se a política de grupo "permitir PINs avançados para inicialização" estiver habilitada, um PIN poderá conter letras, símbolos e espaços além dos números.</span><span class="sxs-lookup"><span data-stu-id="12387-105">If the "Allow enhanced PINs for startup" group policy is enabled, a PIN can contain letters, symbols, and spaces in addition to numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="12387-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12387-106">Syntax</span></span>


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a><span data-ttu-id="12387-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12387-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12387-108">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12387-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12387-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12387-109">Type: **string**</span></span>

<span data-ttu-id="12387-110">O identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="12387-110">The unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="12387-111">*NewPIN* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12387-111">*NewPIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12387-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12387-112">Type: **string**</span></span>

<span data-ttu-id="12387-113">Uma cadeia de caracteres de identificação pessoal especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="12387-113">A user-specified personal identification string.</span></span> <span data-ttu-id="12387-114">Essa cadeia de caracteres deve consistir em uma sequência de 4 a 20 dígitos ou, se a política de grupo "permitir PINs avançados para inicialização" estiver habilitada, de 4 a 20 letras, símbolos, espaços ou números.</span><span class="sxs-lookup"><span data-stu-id="12387-114">This string must consist of a sequence of 4 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 4 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12387-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12387-115">Return value</span></span>

<span data-ttu-id="12387-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12387-116">Type: **uint32**</span></span>

<span data-ttu-id="12387-117">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="12387-117">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="12387-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="12387-118">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="12387-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="12387-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12387-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="12387-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="12387-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="12387-121">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="12387-122"><dt>**FVE \_ E \_ inicializável \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="12387-122"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="12387-123">Um CD/DVD inicializável foi encontrado neste computador.</span><span class="sxs-lookup"><span data-stu-id="12387-123">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="12387-124">Remova o CD/DVD e reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="12387-124">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="12387-125"><dt>**FVE \_ E \_ \_ \_ caracteres de PIN inválidos**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="12387-125"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="12387-126">O parâmetro *NewPIN* contém caracteres que não são válidos.</span><span class="sxs-lookup"><span data-stu-id="12387-126">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="12387-127">Quando a Política de Grupo "permitir PINs avançados para inicialização" está desabilitada, somente os números têm suporte.</span><span class="sxs-lookup"><span data-stu-id="12387-127">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="12387-128"><dt>**FVE \_ E \_ \_ \_ tipo de protetor inválido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="12387-128"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>     | <span data-ttu-id="12387-129">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "senha numérica" ou "chave externa".</span><span class="sxs-lookup"><span data-stu-id="12387-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="12387-130">Use o método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para criar um protetor de chave do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="12387-130">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |
| <dl> <span data-ttu-id="12387-131"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="12387-131"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="12387-132">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="12387-132">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="12387-133"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="12387-133"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>               | <span data-ttu-id="12387-134">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="12387-134">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="12387-135">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="12387-135">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="12387-136"><dt>**FVE \_ \_Política E \_ \_ \_ comprimento de PIN inválido**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="12387-136"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="12387-137">O parâmetro *NewPIN* fornecido tem mais de 20 caracteres, menos de 4 caracteres ou menos que o comprimento mínimo especificado por política de grupo.</span><span class="sxs-lookup"><span data-stu-id="12387-137">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 4 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="12387-138"><dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="12387-138"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>        | <span data-ttu-id="12387-139">O protetor de chave fornecido não existe no volume.</span><span class="sxs-lookup"><span data-stu-id="12387-139">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="12387-140"><dt>**TBS \_ O \_ serviço E \_ não \_ está executando**</dt> o <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="12387-140"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="12387-141">Nenhum Trusted Platform Module compatível (TPM) encontrado neste computador.</span><span class="sxs-lookup"><span data-stu-id="12387-141">No compatible Trusted Platform Module (TPM) is found on this computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="12387-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="12387-142">Remarks</span></span>

<span data-ttu-id="12387-143">O método **ChangePIN** cria um novo TPM e um protetor de PIN com base nas informações de protetor existentes e no PIN fornecido recentemente.</span><span class="sxs-lookup"><span data-stu-id="12387-143">The **ChangePIN** method creates a new TPM and PIN protector based on the existing protector information and the newly provided PIN.</span></span> <span data-ttu-id="12387-144">O novo protetor terá o mesmo GUID.</span><span class="sxs-lookup"><span data-stu-id="12387-144">The new protector will have the same GUID.</span></span> <span data-ttu-id="12387-145">O método **ChangePIN** também pode ser chamado para alterar o PIN de qualquer protetor de chave que usa um PIN, por exemplo, TPM e PIN ou TPM com PIN e USB.</span><span class="sxs-lookup"><span data-stu-id="12387-145">The **ChangePIN** method can also be called to change the PIN of any key protector that uses a PIN, for example, TPM and PIN or TPM with PIN and USB.</span></span>

<span data-ttu-id="12387-146">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="12387-146">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="12387-147">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="12387-147">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="12387-148">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="12387-148">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="12387-149">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="12387-149">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12387-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12387-150">Requirements</span></span>



| <span data-ttu-id="12387-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="12387-151">Requirement</span></span> | <span data-ttu-id="12387-152">Valor</span><span class="sxs-lookup"><span data-stu-id="12387-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12387-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12387-153">Minimum supported client</span></span><br/> | <span data-ttu-id="12387-154">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="12387-154">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="12387-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12387-155">Minimum supported server</span></span><br/> | <span data-ttu-id="12387-156">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="12387-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12387-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="12387-157">Namespace</span></span><br/>                | <span data-ttu-id="12387-158">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="12387-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="12387-159">MOF</span><span class="sxs-lookup"><span data-stu-id="12387-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12387-160"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12387-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12387-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="12387-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12387-162">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="12387-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
