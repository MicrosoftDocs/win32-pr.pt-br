---
description: Descreva como usar as funções de política LSA.
ms.assetid: 7f4b963d-3442-4c04-b3d4-f7c8eb1ed15b
title: Usando a política LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 240a59c9009b91d03c1e0904861f815773c95af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171476"
---
# <a name="using-lsa-policy"></a><span data-ttu-id="b9d6b-103">Usando a política LSA</span><span class="sxs-lookup"><span data-stu-id="b9d6b-103">Using LSA Policy</span></span>

<span data-ttu-id="b9d6b-104">Os tópicos a seguir descrevem como usar as funções de política do LSA.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-104">The following topics describe how to use the LSA Policy functions.</span></span>

-   <span data-ttu-id="b9d6b-105">O [uso de cadeias de caracteres do LSA Unicode](using-lsa-unicode-strings.md) explica como converter cadeias de caracteres no formato de estrutura usado por algumas funções de diretiva LSA.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-105">[Using LSA Unicode Strings](using-lsa-unicode-strings.md) explains how to convert strings into the structure format used by some LSA Policy functions.</span></span>
-   <span data-ttu-id="b9d6b-106">A [abertura de um identificador de objeto de política](opening-a-policy-object-handle.md) descreve como abrir um identificador para o objeto de [**política**](policy-object.md) local.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-106">[Opening a Policy Object Handle](opening-a-policy-object-handle.md) describes how to open a handle to the local [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="b9d6b-107">Esse identificador é exigido por muitas das funções da diretiva LSA como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-107">This handle is required by many of the LSA Policy functions as an input parameter.</span></span>
-   <span data-ttu-id="b9d6b-108">[Gerenciar informações de política](managing-policy-information.md) detalha como definir e consultar informações de política global para o sistema local e o domínio.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-108">[Managing Policy Information](managing-policy-information.md) details how to set and query global policy information for the local system and the domain.</span></span>
-   <span data-ttu-id="b9d6b-109">O [recebimento de eventos de alteração de política](receiving-policy-change-events.md) descreve como criar e registrar um evento para receber notificações quando as informações de política forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-109">[Receiving Policy Change Events](receiving-policy-change-events.md) describes how to create and register an event to receive notifications when policy information changes.</span></span>
-   <span data-ttu-id="b9d6b-110">[Gerenciar permissões de conta](managing-account-permissions.md) explica como criar, excluir e enumerar contas e como adicionar e remover privilégios para essas contas.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-110">[Managing Account Permissions](managing-account-permissions.md) explains how to create, delete, and enumerate accounts and how to add and remove privileges for those accounts.</span></span>
-   <span data-ttu-id="b9d6b-111">[Gerenciar informações de domínio confiável](managing-trusted-domain-information.md) descreve como criar, enumerar e excluir domínios confiáveis e como definir e recuperar informações de domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-111">[Managing Trusted Domain Information](managing-trusted-domain-information.md) describes how to create, enumerate, and delete trusted domains, and how to set and retrieve trusted domain information.</span></span>
-   <span data-ttu-id="b9d6b-112">A [conversão entre nomes e SIDs](translating-between-names-and-sids.md) explica como mapear SIDs para nomes de conta e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-112">[Translating Between Names and SIDs](translating-between-names-and-sids.md) explains how to map SIDs to account names and vice versa.</span></span>
-   <span data-ttu-id="b9d6b-113">[Mapeamento de identificadores POSIX](mapping-posix-identifiers.md) descreve como mapear SIDs para identificadores posix de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-113">[Mapping Posix Identifiers](mapping-posix-identifiers.md) describes how to map SIDs to 32-bit Posix identifiers.</span></span>
-   <span data-ttu-id="b9d6b-114">O [armazenamento de dados privados](storing-private-data.md) explica como armazenar e recuperar cadeias de caracteres de dados particulares.</span><span class="sxs-lookup"><span data-stu-id="b9d6b-114">[Storing Private Data](storing-private-data.md) explains how to store and retrieve private data strings.</span></span>

<span data-ttu-id="b9d6b-115">Para obter informações sobre como usar o LSA para fazer logon e autenticar usuários, consulte [autenticação LSA](/windows/desktop/SecAuthN/lsa-authentication).</span><span class="sxs-lookup"><span data-stu-id="b9d6b-115">For information about how to use the LSA to logon and authenticate users, see [LSA Authentication](/windows/desktop/SecAuthN/lsa-authentication).</span></span>

 

 
