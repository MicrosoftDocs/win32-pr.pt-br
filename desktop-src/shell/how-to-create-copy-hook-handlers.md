---
description: Usando extensões de Shell para implementar um manipulador de vínculo de cópia.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Como criar manipuladores de cabo de cópia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169433"
---
# <a name="how-to-create-copy-hook-handlers"></a><span data-ttu-id="1839e-103">Como criar manipuladores de cabo de cópia</span><span class="sxs-lookup"><span data-stu-id="1839e-103">How to Create Copy Hook Handlers</span></span>

<span data-ttu-id="1839e-104">Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="1839e-104">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="1839e-105">Este documento se concentra nesses aspectos da implementação que são específicos para os manipuladores de cabo de cópia.</span><span class="sxs-lookup"><span data-stu-id="1839e-105">This document focuses on those aspects of implementation that are specific to copy hook handlers.</span></span>

-   [<span data-ttu-id="1839e-106">Implementando manipuladores do cabo de cópia</span><span class="sxs-lookup"><span data-stu-id="1839e-106">Implementing Copy Hook Handlers</span></span>](#step-1-implementing-copy-hook-handlers)
-   [<span data-ttu-id="1839e-107">Registrando manipuladores de cabo de cópia</span><span class="sxs-lookup"><span data-stu-id="1839e-107">Registering Copy Hook Handlers</span></span>](#step-2-registering-copy-hook-handlers)
-   [<span data-ttu-id="1839e-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1839e-108">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="1839e-109">Instruções</span><span class="sxs-lookup"><span data-stu-id="1839e-109">Instructions</span></span>

### <a name="step-1-implementing-copy-hook-handlers"></a><span data-ttu-id="1839e-110">Etapa 1: implementando manipuladores de cabo de cópia</span><span class="sxs-lookup"><span data-stu-id="1839e-110">Step 1: Implementing Copy Hook Handlers</span></span>

<span data-ttu-id="1839e-111">Como todos os manipuladores de extensão de Shell, os manipuladores de cabo de cópia são objetos COM (Component Object Model) em processo implementados como DLLs.</span><span class="sxs-lookup"><span data-stu-id="1839e-111">Like all Shell extension handlers, copy hook handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="1839e-112">Eles exportam uma interface além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1839e-112">They export one interface in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span></span> <span data-ttu-id="1839e-113">O Shell Inicializa o manipulador diretamente, portanto, não há necessidade de uma interface de inicialização, como [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span><span class="sxs-lookup"><span data-stu-id="1839e-113">The Shell initializes the handler directly, so there is no need for an initialization interface such as [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span></span>

<span data-ttu-id="1839e-114">A interface [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) tem um único método, [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1839e-114">The [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) interface has a single method, [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span></span> <span data-ttu-id="1839e-115">Quando uma pasta está prestes a ser movida, o Shell chama esse método.</span><span class="sxs-lookup"><span data-stu-id="1839e-115">When a folder is about to be moved, the Shell calls this method.</span></span> <span data-ttu-id="1839e-116">Ele passa uma variedade de informações, incluindo:</span><span class="sxs-lookup"><span data-stu-id="1839e-116">It passes in a variety of information, including:</span></span>

-   <span data-ttu-id="1839e-117">O nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="1839e-117">The folder's name.</span></span>
-   <span data-ttu-id="1839e-118">O destino da pasta ou o novo nome.</span><span class="sxs-lookup"><span data-stu-id="1839e-118">The folder's destination or new name.</span></span>
-   <span data-ttu-id="1839e-119">A operação que está sendo tentada.</span><span class="sxs-lookup"><span data-stu-id="1839e-119">The operation that is being attempted.</span></span>
-   <span data-ttu-id="1839e-120">Os atributos das pastas de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="1839e-120">The attributes of the source and destination folders.</span></span>
-   <span data-ttu-id="1839e-121">Um identificador de janela que pode ser usado para exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1839e-121">A window handle that can be used to display a user interface.</span></span>

<span data-ttu-id="1839e-122">Quando o método [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) do manipulador é chamado, ele retorna um dos três valores a seguir para indicar ao shell como ele deve continuar.</span><span class="sxs-lookup"><span data-stu-id="1839e-122">When your handler's [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) method is called, it returns one of the three following values to indicate to the Shell how it should proceed.</span></span>



| <span data-ttu-id="1839e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1839e-123">Value</span></span>    | <span data-ttu-id="1839e-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="1839e-124">Description</span></span>                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1839e-125">IDYES</span><span class="sxs-lookup"><span data-stu-id="1839e-125">IDYES</span></span>    | <span data-ttu-id="1839e-126">Permite a operação.</span><span class="sxs-lookup"><span data-stu-id="1839e-126">Allows the operation.</span></span>                                                                                                                            |
| <span data-ttu-id="1839e-127">IDNO</span><span class="sxs-lookup"><span data-stu-id="1839e-127">IDNO</span></span>     | <span data-ttu-id="1839e-128">Impede a operação nesta pasta.</span><span class="sxs-lookup"><span data-stu-id="1839e-128">Prevents the operation on this folder.</span></span> <span data-ttu-id="1839e-129">O Shell pode continuar com todas as outras operações que foram aprovadas, como uma operação de cópia em lote.</span><span class="sxs-lookup"><span data-stu-id="1839e-129">The Shell can continue with any other operations that have been approved, such as a batch copy operation.</span></span> |
| <span data-ttu-id="1839e-130">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="1839e-130">IDCANCEL</span></span> | <span data-ttu-id="1839e-131">Impede a operação atual e cancela as operações pendentes.</span><span class="sxs-lookup"><span data-stu-id="1839e-131">Prevents the current operation and cancels any pending operations.</span></span>                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a><span data-ttu-id="1839e-132">Etapa 2: Registrando manipuladores de gancho de cópia</span><span class="sxs-lookup"><span data-stu-id="1839e-132">Step 2: Registering Copy Hook Handlers</span></span>

<span data-ttu-id="1839e-133">Copiar manipuladores de gancho para pastas são registrados na subchave **HKEY \_ classes \_ raiz** \\ **Directory** \\ **shellex** \\ **CopyHookHandlers** .</span><span class="sxs-lookup"><span data-stu-id="1839e-133">Copy hook handlers for folders are registered under the **HKEY\_CLASSES\_ROOT**\\**Directory**\\**shellex**\\**CopyHookHandlers** subkey.</span></span> <span data-ttu-id="1839e-134">Crie uma subchave de **CopyHookHandlers** chamada para o manipulador e defina o valor padrão da subchave como a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do manipulador.</span><span class="sxs-lookup"><span data-stu-id="1839e-134">Create a subkey of **CopyHookHandlers** named for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="1839e-135">O exemplo a seguir adiciona a subchave **MyCopyHandler** à lista de manipuladores de cabo de cópia do Shell.</span><span class="sxs-lookup"><span data-stu-id="1839e-135">The following example adds the **MyCopyHandler** subkey to the Shell's list of copy hook handlers.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

<span data-ttu-id="1839e-136">Copiar manipuladores de gancho para objetos de impressora são registrados essencialmente da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="1839e-136">Copy hook handlers for printer objects are registered in essentially the same way.</span></span> <span data-ttu-id="1839e-137">A única diferença é que você deve registrá-los na subchave **HKEY \_ classes \_ root** \\ **prints** .</span><span class="sxs-lookup"><span data-stu-id="1839e-137">The only difference is that you must register them under the **HKEY\_CLASSES\_ROOT**\\**Printers** subkey.</span></span>

## <a name="remarks"></a><span data-ttu-id="1839e-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="1839e-138">Remarks</span></span>

<span data-ttu-id="1839e-139">Normalmente, os usuários e os aplicativos podem copiar, mover, excluir ou renomear pastas com poucas restrições.</span><span class="sxs-lookup"><span data-stu-id="1839e-139">Normally, users and applications can copy, move, delete, or rename folders with few restrictions.</span></span> <span data-ttu-id="1839e-140">Ao implementar um manipulador de cópia de cabo, você pode controlar se essas operações ocorrem.</span><span class="sxs-lookup"><span data-stu-id="1839e-140">By implementing a copy hook handler, you can control whether these operations take place.</span></span> <span data-ttu-id="1839e-141">Por exemplo, a implementação desse manipulador permite impedir que pastas críticas sejam renomeadas ou excluídas.</span><span class="sxs-lookup"><span data-stu-id="1839e-141">For instance, implementing such a handler allows you to prevent critical folders from being renamed or deleted.</span></span> <span data-ttu-id="1839e-142">Os manipuladores de cabo de cópia também podem ser implementados para objetos de impressora.</span><span class="sxs-lookup"><span data-stu-id="1839e-142">Copy hook handlers can also be implemented for printer objects.</span></span>

<span data-ttu-id="1839e-143">Os manipuladores de cabo de cópia são globais.</span><span class="sxs-lookup"><span data-stu-id="1839e-143">Copy hook handlers are global.</span></span> <span data-ttu-id="1839e-144">O Shell chama todos os manipuladores registrados toda vez que um aplicativo ou um usuário tenta copiar, mover, excluir ou renomear uma pasta ou um objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="1839e-144">The Shell calls all registered handlers every time an application or user attempts to copy, move, delete, or rename a folder or printer object.</span></span> <span data-ttu-id="1839e-145">O manipulador não executa a própria operação.</span><span class="sxs-lookup"><span data-stu-id="1839e-145">The handler does not perform the operation itself.</span></span> <span data-ttu-id="1839e-146">Ele apenas aprova ou veta.</span><span class="sxs-lookup"><span data-stu-id="1839e-146">It only approves or vetoes it.</span></span> <span data-ttu-id="1839e-147">Se todos os manipuladores aprovarem, o Shell fará a operação.</span><span class="sxs-lookup"><span data-stu-id="1839e-147">If all handlers approve, the Shell does the operation.</span></span> <span data-ttu-id="1839e-148">Se qualquer manipulador vetar a operação, ele será cancelado e os manipuladores restantes não serão chamados.</span><span class="sxs-lookup"><span data-stu-id="1839e-148">If any handler vetoes the operation, it is canceled and the remaining handlers are not called.</span></span> <span data-ttu-id="1839e-149">Os manipuladores de cabo de cópia não são informados sobre o êxito ou a falha da operação, portanto, eles não podem ser usados para monitorar operações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1839e-149">Copy hook handlers are not informed of the success or failure of the operation, so they cannot be used to monitor file operations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1839e-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1839e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1839e-151">Criar Manipuladores de Extensão de Shell</span><span class="sxs-lookup"><span data-stu-id="1839e-151">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

<span data-ttu-id="1839e-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1839e-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span></span>
</dt> </dl>

 

 
