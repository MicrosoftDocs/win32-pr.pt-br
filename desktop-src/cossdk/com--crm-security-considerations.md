---
description: Considerações de segurança do CRM do COM+
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Considerações de segurança do CRM do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089057"
---
# <a name="com-crm-security-considerations"></a><span data-ttu-id="9a121-103">Considerações de segurança do CRM do COM+</span><span class="sxs-lookup"><span data-stu-id="9a121-103">COM+ CRM Security Considerations</span></span>

<span data-ttu-id="9a121-104">Um arquivo de log do CRM pode conter informações confidenciais que devem ser protegidas.</span><span class="sxs-lookup"><span data-stu-id="9a121-104">A CRM log file could contain sensitive information that must be secured.</span></span> <span data-ttu-id="9a121-105">Por esse motivo, se o aplicativo de servidor estiver sendo executado sob qualquer identidade diferente de usuário interativo quando o arquivo de log do CRM for criado, o arquivo de log do CRM será protegido somente para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="9a121-105">For this reason, if the server application is running under any identity other than Interactive User when the CRM log file is first created, the CRM log file is security protected for that user only.</span></span> <span data-ttu-id="9a121-106">Esse recurso está disponível apenas no sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="9a121-106">This feature is available only on the NTFS file system.</span></span> <span data-ttu-id="9a121-107">Se a identidade do aplicativo do servidor for alterada posteriormente, as informações de segurança do arquivo de log do CRM não serão alteradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9a121-107">If the identity of the server application is subsequently changed, the security information for the CRM log file is not automatically changed.</span></span> <span data-ttu-id="9a121-108">Ele pode ser alterado manualmente usando as ferramentas de administração existentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="9a121-108">It can be changed manually by using existing Windows administration tools.</span></span> <span data-ttu-id="9a121-109">A alternativa é simplesmente excluir o arquivo de log do CRM quando ele estiver em um estado limpo (que é esperado após um desligamento controlado do aplicativo de servidor).</span><span class="sxs-lookup"><span data-stu-id="9a121-109">The alternative is simply to delete the CRM log file when it is in a clean state (which is expected after a controlled shutdown of the server application).</span></span>

<span data-ttu-id="9a121-110">Na operação normal, o COM+ cria o componente compensador de CRM e chama a interface [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) .</span><span class="sxs-lookup"><span data-stu-id="9a121-110">In normal operation, COM+ creates the CRM compensator component and calls the [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) interface.</span></span> <span data-ttu-id="9a121-111">No entanto, um usuário com privilégios para criar o compensador de CRM pode chamar a interface **ICrmCompensator** em momentos inadequados, possivelmente causando problemas de segurança do sistema.</span><span class="sxs-lookup"><span data-stu-id="9a121-111">However, a user having privileges to create the CRM Compensator can call the **ICrmCompensator** interface at inappropriate times, possibly causing system security problems.</span></span> <span data-ttu-id="9a121-112">Para ajudar a proteger contra esses problemas de segurança, o administrador do sistema pode usar a segurança baseada em função para restringir o componente compensador de CRM somente a essas identidades dos aplicativos de servidor em que ele é executado.</span><span class="sxs-lookup"><span data-stu-id="9a121-112">To help protect against these security problems, the system administrator can use role-based security to restrict the CRM Compensator component to only those identities of the server applications in which it runs.</span></span> <span data-ttu-id="9a121-113">Se o componente estiver sendo executado em um aplicativo de biblioteca, isso incluirá todas as identidades dos aplicativos de servidor.</span><span class="sxs-lookup"><span data-stu-id="9a121-113">If the component is running in a library application, this would include all the identities of the server applications.</span></span>

> [!Note]  
> <span data-ttu-id="9a121-114">A partir do Windows Server 2003, para ajudar a impedir a ativação de fora do aplicativo de servidor, é possível garantir um sistema mais seguro marcando o componente compensador de CRM como particular.</span><span class="sxs-lookup"><span data-stu-id="9a121-114">Starting with Windows Server 2003, to help prevent activation from outside the server application, it is possible to further ensure a more secure system by marking the CRM Compensator component as private.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9a121-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a121-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a121-116">Conceitos do Gerenciador de recursos de compensação COM+</span><span class="sxs-lookup"><span data-stu-id="9a121-116">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



