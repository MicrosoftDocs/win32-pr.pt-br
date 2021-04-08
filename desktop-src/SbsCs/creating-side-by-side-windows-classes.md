---
description: Os contextos de aplicativo podem ser usados para criar classes lado a lado do Windows.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Criando classes lado a lado do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828841"
---
# <a name="creating-side-by-side-windows-classes"></a><span data-ttu-id="29f49-103">Criando classes lado a lado do Windows</span><span class="sxs-lookup"><span data-stu-id="29f49-103">Creating Side-By-Side Windows Classes</span></span>

<span data-ttu-id="29f49-104">Os contextos de aplicativo podem ser usados para criar classes lado a lado do Windows.</span><span class="sxs-lookup"><span data-stu-id="29f49-104">Application contexts can be used to create side-by-side Windows classes.</span></span> <span data-ttu-id="29f49-105">Usando classes lado a lado do Windows, seu aplicativo pode ter versões diferentes de uma classe ativa ao mesmo tempo em uma janela pai do solitário.</span><span class="sxs-lookup"><span data-stu-id="29f49-105">By using side-by-side Windows classes, your application can have different versions of a class active at the same time in a lone parent window.</span></span> <span data-ttu-id="29f49-106">Para criar uma classe lado a lado do Windows, seu aplicativo deve ativar um contexto de ativação antes de chamar [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para obter um identificador para a nova janela.</span><span class="sxs-lookup"><span data-stu-id="29f49-106">To create a side-by-side Windows class, your application must activate an activation context before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to obtain a handle to the new window.</span></span>

<span data-ttu-id="29f49-107">Por exemplo, os controles comuns do Windows versão 5,82 e a versão 6,0 tinham um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="29f49-107">For example, Windows Common Controls version 5.82 and version 6.0 both had an Edit control.</span></span> <span data-ttu-id="29f49-108">O padrão do Windows é usar o controle de edição da versão 5,82.</span><span class="sxs-lookup"><span data-stu-id="29f49-108">Windows defaults to using the version 5.82 Edit control.</span></span> <span data-ttu-id="29f49-109">Para obter uma janela lado a lado que tem o controle de edição da versão 6,0, antes de chamar [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) como de costume, seu aplicativo pode referenciar um assembly que expõe classes de janela nomeadas e, em seguida, ativar o contexto de ativação que faz referência aos controles da versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="29f49-109">To obtain a side-by-side window that has the version 6.0 Edit control, before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) as usual, your application can reference an assembly that exposes named window classes and then activate the activation context that references the version 6.0 controls.</span></span>

 

 
