---
description: Grava a chave externa associada ao protetor de chave de volume especificado em um arquivo de sistema, oculto e somente leitura na pasta especificada.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Método SaveExternalKeyToFile da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762903"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="20956-103">Método SaveExternalKeyToFile da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="20956-103">SaveExternalKeyToFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="20956-104">O método **SaveExternalKeyToFile** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) grava a chave externa associada ao protetor de chave de volume especificado em um arquivo de sistema, oculto e somente leitura na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="20956-104">The **SaveExternalKeyToFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class writes the external key associated with the specified volume key protector to a system, hidden, read-only file in the specified folder.</span></span>

<span data-ttu-id="20956-105">Esse método só é aplicável a protetores de chave do tipo "chave externa" ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="20956-105">This method is only applicable for key protectors of the type "External Key" or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="20956-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20956-106">Syntax</span></span>


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a><span data-ttu-id="20956-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20956-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20956-108">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20956-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20956-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20956-109">Type: **string**</span></span>

<span data-ttu-id="20956-110">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="20956-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="20956-111">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="20956-111">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20956-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20956-112">Type: **string**</span></span>

<span data-ttu-id="20956-113">Uma cadeia de caracteres que contém o local do volume ou da pasta onde a chave externa associada ao protetor de chave especificado deve ser salva.</span><span class="sxs-lookup"><span data-stu-id="20956-113">A string that contains the volume or folder location where the external key associated with the specified key protector is to be saved.</span></span> <span data-ttu-id="20956-114">Esse caminho não inclui o nome do arquivo, que é interno e pode ser alterado de versão para versão.</span><span class="sxs-lookup"><span data-stu-id="20956-114">This path does not include the name of the file, which is internal and may change from version to version.</span></span> <span data-ttu-id="20956-115">Use **GetExternalKeyFileName** para obter o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="20956-115">Use **GetExternalKeyFileName** to get the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20956-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20956-116">Return value</span></span>

<span data-ttu-id="20956-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20956-117">Type: **uint32**</span></span>

<span data-ttu-id="20956-118">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="20956-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="20956-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="20956-119">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="20956-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="20956-120">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20956-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="20956-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="20956-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="20956-122">The method was successful.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="20956-123"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="20956-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>  | <span data-ttu-id="20956-124">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="20956-124">The volume is locked.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="20956-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="20956-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="20956-126">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "chave externa" ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="20956-126">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key" or "TPM And Startup Key".</span></span><br/>            |
| <dl> <span data-ttu-id="20956-127"><dt>**Erro \_ do CAMINHO \_ não \_ encontrado**</dt> <dt>2147942403 (0x80070003)</dt></span><span class="sxs-lookup"><span data-stu-id="20956-127"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt> <dt>2147942403 (0x80070003)</dt></span></span> </dl> | <span data-ttu-id="20956-128">O parâmetro *path* não se refere a um local válido.</span><span class="sxs-lookup"><span data-stu-id="20956-128">The *Path* parameter does not refer to a valid location.</span></span><br/> <span data-ttu-id="20956-129">Verifique se o nome do arquivo não está incluído no parâmetro *path* .</span><span class="sxs-lookup"><span data-stu-id="20956-129">Ensure that the file name is not included in the *Path* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="20956-130"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="20956-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="20956-131">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="20956-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="20956-132">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="20956-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="20956-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="20956-133">Remarks</span></span>

<span data-ttu-id="20956-134">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="20956-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="20956-135">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="20956-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="20956-136">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="20956-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="20956-137">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="20956-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20956-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20956-138">Requirements</span></span>



| <span data-ttu-id="20956-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="20956-139">Requirement</span></span> | <span data-ttu-id="20956-140">Valor</span><span class="sxs-lookup"><span data-stu-id="20956-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20956-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20956-141">Minimum supported client</span></span><br/> | <span data-ttu-id="20956-142">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="20956-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="20956-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20956-143">Minimum supported server</span></span><br/> | <span data-ttu-id="20956-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20956-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20956-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="20956-145">Namespace</span></span><br/>                | <span data-ttu-id="20956-146">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="20956-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="20956-147">MOF</span><span class="sxs-lookup"><span data-stu-id="20956-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20956-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20956-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20956-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="20956-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20956-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="20956-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
