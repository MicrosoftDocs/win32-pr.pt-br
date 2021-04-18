---
description: Protege a chave de criptografia do volume com uma chave externa de 256 bits.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Método ProtectKeyWithExternalKey da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: adcbdfdb9ea55139626bf3d1657b2e154c8d2b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789483"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e15de-103">Método ProtectKeyWithExternalKey da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="e15de-103">ProtectKeyWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e15de-104">O método **ProtectKeyWithExternalKey** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protege a chave de criptografia do volume com uma chave externa de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="e15de-104">The **ProtectKeyWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a 256-bit external key.</span></span> <span data-ttu-id="e15de-105">Essa chave externa pode ser usada para se recuperar das falhas de autenticação de outros protetores de chave (por exemplo, TPM).</span><span class="sxs-lookup"><span data-stu-id="e15de-105">This external key can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="e15de-106">Use o método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) para salvar essa chave externa em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e15de-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file.</span></span> <span data-ttu-id="e15de-107">Dispositivos de memória USB que contêm essa chave externa podem ser usados como uma chave de inicialização ou uma chave de recuperação quando o computador é iniciado.</span><span class="sxs-lookup"><span data-stu-id="e15de-107">USB memory devices that contain this external key can be used as a startup key or a recovery key when the computer starts.</span></span>

<span data-ttu-id="e15de-108">Um protetor de chave do tipo "chave externa" é criado para o volume.</span><span class="sxs-lookup"><span data-stu-id="e15de-108">A key protector of type "External Key" is created for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="e15de-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e15de-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="e15de-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e15de-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e15de-111">*FriendlyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e15de-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e15de-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e15de-112">Type: **string**</span></span>

<span data-ttu-id="e15de-113">Uma cadeia de caracteres que especifica um identificador atribuído pelo usuário para esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="e15de-113">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="e15de-114">Se esse parâmetro não for especificado, um valor em branco será usado.</span><span class="sxs-lookup"><span data-stu-id="e15de-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="e15de-115">*ExternalKey* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e15de-115">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e15de-116">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e15de-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="e15de-117">Uma matriz de bytes que especifica a chave externa de 256 bits usada para desbloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="e15de-117">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

<span data-ttu-id="e15de-118">Se nenhuma chave externa for especificada, uma será gerada aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="e15de-118">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="e15de-119">Use o método [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) para obter a chave gerada aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="e15de-119">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="e15de-120">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e15de-120">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e15de-121">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e15de-121">Type: **string**</span></span>

<span data-ttu-id="e15de-122">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="e15de-122">A unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="e15de-123">Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.</span><span class="sxs-lookup"><span data-stu-id="e15de-123">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e15de-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e15de-124">Return value</span></span>

<span data-ttu-id="e15de-125">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e15de-125">Type: **uint32**</span></span>

<span data-ttu-id="e15de-126">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="e15de-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="e15de-127">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e15de-127">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="e15de-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="e15de-128">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e15de-129"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e15de-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="e15de-130">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e15de-130">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e15de-131"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="e15de-131"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="e15de-132">O parâmetro *ExternalKey* é fornecido, mas não é uma matriz de tamanho 4.</span><span class="sxs-lookup"><span data-stu-id="e15de-132">The *ExternalKey* parameter is provided but is not an array of size 4.</span></span><br/>            |
| <dl> <span data-ttu-id="e15de-133"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="e15de-133"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="e15de-134">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e15de-134">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="e15de-135"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="e15de-135"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="e15de-136">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="e15de-136">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="e15de-137">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e15de-137">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="e15de-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="e15de-138">Remarks</span></span>

<span data-ttu-id="e15de-139">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e15de-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e15de-140">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="e15de-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e15de-141">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e15de-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e15de-142">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e15de-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e15de-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e15de-143">Requirements</span></span>



| <span data-ttu-id="e15de-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e15de-144">Requirement</span></span> | <span data-ttu-id="e15de-145">Valor</span><span class="sxs-lookup"><span data-stu-id="e15de-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e15de-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e15de-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e15de-147">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="e15de-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e15de-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e15de-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e15de-149">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e15de-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e15de-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="e15de-150">Namespace</span></span><br/>                | <span data-ttu-id="e15de-151">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="e15de-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e15de-152">MOF</span><span class="sxs-lookup"><span data-stu-id="e15de-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e15de-153"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e15de-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e15de-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="e15de-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e15de-155">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="e15de-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
