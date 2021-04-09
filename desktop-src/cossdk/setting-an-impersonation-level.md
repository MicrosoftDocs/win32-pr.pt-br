---
description: Quando você define um nível de representação para um aplicativo, determina o grau de autoridade que o aplicativo concede a outros aplicativos para usar sua identidade quando ele os chama.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Definindo um nível de representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089303"
---
# <a name="setting-an-impersonation-level"></a><span data-ttu-id="314e5-103">Definindo um nível de representação</span><span class="sxs-lookup"><span data-stu-id="314e5-103">Setting an Impersonation Level</span></span>

<span data-ttu-id="314e5-104">Quando você define um nível de representação para um aplicativo, determina o grau de autoridade que o aplicativo concede a outros aplicativos para usar sua identidade quando ele os chama.</span><span class="sxs-lookup"><span data-stu-id="314e5-104">When you set an impersonation level for an application, you determine what degree of authority the application grants other applications to use its identity when it calls them.</span></span> <span data-ttu-id="314e5-105">Você pode definir isso somente para aplicativos de servidor COM+ — os aplicativos de biblioteca são executados sob a identidade do processo de hospedagem e usam o nível de representação que ele especifica.</span><span class="sxs-lookup"><span data-stu-id="314e5-105">You can set this only for COM+ server applications—library applications run under the identity of the hosting process and use the impersonation level that it specifies.</span></span> <span data-ttu-id="314e5-106">Para obter mais detalhes, consulte [níveis de representação](/windows/desktop/com/impersonation-levels).</span><span class="sxs-lookup"><span data-stu-id="314e5-106">For more detail, see [Impersonation Levels](/windows/desktop/com/impersonation-levels).</span></span>

<span data-ttu-id="314e5-107">**Para selecionar um nível de representação**</span><span class="sxs-lookup"><span data-stu-id="314e5-107">**To select an impersonation level**</span></span>

1.  <span data-ttu-id="314e5-108">Clique com o botão direito do mouse no aplicativo COM+ para o qual você está definindo a representação e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="314e5-108">Right-click the COM+ application for which you are setting impersonation, and then click **Properties**.</span></span>

2.  <span data-ttu-id="314e5-109">Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="314e5-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="314e5-110">Na caixa **nível de representação** , selecione o nível apropriado.</span><span class="sxs-lookup"><span data-stu-id="314e5-110">In the **Impersonation level** box, select the appropriate level.</span></span> <span data-ttu-id="314e5-111">Os níveis são os seguintes, ordenados da concessão de menos para a maior autoridade:</span><span class="sxs-lookup"><span data-stu-id="314e5-111">The levels are as follows, ordered from granting least to greatest authority:</span></span>

    -   <span data-ttu-id="314e5-112">**Anônimo**.</span><span class="sxs-lookup"><span data-stu-id="314e5-112">**Anonymous**.</span></span> <span data-ttu-id="314e5-113">O cliente é anônimo ao servidor.</span><span class="sxs-lookup"><span data-stu-id="314e5-113">The client is anonymous to the server.</span></span> <span data-ttu-id="314e5-114">O servidor pode representar o cliente, mas o token de representação (uma credencial local) não contém nenhuma informação sobre o cliente.</span><span class="sxs-lookup"><span data-stu-id="314e5-114">The server can impersonate the client, but the impersonation token (a local credential) does not contain any information about the client.</span></span>
    -   <span data-ttu-id="314e5-115">**Identificar**.</span><span class="sxs-lookup"><span data-stu-id="314e5-115">**Identify**.</span></span> <span data-ttu-id="314e5-116">O servidor pode obter a identidade do cliente e pode representar o cliente para fazer verificações de ACL.</span><span class="sxs-lookup"><span data-stu-id="314e5-116">The server can obtain the client's identity and can impersonate the client to do ACL checks.</span></span>
    -   <span data-ttu-id="314e5-117">**Representar**.</span><span class="sxs-lookup"><span data-stu-id="314e5-117">**Impersonate**.</span></span> <span data-ttu-id="314e5-118">O servidor pode representar o cliente enquanto atua em seu nome, embora com restrições.</span><span class="sxs-lookup"><span data-stu-id="314e5-118">The server can impersonate the client while acting on its behalf, although with restrictions.</span></span> <span data-ttu-id="314e5-119">O servidor pode acessar recursos no mesmo computador que o cliente.</span><span class="sxs-lookup"><span data-stu-id="314e5-119">The server can access resources on the same computer as the client.</span></span> <span data-ttu-id="314e5-120">Se o servidor estiver no mesmo computador que o cliente, ele poderá acessar os recursos de rede como o cliente.</span><span class="sxs-lookup"><span data-stu-id="314e5-120">If the server is on the same computer as the client, it can access network resources as the client.</span></span> <span data-ttu-id="314e5-121">Se o servidor estiver em um computador diferente do cliente, ele poderá acessar apenas os recursos que estão no mesmo computador que o servidor.</span><span class="sxs-lookup"><span data-stu-id="314e5-121">If the server is on a computer different from the client, it can access only resources that are on the same computer as the server.</span></span> <span data-ttu-id="314e5-122">Essa é a configuração padrão para aplicativos de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="314e5-122">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="314e5-123">**Delegar**.</span><span class="sxs-lookup"><span data-stu-id="314e5-123">**Delegate**.</span></span> <span data-ttu-id="314e5-124">O servidor pode representar o cliente ao atuar em seu nome, seja no mesmo computador que o cliente.</span><span class="sxs-lookup"><span data-stu-id="314e5-124">The server can impersonate the client while acting on its behalf, whether on the same computer as the client.</span></span> <span data-ttu-id="314e5-125">Durante a representação, as credenciais do cliente (ambas com local e aquelas com a validade da rede) podem ser passadas para qualquer número de computadores.</span><span class="sxs-lookup"><span data-stu-id="314e5-125">During impersonation, the client's credentials (both those with local and those with network validity) can be passed to any number of machines.</span></span>

4.  <span data-ttu-id="314e5-126">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="314e5-126">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="314e5-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="314e5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="314e5-128">Configurando a segurança do Role-Based</span><span class="sxs-lookup"><span data-stu-id="314e5-128">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="314e5-129">Configurando a política de restrição de software</span><span class="sxs-lookup"><span data-stu-id="314e5-129">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="314e5-130">Habilitando a autenticação para um aplicativo de biblioteca</span><span class="sxs-lookup"><span data-stu-id="314e5-130">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="314e5-131">Definindo um nível de autenticação para um aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="314e5-131">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
