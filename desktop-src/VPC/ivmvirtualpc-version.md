---
title: Propriedade de versão IVMVirtualPC (VPCCOMInterfaces. h)
description: Recupera a versão desta instância do Windows Virtual PC.
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Propriedade de versão Virtual PC
- Propriedade de versão Virtual PC, interface IVMVirtualPC
- Virtual PC de interface IVMVirtualPC, Propriedade Version
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0dc84fd714c50c0a0adb3084603aeea2419d3ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455981"
---
# <a name="ivmvirtualpcversion-property"></a><span data-ttu-id="3793a-106">Propriedade IVMVirtualPC:: Version</span><span class="sxs-lookup"><span data-stu-id="3793a-106">IVMVirtualPC::Version property</span></span>

<span data-ttu-id="3793a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3793a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3793a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3793a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3793a-109">Recupera a versão desta instância do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="3793a-109">Retrieves the version of this instance of Windows Virtual PC.</span></span>

<span data-ttu-id="3793a-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3793a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3793a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3793a-111">Syntax</span></span>


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a><span data-ttu-id="3793a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3793a-112">Property value</span></span>

<span data-ttu-id="3793a-113">A versão.</span><span class="sxs-lookup"><span data-stu-id="3793a-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3793a-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3793a-114">Error codes</span></span>



| <span data-ttu-id="3793a-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3793a-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="3793a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3793a-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3793a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3793a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="3793a-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3793a-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3793a-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3793a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="3793a-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3793a-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="3793a-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3793a-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="3793a-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3793a-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="3793a-123"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3793a-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="3793a-124">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="3793a-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3793a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3793a-125">Remarks</span></span>

<span data-ttu-id="3793a-126">As informações de versão do Windows Virtual PC são retornadas como um valor de cadeia de caracteres com o seguinte formato: "*v*. *s*. *BBB*. " *t*", em que *v* é o número de versão principal, *s* é o número de versão secundário, *BBB* é o número de Build, *t* é o tipo de compilação (0 = Build de versão) e o *EE* é a Server Edition (se = Standard Edition, EE = Enterprise Edition).</span><span class="sxs-lookup"><span data-stu-id="3793a-126">The Windows Virtual PC version information is returned as a string value with the following format: "*v*.*s*.*bbb*.*tee*", where *v* is the major version number, *s* is the minor version number, *bbb* is the build number, *t* is the build type (0 = release build), and *ee* is the server edition (SE = Standard Edition, EE = Enterprise Edition).</span></span>

## <a name="requirements"></a><span data-ttu-id="3793a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3793a-127">Requirements</span></span>



| <span data-ttu-id="3793a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3793a-128">Requirement</span></span> | <span data-ttu-id="3793a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3793a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3793a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3793a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3793a-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3793a-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3793a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3793a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3793a-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3793a-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3793a-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3793a-134">End of client support</span></span><br/>    | <span data-ttu-id="3793a-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3793a-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3793a-136">Produto</span><span class="sxs-lookup"><span data-stu-id="3793a-136">Product</span></span><br/>                  | <span data-ttu-id="3793a-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3793a-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3793a-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3793a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3793a-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3793a-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3793a-140">IID</span><span class="sxs-lookup"><span data-stu-id="3793a-140">IID</span></span><br/>                      | <span data-ttu-id="3793a-141">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="3793a-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3793a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="3793a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3793a-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="3793a-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

