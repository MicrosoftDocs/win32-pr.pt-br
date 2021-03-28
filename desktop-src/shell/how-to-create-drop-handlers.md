---
description: Como implementar e registrar um manipulador drop.
title: Como criar manipuladores drop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169432"
---
# <a name="how-to-create-drop-handlers"></a><span data-ttu-id="5c2e4-103">Como criar manipuladores drop</span><span class="sxs-lookup"><span data-stu-id="5c2e4-103">How to Create Drop Handlers</span></span>

<span data-ttu-id="5c2e4-104">Por padrão, os arquivos não são drop targets.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-104">By default, files are not drop targets.</span></span> <span data-ttu-id="5c2e4-105">Você pode tornar os membros de um [tipo de arquivo](fa-file-types.md) em drop targets implementando e registrando um *manipulador drop*.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-105">You can make the members of a [file type](fa-file-types.md) into drop targets by implementing and registering a *drop handler*.</span></span>

<span data-ttu-id="5c2e4-106">Se um manipulador drop for registrado para um tipo de arquivo, ele será chamado sempre que um objeto for arrastado ou descartado em um membro do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-106">If a drop handler is registered for a file type, it is called whenever an object is dragged over or dropped on a member of the file type.</span></span> <span data-ttu-id="5c2e4-107">O Shell gerencia a operação chamando os métodos apropriados na interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do manipulador.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-107">The Shell manages the operation by calling the appropriate methods on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

<span data-ttu-id="5c2e4-108">Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="5c2e4-108">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="5c2e4-109">Este documento se concentra nesses aspectos da implementação que são específicos para descartar manipuladores.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-109">This document focuses on those aspects of implementation that are specific to drop handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="5c2e4-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="5c2e4-110">Instructions</span></span>

### <a name="step-1-implementing-drop-handlers"></a><span data-ttu-id="5c2e4-111">Etapa 1: implementando manipuladores drop</span><span class="sxs-lookup"><span data-stu-id="5c2e4-111">Step 1: Implementing Drop Handlers</span></span>

<span data-ttu-id="5c2e4-112">Como todos os manipuladores de extensão do Shell, os manipuladores de descarte são objetos COM (Component Object Model) em processo implementados como DLLs.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-112">Like all Shell extension handlers, drop handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="5c2e4-113">Eles exportam duas interfaces além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span><span class="sxs-lookup"><span data-stu-id="5c2e4-113">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span></span>

<span data-ttu-id="5c2e4-114">O Shell Inicializa o manipulador por meio de sua interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="5c2e4-114">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="5c2e4-115">Ele usa essa interface para solicitar o identificador de classe do manipulador (CLSID) e fornece o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-115">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="5c2e4-116">Para obter uma discussão geral sobre como implementar manipuladores de extensão de Shell, incluindo a interface **IPersistFile** , consulte [criando manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="5c2e4-116">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="5c2e4-117">Depois que o manipulador drop é inicializado, o Shell chama o método apropriado na interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do manipulador.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-117">Once the drop handler is initialized, the Shell calls the appropriate method on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

### <a name="step-2-registering-drop-handlers"></a><span data-ttu-id="5c2e4-118">Etapa 2: Registrando manipuladores drop</span><span class="sxs-lookup"><span data-stu-id="5c2e4-118">Step 2: Registering Drop Handlers</span></span>

<span data-ttu-id="5c2e4-119">Os manipuladores de descarte são registrados sob a subchave deste tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-119">Drop handlers are registered under this file type's subkey.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

<span data-ttu-id="5c2e4-120">Crie uma subchave de **DropHandler** chamada para o manipulador e defina o valor padrão da subchave como a forma de cadeia de caracteres do GUID CLSID do manipulador.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-120">Create a subkey of **DropHandler** named for the handler, and set the subkey's default value to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="5c2e4-121">Para obter uma discussão geral sobre como registrar manipuladores de extensão de Shell, consulte [criando manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="5c2e4-121">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="5c2e4-122">O exemplo a seguir ilustra as entradas do registro que habilitam um manipulador drop para um tipo de arquivo example. MYP.</span><span class="sxs-lookup"><span data-stu-id="5c2e4-122">The following example illustrates registry entries that enable a drop handler for an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="5c2e4-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c2e4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c2e4-124">Criar Manipuladores de Extensão de Shell</span><span class="sxs-lookup"><span data-stu-id="5c2e4-124">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="5c2e4-125">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="5c2e4-125">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[<span data-ttu-id="5c2e4-126">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="5c2e4-126">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
