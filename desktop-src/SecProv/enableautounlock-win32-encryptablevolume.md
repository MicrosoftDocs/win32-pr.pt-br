---
description: Permite que um volume de dados seja desbloqueado automaticamente quando o volume é montado.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Método EnableAutoUnlock da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828542"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0967c-103">Método EnableAutoUnlock da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="0967c-103">EnableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0967c-104">O método **EnableAutoUnlock** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) permite que um volume de dados seja desbloqueado automaticamente quando o volume é montado.</span><span class="sxs-lookup"><span data-stu-id="0967c-104">The **EnableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class allows a data volume to be automatically unlocked when the volume is mounted.</span></span>

<span data-ttu-id="0967c-105">O desbloqueio automático salva uma chave externa no sistema operacional que pode desbloquear automaticamente o volume no volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="0967c-105">Automatic unlocking saves an external key to the operating system that can automatically unlock the volume onto the currently running operating system volume.</span></span>

<span data-ttu-id="0967c-106">Para usar esse método, o volume do sistema operacional já deve estar protegido pelo Criptografia de Unidade de Disco BitLocker ou deve ter criptografia em andamento.</span><span class="sxs-lookup"><span data-stu-id="0967c-106">To use this method, the operating system volume must already be protected by BitLocker Drive Encryption or must have encryption in progress.</span></span> <span data-ttu-id="0967c-107">Além disso, já deve existir uma chave externa para o volume de dados.</span><span class="sxs-lookup"><span data-stu-id="0967c-107">In addition, there must already exist an external key for the data volume.</span></span> <span data-ttu-id="0967c-108">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para criar a chave externa que pode desbloquear automaticamente o volume.</span><span class="sxs-lookup"><span data-stu-id="0967c-108">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) to create the external key that can automatically unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="0967c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0967c-109">Syntax</span></span>


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="0967c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0967c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0967c-111">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0967c-111">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0967c-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0967c-112">Type: **string**</span></span>

<span data-ttu-id="0967c-113">Uma cadeia de caracteres que identifica o protetor de chave do tipo "chave externa" usada para desbloquear automaticamente o volume.</span><span class="sxs-lookup"><span data-stu-id="0967c-113">A string that identifies the key protector of the type "External Key" used to automatically unlock the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0967c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0967c-114">Return value</span></span>

<span data-ttu-id="0967c-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0967c-115">Type: **uint32**</span></span>

<span data-ttu-id="0967c-116">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="0967c-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="0967c-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0967c-117">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="0967c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0967c-118">Description</span></span>                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0967c-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0967c-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="0967c-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0967c-120">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="0967c-121"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="0967c-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>          | <span data-ttu-id="0967c-122">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="0967c-122">The volume is locked.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="0967c-123"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="0967c-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>          | <span data-ttu-id="0967c-124">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="0967c-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="0967c-125">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0967c-125">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                 |
| <dl> <span data-ttu-id="0967c-126"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="0967c-126"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                   | <span data-ttu-id="0967c-127">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave válido do tipo "chave externa".</span><span class="sxs-lookup"><span data-stu-id="0967c-127">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector of the type "External Key".</span></span><br/>                                                          |
| <dl> <span data-ttu-id="0967c-128"><dt>**FVE \_ E \_ não \_ \_ VOLUME de dados**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="0967c-128"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>       | <span data-ttu-id="0967c-129">O método não pode ser executado para o volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="0967c-129">The method cannot be run for the currently running operating system volume.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="0967c-130"><dt>**FVE \_ E \_ os \_ não \_ protegidos**</dt> <dt>2150694944 (0x80310020)</dt></span><span class="sxs-lookup"><span data-stu-id="0967c-130"><dt>**FVE\_E\_OS\_NOT\_PROTECTED**</dt> <dt>2150694944 (0x80310020)</dt></span></span> </dl>      | <span data-ttu-id="0967c-131">O método não poderá ser executado se o volume do sistema operacional em execução no momento não estiver protegido pelo Criptografia de Unidade de Disco BitLocker ou não tiver criptografia em andamento.</span><span class="sxs-lookup"><span data-stu-id="0967c-131">The method cannot be run if the currently running operating system volume is not protected by BitLocker Drive Encryption or does not have encryption in progress.</span></span><br/> |
| <dl> <span data-ttu-id="0967c-132"><dt> **FVE \_ E \_ limite de volume \_ \_ já**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="0967c-132"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY** </dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="0967c-133">O desbloqueio automático no volume foi habilitado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0967c-133">Automatic unlocking on the volume has previously been enabled.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="0967c-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="0967c-134">Remarks</span></span>

<span data-ttu-id="0967c-135">Dado um protetor de chave de volume válido do tipo "chave externa", a chave externa de 256 bits relacionada é extraída do protetor e armazenada no registro do sistema operacional em execução no momento, juntamente com a ID do protetor de chave de volume.</span><span class="sxs-lookup"><span data-stu-id="0967c-135">Given a valid volume key protector of the type "External Key", the related 256-bit external key is extracted from the protector and stored into the registry of the currently running operating system, along with the volume key protector ID.</span></span>

<span data-ttu-id="0967c-136">Se a chave externa associada à ID do protetor de chave de volume for excluída, a funcionalidade para desbloquear automaticamente o volume será desabilitada ou suspensa.</span><span class="sxs-lookup"><span data-stu-id="0967c-136">If the external key associated with the volume key protector ID is deleted, the functionality to automatically unlock the volume is disabled or suspended.</span></span>

> [!Note]  
> <span data-ttu-id="0967c-137">Não há suporte para mídia removível no momento.</span><span class="sxs-lookup"><span data-stu-id="0967c-137">Removable media is not currently supported.</span></span>

 

<span data-ttu-id="0967c-138">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0967c-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0967c-139">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="0967c-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0967c-140">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="0967c-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0967c-141">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="0967c-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0967c-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0967c-142">Requirements</span></span>



| <span data-ttu-id="0967c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="0967c-143">Requirement</span></span> | <span data-ttu-id="0967c-144">Valor</span><span class="sxs-lookup"><span data-stu-id="0967c-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0967c-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0967c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0967c-146">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="0967c-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0967c-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0967c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0967c-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0967c-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0967c-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="0967c-149">Namespace</span></span><br/>                | <span data-ttu-id="0967c-150">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0967c-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0967c-151">MOF</span><span class="sxs-lookup"><span data-stu-id="0967c-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0967c-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0967c-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0967c-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="0967c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0967c-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="0967c-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
