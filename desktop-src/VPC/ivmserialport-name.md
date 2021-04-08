---
title: Propriedade nome do IVMSerialPort (VPCCOMInterfaces. h)
description: Nome da porta serial.
ms.assetid: 4d3fe008-f089-4a1b-9c90-2e0b3ded58fa
keywords:
- Propriedade do nome Virtual PC
- Propriedade de nome Virtual PC, interface IVMSerialPort
- IVMSerialPort interface virtual PC, Propriedade Name
topic_type:
- apiref
api_name:
- IVMSerialPort.Name
- IVMSerialPort.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540540e2af91647b9c77735a1c601ed62aecdbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824695"
---
# <a name="ivmserialportname-property"></a><span data-ttu-id="e8768-106">Propriedade IVMSerialPort:: Name</span><span class="sxs-lookup"><span data-stu-id="e8768-106">IVMSerialPort::Name property</span></span>

<span data-ttu-id="e8768-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e8768-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8768-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e8768-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8768-109">Recupera o nome da porta serial.</span><span class="sxs-lookup"><span data-stu-id="e8768-109">Retrieves the name of the serial port.</span></span>

<span data-ttu-id="e8768-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e8768-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8768-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8768-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="e8768-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e8768-112">Property value</span></span>

<span data-ttu-id="e8768-113">O nome da porta serial.</span><span class="sxs-lookup"><span data-stu-id="e8768-113">The name of the serial port.</span></span> <span data-ttu-id="e8768-114">Por exemplo, "COM1" para **vmSerialPort \_ HostPort**, "C: \\SerialPort.txt" para **vmSerialPort \_ textfile** ou " \\ \\ *nome_do_servidor* \\ pipe pipeName \\ " para **vmSerialPort \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="e8768-114">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e8768-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e8768-115">Error codes</span></span>



| <span data-ttu-id="e8768-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="e8768-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e8768-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e8768-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8768-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e8768-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e8768-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e8768-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="e8768-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e8768-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e8768-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e8768-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="e8768-122"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e8768-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="e8768-123">A configuração desta máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="e8768-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="e8768-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e8768-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e8768-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e8768-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="e8768-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8768-126">Requirements</span></span>



| <span data-ttu-id="e8768-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8768-127">Requirement</span></span> | <span data-ttu-id="e8768-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e8768-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8768-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8768-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e8768-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8768-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8768-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8768-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e8768-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e8768-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e8768-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e8768-133">End of client support</span></span><br/>    | <span data-ttu-id="e8768-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8768-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8768-135">Produto</span><span class="sxs-lookup"><span data-stu-id="e8768-135">Product</span></span><br/>                  | <span data-ttu-id="e8768-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8768-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e8768-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8768-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8768-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8768-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e8768-139">IID</span><span class="sxs-lookup"><span data-stu-id="e8768-139">IID</span></span><br/>                      | <span data-ttu-id="e8768-140">IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="e8768-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="e8768-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8768-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8768-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="e8768-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

