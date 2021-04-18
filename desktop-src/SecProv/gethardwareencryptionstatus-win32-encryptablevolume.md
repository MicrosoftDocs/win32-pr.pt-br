---
description: Determina se o volume está localizado em uma unidade que dá suporte ou pode dar suporte à criptografia de hardware.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Método GetHardwareEncryptionStatus da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796358"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a09ad-103">Método GetHardwareEncryptionStatus da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="a09ad-103">GetHardwareEncryptionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a09ad-104">O método **GetHardwareEncryptionStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) determina se o volume está localizado em uma unidade que dá suporte ou pode dar suporte à criptografia de hardware.</span><span class="sxs-lookup"><span data-stu-id="a09ad-104">The **GetHardwareEncryptionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class determines whether the volume is located on a drive that supports or can support hardware encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="a09ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a09ad-105">Syntax</span></span>


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a09ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a09ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a09ad-107">*HardwareEncryptionStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a09ad-107">*HardwareEncryptionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a09ad-108">Especifica se a unidade pode dar suporte à criptografia de hardware.</span><span class="sxs-lookup"><span data-stu-id="a09ad-108">Specifies whether the drive can support hardware encryption.</span></span> <span data-ttu-id="a09ad-109">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a09ad-109">This can be one of the following values.</span></span>



| <span data-ttu-id="a09ad-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a09ad-110">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="a09ad-111">Significado</span><span class="sxs-lookup"><span data-stu-id="a09ad-111">Meaning</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="a09ad-112"><dt>**Sem suporte**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a09ad-112"><dt>**Not supported**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="a09ad-113">Não há suporte para criptografia de hardware.</span><span class="sxs-lookup"><span data-stu-id="a09ad-113">Hardware encryption is not supported.</span></span><br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <span data-ttu-id="a09ad-114"><dt>**Sem proteção**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a09ad-114"><dt>**No protection**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="a09ad-115">Não há suporte para a criptografia de unidade.</span><span class="sxs-lookup"><span data-stu-id="a09ad-115">Drive encryption is not supported.</span></span><br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <span data-ttu-id="a09ad-116"><dt>**Usa software**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a09ad-116"><dt>**Uses software**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="a09ad-117">O método de criptografia é baseado em software.</span><span class="sxs-lookup"><span data-stu-id="a09ad-117">The encryption method is software-based.</span></span><br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <span data-ttu-id="a09ad-118"><dt>**Usa hardware**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a09ad-118"><dt>**Uses hardware**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="a09ad-119">A unidade dá suporte à criptografia de hardware.</span><span class="sxs-lookup"><span data-stu-id="a09ad-119">The drive supports hardware encryption.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a09ad-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a09ad-120">Return value</span></span>

<span data-ttu-id="a09ad-121">Essa função retornará zero (0) se o volume for compatível com a criptografia de hardware do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a09ad-121">This function returns zero (0) if the volume is compatible with BitLocker hardware encryption.</span></span> <span data-ttu-id="a09ad-122">Caso contrário, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a09ad-122">Otherwise, the function returns an error.</span></span>



| <span data-ttu-id="a09ad-123">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a09ad-123">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="a09ad-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="a09ad-124">Description</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a09ad-125"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a09ad-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="a09ad-126">O volume é compatível com a criptografia de hardware do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a09ad-126">The volume is compatible with BitLocker hardware encryption.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a09ad-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a09ad-127">Requirements</span></span>



| <span data-ttu-id="a09ad-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a09ad-128">Requirement</span></span> | <span data-ttu-id="a09ad-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a09ad-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a09ad-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a09ad-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a09ad-131">Windows 8 Enterprise, \[ somente aplicativos de área de trabalho do Windows 8 pro\]</span><span class="sxs-lookup"><span data-stu-id="a09ad-131">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a09ad-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a09ad-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a09ad-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a09ad-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a09ad-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="a09ad-134">Namespace</span></span><br/>                | <span data-ttu-id="a09ad-135">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="a09ad-135">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a09ad-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a09ad-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a09ad-137"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a09ad-137"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a09ad-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a09ad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a09ad-139">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="a09ad-139">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




