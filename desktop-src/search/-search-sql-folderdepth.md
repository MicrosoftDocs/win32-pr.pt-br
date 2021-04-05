---
description: Predicados de profundidade de pasta controlam o escopo de uma pesquisa especificando um caminho e se devem ser executadas uma passagem profunda ou superficial.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Predicados de escopo e diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090070"
---
# <a name="scope-and-directory-predicates"></a><span data-ttu-id="46884-103">Predicados de escopo e diretório</span><span class="sxs-lookup"><span data-stu-id="46884-103">SCOPE and DIRECTORY Predicates</span></span>

<span data-ttu-id="46884-104">Predicados de profundidade de pasta controlam o escopo de uma pesquisa especificando um caminho e se devem ser executadas uma passagem profunda ou superficial.</span><span class="sxs-lookup"><span data-stu-id="46884-104">Folder depth predicates control the scope of a search by specifying a path and whether to perform a deep or shallow traversal.</span></span> <span data-ttu-id="46884-105">O seguinte mostra a sintaxe dos predicados de profundidade de pasta:</span><span class="sxs-lookup"><span data-stu-id="46884-105">The following shows the syntax of the folder depth predicates:</span></span>


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



<span data-ttu-id="46884-106">O predicado é seguido por um sinal de igual.</span><span class="sxs-lookup"><span data-stu-id="46884-106">The predicate is followed by an equal sign.</span></span> <span data-ttu-id="46884-107">O caminho é revelado entre aspas simples e deve começar com um protocolo e dois-pontos (por exemplo,, `file:` `mapi:` ou `csc:` ).</span><span class="sxs-lookup"><span data-stu-id="46884-107">The path is exclosed in single quotes and must begin with a protocol and a colon (for example, `file:`, `mapi:`, or `csc:`).</span></span> <span data-ttu-id="46884-108">O predicado de escopo executa uma passagem profunda do caminho, incluindo todas as subpastas, enquanto o predicado de diretório faz uma passagem superficial apenas da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="46884-108">The SCOPE predicate performs a deep traversal of the path, including all subfolders, while the DIRECTORY predicate does a shallow traversal of only the folder specified.</span></span> <span data-ttu-id="46884-109">Assim como outras restrições de linguagem SQL (SQL), você pode especificar mais de uma restrição de profundidade de pasta em uma única consulta.</span><span class="sxs-lookup"><span data-stu-id="46884-109">Like other Structured Query Language (SQL) restrictions, you can specify more than one folder depth restriction in a single query.</span></span>

<span data-ttu-id="46884-110">Para consultar o catálogo local de um computador remoto, inclua o nome do computador antes do catálogo e um caminho UNC (Convenção de nomenclatura universal) no computador remoto na cláusula SCOPE ou DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="46884-110">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

## <a name="examples"></a><span data-ttu-id="46884-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46884-111">Examples</span></span>


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



<span data-ttu-id="46884-112">O primeiro exemplo de escopo pesquisa a pasta C: \\ files \\ reports e todas as suas subpastas.</span><span class="sxs-lookup"><span data-stu-id="46884-112">The first SCOPE example searches the C:\\Files\\Reports folder and all its subfolders.</span></span> <span data-ttu-id="46884-113">O exemplo de diretório pesquisa apenas a pasta raiz C: \\ files \\ reports.</span><span class="sxs-lookup"><span data-stu-id="46884-113">The DIRECTORY example searches only the root folder C:\\Files\\Reports.</span></span>

> [!Note]  
> <span data-ttu-id="46884-114">As barras invertidas do sistema de arquivos ( \\ ) tornam-se marcas de barras de estilo de URL (às vezes chamadas de barras "/)".</span><span class="sxs-lookup"><span data-stu-id="46884-114">The file system backslashes (\\) become a URL-style slash marks (sometimes called forward slashes) (/).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="46884-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46884-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="46884-116">**Referência**</span><span class="sxs-lookup"><span data-stu-id="46884-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="46884-117">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="46884-117">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="46884-118">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="46884-118">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



