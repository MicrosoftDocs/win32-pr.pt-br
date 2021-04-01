---
title: Propriedade IVMGuestOS IntegrationComponentsVersion (VPCCOMInterfaces. h)
description: Recupera a versão dos componentes de integração instalados no sistema operacional convidado.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- Propriedade IntegrationComponentsVersion Virtual PC
- Propriedade IntegrationComponentsVersion Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade IntegrationComponentsVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85352614b89ab208377fe44fe3b970c693d60dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644316"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a><span data-ttu-id="836c7-106">Propriedade IVMGuestOS:: IntegrationComponentsVersion</span><span class="sxs-lookup"><span data-stu-id="836c7-106">IVMGuestOS::IntegrationComponentsVersion property</span></span>

<span data-ttu-id="836c7-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="836c7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="836c7-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="836c7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="836c7-109">Recupera a versão dos componentes de integração instalados no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="836c7-109">Retrieves the version of the Integration Components installed in the guest operating system.</span></span>

<span data-ttu-id="836c7-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="836c7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="836c7-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="836c7-111">Syntax</span></span>


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a><span data-ttu-id="836c7-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="836c7-112">Property value</span></span>

<span data-ttu-id="836c7-113">A versão.</span><span class="sxs-lookup"><span data-stu-id="836c7-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="836c7-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="836c7-114">Error codes</span></span>



| <span data-ttu-id="836c7-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="836c7-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="836c7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="836c7-116">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="836c7-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="836c7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="836c7-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="836c7-118">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="836c7-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="836c7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="836c7-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="836c7-120">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="836c7-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="836c7-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="836c7-122">Não foi possível encontrar a máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="836c7-122">The virtual machine (VM) could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="836c7-123"><dt>VM \_ E \_ adições \_ não \_ </dt> <dt>0xA0040504</dt> disp.</span><span class="sxs-lookup"><span data-stu-id="836c7-123"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="836c7-124">Os componentes de integração não estão instalados nesta VM ou a VM nunca foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="836c7-124">Integration Components are not installed in this VM, or the VM was never started.</span></span><br/> |
| <dl> <span data-ttu-id="836c7-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="836c7-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="836c7-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="836c7-126">An unexpected error has occurred.</span></span><br/>                                                 |



## <a name="requirements"></a><span data-ttu-id="836c7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="836c7-127">Requirements</span></span>



| <span data-ttu-id="836c7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="836c7-128">Requirement</span></span> | <span data-ttu-id="836c7-129">Valor</span><span class="sxs-lookup"><span data-stu-id="836c7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="836c7-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="836c7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="836c7-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="836c7-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="836c7-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="836c7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="836c7-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="836c7-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="836c7-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="836c7-134">End of client support</span></span><br/>    | <span data-ttu-id="836c7-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="836c7-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="836c7-136">Produto</span><span class="sxs-lookup"><span data-stu-id="836c7-136">Product</span></span><br/>                  | <span data-ttu-id="836c7-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="836c7-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="836c7-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="836c7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="836c7-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="836c7-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="836c7-140">IID</span><span class="sxs-lookup"><span data-stu-id="836c7-140">IID</span></span><br/>                      | <span data-ttu-id="836c7-141">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="836c7-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="836c7-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="836c7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836c7-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="836c7-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

