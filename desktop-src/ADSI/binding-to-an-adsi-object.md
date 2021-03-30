---
title: Associação a um objeto ADSI
description: A conexão a um objeto em um serviço de diretório é conhecida como associação.
ms.assetid: f3963019-9b3a-42d5-a978-484f294110e5
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usando, associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0fefcdb62d374d98e3007864168e2626ecc5d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634893"
---
# <a name="binding-to-an-adsi-object"></a><span data-ttu-id="7c3ff-104">Associação a um objeto ADSI</span><span class="sxs-lookup"><span data-stu-id="7c3ff-104">Binding to an ADSI Object</span></span>

<span data-ttu-id="7c3ff-105">A conexão a um objeto em um serviço de diretório é conhecida como associação.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-105">Connecting to an object in a directory service is known as binding.</span></span> <span data-ttu-id="7c3ff-106">A vinculação a um objeto ADSI é a primeira etapa para se comunicar com o sistema de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-106">Binding to an ADSI object is the first step to communicating with the underlying directory system.</span></span> <span data-ttu-id="7c3ff-107">Um objeto deve estar associado para que você possa navegar no namespace, pesquisar dados, modificar dados ou representar um usuário.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-107">An object must be bound to in order to navigate its namespace, search for data, modify data, or impersonate a user.</span></span> <span data-ttu-id="7c3ff-108">Também é possível fornecer características de associação adicionais, como nome de usuário, senha, nome do servidor, métodos de criptografia e autenticação segura.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-108">It is also possible to supply additional binding characteristics, such as user name, password, server name, encryption methods, and secured authentication.</span></span> <span data-ttu-id="7c3ff-109">As características de associação adicionais reais que podem ser usadas dependerão do provedor.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-109">The actual additional binding characteristics that can be used will depend on the provider.</span></span>

<span data-ttu-id="7c3ff-110">Para obter mais informações sobre a vinculação ADSI, consulte:</span><span class="sxs-lookup"><span data-stu-id="7c3ff-110">For more information about ADSI binding, see:</span></span>

-   [<span data-ttu-id="7c3ff-111">Cadeia de vinculação</span><span class="sxs-lookup"><span data-stu-id="7c3ff-111">Binding String</span></span>](binding-string.md)
-   [<span data-ttu-id="7c3ff-112">Tipos de associação específicos para Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c3ff-112">Binding Types Specific to Active Directory</span></span>](binding-types-specific-to-active-directory.md)
-   [<span data-ttu-id="7c3ff-113">Problemas de associação para ambientes mistos</span><span class="sxs-lookup"><span data-stu-id="7c3ff-113">Binding Issues for Mixed Environments</span></span>](binding-issues-for-mixed-environments.md)
-   [<span data-ttu-id="7c3ff-114">Ligando programaticamente usando uma interface ADSI</span><span class="sxs-lookup"><span data-stu-id="7c3ff-114">Binding Programmatically Using an ADSI Interface</span></span>](binding-programmatically-using-an-adsi-interface.md)
-   [<span data-ttu-id="7c3ff-115">Cache de conexão</span><span class="sxs-lookup"><span data-stu-id="7c3ff-115">Connection Caching</span></span>](connection-caching.md)
-   [<span data-ttu-id="7c3ff-116">Associação a objetos filho</span><span class="sxs-lookup"><span data-stu-id="7c3ff-116">Binding to Child Objects</span></span>](binding-to-child-objects.md)
-   [<span data-ttu-id="7c3ff-117">Associando ao pai de um objeto</span><span class="sxs-lookup"><span data-stu-id="7c3ff-117">Binding to an Object's Parent</span></span>](binding-to-an-objectampaposs-parent.md)
-   [<span data-ttu-id="7c3ff-118">Opção de ligação rápida para operações de gravação/modificação em lote</span><span class="sxs-lookup"><span data-stu-id="7c3ff-118">Fast Binding Option for Batch Write/Modify Operations</span></span>](fast-binding-option-for-batch-writemodify-operations.md)
-   [<span data-ttu-id="7c3ff-119">Escolhendo uma interface para associação</span><span class="sxs-lookup"><span data-stu-id="7c3ff-119">Choosing an Interface for Binding</span></span>](choosing-an-interface.md)

 

 




