---
title: Propriedade IVMGuestOS MultipleUserSessionsAllowed
description: Determina se várias sessões de usuário simultâneas são permitidas no sistema operacional convidado.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- Propriedade MultipleUserSessionsAllowed Virtual PC
- Propriedade MultipleUserSessionsAllowed Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade MultipleUserSessionsAllowed
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085652"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a><span data-ttu-id="dee00-106">Propriedade IVMGuestOS:: MultipleUserSessionsAllowed</span><span class="sxs-lookup"><span data-stu-id="dee00-106">IVMGuestOS::MultipleUserSessionsAllowed property</span></span>

<span data-ttu-id="dee00-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dee00-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dee00-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dee00-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dee00-109">Determina se várias sessões de usuário simultâneas são permitidas no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="dee00-109">Determines whether multiple simultaneous user sessions are allowed in the guest operating system.</span></span>

<span data-ttu-id="dee00-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="dee00-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee00-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dee00-111">Syntax</span></span>


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a><span data-ttu-id="dee00-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="dee00-112">Property value</span></span>

<span data-ttu-id="dee00-113">**Variante \_ TRUE** se várias sessões de usuário simultâneas forem permitidas no sistema operacional convidado; caso contrário, **Variant \_ false** .</span><span class="sxs-lookup"><span data-stu-id="dee00-113">**VARIANT\_TRUE** if multiple simultaneous user sessions are allowed in the guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dee00-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="dee00-114">Error codes</span></span>



| <span data-ttu-id="dee00-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="dee00-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="dee00-116">Significado</span><span class="sxs-lookup"><span data-stu-id="dee00-116">Meaning</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dee00-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dee00-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="dee00-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dee00-118">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="dee00-119"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dee00-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="dee00-120">Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) ainda não foi inicializado no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="dee00-120">Remote Desktop Services (formerly known as Terminal Services) is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="dee00-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="dee00-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="dee00-122">O parâmetro *sessionStatus* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="dee00-122">The *sessionStatus* parameter is **NULL**.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="dee00-123"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="dee00-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="dee00-124">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="dee00-124">The virtual machine is not running.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="dee00-125"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="dee00-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="dee00-126">Os componentes de integração não estão instalados nesta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dee00-126">Integration components are not installed in this virtual machine.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="dee00-127"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="dee00-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="dee00-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="dee00-128">An unexpected error has occurred.</span></span><br/>                                                                                   |



## <a name="remarks"></a><span data-ttu-id="dee00-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="dee00-129">Remarks</span></span>

<span data-ttu-id="dee00-130">O valor dessa propriedade não é válido, a menos que a propriedade [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) seja **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="dee00-130">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="dee00-131">Para sistemas operacionais cliente do Windows, **MultipleUserSessionsAllowed** será **Variant \_ true** se houver suporte para troca rápida de usuário.</span><span class="sxs-lookup"><span data-stu-id="dee00-131">For Windows client operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Fast User Switching is supported.</span></span> <span data-ttu-id="dee00-132">Para sistemas operacionais Windows Server, **MultipleUserSessionsAllowed** será **VARIANT \_ true** se serviços de área de trabalho remota (anteriormente chamado de serviços de terminal) estiver instalado e habilitado.</span><span class="sxs-lookup"><span data-stu-id="dee00-132">For Windows Server operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Remote Desktop Services (formerly called Terminal Services) is installed and enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee00-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dee00-133">Requirements</span></span>



| <span data-ttu-id="dee00-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee00-134">Requirement</span></span> | <span data-ttu-id="dee00-135">Valor</span><span class="sxs-lookup"><span data-stu-id="dee00-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee00-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dee00-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dee00-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dee00-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dee00-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dee00-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dee00-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dee00-139">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="dee00-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dee00-140">End of client support</span></span><br/>    | <span data-ttu-id="dee00-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dee00-141">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="dee00-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="dee00-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dee00-143"><dt>IVMGuestOS. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dee00-143"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="dee00-144">IID</span><span class="sxs-lookup"><span data-stu-id="dee00-144">IID</span></span><br/>                      | <span data-ttu-id="dee00-145">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="dee00-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="dee00-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="dee00-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee00-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="dee00-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

