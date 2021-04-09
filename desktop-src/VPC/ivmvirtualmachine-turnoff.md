---
title: Método de desativação de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Desativa a máquina virtual.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- Método de desativação Virtual PC
- Método de desativação Virtual PC, interface IVMVirtualMachine
- Virtual PC de interface IVMVirtualMachine, método de desativação
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27a5b14955fcc8a060c49932e3fa4f238497a567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009626"
---
# <a name="ivmvirtualmachineturnoff-method"></a><span data-ttu-id="4dd7e-106">Método IVMVirtualMachine:: inativação</span><span class="sxs-lookup"><span data-stu-id="4dd7e-106">IVMVirtualMachine::TurnOff method</span></span>

<span data-ttu-id="4dd7e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4dd7e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4dd7e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4dd7e-109">Desativa a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-109">Turns off the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd7e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4dd7e-110">Syntax</span></span>


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a><span data-ttu-id="4dd7e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4dd7e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd7e-112">*turnOffTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4dd7e-112">*turnOffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd7e-113">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar o progresso da conclusão da sequência de desativação da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's turnoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dd7e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4dd7e-114">Return value</span></span>

<span data-ttu-id="4dd7e-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4dd7e-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4dd7e-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="4dd7e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4dd7e-117">Description</span></span>                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4dd7e-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4dd7e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="4dd7e-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-119">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="4dd7e-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="4dd7e-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="4dd7e-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-121">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4dd7e-122"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="4dd7e-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="4dd7e-123">O chamador deve ter permissões de acesso de execução para desligar esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-123">The caller must have execute access permissions to turn off this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="4dd7e-124"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4dd7e-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="4dd7e-125">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-125">The virtual machine is not running.</span></span><br/>                                               |
| <dl> <span data-ttu-id="4dd7e-126"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4dd7e-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="4dd7e-127">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-127">The configuration is unknown.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="4dd7e-128"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="4dd7e-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="4dd7e-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-129">An unexpected error has occurred.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="4dd7e-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dd7e-130">Remarks</span></span>

<span data-ttu-id="4dd7e-131">Esse método desativa a máquina virtual da mesma maneira que desliga a energia em um computador físico.</span><span class="sxs-lookup"><span data-stu-id="4dd7e-131">This method turns off the virtual machine in the same manner as turning the power off on a physical machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd7e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dd7e-132">Requirements</span></span>



| <span data-ttu-id="4dd7e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dd7e-133">Requirement</span></span> | <span data-ttu-id="4dd7e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="4dd7e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd7e-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4dd7e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4dd7e-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4dd7e-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4dd7e-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4dd7e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4dd7e-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4dd7e-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4dd7e-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4dd7e-139">End of client support</span></span><br/>    | <span data-ttu-id="4dd7e-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4dd7e-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4dd7e-141">Produto</span><span class="sxs-lookup"><span data-stu-id="4dd7e-141">Product</span></span><br/>                  | <span data-ttu-id="4dd7e-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4dd7e-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4dd7e-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4dd7e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dd7e-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dd7e-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4dd7e-145">IID</span><span class="sxs-lookup"><span data-stu-id="4dd7e-145">IID</span></span><br/>                      | <span data-ttu-id="4dd7e-146">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4dd7e-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4dd7e-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dd7e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dd7e-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="4dd7e-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

