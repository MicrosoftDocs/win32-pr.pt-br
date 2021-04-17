---
description: A tabela ModuleSignature contém todas as informações necessárias para identificar o módulo de mesclagem.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Criando tabelas ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752663"
---
# <a name="authoring-modulesignature-tables"></a><span data-ttu-id="5143c-103">Criando tabelas ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="5143c-103">Authoring ModuleSignature Tables</span></span>

<span data-ttu-id="5143c-104">A [tabela ModuleSignature](modulesignature-table.md) contém todas as informações necessárias para identificar o módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5143c-104">The [ModuleSignature table](modulesignature-table.md) contains all the information needed to identify the merge module.</span></span>

<span data-ttu-id="5143c-105">O campo ModuleID é a chave primária para esta tabela e deve seguir a Convenção descrita em [nomeando chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="5143c-105">The ModuleID field is the primary key for this table and must follow the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="5143c-106">Por exemplo, se o nome legível do módulo de mesclagem for MyLibrary e o GUID do módulo de mesclagem for {880DE2F0-CDD8-11D1-A849-006097ABDE17}, a entrada na coluna ModuleID da tabela ModuleSignature se tornará MyLibrary. 880DE2F0 \_ CDD8 11D1 A849 006097ABDE17 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5143c-106">For example, if the readable name of the merge module is MyLibrary and the GUID for the merge module is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column of the ModuleSignature table becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

<span data-ttu-id="5143c-107">Insira o identificador decimal para o idioma padrão do módulo de mesclagem no campo idioma da tabela ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="5143c-107">Enter the decimal identifier for the default language of the merge module into the Language field of the ModuleSignature table.</span></span>

<span data-ttu-id="5143c-108">Insira a versão do módulo de mesclagem no campo versão.</span><span class="sxs-lookup"><span data-stu-id="5143c-108">Enter the version of the merge module into the Version field.</span></span>

 

 



