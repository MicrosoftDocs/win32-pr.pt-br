---
description: Exclui um determinado protetor de chave para o volume.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Método DeleteKeyProtector da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296264"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="98179-103">Método DeleteKeyProtector da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="98179-103">DeleteKeyProtector method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="98179-104">O método **DeleteKeyProtector** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) exclui um determinado protetor de chave para o volume.</span><span class="sxs-lookup"><span data-stu-id="98179-104">The **DeleteKeyProtector** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes a given key protector for the volume.</span></span>

<span data-ttu-id="98179-105">Se um volume não criptografado tiver protetores de chave, quando **DeleteKeyProtector** remover o último protetor de chave, o volume será revertido para um sistema de arquivos NTFS padrão.</span><span class="sxs-lookup"><span data-stu-id="98179-105">If an unencrypted volume has key protectors, when **DeleteKeyProtector** removes the last key protector, the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="98179-106">Se um volume nunca tiver sido criptografado, a exclusão do protetor de chave será revertida para NTFS.</span><span class="sxs-lookup"><span data-stu-id="98179-106">If a volume has never been encrypted, deleting the key protector will revert to NTFS.</span></span>

<span data-ttu-id="98179-107">Se o volume ainda não tiver sido totalmente descriptografado, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de remover o último protetor de chave do volume para garantir que as partes criptografadas do volume permaneçam acessíveis.</span><span class="sxs-lookup"><span data-stu-id="98179-107">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing the volume's last key protector to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="98179-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98179-108">Syntax</span></span>


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="98179-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98179-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98179-110">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98179-110">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98179-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="98179-111">Type: **string**</span></span>

<span data-ttu-id="98179-112">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="98179-112">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98179-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98179-113">Return value</span></span>

<span data-ttu-id="98179-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98179-114">Type: **uint32**</span></span>

<span data-ttu-id="98179-115">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="98179-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="98179-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="98179-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="98179-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="98179-117">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="98179-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="98179-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="98179-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="98179-119">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="98179-120"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="98179-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="98179-121">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="98179-121">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="98179-122"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="98179-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>         | <span data-ttu-id="98179-123">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="98179-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="98179-124">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="98179-124">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="98179-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="98179-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                  | <span data-ttu-id="98179-126">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave válido.</span><span class="sxs-lookup"><span data-stu-id="98179-126">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="98179-127"><dt>**FVE \_ \_Chave E \_ necessária**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="98179-127"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="98179-128">O último protetor de chave para um volume parcialmente ou totalmente criptografado não poderá ser removido se os protetores de chave estiverem habilitados.</span><span class="sxs-lookup"><span data-stu-id="98179-128">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="98179-129">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de remover esse último protetor de chave para garantir que partes criptografadas do volume permaneçam acessíveis.</span><span class="sxs-lookup"><span data-stu-id="98179-129">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="98179-130"><dt>**FVE \_ E o \_ volume \_ associado \_ já**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="98179-130"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="98179-131">Este protetor de chave não pode ser excluído porque está sendo usado para desbloquear automaticamente o volume.</span><span class="sxs-lookup"><span data-stu-id="98179-131">This key protector cannot be deleted because it is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="98179-132">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para desabilitar o desbloqueio automático antes de excluir este protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="98179-132">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before deleting this key protector.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="98179-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="98179-133">Remarks</span></span>

<span data-ttu-id="98179-134">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="98179-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="98179-135">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="98179-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="98179-136">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="98179-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="98179-137">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="98179-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98179-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98179-138">Requirements</span></span>



| <span data-ttu-id="98179-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="98179-139">Requirement</span></span> | <span data-ttu-id="98179-140">Valor</span><span class="sxs-lookup"><span data-stu-id="98179-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98179-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98179-141">Minimum supported client</span></span><br/> | <span data-ttu-id="98179-142">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="98179-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="98179-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98179-143">Minimum supported server</span></span><br/> | <span data-ttu-id="98179-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98179-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98179-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="98179-145">Namespace</span></span><br/>                | <span data-ttu-id="98179-146">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="98179-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="98179-147">MOF</span><span class="sxs-lookup"><span data-stu-id="98179-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98179-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98179-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98179-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="98179-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98179-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="98179-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
