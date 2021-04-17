---
description: Faz backup dos dados de recuperação para Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Método BackupRecoveryInformationToActiveDirectory da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761998"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="69342-103">Método BackupRecoveryInformationToActiveDirectory da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="69342-103">BackupRecoveryInformationToActiveDirectory method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="69342-104">O método **BackupRecoveryInformationToActiveDirectory** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) faz backup dos dados de recuperação para Active Directory.</span><span class="sxs-lookup"><span data-stu-id="69342-104">The **BackupRecoveryInformationToActiveDirectory** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class backs up recovery data to Active Directory.</span></span> <span data-ttu-id="69342-105">Esse método requer que um protetor de senha numérica esteja presente no volume.</span><span class="sxs-lookup"><span data-stu-id="69342-105">This method requires a numerical password protector to be present on the volume.</span></span> <span data-ttu-id="69342-106">Política de Grupo também deve ser configurado para habilitar o backup de informações de recuperação para Active Directory.</span><span class="sxs-lookup"><span data-stu-id="69342-106">Group Policy must also be configured to enable backup of recovery information to Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="69342-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69342-107">Syntax</span></span>


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="69342-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69342-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69342-109">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69342-109">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69342-110">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="69342-110">Type: **string**</span></span>

<span data-ttu-id="69342-111">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="69342-111">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="69342-112">Esse protetor de chave deve ser um protetor de senha numérica.</span><span class="sxs-lookup"><span data-stu-id="69342-112">This key protector must be a numerical password protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69342-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69342-113">Return value</span></span>

<span data-ttu-id="69342-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69342-114">Type: **uint32**</span></span>

<span data-ttu-id="69342-115">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="69342-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="69342-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="69342-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="69342-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="69342-117">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69342-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="69342-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="69342-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="69342-119">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="69342-120"><dt>**S \_ FALSO**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="69342-120"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                         | <span data-ttu-id="69342-121">Política de Grupo não permite o armazenamento de informações de recuperação para Active Directory.</span><span class="sxs-lookup"><span data-stu-id="69342-121">Group Policy does not permit the storage of recovery information to Active Directory.</span></span><br/>                         |
| <dl> <span data-ttu-id="69342-122"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="69342-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="69342-123">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="69342-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="69342-124">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="69342-124">Add a key protector to enable BitLocker.</span></span> <br/>                             |
| <dl> <span data-ttu-id="69342-125"><dt>**FVE \_ E \_ \_ \_ tipo de protetor inválido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="69342-125"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="69342-126">O protetor de chave especificado não é um protetor de chave numérica.</span><span class="sxs-lookup"><span data-stu-id="69342-126">The specified key protector is not a numerical key protector.</span></span> <span data-ttu-id="69342-127">Você deve inserir um protetor de senha numérica.</span><span class="sxs-lookup"><span data-stu-id="69342-127">You must enter a numerical password protector.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="69342-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69342-128">Requirements</span></span>



| <span data-ttu-id="69342-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="69342-129">Requirement</span></span> | <span data-ttu-id="69342-130">Valor</span><span class="sxs-lookup"><span data-stu-id="69342-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69342-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69342-131">Minimum supported client</span></span><br/> | <span data-ttu-id="69342-132">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="69342-132">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="69342-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69342-133">Minimum supported server</span></span><br/> | <span data-ttu-id="69342-134">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="69342-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69342-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="69342-135">Namespace</span></span><br/>                | <span data-ttu-id="69342-136">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="69342-136">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="69342-137">MOF</span><span class="sxs-lookup"><span data-stu-id="69342-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69342-138"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69342-138"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69342-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="69342-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69342-140">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="69342-140">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




