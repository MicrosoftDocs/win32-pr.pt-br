---
description: Os autores de pacote devem garantir que os nomes de quaisquer tabelas, propriedades ou ações personalizadas definidas em seu pacote não entrem em conflito com os nomes de tabelas, propriedades ou ações padrão que são nativas para o Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Nomeando tabelas, propriedades e ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827871"
---
# <a name="naming-custom-tables-properties-and-actions"></a><span data-ttu-id="9441a-103">Nomeando tabelas, propriedades e ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="9441a-103">Naming Custom Tables, Properties, and Actions</span></span>

<span data-ttu-id="9441a-104">Os autores de pacote devem garantir que os nomes de quaisquer tabelas, propriedades ou ações personalizadas definidas em seu pacote não entrem em conflito com os nomes de tabelas, propriedades ou ações padrão que são nativas para o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9441a-104">Package authors should ensure that the names of any custom tables, properties, or actions defined in their package will not conflict with the names of standard tables, properties, or actions that are native to the Windows Installer.</span></span>

<span data-ttu-id="9441a-105">Os autores de pacote devem aderir às seguintes diretrizes para nomes de ações, propriedades ou tabelas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="9441a-105">Package authors should adhere to the following guidelines for custom table, property, or action names.</span></span>

-   <span data-ttu-id="9441a-106">Crie nomes para tabelas, propriedades ou ações personalizadas que tenham um prefixo que identifique seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9441a-106">Make names for custom tables, properties, or actions that have a prefix that identifies your application.</span></span>
-   <span data-ttu-id="9441a-107">Nunca use um nome com MSI como o prefixo.</span><span class="sxs-lookup"><span data-stu-id="9441a-107">Never use a name with Msi as the prefix.</span></span> <span data-ttu-id="9441a-108">A partir do Windows Installer 2,0, todas as novas propriedades, ações e tabelas de Windows Installer nativas recebem nomes prefixados pelo MSI.</span><span class="sxs-lookup"><span data-stu-id="9441a-108">Starting with Windows Installer 2.0, all new native Windows Installer properties, actions, and tables are given names prefixed by Msi.</span></span> <span data-ttu-id="9441a-109">Esse prefixo não diferencia maiúsculas de minúsculas, por exemplo, MsiNewInternalTable.</span><span class="sxs-lookup"><span data-stu-id="9441a-109">This prefix is not case sensitive, for example MsiNewInternalTable.</span></span> <span data-ttu-id="9441a-110">Como o prefixo não diferencia maiúsculas de minúsculas, os autores devem evitar todos os casos do prefixo msi.</span><span class="sxs-lookup"><span data-stu-id="9441a-110">Because the prefix is not case sensitive, authors should avoid all cases of the Msi prefix.</span></span>

<span data-ttu-id="9441a-111">Para obter mais informações, consulte [nomes de tabela](table-names.md).</span><span class="sxs-lookup"><span data-stu-id="9441a-111">For more information, see [Table Names](table-names.md).</span></span>

 

 



