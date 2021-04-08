---
description: Atualiza um volume do formato do Windows Vista para o formato do Windows 7.
ms.assetid: d6654e92-8176-471b-b8e5-815dd9512240
title: Método UpgradeVolume da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UpgradeVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6769e8a4a480becc5a5584826f60cdb85f8b90e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920811"
---
# <a name="upgradevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="fdc3a-103">Método UpgradeVolume da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="fdc3a-103">UpgradeVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="fdc3a-104">O método **UpgradeVolume** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) atualiza um volume do formato do Windows Vista para o formato do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-104">The **UpgradeVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class upgrades a volume from the Windows Vista format to the Windows 7 format.</span></span> <span data-ttu-id="fdc3a-105">Esta é uma operação não reversível.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-105">This is a nonreversible operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc3a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdc3a-106">Syntax</span></span>


```mof
uint32 UpgradeVolume();
```



## <a name="parameters"></a><span data-ttu-id="fdc3a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdc3a-107">Parameters</span></span>

<span data-ttu-id="fdc3a-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdc3a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fdc3a-109">Return value</span></span>

<span data-ttu-id="fdc3a-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fdc3a-110">Type: **uint32**</span></span>

<span data-ttu-id="fdc3a-111">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="fdc3a-112">Se o volume já estiver desbloqueado e nenhum outro erro ocorrer, esse método retornará zero.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-112">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="fdc3a-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fdc3a-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="fdc3a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdc3a-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fdc3a-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc3a-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="fdc3a-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="fdc3a-117"><dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc3a-117"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl>            | <span data-ttu-id="fdc3a-118">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-118">One or more of the arguments are not valid.</span></span><br/>                                       |
| <dl> <span data-ttu-id="fdc3a-119"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc3a-119"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="fdc3a-120">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-120">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="fdc3a-121"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc3a-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="fdc3a-122">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="fdc3a-123">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-123">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="fdc3a-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdc3a-124">Remarks</span></span>

<span data-ttu-id="fdc3a-125">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fdc3a-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fdc3a-126">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="fdc3a-127">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="fdc3a-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fdc3a-128">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="fdc3a-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc3a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdc3a-129">Requirements</span></span>



| <span data-ttu-id="fdc3a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc3a-130">Requirement</span></span> | <span data-ttu-id="fdc3a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="fdc3a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc3a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdc3a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc3a-133">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="fdc3a-133">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fdc3a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdc3a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc3a-135">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="fdc3a-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fdc3a-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="fdc3a-136">Namespace</span></span><br/>                | <span data-ttu-id="fdc3a-137">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="fdc3a-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="fdc3a-138">MOF</span><span class="sxs-lookup"><span data-stu-id="fdc3a-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdc3a-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdc3a-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdc3a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdc3a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc3a-141">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="fdc3a-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
