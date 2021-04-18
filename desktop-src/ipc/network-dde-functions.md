---
description: As funções a seguir são usadas com o DDE de rede.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Funções DDE de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807283"
---
# <a name="network-dde-functions"></a><span data-ttu-id="4e550-103">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="4e550-103">Network DDE Functions</span></span>

<span data-ttu-id="4e550-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="4e550-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="4e550-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="4e550-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="4e550-106">As funções a seguir são usadas com o DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="4e550-106">The following functions are used with network DDE.</span></span>



| <span data-ttu-id="4e550-107">Função</span><span class="sxs-lookup"><span data-stu-id="4e550-107">Function</span></span>                                                   | <span data-ttu-id="4e550-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e550-108">Description</span></span>                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e550-109">**NDdeGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="4e550-109">**NDdeGetErrorString**</span></span>](nddegeterrorstring.md)           | <span data-ttu-id="4e550-110">Converte um código de erro retornado por uma função DDE de rede em uma cadeia de caracteres de erro que explica o código de erro retornado.</span><span class="sxs-lookup"><span data-stu-id="4e550-110">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span> |
| [<span data-ttu-id="4e550-111">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="4e550-111">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)       | <span data-ttu-id="4e550-112">Recupera o descritor de segurança associado ao compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="4e550-112">Retrieves the security descriptor associated with the DDE share.</span></span>                                                      |
| [<span data-ttu-id="4e550-113">**NDdeGetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="4e550-113">**NDdeGetTrustedShare**</span></span>](nddegettrustedshare.md)         | <span data-ttu-id="4e550-114">Recupera as opções associadas a um compartilhamento DDE que está na lista de compartilhamentos confiáveis do usuário do servidor.</span><span class="sxs-lookup"><span data-stu-id="4e550-114">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>                |
| [<span data-ttu-id="4e550-115">**NDdeIsValidAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="4e550-115">**NDdeIsValidAppTopicList**</span></span>](nddeisvalidapptopiclist.md) | <span data-ttu-id="4e550-116">Determina se um aplicativo e uma cadeia de caracteres de tópico ("*AppName* \| *topicname*") usam a sintaxe correta.</span><span class="sxs-lookup"><span data-stu-id="4e550-116">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>                 |
| [<span data-ttu-id="4e550-117">**NDdeIsValidShareName**</span><span class="sxs-lookup"><span data-stu-id="4e550-117">**NDdeIsValidShareName**</span></span>](nddeisvalidsharename.md)       | <span data-ttu-id="4e550-118">Determina se um nome de compartilhamento usa a sintaxe apropriada.</span><span class="sxs-lookup"><span data-stu-id="4e550-118">Determines whether a share name uses the proper syntax.</span></span>                                                               |
| [<span data-ttu-id="4e550-119">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="4e550-119">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)       | <span data-ttu-id="4e550-120">Define o descritor de segurança associado ao compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="4e550-120">Sets the security descriptor associated with the DDE share.</span></span>                                                           |
| [<span data-ttu-id="4e550-121">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="4e550-121">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)         | <span data-ttu-id="4e550-122">Concede o status confiável do compartilhamento DDE especificado no contexto do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="4e550-122">Grants the specified DDE share trusted status within the current user's context.</span></span>                                      |
| [<span data-ttu-id="4e550-123">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="4e550-123">**NDdeShareAdd**</span></span>](nddeshareadd.md)                       | <span data-ttu-id="4e550-124">Cria e adiciona um novo compartilhamento DDE ao Gerenciador de banco de dados de compartilhamento DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="4e550-124">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>                                            |
| [<span data-ttu-id="4e550-125">**NDdeShareDel**</span><span class="sxs-lookup"><span data-stu-id="4e550-125">**NDdeShareDel**</span></span>](nddesharedel.md)                       | <span data-ttu-id="4e550-126">Exclui um compartilhamento DDE do DSDM.</span><span class="sxs-lookup"><span data-stu-id="4e550-126">Deletes a DDE share from the DSDM.</span></span>                                                                                    |
| [<span data-ttu-id="4e550-127">**NDdeShareEnum**</span><span class="sxs-lookup"><span data-stu-id="4e550-127">**NDdeShareEnum**</span></span>](nddeshareenum.md)                     | <span data-ttu-id="4e550-128">Recupera a lista de compartilhamentos DDE disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4e550-128">Retrieves the list of available DDE shares.</span></span>                                                                           |
| [<span data-ttu-id="4e550-129">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="4e550-129">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)               | <span data-ttu-id="4e550-130">Recupera informações de compartilhamento de DDE.</span><span class="sxs-lookup"><span data-stu-id="4e550-130">Retrieves DDE share information.</span></span>                                                                                      |
| [<span data-ttu-id="4e550-131">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="4e550-131">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)               | <span data-ttu-id="4e550-132">Define informações de compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="4e550-132">Sets DDE share information.</span></span>                                                                                           |
| [<span data-ttu-id="4e550-133">**NDdeTrustedShareEnum**</span><span class="sxs-lookup"><span data-stu-id="4e550-133">**NDdeTrustedShareEnum**</span></span>](nddetrustedshareenum.md)       | <span data-ttu-id="4e550-134">Recupera os nomes de todos os compartilhamentos de DDE de rede que são confiáveis no contexto do processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="4e550-134">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>                 |



 

 

 



