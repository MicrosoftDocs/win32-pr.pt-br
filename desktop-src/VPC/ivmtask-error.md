---
title: Propriedade de erro IVMTask (VPCCOMInterfaces. h)
description: Recupera o erro registrado para esta tarefa.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Propriedade de erro PC virtual
- Propriedade de erro Virtual PC, interface IVMTask
- Virtual PC de interface IVMTask, Propriedade Error
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788869"
---
# <a name="ivmtaskerror-property"></a><span data-ttu-id="35787-106">Propriedade IVMTask:: Error</span><span class="sxs-lookup"><span data-stu-id="35787-106">IVMTask::Error property</span></span>

<span data-ttu-id="35787-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="35787-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="35787-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="35787-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="35787-109">Recupera o erro registrado para esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="35787-109">Retrieves the error recorded for this task.</span></span>

<span data-ttu-id="35787-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="35787-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35787-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35787-111">Syntax</span></span>


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a><span data-ttu-id="35787-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="35787-112">Property value</span></span>

<span data-ttu-id="35787-113">O erro registrado.</span><span class="sxs-lookup"><span data-stu-id="35787-113">The recorded error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35787-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="35787-114">Error codes</span></span>

<span data-ttu-id="35787-115">As instâncias de [**IVMTask**](ivmtask.md) retornadas por outras interfaces podem retornar valores adicionais.</span><span class="sxs-lookup"><span data-stu-id="35787-115">Instances of [**IVMTask**](ivmtask.md) returned by other interfaces may return additional values.</span></span> <span data-ttu-id="35787-116">Para obter detalhes, consulte a documentação dos métodos que retornam uma instância de **IVMTask** .</span><span class="sxs-lookup"><span data-stu-id="35787-116">For details, see the documentation of the methods that return a **IVMTask** instance.</span></span>



| <span data-ttu-id="35787-117">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="35787-117">Name/value</span></span>                                                                                                                                                                        | <span data-ttu-id="35787-118">Significado</span><span class="sxs-lookup"><span data-stu-id="35787-118">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="35787-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="35787-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                           | <span data-ttu-id="35787-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="35787-120">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="35787-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="35787-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                             | <span data-ttu-id="35787-122">O valor do parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="35787-122">The parameter value is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="35787-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="35787-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                     | <span data-ttu-id="35787-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="35787-124">An unexpected error has occurred.</span></span><br/>                          |
| <dl> <span data-ttu-id="35787-125"><dt>VM \_ E \_ VMVIRTUALPC \_ \_ versão mais antiga</dt> <dt>0xA0040952</dt></span><span class="sxs-lookup"><span data-stu-id="35787-125"><dt>VM\_E\_VMVIRTUALPC\_OLDER\_VERSION</dt> <dt>0xA0040952</dt></span></span> </dl>     | <span data-ttu-id="35787-126">O Virtual PC 2007 e o Windows Virtual PC estão instalados.</span><span class="sxs-lookup"><span data-stu-id="35787-126">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <dl> <span data-ttu-id="35787-127"><dt>VM \_ E \_ outros 0xA0040953 de \_ \_ software de virtualização</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="35787-127"><dt>VM\_E\_OTHER\_VIRTUALIZATION\_SOFTWARE</dt> <dt>0xA0040953</dt></span></span> </dl> | <span data-ttu-id="35787-128">Outros softwares de virtualização estão instalados.</span><span class="sxs-lookup"><span data-stu-id="35787-128">Other virtualization software is installed.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="35787-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35787-129">Requirements</span></span>



| <span data-ttu-id="35787-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="35787-130">Requirement</span></span> | <span data-ttu-id="35787-131">Valor</span><span class="sxs-lookup"><span data-stu-id="35787-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="35787-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35787-132">Minimum supported client</span></span><br/> | <span data-ttu-id="35787-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="35787-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35787-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35787-134">Minimum supported server</span></span><br/> | <span data-ttu-id="35787-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="35787-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="35787-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="35787-136">End of client support</span></span><br/>    | <span data-ttu-id="35787-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35787-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="35787-138">Produto</span><span class="sxs-lookup"><span data-stu-id="35787-138">Product</span></span><br/>                  | <span data-ttu-id="35787-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="35787-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="35787-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35787-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="35787-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="35787-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="35787-142">IID</span><span class="sxs-lookup"><span data-stu-id="35787-142">IID</span></span><br/>                      | <span data-ttu-id="35787-143">IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="35787-143">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="35787-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="35787-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35787-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="35787-145">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

