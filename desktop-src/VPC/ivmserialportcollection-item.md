---
title: Propriedade de item IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera o objeto de porta serial que corresponde ao índice especificado.
ms.assetid: 24ce1404-d7aa-4125-b1f9-9c54418ea205
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMSerialPortCollection
- IVMSerialPortCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Item
- IVMSerialPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be44cc92507954848c369273ae27de49df8d0ad8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784982"
---
# <a name="ivmserialportcollectionitem-property"></a><span data-ttu-id="06f01-106">Propriedade IVMSerialPortCollection:: item</span><span class="sxs-lookup"><span data-stu-id="06f01-106">IVMSerialPortCollection::Item property</span></span>

<span data-ttu-id="06f01-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="06f01-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="06f01-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="06f01-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="06f01-109">Recupera o objeto de porta serial que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="06f01-109">Retrieves the serial port object that corresponds to the specified index.</span></span>

<span data-ttu-id="06f01-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="06f01-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f01-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06f01-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long          index,
  [out, retval] IVMSerialPort **serialPort
);
```



## <a name="property-value"></a><span data-ttu-id="06f01-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="06f01-112">Property value</span></span>

<span data-ttu-id="06f01-113">O objeto [**IVMSerialPort**](ivmserialport.md) .</span><span class="sxs-lookup"><span data-stu-id="06f01-113">The [**IVMSerialPort**](ivmserialport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06f01-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="06f01-114">Error codes</span></span>



| <span data-ttu-id="06f01-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="06f01-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="06f01-116">Significado</span><span class="sxs-lookup"><span data-stu-id="06f01-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06f01-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="06f01-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="06f01-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="06f01-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="06f01-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="06f01-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="06f01-120">O parâmetro *SerialPort* é nulo.</span><span class="sxs-lookup"><span data-stu-id="06f01-120">The *serialPort* parameter is NULL.</span></span> <br/>                                                |
| <dl> <span data-ttu-id="06f01-121"><dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="06f01-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="06f01-122">O índice do item solicitado não corresponde a um item nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="06f01-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="06f01-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="06f01-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="06f01-124">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="06f01-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="06f01-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="06f01-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="06f01-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="06f01-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="06f01-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06f01-127">Requirements</span></span>



| <span data-ttu-id="06f01-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="06f01-128">Requirement</span></span> | <span data-ttu-id="06f01-129">Valor</span><span class="sxs-lookup"><span data-stu-id="06f01-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06f01-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06f01-130">Minimum supported client</span></span><br/> | <span data-ttu-id="06f01-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="06f01-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06f01-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06f01-132">Minimum supported server</span></span><br/> | <span data-ttu-id="06f01-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="06f01-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="06f01-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="06f01-134">End of client support</span></span><br/>    | <span data-ttu-id="06f01-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06f01-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="06f01-136">Produto</span><span class="sxs-lookup"><span data-stu-id="06f01-136">Product</span></span><br/>                  | <span data-ttu-id="06f01-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="06f01-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="06f01-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06f01-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="06f01-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="06f01-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="06f01-140">IID</span><span class="sxs-lookup"><span data-stu-id="06f01-140">IID</span></span><br/>                      | <span data-ttu-id="06f01-141">IID \_ IVMSerialPortCollection é definido como dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="06f01-141">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="06f01-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="06f01-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f01-143">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="06f01-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="06f01-144">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="06f01-144">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

