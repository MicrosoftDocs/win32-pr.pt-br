---
title: Criando scripts de objetos COM em aplicativos personalizados
description: Criando scripts de objetos COM em aplicativos personalizados
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159702"
---
# <a name="scripting-com-objects-in-custom-applications"></a><span data-ttu-id="a010e-103">Criando scripts de objetos COM em aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="a010e-103">Scripting COM Objects in Custom Applications</span></span>

<span data-ttu-id="a010e-104">A Microsoft fornece vários ambientes para criar scripts de objetos COM: Active Server páginas, Windows Script Host e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a010e-104">Microsoft provides several environments for scripting COM objects: Active Server Pages, Windows Script Host, and so on.</span></span> <span data-ttu-id="a010e-105">ISVs (fornecedores independentes de software) também podem licenciar os mecanismos de script da Microsoft para uso em seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a010e-105">Independent software vendors (ISVs) can also license Microsoft scripting engines for use in their applications.</span></span> <span data-ttu-id="a010e-106">Por exemplo, um ISV que cria um processador de texto pode querer adicionar uma linguagem de macro ao aplicativo para que os usuários pudessem automatizar tarefas simples.</span><span class="sxs-lookup"><span data-stu-id="a010e-106">For example, an ISV creating a word processor might want to add a macro language to the application so users could automate simple tasks.</span></span> <span data-ttu-id="a010e-107">Ao licenciar um mecanismo de script, o ISV pode usar uma linguagem como VBScript ou JScript como linguagem de macro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a010e-107">By licensing a scripting engine, the ISV can use a language such as VBScript or JScript as the application's macro language.</span></span>

<span data-ttu-id="a010e-108">Além de licenciar os mecanismos de script VBScript e JScript, os ISVs podem gravar seus próprios mecanismos de script do ActiveX.</span><span class="sxs-lookup"><span data-stu-id="a010e-108">In addition to licensing VBScript and JScript scripting engines, ISVs can write their own ActiveX scripting engines.</span></span> <span data-ttu-id="a010e-109">Esses mecanismos de script podem então ser conectados a qualquer ambiente de host que dê suporte ao padrão do mecanismo de script do ActiveX.</span><span class="sxs-lookup"><span data-stu-id="a010e-109">These scripting engines can then be plugged into any host environment that supports the ActiveX scripting engine standard.</span></span> <span data-ttu-id="a010e-110">Por exemplo, um ISV pode escrever um mecanismo de script PerlScript e instalá-lo em um servidor ASP, permitindo assim que o servidor ASP processe scripts PerlScript.</span><span class="sxs-lookup"><span data-stu-id="a010e-110">For example, an ISV might write a PerlScript scripting engine and install it on an ASP server, thus enabling the ASP server to process PerlScript scripts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a010e-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a010e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a010e-112">Criando scripts com objetos COM</span><span class="sxs-lookup"><span data-stu-id="a010e-112">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




