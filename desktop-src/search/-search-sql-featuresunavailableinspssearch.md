---
description: A linguagem de consulta do Microsoft Windows Search baseia-se em linguagem SQL (SQL); no entanto, ele não pesquisa em um banco de dados relacional com tabelas ou índices definidos pelo usuário.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Recursos do SQL não disponíveis no Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793629"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a><span data-ttu-id="79cf0-103">Recursos do SQL não disponíveis no Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="79cf0-103">SQL Features Unavailable in Microsoft Windows Search</span></span>

<span data-ttu-id="79cf0-104">A linguagem de consulta do Microsoft Windows Search baseia-se em linguagem SQL (SQL); no entanto, ele não pesquisa em um banco de dados relacional com tabelas ou índices definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="79cf0-104">Microsoft Windows Search query language is based on Structured Query Language (SQL); however, it does not search in a relational database with user-defined tables or indexes.</span></span> <span data-ttu-id="79cf0-105">Por isso, muitas instruções SQL padrão e recursos de sintaxe não se aplicam.</span><span class="sxs-lookup"><span data-stu-id="79cf0-105">Because of this, many standard SQL statements and syntax features do not apply.</span></span> <span data-ttu-id="79cf0-106">A seguir está uma lista dos recursos SQL mais significativos que não têm suporte no Windows Search.</span><span class="sxs-lookup"><span data-stu-id="79cf0-106">The following is a list of the more significant SQL features that are not supported in Windows Search.</span></span>


-   <span data-ttu-id="79cf0-107">Instruções de lote</span><span class="sxs-lookup"><span data-stu-id="79cf0-107">BATCH statements</span></span>
-   <span data-ttu-id="79cf0-108">Função de \_ tabela de adesão</span><span class="sxs-lookup"><span data-stu-id="79cf0-108">COALESCE\_TABLE function</span></span>
-   <span data-ttu-id="79cf0-109">Função CONVERT (use as funções CAST em vez disso)</span><span class="sxs-lookup"><span data-stu-id="79cf0-109">CONVERT function (use the CAST functions instead)</span></span>
-   <span data-ttu-id="79cf0-110">instrução CREATE VIEW</span><span class="sxs-lookup"><span data-stu-id="79cf0-110">CREATE VIEW statement</span></span>
-   <span data-ttu-id="79cf0-111">Linguagem de definição de dados</span><span class="sxs-lookup"><span data-stu-id="79cf0-111">Data definition language</span></span>
-   <span data-ttu-id="79cf0-112">Instrução DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="79cf0-112">DATASOURCE statement</span></span>
-   <span data-ttu-id="79cf0-113">Formatos de data e hora diferentes de data e hora ISO</span><span class="sxs-lookup"><span data-stu-id="79cf0-113">Date and Time formats other than ISO date and time stamp</span></span>
-   <span data-ttu-id="79cf0-114">Instrução DELETE</span><span class="sxs-lookup"><span data-stu-id="79cf0-114">DELETE statement</span></span>
-   <span data-ttu-id="79cf0-115">instrução GRANT</span><span class="sxs-lookup"><span data-stu-id="79cf0-115">GRANT statement</span></span>
-   <span data-ttu-id="79cf0-116">Esquema de informações</span><span class="sxs-lookup"><span data-stu-id="79cf0-116">Information schema</span></span>
-   <span data-ttu-id="79cf0-117">Instrução INSERT</span><span class="sxs-lookup"><span data-stu-id="79cf0-117">INSERT statement</span></span>
-   <span data-ttu-id="79cf0-118">Tipos de dados OLE DB</span><span class="sxs-lookup"><span data-stu-id="79cf0-118">OLE DB data types</span></span>
-   <span data-ttu-id="79cf0-119">SQL-expressões regulares padrão (use CONTAINS ou LIKE em vez disso)</span><span class="sxs-lookup"><span data-stu-id="79cf0-119">SQL-standard regular expressions (use CONTAINS or LIKE instead)</span></span>
-   <span data-ttu-id="79cf0-120">Parâmetros para consultas SQL</span><span class="sxs-lookup"><span data-stu-id="79cf0-120">Parameters to SQL queries</span></span>
-   <span data-ttu-id="79cf0-121">Comparação de coluna relacional</span><span class="sxs-lookup"><span data-stu-id="79cf0-121">Relational column comparison</span></span>
-   <span data-ttu-id="79cf0-122">Cabeçalho da ID de revisão</span><span class="sxs-lookup"><span data-stu-id="79cf0-122">Revision ID header</span></span>
-   <span data-ttu-id="79cf0-123">instrução REVOKE</span><span class="sxs-lookup"><span data-stu-id="79cf0-123">REVOKE statement</span></span>
-   <span data-ttu-id="79cf0-124">Aliases de escopo ou números de revisão</span><span class="sxs-lookup"><span data-stu-id="79cf0-124">SCOPE aliases or revision numbers</span></span>
-   <span data-ttu-id="79cf0-125">SELECIONAR tudo (remove duplicatas automaticamente)</span><span class="sxs-lookup"><span data-stu-id="79cf0-125">SELECT ALL (removes duplicates automatically)</span></span>
-   <span data-ttu-id="79cf0-126">Procedimentos armazenados</span><span class="sxs-lookup"><span data-stu-id="79cf0-126">Stored procedures</span></span>
-   <span data-ttu-id="79cf0-127">Expansão de documento estruturado</span><span class="sxs-lookup"><span data-stu-id="79cf0-127">Structured document expansion</span></span>
-   <span data-ttu-id="79cf0-128">TODOS UNION</span><span class="sxs-lookup"><span data-stu-id="79cf0-128">UNION ALL</span></span>
-   <span data-ttu-id="79cf0-129">Palavra-chave desconhecida</span><span class="sxs-lookup"><span data-stu-id="79cf0-129">UNKNOWN keyword</span></span>
-   <span data-ttu-id="79cf0-130">Instrução UPDATE</span><span class="sxs-lookup"><span data-stu-id="79cf0-130">UPDATE statement</span></span>

<span data-ttu-id="79cf0-131">O Windows Search não dá suporte a palavras de dicionário de sinônimos e de ruído.</span><span class="sxs-lookup"><span data-stu-id="79cf0-131">Windows Search does not support Thesaurus and Noise Words.</span></span>

 

 



