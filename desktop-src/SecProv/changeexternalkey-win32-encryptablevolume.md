---
description: Altera uma chave externa que está associada a um volume criptografado.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Método ChangeExternalKey da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767810"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="dbfa1-103">Método ChangeExternalKey da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="dbfa1-103">ChangeExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="dbfa1-104">O método **ChangeExternalKey** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) altera uma chave externa associada a um volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-104">The **ChangeExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes an external key that is associated with an encrypted volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfa1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbfa1-105">Syntax</span></span>


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="dbfa1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbfa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbfa1-107">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dbfa1-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfa1-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbfa1-108">Type: **string**</span></span>

<span data-ttu-id="dbfa1-109">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

 <span data-ttu-id="dbfa1-110">*NewExternalKey* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dbfa1-110">*NewExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfa1-111">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="dbfa1-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="dbfa1-112">Uma matriz de bytes que especifica a chave externa de 256 bits usada para desbloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-112">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

</dd> <dt>

<span data-ttu-id="dbfa1-113">*NewVolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dbfa1-113">*NewVolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfa1-114">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbfa1-114">Type: **string**</span></span>

<span data-ttu-id="dbfa1-115">Um identificador de cadeia de caracteres exclusivo atualizado que é usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-115">An updated unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbfa1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbfa1-116">Return value</span></span>

<span data-ttu-id="dbfa1-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbfa1-117">Type: **uint32**</span></span>

<span data-ttu-id="dbfa1-118">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="dbfa1-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dbfa1-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="dbfa1-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbfa1-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbfa1-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa1-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="dbfa1-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-122">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="dbfa1-123"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa1-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                    | <span data-ttu-id="dbfa1-124">O parâmetro *NewExternalKey* não é uma matriz de tamanho 32.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-124">The *NewExternalKey* parameter is not an array of size 32.</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="dbfa1-125"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa1-125"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="dbfa1-126">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-126">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="dbfa1-127"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa1-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="dbfa1-128">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="dbfa1-129">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="dbfa1-130"><dt>**FVE \_ E \_ inicializável \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa1-130"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>          | <span data-ttu-id="dbfa1-131">Um CD/DVD inicializável foi encontrado neste computador.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-131">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="dbfa1-132">Remova o CD/DVD e reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-132">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="dbfa1-133"><dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa1-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="dbfa1-134">O protetor de chave fornecido não existe no volume.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="dbfa1-135"><dt>**FVE \_ E \_ \_ \_ tipo de protetor inválido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa1-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="dbfa1-136">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "senha numérica" ou "chave externa".</span><span class="sxs-lookup"><span data-stu-id="dbfa1-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="dbfa1-137">Use o método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para criar um protetor de chave do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbfa1-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbfa1-138">Remarks</span></span>

<span data-ttu-id="dbfa1-139">Esse método pode ser usado para alterar a chave externa para qualquer protetor de chave que usa uma chave externa.</span><span class="sxs-lookup"><span data-stu-id="dbfa1-139">This method can be used to change the external key for any key protector that uses an external key.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbfa1-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbfa1-140">Requirements</span></span>



| <span data-ttu-id="dbfa1-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbfa1-141">Requirement</span></span> | <span data-ttu-id="dbfa1-142">Valor</span><span class="sxs-lookup"><span data-stu-id="dbfa1-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfa1-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbfa1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfa1-144">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="dbfa1-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dbfa1-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbfa1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfa1-146">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="dbfa1-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dbfa1-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbfa1-147">Namespace</span></span><br/>                | <span data-ttu-id="dbfa1-148">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="dbfa1-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="dbfa1-149">MOF</span><span class="sxs-lookup"><span data-stu-id="dbfa1-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbfa1-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbfa1-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbfa1-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbfa1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbfa1-152">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="dbfa1-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




