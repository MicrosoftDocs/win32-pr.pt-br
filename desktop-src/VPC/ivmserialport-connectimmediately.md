---
title: Propriedade IVMSerialPort ConnectImmediately (VPCCOMInterfaces. h)
description: Determina se a porta serial deve ser aberta sem aguardar a recepção de um comando de modem.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- Propriedade ConnectImmediately Virtual PC
- Propriedade ConnectImmediately Virtual PC, interface IVMSerialPort
- IVMSerialPort interface virtual PC, Propriedade ConnectImmediately
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644710"
---
# <a name="ivmserialportconnectimmediately-property"></a><span data-ttu-id="84fc5-106">Propriedade IVMSerialPort:: ConnectImmediately</span><span class="sxs-lookup"><span data-stu-id="84fc5-106">IVMSerialPort::ConnectImmediately property</span></span>

<span data-ttu-id="84fc5-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="84fc5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="84fc5-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="84fc5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="84fc5-109">Determina se a porta serial deve ser aberta sem aguardar a recepção de um comando de modem.</span><span class="sxs-lookup"><span data-stu-id="84fc5-109">Determines whether the serial port should be opened without waiting for a modem command to be received.</span></span>

<span data-ttu-id="84fc5-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="84fc5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84fc5-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84fc5-111">Syntax</span></span>


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a><span data-ttu-id="84fc5-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="84fc5-112">Property value</span></span>

<span data-ttu-id="84fc5-113">**Variante \_ TRUE** se a porta serial deve ser aberta sem esperar que um comando de modem seja recebido; **Variante \_** Caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="84fc5-113">**VARIANT\_TRUE** if the serial port should be opened without waiting for a modem command to be received; **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="84fc5-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="84fc5-114">Error codes</span></span>



| <span data-ttu-id="84fc5-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="84fc5-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="84fc5-116">Significado</span><span class="sxs-lookup"><span data-stu-id="84fc5-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="84fc5-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="84fc5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="84fc5-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="84fc5-118">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="84fc5-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="84fc5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="84fc5-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="84fc5-120">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="84fc5-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="84fc5-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="84fc5-122">A configuração desta máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="84fc5-122">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="84fc5-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="84fc5-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="84fc5-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="84fc5-124">An unexpected error has occurred.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="84fc5-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="84fc5-125">Remarks</span></span>

<span data-ttu-id="84fc5-126">Essa propriedade só será válida se a propriedade de [**tipo**](ivmserialport-type.md) de porta for **vmSerialPort \_ HostPort**.</span><span class="sxs-lookup"><span data-stu-id="84fc5-126">This property is valid only if the port [**Type**](ivmserialport-type.md) property is **vmSerialPort\_HostPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="84fc5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84fc5-127">Requirements</span></span>



| <span data-ttu-id="84fc5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="84fc5-128">Requirement</span></span> | <span data-ttu-id="84fc5-129">Valor</span><span class="sxs-lookup"><span data-stu-id="84fc5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84fc5-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84fc5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84fc5-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="84fc5-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84fc5-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84fc5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84fc5-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="84fc5-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="84fc5-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="84fc5-134">End of client support</span></span><br/>    | <span data-ttu-id="84fc5-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84fc5-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="84fc5-136">Produto</span><span class="sxs-lookup"><span data-stu-id="84fc5-136">Product</span></span><br/>                  | <span data-ttu-id="84fc5-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="84fc5-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="84fc5-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84fc5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="84fc5-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="84fc5-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="84fc5-140">IID</span><span class="sxs-lookup"><span data-stu-id="84fc5-140">IID</span></span><br/>                      | <span data-ttu-id="84fc5-141">IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="84fc5-141">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="84fc5-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="84fc5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84fc5-143">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="84fc5-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

