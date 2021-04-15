---
description: Exporta informações que podem ajudar a recuperar dados criptografados quando a unidade está seriamente danificada e não existem arquivos de backup de dados.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Método GetKeyPackage da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761387"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="fb63a-103">Método GetKeyPackage da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="fb63a-103">GetKeyPackage method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="fb63a-104">O método **GetKeyPackage** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) exporta informações que podem ajudar a recuperar dados criptografados quando a unidade está seriamente danificada e não existem arquivos de backup de dados.</span><span class="sxs-lookup"><span data-stu-id="fb63a-104">The **GetKeyPackage** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class exports information that may help salvage encrypted data when the drive is severely damaged and no data backup files exist.</span></span>

<span data-ttu-id="fb63a-105">As informações exportadas consistem na chave de criptografia do volume protegida por um protetor de chave do tipo "senha numérica" ou "chave externa".</span><span class="sxs-lookup"><span data-stu-id="fb63a-105">The exported information consists of the volume's encryption key secured by a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="fb63a-106">Para usar esse pacote, você também deve salvar a senha numérica ou a chave externa correspondente.</span><span class="sxs-lookup"><span data-stu-id="fb63a-106">To make use of this package, you must also save the corresponding numerical password or external key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb63a-107">Se você optar por exportar um pacote de chaves, certifique-se de manter essas informações em um local bem protegido.</span><span class="sxs-lookup"><span data-stu-id="fb63a-107">If you choose to export a key package, make certain to keep this information in a well-protected location.</span></span> <span data-ttu-id="fb63a-108">Não carregue essas informações com seu computador.</span><span class="sxs-lookup"><span data-stu-id="fb63a-108">Do not carry this information with your computer.</span></span> <span data-ttu-id="fb63a-109">Se esse pacote de chaves for perdido ou roubado, você precisará descriptografar o volume e criptografá-lo novamente usando uma nova chave.</span><span class="sxs-lookup"><span data-stu-id="fb63a-109">If this key package is lost or stolen, you will need to decrypt the volume and reencrypt it by using a new key.</span></span>

 

<span data-ttu-id="fb63a-110">No caso de uma falha de unidade, a ferramenta de reparo do BitLocker existe para ajudar a recuperar os dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fb63a-110">In the event of a drive failure, the BitLocker Repair Tool exists to help salvage available data.</span></span> <span data-ttu-id="fb63a-111">Para obter mais informações sobre como essa ferramenta pode usar o pacote de chaves, consulte [como usar a ferramenta de reparo do BitLocker para ajudar a recuperar dados de um volume criptografado no Windows Vista](https://support.microsoft.com/kb/928201).</span><span class="sxs-lookup"><span data-stu-id="fb63a-111">For more information about how this tool can use the key package, see [How to use the BitLocker Repair Tool to help recover data from an encrypted volume in Windows Vista](https://support.microsoft.com/kb/928201).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb63a-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb63a-112">Syntax</span></span>


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a><span data-ttu-id="fb63a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb63a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb63a-114">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fb63a-114">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb63a-115">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fb63a-115">Type: **string**</span></span>

<span data-ttu-id="fb63a-116">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="fb63a-116">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="fb63a-117">Para exportar um pacote de chaves, você deve usar um protetor de chave do tipo "senha numérica" ou "chave externa".</span><span class="sxs-lookup"><span data-stu-id="fb63a-117">To export a key package, you must use a key protector of type "Numerical Password" or "External Key".</span></span>

</dd> <dt>

<span data-ttu-id="fb63a-118">*\[ Pacote \]* de \[out\]</span><span class="sxs-lookup"><span data-stu-id="fb63a-118">*KeyPackage\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb63a-119">Tipo: **uint8**</span><span class="sxs-lookup"><span data-stu-id="fb63a-119">Type: **uint8**</span></span>

<span data-ttu-id="fb63a-120">Um fluxo de bytes que contém a chave de criptografia para um volume, protegido pelo protetor de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="fb63a-120">A byte stream that contains the encryption key for a volume, secured by the specified key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb63a-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb63a-121">Return value</span></span>

<span data-ttu-id="fb63a-122">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fb63a-122">Type: **uint32**</span></span>

<span data-ttu-id="fb63a-123">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="fb63a-123">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="fb63a-124">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fb63a-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="fb63a-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb63a-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb63a-126"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fb63a-126"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="fb63a-127">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fb63a-127">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="fb63a-128"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="fb63a-128"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="fb63a-129">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="fb63a-129">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="fb63a-130"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="fb63a-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="fb63a-131">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="fb63a-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="fb63a-132">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fb63a-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="fb63a-133"><dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="fb63a-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="fb63a-134">O protetor de chave fornecido não existe no volume.</span><span class="sxs-lookup"><span data-stu-id="fb63a-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="fb63a-135"><dt>**FVE \_ E \_ \_ \_ tipo de protetor inválido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="fb63a-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="fb63a-136">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "senha numérica" ou "chave externa".</span><span class="sxs-lookup"><span data-stu-id="fb63a-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="fb63a-137">Use o método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para criar um protetor de chave do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="fb63a-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb63a-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb63a-138">Remarks</span></span>

<span data-ttu-id="fb63a-139">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fb63a-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fb63a-140">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="fb63a-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="fb63a-141">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="fb63a-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fb63a-142">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="fb63a-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb63a-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb63a-143">Requirements</span></span>



| <span data-ttu-id="fb63a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb63a-144">Requirement</span></span> | <span data-ttu-id="fb63a-145">Valor</span><span class="sxs-lookup"><span data-stu-id="fb63a-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb63a-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb63a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fb63a-147">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="fb63a-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fb63a-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb63a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fb63a-149">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb63a-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb63a-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb63a-150">Namespace</span></span><br/>                | <span data-ttu-id="fb63a-151">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="fb63a-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="fb63a-152">MOF</span><span class="sxs-lookup"><span data-stu-id="fb63a-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb63a-153"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb63a-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb63a-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb63a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb63a-155">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="fb63a-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
