---
description: Lista os protetores usados para proteger a chave de criptografia do volume.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Método GetKeyProtectors da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811039"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c7f81-103">Método GetKeyProtectors da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="c7f81-103">GetKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c7f81-104">O método **GetKeyProtectors** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) lista os protetores usados para proteger a chave de criptografia do volume.</span><span class="sxs-lookup"><span data-stu-id="c7f81-104">The **GetKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class lists the protectors used to secure the volume's encryption key.</span></span> <span data-ttu-id="c7f81-105">Se um tipo de protetor for fornecido, somente os protetores de chave de volume do tipo especificado serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c7f81-105">If a protector type is provided, then only volume key protectors of the specified type are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f81-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7f81-106">Syntax</span></span>


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a><span data-ttu-id="c7f81-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7f81-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7f81-108">*Keyprotetortype* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c7f81-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f81-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f81-109">Type: **uint32**</span></span>

<span data-ttu-id="c7f81-110">Um inteiro sem sinal que especifica o tipo de protetor de chave a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="c7f81-110">An unsigned integer that specifies the type of key protector to return.</span></span>

<span data-ttu-id="c7f81-111">Se esse parâmetro não for especificado, todos os protetores de chave disponíveis do volume serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c7f81-111">If this parameter is not specified, all available key protectors of the volume are returned.</span></span>



| <span data-ttu-id="c7f81-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c7f81-112">Value</span></span>                                                                         | <span data-ttu-id="c7f81-113">Significado</span><span class="sxs-lookup"><span data-stu-id="c7f81-113">Meaning</span></span>                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7f81-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="c7f81-115">Todos os tipos.</span><span class="sxs-lookup"><span data-stu-id="c7f81-115">All types.</span></span><br/> <span data-ttu-id="c7f81-116">Todos os protetores de chave são retornados.</span><span class="sxs-lookup"><span data-stu-id="c7f81-116">All key protectors are returned.</span></span><br/> |
| <dl> <span data-ttu-id="c7f81-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="c7f81-118">Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="c7f81-118">Trusted Platform Module (TPM).</span></span><br/>                         |
| <dl> <span data-ttu-id="c7f81-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="c7f81-120">Chave externa.</span><span class="sxs-lookup"><span data-stu-id="c7f81-120">External key.</span></span><br/>                                          |
| <dl> <span data-ttu-id="c7f81-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="c7f81-122">Senha numérica.</span><span class="sxs-lookup"><span data-stu-id="c7f81-122">Numeric password.</span></span><br/>                                      |
| <dl> <span data-ttu-id="c7f81-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="c7f81-124">TPM e PIN.</span><span class="sxs-lookup"><span data-stu-id="c7f81-124">TPM And PIN.</span></span><br/>                                           |
| <dl> <span data-ttu-id="c7f81-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="c7f81-126">TPM e chave de inicialização.</span><span class="sxs-lookup"><span data-stu-id="c7f81-126">TPM And Startup Key.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c7f81-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="c7f81-128">TPM e PIN e chave de inicialização.</span><span class="sxs-lookup"><span data-stu-id="c7f81-128">TPM And PIN And Startup Key.</span></span><br/>                           |
| <dl> <span data-ttu-id="c7f81-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="c7f81-130">Chave pública.</span><span class="sxs-lookup"><span data-stu-id="c7f81-130">Public Key.</span></span><br/>                                            |
| <dl> <span data-ttu-id="c7f81-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="c7f81-132">Senha.</span><span class="sxs-lookup"><span data-stu-id="c7f81-132">Passphrase.</span></span><br/>                                            |
| <dl> <span data-ttu-id="c7f81-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="c7f81-134">Certificado TPM</span><span class="sxs-lookup"><span data-stu-id="c7f81-134">TPM Certificate</span></span><br/>                                        |
| <dl> <span data-ttu-id="c7f81-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="c7f81-136">Identificador de segurança (SID)</span><span class="sxs-lookup"><span data-stu-id="c7f81-136">Security Identifier (SID)</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="c7f81-137">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c7f81-137">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f81-138">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7f81-138">Type: **string\[\]**</span></span>

<span data-ttu-id="c7f81-139">Uma matriz de cadeias de caracteres que identifica os protetores de chave usados para proteger a chave de criptografia do volume.</span><span class="sxs-lookup"><span data-stu-id="c7f81-139">An array of strings that identify the key protectors used to secure the volume's encryption key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7f81-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7f81-140">Return value</span></span>

<span data-ttu-id="c7f81-141">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f81-141">Type: **uint32**</span></span>

<span data-ttu-id="c7f81-142">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="c7f81-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c7f81-143">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c7f81-143">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="c7f81-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7f81-144">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7f81-145"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="c7f81-146">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c7f81-146">The method was successful.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="c7f81-147"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="c7f81-148">O parâmetro *VolumeKeyProtectorID* é especificado, mas não se refere a um *keyprotetortype* válido.</span><span class="sxs-lookup"><span data-stu-id="c7f81-148">The *VolumeKeyProtectorID* parameter is specified but does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="c7f81-149"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-149"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="c7f81-150">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="c7f81-150">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c7f81-151">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c7f81-151">Add a key protector to enable BitLocker.</span></span> <br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="c7f81-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7f81-152">Remarks</span></span>

<span data-ttu-id="c7f81-153">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c7f81-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c7f81-154">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="c7f81-154">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c7f81-155">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c7f81-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c7f81-156">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c7f81-156">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7f81-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7f81-157">Requirements</span></span>



| <span data-ttu-id="c7f81-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7f81-158">Requirement</span></span> | <span data-ttu-id="c7f81-159">Valor</span><span class="sxs-lookup"><span data-stu-id="c7f81-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f81-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7f81-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c7f81-161">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="c7f81-161">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c7f81-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7f81-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c7f81-163">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7f81-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7f81-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7f81-164">Namespace</span></span><br/>                | <span data-ttu-id="c7f81-165">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c7f81-165">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c7f81-166">MOF</span><span class="sxs-lookup"><span data-stu-id="c7f81-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7f81-167"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7f81-167"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7f81-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7f81-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f81-169">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="c7f81-169">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
