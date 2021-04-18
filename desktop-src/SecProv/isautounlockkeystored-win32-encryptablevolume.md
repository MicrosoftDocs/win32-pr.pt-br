---
description: Indica se as chaves externas ou as informações relacionadas que podem ser usadas para desbloquear automaticamente os volumes de dados existem no volume do sistema operacional em execução no momento.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Método IsAutoUnlockKeyStored da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760372"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="921fe-103">Método IsAutoUnlockKeyStored da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="921fe-103">IsAutoUnlockKeyStored method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="921fe-104">O método **IsAutoUnlockKeyStored** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se as chaves externas ou as informações relacionadas que podem ser usadas para desbloquear automaticamente os volumes de dados existem no volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="921fe-104">The **IsAutoUnlockKeyStored** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether any external keys or related information that may be used to automatically unlock data volumes exist in the currently running operating system volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="921fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="921fe-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a><span data-ttu-id="921fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="921fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="921fe-107">*IsAutoUnlockKeyStored* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="921fe-107">*IsAutoUnlockKeyStored* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="921fe-108">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="921fe-108">Type: **boolean**</span></span>

<span data-ttu-id="921fe-109">Será **true** se qualquer informação que possa ser usada para desbloquear automaticamente os volumes de dados estiver armazenada no registro do volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="921fe-109">Is **true** if any information that can be used to automatically unlock data volumes is stored in the registry of the currently running operating system volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="921fe-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="921fe-110">Return value</span></span>

<span data-ttu-id="921fe-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="921fe-111">Type: **uint32**</span></span>

<span data-ttu-id="921fe-112">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="921fe-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="921fe-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="921fe-113">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="921fe-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="921fe-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="921fe-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="921fe-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="921fe-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="921fe-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="921fe-117"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="921fe-117"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="921fe-118">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="921fe-118">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="921fe-119">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="921fe-119">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="921fe-120"><dt>**FVE \_ E \_ não \_ o \_ VOLUME do so**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="921fe-120"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="921fe-121">O método só pode ser executado para o volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="921fe-121">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="921fe-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="921fe-122">Remarks</span></span>

<span data-ttu-id="921fe-123">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para remover todas as informações de desbloqueio do volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="921fe-123">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove all unlocking information from the currently running operating system volume.</span></span>

<span data-ttu-id="921fe-124">As informações usadas para desbloquear um volume são armazenadas quando o [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) é executado para um volume de dados enquanto o volume do sistema operacional atualmente em execução está em execução.</span><span class="sxs-lookup"><span data-stu-id="921fe-124">Information used to unlock a volume is stored when [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) is run for a data volume while the currently running operating system volume is running.</span></span>

<span data-ttu-id="921fe-125">**IsAutoUnlockKeyStored** difere de [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) , mesmo se o desbloqueio automático estiver desabilitado para todos os volumes de dados atualmente conectados ao computador, ainda poderá haver desbloqueio de informações associadas a volumes de dados desconectados ou volumes de dados que não existem mais.</span><span class="sxs-lookup"><span data-stu-id="921fe-125">**IsAutoUnlockKeyStored** differs from [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) in that even if automatic unlocking is disabled for all data volumes currently connected to the computer, there may still be unlocking information associated with disconnected data volumes or data volumes that no longer exist.</span></span>

<span data-ttu-id="921fe-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="921fe-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="921fe-127">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="921fe-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="921fe-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="921fe-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="921fe-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="921fe-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="921fe-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="921fe-130">Requirements</span></span>



| <span data-ttu-id="921fe-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="921fe-131">Requirement</span></span> | <span data-ttu-id="921fe-132">Valor</span><span class="sxs-lookup"><span data-stu-id="921fe-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="921fe-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="921fe-133">Minimum supported client</span></span><br/> | <span data-ttu-id="921fe-134">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="921fe-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="921fe-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="921fe-135">Minimum supported server</span></span><br/> | <span data-ttu-id="921fe-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="921fe-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="921fe-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="921fe-137">Namespace</span></span><br/>                | <span data-ttu-id="921fe-138">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="921fe-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="921fe-139">MOF</span><span class="sxs-lookup"><span data-stu-id="921fe-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="921fe-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="921fe-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="921fe-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="921fe-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921fe-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="921fe-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
