---
description: Cria um volume do BitLocker com o tipo de sistema de arquivos especificado do volume de descoberta.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Método PrepareVolume da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090171"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e4ccd-103">Método PrepareVolume da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="e4ccd-103">PrepareVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e4ccd-104">O método **PrepareVolume** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) cria um volume do BitLocker com o tipo de sistema de arquivos especificado do volume de descoberta.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-104">The **PrepareVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class creates a BitLocker volume with the specified file system type of the discovery volume.</span></span> <span data-ttu-id="e4ccd-105">Esse método deve ser chamado antes que o volume possa ser protegido com qualquer um dos métodos \**ProtectKeyWith \** _.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-105">This method must be called before the volume can be protected with any of the \**ProtectKeyWith\** _ methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ccd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4ccd-106">Syntax</span></span>

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a><span data-ttu-id="e4ccd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4ccd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ccd-108">_DiscoveryVolumeType \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4ccd-108">_DiscoveryVolumeType\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ccd-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e4ccd-109">Type: **string**</span></span>

<span data-ttu-id="e4ccd-110">Uma cadeia de caracteres que especifica o tipo de volume de descoberta.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-110">A string that specifies the type of discovery volume.</span></span>

| <span data-ttu-id="e4ccd-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e4ccd-111">Value</span></span>               | <span data-ttu-id="e4ccd-112">Significado</span><span class="sxs-lookup"><span data-stu-id="e4ccd-112">Meaning</span></span>                                                            |
|---------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e4ccd-113">**&lt;None&gt;**</span><span class="sxs-lookup"><span data-stu-id="e4ccd-113">**&lt;none&gt;**</span></span>    | <span data-ttu-id="e4ccd-114">Nenhum volume de descoberta.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-114">No discovery volume.</span></span> <span data-ttu-id="e4ccd-115">Esse valor cria um volume do BitLocker nativo.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-115">This value creates a native BitLocker volume.</span></span> |
| <span data-ttu-id="e4ccd-116">**&lt;os&gt;**</span><span class="sxs-lookup"><span data-stu-id="e4ccd-116">**&lt;default&gt;**</span></span> | <span data-ttu-id="e4ccd-117">Esse valor é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-117">This value is the default behavior.</span></span>                                |
| <span data-ttu-id="e4ccd-118">**FAT32**</span><span class="sxs-lookup"><span data-stu-id="e4ccd-118">**FAT32**</span></span>           | <span data-ttu-id="e4ccd-119">Esse valor cria um volume de descoberta FAT32.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-119">This value creates a FAT32 discovery volume.</span></span>                       |

</dd> <dt>

<span data-ttu-id="e4ccd-120">*ForceEncryptionType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4ccd-120">*ForceEncryptionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ccd-121">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4ccd-121">Type: **uint32**</span></span>

<span data-ttu-id="e4ccd-122">Inteiro que especifica o tipo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-122">Integer that specifies the encryption type.</span></span> <span data-ttu-id="e4ccd-123">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-123">This can be one of the following values.</span></span>

| <span data-ttu-id="e4ccd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e4ccd-124">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="e4ccd-125">Significado</span><span class="sxs-lookup"><span data-stu-id="e4ccd-125">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="e4ccd-126"><dt>**Não especificado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e4ccd-126"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e4ccd-127">O tipo de criptografia não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-127">The encryption type is not specified.</span></span><br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <span data-ttu-id="e4ccd-128"><dt>**Software**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e4ccd-128"><dt>**Software**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="e4ccd-129">Criptografia de software.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-129">Software encryption.</span></span><br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <span data-ttu-id="e4ccd-130"><dt>**Hardware**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e4ccd-130"><dt>**Hardware**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="e4ccd-131">Criptografia de hardware.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-131">Hardware encryption.</span></span><br/>                  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4ccd-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4ccd-132">Return value</span></span>

<span data-ttu-id="e4ccd-133">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4ccd-133">Type: **uint32**</span></span>

<span data-ttu-id="e4ccd-134">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-134">This method returns one of the following codes or another error code if it fails.</span></span>

| <span data-ttu-id="e4ccd-135">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e4ccd-135">Return code/value</span></span>      | <span data-ttu-id="e4ccd-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4ccd-136">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="e4ccd-137">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="e4ccd-137">**S_OK**</span></span> <br/> <span data-ttu-id="e4ccd-138">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="e4ccd-138">0 (0x0)</span></span> | <span data-ttu-id="e4ccd-139">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e4ccd-139">The method was successful.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="e4ccd-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4ccd-140">Remarks</span></span>

<span data-ttu-id="e4ccd-141">Se você não chamar esse método ao habilitar um volume do BitLocker, ele será o mesmo que chamar esse método com o valor padrão no parâmetro *DiscoveryVolumeType* .</span><span class="sxs-lookup"><span data-stu-id="e4ccd-141">If you do not call this method when enabling a BitLocker volume, it is the same as calling this method with the default value in the *DiscoveryVolumeType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ccd-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4ccd-142">Requirements</span></span>

| <span data-ttu-id="e4ccd-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4ccd-143">Requirement</span></span> | <span data-ttu-id="e4ccd-144">Valor</span><span class="sxs-lookup"><span data-stu-id="e4ccd-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ccd-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4ccd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e4ccd-146">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="e4ccd-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e4ccd-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4ccd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e4ccd-148">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="e4ccd-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e4ccd-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4ccd-149">Namespace</span></span><br/>                | <span data-ttu-id="e4ccd-150">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="e4ccd-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e4ccd-151">MOF</span><span class="sxs-lookup"><span data-stu-id="e4ccd-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4ccd-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4ccd-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e4ccd-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4ccd-153">See also</span></span>

[<span data-ttu-id="e4ccd-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="e4ccd-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
