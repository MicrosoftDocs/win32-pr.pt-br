---
description: Usa a frase secreta para obter a chave derivada.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Método ProtectKeyWithPassphrase da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f97806652d86b104a0f333d40d299cfa9502cf3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762904"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ad35d-103">Método ProtectKeyWithPassphrase da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="ad35d-103">ProtectKeyWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ad35d-104">O método **ProtectKeyWithPassphrase** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a frase secreta para obter a chave derivada.</span><span class="sxs-lookup"><span data-stu-id="ad35d-104">The **ProtectKeyWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="ad35d-105">Depois que a chave derivada é calculada, a chave derivada é usada para proteger a chave mestra do volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="ad35d-105">After the derived key is calculated, the derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad35d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad35d-106">Syntax</span></span>


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="ad35d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad35d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad35d-108">*FriendlyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ad35d-108">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad35d-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ad35d-109">Type: **string**</span></span>

<span data-ttu-id="ad35d-110">Uma cadeia de caracteres que especifica um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="ad35d-110">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="ad35d-111">Se esse parâmetro não for especificado, um valor em branco será usado.</span><span class="sxs-lookup"><span data-stu-id="ad35d-111">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="ad35d-112">*Frase secreta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad35d-112">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad35d-113">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ad35d-113">Type: **string**</span></span>

<span data-ttu-id="ad35d-114">Uma cadeia de caracteres que especifica a frase secreta.</span><span class="sxs-lookup"><span data-stu-id="ad35d-114">A string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="ad35d-115">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ad35d-115">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad35d-116">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ad35d-116">Type: **string**</span></span>

<span data-ttu-id="ad35d-117">Uma cadeia de caracteres que identifica exclusivamente o protetor de chave criado.</span><span class="sxs-lookup"><span data-stu-id="ad35d-117">A string that uniquely identifies the created key protector.</span></span>

<span data-ttu-id="ad35d-118">Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.</span><span class="sxs-lookup"><span data-stu-id="ad35d-118">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad35d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad35d-119">Return value</span></span>

<span data-ttu-id="ad35d-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad35d-120">Type: **uint32**</span></span>

<span data-ttu-id="ad35d-121">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="ad35d-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ad35d-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ad35d-122">Return code/value</span></span>                                                                                                                                                                                        | <span data-ttu-id="ad35d-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad35d-123">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad35d-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                        | <span data-ttu-id="ad35d-125">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ad35d-125">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="ad35d-126"><dt>**FVE \_ E \_ não \_ é \_ permitido \_ no \_ modo de segurança**</dt> <dt>2150694976 (0x80310040)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-126"><dt>**FVE\_E\_NOT\_ALLOWED\_IN\_SAFE\_MODE**</dt> <dt>2150694976 (0x80310040)</dt></span></span> </dl>         | <span data-ttu-id="ad35d-127">Criptografia de Unidade de Disco BitLocker só pode ser usado para fins de recuperação quando usado no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="ad35d-127">BitLocker Drive Encryption can only be used for recovery purposes when used in Safe Mode.</span></span><br/>                     |
| <dl> <span data-ttu-id="ad35d-128"><dt>**FVE \_ \_Senha da política E \_ \_ não \_ permitida**</dt> <dt>2150695018 (0x8031006A)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-128"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span></span> </dl>     | <span data-ttu-id="ad35d-129">A política de grupo não permite a criação de uma frase secreta.</span><span class="sxs-lookup"><span data-stu-id="ad35d-129">Group policy does not permit the creation of a passphrase.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="ad35d-130"><dt>**FVE \_ E \_ FIPS \_ impede a \_ senha**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-130"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>           | <span data-ttu-id="ad35d-131">A configuração de política de grupo que requer conformidade com FIPS impediu que a frase secreta fosse gerada ou usada.</span><span class="sxs-lookup"><span data-stu-id="ad35d-131">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span><br/> |
| <dl> <span data-ttu-id="ad35d-132"><dt>**FVE \_ E \_ \_ \_ \_ comprimento de senha inválido da política**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-132"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl>  | <span data-ttu-id="ad35d-133">A senha fornecida não atende aos requisitos mínimos ou máximos de comprimento.</span><span class="sxs-lookup"><span data-stu-id="ad35d-133">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                             |
| <dl> <span data-ttu-id="ad35d-134"><dt>**FVE \_ Senha da política de E \_ \_ \_ muito \_ simples**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-134"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>      | <span data-ttu-id="ad35d-135">A senha não atende aos requisitos de complexidade definidos pelo administrador na diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ad35d-135">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>            |
| <dl> <span data-ttu-id="ad35d-136"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                       | <span data-ttu-id="ad35d-137">O volume já está bloqueado por Criptografia de Unidade de Disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ad35d-137">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="ad35d-138">Você deve desbloquear a unidade no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="ad35d-138">You must unlock the drive from Control Panel.</span></span><br/>     |
| <dl> <span data-ttu-id="ad35d-139"><dt>**FVE \_ \_ \_ Atualização do E Overlapped**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-139"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                   | <span data-ttu-id="ad35d-140">O bloco de controle do volume criptografado foi atualizado por outro thread.</span><span class="sxs-lookup"><span data-stu-id="ad35d-140">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                     |
| <dl> <span data-ttu-id="ad35d-141"><dt>**FVE \_ \_ \_ \_ Não \_ há suporte para o protetor de chave E**</dt> <dt>2150695017 (0x80310069)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-141"><dt>**FVE\_E\_KEY\_PROTECTOR\_NOT\_SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span></span> </dl>       | <span data-ttu-id="ad35d-142">O protetor de chave não tem suporte na versão do Criptografia de Unidade de Disco BitLocker atualmente no volume.</span><span class="sxs-lookup"><span data-stu-id="ad35d-142">The key protector is not supported by the version of BitLocker Drive Encryption currently on the volume.</span></span><br/>      |
| <dl> <span data-ttu-id="ad35d-143"><dt>**FVE \_ \_Senha de volume do so E \_ \_ \_ não \_ permitida**</dt> <dt>2150695021 (0x8031006D)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-143"><dt>**FVE\_E\_OS\_VOLUME\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695021 (0x8031006D)</dt></span></span> </dl> | <span data-ttu-id="ad35d-144">A senha não pode ser adicionada ao volume do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ad35d-144">The passphrase cannot be added to the operating system volume.</span></span> <br/>                                               |
| <dl> <span data-ttu-id="ad35d-145"><dt>**FVE \_ O \_ protetor E \_ existe**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-145"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>                    | <span data-ttu-id="ad35d-146">O protetor de chave fornecido já existe neste volume.</span><span class="sxs-lookup"><span data-stu-id="ad35d-146">The provided key protector already exists on this volume.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="ad35d-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad35d-147">Requirements</span></span>



| <span data-ttu-id="ad35d-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad35d-148">Requirement</span></span> | <span data-ttu-id="ad35d-149">Valor</span><span class="sxs-lookup"><span data-stu-id="ad35d-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad35d-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad35d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ad35d-151">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="ad35d-151">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad35d-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad35d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ad35d-153">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ad35d-153">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ad35d-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad35d-154">Namespace</span></span><br/>                | <span data-ttu-id="ad35d-155">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="ad35d-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ad35d-156">MOF</span><span class="sxs-lookup"><span data-stu-id="ad35d-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad35d-157"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad35d-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad35d-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad35d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad35d-159">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="ad35d-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




