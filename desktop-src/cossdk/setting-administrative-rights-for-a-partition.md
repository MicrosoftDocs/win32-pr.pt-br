---
description: Configurando direitos administrativos para uma partição
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Configurando direitos administrativos para uma partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646344"
---
# <a name="setting-administrative-rights-for-a-partition"></a><span data-ttu-id="49491-103">Configurando direitos administrativos para uma partição</span><span class="sxs-lookup"><span data-stu-id="49491-103">Setting Administrative Rights for a Partition</span></span>

<span data-ttu-id="49491-104">Os usuários atribuídos à função de administrador do aplicativo do sistema COM+ têm permissão para criar, modificar e excluir partições COM+.</span><span class="sxs-lookup"><span data-stu-id="49491-104">Users assigned the Administrator role of the COM+ System Application are allowed to create, modify, and delete COM+ partitions.</span></span> <span data-ttu-id="49491-105">Na ferramenta administrativa serviços de componentes, as funções administrativas podem ser atribuídas aos usuários expandindo a pasta **funções** do aplicativo de sistema com+.</span><span class="sxs-lookup"><span data-stu-id="49491-105">Within the Component Services administrative tool, administrative roles can be assigned to users by expanding the **Roles** folder of the COM+ System Application.</span></span>

<span data-ttu-id="49491-106">A partir do Windows Server 2003, o recurso de autenticação para o aplicativo de sistema COM+ inclui o valor EOAC \_ Disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="49491-106">As of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="49491-107">Esse valor, que desabilita as ativações de Activate-as-Activator (AAA), é usado na chamada [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ao iniciar o aplicativo do sistema.</span><span class="sxs-lookup"><span data-stu-id="49491-107">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="49491-108">Definir o recurso de autenticação como EOAC \_ Disable \_ AAA permite que um aplicativo executado em uma conta com privilégios (como LocalSystem) ajude a impedir que sua identidade seja usada para iniciar componentes não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="49491-108">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49491-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="49491-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49491-110">Coletando métricas de partição</span><span class="sxs-lookup"><span data-stu-id="49491-110">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="49491-111">Configurando o cache de partição</span><span class="sxs-lookup"><span data-stu-id="49491-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="49491-112">Agrupando aplicativos em partições</span><span class="sxs-lookup"><span data-stu-id="49491-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="49491-113">Gerenciando partições locais</span><span class="sxs-lookup"><span data-stu-id="49491-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="49491-114">Gerenciando partições no Active Directory</span><span class="sxs-lookup"><span data-stu-id="49491-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
