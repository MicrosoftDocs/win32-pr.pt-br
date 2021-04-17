---
description: Pausa a criptografia ou descriptografia de um volume.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Método PauseConversion da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784131"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="26984-103">Método PauseConversion da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="26984-103">PauseConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="26984-104">O método **PauseConversion** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) pausa a criptografia ou descriptografia de um volume.</span><span class="sxs-lookup"><span data-stu-id="26984-104">The **PauseConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class pauses the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="26984-105">Se o disco oferecer suporte à criptografia de hardware, essa função poderá pausar uma operação de apagamento, mas não poderá pausar a criptografia baseada em hardware.</span><span class="sxs-lookup"><span data-stu-id="26984-105">If the disc supports hardware encryption, this function can pause a wiping operation but cannot pause hardware-based encryption.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="26984-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26984-106">Syntax</span></span>


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a><span data-ttu-id="26984-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26984-107">Parameters</span></span>

<span data-ttu-id="26984-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="26984-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26984-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26984-109">Return value</span></span>

<span data-ttu-id="26984-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26984-110">Type: **uint32**</span></span>

<span data-ttu-id="26984-111">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="26984-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="26984-112">Se esse método for usado em um volume totalmente criptografado ou totalmente descriptografado, ou se a criptografia/descriptografia já estiver em pausa no volume, 0 será retornado supondo que nenhum outro erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="26984-112">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already paused on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="26984-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="26984-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="26984-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="26984-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="26984-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="26984-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="26984-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="26984-116">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="26984-117"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="26984-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="26984-118">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="26984-118">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="26984-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="26984-119">Remarks</span></span>

<span data-ttu-id="26984-120">Se esse método for usado em um volume com criptografia/descriptografia em andamento, a execução bem-sucedida desse método fará com que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que a criptografia ou descriptografia está em pausa.</span><span class="sxs-lookup"><span data-stu-id="26984-120">If this method is used on a volume with encryption/decryption in progress, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is paused.</span></span>

<span data-ttu-id="26984-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="26984-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="26984-122">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="26984-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="26984-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="26984-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="26984-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="26984-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26984-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26984-125">Requirements</span></span>



| <span data-ttu-id="26984-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="26984-126">Requirement</span></span> | <span data-ttu-id="26984-127">Valor</span><span class="sxs-lookup"><span data-stu-id="26984-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26984-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26984-128">Minimum supported client</span></span><br/> | <span data-ttu-id="26984-129">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="26984-129">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="26984-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26984-130">Minimum supported server</span></span><br/> | <span data-ttu-id="26984-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26984-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26984-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="26984-132">Namespace</span></span><br/>                | <span data-ttu-id="26984-133">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="26984-133">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="26984-134">MOF</span><span class="sxs-lookup"><span data-stu-id="26984-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26984-135"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26984-135"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26984-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="26984-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26984-137">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="26984-137">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
