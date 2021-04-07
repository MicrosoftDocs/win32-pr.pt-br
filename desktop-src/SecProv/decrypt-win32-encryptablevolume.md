---
description: Começa a descriptografia de um volume totalmente criptografado ou retoma a descriptografia de um volume parcialmente criptografado.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Método Decrypt da classe Win32_EncryptableVolume (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828548"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5b27a-103">Método Decrypt da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="5b27a-103">Decrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5b27a-104">O método **Decrypt** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) começa a descriptografia de um volume totalmente criptografado ou retoma a descriptografia de um volume parcialmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="5b27a-104">The **Decrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins decryption of a fully encrypted volume, or resumes decryption of a partially encrypted volume.</span></span>

<span data-ttu-id="5b27a-105">Quando a descriptografia é pausada ou em andamento, esse método se comporta da mesma forma que [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="5b27a-105">When decryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="5b27a-106">Quando a criptografia é pausada ou em andamento, esse método reverte a criptografia e começa a descriptografia.</span><span class="sxs-lookup"><span data-stu-id="5b27a-106">When encryption is paused or in-progress, this method reverts the encryption and begins decryption.</span></span> <span data-ttu-id="5b27a-107">Após a conclusão da descriptografia, todos os protetores de chave nesse volume serão removidos do sistema e o volume será convertido em um sistema de arquivos NTFS padrão.</span><span class="sxs-lookup"><span data-stu-id="5b27a-107">After decryption completes, all key protectors on this volume are removed from the system and the volume converts to a standard NTFS file system.</span></span>

> [!Note]  
> <span data-ttu-id="5b27a-108">Se o disco estiver criptografado para hardware, o método **Decrypt** definirá o status da banda como "Always undeleted", removerá todos os metadados associados e zerará a ID de segurança da unidade.</span><span class="sxs-lookup"><span data-stu-id="5b27a-108">If the disc is hardware encrypted, the **Decrypt** method sets band status to "always unlocked", removes all associated metadata, and zeroes the security ID for the drive.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5b27a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b27a-109">Syntax</span></span>


```mof
uint32 Decrypt();
```



## <a name="parameters"></a><span data-ttu-id="5b27a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b27a-110">Parameters</span></span>

<span data-ttu-id="5b27a-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5b27a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b27a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b27a-112">Return value</span></span>

<span data-ttu-id="5b27a-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b27a-113">Type: **uint32**</span></span>

<span data-ttu-id="5b27a-114">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="5b27a-114">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="5b27a-115">Esse método retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="5b27a-115">This method returns immediately.</span></span> <span data-ttu-id="5b27a-116">Se o volume já tiver sido totalmente descriptografado e nenhum outro erro existir, esse método retornará 0.</span><span class="sxs-lookup"><span data-stu-id="5b27a-116">If the volume is already fully decrypted and no other errors exist, this method returns 0.</span></span>



| <span data-ttu-id="5b27a-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5b27a-117">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="5b27a-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b27a-118">Description</span></span>                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5b27a-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5b27a-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="5b27a-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5b27a-120">The method was successful.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="5b27a-121"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5b27a-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>      | <span data-ttu-id="5b27a-122">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5b27a-122">The volume is locked.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="5b27a-123"><dt>**FVE \_ E & \_ desbloqueio automático \_ habilitado**</dt> <dt>2150694953 (0x80310029)</dt></span><span class="sxs-lookup"><span data-stu-id="5b27a-123"><dt>**FVE\_E\_AUTOUNLOCK\_ENABLED**</dt> <dt>2150694953 (0x80310029)</dt></span></span> </dl> | <span data-ttu-id="5b27a-124">Este volume não pode ser descriptografado porque as chaves usadas para desbloquear automaticamente os volumes de dados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5b27a-124">This volume cannot be decrypted because keys used to automatically unlock data volumes are available.</span></span> <br/> <span data-ttu-id="5b27a-125">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para remover essas chaves.</span><span class="sxs-lookup"><span data-stu-id="5b27a-125">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove these keys.</span></span><br/> |



 

## <a name="security-considerations"></a><span data-ttu-id="5b27a-126">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="5b27a-126">Security Considerations</span></span>

<span data-ttu-id="5b27a-127">Chamar o método **Decrypt** deixa os dados desprotegidos.</span><span class="sxs-lookup"><span data-stu-id="5b27a-127">Calling the **Decrypt** method leaves data unprotected.</span></span>

<span data-ttu-id="5b27a-128">Se o status de proteção do volume for 1 (proteção ATIVAda) antes desse método ser usado, a conclusão bem-sucedida desse método alterará o status de proteção para 0 (proteção desativada), pois, por definição, um volume parcialmente criptografado não será protegido.</span><span class="sxs-lookup"><span data-stu-id="5b27a-128">If the protection status of the volume is 1 (PROTECTION ON) before this method is used, successful completion of this method changes the protection status to 0 (PROTECTION OFF), since by definition a partially encrypted volume is not protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b27a-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b27a-129">Remarks</span></span>

<span data-ttu-id="5b27a-130">Se o volume ainda não tiver sido totalmente descriptografado, a execução de **Decrypt** fará com que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que a descriptografia é o progresso e mostra a porcentagem do volume que permanece criptografado.</span><span class="sxs-lookup"><span data-stu-id="5b27a-130">If the volume is not already fully decrypted, running **Decrypt** causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that decryption is progress and shows the percentage of the volume that remains encrypted.</span></span>

<span data-ttu-id="5b27a-131">Se o status de proteção do volume for "on" antes que esse método seja executado, a execução desse método alterará o status de proteção para "desativado", pois, por definição, um volume parcialmente criptografado não será protegido.</span><span class="sxs-lookup"><span data-stu-id="5b27a-131">If the protection status of the volume is "on" before this method is run, running this method changes the protection status to "off", since by definition a partially encrypted volume is not protected.</span></span>

<span data-ttu-id="5b27a-132">Se esse método for executado no volume do sistema operacional em execução no momento e esse volume do sistema operacional estiver sendo usado para desbloquear automaticamente os volumes de dados (consulte o método [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), você deverá primeiro chamar o método [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="5b27a-132">If this method is run on the currently running operating system volume and this operating system volume is being used to automatically unlock data volumes (see method [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)) you must first call the method [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span></span>

<span data-ttu-id="5b27a-133">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5b27a-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5b27a-134">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="5b27a-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5b27a-135">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="5b27a-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5b27a-136">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5b27a-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b27a-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b27a-137">Requirements</span></span>



| <span data-ttu-id="5b27a-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b27a-138">Requirement</span></span> | <span data-ttu-id="5b27a-139">Valor</span><span class="sxs-lookup"><span data-stu-id="5b27a-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b27a-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b27a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5b27a-141">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="5b27a-141">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5b27a-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b27a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5b27a-143">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b27a-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5b27a-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b27a-144">Namespace</span></span><br/>                | <span data-ttu-id="5b27a-145">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5b27a-145">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5b27a-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b27a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b27a-147"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b27a-147"><dt>Infocard.h</dt></span></span> </dl>                   |
| <span data-ttu-id="5b27a-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5b27a-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b27a-149"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b27a-149"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b27a-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b27a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b27a-151">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5b27a-151">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
