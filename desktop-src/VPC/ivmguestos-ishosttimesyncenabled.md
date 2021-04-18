---
title: Propriedade IVMGuestOS IsHostTimeSyncEnabled (VPCCOMInterfaces. h)
description: Indica se os componentes de integração nessa VM devem sincronizar o relógio do convidado com o relógio do host.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- Propriedade IsHostTimeSyncEnabled Virtual PC
- Propriedade IsHostTimeSyncEnabled Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade IsHostTimeSyncEnabled
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87afddb2e3bc940c5dba7e2548e4355d36142012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748735"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a><span data-ttu-id="8e93d-106">Propriedade IVMGuestOS:: IsHostTimeSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="8e93d-106">IVMGuestOS::IsHostTimeSyncEnabled property</span></span>

<span data-ttu-id="8e93d-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8e93d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e93d-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e93d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e93d-109">Indica se os componentes de integração nesta VM (máquina virtual) devem sincronizar o relógio do convidado com o relógio do host.</span><span class="sxs-lookup"><span data-stu-id="8e93d-109">Indicates whether the Integration Components in this virtual machine (VM) should synchronize the guest's clock with the host's clock.</span></span>

<span data-ttu-id="8e93d-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8e93d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e93d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e93d-111">Syntax</span></span>


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="8e93d-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8e93d-112">Property value</span></span>

<span data-ttu-id="8e93d-113">Use **Variant \_ true** se os componentes de integração nessa VM devem sincronizar o relógio do convidado com o relógio do host e a **variante \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8e93d-113">Use **VARIANT\_TRUE** if the integration components in this VM should synchronize the guest's clock with the host's clock and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8e93d-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8e93d-114">Error codes</span></span>



| <span data-ttu-id="8e93d-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="8e93d-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="8e93d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8e93d-116">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="8e93d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e93d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="8e93d-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8e93d-118">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="8e93d-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="8e93d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="8e93d-120">O parâmetro *IsEnabled* não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="8e93d-120">The *isEnabled* parameter is not specified.</span></span><br/> |
| <dl> <span data-ttu-id="8e93d-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8e93d-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="8e93d-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="8e93d-122">The configuration is unknown.</span></span><br/>               |
| <dl> <span data-ttu-id="8e93d-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="8e93d-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="8e93d-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="8e93d-124">An unexpected error has occurred.</span></span><br/>           |



## <a name="remarks"></a><span data-ttu-id="8e93d-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e93d-125">Remarks</span></span>

<span data-ttu-id="8e93d-126">Você não pode alterar essa configuração enquanto a máquina virtual estiver ativa (ou seja, em execução ou em estado salvo).</span><span class="sxs-lookup"><span data-stu-id="8e93d-126">You cannot change this setting while the virtual machine is active (that is, running or in saved state).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e93d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e93d-127">Requirements</span></span>



| <span data-ttu-id="8e93d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e93d-128">Requirement</span></span> | <span data-ttu-id="8e93d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8e93d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e93d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e93d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8e93d-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e93d-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e93d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e93d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8e93d-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8e93d-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8e93d-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8e93d-134">End of client support</span></span><br/>    | <span data-ttu-id="8e93d-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e93d-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8e93d-136">Produto</span><span class="sxs-lookup"><span data-stu-id="8e93d-136">Product</span></span><br/>                  | <span data-ttu-id="8e93d-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e93d-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8e93d-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e93d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e93d-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e93d-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8e93d-140">IID</span><span class="sxs-lookup"><span data-stu-id="8e93d-140">IID</span></span><br/>                      | <span data-ttu-id="8e93d-141">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="8e93d-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8e93d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e93d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e93d-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="8e93d-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

