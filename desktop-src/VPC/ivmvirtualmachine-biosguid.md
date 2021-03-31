---
title: Propriedade IVMVirtualMachine BIOSGUID (VPCCOMInterfaces. h)
description: O GUID do BIOS.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- Propriedade BIOSGUID Virtual PC
- Propriedade BIOSGUID Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade BIOSGUID
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824377"
---
# <a name="ivmvirtualmachinebiosguid-property"></a><span data-ttu-id="afc73-106">Propriedade IVMVirtualMachine:: BIOSGUID</span><span class="sxs-lookup"><span data-stu-id="afc73-106">IVMVirtualMachine::BIOSGUID property</span></span>

<span data-ttu-id="afc73-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="afc73-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="afc73-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="afc73-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="afc73-109">Recupera e define o GUID do BIOS.</span><span class="sxs-lookup"><span data-stu-id="afc73-109">Retrieves and sets the BIOS GUID.</span></span>

<span data-ttu-id="afc73-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="afc73-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc73-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afc73-111">Syntax</span></span>


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a><span data-ttu-id="afc73-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="afc73-112">Property value</span></span>

<span data-ttu-id="afc73-113">Especifica o GUID do BIOS.</span><span class="sxs-lookup"><span data-stu-id="afc73-113">Specifies the BIOS GUID.</span></span> <span data-ttu-id="afc73-114">Inclua as chaves esquerda e direita em volta dos dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="afc73-114">Include left and right braces around the hex digits.</span></span>

## <a name="error-codes"></a><span data-ttu-id="afc73-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="afc73-115">Error codes</span></span>



| <span data-ttu-id="afc73-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="afc73-116">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="afc73-117">Significado</span><span class="sxs-lookup"><span data-stu-id="afc73-117">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="afc73-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="afc73-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="afc73-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="afc73-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="afc73-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="afc73-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="afc73-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="afc73-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="afc73-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="afc73-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="afc73-123">O parâmetro não é válido ou é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="afc73-123">The parameter is not valid or is an empty string.</span></span><br/>   |
| <dl> <span data-ttu-id="afc73-124"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="afc73-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="afc73-125">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="afc73-125">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="afc73-126"><dt>VM \_ E \_ VM \_ em execução \_ ou \_ salvas</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="afc73-126"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="afc73-127">A máquina virtual está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="afc73-127">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="afc73-128"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="afc73-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="afc73-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="afc73-129">An unexpected error has occurred.</span></span><br/>                   |



## <a name="remarks"></a><span data-ttu-id="afc73-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="afc73-130">Remarks</span></span>

<span data-ttu-id="afc73-131">Essa propriedade não conterá informações válidas até que a máquina virtual seja iniciada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="afc73-131">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="afc73-132">Uma cadeia de caracteres vazia será retornada se for lida antes da inicialização inicial.</span><span class="sxs-lookup"><span data-stu-id="afc73-132">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc73-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afc73-133">Requirements</span></span>



| <span data-ttu-id="afc73-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc73-134">Requirement</span></span> | <span data-ttu-id="afc73-135">Valor</span><span class="sxs-lookup"><span data-stu-id="afc73-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc73-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afc73-136">Minimum supported client</span></span><br/> | <span data-ttu-id="afc73-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="afc73-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="afc73-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afc73-138">Minimum supported server</span></span><br/> | <span data-ttu-id="afc73-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="afc73-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="afc73-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="afc73-140">End of client support</span></span><br/>    | <span data-ttu-id="afc73-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="afc73-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="afc73-142">Produto</span><span class="sxs-lookup"><span data-stu-id="afc73-142">Product</span></span><br/>                  | <span data-ttu-id="afc73-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="afc73-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="afc73-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="afc73-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc73-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc73-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="afc73-146">IID</span><span class="sxs-lookup"><span data-stu-id="afc73-146">IID</span></span><br/>                      | <span data-ttu-id="afc73-147">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="afc73-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="afc73-148">Consulte também</span><span class="sxs-lookup"><span data-stu-id="afc73-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc73-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="afc73-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

