---
description: Os tipos de formato de chave de dados configuráveis podem ser usados em campos de texto para fornecer uma chave para uma tabela de banco de dado.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Tipos de formato de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770194"
---
# <a name="key-format-types"></a><span data-ttu-id="5fb22-103">Tipos de formato de chave</span><span class="sxs-lookup"><span data-stu-id="5fb22-103">Key Format Types</span></span>

<span data-ttu-id="5fb22-104">Os tipos de formato de chave de dados configuráveis podem ser usados em campos de texto para fornecer uma chave para uma tabela de banco de dado.</span><span class="sxs-lookup"><span data-stu-id="5fb22-104">The Key Format Types of configurable data may be used in text fields to provide a key into a database table.</span></span> <span data-ttu-id="5fb22-105">O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido.</span><span class="sxs-lookup"><span data-stu-id="5fb22-105">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="5fb22-106">NULL nunca é um valor válido para este tipo.</span><span class="sxs-lookup"><span data-stu-id="5fb22-106">Null is never a valid value for this type.</span></span> <span data-ttu-id="5fb22-107">As respostas a todos os itens de formato de chave devem estar no [formato especial CMSM](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="5fb22-107">Responses to all Key format items must be in [CMSM Special Format](cmsm-special-format.md).</span></span>

<span data-ttu-id="5fb22-108">Existem os seguintes tipos de formato de chave:</span><span class="sxs-lookup"><span data-stu-id="5fb22-108">The following Key Format types exist:</span></span>

[<span data-ttu-id="5fb22-109">Tipo de diretório</span><span class="sxs-lookup"><span data-stu-id="5fb22-109">Directory Type</span></span>](directory-type.md)

[<span data-ttu-id="5fb22-110">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="5fb22-110">File Type</span></span>](file-type.md)

[<span data-ttu-id="5fb22-111">Tipo de propriedade</span><span class="sxs-lookup"><span data-stu-id="5fb22-111">Property Type</span></span>](property-type.md)

[<span data-ttu-id="5fb22-112">Tipo de caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="5fb22-112">Dialog Type</span></span>](dialog-type.md)

[<span data-ttu-id="5fb22-113">Tipo de binário</span><span class="sxs-lookup"><span data-stu-id="5fb22-113">Binary Type</span></span>](binary-type.md)

[<span data-ttu-id="5fb22-114">Tipo de ícone</span><span class="sxs-lookup"><span data-stu-id="5fb22-114">Icon Type</span></span>](icon-type.md)

<span data-ttu-id="5fb22-115">Os itens configuráveis do tipo de formato de chave são usados em colunas de texto para fornecer uma chave de banco de dados e, em geral, podem ser substituídos por qualquer cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="5fb22-115">Configurable items of the Key Format Type are used in text columns to provide a database key and in general could be replaced by any text string.</span></span> <span data-ttu-id="5fb22-116">Os tipos individuais podem ter restrições sintáticas adicionais, mas essas restrições não são impostas pelo Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="5fb22-116">The individual types may have additional syntactic restrictions, but these restrictions are not enforced by Mergemod.dll.</span></span> <span data-ttu-id="5fb22-117">Determinados itens configuráveis também podem ter restrições semânticas de características.</span><span class="sxs-lookup"><span data-stu-id="5fb22-117">Particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="5fb22-118">Por exemplo, um determinado item configurável pode precisar ser uma chave na [tabela binária](binary-table.md) para uma linha que contém uma imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="5fb22-118">For example, a particular configurable item may be required to be a key into the [Binary table](binary-table.md) to a row containing a bitmap image.</span></span> <span data-ttu-id="5fb22-119">Essas restrições não são impostas por Mergemod.dll e, portanto, os autores de módulo devem estar preparados para lidar com qualquer cadeia de caracteres que satisfaça o tipo de formato de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="5fb22-119">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Key Format type.</span></span> <span data-ttu-id="5fb22-120">A menos que especificado de outra forma por significado semântico ou atributos, NULL é uma resposta válida.</span><span class="sxs-lookup"><span data-stu-id="5fb22-120">Unless otherwise specified by semantic meaning or attributes, null is a valid response.</span></span>

 

 



