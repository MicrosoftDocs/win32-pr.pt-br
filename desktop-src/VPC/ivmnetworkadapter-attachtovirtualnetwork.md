---
title: Método IVMNetworkAdapter AttachToVirtualNetwork (VPCCOMInterfaces. h)
description: Anexa a interface de rede à rede virtual especificada.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- AttachToVirtualNetwork do método virtual PC
- Método AttachToVirtualNetwork Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, método AttachToVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455303"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a><span data-ttu-id="873cd-106">Método IVMNetworkAdapter:: AttachToVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="873cd-106">IVMNetworkAdapter::AttachToVirtualNetwork method</span></span>

<span data-ttu-id="873cd-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="873cd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="873cd-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="873cd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="873cd-109">Anexa a interface de rede à rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="873cd-109">Attaches the network interface to the specified virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="873cd-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="873cd-110">Syntax</span></span>


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="873cd-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="873cd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="873cd-112">*virtualNetwork* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="873cd-112">*virtualNetwork* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873cd-113">A rede virtual à qual esta NIC virtual será conectada.</span><span class="sxs-lookup"><span data-stu-id="873cd-113">The virtual network to which this virtual NIC will be connected.</span></span> <span data-ttu-id="873cd-114">Consulte [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="873cd-114">See [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="873cd-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="873cd-115">Return value</span></span>

<span data-ttu-id="873cd-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="873cd-116">This method can return one of these values.</span></span>



| <span data-ttu-id="873cd-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="873cd-117">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="873cd-118">Description</span><span class="sxs-lookup"><span data-stu-id="873cd-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="873cd-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="873cd-119"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                       | <span data-ttu-id="873cd-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="873cd-120">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="873cd-121"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="873cd-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="873cd-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="873cd-122">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="873cd-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="873cd-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="873cd-124">O parâmetro não contém uma rede virtual válida.</span><span class="sxs-lookup"><span data-stu-id="873cd-124">The parameter does not contain a valid virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="873cd-125"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="873cd-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="873cd-126">Acesso negado à rede virtual solicitada.</span><span class="sxs-lookup"><span data-stu-id="873cd-126">Access was denied to the requested virtual network.</span></span><br/>     |
| <dl> <span data-ttu-id="873cd-127"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="873cd-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="873cd-128">A máquina virtual é inválida ou não existe mais.</span><span class="sxs-lookup"><span data-stu-id="873cd-128">The virtual machine is invalid or no longer exists.</span></span><br/>     |
| <dl> <span data-ttu-id="873cd-129"><dt>**\_ID da \_ \_ rede virtual \_ E da VM inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="873cd-129"><dt>**VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID**</dt></span></span> </dl>                                                                        | <span data-ttu-id="873cd-130">O parâmetro não é uma rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="873cd-130">The parameter is not an existing virtual network.</span></span><br/>       |
| <dl> <span data-ttu-id="873cd-131"><dt>**obter \_ E \_ exceção**</dt></span><span class="sxs-lookup"><span data-stu-id="873cd-131"><dt>**DISP\_E\_EXCEPTION**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="873cd-132">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="873cd-132">An unexpected error has occurred.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="873cd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="873cd-133">Requirements</span></span>



| <span data-ttu-id="873cd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="873cd-134">Requirement</span></span> | <span data-ttu-id="873cd-135">Valor</span><span class="sxs-lookup"><span data-stu-id="873cd-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="873cd-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="873cd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="873cd-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="873cd-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="873cd-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="873cd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="873cd-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="873cd-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="873cd-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="873cd-140">End of client support</span></span><br/>    | <span data-ttu-id="873cd-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="873cd-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="873cd-142">Produto</span><span class="sxs-lookup"><span data-stu-id="873cd-142">Product</span></span><br/>                  | <span data-ttu-id="873cd-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="873cd-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="873cd-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="873cd-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="873cd-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="873cd-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="873cd-146">IID</span><span class="sxs-lookup"><span data-stu-id="873cd-146">IID</span></span><br/>                      | <span data-ttu-id="873cd-147">IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="873cd-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="873cd-148">Consulte também</span><span class="sxs-lookup"><span data-stu-id="873cd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873cd-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="873cd-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

