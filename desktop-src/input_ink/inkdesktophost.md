---
description: Implementa a interface IInkDesktopHost.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Classe InkDesktopHost
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: d5dac80a4ee09bb4b78a4d61ca0efa74e99babb9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105764326"
---
# <a name="inkdesktophost-class"></a><span data-ttu-id="b4c55-103">Classe InkDesktopHost</span><span class="sxs-lookup"><span data-stu-id="b4c55-103">InkDesktopHost class</span></span>

<span data-ttu-id="b4c55-104">Implementa a interface [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) .</span><span class="sxs-lookup"><span data-stu-id="b4c55-104">Implements the [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) interface.</span></span>

<span data-ttu-id="b4c55-105">Um objeto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) permite entrada, processamento e renderização de tinta por meio da criação de um thread de aplicativo para hospedar um objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e inseri-lo na árvore visual do [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b4c55-105">An [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) object enables ink input, processing, and rendering through the creation of an app thread to host an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object and insert it into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

## <a name="members"></a><span data-ttu-id="b4c55-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b4c55-106">Members</span></span>

<span data-ttu-id="b4c55-107">A classe **InkDesktopHost** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b4c55-107">The **InkDesktopHost** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b4c55-108">**InkDesktopHost** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b4c55-108">**InkDesktopHost** also has these types of members:</span></span>

- [<span data-ttu-id="b4c55-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4c55-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b4c55-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4c55-110">Methods</span></span>

<span data-ttu-id="b4c55-111">A classe **InkDesktopHost** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b4c55-111">The **InkDesktopHost** class has these methods.</span></span>

| <span data-ttu-id="b4c55-112">Método</span><span class="sxs-lookup"><span data-stu-id="b4c55-112">Method</span></span> | <span data-ttu-id="b4c55-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4c55-113">Description</span></span> |
|---|---|
| [<span data-ttu-id="b4c55-114">**CreateAndInitializeInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="b4c55-114">**CreateAndInitializeInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | <span data-ttu-id="b4c55-115">Cria um objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) em um thread de aplicativo, conecta-o à árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo e define o tamanho do objeto.</span><span class="sxs-lookup"><span data-stu-id="b4c55-115">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread, connects it to the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree, and sets the size of the object.</span></span><br/> |
| [<span data-ttu-id="b4c55-116">**Createinkpresenter**</span><span class="sxs-lookup"><span data-stu-id="b4c55-116">**CreateInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | <span data-ttu-id="b4c55-117">Cria um objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) em um thread de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b4c55-117">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread.</span></span><br/> |
| [<span data-ttu-id="b4c55-118">**QueueWorkItem**</span><span class="sxs-lookup"><span data-stu-id="b4c55-118">**QueueWorkItem**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | <span data-ttu-id="b4c55-119">Adicione uma operação de tinta a uma fila de trabalho para execução no thread **InkDesktopHost** .</span><span class="sxs-lookup"><span data-stu-id="b4c55-119">Add an ink operation to a work queue for execution on the **InkDesktopHost** thread.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="b4c55-120">Criar \\ funções de acesso</span><span class="sxs-lookup"><span data-stu-id="b4c55-120">Creation\\Access Functions</span></span>

<span data-ttu-id="b4c55-121">Chame [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com o identificador de classe <strong>InkDesktopHost</strong> para recuperar uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="b4c55-121">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkDesktopHost</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&amp;_spInkHost));
```

## <a name="requirements"></a><span data-ttu-id="b4c55-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4c55-122">Requirements</span></span>

| <span data-ttu-id="b4c55-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4c55-123">Requirement</span></span> | <span data-ttu-id="b4c55-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b4c55-124">Value</span></span> |
|---|---|
| <span data-ttu-id="b4c55-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4c55-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b4c55-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b4c55-126">Windows 10 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b4c55-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4c55-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b4c55-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b4c55-128">None supported</span></span><br/> |
| <span data-ttu-id="b4c55-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4c55-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4c55-130"><dt>InkPresenterDesktop. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4c55-130"><dt>InkPresenterDesktop.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4c55-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="b4c55-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4c55-132"><dt>InkPresenterDesktop. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4c55-132"><dt>InkPresenterDesktop.idl</dt></span></span> </dl> |
| <span data-ttu-id="b4c55-133">IID</span><span class="sxs-lookup"><span data-stu-id="b4c55-133">IID</span></span><br/>                      | <span data-ttu-id="b4c55-134">IID \_ IInkDesktopHost é definido como 4ce7d875-A981-4140-a1ff-ad93258e8d59</span><span class="sxs-lookup"><span data-stu-id="b4c55-134">IID\_IInkDesktopHost is defined as 4ce7d875-a981-4140-a1ff-ad93258e8d59</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="b4c55-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4c55-135">Related topics</span></span>

<span data-ttu-id="b4c55-136">[Classes de apresentador de tinta](ink-presenter-classes.md), [interações de caneta e caneta](/windows/uwp/design/input/pen-and-stylus-interactions), [exemplo de análise de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), exemplo de [escrita simples](/samples/microsoft/windows-universal-samples/simpleink/), [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="b4c55-136">[Ink presenter classes](ink-presenter-classes.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
