---
description: Indica se o conteúdo do volume pode ser acessado do Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Método GetLockStatus da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757989"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6a81b-103">Método GetLockStatus da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="6a81b-103">GetLockStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6a81b-104">O método **GetLockStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se o conteúdo do volume pode ser acessado do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a81b-104">The **GetLockStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the contents of the volume are accessible from Windows.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a81b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a81b-105">Syntax</span></span>


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6a81b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a81b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a81b-107">*LockStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6a81b-107">*LockStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a81b-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a81b-108">Type: **uint32**</span></span>

<span data-ttu-id="6a81b-109">Especifica se o conteúdo do volume pode ser acessado do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a81b-109">Specifies whether the contents of the volume are accessible from Windows.</span></span>



| <span data-ttu-id="6a81b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6a81b-110">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="6a81b-111">Significado</span><span class="sxs-lookup"><span data-stu-id="6a81b-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <span data-ttu-id="6a81b-112"><dt>**Desbloqueado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6a81b-112"><dt>**Unlocked**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="6a81b-113">Para um HDD padrão:</span><span class="sxs-lookup"><span data-stu-id="6a81b-113">For a standard HDD:</span></span><br/> <span data-ttu-id="6a81b-114">O conteúdo completo do volume pode ser acessado.</span><span class="sxs-lookup"><span data-stu-id="6a81b-114">The full contents of the volume are accessible.</span></span> <span data-ttu-id="6a81b-115">Um volume desbloqueado está totalmente descriptografado ou tem a chave de criptografia disponível em apagar no disco.</span><span class="sxs-lookup"><span data-stu-id="6a81b-115">An unlocked volume is either fully decrypted or has the encryption key available in the clear on disk.</span></span> <span data-ttu-id="6a81b-116">O volume que contém o sistema operacional em execução atual (por exemplo, o volume do Windows em execução) é sempre acessível e não pode ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6a81b-116">The volume containing the current running operating system (for example, the running Windows volume) is always accessible and cannot be locked.</span></span><br/> <span data-ttu-id="6a81b-117">Para um EHDD:</span><span class="sxs-lookup"><span data-stu-id="6a81b-117">For an EHDD:</span></span><br/> <span data-ttu-id="6a81b-118">A banda é desbloqueada perpétuamente.</span><span class="sxs-lookup"><span data-stu-id="6a81b-118">The band is perpetually unlocked.</span></span><br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <span data-ttu-id="6a81b-119"><dt>**Bloqueado**</dt> em <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6a81b-119"><dt>**Locked**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="6a81b-120">Para um HDD padrão:</span><span class="sxs-lookup"><span data-stu-id="6a81b-120">For a standard HDD:</span></span><br/> <span data-ttu-id="6a81b-121">Toda ou uma parte do conteúdo do volume não está acessível.</span><span class="sxs-lookup"><span data-stu-id="6a81b-121">All or a portion of the contents of the volume are not accessible.</span></span> <span data-ttu-id="6a81b-122">Um volume bloqueado deve ser parcialmente ou totalmente criptografado e não deve ter a chave de criptografia disponível no disco não criptografado.</span><span class="sxs-lookup"><span data-stu-id="6a81b-122">A locked volume must be partially or fully encrypted and must not have the encryption key available in the clear on disk.</span></span><br/> <span data-ttu-id="6a81b-123">Para um EHDD:</span><span class="sxs-lookup"><span data-stu-id="6a81b-123">For an EHDD:</span></span><br/> <span data-ttu-id="6a81b-124">A banda está desbloqueada ou bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6a81b-124">The band is unlocked or locked.</span></span><br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a81b-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a81b-125">Return value</span></span>

<span data-ttu-id="6a81b-126">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a81b-126">Type: **uint32**</span></span>

<span data-ttu-id="6a81b-127">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="6a81b-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6a81b-128">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6a81b-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="6a81b-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a81b-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6a81b-130"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6a81b-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6a81b-131">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6a81b-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a81b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a81b-132">Remarks</span></span>

<span data-ttu-id="6a81b-133">Use [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) e [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para obter acesso ao conteúdo do volume.</span><span class="sxs-lookup"><span data-stu-id="6a81b-133">Use the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) and [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) to get access to the volume contents.</span></span> <span data-ttu-id="6a81b-134">Use o método [**Lock**](lock-win32-encryptablevolume.md) para ceder o acesso ao conteúdo do volume.</span><span class="sxs-lookup"><span data-stu-id="6a81b-134">Use the [**Lock**](lock-win32-encryptablevolume.md) method to relinquish access to volume contents.</span></span>

<span data-ttu-id="6a81b-135">O volume que contém o sistema operacional em execução no momento é sempre acessível e não pode ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6a81b-135">The volume that contains the currently running operating system is always accessible and cannot be locked.</span></span>

<span data-ttu-id="6a81b-136">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6a81b-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6a81b-137">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a81b-137">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6a81b-138">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6a81b-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6a81b-139">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6a81b-139">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a81b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a81b-140">Requirements</span></span>



| <span data-ttu-id="6a81b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a81b-141">Requirement</span></span> | <span data-ttu-id="6a81b-142">Valor</span><span class="sxs-lookup"><span data-stu-id="6a81b-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a81b-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a81b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6a81b-144">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="6a81b-144">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6a81b-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a81b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6a81b-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a81b-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6a81b-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a81b-147">Namespace</span></span><br/>                | <span data-ttu-id="6a81b-148">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="6a81b-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6a81b-149">MOF</span><span class="sxs-lookup"><span data-stu-id="6a81b-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a81b-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a81b-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a81b-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a81b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a81b-152">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6a81b-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
