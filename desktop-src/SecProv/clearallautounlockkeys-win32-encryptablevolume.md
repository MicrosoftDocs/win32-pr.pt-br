---
description: Remove todas as chaves externas e informações relacionadas salvas no volume do sistema operacional em execução no momento que são usadas para desbloquear automaticamente os volumes de dados.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Método ClearAllAutoUnlockKeys da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761852"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="dcfb4-103">Método ClearAllAutoUnlockKeys da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="dcfb4-103">ClearAllAutoUnlockKeys method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="dcfb4-104">O método **ClearAllAutoUnlockKeys** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) remove todas as chaves externas e informações relacionadas salvas no volume do sistema operacional em execução no momento que são usadas para desbloquear automaticamente os volumes de dados.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-104">The **ClearAllAutoUnlockKeys** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes all external keys and related information saved onto the currently running operating system volume that are used to automatically unlock data volumes.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfb4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcfb4-105">Syntax</span></span>


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a><span data-ttu-id="dcfb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dcfb4-106">Parameters</span></span>

<span data-ttu-id="dcfb4-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcfb4-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dcfb4-108">Return value</span></span>

<span data-ttu-id="dcfb4-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfb4-109">Type: **uint32**</span></span>

<span data-ttu-id="dcfb4-110">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="dcfb4-111">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dcfb4-111">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="dcfb4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcfb4-112">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcfb4-113"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="dcfb4-113"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="dcfb4-114">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-114">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="dcfb4-115"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="dcfb4-115"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="dcfb4-116">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-116">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="dcfb4-117">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-117">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="dcfb4-118"><dt>**FVE \_ E \_ não \_ o \_ VOLUME do so**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="dcfb4-118"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="dcfb4-119">O método só pode ser executado para o volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-119">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="dcfb4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcfb4-120">Remarks</span></span>

<span data-ttu-id="dcfb4-121">O **ClearAllAutoUnlockKeys** Obtém a mesma funcionalidade que a execução de [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para cada volume de dados que já foi associado ao sistema operacional em execução no momento, até mesmo os volumes de dados que não estão conectados ao computador no momento.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-121">**ClearAllAutoUnlockKeys** achieves the same functionality as running [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) for every data volume that has ever been associated with the currently running operating system, even data volumes that are not currently connected to the computer.</span></span> <span data-ttu-id="dcfb4-122">Ele também remove quaisquer informações desbloqueadas obsoletas associadas a volumes de dados que não existem mais.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-122">It also removes any stale unlocking information associated with data volumes that no longer exist.</span></span>

<span data-ttu-id="dcfb4-123">Antes de chamar a [**descriptografia**](decrypt-win32-encryptablevolume.md) no volume do sistema operacional em execução no momento, use **ClearAllAutoUnlockKeys** para garantir que as informações colocadas no registro do sistema operacional desbloqueiem automaticamente os volumes de dados não estejam acessíveis no disco limpo.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-123">Before calling [**Decrypt**](decrypt-win32-encryptablevolume.md) on the currently running operating system volume, use **ClearAllAutoUnlockKeys** to ensure that information placed in the operating system registry to automatically unlock data volumes is not accessible in the clear on disk.</span></span>

<span data-ttu-id="dcfb4-124">Depois que o **ClearAllAutoUnlockKeys** é executado com êxito, os métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) podem ser usados para desbloquear todos os volumes de dados neste computador.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-124">After **ClearAllAutoUnlockKeys** runs successfully, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) can be used to unlock all data volumes on this computer.</span></span> <span data-ttu-id="dcfb4-125">Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) para reabilitar o desbloqueio automático de um volume de dados.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-125">Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) to re-enable automatic unlocking of a data volume.</span></span>

<span data-ttu-id="dcfb4-126">Se nenhum outro erro for retornado, o **ClearAllAutoUnlockKeys** removerá do registro quaisquer IDs de protetor de volume e chaves externas usadas para desbloquear automaticamente qualquer volume de dados que já tenha sido associado ao volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-126">If no other errors are returned, **ClearAllAutoUnlockKeys** removes from the registry any volume protector IDs and external keys used to automatically unlock any data volume that has ever been associated with the currently running operating system volume.</span></span>

<span data-ttu-id="dcfb4-127">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dcfb4-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dcfb4-128">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="dcfb4-129">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="dcfb4-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dcfb4-130">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="dcfb4-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcfb4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcfb4-131">Requirements</span></span>



| <span data-ttu-id="dcfb4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcfb4-132">Requirement</span></span> | <span data-ttu-id="dcfb4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="dcfb4-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfb4-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcfb4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dcfb4-135">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="dcfb4-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dcfb4-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcfb4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dcfb4-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dcfb4-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dcfb4-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcfb4-138">Namespace</span></span><br/>                | <span data-ttu-id="dcfb4-139">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="dcfb4-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="dcfb4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="dcfb4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcfb4-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcfb4-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcfb4-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcfb4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfb4-143">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="dcfb4-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
