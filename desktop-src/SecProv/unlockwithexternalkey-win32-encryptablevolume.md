---
description: Usa uma chave externa fornecida para acessar o conteúdo de um volume de dados.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Método UnlockWithExternalKey da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749456"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4cd1c-103">Método UnlockWithExternalKey da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="4cd1c-103">UnlockWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4cd1c-104">O método **UnlockWithExternalKey** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa uma chave externa fornecida para acessar o conteúdo de um volume de dados.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-104">The **UnlockWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided external key to access the contents of a data volume.</span></span>

<span data-ttu-id="4cd1c-105">A chave de criptografia do volume deve ter sido protegida com um ou mais protetores de chave do tipo "chave externa" usando o método [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para poder desbloquear o volume com esse método.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-105">The volume's encryption key must have been secured with one or more key protectors of the type "External Key" using the [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="4cd1c-106">Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "</span><span class="sxs-lookup"><span data-stu-id="4cd1c-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4cd1c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cd1c-107">Syntax</span></span>


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="4cd1c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cd1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd1c-109">*ExternalKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cd1c-109">*ExternalKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd1c-110">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="4cd1c-110">Type: **uint8\[\]**</span></span>

<span data-ttu-id="4cd1c-111">Uma matriz de bytes que especifica a chave externa de 256 bits usada para desbloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-111">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span> <span data-ttu-id="4cd1c-112">Essa chave pode ser obtida chamando o método [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd1c-112">This key can be obtained by calling the [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd1c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4cd1c-113">Return value</span></span>

<span data-ttu-id="4cd1c-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4cd1c-114">Type: **uint32**</span></span>

<span data-ttu-id="4cd1c-115">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-115">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="4cd1c-116">Se o volume já estiver desbloqueado, esse método retornará 0.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-116">If the volume is already unlocked, this method returns 0.</span></span>



| <span data-ttu-id="4cd1c-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4cd1c-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="4cd1c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cd1c-118">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cd1c-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd1c-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="4cd1c-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-120">The method was successful.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="4cd1c-121"><dt>**Erro \_ do Não \_ encontrado**</dt> <dt>nenhum valor fornecido (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd1c-121"><dt>**ERROR\_NOT\_FOUND**</dt> <dt>No value given (0x)</dt></span></span> </dl>          | <span data-ttu-id="4cd1c-122">O volume não tem um protetor de chave do tipo "chave externa".</span><span class="sxs-lookup"><span data-stu-id="4cd1c-122">The volume does not have a key protector of the type "External Key".</span></span><br/>                                                             |
| <dl> <span data-ttu-id="4cd1c-123"><dt>**Erro \_ do \_Senha inválida**</dt> <dt>nenhum valor fornecido (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd1c-123"><dt>**ERROR\_INVALID\_PASSWORD**</dt> <dt>No value given (0x)</dt></span></span> </dl>   | <span data-ttu-id="4cd1c-124">Existe um ou mais protetores de chave do tipo "chave externa", mas o parâmetro *ExternalKey* especificado não pode desbloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-124">One or more key protectors of the type "External Key" exist, but the specified *ExternalKey* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="4cd1c-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd1c-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="4cd1c-126">O parâmetro *ExternalKey* não é uma matriz de tamanho 4.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-126">The *ExternalKey* parameter is not an array of size 4.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="4cd1c-127"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd1c-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="4cd1c-128">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="4cd1c-129">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="4cd1c-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cd1c-130">Remarks</span></span>

<span data-ttu-id="4cd1c-131">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4cd1c-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4cd1c-132">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4cd1c-133">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4cd1c-134">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4cd1c-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd1c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cd1c-135">Requirements</span></span>



| <span data-ttu-id="4cd1c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cd1c-136">Requirement</span></span> | <span data-ttu-id="4cd1c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="4cd1c-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd1c-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cd1c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4cd1c-139">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="4cd1c-139">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4cd1c-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cd1c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4cd1c-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4cd1c-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4cd1c-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="4cd1c-142">Namespace</span></span><br/>                | <span data-ttu-id="4cd1c-143">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="4cd1c-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4cd1c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4cd1c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cd1c-145"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4cd1c-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd1c-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cd1c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd1c-147">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="4cd1c-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
