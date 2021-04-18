---
description: Recupera o número de vezes que o BitLocker foi suspenso.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Método GetSuspendCount da classe Win32_EncryptableVolume (Activdbg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810495"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f32eb-103">Método GetSuspendCount da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="f32eb-103">GetSuspendCount method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f32eb-104">O método **GetSuspendCount** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera o número de reinicializações antes que a proteção seja retomada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f32eb-104">The **GetSuspendCount** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the number of reboots before protection will automatically be resumed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f32eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f32eb-105">Syntax</span></span>


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a><span data-ttu-id="f32eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f32eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f32eb-107">*SuspendCount*</span><span class="sxs-lookup"><span data-stu-id="f32eb-107">*SuspendCount*</span></span> 
</dt> <dd>

<span data-ttu-id="f32eb-108">Um valor inteiro de 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="f32eb-108">An integer value from 0 to 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f32eb-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f32eb-109">Return value</span></span>

<span data-ttu-id="f32eb-110">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="f32eb-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f32eb-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f32eb-111">Return code</span></span>                                                                                          | <span data-ttu-id="f32eb-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f32eb-112">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f32eb-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f32eb-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="f32eb-114">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f32eb-114">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="f32eb-115"><dt>**ERRO \_ sem \_ suporte**</dt></span><span class="sxs-lookup"><span data-stu-id="f32eb-115"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="f32eb-116">Retornado se o volume não estiver suspenso ou não for um volume do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f32eb-116">Returned if the volume is not suspended or is not an OS volume.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f32eb-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f32eb-117">Remarks</span></span>

<span data-ttu-id="f32eb-118">Esse método só se aplica ao volume do sistema operacional e somente se ele estiver realmente suspenso no momento.</span><span class="sxs-lookup"><span data-stu-id="f32eb-118">This method only applies to the OS volume, and only if it is actually suspended at the time.</span></span> <span data-ttu-id="f32eb-119">Se o volume não estiver suspenso ou não for um volume do sistema operacional, o **erro \_ não terá \_ suporte** será retornado.</span><span class="sxs-lookup"><span data-stu-id="f32eb-119">If the volume is not suspended or is not an OS volume, **ERROR\_NOT\_SUPPORTED** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="f32eb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f32eb-120">Requirements</span></span>



| <span data-ttu-id="f32eb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f32eb-121">Requirement</span></span> | <span data-ttu-id="f32eb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f32eb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32eb-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f32eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f32eb-124">Windows 8 Enterprise, \[ somente aplicativos de área de trabalho do Windows 8 pro\]</span><span class="sxs-lookup"><span data-stu-id="f32eb-124">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f32eb-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f32eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f32eb-126">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f32eb-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f32eb-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="f32eb-127">Namespace</span></span><br/>                | <span data-ttu-id="f32eb-128">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f32eb-128">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f32eb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f32eb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f32eb-130"><dt>Activdbg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f32eb-130"><dt>Activdbg.h</dt></span></span> </dl>                   |
| <span data-ttu-id="f32eb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f32eb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f32eb-132"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f32eb-132"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32eb-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f32eb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32eb-134">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f32eb-134">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




