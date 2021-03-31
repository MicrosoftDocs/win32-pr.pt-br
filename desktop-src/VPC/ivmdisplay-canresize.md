---
title: Propriedade redimensionamento do IVMDisplay (VPCCOMInterfaces. h)
description: Determina se o convidado permite alterações de resolução.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- Redimensionar a propriedade Virtual PC
- Propriedade redimensionar Virtual PC, interface IVMDisplay
- IVMDisplay interface virtual PC, redimensionar Propriedade
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca865189b1fd155e0edf85bac9a36d94ffe5d656
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645142"
---
# <a name="ivmdisplaycanresize-property"></a><span data-ttu-id="b8307-106">Propriedade IVMDisplay:: reresize</span><span class="sxs-lookup"><span data-stu-id="b8307-106">IVMDisplay::CanResize property</span></span>

<span data-ttu-id="b8307-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b8307-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b8307-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b8307-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b8307-109">Determina se o convidado permite alterações de resolução.</span><span class="sxs-lookup"><span data-stu-id="b8307-109">Determines whether the Guest allows resolution changes.</span></span>

<span data-ttu-id="b8307-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b8307-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8307-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8307-111">Syntax</span></span>


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a><span data-ttu-id="b8307-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b8307-112">Property value</span></span>

<span data-ttu-id="b8307-113">**Variante \_ TRUE** se o convidado permitir alterações de resolução e **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b8307-113">**VARIANT\_TRUE** if the Guest allows resolution changes and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b8307-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b8307-114">Error codes</span></span>



| <span data-ttu-id="b8307-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="b8307-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="b8307-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b8307-116">Meaning</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8307-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b8307-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="b8307-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b8307-118">The operation was successful.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="b8307-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="b8307-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="b8307-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b8307-120">The parameter is **NULL**.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="b8307-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b8307-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="b8307-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="b8307-122">The configuration is unknown.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="b8307-123"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b8307-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="b8307-124">A máquina virtual deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="b8307-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="b8307-125"><dt>VM \_ E \_ nenhum \_ </dt> <dt>0xA0040850</dt> de exibição</span><span class="sxs-lookup"><span data-stu-id="b8307-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="b8307-126">Nenhum dispositivo de vídeo foi encontrado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8307-126">There was no video device found for the virtual machine.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="b8307-127"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="b8307-127"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="b8307-128">O recurso componentes de integração não está disponível; os componentes de integração não estão instalados ou o recurso foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b8307-128">The integration components feature is not available; either the integration components are not installed or the feature has been disabled.</span></span><br/> |
| <dl> <span data-ttu-id="b8307-129"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b8307-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="b8307-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b8307-130">An unexpected error has occurred.</span></span><br/>                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="b8307-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8307-131">Requirements</span></span>



| <span data-ttu-id="b8307-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8307-132">Requirement</span></span> | <span data-ttu-id="b8307-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b8307-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8307-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8307-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b8307-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b8307-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8307-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8307-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b8307-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b8307-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b8307-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b8307-138">End of client support</span></span><br/>    | <span data-ttu-id="b8307-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8307-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b8307-140">Produto</span><span class="sxs-lookup"><span data-stu-id="b8307-140">Product</span></span><br/>                  | <span data-ttu-id="b8307-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b8307-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b8307-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8307-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8307-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8307-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b8307-144">IID</span><span class="sxs-lookup"><span data-stu-id="b8307-144">IID</span></span><br/>                      | <span data-ttu-id="b8307-145">IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="b8307-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b8307-146">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b8307-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8307-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="b8307-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

