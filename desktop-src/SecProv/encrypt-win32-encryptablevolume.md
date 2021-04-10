---
description: Inicia a criptografia de um volume totalmente descriptografado ou retoma a criptografia de um volume parcialmente criptografado.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Método Encrypt da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011712"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a90c5-103">Método Encrypt da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="a90c5-103">Encrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a90c5-104">O método **Encrypt** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) começa a criptografia de um volume totalmente descriptografado ou retoma a criptografia de um volume parcialmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-104">The **Encrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted volume, or resumes encryption of a partially encrypted volume.</span></span> <span data-ttu-id="a90c5-105">Quando a criptografia é pausada ou em andamento, esse método se comporta da mesma forma que [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="a90c5-105">When encryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="a90c5-106">Quando a descriptografia é pausada ou em andamento, esse método interrompe a descriptografia e inicia a criptografia.</span><span class="sxs-lookup"><span data-stu-id="a90c5-106">When decryption is paused or in-progress, this method stops the decryption and begins encryption.</span></span>

> [!Note]  
> <span data-ttu-id="a90c5-107">Se a unidade estiver criptografada em hardware, esse método não criptografará os dados.</span><span class="sxs-lookup"><span data-stu-id="a90c5-107">If the drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="a90c5-108">Em vez disso, ele define o status da banda como "desbloqueado" de "Always undeleted".</span><span class="sxs-lookup"><span data-stu-id="a90c5-108">Instead, it sets the band status to "unlocked" from "always unlocked".</span></span> <span data-ttu-id="a90c5-109">Se a banda estiver bloqueada, desbloqueada ou for somente leitura, a unidade será considerada criptografada.</span><span class="sxs-lookup"><span data-stu-id="a90c5-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

<span data-ttu-id="a90c5-110">**Windows Vista:** Não há suporte para a criptografia de um volume que não seja o volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="a90c5-110">**Windows Vista:** Encryption of a volume other than the currently running operating system volume is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="a90c5-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a90c5-111">Syntax</span></span>


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a90c5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a90c5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a90c5-113">*EncryptionMethod* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-113">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a90c5-114">Type: **uint32**</span></span>

<span data-ttu-id="a90c5-115">Um inteiro sem sinal que especifica o algoritmo de criptografia e o tamanho da chave usados para criptografar o volume.</span><span class="sxs-lookup"><span data-stu-id="a90c5-115">An unsigned integer that specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="a90c5-116">Se esse parâmetro for maior que zero e o volume for parcial ou totalmente criptografado, *EncryptionMethod* deverá corresponder ao método de criptografia existente do volume.</span><span class="sxs-lookup"><span data-stu-id="a90c5-116">If this parameter is greater than zero and the volume is partially or fully encrypted, *EncryptionMethod* must match the volume's existing encryption method.</span></span> <span data-ttu-id="a90c5-117">Se esse parâmetro for maior que zero e a configuração de Política de Grupo correspondente estiver habilitada com um valor válido, *EncryptionMethod* deverá corresponder à configuração de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="a90c5-117">If this parameter is greater than zero and the corresponding Group Policy setting is enabled with a valid value, *EncryptionMethod* must match the Group Policy setting.</span></span>

<span data-ttu-id="a90c5-118">Para obter uma lista de possíveis valores de EncryptionMethod, consulte o método [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="a90c5-118">For a list of possible EncryptionMethod values, see the [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="a90c5-119">O valor padrão para o Windows 7 ou abaixo é: 1 (AES \_ 128 \_ com \_ difusor).</span><span class="sxs-lookup"><span data-stu-id="a90c5-119">Default value for Windows 7 or below is: 1 (AES\_128\_WITH\_DIFFUSER).</span></span>

<span data-ttu-id="a90c5-120">O valor padrão para Windows 8, Windows 8.1 ou Windows 10, versão 1507 é: 3 (AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="a90c5-120">Default value for Windows 8, Windows 8.1 or Windows 10, version 1507 is: 3 (AES\_128).</span></span>

<span data-ttu-id="a90c5-121">O valor padrão para Windows 10, versão 1511 ou superior é: 6 (XTS \_ AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="a90c5-121">Default value for Windows 10, version 1511 or above is: 6 (XTS\_AES\_128).</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-122">*EncryptionFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-122">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a90c5-123">Type: **uint32**</span></span>

<span data-ttu-id="a90c5-124">Sinalizadores que descrevem o comportamento de criptografia.</span><span class="sxs-lookup"><span data-stu-id="a90c5-124">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="a90c5-125">**Windows 7, Windows server 2008 R2, Windows Vista Enterprise e Windows server 2008:** Este parâmetro não está disponível.</span><span class="sxs-lookup"><span data-stu-id="a90c5-125">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="a90c5-126">Uma combinação de 32 bits com os seguintes bits definidos no momento.</span><span class="sxs-lookup"><span data-stu-id="a90c5-126">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="a90c5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a90c5-127">Value</span></span>                                                                                  | <span data-ttu-id="a90c5-128">Significado</span><span class="sxs-lookup"><span data-stu-id="a90c5-128">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a90c5-129"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a90c5-129"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="a90c5-130">Execute a criptografia de volume no modo de criptografia somente de dados ao iniciar o novo processo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="a90c5-130">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="a90c5-131">Se a criptografia tiver sido pausada ou interrompida, chamar o método **Encrypt** efetivamente retomará a conversão e o valor desse bit será ignorado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-131">If encryption has been paused or stopped, calling the **Encrypt** method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="a90c5-132">Esse bit só tem efeito quando os métodos **Encrypt** ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) iniciam a criptografia do estado totalmente descriptografado, a descriptografia em estado de andamento ou o status de descriptografia em pausa.</span><span class="sxs-lookup"><span data-stu-id="a90c5-132">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="a90c5-133">Se esse bit for zero, o que significa que ele não está definido, ao iniciar o novo processo de criptografia, a conversão de modo completo será executada.</span><span class="sxs-lookup"><span data-stu-id="a90c5-133">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="a90c5-134"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="a90c5-134"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="a90c5-135">Execute o apagamento sob demanda do espaço livre no volume.</span><span class="sxs-lookup"><span data-stu-id="a90c5-135">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="a90c5-136">A chamada do método **Encrypt** com esse conjunto de bits só é permitida quando o volume não está convertendo ou apagando e está em um estado "criptografado".</span><span class="sxs-lookup"><span data-stu-id="a90c5-136">Calling the **Encrypt** method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="a90c5-137"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="a90c5-137"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="a90c5-138">Execute a operação solicitada de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="a90c5-138">Perform the requested operation synchronously.</span></span> <span data-ttu-id="a90c5-139">A chamada será bloqueada até que a operação solicitada seja concluída ou interrompida.</span><span class="sxs-lookup"><span data-stu-id="a90c5-139">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="a90c5-140">Só há suporte para esse sinalizador com o método **Encrypt** .</span><span class="sxs-lookup"><span data-stu-id="a90c5-140">This flag is only supported with the **Encrypt** method.</span></span> <span data-ttu-id="a90c5-141">Esse sinalizador pode ser **especificado quando a criptografia é** chamada para retomar a criptografia interrompida ou interrompida ou apagar ou quando a criptografia ou o apagamento estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="a90c5-141">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="a90c5-142">Isso permite que o chamador retome de forma síncrona aguardando até que o processo seja concluído ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="a90c5-142">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a90c5-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a90c5-143">Return value</span></span>

<span data-ttu-id="a90c5-144">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a90c5-144">Type: **uint32**</span></span>

<span data-ttu-id="a90c5-145">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="a90c5-145">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="a90c5-146">Esse método retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a90c5-146">This method returns immediately.</span></span> <span data-ttu-id="a90c5-147">Se o volume já estiver totalmente criptografado e nenhum outro erro for retornado, esse método retornará 0.</span><span class="sxs-lookup"><span data-stu-id="a90c5-147">If the volume is already fully encrypted and no other errors are returned, this method returns 0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a90c5-148">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a90c5-148">Return code/value</span></span></th>
<th><span data-ttu-id="a90c5-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="a90c5-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="a90c5-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="a90c5-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="a90c5-151">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a90c5-151">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="a90c5-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="a90c5-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="a90c5-153">O parâmetro <em>EncryptionMethod</em> é fornecido, mas não está dentro do intervalo conhecido ou não corresponde à configuração de política de grupo atual.</span><span class="sxs-lookup"><span data-stu-id="a90c5-153">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="a90c5-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="a90c5-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="a90c5-155">Não existe chave de criptografia para o volume.</span><span class="sxs-lookup"><span data-stu-id="a90c5-155">No encryption key exists for the volume.</span></span> <span data-ttu-id="a90c5-156">Desabilite protetores de chave usando o método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou use um dos seguintes métodos para especificar protetores de chave para o volume:</span><span class="sxs-lookup"><span data-stu-id="a90c5-156">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="a90c5-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="a90c5-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="a90c5-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="a90c5-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="a90c5-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="a90c5-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="a90c5-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="a90c5-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="a90c5-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="a90c5-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="a90c5-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="a90c5-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul><span data-ttu-id="a90c5-163">
<strong>Windows Vista:</strong> Quando não existir nenhuma chave de criptografia para o volume, ERROR_INVALID_OPERATION será retornado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a90c5-163">
<strong>Windows Vista:</strong> When no encryption key exists for the volume, ERROR_INVALID_OPERATION is returned instead.</span></span> <span data-ttu-id="a90c5-164">O valor decimal é 4317 e o valor hexadecimal é 0x10DD.</span><span class="sxs-lookup"><span data-stu-id="a90c5-164">The decimal value is 4317 and the hexadecimal value is 0x10DD.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="a90c5-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span><span class="sxs-lookup"><span data-stu-id="a90c5-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span></span></dl></td>
<td><span data-ttu-id="a90c5-166">O método de criptografia fornecido não corresponde ao volume parcialmente ou totalmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-166">The provided encryption method does not match that of the partially or fully encrypted volume.</span></span> <span data-ttu-id="a90c5-167">Para continuar a criptografia, deixe o parâmetro <em>EncryptionMethod</em> em branco ou use um valor igual a zero.</span><span class="sxs-lookup"><span data-stu-id="a90c5-167">To continue encryption, leave the <em>EncryptionMethod</em> parameter blank or use a value of zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="a90c5-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="a90c5-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="a90c5-169">O volume não pode ser criptografado porque este computador está configurado para fazer parte de um cluster de servidores.</span><span class="sxs-lookup"><span data-stu-id="a90c5-169">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="a90c5-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span><span class="sxs-lookup"><span data-stu-id="a90c5-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span></span></dl></td>
<td><span data-ttu-id="a90c5-171">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-171">The volume is locked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="a90c5-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="a90c5-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="a90c5-173">Nenhum protetor de chave da &quot; senha numérica de tipo &quot; foi especificado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-173">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="a90c5-174">O Política de Grupo requer um backup das informações de recuperação para Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a90c5-174">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="a90c5-175">Para adicionar pelo menos um protetor de chave desse tipo, use o método <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a90c5-175">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a90c5-176">Comentários</span><span class="sxs-lookup"><span data-stu-id="a90c5-176">Remarks</span></span>

<span data-ttu-id="a90c5-177">Quando você usa esse método sem o segundo parâmetro opcional (de acordo com a definição do Windows 7 e do Windows Vista Enterprise), o método sempre iniciará a conversão em modo completo para manter o comportamento compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a90c5-177">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="a90c5-178">Dessa forma, a expectativa de segurança de aplicativos e scripts existentes não será quebrada com a adição do segundo parâmetro opcional no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a90c5-178">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="a90c5-179">Você pode chamar [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) para determinar se a criptografia está em andamento e a porcentagem do volume que foi criptografado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-179">You can call [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to determine whether encryption is in progress and the percentage of the volume that has been encrypted.</span></span>

<span data-ttu-id="a90c5-180">Depois que o volume estiver totalmente criptografado e se os protetores de chave tiverem sido adicionados e habilitados, o status de proteção do volume será alterado para "ativado".</span><span class="sxs-lookup"><span data-stu-id="a90c5-180">After the volume is fully encrypted and if key protectors have been added and enabled, the protection status for the volume changes to "on".</span></span>

<span data-ttu-id="a90c5-181">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a90c5-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a90c5-182">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="a90c5-182">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a90c5-183">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a90c5-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a90c5-184">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a90c5-184">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a90c5-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a90c5-185">Requirements</span></span>



| <span data-ttu-id="a90c5-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="a90c5-186">Requirement</span></span> | <span data-ttu-id="a90c5-187">Valor</span><span class="sxs-lookup"><span data-stu-id="a90c5-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a90c5-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a90c5-188">Minimum supported client</span></span><br/> | <span data-ttu-id="a90c5-189">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-189">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a90c5-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a90c5-190">Minimum supported server</span></span><br/> | <span data-ttu-id="a90c5-191">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-191">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a90c5-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="a90c5-192">Namespace</span></span><br/>                | <span data-ttu-id="a90c5-193">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="a90c5-193">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a90c5-194">MOF</span><span class="sxs-lookup"><span data-stu-id="a90c5-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a90c5-195"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a90c5-195"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a90c5-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="a90c5-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a90c5-197">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="a90c5-197">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
