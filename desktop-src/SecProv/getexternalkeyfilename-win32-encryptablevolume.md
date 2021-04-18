---
description: Retorna o nome do arquivo que contém a chave externa.
ms.assetid: c02d8dca-f30b-4ab5-a770-1ec6ac0b81c6
title: Método GetExternalKeyFileName da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFileName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bf8de41befa7414c9970ac451d34ee7c5f40dd84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761850"
---
# <a name="getexternalkeyfilename-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="41fa2-103">Método GetExternalKeyFileName da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="41fa2-103">GetExternalKeyFileName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="41fa2-104">O método **GetExternalKeyFileName** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) retorna o nome do arquivo que contém a chave externa, se essa chave externa for salva em um local de arquivo usando o método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="41fa2-104">The **GetExternalKeyFileName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the name of the file that contains the external key, if this external key is saved to a file location by using the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="41fa2-105">Esse método só é aplicável para protetores de chave do tipo "chave externa", "TPM e PIN e chave de inicialização", ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="41fa2-105">This method is only applicable for key protectors of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="41fa2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41fa2-106">Syntax</span></span>


```mof
uint32 GetExternalKeyFileName(
  [in]  string VolumeKeyProtectorID,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="41fa2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41fa2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41fa2-108">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41fa2-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41fa2-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41fa2-109">Type: **string**</span></span>

<span data-ttu-id="41fa2-110">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="41fa2-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="41fa2-111">*Nome do arquivo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="41fa2-111">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41fa2-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41fa2-112">Type: **string**</span></span>

<span data-ttu-id="41fa2-113">Uma cadeia de caracteres que especifica o nome com a extensão, mas sem o caminho do arquivo, que contém a chave externa.</span><span class="sxs-lookup"><span data-stu-id="41fa2-113">A string that specifies the name with extension but without the file path, of the file that contains the external key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41fa2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41fa2-114">Return value</span></span>

<span data-ttu-id="41fa2-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41fa2-115">Type: **uint32**</span></span>

<span data-ttu-id="41fa2-116">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="41fa2-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="41fa2-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="41fa2-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="41fa2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="41fa2-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="41fa2-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="41fa2-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="41fa2-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="41fa2-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="41fa2-121"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="41fa2-121"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="41fa2-122">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "chave externa", "TPM e PIN e chave de inicialização", ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="41fa2-122">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="41fa2-123"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="41fa2-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="41fa2-124">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="41fa2-124">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="41fa2-125"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="41fa2-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="41fa2-126">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="41fa2-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="41fa2-127">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="41fa2-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="41fa2-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="41fa2-128">Remarks</span></span>

<span data-ttu-id="41fa2-129">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="41fa2-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="41fa2-130">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="41fa2-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="41fa2-131">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="41fa2-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="41fa2-132">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="41fa2-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41fa2-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41fa2-133">Requirements</span></span>



| <span data-ttu-id="41fa2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="41fa2-134">Requirement</span></span> | <span data-ttu-id="41fa2-135">Valor</span><span class="sxs-lookup"><span data-stu-id="41fa2-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41fa2-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41fa2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="41fa2-137">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="41fa2-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="41fa2-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41fa2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="41fa2-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41fa2-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41fa2-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="41fa2-140">Namespace</span></span><br/>                | <span data-ttu-id="41fa2-141">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="41fa2-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="41fa2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="41fa2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41fa2-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41fa2-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41fa2-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="41fa2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fa2-145">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="41fa2-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="41fa2-146">**SaveExternalKeyToFile**</span><span class="sxs-lookup"><span data-stu-id="41fa2-146">**SaveExternalKeyToFile**</span></span>](saveexternalkeytofile-win32-encryptablevolume.md)
</dt> </dl>

 

 
