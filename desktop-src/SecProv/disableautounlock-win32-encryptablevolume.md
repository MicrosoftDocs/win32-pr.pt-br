---
description: Remove a chave externa salva no volume do sistema operacional em execução no momento.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Método DisableAutoUnlock da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828547"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="df90e-103">Método DisableAutoUnlock da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="df90e-103">DisableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="df90e-104">O método **DisableAutoUnlock** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) remove a chave externa salva no volume do sistema operacional em execução no momento para que um volume de dados não seja desbloqueado automaticamente quando montado, como quando os dispositivos de memória removível estão conectados ao computador.</span><span class="sxs-lookup"><span data-stu-id="df90e-104">The **DisableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes the external key saved onto the currently running operating system volume so that a data volume is not automatically unlocked when it is mounted, such as when removable memory devices are connected to the computer.</span></span>

<span data-ttu-id="df90e-105">Se o desbloqueio automático estiver desabilitado ou suspenso, os métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) deverão ser usados para desbloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="df90e-105">If automatic unlocking is disabled or suspended, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) must be used to unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="df90e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df90e-106">Syntax</span></span>


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a><span data-ttu-id="df90e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df90e-107">Parameters</span></span>

<span data-ttu-id="df90e-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="df90e-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df90e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df90e-109">Return value</span></span>

<span data-ttu-id="df90e-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df90e-110">Type: **uint32**</span></span>

<span data-ttu-id="df90e-111">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="df90e-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="df90e-112">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="df90e-112">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="df90e-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="df90e-113">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df90e-114"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="df90e-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="df90e-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="df90e-115">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="df90e-116"><dt> **FVE \_ E \_ volume \_ não \_ associado**</dt> <dt>2150694935 (0x80310017)</dt></span><span class="sxs-lookup"><span data-stu-id="df90e-116"><dt>**FVE\_E\_VOLUME\_NOT\_BOUND** </dt> <dt>2150694935 (0x80310017)</dt></span></span> </dl> | <span data-ttu-id="df90e-117">O desbloqueio automático no volume está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="df90e-117">Automatic unlocking on the volume is disabled.</span></span><br/>                                   |
| <dl> <span data-ttu-id="df90e-118"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="df90e-118"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>      | <span data-ttu-id="df90e-119">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="df90e-119">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="df90e-120">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="df90e-120">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="df90e-121"><dt>**FVE \_ E \_ não \_ \_ VOLUME de dados**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="df90e-121"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>   | <span data-ttu-id="df90e-122">O método não pode ser executado para o volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="df90e-122">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="df90e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="df90e-123">Remarks</span></span>

<span data-ttu-id="df90e-124">Se nenhum erro for retornado, esse método removerá do registro quaisquer IDs de protetor de volume e chaves externas usadas para desbloquear automaticamente o volume.</span><span class="sxs-lookup"><span data-stu-id="df90e-124">If no errors are returned, this method removes from the registry any volume protector IDs and external keys used to automatically unlock the volume.</span></span>

<span data-ttu-id="df90e-125">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="df90e-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="df90e-126">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="df90e-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="df90e-127">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="df90e-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="df90e-128">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="df90e-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df90e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df90e-129">Requirements</span></span>



| <span data-ttu-id="df90e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="df90e-130">Requirement</span></span> | <span data-ttu-id="df90e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="df90e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df90e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df90e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="df90e-133">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="df90e-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="df90e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df90e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="df90e-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df90e-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df90e-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="df90e-136">Namespace</span></span><br/>                | <span data-ttu-id="df90e-137">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="df90e-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="df90e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="df90e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df90e-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df90e-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df90e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="df90e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df90e-141">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="df90e-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
