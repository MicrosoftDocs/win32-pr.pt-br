---
description: Os módulos de mesclagem só funcionam com componentes e não com recursos. No entanto, algumas tabelas em módulos de mesclagem, como a tabela PublishComponent, contêm campos que se referem a recursos.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Referenciando recursos em módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921639"
---
# <a name="referencing-features-in-merge-modules"></a><span data-ttu-id="92a66-104">Referenciando recursos em módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="92a66-104">Referencing Features in Merge Modules</span></span>

<span data-ttu-id="92a66-105">Os módulos de mesclagem só funcionam com componentes e não com recursos.</span><span class="sxs-lookup"><span data-stu-id="92a66-105">Merge modules only operate with components and not with features.</span></span> <span data-ttu-id="92a66-106">No entanto, algumas tabelas em módulos de mesclagem, como a [tabela PublishComponent](publishcomponent-table.md), contêm campos que se referem a recursos.</span><span class="sxs-lookup"><span data-stu-id="92a66-106">However, some tables in merge modules, such as the [PublishComponent table](publishcomponent-table.md), contain fields that refer to features.</span></span>

<span data-ttu-id="92a66-107">Um GUID nulo: {00000000-0000-0000-0000-000000000000} deve ser criado em qualquer campo de um banco de dados de módulo de mesclagem que faça referência a um recurso.</span><span class="sxs-lookup"><span data-stu-id="92a66-107">A null GUID: {00000000-0000-0000-0000-000000000000} must be authored into any field of a merge module database that references a feature.</span></span> <span data-ttu-id="92a66-108">Quando o módulo de mesclagem é mesclado em um pacote de instalação, a ferramenta de mesclagem substitui o GUID nulo pelo recurso especificado no pacote de instalação, exceto para tabelas que exigem tratamento especial, como a [tabela ModuleSignature](modulesignature-table.md) e as tabelas ModuleSequence.</span><span class="sxs-lookup"><span data-stu-id="92a66-108">When the merge module is merged into an installation package, the merge tool replaces the null GUID with the feature specified in the installation package, except for tables that require special handling, such as the [ModuleSignature table](modulesignature-table.md) and the ModuleSequence tables.</span></span>

<span data-ttu-id="92a66-109">Observe que, se um GUID NULL for usado como uma chave primária, não haverá garantia de que o valor substituído pela ferramenta de mesclagem seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="92a66-109">Note that if a null GUID is used as a primary key, it is not guaranteed that the value substituted by the merge tool is unique.</span></span> <span data-ttu-id="92a66-110">Os autores de módulos de mesclagem são responsáveis por garantir que nenhuma chave primária existente na interface do usuário seja duplicada quando a ferramenta de mesclagem substituir os GUIDs nulos por recursos.</span><span class="sxs-lookup"><span data-stu-id="92a66-110">Authors of merge modules are responsible for ensuring that no existing primary key in the user's interface is duplicated when the merge tool replaces null GUIDs with features.</span></span>

 

 



