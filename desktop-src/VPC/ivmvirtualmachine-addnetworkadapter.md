---
title: Método IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces. h)
description: Adiciona uma interface de rede à máquina virtual.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- AddNetworkAdapter do método virtual PC
- Método AddNetworkAdapter Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método AddNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763806"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a><span data-ttu-id="940e1-106">Método IVMVirtualMachine:: AddNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="940e1-106">IVMVirtualMachine::AddNetworkAdapter method</span></span>

<span data-ttu-id="940e1-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="940e1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="940e1-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="940e1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="940e1-109">Adiciona uma interface de rede à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="940e1-109">Adds a network interface to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="940e1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="940e1-110">Syntax</span></span>


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="940e1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="940e1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940e1-112">*adaptador* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="940e1-112">*networkAdapter* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="940e1-113">Um objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="940e1-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940e1-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="940e1-114">Return value</span></span>

<span data-ttu-id="940e1-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="940e1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="940e1-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="940e1-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="940e1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="940e1-117">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="940e1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="940e1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="940e1-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="940e1-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="940e1-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="940e1-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="940e1-121">O parâmetro *adaptador* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="940e1-121">The *networkAdapter* parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="940e1-122"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="940e1-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="940e1-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="940e1-123">The configuration is unknown.</span></span><br/>                        |
| <dl> <span data-ttu-id="940e1-124"><dt>**VM \_ E \_ pref \_ \_ valor ilegal**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="940e1-124"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>   | <span data-ttu-id="940e1-125">Não é possível adicionar mais de quatro (4) adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="940e1-125">No more than four (4) network adapters can be added.</span></span><br/> |
| <dl> <span data-ttu-id="940e1-126"><dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="940e1-126"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="940e1-127">A máquina virtual está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="940e1-127">The virtual machine is in a running or saved state.</span></span><br/>  |
| <dl> <span data-ttu-id="940e1-128"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="940e1-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="940e1-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="940e1-129">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="940e1-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="940e1-130">Remarks</span></span>

<span data-ttu-id="940e1-131">Você só pode adicionar uma nova interface de rede a uma máquina virtual parada.</span><span class="sxs-lookup"><span data-stu-id="940e1-131">You can only add a new network interface to a stopped virtual machine.</span></span> <span data-ttu-id="940e1-132">O adaptador de rede recém-criado não está conectado a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="940e1-132">The newly created network adapter is not connected to a virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="940e1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="940e1-133">Requirements</span></span>



| <span data-ttu-id="940e1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="940e1-134">Requirement</span></span> | <span data-ttu-id="940e1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="940e1-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="940e1-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="940e1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="940e1-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="940e1-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="940e1-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="940e1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="940e1-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="940e1-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="940e1-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="940e1-140">End of client support</span></span><br/>    | <span data-ttu-id="940e1-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="940e1-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="940e1-142">Produto</span><span class="sxs-lookup"><span data-stu-id="940e1-142">Product</span></span><br/>                  | <span data-ttu-id="940e1-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="940e1-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="940e1-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="940e1-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="940e1-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="940e1-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="940e1-146">IID</span><span class="sxs-lookup"><span data-stu-id="940e1-146">IID</span></span><br/>                      | <span data-ttu-id="940e1-147">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="940e1-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="940e1-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="940e1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940e1-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="940e1-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

