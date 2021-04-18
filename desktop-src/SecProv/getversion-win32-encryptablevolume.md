---
description: Retorna a versão de metadados FVE do volume.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Método GetVersion da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796356"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7042b-103">Método GetVersion da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="7042b-103">GetVersion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7042b-104">O método **GetVersion** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) retorna a versão de metadados FVE do volume.</span><span class="sxs-lookup"><span data-stu-id="7042b-104">The **GetVersion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the FVE metadata version of the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="7042b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7042b-105">Syntax</span></span>


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a><span data-ttu-id="7042b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7042b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7042b-107">*Versão* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7042b-107">*Version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7042b-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7042b-108">Type: **uint32**</span></span>

<span data-ttu-id="7042b-109">Um inteiro sem sinal que indica a versão de metadados do volume.</span><span class="sxs-lookup"><span data-stu-id="7042b-109">An unsigned integer that indicates the metadata version of the volume.</span></span>



| <span data-ttu-id="7042b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7042b-110">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="7042b-111">Significado</span><span class="sxs-lookup"><span data-stu-id="7042b-111">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="7042b-112"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="7042b-112"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="7042b-113">O sistema operacional é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="7042b-113">The operating system is unknown.</span></span><br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <span data-ttu-id="7042b-114"><dt>**Vista**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7042b-114"><dt>**Vista**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="7042b-115">Formato do Windows Vista, o que significa que o volume foi protegido com o BitLocker em um computador que executa o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7042b-115">Windows Vista format, meaning that the volume was protected with BitLocker on a computer running Windows Vista.</span></span><br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <span data-ttu-id="7042b-116"><dt>**Win7**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7042b-116"><dt>**Win7**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="7042b-117">Formato do Windows 7, o que significa que o volume foi protegido com o BitLocker em um computador que executa o Windows 7 ou o formato de metadados foi atualizado usando o método [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="7042b-117">Windows 7 format, meaning that the volume was protected with BitLocker on a computer running Windows 7 or the metadata format was upgraded by using the [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) method.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7042b-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7042b-118">Return value</span></span>

<span data-ttu-id="7042b-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7042b-119">Type: **uint32**</span></span>

<span data-ttu-id="7042b-120">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="7042b-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="7042b-121">Se o volume já estiver desbloqueado e nenhum outro erro ocorrer, esse método retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7042b-121">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="7042b-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7042b-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="7042b-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="7042b-123">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="7042b-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7042b-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                       | <span data-ttu-id="7042b-125">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7042b-125">The method succeeded.</span></span><br/>                               |
| <dl> <span data-ttu-id="7042b-126"><dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="7042b-126"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl> | <span data-ttu-id="7042b-127">O valor do parâmetro de *versão* não é válido.</span><span class="sxs-lookup"><span data-stu-id="7042b-127">The value for the *Version* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="7042b-128"><dt>**Erro \_ do \_Dados INválidos**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="7042b-128"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>       | <span data-ttu-id="7042b-129">O driver retornou um formato de dados sem suporte.</span><span class="sxs-lookup"><span data-stu-id="7042b-129">The driver returned an unsupported data format.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="7042b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="7042b-130">Remarks</span></span>

<span data-ttu-id="7042b-131">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7042b-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7042b-132">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="7042b-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7042b-133">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="7042b-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7042b-134">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7042b-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7042b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7042b-135">Requirements</span></span>



| <span data-ttu-id="7042b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7042b-136">Requirement</span></span> | <span data-ttu-id="7042b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="7042b-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7042b-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7042b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7042b-139">Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="7042b-139">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7042b-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7042b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7042b-141">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="7042b-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7042b-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="7042b-142">Namespace</span></span><br/>                | <span data-ttu-id="7042b-143">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7042b-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7042b-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7042b-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7042b-145"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7042b-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7042b-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="7042b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7042b-147">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="7042b-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
