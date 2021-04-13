---
description: Inicia a criptografia de um volume de sistema operacional totalmente descriptografado após um teste de hardware.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Método EncryptAfterHardwareTest da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501534"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="de807-103">Método EncryptAfterHardwareTest da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="de807-103">EncryptAfterHardwareTest method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="de807-104">O método **EncryptAfterHardwareTest** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) começa a criptografia de um volume de sistema operacional totalmente descriptografado após um teste de hardware.</span><span class="sxs-lookup"><span data-stu-id="de807-104">The **EncryptAfterHardwareTest** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted operating system volume after a hardware test.</span></span> <span data-ttu-id="de807-105">Uma reinicialização é necessária para executar este teste de hardware.</span><span class="sxs-lookup"><span data-stu-id="de807-105">A reboot is required to perform this hardware test.</span></span> <span data-ttu-id="de807-106">Use esse método em vez do método [**Encrypt**](encrypt-win32-encryptablevolume.md) para verificar se o BitLocker funcionará conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="de807-106">Use this method instead of the [**Encrypt**](encrypt-win32-encryptablevolume.md) method to check that BitLocker will work as expected.</span></span>

> [!Note]  
> <span data-ttu-id="de807-107">Se o disco rígido estiver criptografado para hardware, esse método não criptografará os dados.</span><span class="sxs-lookup"><span data-stu-id="de807-107">If the hard drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="de807-108">Em vez disso, ele define o status da banda como desbloqueado de "permanente desbloqueado".</span><span class="sxs-lookup"><span data-stu-id="de807-108">Instead, it sets the band status to unlocked from "perpetually unlocked".</span></span> <span data-ttu-id="de807-109">Se a banda estiver bloqueada, desbloqueada ou for somente leitura, a unidade será considerada criptografada.</span><span class="sxs-lookup"><span data-stu-id="de807-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="de807-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de807-110">Syntax</span></span>


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="de807-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de807-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de807-112">*EncryptionMethod* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="de807-112">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="de807-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de807-113">Type: **uint32**</span></span>

<span data-ttu-id="de807-114">Especifica o algoritmo de criptografia e o tamanho da chave usados para criptografar o volume.</span><span class="sxs-lookup"><span data-stu-id="de807-114">Specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="de807-115">Deixe esse parâmetro em branco para usar o valor padrão de zero.</span><span class="sxs-lookup"><span data-stu-id="de807-115">Leave this parameter blank to use the default value of zero.</span></span> <span data-ttu-id="de807-116">Se o volume for parcialmente ou totalmente criptografado, o valor desse parâmetro deverá ser 0 ou corresponder ao método de criptografia existente do volume.</span><span class="sxs-lookup"><span data-stu-id="de807-116">If the volume is partially or fully encrypted, the value of this parameter must be 0 or match the volume's existing encryption method.</span></span> <span data-ttu-id="de807-117">Se a configuração de Política de Grupo correspondente tiver sido habilitada com um valor válido, o valor desse parâmetro deverá ser 0 ou corresponder à configuração de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="de807-117">If the corresponding Group Policy setting has been enabled with a valid value, the value of this parameter must be 0 or match the Group Policy setting.</span></span>

<span data-ttu-id="de807-118">Se a configuração de Política de Grupo correspondente for inválida, o padrão de AES 128 com difusor será usado.</span><span class="sxs-lookup"><span data-stu-id="de807-118">If the corresponding Group Policy setting is invalid, the default of AES 128 with diffuser is used.</span></span>



| <span data-ttu-id="de807-119">Valor</span><span class="sxs-lookup"><span data-stu-id="de807-119">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="de807-120">Significado</span><span class="sxs-lookup"><span data-stu-id="de807-120">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="de807-121"><dt>**Não especificado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="de807-121"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="de807-122">Use a configuração de Política de Grupo atual, se disponível e válida, caso contrário, o método de criptografia padrão.</span><span class="sxs-lookup"><span data-stu-id="de807-122">Use the current Group Policy setting, if available and valid, or the default encryption method otherwise.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="de807-123"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="de807-123"><dt>1</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="de807-124">AES 128 COM DIFUSOR</span><span class="sxs-lookup"><span data-stu-id="de807-124">AES 128 WITH DIFFUSER</span></span><br/> <span data-ttu-id="de807-125">Criptografe o volume usando o algoritmo de criptografia AES (AES) aprimorado com uma camada de difusor e usando um tamanho de chave AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="de807-125">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 128 bits.</span></span><br/> |
| <dl> <span data-ttu-id="de807-126"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="de807-126"><dt>2</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="de807-127">AES 256 COM DIFUSOR</span><span class="sxs-lookup"><span data-stu-id="de807-127">AES 256 WITH DIFFUSER</span></span><br/> <span data-ttu-id="de807-128">Criptografe o volume usando o algoritmo de criptografia AES (AES) aprimorado com uma camada de difusor e usando um tamanho de chave AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="de807-128">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 256 bits.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="de807-129"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="de807-129"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="de807-130">Criptografe o volume usando o algoritmo criptografia AES (AES) e usando um tamanho de chave AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="de807-130">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 128 bits.</span></span><br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="de807-131"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="de807-131"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                          | <span data-ttu-id="de807-132">Criptografe o volume usando o algoritmo criptografia AES (AES) e usando um tamanho de chave AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="de807-132">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 256 bits.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="de807-133">*EncryptionFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="de807-133">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="de807-134">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de807-134">Type: **uint32**</span></span>

