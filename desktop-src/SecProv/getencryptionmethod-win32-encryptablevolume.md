---
description: Indica o algoritmo de criptografia e o tamanho da chave usados no volume.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Método GetEncryptionMethod da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779343"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="36eaf-103">Método GetEncryptionMethod da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="36eaf-103">GetEncryptionMethod method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="36eaf-104">O método **GetEncryptionMethod** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica o algoritmo de criptografia e o tamanho da chave usados no volume.</span><span class="sxs-lookup"><span data-stu-id="36eaf-104">The **GetEncryptionMethod** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the encryption algorithm and key size used on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="36eaf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36eaf-105">Syntax</span></span>


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a><span data-ttu-id="36eaf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36eaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36eaf-107">*EncryptionMethod* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="36eaf-107">*EncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36eaf-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36eaf-108">Type: **uint32**</span></span>

<span data-ttu-id="36eaf-109">Um inteiro sem sinal que especifica o algoritmo de criptografia e o tamanho da chave usados no volume.</span><span class="sxs-lookup"><span data-stu-id="36eaf-109">An unsigned integer that specifies the encryption algorithm and key size used on the volume.</span></span>



| <span data-ttu-id="36eaf-110">Valor</span><span class="sxs-lookup"><span data-stu-id="36eaf-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="36eaf-111">Significado</span><span class="sxs-lookup"><span data-stu-id="36eaf-111">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <span data-ttu-id="36eaf-112"><dt>**Nenhum**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-112"><dt>**None**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="36eaf-113">O volume não está criptografado.</span><span class="sxs-lookup"><span data-stu-id="36eaf-113">The volume is not encrypted.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <span data-ttu-id="36eaf-114"><dt>**AES \_ 128 \_ com \_ difusor**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-114"><dt>**AES\_128\_WITH\_DIFFUSER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="36eaf-115">O volume foi totalmente ou parcialmente criptografado com o algoritmo de criptografia AES (AES) aprimorado com uma camada difusor, usando um tamanho de chave AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="36eaf-115">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 128 bits.</span></span> <span data-ttu-id="36eaf-116">Esse método não está mais disponível em dispositivos que executam o Windows 8.1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="36eaf-116">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <span data-ttu-id="36eaf-117"><dt>**AES \_ 256 \_ com \_ difusor**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-117"><dt>**AES\_256\_WITH\_DIFFUSER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="36eaf-118">O volume foi totalmente ou parcialmente criptografado com o algoritmo de criptografia AES (AES) aprimorado com uma camada difusor, usando um tamanho de chave AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="36eaf-118">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 256 bits.</span></span> <span data-ttu-id="36eaf-119">Esse método não está mais disponível em dispositivos que executam o Windows 8.1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="36eaf-119">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="36eaf-120"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-120"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="36eaf-121">O volume foi totalmente ou parcialmente criptografado com o algoritmo criptografia AES (AES), usando um tamanho de chave AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="36eaf-121">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 128 bits.</span></span><br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="36eaf-122"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-122"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                             | <span data-ttu-id="36eaf-123">O volume foi totalmente ou parcialmente criptografado com o algoritmo criptografia AES (AES), usando um tamanho de chave AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="36eaf-123">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 256 bits.</span></span><br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <span data-ttu-id="36eaf-124"><dt>**Hardware \_ do CRIPTOGRAFIA**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-124"><dt>**HARDWARE\_ENCRYPTION**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="36eaf-125">O volume foi totalmente ou parcialmente criptografado usando os recursos de hardware da unidade.</span><span class="sxs-lookup"><span data-stu-id="36eaf-125">The volume has been fully or partially encrypted by using the hardware capabilities of the drive.</span></span><br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <span data-ttu-id="36eaf-126"><dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-126"><dt>**XTS\_AES\_128**</dt> <dt>6</dt></span></span> </dl>                                | <span data-ttu-id="36eaf-127">O volume foi totalmente ou parcialmente criptografado com XTS usando o criptografia AES (AES) e um tamanho de chave AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="36eaf-127">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 128 bits.</span></span> <span data-ttu-id="36eaf-128">Esse método só está disponível em dispositivos que executam o Windows 10, versão 1511 ou superior.</span><span class="sxs-lookup"><span data-stu-id="36eaf-128">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <span data-ttu-id="36eaf-129"><dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-129"><dt>**XTS\_AES\_256**</dt> <dt>7</dt></span></span> </dl>                                | <span data-ttu-id="36eaf-130">O volume foi totalmente ou parcialmente criptografado com XTS usando o criptografia AES (AES) e um tamanho de chave AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="36eaf-130">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 256 bits.</span></span> <span data-ttu-id="36eaf-131">Esse método só está disponível em dispositivos que executam o Windows 10, versão 1511 ou superior.</span><span class="sxs-lookup"><span data-stu-id="36eaf-131">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <dl> <span data-ttu-id="36eaf-132"><dt>(UInt32) – 1</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-132"><dt>(uint32)–1</dt></span></span> </dl>                                                                                                                                                          | <span data-ttu-id="36eaf-133">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="36eaf-133">UNKNOWN</span></span><br/> <span data-ttu-id="36eaf-134">O volume foi totalmente ou parcialmente criptografado com um algoritmo desconhecido e um tamanho de chave.</span><span class="sxs-lookup"><span data-stu-id="36eaf-134">The volume has been fully or partially encrypted with an unknown algorithm and key size.</span></span><br/>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="36eaf-135">*SelfEncryptionDriveEncryptionMethod* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="36eaf-135">*SelfEncryptionDriveEncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36eaf-136">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="36eaf-136">Type: **string**</span></span>

