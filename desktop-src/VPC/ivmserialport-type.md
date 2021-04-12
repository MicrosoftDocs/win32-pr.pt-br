---
title: Propriedade do tipo IVMSerialPort (VPCCOMInterfaces. h)
description: Recupera o tipo da porta serial.
ms.assetid: 0ec9c9d7-9387-458e-befe-42d58c38df35
keywords:
- Propriedade de tipo Virtual PC
- Propriedade de tipo Virtual PC, interface IVMSerialPort
- IVMSerialPort interface virtual PC, Propriedade Type
topic_type:
- apiref
api_name:
- IVMSerialPort.Type
- IVMSerialPort.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ab32ba6e205911fca85474c047e24b7ad7f1f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455261"
---
# <a name="ivmserialporttype-property"></a><span data-ttu-id="f8a6a-106">Propriedade IVMSerialPort:: Type</span><span class="sxs-lookup"><span data-stu-id="f8a6a-106">IVMSerialPort::Type property</span></span>

<span data-ttu-id="f8a6a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f8a6a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f8a6a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f8a6a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f8a6a-109">Recupera o tipo da porta serial.</span><span class="sxs-lookup"><span data-stu-id="f8a6a-109">Retrieves the type of the serial port.</span></span>

<span data-ttu-id="f8a6a-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f8a6a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a6a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8a6a-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMSerialPortType *portType
);
```



## <a name="property-value"></a><span data-ttu-id="f8a6a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f8a6a-112">Property value</span></span>

<span data-ttu-id="f8a6a-113">O tipo de porta serial.</span><span class="sxs-lookup"><span data-stu-id="f8a6a-113">The type of serial port.</span></span> <span data-ttu-id="f8a6a-114">Para obter uma lista de valores, consulte [**VMSerialPortType**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="f8a6a-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="f8a6a-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f8a6a-115">Error codes</span></span>



| <span data-ttu-id="f8a6a-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="f8a6a-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f8a6a-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f8a6a-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8a6a-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f8a6a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f8a6a-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f8a6a-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f8a6a-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="f8a6a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f8a6a-121">O parâmetro é NULL.</span><span class="sxs-lookup"><span data-stu-id="f8a6a-121">The parameter is NULL.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f8a6a-122"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f8a6a-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f8a6a-123">A configuração desta máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="f8a6a-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="f8a6a-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="f8a6a-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f8a6a-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="f8a6a-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="f8a6a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8a6a-126">Requirements</span></span>



| <span data-ttu-id="f8a6a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a6a-127">Requirement</span></span> | <span data-ttu-id="f8a6a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f8a6a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a6a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8a6a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a6a-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f8a6a-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8a6a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8a6a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a6a-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f8a6a-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f8a6a-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f8a6a-133">End of client support</span></span><br/>    | <span data-ttu-id="f8a6a-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8a6a-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f8a6a-135">Produto</span><span class="sxs-lookup"><span data-stu-id="f8a6a-135">Product</span></span><br/>                  | <span data-ttu-id="f8a6a-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f8a6a-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f8a6a-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8a6a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a6a-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a6a-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f8a6a-139">IID</span><span class="sxs-lookup"><span data-stu-id="f8a6a-139">IID</span></span><br/>                      | <span data-ttu-id="f8a6a-140">IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="f8a6a-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="f8a6a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8a6a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a6a-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="f8a6a-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

