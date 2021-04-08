---
title: Propriedade IVMVirtualMachine ChassisSerialNumber (VPCCOMInterfaces. h)
description: Número de série do chassi.
ms.assetid: 03e02e6e-6819-4052-a0e0-9167eb5fdf4b
keywords:
- Propriedade ChassisSerialNumber Virtual PC
- Propriedade ChassisSerialNumber Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade ChassisSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisSerialNumber
- IVMVirtualMachine.get_ChassisSerialNumber
- IVMVirtualMachine.put_ChassisSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00edbac12248f624ac06d1f7b88c3782c3f5a3df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009463"
---
# <a name="ivmvirtualmachinechassisserialnumber-property"></a><span data-ttu-id="6e39a-106">Propriedade IVMVirtualMachine:: ChassisSerialNumber</span><span class="sxs-lookup"><span data-stu-id="6e39a-106">IVMVirtualMachine::ChassisSerialNumber property</span></span>

<span data-ttu-id="6e39a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6e39a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6e39a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6e39a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6e39a-109">Recupera e define o número de série do chassi.</span><span class="sxs-lookup"><span data-stu-id="6e39a-109">Retrieves and sets the chassis serial number.</span></span>

<span data-ttu-id="6e39a-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6e39a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e39a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e39a-111">Syntax</span></span>


```C++
HRESULT put_ChassisSerialNumber(
  [in]          BSTR chasisSerialNumber
);

HRESULT get_ChassisSerialNumber(
  [out, retval] BSTR *chassisSerialNumber
);
```



## <a name="property-value"></a><span data-ttu-id="6e39a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6e39a-112">Property value</span></span>

<span data-ttu-id="6e39a-113">Especifica o número de série do chassi.</span><span class="sxs-lookup"><span data-stu-id="6e39a-113">Specifies the chassis serial number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e39a-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6e39a-114">Error codes</span></span>



| <span data-ttu-id="6e39a-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="6e39a-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="6e39a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="6e39a-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e39a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6e39a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="6e39a-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6e39a-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="6e39a-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6e39a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="6e39a-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6e39a-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="6e39a-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6e39a-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="6e39a-122">O parâmetro é maior que 32 caracteres, uma cadeia de caracteres vazia ou não é válido.</span><span class="sxs-lookup"><span data-stu-id="6e39a-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="6e39a-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6e39a-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="6e39a-124">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="6e39a-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="6e39a-125"><dt>VM \_ E \_ VM \_ em execução \_ ou \_ salvas</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="6e39a-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="6e39a-126">A máquina virtual está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="6e39a-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="6e39a-127"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6e39a-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="6e39a-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6e39a-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="6e39a-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e39a-129">Remarks</span></span>

<span data-ttu-id="6e39a-130">Essa propriedade não conterá informações válidas até que a máquina virtual seja iniciada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="6e39a-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="6e39a-131">Uma cadeia de caracteres vazia será retornada se for lida antes da inicialização inicial.</span><span class="sxs-lookup"><span data-stu-id="6e39a-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e39a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e39a-132">Requirements</span></span>



| <span data-ttu-id="6e39a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e39a-133">Requirement</span></span> | <span data-ttu-id="6e39a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="6e39a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e39a-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e39a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6e39a-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6e39a-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e39a-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e39a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6e39a-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6e39a-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6e39a-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6e39a-139">End of client support</span></span><br/>    | <span data-ttu-id="6e39a-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e39a-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6e39a-141">Produto</span><span class="sxs-lookup"><span data-stu-id="6e39a-141">Product</span></span><br/>                  | <span data-ttu-id="6e39a-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6e39a-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6e39a-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e39a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e39a-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e39a-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6e39a-145">IID</span><span class="sxs-lookup"><span data-stu-id="6e39a-145">IID</span></span><br/>                      | <span data-ttu-id="6e39a-146">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="6e39a-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6e39a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e39a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e39a-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="6e39a-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

