---
description: Desmonta o volume e remove a chave de criptografia do volume da memória do sistema.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Método Lock da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826973"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1aa0b-103">Método Lock da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="1aa0b-103">Lock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1aa0b-104">O método **Lock** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) desmonta o volume e remove a chave de criptografia do volume da memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-104">The **Lock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class dismounts the volume and removes the volume's encryption key from system memory.</span></span> <span data-ttu-id="1aa0b-105">O conteúdo do volume permanece inacessível até que seja desbloqueado pelo método [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou pelo método [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="1aa0b-105">The contents of the volume remain inaccessible until it is unlocked by either the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) method or the [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="1aa0b-106">Este método não pode ser executado com êxito para o volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-106">This method cannot be successfully run for the currently running operating system volume.</span></span>

> [!Note]  
> <span data-ttu-id="1aa0b-107">Se o disco oferecer suporte à criptografia de hardware, a banda será definida como "bloqueada".</span><span class="sxs-lookup"><span data-stu-id="1aa0b-107">If the disc supports hardware encryption, the band is set to "locked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1aa0b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1aa0b-108">Syntax</span></span>


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a><span data-ttu-id="1aa0b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1aa0b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa0b-110">*ForceDismount* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1aa0b-110">*ForceDismount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa0b-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1aa0b-111">Type: **boolean**</span></span>

<span data-ttu-id="1aa0b-112">Se **true** , o disco será forçosamente desmontado.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-112">If **true** the disk is forcibly dismounted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa0b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1aa0b-113">Return value</span></span>

<span data-ttu-id="1aa0b-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1aa0b-114">Type: **uint32**</span></span>

<span data-ttu-id="1aa0b-115">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1aa0b-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1aa0b-116">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="1aa0b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1aa0b-117">Description</span></span>                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1aa0b-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0b-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="1aa0b-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-119">The method was successful.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="1aa0b-120"><dt>**E \_ ACESSO \_ negado**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0b-120"><dt>**E\_ACCESS\_DENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl>               | <span data-ttu-id="1aa0b-121">Os aplicativos estão acessando este volume.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-121">Applications are accessing this volume.</span></span> <span data-ttu-id="1aa0b-122">Se todo o acesso for não exclusivo, especificar o parâmetro *ForceDismount* como true permitirá que o método seja executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-122">If all access is nonexclusive, specifying the *ForceDismount* parameter as true allows the method to run successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1aa0b-123"><dt>**FVE \_ E \_ não \_ criptografado**</dt> <dt>2150694913 (0x80310001)</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0b-123"><dt>**FVE\_E\_NOT\_ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt></span></span> </dl>          | <span data-ttu-id="1aa0b-124">O volume está totalmente descriptografado e não pode ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-124">The volume is fully decrypted and cannot be locked.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="1aa0b-125"><dt>**FVE \_ E \_ proteção \_ desabilitada**</dt> <dt>2150694945 (0x80310021)</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0b-125"><dt>**FVE\_E\_PROTECTION\_DISABLED**</dt> <dt>2150694945 (0x80310021)</dt></span></span> </dl>    | <span data-ttu-id="1aa0b-126">A chave de criptografia do volume está disponível em branco no disco, impedindo que o volume seja bloqueado.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-126">The volume's encryption key is available in the clear on the disk, preventing the volume from being locked.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="1aa0b-127"><dt>**FVE \_ E \_ chave de recuperação \_ \_ necessária**</dt> <dt>2150694946 (0x80310022)</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0b-127"><dt>**FVE\_E\_RECOVERY\_KEY\_REQUIRED**</dt> <dt>2150694946 (0x80310022)</dt></span></span> </dl> | <span data-ttu-id="1aa0b-128">O volume não tem protetores de chave do tipo "senha numérica" ou "chave externa" que são necessários para desbloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-128">The volume does not have key protectors of the type "Numerical Password" or "External Key" that are necessary to unlock the volume.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="1aa0b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="1aa0b-129">Remarks</span></span>

<span data-ttu-id="1aa0b-130">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1aa0b-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1aa0b-131">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1aa0b-132">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="1aa0b-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1aa0b-133">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1aa0b-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa0b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aa0b-134">Requirements</span></span>



| <span data-ttu-id="1aa0b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aa0b-135">Requirement</span></span> | <span data-ttu-id="1aa0b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="1aa0b-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa0b-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aa0b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa0b-138">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="1aa0b-138">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1aa0b-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aa0b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa0b-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1aa0b-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1aa0b-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="1aa0b-141">Namespace</span></span><br/>                | <span data-ttu-id="1aa0b-142">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="1aa0b-142">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1aa0b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="1aa0b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1aa0b-144"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0b-144"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa0b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="1aa0b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa0b-146">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="1aa0b-146">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
