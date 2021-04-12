---
title: Propriedade IVMVirtualMachine ShutdownActionOnQuit (VPCCOMInterfaces. h)
description: Ação a ser executada nesta máquina virtual se estiver em execução quando o Windows Virtual PC for encerrado.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Propriedade ShutdownActionOnQuit Virtual PC
- Propriedade ShutdownActionOnQuit Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade ShutdownActionOnQuit
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455684"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a><span data-ttu-id="787ef-106">Propriedade IVMVirtualMachine:: ShutdownActionOnQuit</span><span class="sxs-lookup"><span data-stu-id="787ef-106">IVMVirtualMachine::ShutdownActionOnQuit property</span></span>

<span data-ttu-id="787ef-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="787ef-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="787ef-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="787ef-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="787ef-109">Recupera e define a ação a ser executada nessa VM (máquina virtual) se ela estiver em execução quando o Windows Virtual PC for encerrado.</span><span class="sxs-lookup"><span data-stu-id="787ef-109">Retrieves and sets the action to be performed on this virtual machine (VM) if it is running when Windows Virtual PC is quit.</span></span>

<span data-ttu-id="787ef-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="787ef-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="787ef-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="787ef-111">Syntax</span></span>


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a><span data-ttu-id="787ef-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="787ef-112">Property value</span></span>

<span data-ttu-id="787ef-113">Especifica como desligar essa VM se ela estiver em execução quando o Windows Virtual PC for encerrado.</span><span class="sxs-lookup"><span data-stu-id="787ef-113">Specifies how to shut down this VM if it is running when Windows Virtual PC is quit.</span></span> <span data-ttu-id="787ef-114">Para obter uma lista de valores, consulte [**VMShutdownAction**](vmshutdownaction.md).</span><span class="sxs-lookup"><span data-stu-id="787ef-114">For a list of values, see [**VMShutdownAction**](vmshutdownaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="787ef-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="787ef-115">Error codes</span></span>



| <span data-ttu-id="787ef-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="787ef-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="787ef-117">Significado</span><span class="sxs-lookup"><span data-stu-id="787ef-117">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="787ef-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="787ef-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="787ef-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="787ef-119">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="787ef-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="787ef-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="787ef-121">O parâmetro é **nulo** ou não é um valor válido.</span><span class="sxs-lookup"><span data-stu-id="787ef-121">The parameter is **NULL** or not a valid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="787ef-122"><dt>E \_ ACCESSDENIED</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="787ef-122"><dt>E\_ACCESSDENIED</dt> <dt>0x80070005</dt></span></span> </dl>    | <span data-ttu-id="787ef-123">O usuário atual não tem acesso suficiente ao arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="787ef-123">The current user has insufficient access to the configuration file.</span></span><br/> |
| <dl> <span data-ttu-id="787ef-124"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="787ef-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="787ef-125">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="787ef-125">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="787ef-126"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="787ef-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="787ef-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="787ef-127">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="remarks"></a><span data-ttu-id="787ef-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="787ef-128">Remarks</span></span>

<span data-ttu-id="787ef-129">Por padrão, as VMs em execução são salvas quando o Windows Virtual PC é encerrado.</span><span class="sxs-lookup"><span data-stu-id="787ef-129">By default, running VMs are saved when Windows Virtual PC is quit.</span></span> <span data-ttu-id="787ef-130">A ação de desligamento **vmShutdownAction \_ Save** (0) irá salvar o estado da VM.</span><span class="sxs-lookup"><span data-stu-id="787ef-130">The shutdown action **vmShutdownAction\_Save** (0) will save the VM's state.</span></span> <span data-ttu-id="787ef-131">A ação de desativação de **vmShutdownAction \_** (1) desligará a VM.</span><span class="sxs-lookup"><span data-stu-id="787ef-131">The **vmShutdownAction\_TurnOff** (1) action will turn off the VM.</span></span> <span data-ttu-id="787ef-132">A ação de **\_ desligamento vmShutdownAction** (2) desligará o sistema operacional convidado se os componentes de integração estiverem disponíveis e salvará a VM de outra forma.</span><span class="sxs-lookup"><span data-stu-id="787ef-132">The **vmShutdownAction\_Shutdown** (2) action will shut down the guest operating system if the integration components are available and will save the VM otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="787ef-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="787ef-133">Requirements</span></span>



| <span data-ttu-id="787ef-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="787ef-134">Requirement</span></span> | <span data-ttu-id="787ef-135">Valor</span><span class="sxs-lookup"><span data-stu-id="787ef-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="787ef-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="787ef-136">Minimum supported client</span></span><br/> | <span data-ttu-id="787ef-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="787ef-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="787ef-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="787ef-138">Minimum supported server</span></span><br/> | <span data-ttu-id="787ef-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="787ef-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="787ef-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="787ef-140">End of client support</span></span><br/>    | <span data-ttu-id="787ef-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="787ef-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="787ef-142">Produto</span><span class="sxs-lookup"><span data-stu-id="787ef-142">Product</span></span><br/>                  | <span data-ttu-id="787ef-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="787ef-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="787ef-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="787ef-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="787ef-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="787ef-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="787ef-146">IID</span><span class="sxs-lookup"><span data-stu-id="787ef-146">IID</span></span><br/>                      | <span data-ttu-id="787ef-147">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="787ef-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="787ef-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="787ef-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787ef-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="787ef-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="787ef-150">**VMShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="787ef-150">**VMShutdownAction**</span></span>](vmshutdownaction.md)
</dt> </dl>

 

