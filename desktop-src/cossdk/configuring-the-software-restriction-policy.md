---
description: Configurando a política de restrição de software
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Configurando a política de restrição de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010265"
---
# <a name="configuring-the-software-restriction-policy"></a><span data-ttu-id="1ac78-103">Configurando a política de restrição de software</span><span class="sxs-lookup"><span data-stu-id="1ac78-103">Configuring the Software Restriction Policy</span></span>

<span data-ttu-id="1ac78-104">Quando você define explicitamente os níveis de confiança da diretiva de restrição de software de um aplicativo do COM+, você está substituindo as configurações padrão de todo o grupo.</span><span class="sxs-lookup"><span data-stu-id="1ac78-104">When you explicitly set the software restriction policy trust levels of a COM+ application, you are overriding the default systemwide settings.</span></span> <span data-ttu-id="1ac78-105">Isso geralmente é necessário para aplicativos de servidor COM+ porque o nível de confiança do todo o grupo é definido como o mesmo para todos os aplicativos de servidor (porque todos eles são executados no mesmo arquivo, dllhost.exe).</span><span class="sxs-lookup"><span data-stu-id="1ac78-105">This is often necessary for COM+ server applications because the systemwide trust level is set the same for all server applications (because they all run in the same file, dllhost.exe).</span></span> <span data-ttu-id="1ac78-106">No entanto, quando você define o nível de confiança da diretiva de restrição de software de um aplicativo de biblioteca COM+, está afetando a configuração de todo o grupo para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1ac78-106">However, when you set the software restriction policy trust level of a COM+ library application, you are affecting the systemwide configuration for that application.</span></span> <span data-ttu-id="1ac78-107">Para obter uma discussão sobre como usar a política de restrição de software no COM+, consulte [usando a política de restrição de software no com+](using-the-software-restriction-policy-in-com-.md).</span><span class="sxs-lookup"><span data-stu-id="1ac78-107">For a discussion of how to use the software restriction policy in COM+, see [Using the Software Restriction Policy in COM+](using-the-software-restriction-policy-in-com-.md).</span></span>

<span data-ttu-id="1ac78-108">**Para definir a diretiva de restrição de software**</span><span class="sxs-lookup"><span data-stu-id="1ac78-108">**To set the software restriction policy**</span></span>

1.  <span data-ttu-id="1ac78-109">Clique com o botão direito do mouse no aplicativo COM+ para o qual você está definindo a diretiva de restrição de software e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="1ac78-109">Right-click the COM+ application for which you are setting the software restriction policy, and then click **Properties**.</span></span>

2.  <span data-ttu-id="1ac78-110">Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="1ac78-110">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="1ac78-111">Em **diretiva de restrição de software**, marque a caixa de seleção **aplicar política de restrição de software** ; Isso permite que você defina o nível de confiança.</span><span class="sxs-lookup"><span data-stu-id="1ac78-111">Under **Software Restriction Policy**, select the **Apply software restriction policy** check box; this enables you to set the trust level.</span></span> <span data-ttu-id="1ac78-112">Desmarcar a caixa de seleção fará com que o COM+ use a configuração em todo o âmbito da diretiva de restrição de software para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1ac78-112">Clearing the check box will cause COM+ to use the systemwide configuration of the software restriction policy for the application.</span></span> <span data-ttu-id="1ac78-113">Essa caixa de seleção corresponde à propriedade SRPEnabled da coleção de [**aplicativos**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="1ac78-113">This check box corresponds to the SRPEnabled property of the [**Applications**](applications.md) collection.</span></span>

4.  <span data-ttu-id="1ac78-114">Na caixa **nível de restrição** , selecione o nível apropriado.</span><span class="sxs-lookup"><span data-stu-id="1ac78-114">In the **Restriction Level** box, select the appropriate level.</span></span> <span data-ttu-id="1ac78-115">Essa caixa suspensa corresponde à propriedade SRPTrustLevel da coleção de [**aplicativos**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="1ac78-115">This drop-down box corresponds to the SRPTrustLevel property of the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="1ac78-116">Os níveis são os seguintes, ordenados do menos para o mais confiável:</span><span class="sxs-lookup"><span data-stu-id="1ac78-116">The levels are as follows, ordered from least to most trusted:</span></span>

    -   <span data-ttu-id="1ac78-117">Não **permitido**.</span><span class="sxs-lookup"><span data-stu-id="1ac78-117">**Disallowed**.</span></span> <span data-ttu-id="1ac78-118">O aplicativo não é permitido de usar os privilégios totais do usuário.</span><span class="sxs-lookup"><span data-stu-id="1ac78-118">The application is disallowed from using the full privileges of the user.</span></span> <span data-ttu-id="1ac78-119">Os componentes com qualquer nível de confiança podem ser carregados nele.</span><span class="sxs-lookup"><span data-stu-id="1ac78-119">Components with any trust level can be loaded into it.</span></span>
    -   <span data-ttu-id="1ac78-120">**Irrestrito**.</span><span class="sxs-lookup"><span data-stu-id="1ac78-120">**Unrestricted**.</span></span> <span data-ttu-id="1ac78-121">O aplicativo tem acesso irrestrito aos privilégios do usuário.</span><span class="sxs-lookup"><span data-stu-id="1ac78-121">The application has unrestricted access to the user's privileges.</span></span> <span data-ttu-id="1ac78-122">Somente os componentes com um nível de confiança irrestrito podem ser carregados nele.</span><span class="sxs-lookup"><span data-stu-id="1ac78-122">Only components with an Unrestricted trust level can be loaded into it.</span></span>

5.  <span data-ttu-id="1ac78-123">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ac78-123">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ac78-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ac78-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ac78-125">Configurando a segurança do Role-Based</span><span class="sxs-lookup"><span data-stu-id="1ac78-125">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="1ac78-126">Habilitando a autenticação para um aplicativo de biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ac78-126">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="1ac78-127">Definindo um nível de autenticação para um aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="1ac78-127">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[<span data-ttu-id="1ac78-128">Definindo um nível de representação</span><span class="sxs-lookup"><span data-stu-id="1ac78-128">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



