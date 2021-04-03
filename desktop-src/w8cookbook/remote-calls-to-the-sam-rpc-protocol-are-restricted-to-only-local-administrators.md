---
title: Chamadas remotas para o Protocolo RPC SAM são restritas somente a administradores locais
description: O Protocolo RPC SAM está sendo restrito. Isso significa que somente os membros do grupo de Administradores local podem fazer chamadas remotas em relação a métodos nesse protocolo. Active Directory comportamento do controlador de domínio não é afetado.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084131"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a><span data-ttu-id="1cf0b-105">Chamadas remotas para o Protocolo RPC SAM são restritas somente a administradores locais</span><span class="sxs-lookup"><span data-stu-id="1cf0b-105">Remote calls to the SAM RPC protocol are restricted to only local administrators</span></span>

<span data-ttu-id="1cf0b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1cf0b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="1cf0b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1cf0b-108">O Protocolo RPC SAM está sendo restrito.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-108">The SAM RPC protocol is being restricted.</span></span> <span data-ttu-id="1cf0b-109">Isso significa que somente os membros do grupo de Administradores local podem fazer chamadas remotas em relação a métodos nesse protocolo.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-109">This means that only members of the local Administrator group can make remote calls against methods in this protocol.</span></span> <span data-ttu-id="1cf0b-110">Active Directory comportamento do controlador de domínio não é afetado.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-110">Active Directory domain controller behavior is unaffected.</span></span>

## <a name="mitigations"></a><span data-ttu-id="1cf0b-111">Atenuações</span><span class="sxs-lookup"><span data-stu-id="1cf0b-111">Mitigations</span></span>

<span data-ttu-id="1cf0b-112">Verifique se os usuários corretos estão definidos como administradores no PC.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-112">Ensure that the right users are set as administrators on the PC.</span></span> <span data-ttu-id="1cf0b-113">A ACL usada para a verificação de acesso é configurável por meio da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-113">The ACL used for the access check is configurable via group policy.</span></span>

 

 




