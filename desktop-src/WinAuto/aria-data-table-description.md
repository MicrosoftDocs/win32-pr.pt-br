---
title: Aviso da tabela de dados do ARIA
description: Aviso da tabela de dados do ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006040"
---
# <a name="aria-data-table-warning"></a><span data-ttu-id="1106d-104">Aviso da tabela de dados do ARIA</span><span class="sxs-lookup"><span data-stu-id="1106d-104">ARIA Data Table Warning</span></span>

## <a name="text"></a><span data-ttu-id="1106d-105">Texto</span><span class="sxs-lookup"><span data-stu-id="1106d-105">Text</span></span>

<span data-ttu-id="1106d-106">A tabela contém dados, mas não tem nenhum resumo nem um atributo **DescribedBy do Aria** válido.</span><span class="sxs-lookup"><span data-stu-id="1106d-106">Table contains data but has neither summary nor a valid **aria-describedby** attribute.</span></span>

## <a name="type"></a><span data-ttu-id="1106d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1106d-107">Type</span></span>

<span data-ttu-id="1106d-108">Aviso</span><span class="sxs-lookup"><span data-stu-id="1106d-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="1106d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1106d-109">Description</span></span>

<span data-ttu-id="1106d-110">Esse aviso se aplica a tabelas HTML com mais de uma célula.</span><span class="sxs-lookup"><span data-stu-id="1106d-110">This warning applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="1106d-111">Ele não se aplica a tabelas com `role="presentation"` uma vez que elas são consideradas como tabelas de layout.</span><span class="sxs-lookup"><span data-stu-id="1106d-111">It does not apply to tables with `role="presentation"` since these are considered to be layout tables.</span></span>

<span data-ttu-id="1106d-112">Esse aviso indica que a tabela é identificada como uma tabela de dados, mas não tem uma descrição acessível definida.</span><span class="sxs-lookup"><span data-stu-id="1106d-112">This warning indicates that the table is identified as a data table but it doesn’t have an accessible description defined.</span></span>

> [!Note]  
> <span data-ttu-id="1106d-113">Nem todas as tabelas de dados precisam ter uma descrição acessível.</span><span class="sxs-lookup"><span data-stu-id="1106d-113">Not all data tables are required to have an accessible description.</span></span> <span data-ttu-id="1106d-114">Você deve definir uma descrição acessível se os usuários precisarem de mais informações para entender a estrutura e o conteúdo da tabela de dados.</span><span class="sxs-lookup"><span data-stu-id="1106d-114">You should define an accessible description if users need more information to understand the data table structure and content.</span></span>

 

<span data-ttu-id="1106d-115">Para resolver esse aviso, defina uma descrição acessível de tabela usando o atributo Summary ou o atributo **Aria-DescribedBy** .</span><span class="sxs-lookup"><span data-stu-id="1106d-115">To address this warning, define a table accessible description by using the summary attribute or the **aria-describedby** attribute.</span></span>

## <a name="example"></a><span data-ttu-id="1106d-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1106d-116">Example</span></span>


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




