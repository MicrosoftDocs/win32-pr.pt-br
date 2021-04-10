---
description: Para usar a segurança baseada em função em seu aplicativo COM+, primeiro você deve habilitar a verificação de autorização baseada em função para o aplicativo.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Habilitando a verificação de autorização de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010230"
---
# <a name="enabling-role-based-authorization-checking"></a><span data-ttu-id="956fb-103">Habilitando a verificação de autorização de Role-Based</span><span class="sxs-lookup"><span data-stu-id="956fb-103">Enabling Role-Based Authorization Checking</span></span>

<span data-ttu-id="956fb-104">Para usar a segurança baseada em função em seu aplicativo COM+, primeiro você deve habilitar a verificação de autorização baseada em função para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="956fb-104">To use role-based security in your COM+ application, you must first enable role-based authorization checking for the application.</span></span> <span data-ttu-id="956fb-105">Isso garante que os usuários que estão acessando o aplicativo sejam verificados para a função à qual pertencem antes que estejam autorizados a fazer qualquer coisa no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="956fb-105">This ensures that users who are accessing the application are checked for the role they belong to before they are authorized to do anything in the application.</span></span> <span data-ttu-id="956fb-106">Se a verificação de autorização baseada em função não estiver habilitada, a segurança baseada em função para o aplicativo não será usada.</span><span class="sxs-lookup"><span data-stu-id="956fb-106">If role-based authorization checking is not enabled, role-based security for the application is not used.</span></span>

<span data-ttu-id="956fb-107">**Para habilitar a verificação de autorização baseada em função**</span><span class="sxs-lookup"><span data-stu-id="956fb-107">**To enable role-based authorization checking**</span></span>

1.  <span data-ttu-id="956fb-108">Clique com o botão direito do mouse no aplicativo COM+ para o qual você está habilitando a verificação de autorização baseada em função e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="956fb-108">Right-click the COM+ application for which you are enabling role-based authorization checking, and then click **Properties**.</span></span>

2.  <span data-ttu-id="956fb-109">Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="956fb-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="956fb-110">Em **autorização**, marque a caixa de seleção **impor verificações de acesso para este aplicativo** ; desmarcar a caixa de seleção significa que a segurança baseada em função não é usada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="956fb-110">Under **Authorization**, select the **Enforce access checks for this application** check box; clearing the check box means that role-based security is not used for the application.</span></span>

4.  <span data-ttu-id="956fb-111">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="956fb-111">Click **OK**.</span></span>

<span data-ttu-id="956fb-112">A configuração de autorização selecionada entrará em vigor na próxima vez em que o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="956fb-112">The selected authorization setting takes effect the next time the application is started.</span></span>

 

 



