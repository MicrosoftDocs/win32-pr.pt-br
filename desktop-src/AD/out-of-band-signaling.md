---
title: Sinalização fora de banda
description: Os aplicativos de cooperação que compartilham dados comuns usando o diretório podem usar a sinalização fora de banda para evitar a distorção de versão e atualizações parciais.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004907"
---
# <a name="out-of-band-signaling"></a><span data-ttu-id="20c42-103">Sinalização fora de banda</span><span class="sxs-lookup"><span data-stu-id="20c42-103">Out-of-Band Signaling</span></span>

<span data-ttu-id="20c42-104">Os aplicativos de cooperação que compartilham dados comuns usando o diretório podem usar a sinalização fora de banda para evitar a distorção de versão e atualizações parciais.</span><span class="sxs-lookup"><span data-stu-id="20c42-104">Cooperating applications that share common data using the directory can use out-of-band signaling to avoid both version skew and partial updates.</span></span> <span data-ttu-id="20c42-105">Em suma, os aplicativos de cooperação usam um mecanismo separado da replicação de diretório para informar um ao outro sobre as alterações nos dados comuns compartilhados.</span><span class="sxs-lookup"><span data-stu-id="20c42-105">Put simply, the cooperating applications use a mechanism separate from directory replication to inform each other of changes in the shared common data.</span></span> <span data-ttu-id="20c42-106">A sinalização fora de banda é mais eficiente quando usada em combinação com um mecanismo de controle de versão — isso permite que o parceiro detecte a alteração para notificar os parceiros remotos de qual versão dos dados compartilhados aguardar.</span><span class="sxs-lookup"><span data-stu-id="20c42-106">Out-of-band signaling is most effective when used in combination with a versioning mechanism—this allows the partner detecting the change to notify remote partners what version of the shared data to wait for.</span></span>

<span data-ttu-id="20c42-107">Retornando ao exemplo de RPC fornecido na seção "distorção de versão" do [comportamento de replicação no Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), o servidor RPC poderia chamar de volta os clientes conectados para informá-los da mudança para um novo servidor: "vou mover.</span><span class="sxs-lookup"><span data-stu-id="20c42-107">Returning to the RPC example given in the "Version Skew" section of [Replication Behavior in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), the RPC server could call back into connected clients to inform them of the move to a new server: "I am going to move.</span></span> <span data-ttu-id="20c42-108">Aguarde, a replicação levará o novo endereço em breve "para que o cliente possa lidar com o período de transição.</span><span class="sxs-lookup"><span data-stu-id="20c42-108">Please stand by, replication will bring you the new address shortly" so that the client can handle the transition period.</span></span>

<span data-ttu-id="20c42-109">Os aplicativos que exigem políticas idênticas em vigor para se comunicar entre si podem usar a sinalização fora de banda para garantir que uma nova política não seja empregada até que todas as partes envolvidas tenham recebido isso.</span><span class="sxs-lookup"><span data-stu-id="20c42-109">Applications that require identical policies to be in force in order to communicate with each other can use out-of-band signaling to ensure that a new policy is not employed until all involved parties have received it.</span></span> <span data-ttu-id="20c42-110">Por exemplo, se a política de IPsec entre dois computadores for alterada, um agente no computador de origem poderá contatar um agente no computador de destino para negociar o aplicativo da política alterada, com o aplicativo de atraso da máquina de origem até que a máquina de destino tenha recebido a nova política também.</span><span class="sxs-lookup"><span data-stu-id="20c42-110">For example, if the Internet Protocol security (IPsec) policy between two machines is changed, an agent on the source machine could contact an agent on the destination machine to negotiate the application of the changed policy, with the source machine delaying application until the destination machine has received the new policy as well.</span></span>

 

 




