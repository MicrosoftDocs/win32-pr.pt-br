---
title: Propriedade IVMGuestOS CSDVersion (VPCCOMInterfaces. h)
description: O CSDVersion do sistema operacional convidado em execução na máquina virtual.
ms.assetid: 6f1d8dd6-6feb-4bdf-a553-631d55c18076
keywords:
- Propriedade CSDVersion Virtual PC
- Propriedade CSDVersion Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade CSDVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.CSDVersion
- IVMGuestOS.get_CSDVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d82b3939f581edf328902f7fd0a26e1916abe1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919105"
---
# <a name="ivmguestoscsdversion-property"></a><span data-ttu-id="bbb95-106">Propriedade IVMGuestOS:: CSDVersion</span><span class="sxs-lookup"><span data-stu-id="bbb95-106">IVMGuestOS::CSDVersion property</span></span>

<span data-ttu-id="bbb95-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bbb95-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bbb95-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bbb95-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bbb95-109">Recupera o CSDVersion do sistema operacional convidado em execução na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bbb95-109">Retrieves the CSDVersion of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="bbb95-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="bbb95-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb95-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbb95-111">Syntax</span></span>


```C++
HRESULT get_CSDVersion(
  [out, retval] BSTR *csdVersion
);
```



## <a name="property-value"></a><span data-ttu-id="bbb95-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bbb95-112">Property value</span></span>

<span data-ttu-id="bbb95-113">Uma cadeia de caracteres terminada em nulo, como "Service Pack 3", que indica o Service Pack mais recente instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="bbb95-113">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="bbb95-114">Se nenhum Service Pack tiver sido instalado, a cadeia de caracteres estará vazia.</span><span class="sxs-lookup"><span data-stu-id="bbb95-114">If no Service Pack has been installed, the string is empty.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bbb95-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bbb95-115">Error codes</span></span>



| <span data-ttu-id="bbb95-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="bbb95-116">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="bbb95-117">Significado</span><span class="sxs-lookup"><span data-stu-id="bbb95-117">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bbb95-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bbb95-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="bbb95-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bbb95-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="bbb95-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="bbb95-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="bbb95-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bbb95-121">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="bbb95-122"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="bbb95-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="bbb95-123">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="bbb95-123">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="bbb95-124"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="bbb95-124"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="bbb95-125">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="bbb95-125">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="bbb95-126"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="bbb95-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="bbb95-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="bbb95-127">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="bbb95-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbb95-128">Requirements</span></span>



| <span data-ttu-id="bbb95-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbb95-129">Requirement</span></span> | <span data-ttu-id="bbb95-130">Valor</span><span class="sxs-lookup"><span data-stu-id="bbb95-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb95-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbb95-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bbb95-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bbb95-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bbb95-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbb95-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bbb95-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bbb95-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bbb95-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bbb95-135">End of client support</span></span><br/>    | <span data-ttu-id="bbb95-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbb95-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bbb95-137">Produto</span><span class="sxs-lookup"><span data-stu-id="bbb95-137">Product</span></span><br/>                  | <span data-ttu-id="bbb95-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bbb95-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bbb95-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbb95-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbb95-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbb95-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bbb95-141">IID</span><span class="sxs-lookup"><span data-stu-id="bbb95-141">IID</span></span><br/>                      | <span data-ttu-id="bbb95-142">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="bbb95-142">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="bbb95-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbb95-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbb95-144">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="bbb95-144">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

