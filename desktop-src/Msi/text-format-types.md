---
description: Os tipos de formato de texto de dados configuráveis podem ser cadeias de caracteres de texto de qualquer comprimento. Nulos inseridos não são permitidos.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Tipos de formato de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748566"
---
# <a name="text-format-types"></a><span data-ttu-id="29bad-104">Tipos de formato de texto</span><span class="sxs-lookup"><span data-stu-id="29bad-104">Text Format Types</span></span>

<span data-ttu-id="29bad-105">Os tipos de formato de texto de dados configuráveis podem ser cadeias de caracteres de texto de qualquer comprimento.</span><span class="sxs-lookup"><span data-stu-id="29bad-105">The text format types of configurable data may be text strings of any length.</span></span> <span data-ttu-id="29bad-106">Nulos inseridos não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="29bad-106">Embedded nulls are not allowed.</span></span>

<span data-ttu-id="29bad-107">Existem os seguintes tipos de formato de texto:</span><span class="sxs-lookup"><span data-stu-id="29bad-107">The following Text Format types exist:</span></span>

[<span data-ttu-id="29bad-108">Texto arbitrário</span><span class="sxs-lookup"><span data-stu-id="29bad-108">Arbitrary Text</span></span>](arbitrary-text-type.md)

[<span data-ttu-id="29bad-109">RTF</span><span class="sxs-lookup"><span data-stu-id="29bad-109">RTF</span></span>](rtf-type.md)

[<span data-ttu-id="29bad-110">Binário</span><span class="sxs-lookup"><span data-stu-id="29bad-110">Formatted</span></span>](formatted-type.md)

[<span data-ttu-id="29bad-111">Enumeração</span><span class="sxs-lookup"><span data-stu-id="29bad-111">Enum</span></span>](enum-type.md)

[<span data-ttu-id="29bad-112">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="29bad-112">Identifier Type</span></span>](identifier-type.md)

<span data-ttu-id="29bad-113">Os itens configuráveis do tipo de formato de texto são usados em campos de banco de dados não binários e, em geral, podem ser substituídos por qualquer cadeia de caracteres de qualquer comprimento.</span><span class="sxs-lookup"><span data-stu-id="29bad-113">Configurable items of the Text Format Type are used in non-binary database fields and in general could be replaced by any string of any length.</span></span> <span data-ttu-id="29bad-114">No entanto, determinados itens configuráveis também têm restrições semânticas.</span><span class="sxs-lookup"><span data-stu-id="29bad-114">However, particular configurable items also have semantic restrictions.</span></span> <span data-ttu-id="29bad-115">Por exemplo, um item configurável que é necessário para ser uma chave estrangeira em uma tabela específica tem restrições semânticas adicionais.</span><span class="sxs-lookup"><span data-stu-id="29bad-115">For example, a configurable item that is required to be a foreign key into a specific table has additional semantic restrictions.</span></span> <span data-ttu-id="29bad-116">Essas restrições semânticas não são impostas por Mergemod.dll e, portanto, os autores de módulo devem estar preparados para lidar com qualquer cadeia de caracteres que satisfaça o tipo de formato de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="29bad-116">Such semantic restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Text Format type.</span></span>

 

 



