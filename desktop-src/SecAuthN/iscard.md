---
description: Permite abrir e gerenciar uma conexão com um cartão inteligente.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interface iscard (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502355"
---
# <a name="iscard-interface"></a><span data-ttu-id="1f3fe-103">Interface iscard</span><span class="sxs-lookup"><span data-stu-id="1f3fe-103">ISCard interface</span></span>

<span data-ttu-id="1f3fe-104">\[A interface **iscard** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-104">\[The **ISCard** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1f3fe-105">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1f3fe-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1f3fe-106">A interface **iscard** permite que você abra e gerencie uma conexão a um [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1f3fe-106">The **ISCard** interface lets you open and manage a connection to a [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1f3fe-107">Cada conexão com um cartão requer uma única instância correspondente da interface **iscard** .</span><span class="sxs-lookup"><span data-stu-id="1f3fe-107">Each connection to a card requires a single, corresponding instance of the **ISCard** interface.</span></span>

<span data-ttu-id="1f3fe-108">O Gerenciador de [*recursos*](../secgloss/r-gly.md) de cartão inteligente deve estar disponível sempre que uma instância do **iscard** for criada.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-108">The smart card [*resource manager*](../secgloss/r-gly.md) must be available whenever an instance of **ISCard** is created.</span></span> <span data-ttu-id="1f3fe-109">Se esse serviço não estiver disponível, a criação da interface falhará.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-109">If this service is unavailable, creation of the interface will fail.</span></span>

<span data-ttu-id="1f3fe-110">O exemplo a seguir mostra um uso típico da interface **iscard** .</span><span class="sxs-lookup"><span data-stu-id="1f3fe-110">The following example shows a typical use of the **ISCard** interface.</span></span> <span data-ttu-id="1f3fe-111">A interface **iscard** é usada para se conectar ao cartão inteligente, enviar uma [*transação*](../secgloss/t-gly.md)e liberar o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-111">The **ISCard** interface is used to connect to the smart card, submit a [*transaction*](../secgloss/t-gly.md), and release the smart card.</span></span>

<span data-ttu-id="1f3fe-112">**Para enviar uma transação para um cartão específico**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="1f3fe-113">Crie uma interface **iscard** .</span><span class="sxs-lookup"><span data-stu-id="1f3fe-113">Create an **ISCard** interface.</span></span>
2.  <span data-ttu-id="1f3fe-114">Anexe a um cartão inteligente especificando um [*leitor*](../secgloss/r-gly.md) de cartão inteligente ou usando um identificador válido estabelecido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-114">Attach to a smart card by specifying a smart card [*reader*](../secgloss/r-gly.md) or by using a previously established, valid handle.</span></span>
3.  <span data-ttu-id="1f3fe-115">Crie comandos de transação com as interfaces de cartão inteligente [**ISCardCmd**](iscardcmd.md)e [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="1f3fe-115">Create transaction commands with [**ISCardCmd**](iscardcmd.md), and [**ISCardISO7816**](iscardiso7816.md) smart card interfaces.</span></span>
4.  <span data-ttu-id="1f3fe-116">Use **iscard** para enviar os comandos de transação para processamento pelo cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-116">Use **ISCard** to submit the transaction commands for processing by the smart card.</span></span>
5.  <span data-ttu-id="1f3fe-117">Use **iscard** para liberar o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-117">Use **ISCard** to release the smart card.</span></span>
6.  <span data-ttu-id="1f3fe-118">Libere a interface **iscard** .</span><span class="sxs-lookup"><span data-stu-id="1f3fe-118">Release the **ISCard** interface.</span></span>

## <a name="members"></a><span data-ttu-id="1f3fe-119">Membros</span><span class="sxs-lookup"><span data-stu-id="1f3fe-119">Members</span></span>

<span data-ttu-id="1f3fe-120">A interface **Iscard** é herdada da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1f3fe-120">The **ISCard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1f3fe-121">**Iscard** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1f3fe-121">**ISCard** also has these types of members:</span></span>

-   [<span data-ttu-id="1f3fe-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f3fe-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="1f3fe-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f3fe-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1f3fe-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f3fe-124">Methods</span></span>

<span data-ttu-id="1f3fe-125">A interface **iscard** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-125">The **ISCard** interface has these methods.</span></span>



| <span data-ttu-id="1f3fe-126">Método</span><span class="sxs-lookup"><span data-stu-id="1f3fe-126">Method</span></span>                                          | <span data-ttu-id="1f3fe-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f3fe-127">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f3fe-128">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-128">**AttachByHandle**</span></span>](iscard-attachbyhandle.md) | <span data-ttu-id="1f3fe-129">Anexa um objeto a um identificador de cartão inteligente aberto e configurado.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-129">Attaches an object to an open and configured smart card handle.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="1f3fe-130">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-130">**AttachByReader**</span></span>](iscard-attachbyreader.md) | <span data-ttu-id="1f3fe-131">Abre o cartão inteligente no leitor nomeado.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-131">Opens the smart card in the named reader.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="1f3fe-132">**Detach**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-132">**Detach**</span></span>](iscard-detach.md)                 | <span data-ttu-id="1f3fe-133">Fecha a conexão aberta com o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-133">Closes the open connection to the smart card.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="1f3fe-134">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-134">**LockSCard**</span></span>](iscard-lockscard.md)           | <span data-ttu-id="1f3fe-135">Alega acesso exclusivo ao cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-135">Claims exclusive access to the smart card.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="1f3fe-136">**Anexar novamente**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-136">**ReAttach**</span></span>](iscard-reattach.md)             | <span data-ttu-id="1f3fe-137">Redefine e reinicializa o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-137">Resets and reinitializes the smart card.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="1f3fe-138">**Transação**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-138">**Transaction**</span></span>](iscard-transaction.md)       | <span data-ttu-id="1f3fe-139">Executa uma operação de gravação e leitura no objeto de comando de cartão inteligente ([*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="1f3fe-139">Executes a write and read operation on the smart card command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span><br/> |
| [<span data-ttu-id="1f3fe-140">**UnlockScard**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-140">**UnlockScard**</span></span>](iscard-unlockscard.md)       | <span data-ttu-id="1f3fe-141">Libera o acesso exclusivo ao cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-141">Releases exclusive access to the smart card.</span></span><br/>                                                                                                                                                                         |



 

### <a name="properties"></a><span data-ttu-id="1f3fe-142">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f3fe-142">Properties</span></span>

<span data-ttu-id="1f3fe-143">A interface **iscard** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-143">The **ISCard** interface has these properties.</span></span>



| <span data-ttu-id="1f3fe-144">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1f3fe-144">Property</span></span>                                               | <span data-ttu-id="1f3fe-145">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="1f3fe-145">Access type</span></span>          | <span data-ttu-id="1f3fe-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f3fe-146">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f3fe-147">**Atr**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-147">**Atr**</span></span>](iscard-get-atr.md)<br/>               | <span data-ttu-id="1f3fe-148">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f3fe-148">Read-only</span></span><br/> | <span data-ttu-id="1f3fe-149">Recupera a [*cadeia de caracteres ATR*](../secgloss/a-gly.md) do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-149">Retrieves the [*ATR string*](../secgloss/a-gly.md) of the smart card.</span></span><br/>                                                                   |
| [<span data-ttu-id="1f3fe-150">**CardHandle**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-150">**CardHandle**</span></span>](iscard-get-cardhandle.md)<br/> | <span data-ttu-id="1f3fe-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f3fe-151">Read-only</span></span><br/> | <span data-ttu-id="1f3fe-152">Recupera o identificador do cartão inteligente conectado.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-152">Retrieves the handle for the connected smart card.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="1f3fe-153">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-153">**Context**</span></span>](iscard-get-context.md)<br/>       | <span data-ttu-id="1f3fe-154">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f3fe-154">Read-only</span></span><br/> | <span data-ttu-id="1f3fe-155">Recupera o identificador de contexto atual do [*Resource Manager*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1f3fe-155">Retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span><br/>                            |
| [<span data-ttu-id="1f3fe-156">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-156">**Protocol**</span></span>](iscard-get-protocol.md)<br/>     | <span data-ttu-id="1f3fe-157">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f3fe-157">Read-only</span></span><br/> | <span data-ttu-id="1f3fe-158">Recupera o identificador do protocolo atualmente em uso no cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-158">Retrieves the identifier of the protocol currently in use on the smart card.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="1f3fe-159">**Status**</span><span class="sxs-lookup"><span data-stu-id="1f3fe-159">**Status**</span></span>](iscard-get-status.md)<br/>         | <span data-ttu-id="1f3fe-160">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f3fe-160">Read-only</span></span><br/> | <span data-ttu-id="1f3fe-161">Recupera o [*estado*](../secgloss/s-gly.md) atual em que o [*cartão inteligente*](../secgloss/s-gly.md) está.</span><span class="sxs-lookup"><span data-stu-id="1f3fe-161">Retrieves the current [*state*](../secgloss/s-gly.md) the [*smart card*](../secgloss/s-gly.md) is in.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1f3fe-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f3fe-162">Requirements</span></span>



| <span data-ttu-id="1f3fe-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f3fe-163">Requirement</span></span> | <span data-ttu-id="1f3fe-164">Valor</span><span class="sxs-lookup"><span data-stu-id="1f3fe-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3fe-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f3fe-165">Minimum supported client</span></span><br/> | <span data-ttu-id="1f3fe-166">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1f3fe-166">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f3fe-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f3fe-167">Minimum supported server</span></span><br/> | <span data-ttu-id="1f3fe-168">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f3fe-168">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f3fe-169">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1f3fe-169">End of client support</span></span><br/>    | <span data-ttu-id="1f3fe-170">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1f3fe-170">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1f3fe-171">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1f3fe-171">End of server support</span></span><br/>    | <span data-ttu-id="1f3fe-172">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f3fe-172">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1f3fe-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f3fe-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f3fe-174"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f3fe-174"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f3fe-175">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1f3fe-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f3fe-176"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1f3fe-176"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1f3fe-177">DLL</span><span class="sxs-lookup"><span data-stu-id="1f3fe-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f3fe-178"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f3fe-178"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f3fe-179">IID</span><span class="sxs-lookup"><span data-stu-id="1f3fe-179">IID</span></span><br/>                      | <span data-ttu-id="1f3fe-180">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1f3fe-180">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



 

 
