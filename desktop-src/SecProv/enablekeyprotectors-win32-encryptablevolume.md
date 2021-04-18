---
description: Habilita ou retoma todos os protetores de chave desabilitados ou suspensos.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Método EnableKeyProtectors da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 78f8502ae141458f1ae46a48d21c110b9434acd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796359"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0ec76-103">Método EnableKeyProtectors da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="0ec76-103">EnableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0ec76-104">O método **EnableKeyProtectors** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) habilita ou retoma todos os protetores de chave desabilitados ou suspensos.</span><span class="sxs-lookup"><span data-stu-id="0ec76-104">The **EnableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enables or resumes all disabled or suspended key protectors.</span></span> <span data-ttu-id="0ec76-105">Você pode usar esse método para habilitar novamente ou retomar a proteção BitLocker em um volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="0ec76-105">You can use this method to reenable or resume BitLocker protection on an encrypted volume.</span></span> <span data-ttu-id="0ec76-106">Esse método garante que a chave de criptografia do volume não seja exposta na limpeza no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="0ec76-106">This method ensures that the volume's encryption key is not exposed in the clear on the hard disk.</span></span>

> [!Note]  
> <span data-ttu-id="0ec76-107">Se o disco oferecer suporte à criptografia de hardware, o estado de banda passará para "desbloqueado" de "Always undeled".</span><span class="sxs-lookup"><span data-stu-id="0ec76-107">If the disc supports hardware encryption, the band state transitions to "unlocked" from "always unlocked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0ec76-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ec76-108">Syntax</span></span>


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="0ec76-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ec76-109">Parameters</span></span>

<span data-ttu-id="0ec76-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0ec76-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ec76-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ec76-111">Return value</span></span>

<span data-ttu-id="0ec76-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ec76-112">Type: **uint32**</span></span>

<span data-ttu-id="0ec76-113">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="0ec76-113">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="0ec76-114">Se os protetores de chave já estiverem habilitados e nenhum outro erro ocorrer, esse método retornará zero.</span><span class="sxs-lookup"><span data-stu-id="0ec76-114">If key protectors are already enabled and no other errors occur, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec76-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0ec76-115">Return code/value</span></span></th>
<th><span data-ttu-id="0ec76-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ec76-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="0ec76-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="0ec76-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="0ec76-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0ec76-118">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="0ec76-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span><span class="sxs-lookup"><span data-stu-id="0ec76-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span></span></dl></td>
<td><span data-ttu-id="0ec76-120">Não existem protetores de chave no volume.</span><span class="sxs-lookup"><span data-stu-id="0ec76-120">No key protectors exist on the volume.</span></span> <span data-ttu-id="0ec76-121">Use um dos seguintes métodos para especificar protetores de chave para o volume:</span><span class="sxs-lookup"><span data-stu-id="0ec76-121">Use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="0ec76-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ec76-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="0ec76-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ec76-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="0ec76-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ec76-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="0ec76-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ec76-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="0ec76-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ec76-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="0ec76-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ec76-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="0ec76-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ec76-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="0ec76-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ec76-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="0ec76-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ec76-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="0ec76-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span><span class="sxs-lookup"><span data-stu-id="0ec76-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span></span></dl></td>
<td><span data-ttu-id="0ec76-132">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="0ec76-132">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="0ec76-133">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0ec76-133">Add a key protector to enable BitLocker.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0ec76-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ec76-134">Remarks</span></span>

<span data-ttu-id="0ec76-135">Se o volume estiver totalmente criptografado, a execução bem-sucedida desse método garantirá que o volume esteja protegido.</span><span class="sxs-lookup"><span data-stu-id="0ec76-135">If the volume is fully encrypted, successfully running this method ensures that the volume is protected.</span></span> <span data-ttu-id="0ec76-136">Se o volume for parcialmente criptografado, a execução bem-sucedida desse método implicará que o volume será protegido quando ele se tornar totalmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="0ec76-136">If the volume is partially encrypted, successfully running this method implies that the volume will be protected when it becomes fully encrypted.</span></span> <span data-ttu-id="0ec76-137">Para obter mais informações, consulte o método [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec76-137">For more information, see the [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="0ec76-138">Se existirem protetores de chave baseados em TPM para o volume, a execução bem-sucedida desse método também atualizará esses protetores para que o TPM seja validado em relação aos serviços de inicialização atuais na plataforma.</span><span class="sxs-lookup"><span data-stu-id="0ec76-138">If TPM-based key protectors exist for the volume, successfully running this method also refreshes these protectors so that the TPM validates against the current startup services on the platform.</span></span> <span data-ttu-id="0ec76-139">Em outras palavras, você está afirmando que o estado atual do computador é o estado correto no qual o TPM fará a verificação em caso de reinicializações futuras do computador.</span><span class="sxs-lookup"><span data-stu-id="0ec76-139">In other words, you are asserting that the current computer state is the correct state that the TPM will check against on future computer restarts.</span></span>

<span data-ttu-id="0ec76-140">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0ec76-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0ec76-141">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="0ec76-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0ec76-142">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="0ec76-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0ec76-143">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="0ec76-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ec76-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ec76-144">Requirements</span></span>



| <span data-ttu-id="0ec76-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ec76-145">Requirement</span></span> | <span data-ttu-id="0ec76-146">Valor</span><span class="sxs-lookup"><span data-stu-id="0ec76-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec76-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ec76-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0ec76-148">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="0ec76-148">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0ec76-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ec76-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0ec76-150">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ec76-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ec76-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ec76-151">Namespace</span></span><br/>                | <span data-ttu-id="0ec76-152">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0ec76-152">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0ec76-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0ec76-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ec76-154"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ec76-154"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ec76-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ec76-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec76-156">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="0ec76-156">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-157">**DisableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="0ec76-157">**DisableKeyProtectors**</span></span>](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-158">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="0ec76-158">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-159">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="0ec76-159">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-160">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="0ec76-160">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-161">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="0ec76-161">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-162">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="0ec76-162">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-163">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="0ec76-163">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-164">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="0ec76-164">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="0ec76-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ec76-166">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="0ec76-166">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
