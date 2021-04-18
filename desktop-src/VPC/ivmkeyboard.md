---
title: Interface IVMKeyboard (VPCCOMInterfaces. h)
description: Controla o dispositivo de teclado em uma máquina virtual. O IVMKeyboard para uma máquina virtual pode ser recuperado usando a propriedade de teclado IVMVirtualMachine.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Virtual PC de interface IVMKeyboard
- Virtual PC de interface IVMKeyboard, descrito
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784983"
---
# <a name="ivmkeyboard-interface"></a><span data-ttu-id="de540-106">Interface IVMKeyboard</span><span class="sxs-lookup"><span data-stu-id="de540-106">IVMKeyboard interface</span></span>

<span data-ttu-id="de540-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="de540-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="de540-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="de540-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="de540-109">Controla o dispositivo de teclado em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de540-109">Controls the keyboard device within a virtual machine.</span></span> <span data-ttu-id="de540-110">O **IVMKeyboard** para uma máquina virtual pode ser recuperado usando a propriedade [**IVMVirtualMachine:: Keyboard**](ivmvirtualmachine-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="de540-110">The **IVMKeyboard** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Keyboard**](ivmvirtualmachine-keyboard.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="de540-111">Membros</span><span class="sxs-lookup"><span data-stu-id="de540-111">Members</span></span>

<span data-ttu-id="de540-112">A interface **IVMKeyboard** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="de540-112">The **IVMKeyboard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="de540-113">**IVMKeyboard** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="de540-113">**IVMKeyboard** also has these types of members:</span></span>

