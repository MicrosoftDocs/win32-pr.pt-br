---
description: Habilitando a autenticação para um aplicativo de biblioteca
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Habilitando a autenticação para um aplicativo de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788147"
---
# <a name="enabling-authentication-for-a-library-application"></a><span data-ttu-id="c0c25-103">Habilitando a autenticação para um aplicativo de biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0c25-103">Enabling Authentication for a Library Application</span></span>

<span data-ttu-id="c0c25-104">Como os aplicativos de biblioteca COM+ são hospedados por outros processos, seus requisitos de segurança podem ser diferentes dos aplicativos de servidor.</span><span class="sxs-lookup"><span data-stu-id="c0c25-104">Because COM+ library applications are hosted by other processes, their security requirements may be different from those of server applications.</span></span> <span data-ttu-id="c0c25-105">Se o aplicativo de biblioteca for hospedado por um navegador, talvez seja necessário receber retornos de chamada não autenticados.</span><span class="sxs-lookup"><span data-stu-id="c0c25-105">If the library application will be hosted by a browser, it might need to receive unauthenticated callbacks.</span></span>

<span data-ttu-id="c0c25-106">Para atender a essa necessidade, você pode desabilitar a autenticação para que o processo de hospedagem não execute verificações de segurança para os chamadores do aplicativo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c0c25-106">To address this need, you can disable authentication so that the hosting process does not perform security checks for callers of the library application.</span></span> <span data-ttu-id="c0c25-107">Quando você desabilita a autenticação, as chamadas para o aplicativo de biblioteca efetivamente não são autenticadas – todas as chamadas para ela serão realizadas com sucesso.</span><span class="sxs-lookup"><span data-stu-id="c0c25-107">When you disable authentication, calls to the library application effectively go unauthenticated—all calls to it will succeed.</span></span> <span data-ttu-id="c0c25-108">Para obter mais informações, consulte [segurança do aplicativo de biblioteca](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="c0c25-108">For more information, see [Library Application Security](library-application-security.md).</span></span>

<span data-ttu-id="c0c25-109">**Para habilitar (ou desabilitar) a autenticação para um aplicativo de biblioteca**</span><span class="sxs-lookup"><span data-stu-id="c0c25-109">**To enable (or disable) authentication for a library application**</span></span>

1.  <span data-ttu-id="c0c25-110">Clique com o botão direito do mouse no aplicativo COM+ para o qual você está habilitando ou desabilitando a autenticação e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="c0c25-110">Right-click the COM+ application for which you are enabling or disabling authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="c0c25-111">Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="c0c25-111">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="c0c25-112">Em **autenticação**, marque a caixa de seleção **habilitar autenticação** para habilitar a autenticação; desmarcar a caixa de seleção desativará a autenticação.</span><span class="sxs-lookup"><span data-stu-id="c0c25-112">Under **Authentication**, select the **Enable authentication** check box to enable authentication; clearing the check box will disable authentication.</span></span>

4.  <span data-ttu-id="c0c25-113">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0c25-113">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0c25-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0c25-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0c25-115">Definindo um nível de autenticação para um aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="c0c25-115">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



