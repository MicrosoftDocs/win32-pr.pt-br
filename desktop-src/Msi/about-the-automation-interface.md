---
description: Um objeto instalador deve ser criado inicialmente para carregar o suporte de automação necessário para acessar os componentes do instalador por meio de COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Sobre a interface de automação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169220"
---
# <a name="about-the-automation-interface"></a><span data-ttu-id="adfad-103">Sobre a interface de automação</span><span class="sxs-lookup"><span data-stu-id="adfad-103">About the Automation Interface</span></span>

<span data-ttu-id="adfad-104">Um [**objeto instalador**](installer-object.md) deve ser criado inicialmente para carregar o suporte de automação necessário para acessar os componentes do instalador por meio de com.</span><span class="sxs-lookup"><span data-stu-id="adfad-104">An [**Installer object**](installer-object.md) must be created initially to load the automation support required to access the installer components through COM.</span></span> <span data-ttu-id="adfad-105">Esse objeto fornece wrappers para criar os objetos de nível superior e acessar seus métodos.</span><span class="sxs-lookup"><span data-stu-id="adfad-105">This object provides wrappers to create the top-level objects and access their methods.</span></span> <span data-ttu-id="adfad-106">Esses wrappers simplesmente fornecem conversões de parâmetro para expor as funções do instalador de uma maneira consistente com o Microsoft Visual Basic sem alterar o comportamento dos métodos.</span><span class="sxs-lookup"><span data-stu-id="adfad-106">These wrappers simply provide parameter translations to expose the installer functions in a manner consistent with Microsoft Visual Basic without changing the behavior of the methods.</span></span>

<span data-ttu-id="adfad-107">Sempre que possível, um par de métodos get e set do C++ é exposto a Visual Basic como uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="adfad-107">Whenever possible, a pair of Get and Set C++ methods are exposed to Visual Basic as a single property.</span></span> <span data-ttu-id="adfad-108">Em alguns casos, os métodos do C++ que levam um argumento de índice são expostos como uma propriedade indexada.</span><span class="sxs-lookup"><span data-stu-id="adfad-108">In some cases C++ methods taking an index argument are exposed as an indexed property.</span></span> <span data-ttu-id="adfad-109">Muitos métodos C++ retornam o resultado por meio de um parâmetro porque o valor de retorno é usado para o retorno de erro.</span><span class="sxs-lookup"><span data-stu-id="adfad-109">Many C++ methods return the result through a parameter because the return value is used for the error return.</span></span> <span data-ttu-id="adfad-110">No entanto, no Visual Basic, os erros são tratados por um mecanismo separado e o resultado é sempre passado no valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="adfad-110">However, in Visual Basic, errors are handled by a separate mechanism, and the result is always passed in the return value.</span></span>

<span data-ttu-id="adfad-111">Para obter informações sobre como usar a automação e criar o objeto do instalador, consulte [usando a interface de automação](using-the-automation-interface.md).</span><span class="sxs-lookup"><span data-stu-id="adfad-111">For information about using automation and creating the Installer object, see [Using the Automation Interface](using-the-automation-interface.md).</span></span>

<span data-ttu-id="adfad-112">Para obter material de referência para os objetos Windows Installer, consulte [referência da interface de automação](automation-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="adfad-112">For reference material for the Windows Installer objects, see [Automation Interface Reference](automation-interface-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="adfad-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="adfad-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adfad-114">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="adfad-114">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



