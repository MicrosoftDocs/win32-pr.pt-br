---
description: O ICE06 verifica todas as tabelas para validar se todas as colunas listadas na \_ tabela de validação estão presentes na tabela. Se uma tabela não existir, todas \_ as entradas de validação para essa tabela serão ignoradas.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922025"
---
# <a name="ice06"></a><span data-ttu-id="6cbfe-104">ICE06</span><span class="sxs-lookup"><span data-stu-id="6cbfe-104">ICE06</span></span>

<span data-ttu-id="6cbfe-105">O ICE06 verifica todas as tabelas para validar se todas as colunas listadas na [ \_ tabela de validação](-validation-table.md) estão presentes na tabela.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-105">ICE06 checks every table to validate that all the columns listed in the [\_Validation table](-validation-table.md) are present in the table.</span></span> <span data-ttu-id="6cbfe-106">Se uma tabela não existir, todas \_ as entradas de validação para essa tabela serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-106">If a table does not exist, any \_Validation entries for that table are ignored.</span></span>

<span data-ttu-id="6cbfe-107">A finalidade do ICE06 é detectar instâncias nas quais um autor tenta usar uma nova tabela de \_ validação que reflete uma alteração de esquema com um banco de dados antigo que não foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-107">The purpose of ICE06 is to detect instances in which an author tries to use a new \_Validation table that reflects a schema change with an old database that has not been updated.</span></span> <span data-ttu-id="6cbfe-108">ICE06 também detecta o caso inverso de uma \_ tabela de validação antiga que está sendo usada com um banco de dados alterado.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-108">ICE06 also detects the reverse case of an old \_Validation table being used with an altered database.</span></span>

<span data-ttu-id="6cbfe-109">Observe que a validação interna executada pelo [ICE03](ice03.md) captura a instância de uma coluna de tabela não definida na \_ tabela de validação que está sendo listada no catálogo de colunas.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-109">Note that the internal validation performed by [ICE03](ice03.md) catches the instance of a table column not defined in the \_Validation table being listed in the columns catalog.</span></span> <span data-ttu-id="6cbfe-110">O uso de ICE03 e ICE06, portanto, garante que todas as colunas no banco de dados sejam testadas.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-110">The use of both ICE03 and ICE06 therefore ensures every column in the database is tested.</span></span>

## <a name="result"></a><span data-ttu-id="6cbfe-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="6cbfe-111">Result</span></span>

<span data-ttu-id="6cbfe-112">ICE06 posta um erro quando há uma coluna de tabela definida na \_ tabela de validação que não está listada na \_ tabela colunas.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-112">ICE06 posts an error when there is a table column defined in the \_Validation table that is not listed in the \_Columns table.</span></span>

## <a name="example"></a><span data-ttu-id="6cbfe-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6cbfe-113">Example</span></span>

<span data-ttu-id="6cbfe-114">Para o exemplo a seguir, o ICE06 posta a mensagem</span><span class="sxs-lookup"><span data-stu-id="6cbfe-114">For the following example ICE06 posts the message</span></span>

<span data-ttu-id="6cbfe-115">A coluna: versão da tabela: ModuleSignature não está definida no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-115">Column: Version of Table: ModuleSignature is not defined in database.</span></span>

<span data-ttu-id="6cbfe-116">[ \_ Tabela de validação](-validation-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6cbfe-116">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="6cbfe-117">Tabela</span><span class="sxs-lookup"><span data-stu-id="6cbfe-117">Table</span></span>           | <span data-ttu-id="6cbfe-118">Coluna</span><span class="sxs-lookup"><span data-stu-id="6cbfe-118">Column</span></span>   |
|-----------------|----------|
| <span data-ttu-id="6cbfe-119">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="6cbfe-119">ModuleSignature</span></span> | <span data-ttu-id="6cbfe-120">ModuleID</span><span class="sxs-lookup"><span data-stu-id="6cbfe-120">ModuleID</span></span> |
| <span data-ttu-id="6cbfe-121">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="6cbfe-121">ModuleSignature</span></span> | <span data-ttu-id="6cbfe-122">Versão</span><span class="sxs-lookup"><span data-stu-id="6cbfe-122">Version</span></span>  |



 

<span data-ttu-id="6cbfe-123">[ \_ Tabela de colunas](-columns-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6cbfe-123">[\_Columns Table](-columns-table.md) (partial)</span></span>



| <span data-ttu-id="6cbfe-124">Tabela</span><span class="sxs-lookup"><span data-stu-id="6cbfe-124">Table</span></span>           | <span data-ttu-id="6cbfe-125">Número</span><span class="sxs-lookup"><span data-stu-id="6cbfe-125">Number</span></span> | <span data-ttu-id="6cbfe-126">Nome</span><span class="sxs-lookup"><span data-stu-id="6cbfe-126">Name</span></span>     |
|-----------------|--------|----------|
| <span data-ttu-id="6cbfe-127">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="6cbfe-127">ModuleSignature</span></span> | <span data-ttu-id="6cbfe-128">1</span><span class="sxs-lookup"><span data-stu-id="6cbfe-128">1</span></span>      | <span data-ttu-id="6cbfe-129">ModuleID</span><span class="sxs-lookup"><span data-stu-id="6cbfe-129">ModuleID</span></span> |



 

<span data-ttu-id="6cbfe-130">A coluna versão da tabela ModuleSignature não está no banco de dados ou está listada na \_ tabela colunas.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-130">The Version column of the ModuleSignature table is not in the database or listed in the \_Columns table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cbfe-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cbfe-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cbfe-132">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="6cbfe-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



