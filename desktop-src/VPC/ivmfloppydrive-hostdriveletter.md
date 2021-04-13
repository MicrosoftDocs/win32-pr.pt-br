---
title: Propriedade IVMFloppyDrive HostDriveLetter (VPCCOMInterfaces. h)
description: A letra da unidade do host à qual a unidade de disquete está conectada.
ms.assetid: 16d11e06-e3bc-4a4a-850d-f7b4122e6af9
keywords:
- Propriedade HostDriveLetter Virtual PC
- Propriedade HostDriveLetter Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface virtual PC, Propriedade HostDriveLetter
topic_type:
- apiref
api_name:
- IVMFloppyDrive.HostDriveLetter
- IVMFloppyDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4896699dd3547eb3488e2fc085b5b2c54de827b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499416"
---
# <a name="ivmfloppydrivehostdriveletter-property"></a><span data-ttu-id="2b38b-106">Propriedade IVMFloppyDrive:: HostDriveLetter</span><span class="sxs-lookup"><span data-stu-id="2b38b-106">IVMFloppyDrive::HostDriveLetter property</span></span>

<span data-ttu-id="2b38b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2b38b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2b38b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2b38b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2b38b-109">Recupera a letra da unidade do host à qual a unidade de disquete está anexada.</span><span class="sxs-lookup"><span data-stu-id="2b38b-109">Retrieves the letter of the host drive to which the floppy drive is attached.</span></span>

<span data-ttu-id="2b38b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2b38b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b38b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b38b-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="2b38b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2b38b-112">Property value</span></span>

<span data-ttu-id="2b38b-113">A letra da unidade de disquete física.</span><span class="sxs-lookup"><span data-stu-id="2b38b-113">The letter of the physical floppy drive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2b38b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="2b38b-114">Error codes</span></span>



| <span data-ttu-id="2b38b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="2b38b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2b38b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="2b38b-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b38b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2b38b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2b38b-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2b38b-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="2b38b-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="2b38b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2b38b-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b38b-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="2b38b-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2b38b-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="2b38b-122">A configuração desta máquina virtual não é válida ou não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="2b38b-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="2b38b-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="2b38b-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2b38b-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="2b38b-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="2b38b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b38b-125">Requirements</span></span>



| <span data-ttu-id="2b38b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b38b-126">Requirement</span></span> | <span data-ttu-id="2b38b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2b38b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b38b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b38b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2b38b-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2b38b-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b38b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b38b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2b38b-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2b38b-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2b38b-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2b38b-132">End of client support</span></span><br/>    | <span data-ttu-id="2b38b-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b38b-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2b38b-134">Produto</span><span class="sxs-lookup"><span data-stu-id="2b38b-134">Product</span></span><br/>                  | <span data-ttu-id="2b38b-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2b38b-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2b38b-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b38b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b38b-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b38b-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2b38b-138">IID</span><span class="sxs-lookup"><span data-stu-id="2b38b-138">IID</span></span><br/>                      | <span data-ttu-id="2b38b-139">IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="2b38b-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2b38b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b38b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b38b-141">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="2b38b-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

