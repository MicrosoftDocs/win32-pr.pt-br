---
title: Propriedade DefaultAction
description: A propriedade DefaultAction de um objeto descreve o método principal de manipulação do objeto do ponto de vista do usuário. A propriedade DefaultAction de um objeto deve ser um verbo ou uma frase verbal curta.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291901"
---
# <a name="defaultaction-property"></a><span data-ttu-id="86cf2-104">Propriedade DefaultAction</span><span class="sxs-lookup"><span data-stu-id="86cf2-104">DefaultAction Property</span></span>

<span data-ttu-id="86cf2-105">A propriedade **DefaultAction** de um objeto descreve o método principal de manipulação do objeto do ponto de vista do usuário.</span><span class="sxs-lookup"><span data-stu-id="86cf2-105">An object's **DefaultAction** property describes the object's primary method of manipulation from the user's viewpoint.</span></span> <span data-ttu-id="86cf2-106">A propriedade **DefaultAction** de um objeto deve ser um verbo ou uma frase verbal curta.</span><span class="sxs-lookup"><span data-stu-id="86cf2-106">An object's **DefaultAction** property should be a verb or a short verb phrase.</span></span>

<span data-ttu-id="86cf2-107">A propriedade **DefaultAction** é recuperada chamando [**IAccessible:: get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span><span class="sxs-lookup"><span data-stu-id="86cf2-107">The **DefaultAction** property is retrieved by calling [**IAccessible::get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span></span>

<span data-ttu-id="86cf2-108">Para executar a ação padrão de um objeto, os clientes chamam [**IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span><span class="sxs-lookup"><span data-stu-id="86cf2-108">To perform an object's default action, clients call [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span></span>

<span data-ttu-id="86cf2-109">Nem todos os objetos têm ações padrão e alguns objetos têm uma ação padrão relacionada à sua propriedade [**Value**](value-property.md) , como nos exemplos a seguir:</span><span class="sxs-lookup"><span data-stu-id="86cf2-109">Not all objects have default actions, and some objects have a default action that is related to its [**Value**](value-property.md) property, such as in the following examples:</span></span>

-   <span data-ttu-id="86cf2-110">Uma caixa de seleção selecionada tem uma ação padrão de "desmarcar" e um valor de "marcado".</span><span class="sxs-lookup"><span data-stu-id="86cf2-110">A selected check box has a default action of "Uncheck" and a value of "Checked."</span></span>
-   <span data-ttu-id="86cf2-111">Uma caixa de seleção desmarcada tem uma ação padrão de "verificar" e um valor de "desmarcado".</span><span class="sxs-lookup"><span data-stu-id="86cf2-111">A cleared check box has a default action of "Check" and a value of "Unchecked."</span></span>
-   <span data-ttu-id="86cf2-112">Um botão chamado "Print" tem uma ação padrão de "Press", sem valor.</span><span class="sxs-lookup"><span data-stu-id="86cf2-112">A button labeled "Print" has a default action of "Press," with no value.</span></span>
-   <span data-ttu-id="86cf2-113">Um controle de texto estático ou um controle de edição que mostra "impressora" não tem nenhuma ação padrão, mas tem um valor de "impressora".</span><span class="sxs-lookup"><span data-stu-id="86cf2-113">A static text control or an edit control that shows "Printer" has no default action, but has a value of "Printer."</span></span>

 

 




