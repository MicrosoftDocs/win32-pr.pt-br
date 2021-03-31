---
description: O predicado CONTAINS dá suporte ao uso do asterisco ( \* ) como um caractere curinga para representar palavras e frases. Você pode adicionar o asterisco somente no final da palavra ou frase. A presença do asterisco habilita o modo de correspondência de prefixo.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Usando caracteres curinga no predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090059"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a><span data-ttu-id="35fa1-105">Usando caracteres curinga no predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="35fa1-105">Using Wildcard Characters in the CONTAINS Predicate</span></span>

<span data-ttu-id="35fa1-106">O predicado CONTAINS dá suporte ao uso do asterisco ( \* ) como um caractere curinga para representar palavras e frases.</span><span class="sxs-lookup"><span data-stu-id="35fa1-106">The CONTAINS predicate supports the use of the asterisk (\*) as a wildcard character to represent words and phrases.</span></span> <span data-ttu-id="35fa1-107">Você pode adicionar o asterisco somente no final da palavra ou frase.</span><span class="sxs-lookup"><span data-stu-id="35fa1-107">You can add the asterisk only at the end of the word or phrase.</span></span> <span data-ttu-id="35fa1-108">A presença do asterisco habilita o modo de correspondência de prefixo.</span><span class="sxs-lookup"><span data-stu-id="35fa1-108">The presence of the asterisk enables the prefix-matching mode.</span></span> <span data-ttu-id="35fa1-109">Nesse modo, as correspondências serão retornadas se a coluna contiver a palavra de pesquisa especificada seguida por zero ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="35fa1-109">In this mode, matches are returned if the column contains the specified search word followed by zero or more other characters.</span></span> <span data-ttu-id="35fa1-110">Se uma frase for fornecida, as correspondências serão detectadas se a coluna contiver todas as palavras especificadas com zero ou mais caracteres após a palavra final.</span><span class="sxs-lookup"><span data-stu-id="35fa1-110">If a phrase is provided, matches are detected if the column contains all the specified words with zero or more other characters following the final word.</span></span>

## <a name="examples"></a><span data-ttu-id="35fa1-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="35fa1-111">Examples</span></span>

<span data-ttu-id="35fa1-112">O primeiro exemplo corresponde a documentos que têm qualquer palavra na coluna FileName que começa com "serv".</span><span class="sxs-lookup"><span data-stu-id="35fa1-112">The first example matches documents that have any word in the FileName column beginning with "serv".</span></span> <span data-ttu-id="35fa1-113">Exemplos de palavras correspondentes incluem "servidor", "servidores" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="35fa1-113">Example matching words include "server", "servers", and "service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



<span data-ttu-id="35fa1-114">O segundo exemplo corresponde a documentos com qualquer frase na coluna FileName que começa com "comp" e na qual a próxima palavra começa com "serv".</span><span class="sxs-lookup"><span data-stu-id="35fa1-114">The second example matches documents with any phrase in the FileName column that begins with "comp" and in which the next word begins with "serv".</span></span> <span data-ttu-id="35fa1-115">Exemplos de palavras de correspondência incluem "servidor de comp", "servidores de comp" e "serviço de comp".</span><span class="sxs-lookup"><span data-stu-id="35fa1-115">Example matching words include "comp server", "comp servers", and "comp service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



<span data-ttu-id="35fa1-116">O asterisco só funciona para correspondência de prefixo e pode ser posicionado somente no final da palavra ou frase; Ele não funciona para correspondência de sufixo.</span><span class="sxs-lookup"><span data-stu-id="35fa1-116">The asterisk works only for prefix-matching and can be placed only at the end of the word or phrase; it does not work for suffix-matching.</span></span> <span data-ttu-id="35fa1-117">A sintaxe a seguir não é válida e não corresponde a documentos com nenhuma palavra na coluna FileName que termina com "servi".</span><span class="sxs-lookup"><span data-stu-id="35fa1-117">The following syntax is not valid and does not match documents with any word in the FileName column ending with "serve".</span></span>


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a><span data-ttu-id="35fa1-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35fa1-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="35fa1-119">**Referência**</span><span class="sxs-lookup"><span data-stu-id="35fa1-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35fa1-120">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="35fa1-120">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="35fa1-121">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="35fa1-121">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



