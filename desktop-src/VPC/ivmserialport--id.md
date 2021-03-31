---
title: Método de _ID IVMSerialPort (VPCCOMInterfaces. h)
description: Identificador interno da porta serial.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- _ID o método virtual PC
- _ID método virtual PC, interface IVMSerialPort
- IVMSerialPort interface virtual PC, método de _ID
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e60f301f80f24681ee297d0fb579994561155
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085519"
---
# <a name="ivmserialport_id-method"></a><span data-ttu-id="1ade3-106">Método IVMSerialPort:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="1ade3-106">IVMSerialPort::\_ID method</span></span>

<span data-ttu-id="1ade3-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1ade3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1ade3-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1ade3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1ade3-109">Recupera o identificador interno da porta serial.</span><span class="sxs-lookup"><span data-stu-id="1ade3-109">Retrieves the internal identifier of the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ade3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ade3-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="1ade3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ade3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ade3-112">*portaid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1ade3-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ade3-113">O identificador da porta serial.</span><span class="sxs-lookup"><span data-stu-id="1ade3-113">The serial port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ade3-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ade3-114">Return value</span></span>

<span data-ttu-id="1ade3-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1ade3-115">This method can return one of these values.</span></span>



| <span data-ttu-id="1ade3-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1ade3-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="1ade3-117">Description</span><span class="sxs-lookup"><span data-stu-id="1ade3-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ade3-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1ade3-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1ade3-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1ade3-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="1ade3-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="1ade3-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1ade3-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1ade3-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="1ade3-122"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="1ade3-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1ade3-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="1ade3-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="1ade3-124"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1ade3-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="1ade3-125">A configuração desta máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="1ade3-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ade3-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ade3-126">Remarks</span></span>

<span data-ttu-id="1ade3-127">Essa propriedade não pode ser usada por linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="1ade3-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ade3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ade3-128">Requirements</span></span>



| <span data-ttu-id="1ade3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ade3-129">Requirement</span></span> | <span data-ttu-id="1ade3-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1ade3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ade3-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ade3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1ade3-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1ade3-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ade3-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ade3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1ade3-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1ade3-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1ade3-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1ade3-135">End of client support</span></span><br/>    | <span data-ttu-id="1ade3-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ade3-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1ade3-137">Produto</span><span class="sxs-lookup"><span data-stu-id="1ade3-137">Product</span></span><br/>                  | <span data-ttu-id="1ade3-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1ade3-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1ade3-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ade3-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ade3-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ade3-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1ade3-141">IID</span><span class="sxs-lookup"><span data-stu-id="1ade3-141">IID</span></span><br/>                      | <span data-ttu-id="1ade3-142">IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="1ade3-142">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="1ade3-143">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1ade3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ade3-144">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="1ade3-144">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

