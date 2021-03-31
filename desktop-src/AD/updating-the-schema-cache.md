---
title: Atualizando o cache de esquema
description: Todas as informações gravadas em um servidor Active Directory são validadas em relação ao esquema.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Atualizando o AD do cache de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634907"
---
# <a name="updating-the-schema-cache"></a><span data-ttu-id="a9aa3-104">Atualizando o cache de esquema</span><span class="sxs-lookup"><span data-stu-id="a9aa3-104">Updating the Schema Cache</span></span>

<span data-ttu-id="a9aa3-105">Todas as informações gravadas em um servidor Active Directory são validadas em relação ao esquema.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-105">All information that is written to an Active Directory server is validated against the schema.</span></span> <span data-ttu-id="a9aa3-106">O esquema é mantido na memória nos servidores de diretório (controladores de domínio) por motivos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-106">The schema is held in memory on directory servers (domain controllers) for performance reasons.</span></span> <span data-ttu-id="a9aa3-107">A versão na memória é atualizada automaticamente depois que a versão em disco é atualizada.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-107">The in-memory version is updated automatically after the on-disk version has been updated.</span></span> <span data-ttu-id="a9aa3-108">A atualização automática ocorre cinco minutos após a aplicação da última alteração; aplicar outra alteração ao esquema na janela de 5 minutos redefine o temporizador para outros 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-108">The automatic update occurs five minutes after the last change was applied; applying another change to the schema in the 5-minute window resets the timer for another 5 minutes.</span></span> <span data-ttu-id="a9aa3-109">Esse comportamento mantém o cache consistente, mas pode ser confuso, pois as alterações não aparecem no esquema até que o cache seja atualizado, mesmo que elas tenham sido aplicadas no disco.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-109">This behavior keeps the cache consistent, but can be confusing, because changes do not appear in the schema until the cache is updated, even though they were applied on disk.</span></span>

<span data-ttu-id="a9aa3-110">Para atualizar o cache de esquema de Active Directory após uma atualização de esquema, ou se você quiser usar a atualização de esquema para operações que não sejam de esquema imediatamente, adicione o atributo **schemaUpdateNow** (é um atributo operacional) ao DSE raiz (DN em branco) com o valor 1.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-110">To update the Active Directory schema cache after a schema update, or if you want to use the schema update for non-schema operations immediately, add the **schemaUpdateNow** attribute (it is an operational attribute) to the root DSE (blank DN) with value 1.</span></span> <span data-ttu-id="a9aa3-111">Uma atualização do cache de esquema será iniciada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-111">A schema cache update will start immediately.</span></span> <span data-ttu-id="a9aa3-112">A chamada está sendo bloqueada.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-112">The call is blocking.</span></span> <span data-ttu-id="a9aa3-113">Se a chamada retornar sem erro, o cache será atualizado e todas as atualizações de esquema estarão prontas para serem usadas.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-113">If the call returns with no error, the cache is updated and all schema updates are ready to be used.</span></span> <span data-ttu-id="a9aa3-114">Um retorno de erro indica que a atualização do cache não foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-114">An error return indicates the cache update was unsuccessful.</span></span> <span data-ttu-id="a9aa3-115">Os aplicativos que devem usar esse recurso devem ser projetados para acomodar a gravação de bloqueio, particularmente em fornecer os comentários do usuário, se o programa ou o script for executado interativamente.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-115">Applications that must use this feature should be designed to accommodate the blocking write, particularly in giving the user feedback, if the program or script executes interactively.</span></span>

<span data-ttu-id="a9aa3-116">O exemplo de código a seguir é um exemplo de script do LDIFDE que mostra como disparar um recarregamento de cache.</span><span class="sxs-lookup"><span data-stu-id="a9aa3-116">The following code example is a sample LDIFDE script that shows how to trigger a cache reload.</span></span>

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

<span data-ttu-id="a9aa3-117">Para obter mais informações sobre como atualizar o cache de esquema programaticamente, consulte [código de exemplo para atualizar o cache de esquema](example-code-for-updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="a9aa3-117">For more information about how to update the schema cache programmatically, see [Example Code for Updating the Schema Cache](example-code-for-updating-the-schema-cache.md).</span></span>

 

 




