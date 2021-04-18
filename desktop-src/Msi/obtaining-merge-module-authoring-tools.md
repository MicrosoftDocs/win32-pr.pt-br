---
description: Para gerar um módulo de mesclagem, você precisa obter uma ferramenta de software com a qual editar um arquivo. msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Obtendo ferramentas de criação de módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757380"
---
# <a name="obtaining-merge-module-authoring-tools"></a><span data-ttu-id="2b585-103">Obtendo ferramentas de criação de módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="2b585-103">Obtaining Merge Module Authoring Tools</span></span>

<span data-ttu-id="2b585-104">Para gerar um módulo de mesclagem, você precisa obter uma ferramenta de software com a qual editar um arquivo. msm.</span><span class="sxs-lookup"><span data-stu-id="2b585-104">To generate a merge module, you need to obtain a software tool with which to edit an .msm file.</span></span> <span data-ttu-id="2b585-105">Como um arquivo. msm é basicamente um arquivo. msi simplificado, talvez você possa usar as mesmas ferramentas usadas para criar um banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="2b585-105">Because an .msm file is basically a simplified .msi file, you may be able to use the same tools used to create an installation database.</span></span> <span data-ttu-id="2b585-106">Por exemplo, o aplicativo Orca.exe fornecido com o SDK do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b585-106">For example, the application Orca.exe provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="2b585-107">Uma alternativa é comprar uma das ferramentas de empacotamento do instalador para estar disponível de fornecedores de software independentes.</span><span class="sxs-lookup"><span data-stu-id="2b585-107">An alternative is to purchase one of the installer packaging tools to be available from independent software vendors.</span></span> <span data-ttu-id="2b585-108">Há várias ferramentas de terceiros em desenvolvimento que podem ser usadas para produzir módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="2b585-108">There are several third-party tools under development that may be used for producing merge modules.</span></span> <span data-ttu-id="2b585-109">Se você optar por usar uma ferramenta de terceiros, deverá verificar se ela gera módulos de mesclagem consistentes com o padrão descrito neste documento.</span><span class="sxs-lookup"><span data-stu-id="2b585-109">If you choose to use a third-party tool you should verify that it generates merge modules that are consistent with the standard described in this document.</span></span> <span data-ttu-id="2b585-110">Em particular, você deve determinar que as ferramentas de edição não fizeram nenhuma das ações a seguir para o módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="2b585-110">In particular, you should determine that the editing tools have not done any of the following to the merge module.</span></span>

-   <span data-ttu-id="2b585-111">Adicionadas tabelas estranhas ao módulo de mesclagem que não são referenciadas na [tabela ModuleIgnoreTable](moduleignoretable-table.md).</span><span class="sxs-lookup"><span data-stu-id="2b585-111">Added extraneous tables to the merge module that are not referenced in the [ModuleIgnoreTable table](moduleignoretable-table.md).</span></span>

    <span data-ttu-id="2b585-112">Exclua essas tabelas ou adicione-as à tabela ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="2b585-112">Delete these tables or add them to the ModuleIgnoreTable table.</span></span>

-   <span data-ttu-id="2b585-113">Adicionada uma [tabela de TextStyle](textstyle-table.md) desnecessária ao módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="2b585-113">Added an unnecessary [TextStyle table](textstyle-table.md) to the merge module.</span></span>

    <span data-ttu-id="2b585-114">Se o módulo de mesclagem não tiver nenhuma interface do usuário (e geralmente não deveria), você poderá excluir essa tabela com segurança.</span><span class="sxs-lookup"><span data-stu-id="2b585-114">If your merge module has no UI (and it generally should not) you can safely delete this table.</span></span>

-   <span data-ttu-id="2b585-115">Foram adicionadas entradas desnecessárias à [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="2b585-115">Added unnecessary entries to the [Directory table](directory-table.md).</span></span>

    <span data-ttu-id="2b585-116">Remova as entradas desnecessárias da tabela de diretórios.</span><span class="sxs-lookup"><span data-stu-id="2b585-116">Remove unnecessary entries from the Directory table.</span></span>

-   <span data-ttu-id="2b585-117">Informações da esquerda da tabela de validação do módulo de mesclagem \_ .</span><span class="sxs-lookup"><span data-stu-id="2b585-117">Left information out of the merge module's \_Validation table.</span></span>

    <span data-ttu-id="2b585-118">Isso impede a validação do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="2b585-118">This prevents merge module validation.</span></span> <span data-ttu-id="2b585-119">Adicione uma \_ tabela de validação completa.</span><span class="sxs-lookup"><span data-stu-id="2b585-119">Add a complete \_Validation table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b585-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b585-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b585-121">Criando interfaces de usuário em módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="2b585-121">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="2b585-122">Criando tabelas de diretório do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="2b585-122">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="2b585-123">Validando módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="2b585-123">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> </dl>

 

 