-   [<span data-ttu-id="de540-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="de540-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="de540-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de540-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="de540-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="de540-116">Methods</span></span>

<span data-ttu-id="de540-117">A interface **IVMKeyboard** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="de540-117">The **IVMKeyboard** interface has these methods.</span></span>



| <span data-ttu-id="de540-118">Método</span><span class="sxs-lookup"><span data-stu-id="de540-118">Method</span></span>                                                       | <span data-ttu-id="de540-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="de540-119">Description</span></span>                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="de540-120">**Ispressioned**</span><span class="sxs-lookup"><span data-stu-id="de540-120">**IsPressed**</span></span>](ivmkeyboard-ispressed.md)                   | <span data-ttu-id="de540-121">Determina se a chave especificada está inativa.</span><span class="sxs-lookup"><span data-stu-id="de540-121">Determines whether the specified key is down.</span></span><br/>                      |
| [<span data-ttu-id="de540-122">**PressAndReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="de540-122">**PressAndReleaseKey**</span></span>](ivmkeyboard-pressandreleasekey.md) | <span data-ttu-id="de540-123">Simula uma tecla que está sendo pressionada e liberada.</span><span class="sxs-lookup"><span data-stu-id="de540-123">Simulates a key being pressed down and then released.</span></span><br/>              |
| [<span data-ttu-id="de540-124">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="de540-124">**PressKey**</span></span>](ivmkeyboard-presskey.md)                     | <span data-ttu-id="de540-125">Simula uma tecla que está sendo pressionada.</span><span class="sxs-lookup"><span data-stu-id="de540-125">Simulates a key being pressed down.</span></span><br/>                                |
| [<span data-ttu-id="de540-126">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="de540-126">**ReleaseKey**</span></span>](ivmkeyboard-releasekey.md)                 | <span data-ttu-id="de540-127">Simula uma chave que está sendo liberada.</span><span class="sxs-lookup"><span data-stu-id="de540-127">Simulates a key being released.</span></span><br/>                                    |
| [<span data-ttu-id="de540-128">**TypeAsciiText**</span><span class="sxs-lookup"><span data-stu-id="de540-128">**TypeAsciiText**</span></span>](ivmkeyboard-typeasciitext.md)           | <span data-ttu-id="de540-129">Simula uma série de chaves ASCII que estão sendo digitadas no convidado.</span><span class="sxs-lookup"><span data-stu-id="de540-129">Simulates a series of ASCII keys being typed into the guest.</span></span><br/>       |
| [<span data-ttu-id="de540-130">**TypeKeySequence**</span><span class="sxs-lookup"><span data-stu-id="de540-130">**TypeKeySequence**</span></span>](ivmkeyboard-typekeysequence.md)       | <span data-ttu-id="de540-131">Simula uma lista delimitada por vírgulas de chaves que estão sendo digitadas no convidado.</span><span class="sxs-lookup"><span data-stu-id="de540-131">Simulates a comma-delimited list of keys being typed in the guest.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="de540-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de540-132">Properties</span></span>

<span data-ttu-id="de540-133">A interface **IVMKeyboard** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="de540-133">The **IVMKeyboard** interface has these properties.</span></span>



| <span data-ttu-id="de540-134">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de540-134">Property</span></span>                                                                | <span data-ttu-id="de540-135">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="de540-135">Access type</span></span>           | <span data-ttu-id="de540-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="de540-136">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de540-137">**HasExclusiveAccess**</span><span class="sxs-lookup"><span data-stu-id="de540-137">**HasExclusiveAccess**</span></span>](ivmkeyboard-hasexclusiveaccess.md)<br/> | <span data-ttu-id="de540-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="de540-138">Read/write</span></span><br/> | <span data-ttu-id="de540-139">Indica se este objeto tem controle exclusivo sobre o dispositivo de teclado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de540-139">Indicates whether this object has exclusive control over the virtual machine's keyboard device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de540-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="de540-140">Remarks</span></span>

<span data-ttu-id="de540-141">As chaves podem ser digitadas na máquina virtual de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="de540-141">Keys can be typed into the virtual machine in several ways.</span></span> <span data-ttu-id="de540-142">Para digitar uma sequência ASCII normal de caracteres, use o método [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) .</span><span class="sxs-lookup"><span data-stu-id="de540-142">To type a normal ASCII sequence of characters, use the [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) method.</span></span> <span data-ttu-id="de540-143">Se for necessária maior flexibilidade, o **IVMKeyboard** terá vários métodos projetados para serem usados com os códigos de chave na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="de540-143">If greater flexibility is required, **IVMKeyboard** has several methods that are designed to be used with the key codes in the following list.</span></span> <span data-ttu-id="de540-144">O método [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) pode aceitar uma cadeia de caracteres delimitada por vírgulas de códigos de chave, que serão prensados e liberados, em ordem, dentro da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de540-144">The [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) method can accept a comma-delimited string of key codes, which will be pressed and released, in order, within the virtual machine.</span></span> <span data-ttu-id="de540-145">Além desses códigos-chave, as palavras-chave para cima e para baixo podem ser usadas para forçar uma tecla a ser pressionada apenas ou ser liberada.</span><span class="sxs-lookup"><span data-stu-id="de540-145">In addition to these key codes, the keywords UP and DOWN can be used to force a key to only be pressed, or only be released.</span></span> <span data-ttu-id="de540-146">As palavras-chave para cima e para baixo aplicam-se apenas ao código de tecla diretamente após a palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="de540-146">The UP and DOWN keywords only apply to the key code directly following the keyword.</span></span>

<span data-ttu-id="de540-147">Para evitar que vários scripts, aplicativos ou usuários tentem simultaneamente acessar o mesmo dispositivo de teclado, defina a propriedade [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="de540-147">To avoid multiple scripts, applications, or users from simultaneously attempting to access the same keyboard device, set the [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) property to **TRUE**.</span></span> <span data-ttu-id="de540-148">Se o acesso exclusivo for adquirido por um processo, as tentativas feitas por outros processos para enviar a entrada para o dispositivo de teclado serão ignoradas até que o acesso exclusivo seja liberado.</span><span class="sxs-lookup"><span data-stu-id="de540-148">If exclusive access is acquired by one process, any attempts by other processes to send input to the keyboard device will be ignored until exclusive access has been released.</span></span>

## <a name="requirements"></a><span data-ttu-id="de540-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de540-149">Requirements</span></span>



| <span data-ttu-id="de540-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="de540-150">Requirement</span></span> | <span data-ttu-id="de540-151">Valor</span><span class="sxs-lookup"><span data-stu-id="de540-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="de540-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de540-152">Minimum supported client</span></span><br/> | <span data-ttu-id="de540-153">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="de540-153">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de540-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de540-154">Minimum supported server</span></span><br/> | <span data-ttu-id="de540-155">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="de540-155">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="de540-156">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="de540-156">End of client support</span></span><br/>    | <span data-ttu-id="de540-157">Windows 7</span><span class="sxs-lookup"><span data-stu-id="de540-157">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="de540-158">Produto</span><span class="sxs-lookup"><span data-stu-id="de540-158">Product</span></span><br/>                  | <span data-ttu-id="de540-159">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="de540-159">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="de540-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de540-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="de540-161"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="de540-161"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="de540-162">IID</span><span class="sxs-lookup"><span data-stu-id="de540-162">IID</span></span><br/>                      | <span data-ttu-id="de540-163">IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="de540-163">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="de540-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="de540-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de540-165">Interfaces do Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="de540-165">Windows Virtual PC Interfaces</span></span>](virtual-pc-interfaces.md)
</dt> <dt>

[<span data-ttu-id="de540-166">Sequências de chave</span><span class="sxs-lookup"><span data-stu-id="de540-166">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

