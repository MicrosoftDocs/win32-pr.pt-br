---
description: Visão geral dos controles de tinta para o Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Controles de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501627"
---
# <a name="ink-controls"></a><span data-ttu-id="32818-103">Controles de tinta</span><span class="sxs-lookup"><span data-stu-id="32818-103">Ink Controls</span></span>

<span data-ttu-id="32818-104">A plataforma do Tablet PC fornece dois controles, [InkEdit](inkedit-control.md) e [InkPicture](inkpicture-control.md), que permitem adicionar facilmente a tinta e o reconhecimento de manuscrito aos aplicativos do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="32818-104">The Tablet PC platform provides two controls, [InkEdit](inkedit-control.md) and [InkPicture](inkpicture-control.md), which enable you to easily add ink and handwriting recognition to Tablet PC applications.</span></span> <span data-ttu-id="32818-105">O controle InkEdit tem versões [gerenciadas](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) e Win32, enquanto a InkPicture tem apenas as versões gerenciadas e [ActiveX](inkpicture-control-reference.md) do [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="32818-105">The InkEdit control has [managed](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) , and Win32 versions, while InkPicture has only the managed [InkPicture](/previous-versions/ms583740(v=vs.100)) and [ActiveX](inkpicture-control-reference.md) versions.</span></span>

<span data-ttu-id="32818-106">A principal diferença entre os controles é a forma como os dados são salvos.</span><span class="sxs-lookup"><span data-stu-id="32818-106">The key difference between the controls is in how data is saved.</span></span> <span data-ttu-id="32818-107">O controle [InkEdit](inkedit-control.md) salva a tinta como texto por padrão, enquanto a [InkPicture](inkpicture-control.md) salva a tinta como tinta.</span><span class="sxs-lookup"><span data-stu-id="32818-107">The [InkEdit](inkedit-control.md) control saves ink as text by default, while [InkPicture](inkpicture-control.md) saves ink as ink.</span></span>

<span data-ttu-id="32818-108">O controle [InkEdit](inkedit-control.md) destina-se à entrada de texto por meio do reconhecimento de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="32818-108">The [InkEdit](inkedit-control.md) control is intended for text entry through handwriting recognition.</span></span> <span data-ttu-id="32818-109">O [InkPicture](inkpicture-control.md) destina-se à anotação (por exemplo, marcando um slide de apresentação ou outra imagem).</span><span class="sxs-lookup"><span data-stu-id="32818-109">[InkPicture](inkpicture-control.md) is intended for annotation (for example, marking up a presentation slide or other picture).</span></span>

<span data-ttu-id="32818-110">Em código gerenciado, crie controles de tinta no mesmo thread que o thread principal para o formulário.</span><span class="sxs-lookup"><span data-stu-id="32818-110">In managed code, create ink controls in the same thread as the main thread for the form.</span></span> <span data-ttu-id="32818-111">Se um controle [InkEdit](inkedit-control.md) ou [InkPicture](inkpicture-control.md) for criado em um thread diferente, o aplicativo poderá não responder corretamente.</span><span class="sxs-lookup"><span data-stu-id="32818-111">If an [InkEdit](inkedit-control.md) or [InkPicture](inkpicture-control.md) control is created in a different thread, then your application may not respond properly.</span></span>

<span data-ttu-id="32818-112">Você deve alterar explicitamente o modelo de threading para single-thread apartment (STA) antes de criar um controle de tinta.</span><span class="sxs-lookup"><span data-stu-id="32818-112">You should explicitly change the threading model to single-thread apartment (STA) before creating an ink control.</span></span> <span data-ttu-id="32818-113">Isso faz com que o controle seja criado no thread principal.</span><span class="sxs-lookup"><span data-stu-id="32818-113">This causes the control to be created on the main thread.</span></span> <span data-ttu-id="32818-114">Você pode usar o seguinte código C++ gerenciado para definir explicitamente o modelo de Threading.</span><span class="sxs-lookup"><span data-stu-id="32818-114">You can use the following Managed C++ code to explicitly set the threading model.</span></span>


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



<span data-ttu-id="32818-115">Você pode usar o código a seguir para fazer a mesma coisa em C \# .</span><span class="sxs-lookup"><span data-stu-id="32818-115">You can use the following code to do the same thing in C\#.</span></span>


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



<span data-ttu-id="32818-116">Em código gerenciado, para evitar um vazamento de memória, você deve chamar explicitamente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) em qualquer controle do Tablet PC ao qual um manipulador de eventos tenha sido anexado antes que o controle saia do escopo.</span><span class="sxs-lookup"><span data-stu-id="32818-116">In managed code, to avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC control to which an event handler has been attached before the control goes out of scope.</span></span>

<span data-ttu-id="32818-117">As seções a seguir descrevem os controles de tinta e o uso de controles de tinta em aplicativos:</span><span class="sxs-lookup"><span data-stu-id="32818-117">The following sections describe ink controls and the use of ink controls in applications:</span></span>

-   [<span data-ttu-id="32818-118">Adicionando controles de tinta a um projeto</span><span class="sxs-lookup"><span data-stu-id="32818-118">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
-   [<span data-ttu-id="32818-119">Controle InkEdit</span><span class="sxs-lookup"><span data-stu-id="32818-119">InkEdit Control</span></span>](inkedit-control.md)
-   [<span data-ttu-id="32818-120">Controle InkPicture</span><span class="sxs-lookup"><span data-stu-id="32818-120">InkPicture Control</span></span>](inkpicture-control.md)

 

 
