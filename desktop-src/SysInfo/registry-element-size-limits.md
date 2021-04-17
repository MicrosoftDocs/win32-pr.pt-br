---
description: A tabela a seguir identifica os limites de tamanho para os vários elementos do registro.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Limites de tamanho de elemento do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749190"
---
# <a name="registry-element-size-limits"></a><span data-ttu-id="68386-103">Limites de tamanho de elemento do registro</span><span class="sxs-lookup"><span data-stu-id="68386-103">Registry Element Size Limits</span></span>

<span data-ttu-id="68386-104">A tabela a seguir identifica os limites de tamanho para os vários elementos do registro.</span><span class="sxs-lookup"><span data-stu-id="68386-104">The following table identifies the size limits for the various registry elements.</span></span>



| <span data-ttu-id="68386-105">Elemento do registro</span><span class="sxs-lookup"><span data-stu-id="68386-105">Registry Element</span></span> | <span data-ttu-id="68386-106">Limite de tamanho</span><span class="sxs-lookup"><span data-stu-id="68386-106">Size Limit</span></span>                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68386-107">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="68386-107">Key name</span></span>         | <span data-ttu-id="68386-108">255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="68386-108">255 characters.</span></span> <span data-ttu-id="68386-109">O nome da chave inclui o caminho absoluto da chave no registro, sempre Iniciando em uma chave base, por exemplo, HKEY \_ local \_ Machine.</span><span class="sxs-lookup"><span data-stu-id="68386-109">The key name includes the absolute path of the key in the registry, always starting at a base key, for example, HKEY\_LOCAL\_MACHINE.</span></span> |
| <span data-ttu-id="68386-110">Nome do valor</span><span class="sxs-lookup"><span data-stu-id="68386-110">Value name</span></span>       | <span data-ttu-id="68386-111">16.383 caracteres **Windows 2000:** 260 caracteres ANSI ou 16.383 caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="68386-111">16,383 characters **Windows 2000:** 260 ANSI characters or 16,383 Unicode characters.</span></span><br/>                                                       |
| <span data-ttu-id="68386-112">Valor</span><span class="sxs-lookup"><span data-stu-id="68386-112">Value</span></span>            | <span data-ttu-id="68386-113">Memória disponível (formato mais recente) 1 MB (formato padrão)</span><span class="sxs-lookup"><span data-stu-id="68386-113">Available memory (latest format)1 MB (standard format)</span></span><br/>                                                                                     |
| <span data-ttu-id="68386-114">Árvore</span><span class="sxs-lookup"><span data-stu-id="68386-114">Tree</span></span>             | <span data-ttu-id="68386-115">Uma árvore do registro pode ter 512 níveis de profundidade.</span><span class="sxs-lookup"><span data-stu-id="68386-115">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="68386-116">Você pode criar até 32 níveis por vez por meio de uma única chamada à API do registro.</span><span class="sxs-lookup"><span data-stu-id="68386-116">You can create up to 32 levels at a time through a single registry API call.</span></span>                                  |



 

<span data-ttu-id="68386-117">Valores longos (mais de 2.048 bytes) devem ser armazenados em um arquivo e o local do arquivo deve ser armazenado no registro.</span><span class="sxs-lookup"><span data-stu-id="68386-117">Long values (more than 2,048 bytes) should be stored in a file, and the location of the file should be stored in the registry.</span></span> <span data-ttu-id="68386-118">Isso ajuda o registro a ser executado com eficiência.</span><span class="sxs-lookup"><span data-stu-id="68386-118">This helps the registry perform efficiently.</span></span>

<span data-ttu-id="68386-119">O local do arquivo pode ser o nome de um valor ou os dados de um valor.</span><span class="sxs-lookup"><span data-stu-id="68386-119">The file location can be the name of a value or the data of a value.</span></span> <span data-ttu-id="68386-120">Cada barra invertida na cadeia de caracteres de localização deve ser precedida por outra barra invertida como um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="68386-120">Each backslash in the location string must be preceded by another backslash as an escape character.</span></span> <span data-ttu-id="68386-121">Por exemplo, especifique "C: \\ \\ mydir \\ \\ MyFile" para armazenar a cadeia de caracteres "c: \\ mydir \\ MyFile".</span><span class="sxs-lookup"><span data-stu-id="68386-121">For example, specify "C:\\\\mydir\\\\myfile" to store the string "C:\\mydir\\myfile".</span></span> <span data-ttu-id="68386-122">Um local de arquivo também pode ser o nome de uma chave se estiver dentro do limite de 255 caracteres para nomes de chave e não contiver barras invertidas, que não são permitidas em nomes de chave.</span><span class="sxs-lookup"><span data-stu-id="68386-122">A file location can also be the name of a key if it is within the 255-character limit for key names and does not contain backslashes, which are not allowed in key names.</span></span>

 

 




