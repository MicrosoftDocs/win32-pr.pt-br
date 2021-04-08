---
description: Protege a chave de criptografia do volume com uma senha de 48 dígitos formatada especialmente.
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Método ProtectKeyWithNumericalPassword da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829306"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f68fb-103">Método ProtectKeyWithNumericalPassword da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="f68fb-103">ProtectKeyWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f68fb-104">O método **ProtectKeyWithNumericalPassword** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protege a chave de criptografia do volume com uma senha de 48 dígitos formatada especialmente.</span><span class="sxs-lookup"><span data-stu-id="f68fb-104">The **ProtectKeyWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a specially formatted 48-digit password.</span></span> <span data-ttu-id="f68fb-105">Essa senha numérica pode ser usada para se recuperar das falhas de autenticação de outros protetores de chave (por exemplo, TPM).</span><span class="sxs-lookup"><span data-stu-id="f68fb-105">This numerical password can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="f68fb-106">Um protetor de chave do tipo "senha numérica" é criado para o volume.</span><span class="sxs-lookup"><span data-stu-id="f68fb-106">A key protector of type "Numerical Password" is created for the volume.</span></span>

<span data-ttu-id="f68fb-107">Use o método [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) para validar o formato da senha numérica.</span><span class="sxs-lookup"><span data-stu-id="f68fb-107">Use the [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) method to validate the format of the numerical password.</span></span>

## <a name="syntax"></a><span data-ttu-id="f68fb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f68fb-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="f68fb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f68fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f68fb-110">*FriendlyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f68fb-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f68fb-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f68fb-111">Type: **string**</span></span>

<span data-ttu-id="f68fb-112">Uma cadeia de caracteres que especifica um identificador atribuído pelo usuário para esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="f68fb-112">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="f68fb-113">Se esse parâmetro não for especificado, um valor em branco será usado.</span><span class="sxs-lookup"><span data-stu-id="f68fb-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="f68fb-114">*NumericalPassword* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f68fb-114">*NumericalPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f68fb-115">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f68fb-115">Type: **string**</span></span>

<span data-ttu-id="f68fb-116">Uma cadeia de caracteres que especifica a senha numérica especialmente formatada de 48 dígitos.</span><span class="sxs-lookup"><span data-stu-id="f68fb-116">A string that specifies the specially formatted 48-digit numerical password.</span></span>

<span data-ttu-id="f68fb-117">A senha numérica deve conter 48 dígitos.</span><span class="sxs-lookup"><span data-stu-id="f68fb-117">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="f68fb-118">Esses dígitos podem ser divididos em 8 grupos de 6 dígitos, com o último dígito em cada grupo, indicando um valor de soma de verificação para o grupo.</span><span class="sxs-lookup"><span data-stu-id="f68fb-118">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="f68fb-119">Cada grupo de 6 dígitos deve ser divisível por 11 e deve ser menor que 720896.</span><span class="sxs-lookup"><span data-stu-id="f68fb-119">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="f68fb-120">Supondo que um grupo de seis dígitos seja rotulado como X1, X2, X3, x4, X5 e X6, o dígito de soma de verificação X6 é calculado como – X1 + X2 – X3 + X4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="f68fb-120">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="f68fb-121">Os grupos de dígitos podem, opcionalmente, ser separados por um espaço ou hífen.</span><span class="sxs-lookup"><span data-stu-id="f68fb-121">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="f68fb-122">Portanto, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" ou "XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX, XXXXXX XXXXXX", também pode conter senhas numéricas válidas.</span><span class="sxs-lookup"><span data-stu-id="f68fb-122">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

<span data-ttu-id="f68fb-123">Se nenhuma senha numérica for especificada, uma será gerada aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="f68fb-123">If no numerical password is specified, one is randomly generated.</span></span> <span data-ttu-id="f68fb-124">Use o método [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) para obter a senha gerada aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="f68fb-124">Use the [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) method to obtain the randomly generated password.</span></span>

</dd> <dt>

<span data-ttu-id="f68fb-125">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f68fb-125">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f68fb-126">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f68fb-126">Type: **string**</span></span>

<span data-ttu-id="f68fb-127">Uma cadeia de caracteres que é o identificador exclusivo associado ao protetor criado e que pode ser usado para gerenciar o protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="f68fb-127">A string that is the unique identifier associated with the created protector and that can be used to manage the key protector.</span></span>

<span data-ttu-id="f68fb-128">Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.</span><span class="sxs-lookup"><span data-stu-id="f68fb-128">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f68fb-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f68fb-129">Return value</span></span>

<span data-ttu-id="f68fb-130">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f68fb-130">Type: **uint32**</span></span>

<span data-ttu-id="f68fb-131">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="f68fb-131">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f68fb-132">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f68fb-132">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="f68fb-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="f68fb-133">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f68fb-134"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f68fb-134"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="f68fb-135">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f68fb-135">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="f68fb-136"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="f68fb-136"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="f68fb-137">O parâmetro *NumericalPassword* não tem um formato válido.</span><span class="sxs-lookup"><span data-stu-id="f68fb-137">The *NumericalPassword* parameter does not have a valid format.</span></span><br/> |
| <dl> <span data-ttu-id="f68fb-138"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="f68fb-138"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="f68fb-139">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f68fb-139">The volume is locked.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f68fb-140"><dt>**FVE \_ E \_ \_ \_ formato de senha inválido**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="f68fb-140"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="f68fb-141">O parâmetro *NumericalPassword* não tem um formato válido.</span><span class="sxs-lookup"><span data-stu-id="f68fb-141">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="f68fb-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="f68fb-142">Remarks</span></span>

<span data-ttu-id="f68fb-143">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f68fb-143">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f68fb-144">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="f68fb-144">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f68fb-145">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f68fb-145">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f68fb-146">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f68fb-146">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f68fb-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f68fb-147">Requirements</span></span>



| <span data-ttu-id="f68fb-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="f68fb-148">Requirement</span></span> | <span data-ttu-id="f68fb-149">Valor</span><span class="sxs-lookup"><span data-stu-id="f68fb-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f68fb-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f68fb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f68fb-151">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="f68fb-151">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f68fb-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f68fb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f68fb-153">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f68fb-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f68fb-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="f68fb-154">Namespace</span></span><br/>                | <span data-ttu-id="f68fb-155">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f68fb-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f68fb-156">MOF</span><span class="sxs-lookup"><span data-stu-id="f68fb-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f68fb-157"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f68fb-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f68fb-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="f68fb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f68fb-159">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f68fb-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
