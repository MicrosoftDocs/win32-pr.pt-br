---
title: Propriedade IVMVirtualMachine ChassisAssetTag (VPCCOMInterfaces. h)
description: Marca de ativo do chassi.
ms.assetid: 469816a8-3078-4960-a5e1-79d65b5fc8fc
keywords:
- Propriedade ChassisAssetTag Virtual PC
- Propriedade ChassisAssetTag Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade ChassisAssetTag
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisAssetTag
- IVMVirtualMachine.get_ChassisAssetTag
- IVMVirtualMachine.put_ChassisAssetTag
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d02f71907121354c4d937436366548d41f9944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824538"
---
# <a name="ivmvirtualmachinechassisassettag-property"></a><span data-ttu-id="1e55b-106">Propriedade IVMVirtualMachine:: ChassisAssetTag</span><span class="sxs-lookup"><span data-stu-id="1e55b-106">IVMVirtualMachine::ChassisAssetTag property</span></span>

<span data-ttu-id="1e55b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1e55b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1e55b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1e55b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1e55b-109">Recupera e define a marca de ativo do chassi.</span><span class="sxs-lookup"><span data-stu-id="1e55b-109">Retrieves and sets the chassis asset tag.</span></span>

<span data-ttu-id="1e55b-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1e55b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e55b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e55b-111">Syntax</span></span>


```C++
HRESULT put_ChassisAssetTag(
  [in]          BSTR chassisAssetTag
);

HRESULT get_ChassisAssetTag(
  [out, retval] BSTR *chassisAssetTag
);
```



## <a name="property-value"></a><span data-ttu-id="1e55b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1e55b-112">Property value</span></span>

<span data-ttu-id="1e55b-113">Especifica a marca de ativo do chassi.</span><span class="sxs-lookup"><span data-stu-id="1e55b-113">Specifies the chassis asset tag.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1e55b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1e55b-114">Error codes</span></span>



| <span data-ttu-id="1e55b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="1e55b-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="1e55b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1e55b-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e55b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="1e55b-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1e55b-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1e55b-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="1e55b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="1e55b-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1e55b-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="1e55b-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="1e55b-122">O parâmetro é maior que 32 caracteres, uma cadeia de caracteres vazia ou não é válido.</span><span class="sxs-lookup"><span data-stu-id="1e55b-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="1e55b-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="1e55b-124">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="1e55b-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1e55b-125"><dt>VM \_ E \_ VM \_ em execução \_ ou \_ salvas</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="1e55b-126">A máquina virtual está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="1e55b-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="1e55b-127"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="1e55b-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="1e55b-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="1e55b-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="1e55b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e55b-129">Remarks</span></span>

<span data-ttu-id="1e55b-130">Essa propriedade não conterá informações válidas até que a máquina virtual seja iniciada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="1e55b-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="1e55b-131">Uma cadeia de caracteres vazia será retornada se for lida antes da inicialização inicial.</span><span class="sxs-lookup"><span data-stu-id="1e55b-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e55b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e55b-132">Requirements</span></span>



| <span data-ttu-id="1e55b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e55b-133">Requirement</span></span> | <span data-ttu-id="1e55b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="1e55b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e55b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e55b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1e55b-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1e55b-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e55b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e55b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1e55b-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1e55b-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1e55b-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1e55b-139">End of client support</span></span><br/>    | <span data-ttu-id="1e55b-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e55b-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1e55b-141">Produto</span><span class="sxs-lookup"><span data-stu-id="1e55b-141">Product</span></span><br/>                  | <span data-ttu-id="1e55b-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e55b-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1e55b-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e55b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e55b-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e55b-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1e55b-145">IID</span><span class="sxs-lookup"><span data-stu-id="1e55b-145">IID</span></span><br/>                      | <span data-ttu-id="1e55b-146">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="1e55b-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1e55b-147">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1e55b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e55b-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="1e55b-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

