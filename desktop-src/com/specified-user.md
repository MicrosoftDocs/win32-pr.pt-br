---
title: Usuário especificado
description: Usuário especificado
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105790626"
---
# <a name="specified-user"></a><span data-ttu-id="b5c39-103">Usuário especificado</span><span class="sxs-lookup"><span data-stu-id="b5c39-103">Specified User</span></span>

<span data-ttu-id="b5c39-104">A especificação de um usuário específico (e a senha do usuário) é a identidade preferida para servidores COM.</span><span class="sxs-lookup"><span data-stu-id="b5c39-104">Specifying a particular user (and the user's password) is the preferred identity for COM servers.</span></span> <span data-ttu-id="b5c39-105">A razão pela qual essa identidade é preferida é que ninguém precisa ser registrado no computador onde o servidor está sendo executado para que o servidor seja executado, e cada cliente se comunica com a mesma instância do servidor se o servidor registrar sua fábrica de classes como multiutilização.</span><span class="sxs-lookup"><span data-stu-id="b5c39-105">The reason this identity is preferred is that no one has to be logged on the machine where the server is running for the server to run, and every client talks to the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="b5c39-106">Se o servidor tiver uma GUI, você não deverá escolher essa identidade; Se você fizer isso, o usuário não poderá ver a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b5c39-106">If the server has a GUI, you should not choose this identity; if you do, the user will not be able to see the user interface.</span></span>

<span data-ttu-id="b5c39-107">Esse tipo de servidor tem um token primário e pode acessar recursos remotos em que um servidor com a identidade de usuário de inicialização pode não ser capaz de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="b5c39-107">This type of server has a primary token and can access remote resources where a server that has the launching-user identity might not be able to.</span></span> <span data-ttu-id="b5c39-108">Para obter mais informações sobre representação e tokens de acesso, consulte [níveis de representação](impersonation-levels.md) e [encobrimento](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="b5c39-108">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="b5c39-109">A execução como uma conta de usuário fixa é mais segura do que a identidade do usuário interativo, pois essa identidade pode ser atribuída ao aplicativo somente por alguém que tenha a senha do usuário específico.</span><span class="sxs-lookup"><span data-stu-id="b5c39-109">Running as a fixed user account is more secure than the interactive user identity because this identity can be assigned to the application only by someone who has the specific user's password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5c39-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5c39-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5c39-111">Identidade do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="b5c39-111">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="b5c39-112">Usuário interativo</span><span class="sxs-lookup"><span data-stu-id="b5c39-112">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="b5c39-113">Iniciando usuário</span><span class="sxs-lookup"><span data-stu-id="b5c39-113">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="b5c39-114">Identidade do serviço</span><span class="sxs-lookup"><span data-stu-id="b5c39-114">Service Identity</span></span>](service-identity.md)
</dt> </dl>

 

 




