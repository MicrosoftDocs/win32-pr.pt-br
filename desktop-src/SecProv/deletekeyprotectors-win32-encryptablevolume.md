---
description: Exclui todos os protetores de chave do volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Método DeleteKeyProtectors da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760006"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="520c4-103">Método DeleteKeyProtectors da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="520c4-103">DeleteKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="520c4-104">O método **DeleteKeyProtectors** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) exclui todos os protetores de chave do volume.</span><span class="sxs-lookup"><span data-stu-id="520c4-104">The **DeleteKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes all key protectors for the volume.</span></span>

<span data-ttu-id="520c4-105">Se um volume não criptografado tiver protetores de chave, quando **DeleteKeyProtectors** for executado com êxito, o volume será revertido para um sistema de arquivos NTFS padrão.</span><span class="sxs-lookup"><span data-stu-id="520c4-105">If an unencrypted volume has key protectors, when **DeleteKeyProtectors** is run successfully the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="520c4-106">Se o volume ainda não tiver sido totalmente descriptografado, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de executar **DeleteKeyProtectors** para garantir que partes criptografadas do volume permaneçam acessíveis.</span><span class="sxs-lookup"><span data-stu-id="520c4-106">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before running **DeleteKeyProtectors** to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="520c4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="520c4-107">Syntax</span></span>


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="520c4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="520c4-108">Parameters</span></span>

<span data-ttu-id="520c4-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="520c4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="520c4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="520c4-110">Return value</span></span>

<span data-ttu-id="520c4-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="520c4-111">Type: **uint32**</span></span>

<span data-ttu-id="520c4-112">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="520c4-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="520c4-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="520c4-113">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="520c4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="520c4-114">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="520c4-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="520c4-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="520c4-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="520c4-116">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="520c4-117"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="520c4-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="520c4-118">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="520c4-118">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="520c4-119"><dt>**FVE \_ \_Chave E \_ necessária**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="520c4-119"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="520c4-120">O último protetor de chave para um volume parcialmente ou totalmente criptografado não poderá ser removido se os protetores de chave estiverem habilitados.</span><span class="sxs-lookup"><span data-stu-id="520c4-120">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="520c4-121">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de remover esse último protetor de chave para garantir que partes criptografadas do volume permaneçam acessíveis.</span><span class="sxs-lookup"><span data-stu-id="520c4-121">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="520c4-122"><dt>**FVE \_ E o \_ volume \_ associado \_ já**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="520c4-122"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="520c4-123">Os protetores de chave não podem ser excluídos porque um deles está sendo usado para desbloquear automaticamente o volume.</span><span class="sxs-lookup"><span data-stu-id="520c4-123">Key protectors cannot be deleted because one of them is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="520c4-124">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para desabilitar o desbloqueio automático antes de executar este método.</span><span class="sxs-lookup"><span data-stu-id="520c4-124">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before running this method.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="520c4-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="520c4-125">Remarks</span></span>

<span data-ttu-id="520c4-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="520c4-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="520c4-127">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="520c4-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="520c4-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="520c4-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="520c4-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="520c4-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="520c4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="520c4-130">Requirements</span></span>



| <span data-ttu-id="520c4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="520c4-131">Requirement</span></span> | <span data-ttu-id="520c4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="520c4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="520c4-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="520c4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="520c4-134">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="520c4-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="520c4-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="520c4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="520c4-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="520c4-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="520c4-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="520c4-137">Namespace</span></span><br/>                | <span data-ttu-id="520c4-138">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="520c4-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="520c4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="520c4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="520c4-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="520c4-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="520c4-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="520c4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520c4-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="520c4-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
