---
description: A tabela CCPSearch contém a lista de assinaturas de arquivo usadas para o CCP (programa de verificação de conformidade). Pelo menos um desses arquivos precisa estar presente no computador de um usuário para que o usuário esteja em conformidade com o programa.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Tabela CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770383"
---
# <a name="ccpsearch-table"></a><span data-ttu-id="6ecd8-104">Tabela CCPSearch</span><span class="sxs-lookup"><span data-stu-id="6ecd8-104">CCPSearch Table</span></span>

<span data-ttu-id="6ecd8-105">A tabela CCPSearch contém a lista de assinaturas de arquivo usadas para o CCP (programa de verificação de conformidade).</span><span class="sxs-lookup"><span data-stu-id="6ecd8-105">The CCPSearch table contains the list of file signatures used for the Compliance Checking Program (CCP).</span></span> <span data-ttu-id="6ecd8-106">Pelo menos um desses arquivos precisa estar presente no computador de um usuário para que o usuário esteja em conformidade com o programa.</span><span class="sxs-lookup"><span data-stu-id="6ecd8-106">At least one of these files needs to be present on a user's computer for the user to be in compliance with the program.</span></span>

<span data-ttu-id="6ecd8-107">A tabela CCPSearch tem a seguinte coluna.</span><span class="sxs-lookup"><span data-stu-id="6ecd8-107">The CCPSearch table has the following column.</span></span>



| <span data-ttu-id="6ecd8-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="6ecd8-108">Column</span></span>      | <span data-ttu-id="6ecd8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ecd8-109">Type</span></span>                         | <span data-ttu-id="6ecd8-110">Chave</span><span class="sxs-lookup"><span data-stu-id="6ecd8-110">Key</span></span> | <span data-ttu-id="6ecd8-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="6ecd8-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="6ecd8-112">Signature\_</span><span class="sxs-lookup"><span data-stu-id="6ecd8-112">Signature\_</span></span> | [<span data-ttu-id="6ecd8-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="6ecd8-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="6ecd8-114">S</span><span class="sxs-lookup"><span data-stu-id="6ecd8-114">Y</span></span>   | <span data-ttu-id="6ecd8-115">N</span><span class="sxs-lookup"><span data-stu-id="6ecd8-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="6ecd8-116">Coluna</span><span class="sxs-lookup"><span data-stu-id="6ecd8-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="6ecd8-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="6ecd8-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="6ecd8-118">A assinatura \_ representa uma assinatura de arquivo exclusiva e também é a chave externa nas tabelas [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)e [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="6ecd8-118">The Signature\_ represents a unique file signature and is also the external key into the [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ecd8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ecd8-119">Remarks</span></span>

<span data-ttu-id="6ecd8-120">Essa tabela é referida quando a ação [CCPSearch](ccpsearch-action.md) ou a [ação RMCCPSearch](rmccpsearch-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="6ecd8-120">This table is referred to when the [CCPSearch action](ccpsearch-action.md) or the [RMCCPSearch action](rmccpsearch-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="6ecd8-121">Validação</span><span class="sxs-lookup"><span data-stu-id="6ecd8-121">Validation</span></span>

<dl>

[<span data-ttu-id="6ecd8-122">ICE03</span><span class="sxs-lookup"><span data-stu-id="6ecd8-122">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6ecd8-123">ICE06</span><span class="sxs-lookup"><span data-stu-id="6ecd8-123">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6ecd8-124">ICE32</span><span class="sxs-lookup"><span data-stu-id="6ecd8-124">ICE32</span></span>](ice32.md)  
</dl>

 

 



