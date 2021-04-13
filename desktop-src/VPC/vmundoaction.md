---
title: Enumeração VMUndoAction (VPCCOMInterfaces. h)
description: Especifica o que acontece para desfazer unidades quando uma máquina virtual é desligada ou desativada.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- VMUndoAction de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10917a5fb8d00e16a28f4b175237484b977cf914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499750"
---
# <a name="vmundoaction-enumeration"></a><span data-ttu-id="a77bb-104">Enumeração VMUndoAction</span><span class="sxs-lookup"><span data-stu-id="a77bb-104">VMUndoAction enumeration</span></span>

<span data-ttu-id="a77bb-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a77bb-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a77bb-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a77bb-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a77bb-107">Especifica o que acontece para desfazer unidades quando uma máquina virtual é desligada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="a77bb-107">Specifies what happens to undo drives when a virtual machine is shut down or turned off.</span></span>

## <a name="syntax"></a><span data-ttu-id="a77bb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a77bb-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a><span data-ttu-id="a77bb-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="a77bb-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a77bb-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**\_descartar vmUndoAction**</span><span class="sxs-lookup"><span data-stu-id="a77bb-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction\_Discard**</span></span>
</dt> <dd>

<span data-ttu-id="a77bb-111">Descartar as unidades de desfazer; as unidades pai permanecem inalteradas.</span><span class="sxs-lookup"><span data-stu-id="a77bb-111">Discard the undo drives; the parent drives remain unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="a77bb-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction \_ manter**</span><span class="sxs-lookup"><span data-stu-id="a77bb-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction\_Keep**</span></span>
</dt> <dd>

<span data-ttu-id="a77bb-113">Manter as unidades de desfazer; as unidades pai permanecem inalteradas, mas as alterações serão mantidas na próxima vez que a máquina virtual for iniciada.</span><span class="sxs-lookup"><span data-stu-id="a77bb-113">Keep the undo drives; the parent drives remain unchanged, but changes will be maintained the next time the virtual machine starts.</span></span>

</dd> <dt>

<span data-ttu-id="a77bb-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction \_ confirmação**</span><span class="sxs-lookup"><span data-stu-id="a77bb-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction\_Commit**</span></span>
</dt> <dd>

<span data-ttu-id="a77bb-115">Confirme as alterações nas unidades pai.</span><span class="sxs-lookup"><span data-stu-id="a77bb-115">Commit changes to the parent drives.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a77bb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a77bb-116">Requirements</span></span>



| <span data-ttu-id="a77bb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a77bb-117">Requirement</span></span> | <span data-ttu-id="a77bb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a77bb-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a77bb-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a77bb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a77bb-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a77bb-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a77bb-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a77bb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a77bb-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a77bb-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a77bb-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a77bb-123">End of client support</span></span><br/>    | <span data-ttu-id="a77bb-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a77bb-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a77bb-125">Produto</span><span class="sxs-lookup"><span data-stu-id="a77bb-125">Product</span></span><br/>                  | <span data-ttu-id="a77bb-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a77bb-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a77bb-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a77bb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a77bb-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a77bb-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a77bb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a77bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a77bb-130">**IVMVirtualMachine:: UndoAction**</span><span class="sxs-lookup"><span data-stu-id="a77bb-130">**IVMVirtualMachine::UndoAction**</span></span>](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

