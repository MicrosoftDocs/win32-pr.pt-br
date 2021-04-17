---
title: Propriedade de função
description: A propriedade Role descreve o elemento de interface do usuário de um objeto. Todos os objetos dão suporte à propriedade Role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798394"
---
# <a name="role-property"></a><span data-ttu-id="00402-104">Propriedade de função</span><span class="sxs-lookup"><span data-stu-id="00402-104">Role Property</span></span>

<span data-ttu-id="00402-105">A propriedade **role** descreve o elemento de interface do usuário de um objeto.</span><span class="sxs-lookup"><span data-stu-id="00402-105">The **Role** property describes an object's user interface element.</span></span> <span data-ttu-id="00402-106">Todos os objetos dão suporte à propriedade **role** .</span><span class="sxs-lookup"><span data-stu-id="00402-106">All objects support the **Role** property.</span></span>

<span data-ttu-id="00402-107">Em muitos casos, a função do objeto é óbvia.</span><span class="sxs-lookup"><span data-stu-id="00402-107">In many cases, the object's role is obvious.</span></span> <span data-ttu-id="00402-108">Por exemplo, o Windows tem a função de [**\_ \_ janela do sistema de função**](object-roles.md) e os botões de push têm a função de [**\_ \_ pressão do sistema de função**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="00402-108">For example, windows have the [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) role and push buttons have the [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md) role.</span></span>

<span data-ttu-id="00402-109">A propriedade **role** é recuperada chamando [**IAccessible:: get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span><span class="sxs-lookup"><span data-stu-id="00402-109">The **Role** property is retrieved by calling [**IAccessible::get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span></span>

## <a name="identifying-an-objects-role"></a><span data-ttu-id="00402-110">Identificando a função de um objeto</span><span class="sxs-lookup"><span data-stu-id="00402-110">Identifying an Object's Role</span></span>

<span data-ttu-id="00402-111">O Microsoft Acessibilidade Ativa fornece [constantes de função](object-roles.md), definidas em OleAcc. h, que identificam funções de objeto comuns.</span><span class="sxs-lookup"><span data-stu-id="00402-111">Microsoft Active Accessibility provides [role constants](object-roles.md), defined in oleacc.h, that identify common object roles.</span></span> <span data-ttu-id="00402-112">É recomendável que os desenvolvedores de servidor usem esses valores de função predefinidos.</span><span class="sxs-lookup"><span data-stu-id="00402-112">It is recommended that server developers use these predefined role values.</span></span> <span data-ttu-id="00402-113">Se uma constante de função predefinida for retornada, os clientes usarão a função [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) para recuperar uma cadeia de caracteres localizada que descreve a função.</span><span class="sxs-lookup"><span data-stu-id="00402-113">If a predefined role constant is returned, clients use the [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) function to retrieve a localized string that describes the role.</span></span>

<span data-ttu-id="00402-114">Para controles de animação, como o controle de animação exibido ao copiar arquivos, use a [**\_ \_ animação do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="00402-114">For animation controls, such as the animation control displayed when copying files, use [**ROLE\_SYSTEM\_ANIMATION**](object-roles.md).</span></span> <span data-ttu-id="00402-115">Os gráficos que são ocasionalmente animados são descritos como [**\_ \_ elemento gráfico do sistema de funções**](object-roles.md) com a propriedade [**State**](state-property.md) definida como [**estado \_ sistema \_ animado**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="00402-115">Graphics that are occasionally animated are described as [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md) with the [**State**](state-property.md) property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md).</span></span>

<span data-ttu-id="00402-116">Observe que algumas funções não são fáceis de descrever.</span><span class="sxs-lookup"><span data-stu-id="00402-116">Note that some roles are not easy to describe.</span></span> <span data-ttu-id="00402-117">Por exemplo, a exibição de ícones grandes de uma pasta permite a disposição arbitrária de ícones, de modo que sua função poderia ser descrita como [**\_ \_ agrupamento do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="00402-117">For example, a folder's large-icon view allows arbitrary arrangement of icons, so its role could be described as [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span> <span data-ttu-id="00402-118">Ou, um controle que fornece itens em linhas e colunas fixas pode ter a função de [**\_ \_ tabela do sistema de função**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="00402-118">Or, a control that provides items in fixed rows and columns could have the [**ROLE\_SYSTEM\_TABLE**](object-roles.md) role.</span></span> <span data-ttu-id="00402-119">Como uma função é usada para comunicar o modelo de uso para um usuário final, é importante usar a função apropriada.</span><span class="sxs-lookup"><span data-stu-id="00402-119">Since a role is used to communicate the use model to an end user, it is important to use the appropriate role.</span></span> <span data-ttu-id="00402-120">Por exemplo, se o seu controle atua como um botão, use a ação do [**sistema de função \_ \_**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="00402-120">For example, if your control acts like a button, then use [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md).</span></span>

 

 




