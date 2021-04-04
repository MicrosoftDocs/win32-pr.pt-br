---
description: ICE26 valida as tabelas de sequência em um banco de dados Windows Installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828976"
---
# <a name="ice26"></a><span data-ttu-id="45cdf-103">ICE26</span><span class="sxs-lookup"><span data-stu-id="45cdf-103">ICE26</span></span>

<span data-ttu-id="45cdf-104">ICE26 valida que cada uma das tabelas de [*sequência*](s-gly.md) a seguir contém as ações exigidas pela tabela e não contém nenhuma ação não permitida na tabela:</span><span class="sxs-lookup"><span data-stu-id="45cdf-104">ICE26 validates that each of the following [*sequence tables*](s-gly.md) contain the actions that are required by the table and does not contain any actions disallowed in the table:</span></span>

-   [<span data-ttu-id="45cdf-105">Tabela AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="45cdf-105">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="45cdf-106">Tabela AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="45cdf-106">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="45cdf-107">Tabela InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="45cdf-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="45cdf-108">Tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="45cdf-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="45cdf-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="45cdf-109">Result</span></span>

<span data-ttu-id="45cdf-110">ICE26 posta uma mensagem de erro se o pacote de instalação tiver uma tabela de sequência que não tem uma ação necessária ou que contenha uma ação que não é permitida para a tabela.</span><span class="sxs-lookup"><span data-stu-id="45cdf-110">ICE26 posts an error message if the installation package has a sequence table that lacks a required action or that contains an action that is disallowed for the table.</span></span>

## <a name="example"></a><span data-ttu-id="45cdf-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="45cdf-111">Example</span></span>



| <span data-ttu-id="45cdf-112">Erro de ICE26</span><span class="sxs-lookup"><span data-stu-id="45cdf-112">ICE26 error</span></span>                                                                   | <span data-ttu-id="45cdf-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="45cdf-113">Description</span></span>                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45cdf-114">Ação: ' Action1 ' é necessário na tabela de sequência InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="45cdf-114">Action: 'Action1' is required in the InstallExecuteSequence Sequence table.</span></span>   | <span data-ttu-id="45cdf-115">Uma ação necessária está ausente na tabela de sequência indicada.</span><span class="sxs-lookup"><span data-stu-id="45cdf-115">A required action is missing from the indicated sequence table.</span></span> <span data-ttu-id="45cdf-116">Consulte a template.msi ou as tabelas de sequência sugeridas em [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="45cdf-116">See the template.msi or the suggested sequence tables in [Using a Sequence Table](using-a-sequence-table.md).</span></span> |
| <span data-ttu-id="45cdf-117">Ação: ' Action2 ' é proibido na tabela de sequência InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="45cdf-117">Action: 'Action2' is prohibited in the InstallExecuteSequence Sequence table.</span></span> | <span data-ttu-id="45cdf-118">Esta ação não pode estar na tabela de sequência indicada.</span><span class="sxs-lookup"><span data-stu-id="45cdf-118">This action cannot be in the indicated sequence table.</span></span> <span data-ttu-id="45cdf-119">Remova esta ação da tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="45cdf-119">Remove this action from the sequence table.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="45cdf-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45cdf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45cdf-121">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="45cdf-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



