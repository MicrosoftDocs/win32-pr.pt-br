---
title: Propriedade Description (recursos de acessibilidade do Windows)
description: A propriedade Descrição de um objeto fornece uma descrição textual sobre a aparência visual de um objeto.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454567"
---
# <a name="description-property-windows-accessibility-features"></a><span data-ttu-id="a860e-103">Propriedade Description (recursos de acessibilidade do Windows)</span><span class="sxs-lookup"><span data-stu-id="a860e-103">Description Property (Windows Accessibility features)</span></span>

> [!Note]  
> <span data-ttu-id="a860e-104">A propriedade **Description** geralmente é usada incorretamente e não é suportada pela automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a860e-104">The **Description** property is often used incorrectly and is not supported by Microsoft UI Automation.</span></span> <span data-ttu-id="a860e-105">Os desenvolvedores do Microsoft Acessibilidade Ativa Server não devem usar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="a860e-105">Microsoft Active Accessibility server developers should not use this property.</span></span> <span data-ttu-id="a860e-106">Se mais informações forem necessárias para cenários de acessibilidade e automação, use as propriedades com suporte pelos elementos de automação da interface do usuário e padrões de controle.</span><span class="sxs-lookup"><span data-stu-id="a860e-106">If more information is needed for accessibility and automation scenarios, use the properties supported by UI Automation elements and control patterns.</span></span>

 

<span data-ttu-id="a860e-107">A propriedade **Descrição** de um objeto fornece uma descrição textual sobre a aparência visual de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a860e-107">An object's **Description** property provides a textual description about an object's visual appearance.</span></span> <span data-ttu-id="a860e-108">A descrição é usada principalmente para fornecer um contexto maior para usuários com deficiência visual ou cegas, mas também é usada para pesquisa de contexto ou outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a860e-108">The description is primarily used to provide greater context for low-vision or blind users, but is also used for context searching or other applications.</span></span> <span data-ttu-id="a860e-109">Essa propriedade pode ajudar os usuários a entender um ícone ou a aparência visual geral.</span><span class="sxs-lookup"><span data-stu-id="a860e-109">This property can help users understand an icon or the overall visual appearance.</span></span>

<span data-ttu-id="a860e-110">A propriedade **Description** é recuperada chamando [**IAccessible:: get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span><span class="sxs-lookup"><span data-stu-id="a860e-110">The **Description** property is retrieved by calling [**IAccessible::get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span></span>

## <a name="when-to-support-the-description-property"></a><span data-ttu-id="a860e-111">Quando dar suporte à propriedade Description</span><span class="sxs-lookup"><span data-stu-id="a860e-111">When to Support the Description Property</span></span>

<span data-ttu-id="a860e-112">Os servidores suportarão a propriedade **Descrição** se a descrição não for óbvia ou quando ela não for redundante com base nas propriedades [**nome**](name-property.md), [**função**](role-property.md), [**estado**](state-property.md)e [**valor**](value-property.md) do objeto.</span><span class="sxs-lookup"><span data-stu-id="a860e-112">Servers support the **Description** property if the description is not obvious, or when it is not redundant based on the object's [**Name**](name-property.md), [**Role**](role-property.md), [**State**](state-property.md), and [**Value**](value-property.md) properties.</span></span> <span data-ttu-id="a860e-113">Por exemplo, um botão rotulado como "OK" não precisará de informações adicionais, enquanto um botão que mostra uma imagem de um cacto faria.</span><span class="sxs-lookup"><span data-stu-id="a860e-113">For example, a button labeled "OK" would not need additional information, whereas a button that shows a picture of a cactus would.</span></span> <span data-ttu-id="a860e-114">As propriedades **Name**, **role** e [**Help**](help-property.md) para tal botão descrevem sua finalidade, mas a propriedade **Description** transmite informações que são menos tangíveis; por exemplo, "esse botão mostra uma imagem de um cacto".</span><span class="sxs-lookup"><span data-stu-id="a860e-114">The **Name**, **Role**, and [**Help**](help-property.md) properties for such a button describe its purpose, but the **Description** property conveys information that is less tangible; for example, "This button shows a picture of a cactus."</span></span>

<span data-ttu-id="a860e-115">Um Microsoft Acessibilidade Ativa Server pode adicionar suporte para automação da interface do usuário usando [anotação direta](direct-annotation.md), usando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) ou implementando o Microsoft acessibilidade ativa e a automação da interface do usuário lado a lado com ambas as implementações que manipulam a mensagem do [**WM \_ GetObject**](wm-getobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a860e-115">A Microsoft Active Accessibility server can add support for UI Automation by using [Direct Annotation](direct-annotation.md), using the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, or by implementing Microsoft Active Accessibility and UI Automation side-by-side with both implementations handling the [**WM\_GETOBJECT**](wm-getobject.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a860e-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a860e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a860e-117">Usando anotação direta</span><span class="sxs-lookup"><span data-stu-id="a860e-117">Using Direct Annotation</span></span>](using-direct-annotation.md)
</dt> <dt>

[<span data-ttu-id="a860e-118">A interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="a860e-118">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> </dl>

 

 




