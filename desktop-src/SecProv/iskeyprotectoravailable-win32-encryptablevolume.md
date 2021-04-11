---
description: Indica se os protetores estão disponíveis para o volume.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Método IsKeyProtectorAvailable da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164389"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5a539-103">Método IsKeyProtectorAvailable da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="5a539-103">IsKeyProtectorAvailable method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5a539-104">O método **IsKeyProtectorAvailable** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se os protetores estão disponíveis para o volume.</span><span class="sxs-lookup"><span data-stu-id="5a539-104">The **IsKeyProtectorAvailable** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether protectors are available for the volume.</span></span>

<span data-ttu-id="5a539-105">Se um tipo de protetor for fornecido, o método indicará se os protetores do tipo especificado estão disponíveis para o volume.</span><span class="sxs-lookup"><span data-stu-id="5a539-105">If a protector type is provided, then the method indicates whether protectors of the specified type are available for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a539-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a539-106">Syntax</span></span>


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="5a539-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a539-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a539-108">*Keyprotetortype* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5a539-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a539-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a539-109">Type: **uint32**</span></span>

<span data-ttu-id="5a539-110">Um inteiro sem sinal que indica o tipo de protetor de chave de volume consultado.</span><span class="sxs-lookup"><span data-stu-id="5a539-110">An unsigned integer that indicates the type of volume key protector queried.</span></span>

<span data-ttu-id="5a539-111">Se esse parâmetro não for especificado, todos os protetores de chave disponíveis do volume serão consultados.</span><span class="sxs-lookup"><span data-stu-id="5a539-111">If this parameter is not specified, all available key protectors of the volume are queried.</span></span>



| <span data-ttu-id="5a539-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5a539-112">Value</span></span>                                                                         | <span data-ttu-id="5a539-113">Significado</span><span class="sxs-lookup"><span data-stu-id="5a539-113">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a539-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="5a539-115">Todos os tipos.</span><span class="sxs-lookup"><span data-stu-id="5a539-115">All types.</span></span><br/> <span data-ttu-id="5a539-116">Todos os protetores de chave são consultados.</span><span class="sxs-lookup"><span data-stu-id="5a539-116">All key protectors are queried.</span></span><br/> |
| <dl> <span data-ttu-id="5a539-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="5a539-118">Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="5a539-118">Trusted Platform Module (TPM).</span></span><br/>                        |
| <dl> <span data-ttu-id="5a539-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="5a539-120">Chave externa.</span><span class="sxs-lookup"><span data-stu-id="5a539-120">External key.</span></span><br/>                                         |
| <dl> <span data-ttu-id="5a539-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="5a539-122">Senha numérica.</span><span class="sxs-lookup"><span data-stu-id="5a539-122">Numerical password.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5a539-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="5a539-124">TPM e PIN.</span><span class="sxs-lookup"><span data-stu-id="5a539-124">TPM And PIN.</span></span><br/>                                          |
| <dl> <span data-ttu-id="5a539-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="5a539-126">TPM e chave de inicialização.</span><span class="sxs-lookup"><span data-stu-id="5a539-126">TPM And Startup Key.</span></span><br/>                                  |
| <dl> <span data-ttu-id="5a539-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="5a539-128">TPM e PIN e chave de inicialização.</span><span class="sxs-lookup"><span data-stu-id="5a539-128">TPM And PIN And Startup Key.</span></span><br/>                          |
| <dl> <span data-ttu-id="5a539-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="5a539-130">Chave pública.</span><span class="sxs-lookup"><span data-stu-id="5a539-130">Public Key.</span></span><br/>                                           |
| <dl> <span data-ttu-id="5a539-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="5a539-132">Senha.</span><span class="sxs-lookup"><span data-stu-id="5a539-132">Passphrase.</span></span><br/>                                           |
| <dl> <span data-ttu-id="5a539-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="5a539-134">Certificado TPM</span><span class="sxs-lookup"><span data-stu-id="5a539-134">TPM Certificate</span></span><br/>                                       |
| <dl> <span data-ttu-id="5a539-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="5a539-136">Identificador de segurança (SID)</span><span class="sxs-lookup"><span data-stu-id="5a539-136">Security Identifier (SID)</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="5a539-137">*IsKeyProtectorAvailable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5a539-137">*IsKeyProtectorAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a539-138">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a539-138">Type: **boolean**</span></span>

<span data-ttu-id="5a539-139">Um valor booliano que indica se um protetor de chave de volume do tipo especificado existe no volume.</span><span class="sxs-lookup"><span data-stu-id="5a539-139">A Boolean value that indicates whether a volume key protector of the specified type exists on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a539-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a539-140">Return value</span></span>

<span data-ttu-id="5a539-141">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a539-141">Type: **uint32**</span></span>

<span data-ttu-id="5a539-142">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="5a539-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5a539-143">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5a539-143">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="5a539-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a539-144">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a539-145"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                         | <span data-ttu-id="5a539-146">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5a539-146">The method was successful.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="5a539-147"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl> | <span data-ttu-id="5a539-148">O parâmetro *Keyprotetortype* é especificado, mas não se refere a um tipo de protetor de chave válido.</span><span class="sxs-lookup"><span data-stu-id="5a539-148">The *KeyProtectorType* parameter is specified but does not refer to a valid key protector type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a539-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a539-149">Remarks</span></span>

<span data-ttu-id="5a539-150">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5a539-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5a539-151">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="5a539-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5a539-152">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="5a539-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5a539-153">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5a539-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a539-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a539-154">Requirements</span></span>



| <span data-ttu-id="5a539-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a539-155">Requirement</span></span> | <span data-ttu-id="5a539-156">Valor</span><span class="sxs-lookup"><span data-stu-id="5a539-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a539-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a539-157">Minimum supported client</span></span><br/> | <span data-ttu-id="5a539-158">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="5a539-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5a539-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a539-159">Minimum supported server</span></span><br/> | <span data-ttu-id="5a539-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a539-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a539-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a539-161">Namespace</span></span><br/>                | <span data-ttu-id="5a539-162">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5a539-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5a539-163">MOF</span><span class="sxs-lookup"><span data-stu-id="5a539-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a539-164"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a539-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a539-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a539-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a539-166">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5a539-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
