---
description: Desabilita ou suspende todos os protetores de chave associados a este volume.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Método DisableKeyProtectors da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761388"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ebd39-103">Método DisableKeyProtectors da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="ebd39-103">DisableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ebd39-104">O método **DisableKeyProtectors** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) desabilita ou suspende todos os protetores de chave associados a esse volume.</span><span class="sxs-lookup"><span data-stu-id="ebd39-104">The **DisableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class disables or suspends all key protectors associated with this volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd39-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebd39-105">Syntax</span></span>


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a><span data-ttu-id="ebd39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebd39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd39-107">*DisableCount* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ebd39-107">*DisableCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd39-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ebd39-108">Type: **uint32**</span></span>

<span data-ttu-id="ebd39-109">Inteiro que especifica o número de reinicializações para as quais os protetores de chave serão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="ebd39-109">Integer that specifies the number of reboots for which the key protectors will be disabled.</span></span> <span data-ttu-id="ebd39-110">Esse parâmetro só está disponível em volumes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ebd39-110">This parameter is only available on OS volumes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd39-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebd39-111">Return value</span></span>

<span data-ttu-id="ebd39-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ebd39-112">Type: **uint32**</span></span>

<span data-ttu-id="ebd39-113">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="ebd39-113">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ebd39-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ebd39-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="ebd39-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebd39-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ebd39-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ebd39-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="ebd39-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ebd39-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="ebd39-118"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="ebd39-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="ebd39-119">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ebd39-119">The volume is locked.</span></span><br/>      |



 

## <a name="security-considerations"></a><span data-ttu-id="ebd39-120">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="ebd39-120">Security Considerations</span></span>

<span data-ttu-id="ebd39-121">Esse método expõe a chave de criptografia do volume em Clear no disco rígido, desativando qualquer proteção de volume.</span><span class="sxs-lookup"><span data-stu-id="ebd39-121">This method exposes the volume's encryption key in the clear on the hard disk, turning off any volume protection.</span></span> <span data-ttu-id="ebd39-122">É recomendável que você tenha qualquer senha ou chave de criptografia em texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="ebd39-122">We recommend against having any password or encryption key in plaintext.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebd39-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebd39-123">Remarks</span></span>

<span data-ttu-id="ebd39-124">Novos protetores de chave podem ser adicionados mesmo quando protetores de chave estão desabilitados ou suspensos.</span><span class="sxs-lookup"><span data-stu-id="ebd39-124">New key protectors can be added even when key protectors are disabled or suspended.</span></span> <span data-ttu-id="ebd39-125">Esses protetores de chave permanecerão desabilitados, a menos que [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="ebd39-125">These key protectors will remain disabled unless [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) is called.</span></span>

<span data-ttu-id="ebd39-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ebd39-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ebd39-127">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="ebd39-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ebd39-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ebd39-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ebd39-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ebd39-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd39-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebd39-130">Requirements</span></span>



| <span data-ttu-id="ebd39-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd39-131">Requirement</span></span> | <span data-ttu-id="ebd39-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ebd39-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd39-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebd39-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd39-134">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ebd39-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ebd39-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebd39-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd39-136">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="ebd39-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ebd39-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebd39-137">Namespace</span></span><br/>                | <span data-ttu-id="ebd39-138">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="ebd39-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ebd39-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ebd39-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebd39-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebd39-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd39-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebd39-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd39-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="ebd39-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="ebd39-143">**EnableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="ebd39-143">**EnableKeyProtectors**</span></span>](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
