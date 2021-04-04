---
description: Retoma a criptografia ou descriptografia de um volume.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Método ResumeConversion da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eafa700f86e51310096835e2f24b53a28e66f800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646983"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6c675-103">Método ResumeConversion da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="6c675-103">ResumeConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6c675-104">O método **ResumeConversion** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) retoma a criptografia ou descriptografia de um volume.</span><span class="sxs-lookup"><span data-stu-id="6c675-104">The **ResumeConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class resumes the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="6c675-105">Se o disco oferecer suporte à criptografia de hardware, essa função poderá retomar apenas uma operação de apagamento.</span><span class="sxs-lookup"><span data-stu-id="6c675-105">If the disc supports hardware encryption, this function can resume a wiping operation only.</span></span> <span data-ttu-id="6c675-106">Para obter mais informações, consulte [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="6c675-106">For more information, see [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6c675-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c675-107">Syntax</span></span>


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a><span data-ttu-id="6c675-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c675-108">Parameters</span></span>

<span data-ttu-id="6c675-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6c675-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c675-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c675-110">Return value</span></span>

<span data-ttu-id="6c675-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c675-111">Type: **uint32**</span></span>

<span data-ttu-id="6c675-112">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="6c675-112">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="6c675-113">Se esse método for usado em um volume totalmente criptografado ou totalmente descriptografado, ou se a criptografia/descriptografia já estiver em andamento no volume, 0 será retornado supondo que nenhum outro erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="6c675-113">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already in progress on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="6c675-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6c675-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="6c675-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c675-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6c675-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6c675-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="6c675-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6c675-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="6c675-118"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6c675-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="6c675-119">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6c675-119">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="6c675-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c675-120">Remarks</span></span>

<span data-ttu-id="6c675-121">Se esse método for usado em um volume com criptografia/descriptografia em pausa, a execução bem-sucedida desse método fará com que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que a criptografia ou descriptografia está em andamento.</span><span class="sxs-lookup"><span data-stu-id="6c675-121">If this method is used on a volume with paused encryption/decryption, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is in progress.</span></span>

<span data-ttu-id="6c675-122">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6c675-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6c675-123">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="6c675-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6c675-124">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6c675-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6c675-125">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6c675-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c675-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c675-126">Requirements</span></span>



| <span data-ttu-id="6c675-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c675-127">Requirement</span></span> | <span data-ttu-id="6c675-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6c675-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c675-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c675-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6c675-130">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="6c675-130">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6c675-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c675-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6c675-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c675-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c675-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c675-133">Namespace</span></span><br/>                | <span data-ttu-id="6c675-134">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="6c675-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6c675-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6c675-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c675-136"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c675-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c675-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c675-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c675-138">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6c675-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
