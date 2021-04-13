---
description: O WMI usa caminhos de objeto nas propriedades de referência de classes de associação para identificar objetos relacionados, bem como usar caminhos de objeto em parâmetros de entrada ou saída para vários métodos.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Requisitos de caminho do objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370675"
---
# <a name="wmi-object-path-requirements"></a><span data-ttu-id="af322-103">Requisitos de caminho do objeto WMI</span><span class="sxs-lookup"><span data-stu-id="af322-103">WMI Object Path Requirements</span></span>

<span data-ttu-id="af322-104">O WMI usa caminhos de objeto nas propriedades de referência de classes de associação para identificar objetos relacionados, bem como usar caminhos de objeto em parâmetros de entrada ou saída para vários métodos.</span><span class="sxs-lookup"><span data-stu-id="af322-104">WMI uses object paths in the reference properties of association classes to identify related objects, as well as using object paths in input or output parameters for several methods.</span></span> <span data-ttu-id="af322-105">Como os caminhos de objeto são tratados como cadeias de caracteres para fins de pesquisa e comparação, o valor de um caminho de objeto quando usado como uma propriedade de referência é sempre a própria cadeia de caracteres e não o objeto desreferenciado.</span><span class="sxs-lookup"><span data-stu-id="af322-105">Because object paths are treated as strings for the purpose of lookup and comparison, the value of an object path when used as a reference property is always the string itself and not the dereferenced object.</span></span> <span data-ttu-id="af322-106">Comparações de cadeias de caracteres que lidam com caminhos de objeto sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="af322-106">String comparisons that deal with object paths are always case-insensitive.</span></span>

<span data-ttu-id="af322-107">Um caminho de objeto pode usar a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="af322-107">An object path can use the following syntax:</span></span>

-   <span data-ttu-id="af322-108">Cadeias de caracteres contidas entre aspas simples.</span><span class="sxs-lookup"><span data-stu-id="af322-108">Strings contained in single quotation marks.</span></span>
-   <span data-ttu-id="af322-109">Redirecionar barras como separadores.</span><span class="sxs-lookup"><span data-stu-id="af322-109">Forward slashes as separators.</span></span>
-   <span data-ttu-id="af322-110">Barras invertidas como separadores.</span><span class="sxs-lookup"><span data-stu-id="af322-110">Backslashes as separators.</span></span>
-   <span data-ttu-id="af322-111">Constantes hexadecimais para inteiros.</span><span class="sxs-lookup"><span data-stu-id="af322-111">Hexadecimal constants for integers.</span></span>
-   <span data-ttu-id="af322-112">Constantes booleanas para classes com chaves que usam valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="af322-112">Boolean constants for classes with keys that take Boolean values.</span></span>
-   <span data-ttu-id="af322-113">Notação de URL para representar caracteres não imprimíveis, como %20 para um espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="af322-113">URL notation to represent nonprinting characters, such as %20 for a blank space.</span></span>

<span data-ttu-id="af322-114">Além disso, uma cadeia de caracteres de caminho de objeto deve obedecer às seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="af322-114">In addition, an object path string must obey the following restrictions:</span></span>

-   <span data-ttu-id="af322-115">Um servidor local assumido com um caminho de namespace parcial.</span><span class="sxs-lookup"><span data-stu-id="af322-115">An assumed local server with a partial namespace path.</span></span> <span data-ttu-id="af322-116">Assim, especificar a raiz e o namespace padrão implica a raiz e o namespace padrão no servidor local.</span><span class="sxs-lookup"><span data-stu-id="af322-116">Thus, specifying the root and default namespace implies the root and default namespace on the local server.</span></span>
-   <span data-ttu-id="af322-117">Não há espaço em branco dentro de um elemento ou entre elementos.</span><span class="sxs-lookup"><span data-stu-id="af322-117">No white space either within an element or between elements.</span></span>
-   <span data-ttu-id="af322-118">Aspas inseridas em caminhos de objeto são permitidas, mas devem delimitar as aspas com caracteres de escape, como em um aplicativo C ou C++.</span><span class="sxs-lookup"><span data-stu-id="af322-118">Embedded quotation marks in object paths are allowed but must delimit the quotation mark with escape characters, as in a C or C++ application.</span></span>
-   <span data-ttu-id="af322-119">Somente valores decimais são reconhecidos como partes numéricas de chaves.</span><span class="sxs-lookup"><span data-stu-id="af322-119">Only decimal values are recognized as numeric portions of keys.</span></span>

 

 



