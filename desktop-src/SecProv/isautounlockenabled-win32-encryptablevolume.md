---
description: Indica se o volume é desbloqueado automaticamente quando é montado.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Método IsAutoUnlockEnabled da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810494"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="57670-103">Método IsAutoUnlockEnabled da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="57670-103">IsAutoUnlockEnabled method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="57670-104">O método **IsAutoUnlockEnabled** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se o volume será desbloqueado automaticamente quando for montado (por exemplo, quando dispositivos de memória removível estiverem conectados ao computador).</span><span class="sxs-lookup"><span data-stu-id="57670-104">The **IsAutoUnlockEnabled** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume is automatically unlocked when it is mounted (for example, when removable memory devices are connected to the computer).</span></span>

## <a name="syntax"></a><span data-ttu-id="57670-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57670-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="57670-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57670-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57670-107">*IsAutoUnlockEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="57670-107">*IsAutoUnlockEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57670-108">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="57670-108">Type: **boolean**</span></span>

<span data-ttu-id="57670-109">Um valor booliano que será true se a chave externa usada para desbloquear automaticamente o volume existir e tiver sido armazenada no volume do sistema operacional em execução no momento; caso contrário, será false.</span><span class="sxs-lookup"><span data-stu-id="57670-109">A Boolean value that is true if the external key used to automatically unlock the volume exists and has been stored in the currently running operating system volume, otherwise it is false.</span></span>

</dd> <dt>

<span data-ttu-id="57670-110">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="57670-110">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57670-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57670-111">Type: **string**</span></span>

<span data-ttu-id="57670-112">Um identificador de cadeia de caracteres exclusivo que contém a ID do protetor de chave de volume criptografado associado se *IsAutoUnlockEnabled* for true.</span><span class="sxs-lookup"><span data-stu-id="57670-112">A unique string identifier that contains the associated encrypted volume key protector ID if *IsAutoUnlockEnabled* is true.</span></span>

<span data-ttu-id="57670-113">Se *IsAutoUnlockEnabled* for false, *VolumeKeyProtectorID* será uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="57670-113">If *IsAutoUnlockEnabled* is false, *VolumeKeyProtectorID* is an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57670-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57670-114">Return value</span></span>

<span data-ttu-id="57670-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57670-115">Type: **uint32**</span></span>

<span data-ttu-id="57670-116">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="57670-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="57670-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="57670-117">Return code/value</span></span>                                                                                                                                                                     | <span data-ttu-id="57670-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="57670-118">Description</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57670-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="57670-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                     | <span data-ttu-id="57670-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="57670-120">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="57670-121"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="57670-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>    | <span data-ttu-id="57670-122">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="57670-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="57670-123">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="57670-123">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="57670-124"><dt>**FVE \_ E \_ não \_ \_ VOLUME de dados**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="57670-124"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl> | <span data-ttu-id="57670-125">O método não pode ser executado para o volume do sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="57670-125">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="57670-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="57670-126">Remarks</span></span>

<span data-ttu-id="57670-127">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="57670-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="57670-128">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="57670-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="57670-129">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="57670-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="57670-130">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="57670-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57670-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57670-131">Requirements</span></span>



| <span data-ttu-id="57670-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="57670-132">Requirement</span></span> | <span data-ttu-id="57670-133">Valor</span><span class="sxs-lookup"><span data-stu-id="57670-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57670-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57670-134">Minimum supported client</span></span><br/> | <span data-ttu-id="57670-135">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="57670-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="57670-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57670-136">Minimum supported server</span></span><br/> | <span data-ttu-id="57670-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="57670-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57670-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="57670-138">Namespace</span></span><br/>                | <span data-ttu-id="57670-139">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="57670-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="57670-140">MOF</span><span class="sxs-lookup"><span data-stu-id="57670-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57670-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57670-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57670-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="57670-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57670-143">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="57670-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
