---
description: Habilitando verificações de acesso no nível do componente
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Habilitando verificações de acesso no nível do componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797609"
---
# <a name="enabling-access-checks-at-the-component-level"></a><span data-ttu-id="9cc61-103">Habilitando verificações de acesso no nível do componente</span><span class="sxs-lookup"><span data-stu-id="9cc61-103">Enabling Access Checks at the Component Level</span></span>

<span data-ttu-id="9cc61-104">Se seu aplicativo inclui um componente que não precisa de verificações de segurança, você pode optar por desabilitar as verificações de função para esse componente para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="9cc61-104">If your application includes a component that does not need security checks, you might decide to disable role checks for that component to improve performance.</span></span> <span data-ttu-id="9cc61-105">Ou durante a depuração, pode ser útil desabilitar a segurança para que você possa se concentrar em outros aspectos da funcionalidade do programa.</span><span class="sxs-lookup"><span data-stu-id="9cc61-105">Or when debugging, it might be helpful to disable security so that you can concentrate on other aspects of program functionality.</span></span>

<span data-ttu-id="9cc61-106">Por padrão, quando você instala um componente, as verificações de acesso no nível de componente são habilitadas.</span><span class="sxs-lookup"><span data-stu-id="9cc61-106">By default, when you install a component, component-level access checks are enabled.</span></span> <span data-ttu-id="9cc61-107">No entanto, isso só terá efeito quando as [verificações de acesso no nível do aplicativo](enabling-access-checks-for-an-application.md) estiverem habilitadas e quando o nível de [segurança](setting-a-security-level-for-access-checks.md) estiver definido para **executar verificações de acesso no nível do processo e do componente**.</span><span class="sxs-lookup"><span data-stu-id="9cc61-107">However, this takes effect only when [application-level access checks](enabling-access-checks-for-an-application.md) are enabled and when the [security level](setting-a-security-level-for-access-checks.md) is set to **Perform access checks at the process and component level**.</span></span>

<span data-ttu-id="9cc61-108">**Para habilitar ou desabilitar verificações de acesso no nível do componente**</span><span class="sxs-lookup"><span data-stu-id="9cc61-108">**To enable or disable access checks at the component level**</span></span>

1.  <span data-ttu-id="9cc61-109">Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém o componente para o qual você deseja desabilitar (ou habilitar) as verificações de função.</span><span class="sxs-lookup"><span data-stu-id="9cc61-109">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the component for which you want to disable (or enable) role checks.</span></span> <span data-ttu-id="9cc61-110">Expanda a exibição na árvore para exibir os componentes na pasta **componentes** .</span><span class="sxs-lookup"><span data-stu-id="9cc61-110">Expand the view in the tree to view the components in the **Components** folder.</span></span>

2.  <span data-ttu-id="9cc61-111">Clique com o botão direito do mouse no componente para o qual você deseja habilitar as verificações de função e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="9cc61-111">Right-click the component for which you want to enable role checks, and then click **Properties**.</span></span>

3.  <span data-ttu-id="9cc61-112">Na caixa de diálogo Propriedades do componente, clique na guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="9cc61-112">In the component properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="9cc61-113">Selecione **impor verificações de acesso no nível do componente** para impor verificações de nível de componente.</span><span class="sxs-lookup"><span data-stu-id="9cc61-113">Select **Enforce component level access checks** to enforce component-level checks.</span></span>

5.  <span data-ttu-id="9cc61-114">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="9cc61-114">Click **OK**.</span></span>

<span data-ttu-id="9cc61-115">A nova configuração entrará em vigor na próxima vez em que o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="9cc61-115">The new setting will take effect the next time the application is started.</span></span>

> [!Note]  
> <span data-ttu-id="9cc61-116">A partir do Windows Server 2003, as verificações de acesso no nível de componente são desabilitadas por padrão durante a criação de um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="9cc61-116">As of Windows Server 2003, component-level access checks are disabled by default when creating a COM+ application.</span></span> <span data-ttu-id="9cc61-117">As verificações de acesso são habilitadas por padrão no nível do aplicativo e desabilitadas por padrão no nível do componente.</span><span class="sxs-lookup"><span data-stu-id="9cc61-117">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="9cc61-118">Anteriormente, as verificações de acesso foram desabilitadas por padrão no nível do aplicativo e habilitadas por padrão no nível do componente.</span><span class="sxs-lookup"><span data-stu-id="9cc61-118">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9cc61-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9cc61-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cc61-120">Atribuindo funções a componentes, interfaces ou métodos</span><span class="sxs-lookup"><span data-stu-id="9cc61-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="9cc61-121">Configurando a segurança do Role-Based</span><span class="sxs-lookup"><span data-stu-id="9cc61-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="9cc61-122">Definindo funções para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="9cc61-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="9cc61-123">Habilitando verificações de acesso para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="9cc61-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="9cc61-124">Configurando um nível de segurança para verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="9cc61-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



