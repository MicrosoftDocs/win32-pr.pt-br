---
title: Propriedade IVMGuestOS TerminalServicesInitialized (VPCCOMInterfaces. h)
description: Status de Serviços de Área de Trabalho Remota no sistema operacional convidado.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- Propriedade TerminalServicesInitialized Virtual PC
- Propriedade TerminalServicesInitialized Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade TerminalServicesInitialized
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92ce23b4b07f3e2d06f605f4598c8b31e4c70692
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499754"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a><span data-ttu-id="05c3c-106">Propriedade IVMGuestOS:: TerminalServicesInitialized</span><span class="sxs-lookup"><span data-stu-id="05c3c-106">IVMGuestOS::TerminalServicesInitialized property</span></span>

<span data-ttu-id="05c3c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="05c3c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="05c3c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="05c3c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="05c3c-109">Recupera o status de Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="05c3c-109">Retrieves the status of Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="05c3c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="05c3c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c3c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05c3c-111">Syntax</span></span>


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a><span data-ttu-id="05c3c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="05c3c-112">Property value</span></span>

<span data-ttu-id="05c3c-113">O status de inicialização.</span><span class="sxs-lookup"><span data-stu-id="05c3c-113">The initialization status.</span></span>

## <a name="error-codes"></a><span data-ttu-id="05c3c-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="05c3c-114">Error codes</span></span>



| <span data-ttu-id="05c3c-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="05c3c-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="05c3c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="05c3c-116">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05c3c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05c3c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="05c3c-118">A operação foi bem-sucedida e Serviços de Área de Trabalho Remota foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="05c3c-118">The operation was successful and Remote Desktop Services has been initialized.</span></span> <span data-ttu-id="05c3c-119">O valor da propriedade retornada indica se Serviços de Área de Trabalho Remota está disponível no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="05c3c-119">The returned property value indicates whether Remote Desktop Services is available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="05c3c-120"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="05c3c-120"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="05c3c-121">O recurso componentes de integração está em execução, mas Serviços de Área de Trabalho Remota ainda não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="05c3c-121">The integration components feature is running, but Remote Desktop Services is not yet initialized.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="05c3c-122"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="05c3c-122"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="05c3c-123">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="05c3c-123">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="05c3c-124"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="05c3c-124"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="05c3c-125">A máquina virtual (VM) deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="05c3c-125">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="05c3c-126"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="05c3c-126"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="05c3c-127">O recurso componentes de integração não está em execução no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="05c3c-127">The integration components feature is not running in the guest operating system.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="05c3c-128"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="05c3c-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="05c3c-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="05c3c-129">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="05c3c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c3c-130">Requirements</span></span>



| <span data-ttu-id="05c3c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c3c-131">Requirement</span></span> | <span data-ttu-id="05c3c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="05c3c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c3c-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c3c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="05c3c-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="05c3c-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05c3c-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c3c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="05c3c-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="05c3c-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="05c3c-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="05c3c-137">End of client support</span></span><br/>    | <span data-ttu-id="05c3c-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="05c3c-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="05c3c-139">Produto</span><span class="sxs-lookup"><span data-stu-id="05c3c-139">Product</span></span><br/>                  | <span data-ttu-id="05c3c-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05c3c-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="05c3c-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05c3c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="05c3c-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="05c3c-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="05c3c-143">IID</span><span class="sxs-lookup"><span data-stu-id="05c3c-143">IID</span></span><br/>                      | <span data-ttu-id="05c3c-144">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="05c3c-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="05c3c-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="05c3c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c3c-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="05c3c-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

