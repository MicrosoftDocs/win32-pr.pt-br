---
description: Indica o tipo de um protetor de chave fornecido.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Método GetKeyProtectorType da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506105"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a72fd-103">Método GetKeyProtectorType da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="a72fd-103">GetKeyProtectorType method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a72fd-104">O método **GetKeyProtectorType** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica o tipo de um protetor de chave específico.</span><span class="sxs-lookup"><span data-stu-id="a72fd-104">The **GetKeyProtectorType** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the type of a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a72fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a72fd-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a><span data-ttu-id="a72fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a72fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a72fd-107">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a72fd-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a72fd-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a72fd-108">Type: **string**</span></span>

<span data-ttu-id="a72fd-109">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="a72fd-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="a72fd-110">*Keyprotetortype* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a72fd-110">*KeyProtectorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a72fd-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a72fd-111">Type: **uint32**</span></span>

<span data-ttu-id="a72fd-112">Um inteiro sem sinal que especifica o tipo do protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="a72fd-112">An unsigned integer that specifies the type of the key protector.</span></span>



| <span data-ttu-id="a72fd-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a72fd-113">Value</span></span>                                                                         | <span data-ttu-id="a72fd-114">Significado</span><span class="sxs-lookup"><span data-stu-id="a72fd-114">Meaning</span></span>                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a72fd-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-115"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="a72fd-116">Tipo de protetor desconhecido ou outro</span><span class="sxs-lookup"><span data-stu-id="a72fd-116">Unknown or other protector type</span></span><br/>           |
| <dl> <span data-ttu-id="a72fd-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="a72fd-118">TPM (Trusted Platform Module)</span><span class="sxs-lookup"><span data-stu-id="a72fd-118">Trusted Platform Module (TPM)</span></span><br/>             |
| <dl> <span data-ttu-id="a72fd-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="a72fd-120">Chave externa</span><span class="sxs-lookup"><span data-stu-id="a72fd-120">External key</span></span><br/>                              |
| <dl> <span data-ttu-id="a72fd-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="a72fd-122">Senha numérica</span><span class="sxs-lookup"><span data-stu-id="a72fd-122">Numerical password</span></span><br/>                        |
| <dl> <span data-ttu-id="a72fd-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="a72fd-124">TPM e PIN</span><span class="sxs-lookup"><span data-stu-id="a72fd-124">TPM And PIN</span></span><br/>                               |
| <dl> <span data-ttu-id="a72fd-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="a72fd-126">TPM e chave de inicialização</span><span class="sxs-lookup"><span data-stu-id="a72fd-126">TPM And Startup Key</span></span><br/>                       |
| <dl> <span data-ttu-id="a72fd-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="a72fd-128">TPM e PIN e chave de inicialização</span><span class="sxs-lookup"><span data-stu-id="a72fd-128">TPM And PIN And Startup Key</span></span><br/>               |
| <dl> <span data-ttu-id="a72fd-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="a72fd-130">Chave pública</span><span class="sxs-lookup"><span data-stu-id="a72fd-130">Public Key</span></span><br/>                                |
| <dl> <span data-ttu-id="a72fd-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="a72fd-132">Senha</span><span class="sxs-lookup"><span data-stu-id="a72fd-132">Passphrase</span></span><br/>                                |
| <dl> <span data-ttu-id="a72fd-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="a72fd-134">Certificado TPM</span><span class="sxs-lookup"><span data-stu-id="a72fd-134">TPM Certificate</span></span><br/>                           |
| <dl> <span data-ttu-id="a72fd-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="a72fd-136">Protetor de CNG (CryptoAPI Next Generation)</span><span class="sxs-lookup"><span data-stu-id="a72fd-136">CryptoAPI Next Generation (CNG) Protector</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a72fd-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a72fd-137">Return value</span></span>

<span data-ttu-id="a72fd-138">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a72fd-138">Type: **uint32**</span></span>

<span data-ttu-id="a72fd-139">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="a72fd-139">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="a72fd-140">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a72fd-140">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="a72fd-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="a72fd-141">Description</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a72fd-142"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-142"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="a72fd-143">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a72fd-143">The method was successful.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="a72fd-144"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-144"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="a72fd-145">O parâmetro *VolumeKeyProtectorID* não se refere a um *keyprotetortype* válido.</span><span class="sxs-lookup"><span data-stu-id="a72fd-145">The *VolumeKeyProtectorID* parameter does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="a72fd-146"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-146"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="a72fd-147">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="a72fd-147">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="a72fd-148">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a72fd-148">Add a key protector to enable BitLocker.</span></span> <br/>  |



 

## <a name="remarks"></a><span data-ttu-id="a72fd-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="a72fd-149">Remarks</span></span>

<span data-ttu-id="a72fd-150">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a72fd-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a72fd-151">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="a72fd-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a72fd-152">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a72fd-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a72fd-153">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a72fd-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a72fd-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a72fd-154">Requirements</span></span>



| <span data-ttu-id="a72fd-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="a72fd-155">Requirement</span></span> | <span data-ttu-id="a72fd-156">Valor</span><span class="sxs-lookup"><span data-stu-id="a72fd-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72fd-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a72fd-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a72fd-158">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="a72fd-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a72fd-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a72fd-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a72fd-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a72fd-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a72fd-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="a72fd-161">Namespace</span></span><br/>                | <span data-ttu-id="a72fd-162">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="a72fd-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a72fd-163">MOF</span><span class="sxs-lookup"><span data-stu-id="a72fd-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a72fd-164"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a72fd-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a72fd-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="a72fd-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a72fd-166">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="a72fd-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
