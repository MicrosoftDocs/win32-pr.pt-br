---
description: Indica se o volume e sua chave de criptografia estão protegidos.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Método GetProtectionStatus da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646985"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f09d4-103">Método GetProtectionStatus da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="f09d4-103">GetProtectionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f09d4-104">O método **GetProtectionStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se o volume e sua chave de criptografia (se houver) estão protegidos.</span><span class="sxs-lookup"><span data-stu-id="f09d4-104">The **GetProtectionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume and its encryption key (if any) are secured.</span></span>

<span data-ttu-id="f09d4-105">A proteção será desativada se um volume for não criptografado ou parcialmente criptografado, ou se a chave de criptografia do volume estiver disponível em claro no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="f09d4-105">Protection is off if a volume is unencrypted or partially encrypted, or if the volume's encryption key is available in the clear on the hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="f09d4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f09d4-106">Syntax</span></span>


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f09d4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f09d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f09d4-108">*ProtectionStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f09d4-108">*ProtectionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f09d4-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f09d4-109">Type: **uint32**</span></span>

<span data-ttu-id="f09d4-110">Especifica se o volume e a chave de criptografia (se houver) estão protegidos.</span><span class="sxs-lookup"><span data-stu-id="f09d4-110">Specifies whether the volume and the encryption key (if any) are secured.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f09d4-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f09d4-111">Value</span></span></th>
<th><span data-ttu-id="f09d4-112">Significado</span><span class="sxs-lookup"><span data-stu-id="f09d4-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <span data-ttu-id="f09d4-113">Não <dt><strong>protegido</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="f09d4-113"><dt><strong>Unprotected</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="f09d4-114">PROTEÇÃO DESATIVADA</span><span class="sxs-lookup"><span data-stu-id="f09d4-114">PROTECTION OFF</span></span><br/> <span data-ttu-id="f09d4-115">Para um HDD padrão:</span><span class="sxs-lookup"><span data-stu-id="f09d4-115">For a standard HDD:</span></span><br/> <span data-ttu-id="f09d4-116">O volume é não criptografado, parcialmente criptografado ou a chave de criptografia do volume está disponível em claro no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="f09d4-116">The volume is unencrypted, partially encrypted, or the volume's encryption key is available in the clear on the hard disk.</span></span> <span data-ttu-id="f09d4-117">A chave de criptografia estará disponível em claro no disco rígido se os protetores de chave tiverem sido desabilitados usando o método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou se nenhum protetor de chave tiver sido especificado usando os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="f09d4-117">The encryption key is available in the clear on the hard disk if key protectors have been disabled by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or if no key protectors have been specified by using the following methods:</span></span>
<ul>
<li><span data-ttu-id="f09d4-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="f09d4-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="f09d4-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="f09d4-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="f09d4-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="f09d4-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="f09d4-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="f09d4-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="f09d4-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="f09d4-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="f09d4-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="f09d4-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="f09d4-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="f09d4-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="f09d4-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="f09d4-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="f09d4-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="f09d4-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="f09d4-127">Para um EHDD:</span><span class="sxs-lookup"><span data-stu-id="f09d4-127">For an EHDD:</span></span><br/> <span data-ttu-id="f09d4-128">A banda para o volume é permanente desbloqueada, não tem um Gerenciador de chaves ou é gerenciada por um Gerenciador de chaves de terceiros.</span><span class="sxs-lookup"><span data-stu-id="f09d4-128">The band for the volume is perpetually unlocked, has no key manager, or is managed by a third party key manager.</span></span><br/> <span data-ttu-id="f09d4-129">Isso também pode significar que a banda é gerenciada pelo BitLocker, mas o método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> foi chamado e a unidade está suspensa.</span><span class="sxs-lookup"><span data-stu-id="f09d4-129">This can also mean that the band is managed by BitLocker but the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method has been called and the drive is suspended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <span data-ttu-id="f09d4-130"><dt><strong>Protegido</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="f09d4-130"><dt><strong>Protected</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="f09d4-131">PROTEÇÃO ATIVADA</span><span class="sxs-lookup"><span data-stu-id="f09d4-131">PROTECTION ON</span></span><br/> <span data-ttu-id="f09d4-132">Para um HDD padrão:</span><span class="sxs-lookup"><span data-stu-id="f09d4-132">For a standard HDD:</span></span><br/> <span data-ttu-id="f09d4-133">O volume é totalmente criptografado e a chave de criptografia para o volume não está disponível em claro no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="f09d4-133">The volume is fully encrypted and the encryption key for the volume is not available in the clear on the hard disk.</span></span><br/> <span data-ttu-id="f09d4-134">Para um EHDD:</span><span class="sxs-lookup"><span data-stu-id="f09d4-134">For an EHDD:</span></span><br/> <span data-ttu-id="f09d4-135">O BitLocker é o Gerenciador de chaves da banda.</span><span class="sxs-lookup"><span data-stu-id="f09d4-135">BitLocker is the key manager for the band.</span></span> <span data-ttu-id="f09d4-136">A unidade pode ser bloqueada ou desbloqueada, mas não pode ser desbloqueada perpétuamente.</span><span class="sxs-lookup"><span data-stu-id="f09d4-136">The drive can be locked or unlocked but cannot be perpetually unlocked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="f09d4-137"><dt><strong>Desconhecido</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="f09d4-137"><dt><strong>Unknown</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="f09d4-138">Não é possível determinar o status de proteção do volume.</span><span class="sxs-lookup"><span data-stu-id="f09d4-138">The volume protection status cannot be determined.</span></span> <span data-ttu-id="f09d4-139">Isso pode ser causado pelo volume estar em um estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f09d4-139">This can be caused by the volume being in a locked state.</span></span><br/> <span data-ttu-id="f09d4-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise e Windows Server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f09d4-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise and Windows Server 2008:</strong> This value is not supported.</span></span> <span data-ttu-id="f09d4-141">Esse valor tem suporte a partir do Windows 7 e do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f09d4-141">This value is supported beginning with Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f09d4-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f09d4-142">Return value</span></span>

