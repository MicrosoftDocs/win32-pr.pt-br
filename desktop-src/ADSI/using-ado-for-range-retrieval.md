---
title: Usando ADO para recuperação de intervalo
description: Se for usado um idioma de automação, os ADO (objetos de diretório do ActiveX) deverão ser usados para recuperar um intervalo de valores de propriedade. Ao usar o ADO para recuperação de intervalo, há um problema que deve ser resolvido especificamente.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Usando ADO para o ADSI de recuperação de intervalo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634857"
---
# <a name="using-ado-for-range-retrieval"></a><span data-ttu-id="c62a5-104">Usando ADO para recuperação de intervalo</span><span class="sxs-lookup"><span data-stu-id="c62a5-104">Using ADO for Range Retrieval</span></span>

<span data-ttu-id="c62a5-105">Se for usado um idioma de automação, os ADO (objetos de diretório do ActiveX) deverão ser usados para recuperar um intervalo de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c62a5-105">If an automation language is used, the ActiveX Directory Objects (ADO) should be used to retrieve a range of property values.</span></span>

<span data-ttu-id="c62a5-106">Ao usar o ADO para recuperação de intervalo, há um problema que deve ser resolvido especificamente.</span><span class="sxs-lookup"><span data-stu-id="c62a5-106">When using ADO for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="c62a5-107">Ao consultar o grupo final de valores de propriedade, o objeto ADO recuperará zero objetos, embora mais permaneça.</span><span class="sxs-lookup"><span data-stu-id="c62a5-107">When querying for the final group of property values, the ADO object will retrieve zero objects, even though more remain.</span></span> <span data-ttu-id="c62a5-108">Para recuperar os valores restantes, use o curinga de intervalo ' \* '.</span><span class="sxs-lookup"><span data-stu-id="c62a5-108">To retrieve the remaining values, use the range wildcard '\*'.</span></span> <span data-ttu-id="c62a5-109">Por exemplo, se um grupo contiver 150 Membros, os valores de membro 0-100 poderão ser recuperados normalmente usando a recuperação em intervalos.</span><span class="sxs-lookup"><span data-stu-id="c62a5-109">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="c62a5-110">Se o intervalo 101-200 for solicitado, o objeto ADO retornará zero objetos.</span><span class="sxs-lookup"><span data-stu-id="c62a5-110">If range 101-200 is then requested, the ADO object will return zero objects.</span></span> <span data-ttu-id="c62a5-111">Neste ponto, é necessário modificar a consulta para o intervalo de solicitação 101- \* .</span><span class="sxs-lookup"><span data-stu-id="c62a5-111">At this point, it is necessary to modify the query to request range 101-\*.</span></span> <span data-ttu-id="c62a5-112">Isso recuperará os valores de 101 para 150.</span><span class="sxs-lookup"><span data-stu-id="c62a5-112">This will retrieve values from 101 to 150.</span></span> <span data-ttu-id="c62a5-113">Para obter mais informações e um exemplo de código, consulte [código de exemplo para usar a variação para recuperar membros de um grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span><span class="sxs-lookup"><span data-stu-id="c62a5-113">For more information and a code example, see [Example Code for Using Ranging to Retrieve Members of a Group](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span></span>

<span data-ttu-id="c62a5-114">Para obter mais informações sobre como usar o ADO para recuperação de intervalo, consulte:</span><span class="sxs-lookup"><span data-stu-id="c62a5-114">For more information about using ADO for range retrieval, see:</span></span>

-   [<span data-ttu-id="c62a5-115">Dialeto de intervalo de LDAP do ADO</span><span class="sxs-lookup"><span data-stu-id="c62a5-115">ADO LDAP Ranging Dialect</span></span>](ado-ldap-ranging-dialect.md)
-   [<span data-ttu-id="c62a5-116">Dialeto de intervalo de SQL do ADO</span><span class="sxs-lookup"><span data-stu-id="c62a5-116">ADO SQL Ranging Dialect</span></span>](ado-sql-ranging-dialect.md)
-   [<span data-ttu-id="c62a5-117">Exemplo de código para usar o intervalo para recuperar membros de um grupo</span><span class="sxs-lookup"><span data-stu-id="c62a5-117">Example Code for Using Ranging to Retrieve Members of a Group</span></span>](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




