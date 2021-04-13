---
title: Método IVMGuestOS InstallIntegrationComponents (VPCCOMInterfaces. h)
description: Localiza e instala os componentes de integração mais recentes no sistema operacional convidado.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- InstallIntegrationComponents do método virtual PC
- Método InstallIntegrationComponents Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, método InstallIntegrationComponents
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879ded1464ebd310e1d1da4e3a952dc086600350
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369260"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a><span data-ttu-id="b9599-106">Método IVMGuestOS:: InstallIntegrationComponents</span><span class="sxs-lookup"><span data-stu-id="b9599-106">IVMGuestOS::InstallIntegrationComponents method</span></span>

<span data-ttu-id="b9599-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b9599-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b9599-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b9599-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b9599-109">Localiza e instala os componentes de integração mais recentes no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="b9599-109">Locates and installs the latest Integration Components into the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9599-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9599-110">Syntax</span></span>


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a><span data-ttu-id="b9599-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9599-111">Parameters</span></span>

<span data-ttu-id="b9599-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b9599-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9599-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9599-113">Return value</span></span>

<span data-ttu-id="b9599-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b9599-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b9599-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b9599-115">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="b9599-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9599-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9599-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b9599-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b9599-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b9599-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b9599-119"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b9599-119"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                       | <span data-ttu-id="b9599-120">A máquina virtual deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="b9599-120">The virtual machine must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="b9599-121"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b9599-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="b9599-122">Não foi possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9599-122">The virtual machine could not be found.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b9599-123"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b9599-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="b9599-124">A máquina virtual não tem uma unidade de DVD vazia.</span><span class="sxs-lookup"><span data-stu-id="b9599-124">The virtual machine does not have an empty DVD drive.</span></span><br/>                       |
| <dl> <span data-ttu-id="b9599-125"><dt>**VM \_ \_Falha de \_ desmontagem \_ de mídia E**</dt> <dt>0xA0040508</dt></span><span class="sxs-lookup"><span data-stu-id="b9599-125"><dt>**VM\_E\_MEDIA\_UNMOUNT\_FAIL**</dt> <dt>0xA0040508</dt></span></span> </dl>                   | <span data-ttu-id="b9599-126">Falha na tentativa de desmontar a mídia da unidade de DVD da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9599-126">The attempt to unmount the media from the virtual machine DVD drive failed.</span></span><br/> |
| <dl> <span data-ttu-id="b9599-127"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b9599-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b9599-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b9599-128">An unexpected error has occurred.</span></span><br/>                                           |
| <dl> <span data-ttu-id="b9599-129"><dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="b9599-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="b9599-130">O sistema não pode localizar o arquivo ISO para os componentes de integração.</span><span class="sxs-lookup"><span data-stu-id="b9599-130">The system cannot find the ISO file for the Integration Components.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="b9599-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9599-131">Requirements</span></span>



| <span data-ttu-id="b9599-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9599-132">Requirement</span></span> | <span data-ttu-id="b9599-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b9599-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9599-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9599-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b9599-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b9599-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9599-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9599-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b9599-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b9599-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b9599-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b9599-138">End of client support</span></span><br/>    | <span data-ttu-id="b9599-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9599-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b9599-140">Produto</span><span class="sxs-lookup"><span data-stu-id="b9599-140">Product</span></span><br/>                  | <span data-ttu-id="b9599-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b9599-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b9599-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9599-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9599-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9599-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b9599-144">IID</span><span class="sxs-lookup"><span data-stu-id="b9599-144">IID</span></span><br/>                      | <span data-ttu-id="b9599-145">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="b9599-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b9599-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9599-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9599-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="b9599-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

