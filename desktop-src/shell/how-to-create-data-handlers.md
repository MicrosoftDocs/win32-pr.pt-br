---
description: Estendendo a área de transferência com manipuladores de formato de dados personalizados.
title: Como criar manipuladores de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988984"
---
# <a name="how-to-create-data-handlers"></a><span data-ttu-id="01ad8-103">Como criar manipuladores de dados</span><span class="sxs-lookup"><span data-stu-id="01ad8-103">How to Create Data Handlers</span></span>

<span data-ttu-id="01ad8-104">Quando um arquivo é copiado para a área de transferência ou arrastado e descartado, o Shell cria um objeto de dados que dá suporte a uma variedade de [formatos de área de transferência](dragdrop.md)padrão.</span><span class="sxs-lookup"><span data-stu-id="01ad8-104">When a file is copied to the clipboard or dragged and dropped, the Shell creates a data object that supports a variety of standard [clipboard formats](dragdrop.md).</span></span> <span data-ttu-id="01ad8-105">Para arquivos que são de um tipo de arquivo específico, você pode estender os formatos de área de transferência disponíveis implementando e registrando um *manipulador de dados*.</span><span class="sxs-lookup"><span data-stu-id="01ad8-105">For files that are of a specific file type, you can extend the available clipboard formats by implementing and registering a *data handler*.</span></span> <span data-ttu-id="01ad8-106">Quando um arquivo do tipo de arquivo for transferido, o Shell delegará chamadas para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados para o manipulador de dados se um dos formatos personalizados for usado.</span><span class="sxs-lookup"><span data-stu-id="01ad8-106">When a file of the file type is transferred, the Shell delegates calls to the data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface to the data handler if one of the custom formats is used.</span></span>

<span data-ttu-id="01ad8-107">Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="01ad8-107">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="01ad8-108">Este documento se concentra nesses aspectos da implementação que são específicos de manipuladores de dados.</span><span class="sxs-lookup"><span data-stu-id="01ad8-108">This document focuses on those aspects of implementation that are specific to data handlers.</span></span>

-   [<span data-ttu-id="01ad8-109">Implementando manipuladores de dados</span><span class="sxs-lookup"><span data-stu-id="01ad8-109">Implementing Data Handlers</span></span>](#step-1-implementing-data-handlers)
-   [<span data-ttu-id="01ad8-110">Registrando manipuladores de dados</span><span class="sxs-lookup"><span data-stu-id="01ad8-110">Registering Data Handlers</span></span>](#step-2-registering-data-handlers)
-   [<span data-ttu-id="01ad8-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01ad8-111">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="01ad8-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="01ad8-112">Instructions</span></span>

### <a name="step-1-implementing-data-handlers"></a><span data-ttu-id="01ad8-113">Etapa 1: implementando manipuladores de dados</span><span class="sxs-lookup"><span data-stu-id="01ad8-113">Step 1: Implementing Data Handlers</span></span>

<span data-ttu-id="01ad8-114">Como todos os manipuladores de extensão do Shell, os manipuladores de dados são objetos COM (Component Object Model) em processo implementados como DLLs.</span><span class="sxs-lookup"><span data-stu-id="01ad8-114">Like all Shell extension handlers, data handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="01ad8-115">Eles exportam duas interfaces além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="01ad8-115">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span></span>

<span data-ttu-id="01ad8-116">O Shell Inicializa o manipulador por meio de sua interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="01ad8-116">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="01ad8-117">Ele usa essa interface para solicitar o identificador de classe do manipulador (CLSID) e fornece o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="01ad8-117">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="01ad8-118">Para obter uma discussão geral sobre como implementar manipuladores de extensão de Shell, incluindo a interface **IPersistFile** , consulte [criando manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="01ad8-118">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="01ad8-119">Depois que o manipulador de dados for inicializado, o Shell delegará chamadas do objeto de dados para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do manipulador se um dos formatos personalizados for usado.</span><span class="sxs-lookup"><span data-stu-id="01ad8-119">Once the data handler is initialized, the Shell delegates calls from the data object to the handler's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface if one of the custom formats is used.</span></span>

### <a name="step-2-registering-data-handlers"></a><span data-ttu-id="01ad8-120">Etapa 2: Registrando manipuladores de dados</span><span class="sxs-lookup"><span data-stu-id="01ad8-120">Step 2: Registering Data Handlers</span></span>

<span data-ttu-id="01ad8-121">Os manipuladores de dados são registrados na subchave *ProgID* do tipo de arquivo, conforme mostrado aqui: **HKEY \_ classes \_ raiz** \\ *ProgID* \\ **shellex** \\ **DataHandler**</span><span class="sxs-lookup"><span data-stu-id="01ad8-121">Data handlers are registered under the file type's *ProgID* subkey as shown here: **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shellex**\\**DataHandler**</span></span>

<span data-ttu-id="01ad8-122">Crie uma subchave chamada para o manipulador em **DataHandler** e defina o valor padrão da subchave desse manipulador como a forma de cadeia de caracteres do GUID CLSID do manipulador.</span><span class="sxs-lookup"><span data-stu-id="01ad8-122">Create a subkey named for the handler under **DataHandler** and set the default value of that handler's subkey to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="01ad8-123">Para obter uma discussão geral sobre como registrar manipuladores de extensão de Shell, consulte [criando manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="01ad8-123">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="01ad8-124">O exemplo a seguir ilustra as entradas do registro que habilitam um manipulador de dados para um tipo de arquivo. MYP de exemplo.</span><span class="sxs-lookup"><span data-stu-id="01ad8-124">The following example illustrates registry entries that enable a data handler for an example .myp file type.</span></span>

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="01ad8-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01ad8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01ad8-126">Criar Manipuladores de Extensão de Shell</span><span class="sxs-lookup"><span data-stu-id="01ad8-126">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="01ad8-127">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="01ad8-127">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[<span data-ttu-id="01ad8-128">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="01ad8-128">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
