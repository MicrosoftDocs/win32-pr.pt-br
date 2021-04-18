---
title: Método IVMGuestOS GetOsVersionInfo (VPCCOMInterfaces. h)
description: Recupera informações de versão para o sistema operacional convidado em execução na máquina virtual.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- GetOsVersionInfo do método virtual PC
- Método GetOsVersionInfo Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, método GetOsVersionInfo
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759168"
---
# <a name="ivmguestosgetosversioninfo-method"></a><span data-ttu-id="2db2b-106">Método IVMGuestOS:: GetOsVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2db2b-106">IVMGuestOS::GetOsVersionInfo method</span></span>

<span data-ttu-id="2db2b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2db2b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2db2b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2db2b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2db2b-109">Recupera informações de versão para o sistema operacional convidado em execução na VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="2db2b-109">Retrieves version information for the guest operating system running in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="2db2b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2db2b-110">Syntax</span></span>


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2db2b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2db2b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db2b-112">*guestOsVersionInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2db2b-112">*guestOsVersionInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2db2b-113">Um ponteiro para uma estrutura [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) .</span><span class="sxs-lookup"><span data-stu-id="2db2b-113">A pointer to a [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db2b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2db2b-114">Return value</span></span>

<span data-ttu-id="2db2b-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="2db2b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2db2b-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2db2b-116">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="2db2b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="2db2b-117">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2db2b-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2db2b-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="2db2b-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2db2b-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="2db2b-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="2db2b-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="2db2b-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2db2b-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="2db2b-122"><dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="2db2b-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="2db2b-123">Não há memória suficiente disponível para concluir esta solicitação.</span><span class="sxs-lookup"><span data-stu-id="2db2b-123">There is not enough memory available to complete this request.</span></span><br/> |
| <dl> <span data-ttu-id="2db2b-124"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="2db2b-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="2db2b-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="2db2b-125">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="2db2b-126"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="2db2b-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="2db2b-127">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="2db2b-127">The VM is not running.</span></span><br/>                                         |
| <dl> <span data-ttu-id="2db2b-128"><dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="2db2b-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="2db2b-129">Os componentes de integração não estão instalados nesta VM.</span><span class="sxs-lookup"><span data-stu-id="2db2b-129">Integration components are not installed in this VM.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="2db2b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2db2b-130">Requirements</span></span>



| <span data-ttu-id="2db2b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2db2b-131">Requirement</span></span> | <span data-ttu-id="2db2b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2db2b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db2b-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2db2b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2db2b-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2db2b-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2db2b-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2db2b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2db2b-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2db2b-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2db2b-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2db2b-137">End of client support</span></span><br/>    | <span data-ttu-id="2db2b-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2db2b-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2db2b-139">Produto</span><span class="sxs-lookup"><span data-stu-id="2db2b-139">Product</span></span><br/>                  | <span data-ttu-id="2db2b-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2db2b-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2db2b-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2db2b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="2db2b-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db2b-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2db2b-143">IID</span><span class="sxs-lookup"><span data-stu-id="2db2b-143">IID</span></span><br/>                      | <span data-ttu-id="2db2b-144">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="2db2b-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="2db2b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="2db2b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db2b-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="2db2b-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

