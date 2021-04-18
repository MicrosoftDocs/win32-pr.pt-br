---
title: Método IVMGuestOS IsUserLoggedOn (VPCCOMInterfaces. h)
description: Determina se a sessão solicitada está presente.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- IsUserLoggedOn do método virtual PC
- Método IsUserLoggedOn Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, método IsUserLoggedOn
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810652"
---
# <a name="ivmguestosisuserloggedon-method"></a><span data-ttu-id="6895c-106">Método IVMGuestOS:: IsUserLoggedOn</span><span class="sxs-lookup"><span data-stu-id="6895c-106">IVMGuestOS::IsUserLoggedOn method</span></span>

<span data-ttu-id="6895c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6895c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6895c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6895c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6895c-109">Determina se a sessão solicitada está presente.</span><span class="sxs-lookup"><span data-stu-id="6895c-109">Determines whether the requested session is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="6895c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6895c-110">Syntax</span></span>


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a><span data-ttu-id="6895c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6895c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6895c-112">*inRailSession* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6895c-112">*inRailSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6895c-113">Defina como 0 para uma sessão de trilho ou 1 para uma sessão de RDP.</span><span class="sxs-lookup"><span data-stu-id="6895c-113">Set to 0 for a Rail session or 1 for an RDP session.</span></span>

</dd> <dt>

<span data-ttu-id="6895c-114">*outSessionPresent* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6895c-114">*outSessionPresent* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6895c-115">Defina como **Variant \_ true** se a sessão estiver presente e **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6895c-115">Set to **VARIANT\_TRUE** if the session is present and **VARIANT\_FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6895c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6895c-116">Return value</span></span>

<span data-ttu-id="6895c-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="6895c-117">This method can return one of these values.</span></span>



| <span data-ttu-id="6895c-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6895c-118">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="6895c-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="6895c-119">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6895c-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6895c-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="6895c-121">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6895c-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6895c-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6895c-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="6895c-123">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6895c-123">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="6895c-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6895c-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                            | <span data-ttu-id="6895c-125">O parâmetro *outSessionPresent* não é válido ou é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6895c-125">The *outSessionPresent* parameter is not valid or is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="6895c-126"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6895c-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="6895c-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6895c-127">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="6895c-128"><dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="6895c-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="6895c-129">Não há memória suficiente disponível para concluir esta solicitação.</span><span class="sxs-lookup"><span data-stu-id="6895c-129">There is not enough memory available to complete this request.</span></span><br/>  |
| <dl> <span data-ttu-id="6895c-130"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="6895c-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                        | <span data-ttu-id="6895c-131">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="6895c-131">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="6895c-132"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="6895c-132"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="6895c-133">A máquina virtual (VM) deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="6895c-133">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="6895c-134"><dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="6895c-134"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="6895c-135">O recurso componentes de integração não está instalado nesta VM.</span><span class="sxs-lookup"><span data-stu-id="6895c-135">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="6895c-136"><dt>**VM \_ E \_ VM em \_ pausa**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="6895c-136"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                       | <span data-ttu-id="6895c-137">A VM está pausada.</span><span class="sxs-lookup"><span data-stu-id="6895c-137">The VM is paused.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="6895c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6895c-138">Requirements</span></span>



| <span data-ttu-id="6895c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6895c-139">Requirement</span></span> | <span data-ttu-id="6895c-140">Valor</span><span class="sxs-lookup"><span data-stu-id="6895c-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6895c-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6895c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6895c-142">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6895c-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6895c-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6895c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6895c-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6895c-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6895c-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6895c-145">End of client support</span></span><br/>    | <span data-ttu-id="6895c-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6895c-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6895c-147">Produto</span><span class="sxs-lookup"><span data-stu-id="6895c-147">Product</span></span><br/>                  | <span data-ttu-id="6895c-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6895c-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6895c-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6895c-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="6895c-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6895c-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6895c-151">IID</span><span class="sxs-lookup"><span data-stu-id="6895c-151">IID</span></span><br/>                      | <span data-ttu-id="6895c-152">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="6895c-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6895c-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="6895c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6895c-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="6895c-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

