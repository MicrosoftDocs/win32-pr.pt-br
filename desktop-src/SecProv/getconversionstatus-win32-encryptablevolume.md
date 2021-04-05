---
description: Indica o status da criptografia ou descriptografia no volume.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Método GetConversionStatus da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826975"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="70afd-103">Método GetConversionStatus da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="70afd-103">GetConversionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="70afd-104">O método **GetConversionStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica o status da criptografia ou descriptografia no volume.</span><span class="sxs-lookup"><span data-stu-id="70afd-104">The **GetConversionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the status of the encryption or decryption on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="70afd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70afd-105">Syntax</span></span>


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a><span data-ttu-id="70afd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70afd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70afd-107">*ConversionStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="70afd-107">*ConversionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70afd-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70afd-108">Type: **uint32**</span></span>

<span data-ttu-id="70afd-109">Criptografia de volume ou status de descriptografia.</span><span class="sxs-lookup"><span data-stu-id="70afd-109">Volume encryption or decryption status.</span></span> <span data-ttu-id="70afd-110">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="70afd-110">This can be one of the following values.</span></span>



| <span data-ttu-id="70afd-111">Valor</span><span class="sxs-lookup"><span data-stu-id="70afd-111">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="70afd-112">Significado</span><span class="sxs-lookup"><span data-stu-id="70afd-112">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <span data-ttu-id="70afd-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span></span> </dl>                         | <span data-ttu-id="70afd-114">Para uma HDD (unidade de disco rígido) padrão, o volume é totalmente descriptografado.</span><span class="sxs-lookup"><span data-stu-id="70afd-114">For a standard hard drive (HDD), the volume is fully decrypted.</span></span><br/> <span data-ttu-id="70afd-115">Para um disco rígido criptografado por hardware (EHDD), o volume é permanente desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="70afd-115">For a hardware encrypted hard drive (EHDD), the volume is perpetually unlocked.</span></span><br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <span data-ttu-id="70afd-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="70afd-117">Para uma HDD (unidade de disco rígido) padrão, o volume é totalmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="70afd-117">For a standard hard drive (HDD), the volume is fully encrypted.</span></span><br/> <span data-ttu-id="70afd-118">Para um disco rígido criptografado por hardware (EHDD), o volume não é permanente desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="70afd-118">For a hardware encrypted hard drive (EHDD), the volume is not perpetually unlocked.</span></span><br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="70afd-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="70afd-120">O volume é parcialmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="70afd-120">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="70afd-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="70afd-122">O volume é parcialmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="70afd-122">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <span data-ttu-id="70afd-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="70afd-124">O volume foi pausado durante o andamento da criptografia.</span><span class="sxs-lookup"><span data-stu-id="70afd-124">The volume has been paused during the encryption progress.</span></span> <span data-ttu-id="70afd-125">O volume é parcialmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="70afd-125">The volume is partially encrypted.</span></span><br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <span data-ttu-id="70afd-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="70afd-127">O volume foi pausado durante o andamento da descriptografia.</span><span class="sxs-lookup"><span data-stu-id="70afd-127">The volume has been paused during the decryption progress.</span></span> <span data-ttu-id="70afd-128">O volume é parcialmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="70afd-128">The volume is partially encrypted.</span></span><br/>                                                                  |



 

</dd> <dt>

<span data-ttu-id="70afd-129">*EncryptionPercentage* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="70afd-129">*EncryptionPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70afd-130">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70afd-130">Type: **uint32**</span></span>

<span data-ttu-id="70afd-131">Porcentagem do volume que é criptografado.</span><span class="sxs-lookup"><span data-stu-id="70afd-131">Percentage of the volume that is encrypted.</span></span> <span data-ttu-id="70afd-132">Este é um inteiro de 0 a 100, inclusive.</span><span class="sxs-lookup"><span data-stu-id="70afd-132">This is an integer from 0 to 100 inclusive.</span></span>

<span data-ttu-id="70afd-133">Devido ao arredondamento de números, um percentual de criptografia de 0 ou 100 não indica necessariamente que o disco está totalmente descriptografado ou totalmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="70afd-133">Due to rounding of numbers, an encryption percentage of 0 or 100 does not necessarily indicate that the disk is fully decrypted or fully encrypted.</span></span> <span data-ttu-id="70afd-134">Sempre use *ConversionStatus* para determinar se o disco está, de fato, totalmente descriptografado ou totalmente criptografado.</span><span class="sxs-lookup"><span data-stu-id="70afd-134">Always use *ConversionStatus* to determine whether the disk is in fact fully decrypted or fully encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="70afd-135">*EncryptionFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="70afd-135">*EncryptionFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70afd-136">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70afd-136">Type: **uint32**</span></span>