<span data-ttu-id="f09d4-143">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f09d4-143">Type: **uint32**</span></span>

<span data-ttu-id="f09d4-144">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="f09d4-144">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f09d4-145">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f09d4-145">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="f09d4-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="f09d4-146">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f09d4-147"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f09d4-147"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="f09d4-148">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f09d4-148">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f09d4-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="f09d4-149">Remarks</span></span>

<span data-ttu-id="f09d4-150">Você só poderá criptografar um volume se chamar [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) primeiro ou usar um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="f09d4-150">You can encrypt a volume only if you either call [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) first or use one of the following methods:</span></span>

-   [<span data-ttu-id="f09d4-151">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="f09d4-151">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [<span data-ttu-id="f09d4-152">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="f09d4-152">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [<span data-ttu-id="f09d4-153">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="f09d4-153">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="f09d4-154">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="f09d4-154">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [<span data-ttu-id="f09d4-155">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="f09d4-155">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [<span data-ttu-id="f09d4-156">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="f09d4-156">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="f09d4-157">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="f09d4-157">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="f09d4-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="f09d4-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="f09d4-159">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="f09d4-159">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="f09d4-160">Portanto, se o disco for criptografado e *ProtectionStatus* retornar zero (proteção desativada), as chaves serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="f09d4-160">Therefore, if the disk is encrypted and *ProtectionStatus* returns zero (PROTECTION OFF), keys are disabled.</span></span>

<span data-ttu-id="f09d4-161">Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) para listar os protetores de chave que foram especificados para proteger a chave de criptografia do volume.</span><span class="sxs-lookup"><span data-stu-id="f09d4-161">Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) to list the key protectors that have been specified to secure the volume's encryption key.</span></span> <span data-ttu-id="f09d4-162">Se os protetores de chave existirem, mas a proteção for zero (proteção desativada), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) para ativar a proteção de volume.</span><span class="sxs-lookup"><span data-stu-id="f09d4-162">If key protectors exist but protection is zero (PROTECTION OFF), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) to turn on volume protection.</span></span>

<span data-ttu-id="f09d4-163">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f09d4-163">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f09d4-164">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="f09d4-164">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f09d4-165">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f09d4-165">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f09d4-166">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f09d4-166">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f09d4-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f09d4-167">Requirements</span></span>



| <span data-ttu-id="f09d4-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="f09d4-168">Requirement</span></span> | <span data-ttu-id="f09d4-169">Valor</span><span class="sxs-lookup"><span data-stu-id="f09d4-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f09d4-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f09d4-170">Minimum supported client</span></span><br/> | <span data-ttu-id="f09d4-171">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="f09d4-171">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f09d4-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f09d4-172">Minimum supported server</span></span><br/> | <span data-ttu-id="f09d4-173">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f09d4-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f09d4-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="f09d4-174">Namespace</span></span><br/>                | <span data-ttu-id="f09d4-175">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f09d4-175">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f09d4-176">MOF</span><span class="sxs-lookup"><span data-stu-id="f09d4-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f09d4-177"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f09d4-177"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09d4-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="f09d4-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09d4-179">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f09d4-179">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
