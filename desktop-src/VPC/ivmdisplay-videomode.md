---
title: Propriedade videomode IVMDisplay (VPCCOMInterfaces. h)
description: Recupera o modo de vídeo atual.
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- Propriedade de video PC virtual
- Propriedade videomode Virtual PC, interface IVMDisplay
- IVMDisplay interface virtual PC, Propriedade videomode
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164a658766cb8973a7c1ac403756ee888abab1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918402"
---
# <a name="ivmdisplayvideomode-property"></a><span data-ttu-id="1439e-106">Propriedade IVMDisplay:: videomode</span><span class="sxs-lookup"><span data-stu-id="1439e-106">IVMDisplay::VideoMode property</span></span>

<span data-ttu-id="1439e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1439e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1439e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1439e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1439e-109">Recupera o modo de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="1439e-109">Retrieves the current video mode.</span></span>

<span data-ttu-id="1439e-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1439e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1439e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1439e-111">Syntax</span></span>


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a><span data-ttu-id="1439e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1439e-112">Property value</span></span>

<span data-ttu-id="1439e-113">O modo de vídeo atual do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="1439e-113">The current video mode of the guest operating system.</span></span> <span data-ttu-id="1439e-114">Para obter uma lista de valores, consulte [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span><span class="sxs-lookup"><span data-stu-id="1439e-114">For a list of values, see [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="1439e-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1439e-115">Error codes</span></span>



| <span data-ttu-id="1439e-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="1439e-116">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="1439e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="1439e-117">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1439e-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1439e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="1439e-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1439e-119">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="1439e-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="1439e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="1439e-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1439e-121">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1439e-122"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="1439e-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="1439e-123">A máquina virtual deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="1439e-123">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="1439e-124"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1439e-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="1439e-125">A máquina virtual não é válida ou não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="1439e-125">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="1439e-126"><dt>VM \_ E \_ nenhum \_ </dt> <dt>0xA0040850</dt> de exibição</span><span class="sxs-lookup"><span data-stu-id="1439e-126"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="1439e-127">Não é possível localizar uma exibição válida para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1439e-127">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="1439e-128"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="1439e-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="1439e-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="1439e-129">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="1439e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1439e-130">Requirements</span></span>



| <span data-ttu-id="1439e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1439e-131">Requirement</span></span> | <span data-ttu-id="1439e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1439e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1439e-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1439e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1439e-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1439e-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1439e-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1439e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1439e-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1439e-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1439e-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1439e-137">End of client support</span></span><br/>    | <span data-ttu-id="1439e-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1439e-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1439e-139">Produto</span><span class="sxs-lookup"><span data-stu-id="1439e-139">Product</span></span><br/>                  | <span data-ttu-id="1439e-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1439e-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1439e-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1439e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1439e-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1439e-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1439e-143">IID</span><span class="sxs-lookup"><span data-stu-id="1439e-143">IID</span></span><br/>                      | <span data-ttu-id="1439e-144">IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="1439e-144">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1439e-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="1439e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1439e-146">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="1439e-146">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