<span data-ttu-id="70afd-137">Sinalizadores que descrevem o comportamento de criptografia.</span><span class="sxs-lookup"><span data-stu-id="70afd-137">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="70afd-138">Uma combinação de 32 bits com os seguintes bits definidos no momento.</span><span class="sxs-lookup"><span data-stu-id="70afd-138">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="70afd-139">Valor</span><span class="sxs-lookup"><span data-stu-id="70afd-139">Value</span></span>                                                                                  | <span data-ttu-id="70afd-140">Significado</span><span class="sxs-lookup"><span data-stu-id="70afd-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70afd-141"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-141"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="70afd-142">Execute a criptografia de volume no modo de criptografia somente de dados ao iniciar o novo processo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="70afd-142">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="70afd-143">Se a criptografia tiver sido pausada ou interrompida, chamar o método [**Encrypt**](encrypt-win32-encryptablevolume.md) efetivamente retomará a conversão e o valor desse bit será ignorado.</span><span class="sxs-lookup"><span data-stu-id="70afd-143">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="70afd-144">Esse bit só tem efeito quando os métodos **Encrypt** ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) iniciam a criptografia do estado totalmente descriptografado, a descriptografia em estado de andamento ou o status de descriptografia em pausa.</span><span class="sxs-lookup"><span data-stu-id="70afd-144">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="70afd-145">Se esse bit for zero, o que significa que ele não está definido, ao iniciar o novo processo de criptografia, a conversão de modo completo será executada.</span><span class="sxs-lookup"><span data-stu-id="70afd-145">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="70afd-146"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-146"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="70afd-147">Execute o apagamento sob demanda do espaço livre no volume.</span><span class="sxs-lookup"><span data-stu-id="70afd-147">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="70afd-148">A chamada do método [**Encrypt**](encrypt-win32-encryptablevolume.md) com esse conjunto de bits só é permitida quando o volume não está convertendo ou apagando e está em um estado "criptografado".</span><span class="sxs-lookup"><span data-stu-id="70afd-148">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="70afd-149"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="70afd-149"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="70afd-150">Execute a operação solicitada de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="70afd-150">Perform the requested operation synchronously.</span></span> <span data-ttu-id="70afd-151">A chamada será bloqueada até que a operação solicitada seja concluída ou interrompida.</span><span class="sxs-lookup"><span data-stu-id="70afd-151">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="70afd-152">Só há suporte para esse sinalizador com o método [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="70afd-152">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="70afd-153">Esse sinalizador pode ser **especificado quando a criptografia é** chamada para retomar a criptografia interrompida ou interrompida ou apagar ou quando a criptografia ou o apagamento estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="70afd-153">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="70afd-154">Isso permite que o chamador retome de forma síncrona aguardando até que o processo seja concluído ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="70afd-154">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="70afd-155">*WipingStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="70afd-155">*WipingStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70afd-156">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70afd-156">Type: **uint32**</span></span>

<span data-ttu-id="70afd-157">Status de apagamento de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="70afd-157">Free space wiping status.</span></span> <span data-ttu-id="70afd-158">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="70afd-158">This can be one of the following values.</span></span>



| <span data-ttu-id="70afd-159">Valor</span><span class="sxs-lookup"><span data-stu-id="70afd-159">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="70afd-160">Significado</span><span class="sxs-lookup"><span data-stu-id="70afd-160">Meaning</span></span>                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <span data-ttu-id="70afd-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="70afd-162">O espaço livre não foi apagado.</span><span class="sxs-lookup"><span data-stu-id="70afd-162">The free space has not been wiped.</span></span><br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <span data-ttu-id="70afd-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span></span> </dl>                                             | <span data-ttu-id="70afd-164">O espaço livre foi apagado.</span><span class="sxs-lookup"><span data-stu-id="70afd-164">The free space has been wiped.</span></span><br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <span data-ttu-id="70afd-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="70afd-166">O apagamento de espaço livre está em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="70afd-166">Free space wiping is currently in progress.</span></span><br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <span data-ttu-id="70afd-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="70afd-168">O apagamento de espaço livre foi pausado.</span><span class="sxs-lookup"><span data-stu-id="70afd-168">Free space wiping has been paused.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="70afd-169">*WipingPercentage* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="70afd-169">*WipingPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70afd-170">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70afd-170">Type: **uint32**</span></span>

<span data-ttu-id="70afd-171">Um valor de 0 a 100 que especifica a porcentagem de espaço livre que foi apagado.</span><span class="sxs-lookup"><span data-stu-id="70afd-171">A value from 0 to 100 that specifies the percentage of free space that has been wiped.</span></span>

</dd> <dt>

<span data-ttu-id="70afd-172">*PrecisionFactor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70afd-172">*PrecisionFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70afd-173">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70afd-173">Type: **uint32**</span></span>

<span data-ttu-id="70afd-174">Um valor de 0 a 4 que especifica o nível de precisão</span><span class="sxs-lookup"><span data-stu-id="70afd-174">A value from 0 to 4 that specifies the precision level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70afd-175">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70afd-175">Return value</span></span>

<span data-ttu-id="70afd-176">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70afd-176">Type: **uint32**</span></span>

<span data-ttu-id="70afd-177">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="70afd-177">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="70afd-178">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="70afd-178">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="70afd-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="70afd-179">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="70afd-180"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-180"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="70afd-181">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="70afd-181">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="70afd-182"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-182"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="70afd-183">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="70afd-183">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="70afd-184">Comentários</span><span class="sxs-lookup"><span data-stu-id="70afd-184">Remarks</span></span>

<span data-ttu-id="70afd-185">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="70afd-185">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="70afd-186">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="70afd-186">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="70afd-187">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="70afd-187">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="70afd-188">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="70afd-188">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70afd-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70afd-189">Requirements</span></span>



| <span data-ttu-id="70afd-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="70afd-190">Requirement</span></span> | <span data-ttu-id="70afd-191">Valor</span><span class="sxs-lookup"><span data-stu-id="70afd-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70afd-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70afd-192">Minimum supported client</span></span><br/> | <span data-ttu-id="70afd-193">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="70afd-193">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="70afd-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70afd-194">Minimum supported server</span></span><br/> | <span data-ttu-id="70afd-195">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70afd-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70afd-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="70afd-196">Namespace</span></span><br/>                | <span data-ttu-id="70afd-197">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="70afd-197">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="70afd-198">MOF</span><span class="sxs-lookup"><span data-stu-id="70afd-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70afd-199"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70afd-199"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70afd-200">Confira também</span><span class="sxs-lookup"><span data-stu-id="70afd-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70afd-201">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="70afd-201">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