<span data-ttu-id="36eaf-137">O algoritmo de criptografia é configurado na unidade de criptografia automática.</span><span class="sxs-lookup"><span data-stu-id="36eaf-137">The encryption algorithm is configured on the self-encrypting drive.</span></span> <span data-ttu-id="36eaf-138">Uma cadeia de caracteres nula significa que o BitLocker está usando criptografia de software ou nenhum método de criptografia é relatado.</span><span class="sxs-lookup"><span data-stu-id="36eaf-138">A null string means that either BitLocker is using software encryption or no encryption method is reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36eaf-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36eaf-139">Return value</span></span>

<span data-ttu-id="36eaf-140">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36eaf-140">Type: **uint32**</span></span>

<span data-ttu-id="36eaf-141">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="36eaf-141">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="36eaf-142">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="36eaf-142">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="36eaf-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="36eaf-143">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="36eaf-144"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-144"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="36eaf-145">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="36eaf-145">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36eaf-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="36eaf-146">Remarks</span></span>

<span data-ttu-id="36eaf-147">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="36eaf-147">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="36eaf-148">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="36eaf-148">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="36eaf-149">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="36eaf-149">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="36eaf-150">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="36eaf-150">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36eaf-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36eaf-151">Requirements</span></span>



| <span data-ttu-id="36eaf-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="36eaf-152">Requirement</span></span> | <span data-ttu-id="36eaf-153">Valor</span><span class="sxs-lookup"><span data-stu-id="36eaf-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36eaf-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36eaf-154">Minimum supported client</span></span><br/> | <span data-ttu-id="36eaf-155">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="36eaf-155">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="36eaf-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36eaf-156">Minimum supported server</span></span><br/> | <span data-ttu-id="36eaf-157">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36eaf-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36eaf-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="36eaf-158">Namespace</span></span><br/>                | <span data-ttu-id="36eaf-159">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="36eaf-159">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="36eaf-160">MOF</span><span class="sxs-lookup"><span data-stu-id="36eaf-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36eaf-161"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36eaf-161"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36eaf-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="36eaf-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36eaf-163">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="36eaf-163">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
