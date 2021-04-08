---
title: Método QueryOfflineInformation da classe Win32_TSVm
description: Recupera as propriedades do VDS (servidor de área de trabalho virtual) atual, mas somente quando o servidor estiver offline.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método QueryOfflineInformation
- Método QueryOfflineInformation Serviços de Área de Trabalho Remota, classe Win32_TSVm
- Classe Win32_TSVm Serviços de Área de Trabalho Remota, método QueryOfflineInformation
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824544"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a><span data-ttu-id="072c7-106">Método QueryOfflineInformation da classe Win32 \_ TSVm</span><span class="sxs-lookup"><span data-stu-id="072c7-106">QueryOfflineInformation method of the Win32\_TSVm class</span></span>

<span data-ttu-id="072c7-107">Recupera as propriedades do VDS (servidor de área de trabalho virtual) atual, mas somente quando o servidor estiver offline.</span><span class="sxs-lookup"><span data-stu-id="072c7-107">Retrieves the properties of the current virtual desktop server (VDS), but only when the server is offline.</span></span>

## <a name="syntax"></a><span data-ttu-id="072c7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="072c7-108">Syntax</span></span>


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="072c7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="072c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="072c7-110">*Criar* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="072c7-110">*Build* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072c7-111">Em caso de sucesso, retorna a versão de compilação do VDS.</span><span class="sxs-lookup"><span data-stu-id="072c7-111">On a success, returns the build version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="072c7-112">*CurrentVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="072c7-112">*CurrentVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072c7-113">Em caso de sucesso, retorna a versão atual do VDS.</span><span class="sxs-lookup"><span data-stu-id="072c7-113">On a success, returns the current version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="072c7-114">*Installationtype* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="072c7-114">*InstallationType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072c7-115">Em caso de sucesso, retorna o tipo de instalação do VDS.</span><span class="sxs-lookup"><span data-stu-id="072c7-115">On a success, returns the installation type of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="072c7-116">*Edição do* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="072c7-116">*EditionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072c7-117">Em caso de sucesso, retorna a ID de edição do VDS.</span><span class="sxs-lookup"><span data-stu-id="072c7-117">On a success, returns the edition ID of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="072c7-118">*SysPrepImageState* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="072c7-118">*SysPrepImageState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072c7-119">Em caso de sucesso, retorna o estado da imagem de preparação do sistema do VDS.</span><span class="sxs-lookup"><span data-stu-id="072c7-119">On success, returns the system prep image state of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="072c7-120">*Sysprepmode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="072c7-120">*SysPrepMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072c7-121">Em caso de sucesso, retorna o modo de preparação do sistema do VDS.</span><span class="sxs-lookup"><span data-stu-id="072c7-121">On a success, returns the system prep mode of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="072c7-122">*ProcArch* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="072c7-122">*ProcArch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072c7-123">Em caso de sucesso, retorna um valor que indica a arquitetura do processador.</span><span class="sxs-lookup"><span data-stu-id="072c7-123">On a success, returns a value indicating the processor architecture.</span></span>

<dt>

<span data-ttu-id="072c7-124">0</span><span class="sxs-lookup"><span data-stu-id="072c7-124">0</span></span>
</dt> <dd>

<span data-ttu-id="072c7-125">x86</span><span class="sxs-lookup"><span data-stu-id="072c7-125">x86</span></span>

</dd> <dt>

<span data-ttu-id="072c7-126">1</span><span class="sxs-lookup"><span data-stu-id="072c7-126">1</span></span>
</dt> <dd>

<span data-ttu-id="072c7-127">amd64</span><span class="sxs-lookup"><span data-stu-id="072c7-127">amd64</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="072c7-128">*fIsVmbusCapable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="072c7-128">*fIsVmbusCapable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072c7-129">em caso de sucesso, indica se o sistema tem capacidade de VMBus.</span><span class="sxs-lookup"><span data-stu-id="072c7-129">on a success, indicates whether the system is VMBus-capable.</span></span>

</dd> <dt>

<span data-ttu-id="072c7-130">*fIsRdvIcInstalled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="072c7-130">*fIsRdvIcInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072c7-131">Em caso de sucesso, indica se o RDVIC está instalado.</span><span class="sxs-lookup"><span data-stu-id="072c7-131">On a success, indicates if RDVIC is installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="072c7-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="072c7-132">Return value</span></span>

<span data-ttu-id="072c7-133">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="072c7-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="072c7-134">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="072c7-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="072c7-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="072c7-135">Requirements</span></span>



| <span data-ttu-id="072c7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="072c7-136">Requirement</span></span> | <span data-ttu-id="072c7-137">Valor</span><span class="sxs-lookup"><span data-stu-id="072c7-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="072c7-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="072c7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="072c7-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="072c7-139">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="072c7-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="072c7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="072c7-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="072c7-141">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="072c7-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="072c7-142">Namespace</span></span><br/>                | <span data-ttu-id="072c7-143">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="072c7-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="072c7-144">MOF</span><span class="sxs-lookup"><span data-stu-id="072c7-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="072c7-145"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="072c7-145"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="072c7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="072c7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="072c7-147"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="072c7-147"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="072c7-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="072c7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="072c7-149">**\_TSVm Win32**</span><span class="sxs-lookup"><span data-stu-id="072c7-149">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