<span data-ttu-id="de807-135">Sinalizadores que descrevem o comportamento de criptografia.</span><span class="sxs-lookup"><span data-stu-id="de807-135">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="de807-136">**Windows 7, Windows server 2008 R2, Windows Vista Enterprise e Windows server 2008:** Este parâmetro não está disponível.</span><span class="sxs-lookup"><span data-stu-id="de807-136">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="de807-137">Uma combinação de 32 bits com os seguintes bits definidos no momento.</span><span class="sxs-lookup"><span data-stu-id="de807-137">A combination of 32 bits with the following bits currently defined.</span></span>



| <span data-ttu-id="de807-138">Valor</span><span class="sxs-lookup"><span data-stu-id="de807-138">Value</span></span>                                                                                  | <span data-ttu-id="de807-139">Significado</span><span class="sxs-lookup"><span data-stu-id="de807-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de807-140"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="de807-140"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="de807-141">Execute a criptografia de volume no modo de criptografia somente de dados ao iniciar o novo processo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="de807-141">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="de807-142">Se a criptografia tiver sido pausada ou interrompida, chamar o método [**Encrypt**](encrypt-win32-encryptablevolume.md) efetivamente retomará a conversão e o valor desse bit será ignorado.</span><span class="sxs-lookup"><span data-stu-id="de807-142">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="de807-143">Esse bit só tem efeito quando os métodos **Encrypt** ou **EncryptAfterHardwareTest** iniciam a criptografia do estado totalmente descriptografado, a descriptografia em estado de andamento ou o status de descriptografia em pausa.</span><span class="sxs-lookup"><span data-stu-id="de807-143">This bit only has effect when either the **Encrypt** or **EncryptAfterHardwareTest** methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="de807-144">Se esse bit for zero, o que significa que ele não está definido, ao iniciar o novo processo de criptografia, a conversão de modo completo será executada.</span><span class="sxs-lookup"><span data-stu-id="de807-144">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="de807-145"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="de807-145"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="de807-146">Execute o apagamento sob demanda do espaço livre no volume.</span><span class="sxs-lookup"><span data-stu-id="de807-146">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="de807-147">A chamada do método [**Encrypt**](encrypt-win32-encryptablevolume.md) com esse conjunto de bits só é permitida quando o volume não está convertendo ou apagando e está em um estado "criptografado".</span><span class="sxs-lookup"><span data-stu-id="de807-147">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="de807-148"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="de807-148"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="de807-149">Execute a operação solicitada de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="de807-149">Perform the requested operation synchronously.</span></span> <span data-ttu-id="de807-150">A chamada será bloqueada até que a operação solicitada seja concluída ou interrompida.</span><span class="sxs-lookup"><span data-stu-id="de807-150">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="de807-151">Só há suporte para esse sinalizador com o método [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="de807-151">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="de807-152">Esse sinalizador pode ser **especificado quando a criptografia é** chamada para retomar a criptografia interrompida ou interrompida ou apagar ou quando a criptografia ou o apagamento estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="de807-152">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="de807-153">Isso permite que o chamador retome de forma síncrona aguardando até que o processo seja concluído ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="de807-153">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de807-154">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de807-154">Return value</span></span>

<span data-ttu-id="de807-155">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de807-155">Type: **uint32**</span></span>

<span data-ttu-id="de807-156">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="de807-156">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="de807-157">Esse método retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="de807-157">This method returns immediately.</span></span> <span data-ttu-id="de807-158">Se o volume já estiver totalmente criptografado e nenhum outro erro for retornado, esse método retornará zero.</span><span class="sxs-lookup"><span data-stu-id="de807-158">If the volume is already fully encrypted and no other errors are returned, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de807-159">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="de807-159">Return code/value</span></span></th>
<th><span data-ttu-id="de807-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="de807-160">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="de807-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="de807-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="de807-162">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="de807-162">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="de807-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="de807-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="de807-164">O parâmetro <em>EncryptionMethod</em> é fornecido, mas não está dentro do intervalo conhecido ou não corresponde à configuração de política de grupo atual.</span><span class="sxs-lookup"><span data-stu-id="de807-164">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="de807-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="de807-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="de807-166">Não existe chave de criptografia para o volume.</span><span class="sxs-lookup"><span data-stu-id="de807-166">No encryption key exists for the volume.</span></span><br/> <span data-ttu-id="de807-167">Desabilite protetores de chave usando o método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou use um dos seguintes métodos para especificar protetores de chave para o volume:</span><span class="sxs-lookup"><span data-stu-id="de807-167">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method, or use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="de807-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="de807-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="de807-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="de807-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="de807-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="de807-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="de807-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="de807-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="de807-175">O volume não pode ser criptografado porque este computador está configurado para fazer parte de um cluster de servidores.</span><span class="sxs-lookup"><span data-stu-id="de807-175">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="de807-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span><span class="sxs-lookup"><span data-stu-id="de807-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span></span></dl></td>
<td><span data-ttu-id="de807-177">Nenhum protetor de chave do tipo &quot; TPM &quot; , &quot; TPM e PIN &quot; , &quot; TPM e PIN e chave de inicialização &quot; , &quot; TPM e chave de inicialização &quot; ou &quot; chave externa &quot; podem ser encontrados.</span><span class="sxs-lookup"><span data-stu-id="de807-177">No key protectors of the type &quot;TPM&quot;, &quot;TPM And PIN&quot;, &quot;TPM And PIN And Startup Key&quot;, &quot;TPM And Startup Key&quot;, or &quot;External Key&quot; can be found.</span></span> <span data-ttu-id="de807-178">O teste de hardware só envolve os protetores de chave anteriores.</span><span class="sxs-lookup"><span data-stu-id="de807-178">The hardware test only involves the previous key protectors.</span></span><br/> <span data-ttu-id="de807-179">Se você ainda quiser executar um teste de hardware, deverá usar um dos seguintes métodos para especificar protetores de chave para o volume:</span><span class="sxs-lookup"><span data-stu-id="de807-179">If you still want to run a hardware test, you must use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="de807-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="de807-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="de807-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="de807-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="de807-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="de807-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="de807-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span><span class="sxs-lookup"><span data-stu-id="de807-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span></span></dl></td>
<td><span data-ttu-id="de807-187">O volume é parcialmente ou totalmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="de807-187">The volume is partially or fully encrypted.</span></span><br/> <span data-ttu-id="de807-188">O teste de hardware se aplica antes que ocorra a criptografia.</span><span class="sxs-lookup"><span data-stu-id="de807-188">The hardware test applies before encryption occurs.</span></span> <span data-ttu-id="de807-189">Se você ainda quiser executar o teste, primeiro use o método <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> e, em seguida, use um dos seguintes métodos para adicionar protetores de chave:</span><span class="sxs-lookup"><span data-stu-id="de807-189">If you still want to run the test, first use the <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> method and then use one of the following methods to add key protectors:</span></span>
<ul>
<li><span data-ttu-id="de807-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="de807-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="de807-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="de807-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="de807-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="de807-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="de807-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span><span class="sxs-lookup"><span data-stu-id="de807-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span></span></dl></td>
<td><span data-ttu-id="de807-196">O volume é um volume de dados.</span><span class="sxs-lookup"><span data-stu-id="de807-196">The volume is a data volume.</span></span><br/> <span data-ttu-id="de807-197">O teste de hardware aplica-se somente a volumes que podem iniciar o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="de807-197">The hardware test applies only to volumes that can start the operating system.</span></span> <span data-ttu-id="de807-198">Execute este método no volume do sistema operacional atualmente iniciado.</span><span class="sxs-lookup"><span data-stu-id="de807-198">Run this method on the currently started operating system volume.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="de807-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="de807-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="de807-200">Nenhum protetor de chave da &quot; senha numérica de tipo &quot; foi especificado.</span><span class="sxs-lookup"><span data-stu-id="de807-200">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="de807-201">O Política de Grupo requer um backup das informações de recuperação para Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="de807-201">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="de807-202">Para adicionar pelo menos um protetor de chave desse tipo, use o método <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="de807-202">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="de807-203">Comentários</span><span class="sxs-lookup"><span data-stu-id="de807-203">Remarks</span></span>

<span data-ttu-id="de807-204">Quando você usa esse método sem o segundo parâmetro opcional (de acordo com a definição do Windows 7 e do Windows Vista Enterprise), o método sempre iniciará a conversão em modo completo para manter o comportamento compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="de807-204">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="de807-205">Dessa forma, a expectativa de segurança de aplicativos e scripts existentes não será quebrada com a adição do segundo parâmetro opcional no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="de807-205">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="de807-206">Ao contrário do método [**Encrypt**](encrypt-win32-encryptablevolume.md) , esse método faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="de807-206">Unlike the [**Encrypt**](encrypt-win32-encryptablevolume.md) method, this method does the following:</span></span>

-   <span data-ttu-id="de807-207">Testa se o TPM poderá desbloquear o volume, se existir um protetor de chave relacionado ao TPM.</span><span class="sxs-lookup"><span data-stu-id="de807-207">Tests whether the TPM will be able to unlock the volume, if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="de807-208">Testa se o computador pode ler uma unidade flash USB que contém um arquivo de chave externa durante o início, se o volume for desbloqueado por uma chave externa (incluindo uma chave de inicialização).</span><span class="sxs-lookup"><span data-stu-id="de807-208">Tests whether the computer can read a USB flash drive that contains an external key file during start, if the volume will be unlocked by an external key (including a startup key).</span></span>
-   <span data-ttu-id="de807-209">Requer uma reinicialização do computador para executar o teste de hardware.</span><span class="sxs-lookup"><span data-stu-id="de807-209">Requires a computer restart to run the hardware test.</span></span>
-   <span data-ttu-id="de807-210">Inicia a criptografia somente se o teste de hardware tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="de807-210">Begins encryption only if the hardware test succeeds.</span></span>
-   <span data-ttu-id="de807-211">Não pode ser usado em um volume de dados, em um volume parcialmente ou totalmente criptografado ou para retomar a criptografia.</span><span class="sxs-lookup"><span data-stu-id="de807-211">Cannot be used on a data volume, on a partially or fully encrypted volume, or to resume encryption.</span></span>

<span data-ttu-id="de807-212">Antes de executar esse método, use os seguintes métodos para criar os protetores de chave relacionados:</span><span class="sxs-lookup"><span data-stu-id="de807-212">Before running this method, use the following methods to create the related key protectors:</span></span>

-   [<span data-ttu-id="de807-213">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="de807-213">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="de807-214">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="de807-214">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="de807-215">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="de807-215">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="de807-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="de807-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="de807-217">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="de807-217">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="de807-218">Depois de executar esse método, execute estas etapas adicionais:</span><span class="sxs-lookup"><span data-stu-id="de807-218">After running this method, take these additional steps:</span></span>

1.  <span data-ttu-id="de807-219">Insira no computador uma unidade flash USB que contenha um arquivo de chave externa.</span><span class="sxs-lookup"><span data-stu-id="de807-219">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="de807-220">Esta etapa se aplica somente se o volume tiver um protetor de chave do tipo "chave externa" ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="de807-220">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="de807-221">Reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="de807-221">Restart the computer.</span></span>

<span data-ttu-id="de807-222">Na reinicialização do computador, o teste de hardware é executado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="de807-222">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="de807-223">A criptografia começa se o teste de hardware for executado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="de807-223">Encryption begins if the hardware test succeeds.</span></span> <span data-ttu-id="de807-224">Caso contrário, tente resolver quaisquer falhas de hardware.</span><span class="sxs-lookup"><span data-stu-id="de807-224">Otherwise, attempt to resolve any hardware failures.</span></span> <span data-ttu-id="de807-225">Execute [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) depois de reiniciar o computador para obter os resultados do teste.</span><span class="sxs-lookup"><span data-stu-id="de807-225">Run [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) after restarting the computer to get test results.</span></span>

<span data-ttu-id="de807-226">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="de807-226">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="de807-227">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="de807-227">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="de807-228">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="de807-228">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="de807-229">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="de807-229">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de807-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de807-230">Requirements</span></span>



| <span data-ttu-id="de807-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="de807-231">Requirement</span></span> | <span data-ttu-id="de807-232">Valor</span><span class="sxs-lookup"><span data-stu-id="de807-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de807-233">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de807-233">Minimum supported client</span></span><br/> | <span data-ttu-id="de807-234">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="de807-234">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="de807-235">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de807-235">Minimum supported server</span></span><br/> | <span data-ttu-id="de807-236">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de807-236">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de807-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="de807-237">Namespace</span></span><br/>                | <span data-ttu-id="de807-238">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="de807-238">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="de807-239">MOF</span><span class="sxs-lookup"><span data-stu-id="de807-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de807-240"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de807-240"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de807-241">Confira também</span><span class="sxs-lookup"><span data-stu-id="de807-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de807-242">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="de807-242">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
