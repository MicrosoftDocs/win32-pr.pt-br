---
title: Propriedade da ajuda
description: A propriedade Help fornece informações que dizem ao usuário sobre a função de um objeto.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292120"
---
# <a name="help-property"></a><span data-ttu-id="1e050-103">Propriedade da ajuda</span><span class="sxs-lookup"><span data-stu-id="1e050-103">Help Property</span></span>

<span data-ttu-id="1e050-104">A propriedade **Help** fornece informações que dizem ao usuário sobre a função de um objeto.</span><span class="sxs-lookup"><span data-stu-id="1e050-104">The **Help** property provides information that tells the user about the function of an object.</span></span>

<span data-ttu-id="1e050-105">A propriedade **Help** é recuperada chamando [**IAccessible:: get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span><span class="sxs-lookup"><span data-stu-id="1e050-105">The **Help** property is retrieved by calling [**IAccessible::get\_accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span></span>

<span data-ttu-id="1e050-106">Essa propriedade contém informações de estilo de balão (conforme encontradas em dicas de ferramenta) que são usadas para descrever o que o objeto faz ou como usá-lo.</span><span class="sxs-lookup"><span data-stu-id="1e050-106">This property contains balloon-style information (as found in ToolTips) that is used either to describe what the object does or how to use it.</span></span> <span data-ttu-id="1e050-107">Por exemplo, a propriedade da **ajuda** para um botão da barra de ferramentas que mostra uma impressora pode fornecer o seguinte texto: "imprime o documento atual".</span><span class="sxs-lookup"><span data-stu-id="1e050-107">For example, the **Help** property for a toolbar button that shows a printer might provide the following text: "Prints the current document."</span></span>

<span data-ttu-id="1e050-108">O texto da propriedade da **ajuda** não precisa ser exclusivo na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e050-108">The text for the **Help** property does not have to be unique within the user interface.</span></span>

## <a name="when-to-support-the-help-property"></a><span data-ttu-id="1e050-109">Quando dar suporte à propriedade Help</span><span class="sxs-lookup"><span data-stu-id="1e050-109">When to Support the Help Property</span></span>

<span data-ttu-id="1e050-110">Os servidores não oferecerão suporte à propriedade de **ajuda** se outras propriedades fornecerem informações suficientes sobre a finalidade do objeto e as ações que o objeto executa.</span><span class="sxs-lookup"><span data-stu-id="1e050-110">Servers do not support the **Help** property if other properties provide sufficient information about the object's purpose and the actions the object performs.</span></span> <span data-ttu-id="1e050-111">Os objetos acessíveis que expõem os controles fornecidos pelo sistema não oferecem suporte à propriedade da **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="1e050-111">Accessible objects that expose system-provided controls do not support the **Help** property.</span></span>

 

 




