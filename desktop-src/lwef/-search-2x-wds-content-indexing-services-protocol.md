---
title: Protocolo de serviços de indexação de conteúdo
description: Este documento é uma especificação do protocolo de serviço de indexação de conteúdo.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c22bbda912333368e50d3e4a8ace2cd98856ea
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103640330"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="c3012-103">Protocolo de serviços de indexação de conteúdo</span><span class="sxs-lookup"><span data-stu-id="c3012-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="c3012-104">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c3012-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c3012-105">Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c3012-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="c3012-106">Especificação de protocolo, versão 0,12</span><span class="sxs-lookup"><span data-stu-id="c3012-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="c3012-107">1 Introdução</span><span class="sxs-lookup"><span data-stu-id="c3012-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="c3012-108">1.1 Glossário</span><span class="sxs-lookup"><span data-stu-id="c3012-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="c3012-109">1.2 Referências</span><span class="sxs-lookup"><span data-stu-id="c3012-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="c3012-110">1,3 visão geral do protocolo (Sinopse)</span><span class="sxs-lookup"><span data-stu-id="c3012-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="c3012-111">1.4 Relacionamento com outros protocolos</span><span class="sxs-lookup"><span data-stu-id="c3012-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="c3012-112">1,5 pré-requisitos e pré-condições</span><span class="sxs-lookup"><span data-stu-id="c3012-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="c3012-113">1.6 Applicability Statement</span><span class="sxs-lookup"><span data-stu-id="c3012-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="c3012-114">1.7 Controle de versão e negociação de capacidade</span><span class="sxs-lookup"><span data-stu-id="c3012-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="c3012-115">1.8 Campos extensíveis para fornecedor</span><span class="sxs-lookup"><span data-stu-id="c3012-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="c3012-116">1.9 Atribuições standard</span><span class="sxs-lookup"><span data-stu-id="c3012-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="c3012-117">2 Mensagens</span><span class="sxs-lookup"><span data-stu-id="c3012-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="c3012-118">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="c3012-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="c3012-119">2.2 Sintaxe da mensagem</span><span class="sxs-lookup"><span data-stu-id="c3012-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="c3012-120">3 Detalhes do protocolo</span><span class="sxs-lookup"><span data-stu-id="c3012-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="c3012-121">3,1 detalhes do servidor</span><span class="sxs-lookup"><span data-stu-id="c3012-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="c3012-122">3,2 detalhes do cliente</span><span class="sxs-lookup"><span data-stu-id="c3012-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="c3012-123">4 Exemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="c3012-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="c3012-124">4,1 exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3012-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="c3012-125">4,2 exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3012-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="c3012-126">5 Segurança</span><span class="sxs-lookup"><span data-stu-id="c3012-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="c3012-127">5.1 Considerações de segurança para implementadores</span><span class="sxs-lookup"><span data-stu-id="c3012-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="c3012-128">5.2 Índice de parâmetros de segurança</span><span class="sxs-lookup"><span data-stu-id="c3012-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="c3012-129">6 índice de comportamento de versão específica</span><span class="sxs-lookup"><span data-stu-id="c3012-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="c3012-130">Este documento é uma especificação do protocolo de serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c3012-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="c3012-131">A documentação do WSPP (programa de protocolo de servidor de grupo de trabalho) destina-se ao uso em conjunto com a documentação de padrões públicos, a arte de programação de rede e os conceitos de sistemas distribuídos do Windows Workgroup e pressupõe que o leitor esteja familiarizado com o material mencionado anteriormente ou tenha acesso imediato a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="c3012-132">Uma especificação de protocolo WSPP não requer o uso de ferramentas de programação da Microsoft ou de ambientes de programação para que um licenciado desenvolva uma implementação.</span><span class="sxs-lookup"><span data-stu-id="c3012-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="c3012-133">Os licenciados que têm acesso a ambientes e ferramentas de programação da Microsoft são gratuitos para se beneficiar deles.</span><span class="sxs-lookup"><span data-stu-id="c3012-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="c3012-134">1 Introdução</span><span class="sxs-lookup"><span data-stu-id="c3012-134">1 Introduction</span></span>

-   [<span data-ttu-id="c3012-135">1.1 Glossário</span><span class="sxs-lookup"><span data-stu-id="c3012-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="c3012-136">1.2 Referências</span><span class="sxs-lookup"><span data-stu-id="c3012-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="c3012-137">1,3 visão geral do protocolo (Sinopse)</span><span class="sxs-lookup"><span data-stu-id="c3012-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="c3012-138">1.4 Relacionamento com outros protocolos</span><span class="sxs-lookup"><span data-stu-id="c3012-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="c3012-139">1,5 pré-requisitos e pré-condições</span><span class="sxs-lookup"><span data-stu-id="c3012-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="c3012-140">1.6 Applicability Statement</span><span class="sxs-lookup"><span data-stu-id="c3012-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="c3012-141">1.7 Controle de versão e negociação de capacidade</span><span class="sxs-lookup"><span data-stu-id="c3012-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="c3012-142">1.8 Campos extensíveis para fornecedor</span><span class="sxs-lookup"><span data-stu-id="c3012-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="c3012-143">1.9 Atribuições standard</span><span class="sxs-lookup"><span data-stu-id="c3012-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="c3012-144">1.1 Glossário</span><span class="sxs-lookup"><span data-stu-id="c3012-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="c3012-145">Os termos a seguir são definidos na seção Glossário do \[ MS-sys \] :</span><span class="sxs-lookup"><span data-stu-id="c3012-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="c3012-146">GUID</span><span class="sxs-lookup"><span data-stu-id="c3012-146">GUID</span></span>
> -   <span data-ttu-id="c3012-147">Little endian</span><span class="sxs-lookup"><span data-stu-id="c3012-147">Little Endian</span></span>
> -   <span data-ttu-id="c3012-148">Pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="c3012-148">Named Pipe</span></span>
> -   <span data-ttu-id="c3012-149">Caminho</span><span class="sxs-lookup"><span data-stu-id="c3012-149">Path</span></span>

 

<span data-ttu-id="c3012-150">**Binding**: uma solicitação para incluir uma **coluna** específica em um **conjunto de linhas** retornado.</span><span class="sxs-lookup"><span data-stu-id="c3012-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="c3012-151">A **Associação** especifica uma propriedade a ser incluída nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3012-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="c3012-152">**Indicador**: um marcador que identifica exclusivamente uma linha dentro de um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="c3012-153">**Catálogo**: a unidade de nível mais alto da organização no serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="c3012-154">Ele representa um conjunto de documentos indexados em relação a quais consultas podem ser executadas usando o protocolo de serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c3012-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="c3012-155">**Categoria**: um agrupamento hierárquico de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="c3012-156">Por exemplo, um resultado de consulta contendo colunas de autor e título pode ser categorizado com base no autor.</span><span class="sxs-lookup"><span data-stu-id="c3012-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="c3012-157">Cada grupo de linhas que contém o mesmo valor para o autor constituiria uma categoria.</span><span class="sxs-lookup"><span data-stu-id="c3012-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="c3012-158">**Capítulo** : um intervalo de **linhas** dentro de um conjunto de **linhas** .</span><span class="sxs-lookup"><span data-stu-id="c3012-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="c3012-159">**Column**: o contêiner para um único tipo de informação em uma **linha** .</span><span class="sxs-lookup"><span data-stu-id="c3012-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="c3012-160">As colunas são mapeadas para nomes de propriedade e especifica quais propriedades são usadas para os elementos de **árvore** de **comando** da consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3012-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="c3012-161">**Árvore de comandos**: uma combinação **de restrições** , **categorias** e **ordens de classificação** especificadas para a consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3012-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="c3012-162">**Cursor**: uma entidade que é usada como um mecanismo para trabalhar com uma **linha** ou um pequeno bloco de **linhas** por vez em um conjunto de dados retornado em um conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c3012-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="c3012-163">Um **cursor** é posicionado em uma única **linha** dentro do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c3012-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="c3012-164">Depois que o **cursor** é posicionado em uma linha, as operações podem ser executadas nessa **linha** ou em um bloco de **linhas** que começam nessa posição.</span><span class="sxs-lookup"><span data-stu-id="c3012-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="c3012-165">**Identificador**: um token que pode ser usado para identificar e acessar **cursores** , **capítulos** e **indicadores** .</span><span class="sxs-lookup"><span data-stu-id="c3012-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="c3012-166">**Índice**: uma estrutura persistente que contém o conteúdo de texto extraído de arquivos por um **serviço de indexação** .</span><span class="sxs-lookup"><span data-stu-id="c3012-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="c3012-167">Isso inclui a lista de palavras, que são armazenadas junto com o nome do arquivo contido, o local do Word e a **localidade** .</span><span class="sxs-lookup"><span data-stu-id="c3012-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="c3012-168">**Indexação**: o processo de extração de texto e propriedades de arquivos e armazenamento dos valores extraídos nos **índices** (para texto) e o **cache de propriedades** (para propriedades).</span><span class="sxs-lookup"><span data-stu-id="c3012-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="c3012-169">**Serviço de indexação**: um serviço que cria **catálogos** indexados para o conteúdo e as propriedades dos sistemas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c3012-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="c3012-170">Os aplicativos podem pesquisar os catálogos em busca de informações dos arquivos no sistema de arquivos indexado.</span><span class="sxs-lookup"><span data-stu-id="c3012-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="c3012-171">**Localidade**: um identificador, conforme especificado no \[ Apêndice a MS-GPSI \] , que especifica as preferências relacionadas ao idioma.</span><span class="sxs-lookup"><span data-stu-id="c3012-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="c3012-172">Essas preferências indicam como as datas e horas devem ser formatadas, os itens devem ser classificados alfabeticamente, as cadeias de caracteres devem ser comparadas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c3012-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="c3012-173">**Consulta de linguagem natural**: uma consulta construída usando o idioma humano em vez da sintaxe de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="c3012-174">**Palavra de ruído**: uma palavra que é ignorada pelo serviço de indexação quando presente nas **restrições** especificadas para a consulta de pesquisa porque ela tem pouco valor de discriminador.</span><span class="sxs-lookup"><span data-stu-id="c3012-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="c3012-175">Os exemplos em inglês incluem "a", "e" e "o".</span><span class="sxs-lookup"><span data-stu-id="c3012-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="c3012-176">**Cache de propriedades**: um cache de propriedades de arquivo extraído por um **serviço de indexação** .</span><span class="sxs-lookup"><span data-stu-id="c3012-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="c3012-177">**Indexação de propriedade**: o processo de criação de um **índice** de propriedades de **tipo de valor** de um documento, incluindo autor, assunto, tipo, contagem de palavras, contagem de páginas impressa e outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3012-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="c3012-178">**Restrição**: um conjunto de condições que um arquivo deve atender para ser incluído nos resultados da pesquisa retornados pelo **serviço de indexação** em resposta a uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3012-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="c3012-179">Uma **restrição** reduz o foco de uma consulta de pesquisa, limitando os arquivos que o **serviço de indexação** incluirá nos resultados da pesquisa apenas àqueles que correspondem às condições.</span><span class="sxs-lookup"><span data-stu-id="c3012-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="c3012-180">**Row**: a coleção de **colunas** , que contém os valores de propriedade que descrevem um único arquivo do conjunto de arquivos que correspondeu às **restrições** especificadas na consulta de pesquisa enviada ao **serviço de indexação** .</span><span class="sxs-lookup"><span data-stu-id="c3012-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="c3012-181">**Conjunto de linhas**: um conjunto de **linhas** retornadas nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3012-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="c3012-182">**Ordem de classificação**: o conjunto de regras em uma consulta de pesquisa que define a ordenação de linhas no resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3012-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="c3012-183">Cada regra consiste em uma propriedade (nome, tamanho, etc.) e uma direção para a ordenação (crescente ou decrescente).</span><span class="sxs-lookup"><span data-stu-id="c3012-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="c3012-184">Várias regras são aplicadas sequencialmente</span><span class="sxs-lookup"><span data-stu-id="c3012-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="c3012-185">**Propriedade de tipo de texto**: uma propriedade que descreve o conteúdo de um documento e só tem texto não formatado associado ao seu nome.</span><span class="sxs-lookup"><span data-stu-id="c3012-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="c3012-186">**Propriedade de tipo de valor**: uma propriedade que descreve um único atributo de um documento inteiro.</span><span class="sxs-lookup"><span data-stu-id="c3012-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="c3012-187">Uma propriedade de tipo de valor tem uma ID de tipo de dados e um valor desse tipo de dados associado ao seu nome.</span><span class="sxs-lookup"><span data-stu-id="c3012-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="c3012-188">**Raiz virtual**: um caminho alternativo para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="c3012-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="c3012-189">Uma pasta física pode ter zero ou mais raízes virtuais.</span><span class="sxs-lookup"><span data-stu-id="c3012-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="c3012-190">Caminhos que começam com uma raiz virtual são chamados de caminhos virtuais.</span><span class="sxs-lookup"><span data-stu-id="c3012-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="c3012-191">Por exemplo,/Server/vanityroot pode ser uma raiz virtual de C: \\ IIS \\ Web \\ Pasta1.</span><span class="sxs-lookup"><span data-stu-id="c3012-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="c3012-192">Em seguida, o arquivo C: \\ IIS \\ web \\ Pasta1 \\default.htm teria um caminho virtual de/Server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="c3012-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="c3012-193">**Maio, deveria**, deve, não, não deve: estes termos (em todos os limites) são usados conforme descrito em \[ RFC2119 \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="c3012-194">Todas as instruções de comportamento opcional utilizam PODE, DEVERIA OU NÃO DEVERIA.</span><span class="sxs-lookup"><span data-stu-id="c3012-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="c3012-195">1.2 Referências</span><span class="sxs-lookup"><span data-stu-id="c3012-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="c3012-196">1.2.1 Referências normativas</span><span class="sxs-lookup"><span data-stu-id="c3012-196">1.2.1 Normative References</span></span>

<span data-ttu-id="c3012-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "padrão para Binary Floating-Point aritmético", IEEE 754-1985, outubro de 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="c3012-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="c3012-198">\[MS-DCOM \] Microsoft Corporation, "distribuído Component Object Model protocolos remotos", junho de 2006.</span><span class="sxs-lookup"><span data-stu-id="c3012-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="c3012-199">\[MS-GPSI \] Microsoft Corporation, "extensão de política de grupo de instalação de software", junho de 2006.</span><span class="sxs-lookup"><span data-stu-id="c3012-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="c3012-200">\[MS-SMB \] Microsoft Corporation, "protocolo e extensões do Microsoft Server Message Block (SMB)", maio de 2006.</span><span class="sxs-lookup"><span data-stu-id="c3012-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="c3012-201">\[MS-SYS \] Microsoft Corporation, "visão geral do sistema v4", julho de 2006.</span><span class="sxs-lookup"><span data-stu-id="c3012-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="c3012-202">\[Sale \] saltize, G., "processamento de texto automático: a análise de transformação e a recuperação de informações por computador", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="c3012-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="c3012-203">\[UNICODE \] consórcio Unicode, "o padrão Unicode, versão 2,0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="c3012-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="c3012-204">1.2.2 Referências informativas</span><span class="sxs-lookup"><span data-stu-id="c3012-204">1.2.2 Informative References</span></span>

<span data-ttu-id="c3012-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="c3012-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="c3012-206">\[MSDN-QUERYERR \] Microsoft Corporation, valores de Query-Execution, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="c3012-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="c3012-207">1,3 visão geral do protocolo (Sinopse)</span><span class="sxs-lookup"><span data-stu-id="c3012-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="c3012-208">Um **serviço de indexação** de conteúdo ajuda a organizar com eficiência os recursos extraídos de uma coleção de documentos.</span><span class="sxs-lookup"><span data-stu-id="c3012-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="c3012-209">O CISP (Content Indexing Service Protocol) permite que um cliente se comunique com um servidor que hospeda um serviço de indexação para emitir consultas e permitir que um administrador gerencie o servidor de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="c3012-210">Ao processar arquivos, um serviço de indexação analisa um conjunto de documentos e reorganiza seu conteúdo de forma que **as propriedades** desses documentos possam ser retornadas de forma eficiente em resposta a consultas.</span><span class="sxs-lookup"><span data-stu-id="c3012-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="c3012-211">Uma coleção de documentos que podem ser consultados abrange um **Catálogo** .</span><span class="sxs-lookup"><span data-stu-id="c3012-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="c3012-212">Um catálogo pode conter um **índice** (para referência rápida a texto) e um **cache de propriedades** (para recuperação rápida de valores de propriedade).</span><span class="sxs-lookup"><span data-stu-id="c3012-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="c3012-213">Conceitualmente, um catálogo consiste em uma "tabela" lógica de propriedades com o texto ou o valor e a localidade correspondente armazenada em **colunas** da tabela.</span><span class="sxs-lookup"><span data-stu-id="c3012-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="c3012-214">Cada "linha" da tabela corresponde a um documento separado no escopo do catálogo e cada "coluna" da tabela corresponde a uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="c3012-215">As tarefas específicas executadas pelo CISP são agrupadas em duas áreas funcionais:</span><span class="sxs-lookup"><span data-stu-id="c3012-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="c3012-216">Administração remota da indexação de catálogos de serviço,</span><span class="sxs-lookup"><span data-stu-id="c3012-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="c3012-217">Consulta remota de catálogos de serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="c3012-218">Tarefas de administração remota do 1.3.1</span><span class="sxs-lookup"><span data-stu-id="c3012-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="c3012-219">O CISP habilita as seguintes tarefas de gerenciamento de catálogo do serviço de indexação de um cliente:</span><span class="sxs-lookup"><span data-stu-id="c3012-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="c3012-220">Consulte o estado atual de um catálogo de serviço de indexação no servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="c3012-221">Atualize o estado de um catálogo de serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="c3012-222">Inicie o processo de indexação para um determinado conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c3012-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="c3012-223">Inicie a otimização de um índice para melhorar o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="c3012-224">Todas as tarefas de administração remota seguem um modelo simples de solicitação/resposta.</span><span class="sxs-lookup"><span data-stu-id="c3012-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="c3012-225">Nenhum estado é mantido no cliente para qualquer chamada de administração e chamadas administrativas podem ser feitas em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="c3012-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="c3012-226">Consulta remota 1.3.2</span><span class="sxs-lookup"><span data-stu-id="c3012-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="c3012-227">O CISP permite que os clientes executem consultas de pesquisa em um servidor remoto que hospeda um serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="c3012-228">O envio de uma consulta de pesquisa é um processo de várias etapas iniciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="c3012-229">As etapas são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="c3012-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="c3012-230">O cliente solicita uma conexão a um servidor que hospeda um serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="c3012-231">O cliente envia os parâmetros para a consulta de pesquisa, que incluem:</span><span class="sxs-lookup"><span data-stu-id="c3012-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="c3012-232">As **restrições** para especificar quais documentos devem ser incluídos e/ou excluídos dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3012-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="c3012-233">A ordem na qual os resultados da pesquisa devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="c3012-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="c3012-234">As colunas a serem retornadas no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c3012-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="c3012-235">O número máximo de **linhas** que devem ser retornadas para a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="c3012-236">O tempo máximo para a execução da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="c3012-237">Depois que o servidor tiver confirmado a solicitação do cliente para iniciar a consulta, o cliente poderá solicitar informações de status sobre a consulta, mas essa não é uma etapa necessária.</span><span class="sxs-lookup"><span data-stu-id="c3012-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="c3012-238">O cliente especifica quais propriedades o servidor deve incluir nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3012-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="c3012-239">O cliente solicita um conjunto de resultados do servidor e o servidor responde enviando ao cliente os valores de propriedade dos arquivos que foram incluídos nos resultados para a consulta de pesquisa do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="c3012-240">Se o valor de uma propriedade for muito grande para caber em um único buffer de resposta, o servidor não enviará a propriedade, mas, em vez disso, definirá o status da propriedade como adiada.</span><span class="sxs-lookup"><span data-stu-id="c3012-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="c3012-241">Em seguida, o cliente solicita o valor da propriedade separadamente usando uma série de solicitações para partes sucessivas do valor e, em seguida, retoma a solicitação de outros valores.</span><span class="sxs-lookup"><span data-stu-id="c3012-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="c3012-242">Depois que o cliente for concluído com a consulta de pesquisa e não exigir mais resultados adicionais, o cliente entrará em contato com o servidor para liberar a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="c3012-243">Depois que o servidor tiver lançado a consulta, o cliente poderá enviar uma solicitação para desconectar-se do servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="c3012-244">A conexão é fechada.</span><span class="sxs-lookup"><span data-stu-id="c3012-244">The connection is then closed.</span></span> <span data-ttu-id="c3012-245">Como alternativa, o cliente pode emitir outra consulta e repetir a sequência da etapa 2.</span><span class="sxs-lookup"><span data-stu-id="c3012-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="c3012-246">Comportamento do Windows: esse protocolo é implementado no Windows 2000, no Windows XP, no Windows Server 2003 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3012-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="c3012-247">1.4 Relacionamento com outros protocolos</span><span class="sxs-lookup"><span data-stu-id="c3012-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="c3012-248">O CISP se baseia no protocolo SMB \[ MS-SMB \] para transporte de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3012-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="c3012-249">Nenhum outro protocolo depende diretamente do protocolo de serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c3012-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="c3012-250">*Comportamento do Windows: normalmente, os aplicativos interagem com um wrapper de interface OLE DB \[ msdn-OLEDB \] (por exemplo, um cliente de protocolo) e não diretamente com o protocolo.*</span><span class="sxs-lookup"><span data-stu-id="c3012-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="c3012-251">1,5 pré-requisitos e pré-condições</span><span class="sxs-lookup"><span data-stu-id="c3012-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="c3012-252">Supõe-se que o cliente tenha obtido o nome do servidor e um nome de catálogo antes que esse protocolo seja invocado.</span><span class="sxs-lookup"><span data-stu-id="c3012-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="c3012-253">Como um cliente faz isso está fora do escopo desta especificação.</span><span class="sxs-lookup"><span data-stu-id="c3012-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="c3012-254">Também pressupõe-se que o cliente e o servidor tenham uma associação de segurança utilizável com pipes nomeados \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="c3012-255">1.6 Applicability Statement</span><span class="sxs-lookup"><span data-stu-id="c3012-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="c3012-256">O CISP é projetado para consultar e gerenciar catálogos em um servidor remoto a partir de um cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="c3012-257">O CISP foi preterido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3012-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="c3012-258">1.7 Controle de versão e negociação de capacidade</span><span class="sxs-lookup"><span data-stu-id="c3012-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="c3012-259">Esse protocolo não possui controle de versão ou mecanismos de negociação de capacidade.</span><span class="sxs-lookup"><span data-stu-id="c3012-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="c3012-260">1.8 Campos extensíveis para fornecedor</span><span class="sxs-lookup"><span data-stu-id="c3012-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="c3012-261">Esse protocolo usa HRESULTs que são extensíveis pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c3012-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="c3012-262">Os fornecedores são livres para escolher seus próprios valores para esse campo, desde que o C bit (0x20000000) esteja definido conforme especificado na seção 4.1.1 do \[ MS-sys \] , indicando que ele é um código de cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="c3012-263">Esse protocolo também usa valores de NTSTATUS obtidos do espaço de número NTSTATUS definido em \[ MS-sys \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="c3012-264">Os fornecedores devem reutilizar esses valores com o significado indicado.</span><span class="sxs-lookup"><span data-stu-id="c3012-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="c3012-265">Escolher qualquer outro valor executará o risco de uma colisão no futuro.</span><span class="sxs-lookup"><span data-stu-id="c3012-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="c3012-266">*Comportamento do Windows: o Windows usa apenas os valores especificados na seção 4.1.3 do \[ MS-sys \] .*</span><span class="sxs-lookup"><span data-stu-id="c3012-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="c3012-267">IDs da propriedade 1.8.1</span><span class="sxs-lookup"><span data-stu-id="c3012-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="c3012-268">As propriedades são representadas por IDs conhecidas como IDs de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="c3012-269">Cada propriedade deve ter um identificador global exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c3012-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="c3012-270">Esse identificador consiste em um **GUID** que representa uma coleção de propriedades chamada um conjunto de propriedades, além de uma cadeia de caracteres ou um inteiro de 32 bits para identificar a propriedade dentro do conjunto.</span><span class="sxs-lookup"><span data-stu-id="c3012-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="c3012-271">Se o formulário inteiro da ID for usado, os valores 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE serão considerados inválidos.</span><span class="sxs-lookup"><span data-stu-id="c3012-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="c3012-272">Os fornecedores podem garantir que suas propriedades sejam definidas exclusivamente colocando-as em um conjunto de propriedades definido por seu próprio GUID.</span><span class="sxs-lookup"><span data-stu-id="c3012-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="c3012-273">1.9 Atribuições standard</span><span class="sxs-lookup"><span data-stu-id="c3012-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="c3012-274">Esse protocolo não tem nenhuma atribuição de padrões, somente atribuições privadas feitas pela Microsoft usando os procedimentos de alocação especificados em outros protocolos.</span><span class="sxs-lookup"><span data-stu-id="c3012-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="c3012-275">A Microsoft alocou esse protocolo como um pipe nomeado, conforme especificado em \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="c3012-276">A atribuição é:</span><span class="sxs-lookup"><span data-stu-id="c3012-276">The assignment is:</span></span>



| <span data-ttu-id="c3012-277">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3012-277">Parameter</span></span> | <span data-ttu-id="c3012-278">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-278">Value</span></span>             | <span data-ttu-id="c3012-279">Referência</span><span class="sxs-lookup"><span data-stu-id="c3012-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="c3012-280">Nome do pipe</span><span class="sxs-lookup"><span data-stu-id="c3012-280">Pipe name</span></span> | <span data-ttu-id="c3012-281">\\\\SKADS de CI de pipe \_</span><span class="sxs-lookup"><span data-stu-id="c3012-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="c3012-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="c3012-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="c3012-283">2 Mensagens</span><span class="sxs-lookup"><span data-stu-id="c3012-283">2 Messages</span></span>

-   [<span data-ttu-id="c3012-284">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="c3012-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="c3012-285">2.2 Sintaxe da mensagem</span><span class="sxs-lookup"><span data-stu-id="c3012-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="c3012-286">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="c3012-286">2.1 Transport</span></span>

<span data-ttu-id="c3012-287">Todas as mensagens devem ser transportadas usando um pipe nomeado, conforme especificado em \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="c3012-288">O seguinte nome de pipe é usado:</span><span class="sxs-lookup"><span data-stu-id="c3012-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="c3012-289">\\\\SKADS de CI de pipe \_</span><span class="sxs-lookup"><span data-stu-id="c3012-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="c3012-290">Esse protocolo usa o protocolo de pipe nomeado SMB subjacente para recuperar a identidade do chamador que fez a conexão, conforme especificado na seção 2.2.8 do \[ MS-SMB \] ; o cliente deve definir a identificação de segurança \_ como o ImpersonationLevel na solicitação para abrir o pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="c3012-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="c3012-291">2.2 Sintaxe da mensagem</span><span class="sxs-lookup"><span data-stu-id="c3012-291">2.2 Message Syntax</span></span>

<span data-ttu-id="c3012-292">Várias estruturas e mensagens nas seções a seguir referem-se aos identificadores de capítulo ou indicador.</span><span class="sxs-lookup"><span data-stu-id="c3012-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="c3012-293">Um identificador é uma estrutura opaca de longa de 32 bits que identifica exclusivamente um capítulo ou indicador.</span><span class="sxs-lookup"><span data-stu-id="c3012-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="c3012-294">Normalmente, os aplicativos cliente recebem valores de identificador por meio de chamadas de método; no entanto, há vários valores bem conhecidos que não precisam ser obtidos de um servidor, o significado do que é especificado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="c3012-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="c3012-295">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-295">Value</span></span>                         | <span data-ttu-id="c3012-296">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-297">DB \_ NULL \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="c3012-298">Um capítulo manipula o conjunto de linhas sem capítulos, que contém todos os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="c3012-299">DBBMK \_ primeiro 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="c3012-300">Um identificador de indicador para um indicador que identifica a primeira linha no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="c3012-301">DBBMK \_ último 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="c3012-302">Um identificador de indicador para um indicador que identifica a última linha no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="c3012-303">estruturas 2.2.1</span><span class="sxs-lookup"><span data-stu-id="c3012-303">2.2.1 Structures</span></span>

<span data-ttu-id="c3012-304">Esta seção detalha as estruturas de dados que são definidas e usadas pelo CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="c3012-305">Todos os inteiros de 2, 4 e 8 bytes assinados e não assinados nas seguintes estruturas devem ser transferidos em ordem de byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="c3012-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="c3012-306">A tabela a seguir resume as estruturas de dados definidas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="c3012-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="c3012-307">Estrutura</span><span class="sxs-lookup"><span data-stu-id="c3012-307">Structure</span></span>                    | <span data-ttu-id="c3012-308">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3012-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="c3012-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="c3012-310">Contém o valor no qual executar uma operação de correspondência para uma propriedade especificada em uma estrutura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="c3012-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="c3012-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="c3012-312">Contém uma matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="c3012-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="c3012-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="c3012-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="c3012-314">Representa os limites de uma dimensão de uma matriz especificada em uma estrutura SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="c3012-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="c3012-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="c3012-315">CFullPropSpec</span></span>                | <span data-ttu-id="c3012-316">Contém uma especificação de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="c3012-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-317">CContentRestriction</span></span>          | <span data-ttu-id="c3012-318">Contém uma cadeia de caracteres para corresponder a um valor de propriedade no cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3012-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="c3012-319">CKey</span><span class="sxs-lookup"><span data-stu-id="c3012-319">CKey</span></span>                         | <span data-ttu-id="c3012-320">Contém um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="c3012-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="c3012-322">Contém um valor de propriedade para corresponder a uma operação.</span><span class="sxs-lookup"><span data-stu-id="c3012-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="c3012-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="c3012-324">Contém uma correspondência de consulta de idioma natural para uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="c3012-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-325">CNodeRestriction</span></span>             | <span data-ttu-id="c3012-326">Contém uma matriz de nós de árvore de comando especificando as restrições para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="c3012-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-327">COccRestriction</span></span>              | <span data-ttu-id="c3012-328">Contém o local de uma palavra em uma frase.</span><span class="sxs-lookup"><span data-stu-id="c3012-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="c3012-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-329">CPropertyRestriction</span></span>         | <span data-ttu-id="c3012-330">Contém um valor de propriedade para corresponder a uma operação.</span><span class="sxs-lookup"><span data-stu-id="c3012-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="c3012-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-331">CRangeRestriction</span></span>            | <span data-ttu-id="c3012-332">Contém uma restrição em um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="c3012-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="c3012-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-333">CScopeRestriction</span></span>            | <span data-ttu-id="c3012-334">Contém uma restrição sobre os arquivos a serem pesquisados.</span><span class="sxs-lookup"><span data-stu-id="c3012-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="c3012-335">CSort</span><span class="sxs-lookup"><span data-stu-id="c3012-335">CSort</span></span>                        | <span data-ttu-id="c3012-336">Identifica uma coluna a ser classificada.</span><span class="sxs-lookup"><span data-stu-id="c3012-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="c3012-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-337">CSynRestriction</span></span>              | <span data-ttu-id="c3012-338">Contém uma palavra ou seus sinônimos para uma frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="c3012-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-339">CVectorRestriction</span></span>           | <span data-ttu-id="c3012-340">Contém uma operação ponderada ou em um nó de árvore de comandos.</span><span class="sxs-lookup"><span data-stu-id="c3012-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="c3012-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-341">CWordRestriction</span></span>             | <span data-ttu-id="c3012-342">Contém uma palavra para uma frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="c3012-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-343">CRestriction</span></span>                 | <span data-ttu-id="c3012-344">Contém um nó de uma árvore de comando de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="c3012-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="c3012-345">CColumnSet</span></span>                   | <span data-ttu-id="c3012-346">Indica o número de colunas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="c3012-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="c3012-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="c3012-347">CCategorizationSet</span></span>           | <span data-ttu-id="c3012-348">Contém informações sobre o agrupamento de um conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="c3012-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="c3012-349">CCategorizationSpec</span></span>          | <span data-ttu-id="c3012-350">Contém uma definição de categorias nas quais os resultados da consulta serão categorizados.</span><span class="sxs-lookup"><span data-stu-id="c3012-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="c3012-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="c3012-351">CDbColId</span></span>                     | <span data-ttu-id="c3012-352">Contém uma coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="c3012-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="c3012-353">CDbProp</span></span>                      | <span data-ttu-id="c3012-354">Contém uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="c3012-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="c3012-355">CDbPropSet</span></span>                   | <span data-ttu-id="c3012-356">Contém um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3012-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="c3012-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="c3012-357">CPidMapper</span></span>                   | <span data-ttu-id="c3012-358">Contém uma matriz de IDs de propriedade especificando as propriedades a serem retornadas em um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="c3012-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="c3012-359">CRowSeekAt</span></span>                   | <span data-ttu-id="c3012-360">Contém o deslocamento no qual recuperar linhas em uma mensagem CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="c3012-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="c3012-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="c3012-362">Identifica o ponto no qual iniciar a recuperação para uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="c3012-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="c3012-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="c3012-364">Identifica os indicadores dos quais recuperar linhas para uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="c3012-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="c3012-365">CRowSeekNext</span></span>                 | <span data-ttu-id="c3012-366">Contém o número de linhas a serem ignoradas em uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="c3012-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="c3012-367">CRowsetProperties</span></span>            | <span data-ttu-id="c3012-368">Contém as informações de configuração de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="c3012-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="c3012-369">CSortSet</span></span>                     | <span data-ttu-id="c3012-370">Contém a ordem de classificação para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="c3012-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="c3012-371">CTableColumn</span></span>                 | <span data-ttu-id="c3012-372">Contém uma coluna para a mensagem CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="c3012-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="c3012-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="c3012-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="c3012-374">Contém um valor serializado.</span><span class="sxs-lookup"><span data-stu-id="c3012-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="c3012-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="c3012-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="c3012-376">A estrutura CBaseStorageVariant contém o valor no qual executar uma operação de correspondência para uma propriedade especificada na estrutura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="c3012-377">0</span><span class="sxs-lookup"><span data-stu-id="c3012-377">0</span></span>

<span data-ttu-id="c3012-378">1</span><span class="sxs-lookup"><span data-stu-id="c3012-378">1</span></span>

<span data-ttu-id="c3012-379">2</span><span class="sxs-lookup"><span data-stu-id="c3012-379">2</span></span>

<span data-ttu-id="c3012-380">3</span><span class="sxs-lookup"><span data-stu-id="c3012-380">3</span></span>

<span data-ttu-id="c3012-381">4</span><span class="sxs-lookup"><span data-stu-id="c3012-381">4</span></span>

<span data-ttu-id="c3012-382">5</span><span class="sxs-lookup"><span data-stu-id="c3012-382">5</span></span>

<span data-ttu-id="c3012-383">6</span><span class="sxs-lookup"><span data-stu-id="c3012-383">6</span></span>

<span data-ttu-id="c3012-384">7</span><span class="sxs-lookup"><span data-stu-id="c3012-384">7</span></span>

<span data-ttu-id="c3012-385">8</span><span class="sxs-lookup"><span data-stu-id="c3012-385">8</span></span>

<span data-ttu-id="c3012-386">9</span><span class="sxs-lookup"><span data-stu-id="c3012-386">9</span></span>

<span data-ttu-id="c3012-387">1</span><span class="sxs-lookup"><span data-stu-id="c3012-387">1</span></span><br/> <span data-ttu-id="c3012-388">0</span><span class="sxs-lookup"><span data-stu-id="c3012-388">0</span></span><br/>

<span data-ttu-id="c3012-389">1</span><span class="sxs-lookup"><span data-stu-id="c3012-389">1</span></span>

<span data-ttu-id="c3012-390">2</span><span class="sxs-lookup"><span data-stu-id="c3012-390">2</span></span>

<span data-ttu-id="c3012-391">3</span><span class="sxs-lookup"><span data-stu-id="c3012-391">3</span></span>

<span data-ttu-id="c3012-392">4</span><span class="sxs-lookup"><span data-stu-id="c3012-392">4</span></span>

<span data-ttu-id="c3012-393">5</span><span class="sxs-lookup"><span data-stu-id="c3012-393">5</span></span>

<span data-ttu-id="c3012-394">6</span><span class="sxs-lookup"><span data-stu-id="c3012-394">6</span></span>

<span data-ttu-id="c3012-395">7</span><span class="sxs-lookup"><span data-stu-id="c3012-395">7</span></span>

<span data-ttu-id="c3012-396">8</span><span class="sxs-lookup"><span data-stu-id="c3012-396">8</span></span>

<span data-ttu-id="c3012-397">9</span><span class="sxs-lookup"><span data-stu-id="c3012-397">9</span></span>

<span data-ttu-id="c3012-398">2</span><span class="sxs-lookup"><span data-stu-id="c3012-398">2</span></span><br/> <span data-ttu-id="c3012-399">0</span><span class="sxs-lookup"><span data-stu-id="c3012-399">0</span></span><br/>

<span data-ttu-id="c3012-400">1</span><span class="sxs-lookup"><span data-stu-id="c3012-400">1</span></span>

<span data-ttu-id="c3012-401">2</span><span class="sxs-lookup"><span data-stu-id="c3012-401">2</span></span>

<span data-ttu-id="c3012-402">3</span><span class="sxs-lookup"><span data-stu-id="c3012-402">3</span></span>

<span data-ttu-id="c3012-403">4</span><span class="sxs-lookup"><span data-stu-id="c3012-403">4</span></span>

<span data-ttu-id="c3012-404">5</span><span class="sxs-lookup"><span data-stu-id="c3012-404">5</span></span>

<span data-ttu-id="c3012-405">6</span><span class="sxs-lookup"><span data-stu-id="c3012-405">6</span></span>

<span data-ttu-id="c3012-406">7</span><span class="sxs-lookup"><span data-stu-id="c3012-406">7</span></span>

<span data-ttu-id="c3012-407">8</span><span class="sxs-lookup"><span data-stu-id="c3012-407">8</span></span>

<span data-ttu-id="c3012-408">9</span><span class="sxs-lookup"><span data-stu-id="c3012-408">9</span></span>

<span data-ttu-id="c3012-409">3</span><span class="sxs-lookup"><span data-stu-id="c3012-409">3</span></span><br/> <span data-ttu-id="c3012-410">0</span><span class="sxs-lookup"><span data-stu-id="c3012-410">0</span></span><br/>

<span data-ttu-id="c3012-411">1</span><span class="sxs-lookup"><span data-stu-id="c3012-411">1</span></span>

<span data-ttu-id="c3012-412">vType</span><span class="sxs-lookup"><span data-stu-id="c3012-412">vType</span></span>

<span data-ttu-id="c3012-413">vData1</span><span class="sxs-lookup"><span data-stu-id="c3012-413">vData1</span></span>

<span data-ttu-id="c3012-414">vData2</span><span class="sxs-lookup"><span data-stu-id="c3012-414">vData2</span></span>

<span data-ttu-id="c3012-415">vValue (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-415">vValue (variable)</span></span>



 

<span data-ttu-id="c3012-416">**vType**: um indicador de tipo, que indica o tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="c3012-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="c3012-417">DEVE ser um dos valores de VARENUM especificados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3012-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="c3012-418">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-418">Value</span></span>                 | <span data-ttu-id="c3012-419">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-420">VT \_ vazio (0x0000)</span><span class="sxs-lookup"><span data-stu-id="c3012-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="c3012-421">vValue não está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="c3012-422">VT \_ NULL (0x0001)</span><span class="sxs-lookup"><span data-stu-id="c3012-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="c3012-423">vValue não está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="c3012-424">VT \_ i1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="c3012-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="c3012-425">Um inteiro de um byte com sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="c3012-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="c3012-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="c3012-427">Um inteiro de um byte sem sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="c3012-428">VT \_ i2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="c3012-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="c3012-429">Um inteiro de dois bytes com sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="c3012-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="c3012-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="c3012-431">Um inteiro de dois bytes sem sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="c3012-432">VT \_ bool (0x000B)</span><span class="sxs-lookup"><span data-stu-id="c3012-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="c3012-433">Um valor booliano; um inteiro de 2 bytes contendo 0x0000 (FALSE) ou 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="c3012-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="c3012-434">VT \_ i4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="c3012-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="c3012-435">Um inteiro de quatro bytes com sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="c3012-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="c3012-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="c3012-437">Um inteiro de quatro bytes sem sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="c3012-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="c3012-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="c3012-439">Um número de ponto flutuante de IEEE 32 bits, conforme definido em \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="c3012-440">VT \_ int (0x0016)</span><span class="sxs-lookup"><span data-stu-id="c3012-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="c3012-441">Um inteiro de quatro bytes com sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="c3012-442">VT \_ uint (0x0017)</span><span class="sxs-lookup"><span data-stu-id="c3012-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="c3012-443">Um inteiro de quatro bytes sem sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="c3012-444">\_Erro de VT (0x000a)</span><span class="sxs-lookup"><span data-stu-id="c3012-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="c3012-445">Um inteiro sem sinal de 4 bytes contendo um HRESULT, conforme especificado em \[ MS-sys \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="c3012-446">VT \_ i8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="c3012-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="c3012-447">Um inteiro com sinal de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="c3012-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="c3012-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="c3012-449">Um inteiro de oito bytes sem sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="c3012-450">\_R8 de VT (0x0005)</span><span class="sxs-lookup"><span data-stu-id="c3012-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="c3012-451">Um número de ponto flutuante de IEEE 64 bits, conforme definido em \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="c3012-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="c3012-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="c3012-453">Um inteiro de complemento de 8 bytes (dimensionado por 10.000).</span><span class="sxs-lookup"><span data-stu-id="c3012-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="c3012-454">\_Data VT (0x0007)</span><span class="sxs-lookup"><span data-stu-id="c3012-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="c3012-455">Um número de ponto flutuante de 64 bits que representa o número de dias desde 00:00:00 em 31 de dezembro de 1899 (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="c3012-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="c3012-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="c3012-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="c3012-457">Um inteiro de 64 bits que representa o número de intervalos de 100 nanossegundos desde 00:00:00 em 1º de janeiro de 1601 (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="c3012-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="c3012-458">VT \_ decimal (0x000e)</span><span class="sxs-lookup"><span data-stu-id="c3012-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="c3012-459">Uma estrutura DECIMAL, conforme especificado na seção 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="c3012-460">\_CLSID do VT (0x0048)</span><span class="sxs-lookup"><span data-stu-id="c3012-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="c3012-461">Um valor binário de 16 bytes que contém um GUID.</span><span class="sxs-lookup"><span data-stu-id="c3012-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="c3012-462">\_Blob VT (0x0041)</span><span class="sxs-lookup"><span data-stu-id="c3012-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="c3012-463">Uma contagem de inteiros sem sinal de 4 bytes de bytes no BLOB, seguida por muitos bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="c3012-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="c3012-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="c3012-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="c3012-465">Uma contagem de inteiros sem sinal de 4 bytes de bytes na cadeia de caracteres, seguida por uma cadeia de caracteres, conforme especificado abaixo em vValue.</span><span class="sxs-lookup"><span data-stu-id="c3012-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="c3012-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="c3012-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="c3012-467">Uma cadeia de caracteres ANSI terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="c3012-468">\_0x001F (VT LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="c3012-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="c3012-469">Uma String Unicode Unicode terminada em nulo \[ \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="c3012-470">\_Variável VT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="c3012-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="c3012-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="c3012-471">CBaseStorageVariant.</span></span> <span data-ttu-id="c3012-472">DEVE ser combinado com um modificador de tipo da \_ matriz VT ou do \_ vetor VT.</span><span class="sxs-lookup"><span data-stu-id="c3012-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="c3012-473">A tabela a seguir especifica os modificadores de tipo para vType.</span><span class="sxs-lookup"><span data-stu-id="c3012-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="c3012-474">Os modificadores de tipo podem ser Binary or com vType, para alterar o significado de vValue para indicar que ele é um dos dois tipos de matriz possíveis.</span><span class="sxs-lookup"><span data-stu-id="c3012-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="c3012-475">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-475">Value</span></span>               | <span data-ttu-id="c3012-476">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-477">\_Vetor VT (0x1000)</span><span class="sxs-lookup"><span data-stu-id="c3012-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="c3012-478">Se o indicador de tipo for combinado com o \_ vetor VT usando um operador OR, vValue será uma matriz contada de valores do tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="c3012-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="c3012-479">Consulte a seção 2.2.1.1.1.2 para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="c3012-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="c3012-480">Este modificador de tipo não deve ser combinado com os seguintes tipos: VT \_ int, VT \_ uint, VT \_ decimal, VT \_ BLOB, VT \_ blob \_ Object.</span><span class="sxs-lookup"><span data-stu-id="c3012-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="c3012-481">\_Matriz VT (0x2000)</span><span class="sxs-lookup"><span data-stu-id="c3012-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="c3012-482">Se o indicador de tipo for combinado com a \_ matriz VT por um operador OR, o valor será um SafeArray (conforme especificado na seção 2.2.1.1.1.3) que contém os valores do tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="c3012-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="c3012-483">Este modificador de tipo não deve ser combinado com os seguintes tipos: VT \_ i8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ blob \_ Object, VT \_ LPStr, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="c3012-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="c3012-484">**vData1**: quando VTYPE é VT \_ decimal, o valor desse campo é especificado como o campo de escala na seção 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="c3012-485">Para todos os outros vTypes, o valor deve ser definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3012-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="c3012-486">**vData2**: quando VTYPE é VT \_ decimal, o valor desse campo é especificado como o campo de sinal na seção 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="c3012-487">Para todos os outros vTypes, o valor deve ser definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3012-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="c3012-488">**vValue**: o valor para a operação de correspondência.</span><span class="sxs-lookup"><span data-stu-id="c3012-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="c3012-489">A sintaxe deve ser conforme indicado no campo vType.</span><span class="sxs-lookup"><span data-stu-id="c3012-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="c3012-490">A tabela a seguir resume os tamanhos do campo vValue, dependendo do campo vType para tipos de dados de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="c3012-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="c3012-491">O tamanho é em bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-491">The size is in bytes.</span></span>



| <span data-ttu-id="c3012-492">vType</span><span class="sxs-lookup"><span data-stu-id="c3012-492">vType</span></span>                                                   | <span data-ttu-id="c3012-493">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c3012-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="c3012-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="c3012-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="c3012-495">1</span><span class="sxs-lookup"><span data-stu-id="c3012-495">1</span></span>    |
| <span data-ttu-id="c3012-496">VT \_ I2, VT \_ UI2, VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="c3012-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="c3012-497">2</span><span class="sxs-lookup"><span data-stu-id="c3012-497">2</span></span>    |
| <span data-ttu-id="c3012-498">VT \_ i4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, erro de VT \_</span><span class="sxs-lookup"><span data-stu-id="c3012-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="c3012-499">4</span><span class="sxs-lookup"><span data-stu-id="c3012-499">4</span></span>    |
| <span data-ttu-id="c3012-500">VT \_ i8, VT \_ UI8, VT \_ R8, VT \_ Cy, \_ Data VT, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="c3012-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="c3012-501">8</span><span class="sxs-lookup"><span data-stu-id="c3012-501">8</span></span>    |
| <span data-ttu-id="c3012-502">VT \_ decimal, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="c3012-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="c3012-503">16</span><span class="sxs-lookup"><span data-stu-id="c3012-503">16</span></span>   |



 

<span data-ttu-id="c3012-504">Se vType for definido como VT \_ BLOB, VT \_ BSTR ou VT \_ LPStr, a estrutura de vValue será especificada no diagrama a seguir:</span><span class="sxs-lookup"><span data-stu-id="c3012-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="c3012-505">0</span><span class="sxs-lookup"><span data-stu-id="c3012-505">0</span></span>

<span data-ttu-id="c3012-506">1</span><span class="sxs-lookup"><span data-stu-id="c3012-506">1</span></span>

<span data-ttu-id="c3012-507">2</span><span class="sxs-lookup"><span data-stu-id="c3012-507">2</span></span>

<span data-ttu-id="c3012-508">3</span><span class="sxs-lookup"><span data-stu-id="c3012-508">3</span></span>

<span data-ttu-id="c3012-509">4</span><span class="sxs-lookup"><span data-stu-id="c3012-509">4</span></span>

<span data-ttu-id="c3012-510">5</span><span class="sxs-lookup"><span data-stu-id="c3012-510">5</span></span>

<span data-ttu-id="c3012-511">6</span><span class="sxs-lookup"><span data-stu-id="c3012-511">6</span></span>

<span data-ttu-id="c3012-512">7</span><span class="sxs-lookup"><span data-stu-id="c3012-512">7</span></span>

<span data-ttu-id="c3012-513">8</span><span class="sxs-lookup"><span data-stu-id="c3012-513">8</span></span>

<span data-ttu-id="c3012-514">9</span><span class="sxs-lookup"><span data-stu-id="c3012-514">9</span></span>

<span data-ttu-id="c3012-515">1</span><span class="sxs-lookup"><span data-stu-id="c3012-515">1</span></span><br/> <span data-ttu-id="c3012-516">0</span><span class="sxs-lookup"><span data-stu-id="c3012-516">0</span></span><br/>

<span data-ttu-id="c3012-517">1</span><span class="sxs-lookup"><span data-stu-id="c3012-517">1</span></span>

<span data-ttu-id="c3012-518">2</span><span class="sxs-lookup"><span data-stu-id="c3012-518">2</span></span>

<span data-ttu-id="c3012-519">3</span><span class="sxs-lookup"><span data-stu-id="c3012-519">3</span></span>

<span data-ttu-id="c3012-520">4</span><span class="sxs-lookup"><span data-stu-id="c3012-520">4</span></span>

<span data-ttu-id="c3012-521">5</span><span class="sxs-lookup"><span data-stu-id="c3012-521">5</span></span>

<span data-ttu-id="c3012-522">6</span><span class="sxs-lookup"><span data-stu-id="c3012-522">6</span></span>

<span data-ttu-id="c3012-523">7</span><span class="sxs-lookup"><span data-stu-id="c3012-523">7</span></span>

<span data-ttu-id="c3012-524">8</span><span class="sxs-lookup"><span data-stu-id="c3012-524">8</span></span>

<span data-ttu-id="c3012-525">9</span><span class="sxs-lookup"><span data-stu-id="c3012-525">9</span></span>

<span data-ttu-id="c3012-526">2</span><span class="sxs-lookup"><span data-stu-id="c3012-526">2</span></span><br/> <span data-ttu-id="c3012-527">0</span><span class="sxs-lookup"><span data-stu-id="c3012-527">0</span></span><br/>

<span data-ttu-id="c3012-528">1</span><span class="sxs-lookup"><span data-stu-id="c3012-528">1</span></span>

<span data-ttu-id="c3012-529">2</span><span class="sxs-lookup"><span data-stu-id="c3012-529">2</span></span>

<span data-ttu-id="c3012-530">3</span><span class="sxs-lookup"><span data-stu-id="c3012-530">3</span></span>

<span data-ttu-id="c3012-531">4</span><span class="sxs-lookup"><span data-stu-id="c3012-531">4</span></span>

<span data-ttu-id="c3012-532">5</span><span class="sxs-lookup"><span data-stu-id="c3012-532">5</span></span>

<span data-ttu-id="c3012-533">6</span><span class="sxs-lookup"><span data-stu-id="c3012-533">6</span></span>

<span data-ttu-id="c3012-534">7</span><span class="sxs-lookup"><span data-stu-id="c3012-534">7</span></span>

<span data-ttu-id="c3012-535">8</span><span class="sxs-lookup"><span data-stu-id="c3012-535">8</span></span>

<span data-ttu-id="c3012-536">9</span><span class="sxs-lookup"><span data-stu-id="c3012-536">9</span></span>

<span data-ttu-id="c3012-537">3</span><span class="sxs-lookup"><span data-stu-id="c3012-537">3</span></span><br/> <span data-ttu-id="c3012-538">0</span><span class="sxs-lookup"><span data-stu-id="c3012-538">0</span></span><br/>

<span data-ttu-id="c3012-539">1</span><span class="sxs-lookup"><span data-stu-id="c3012-539">1</span></span>

<span data-ttu-id="c3012-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="c3012-540">cbSize</span></span>

<span data-ttu-id="c3012-541">blobData (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="c3012-542">**cbSize**: inteiro de 32 bits sem sinal, indicando o tamanho do campo blobData em bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="c3012-543">Se vType for definido como VT \_ BSTR ou VT \_ LPStr, cbSize deverá ser definido como 0x00000000 quando a cadeia de caracteres representada for uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="c3012-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="c3012-544">**blobData**: deve ter comprimento cbSize em bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="c3012-545">Para vType definido como \_ blob VT, esse campo é dados de blob binário opaco.</span><span class="sxs-lookup"><span data-stu-id="c3012-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="c3012-546">Para vType definido como VT \_ BSTR, esse campo é um conjunto de caracteres em um conjunto de caracteres selecionado pelo OEM.</span><span class="sxs-lookup"><span data-stu-id="c3012-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="c3012-547">O cliente e o servidor devem ser configurados para ter conjuntos de caracteres interoperáveis (fora da banda do protocolo).</span><span class="sxs-lookup"><span data-stu-id="c3012-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="c3012-548">Não há nenhum requisito de que seja encerrado em nulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="c3012-549">Para vType definido como VT \_ LPStr, este campo é uma cadeia de caracteres terminada em nulo em um conjunto de caracteres selecionado pelo OEM.</span><span class="sxs-lookup"><span data-stu-id="c3012-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="c3012-550">O cliente e o servidor devem ser configurados para ter conjuntos de caracteres interoperáveis (fora da banda do protocolo).</span><span class="sxs-lookup"><span data-stu-id="c3012-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="c3012-551">Se vType for definido como VT \_ LPWStr, a estrutura de vValue será especificada no diagrama a seguir:</span><span class="sxs-lookup"><span data-stu-id="c3012-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="c3012-552">0</span><span class="sxs-lookup"><span data-stu-id="c3012-552">0</span></span>

<span data-ttu-id="c3012-553">1</span><span class="sxs-lookup"><span data-stu-id="c3012-553">1</span></span>

<span data-ttu-id="c3012-554">2</span><span class="sxs-lookup"><span data-stu-id="c3012-554">2</span></span>

<span data-ttu-id="c3012-555">3</span><span class="sxs-lookup"><span data-stu-id="c3012-555">3</span></span>

<span data-ttu-id="c3012-556">4</span><span class="sxs-lookup"><span data-stu-id="c3012-556">4</span></span>

<span data-ttu-id="c3012-557">5</span><span class="sxs-lookup"><span data-stu-id="c3012-557">5</span></span>

<span data-ttu-id="c3012-558">6</span><span class="sxs-lookup"><span data-stu-id="c3012-558">6</span></span>

<span data-ttu-id="c3012-559">7</span><span class="sxs-lookup"><span data-stu-id="c3012-559">7</span></span>

<span data-ttu-id="c3012-560">8</span><span class="sxs-lookup"><span data-stu-id="c3012-560">8</span></span>

<span data-ttu-id="c3012-561">9</span><span class="sxs-lookup"><span data-stu-id="c3012-561">9</span></span>

<span data-ttu-id="c3012-562">1</span><span class="sxs-lookup"><span data-stu-id="c3012-562">1</span></span><br/> <span data-ttu-id="c3012-563">0</span><span class="sxs-lookup"><span data-stu-id="c3012-563">0</span></span><br/>

<span data-ttu-id="c3012-564">1</span><span class="sxs-lookup"><span data-stu-id="c3012-564">1</span></span>

<span data-ttu-id="c3012-565">2</span><span class="sxs-lookup"><span data-stu-id="c3012-565">2</span></span>

<span data-ttu-id="c3012-566">3</span><span class="sxs-lookup"><span data-stu-id="c3012-566">3</span></span>

<span data-ttu-id="c3012-567">4</span><span class="sxs-lookup"><span data-stu-id="c3012-567">4</span></span>

<span data-ttu-id="c3012-568">5</span><span class="sxs-lookup"><span data-stu-id="c3012-568">5</span></span>

<span data-ttu-id="c3012-569">6</span><span class="sxs-lookup"><span data-stu-id="c3012-569">6</span></span>

<span data-ttu-id="c3012-570">7</span><span class="sxs-lookup"><span data-stu-id="c3012-570">7</span></span>

<span data-ttu-id="c3012-571">8</span><span class="sxs-lookup"><span data-stu-id="c3012-571">8</span></span>

<span data-ttu-id="c3012-572">9</span><span class="sxs-lookup"><span data-stu-id="c3012-572">9</span></span>

<span data-ttu-id="c3012-573">2</span><span class="sxs-lookup"><span data-stu-id="c3012-573">2</span></span><br/> <span data-ttu-id="c3012-574">0</span><span class="sxs-lookup"><span data-stu-id="c3012-574">0</span></span><br/>

<span data-ttu-id="c3012-575">1</span><span class="sxs-lookup"><span data-stu-id="c3012-575">1</span></span>

<span data-ttu-id="c3012-576">2</span><span class="sxs-lookup"><span data-stu-id="c3012-576">2</span></span>

<span data-ttu-id="c3012-577">3</span><span class="sxs-lookup"><span data-stu-id="c3012-577">3</span></span>

<span data-ttu-id="c3012-578">4</span><span class="sxs-lookup"><span data-stu-id="c3012-578">4</span></span>

<span data-ttu-id="c3012-579">5</span><span class="sxs-lookup"><span data-stu-id="c3012-579">5</span></span>

<span data-ttu-id="c3012-580">6</span><span class="sxs-lookup"><span data-stu-id="c3012-580">6</span></span>

<span data-ttu-id="c3012-581">7</span><span class="sxs-lookup"><span data-stu-id="c3012-581">7</span></span>

<span data-ttu-id="c3012-582">8</span><span class="sxs-lookup"><span data-stu-id="c3012-582">8</span></span>

<span data-ttu-id="c3012-583">9</span><span class="sxs-lookup"><span data-stu-id="c3012-583">9</span></span>

<span data-ttu-id="c3012-584">3</span><span class="sxs-lookup"><span data-stu-id="c3012-584">3</span></span><br/> <span data-ttu-id="c3012-585">0</span><span class="sxs-lookup"><span data-stu-id="c3012-585">0</span></span><br/>

<span data-ttu-id="c3012-586">1</span><span class="sxs-lookup"><span data-stu-id="c3012-586">1</span></span>

<span data-ttu-id="c3012-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="c3012-587">ccLen</span></span>

<span data-ttu-id="c3012-588">Cadeia de caracteres (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-588">string (variable, optional)</span></span>



 

<span data-ttu-id="c3012-589">**ccLen**: inteiro de 32 bits sem sinal, indicando o tamanho do campo de cadeia de caracteres em caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3012-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="c3012-590">DEVE ser definido como 0x00000000 para uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="c3012-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="c3012-591">**cadeia** de caracteres: cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="c3012-592">Estruturas 2.2.1.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="c3012-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="c3012-593">As estruturas a seguir são usadas na estrutura CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="c3012-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="c3012-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="c3012-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="c3012-595">DECIMAL é usado para representar um valor numérico exato com uma precisão fixa e uma escala fixa.</span><span class="sxs-lookup"><span data-stu-id="c3012-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="c3012-596">Quando vType é definido como VT \_ decimal (0x0000E), os campos vData1 e vData2 de CBASESTORAGEVARIANT devem ser interpretados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="c3012-597">**vData1**: o número de dígitos à direita do ponto decimal.</span><span class="sxs-lookup"><span data-stu-id="c3012-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="c3012-598">DEVE estar no intervalo de 0 a 28.</span><span class="sxs-lookup"><span data-stu-id="c3012-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="c3012-599">**vData2**: o sinal do valor numérico.</span><span class="sxs-lookup"><span data-stu-id="c3012-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="c3012-600">Defina como 0x00 se positivo, 0x80 se negativo.</span><span class="sxs-lookup"><span data-stu-id="c3012-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="c3012-601">O formato do campo vValue é:</span><span class="sxs-lookup"><span data-stu-id="c3012-601">The format of the vValue field is:</span></span>



<span data-ttu-id="c3012-602">0</span><span class="sxs-lookup"><span data-stu-id="c3012-602">0</span></span>

<span data-ttu-id="c3012-603">1</span><span class="sxs-lookup"><span data-stu-id="c3012-603">1</span></span>

<span data-ttu-id="c3012-604">2</span><span class="sxs-lookup"><span data-stu-id="c3012-604">2</span></span>

<span data-ttu-id="c3012-605">3</span><span class="sxs-lookup"><span data-stu-id="c3012-605">3</span></span>

<span data-ttu-id="c3012-606">4</span><span class="sxs-lookup"><span data-stu-id="c3012-606">4</span></span>

<span data-ttu-id="c3012-607">5</span><span class="sxs-lookup"><span data-stu-id="c3012-607">5</span></span>

<span data-ttu-id="c3012-608">6</span><span class="sxs-lookup"><span data-stu-id="c3012-608">6</span></span>

<span data-ttu-id="c3012-609">7</span><span class="sxs-lookup"><span data-stu-id="c3012-609">7</span></span>

<span data-ttu-id="c3012-610">8</span><span class="sxs-lookup"><span data-stu-id="c3012-610">8</span></span>

<span data-ttu-id="c3012-611">9</span><span class="sxs-lookup"><span data-stu-id="c3012-611">9</span></span>

<span data-ttu-id="c3012-612">1</span><span class="sxs-lookup"><span data-stu-id="c3012-612">1</span></span><br/> <span data-ttu-id="c3012-613">0</span><span class="sxs-lookup"><span data-stu-id="c3012-613">0</span></span><br/>

<span data-ttu-id="c3012-614">1</span><span class="sxs-lookup"><span data-stu-id="c3012-614">1</span></span>

<span data-ttu-id="c3012-615">2</span><span class="sxs-lookup"><span data-stu-id="c3012-615">2</span></span>

<span data-ttu-id="c3012-616">3</span><span class="sxs-lookup"><span data-stu-id="c3012-616">3</span></span>

<span data-ttu-id="c3012-617">4</span><span class="sxs-lookup"><span data-stu-id="c3012-617">4</span></span>

<span data-ttu-id="c3012-618">5</span><span class="sxs-lookup"><span data-stu-id="c3012-618">5</span></span>

<span data-ttu-id="c3012-619">6</span><span class="sxs-lookup"><span data-stu-id="c3012-619">6</span></span>

<span data-ttu-id="c3012-620">7</span><span class="sxs-lookup"><span data-stu-id="c3012-620">7</span></span>

<span data-ttu-id="c3012-621">8</span><span class="sxs-lookup"><span data-stu-id="c3012-621">8</span></span>

<span data-ttu-id="c3012-622">9</span><span class="sxs-lookup"><span data-stu-id="c3012-622">9</span></span>

<span data-ttu-id="c3012-623">2</span><span class="sxs-lookup"><span data-stu-id="c3012-623">2</span></span><br/> <span data-ttu-id="c3012-624">0</span><span class="sxs-lookup"><span data-stu-id="c3012-624">0</span></span><br/>

<span data-ttu-id="c3012-625">1</span><span class="sxs-lookup"><span data-stu-id="c3012-625">1</span></span>

<span data-ttu-id="c3012-626">2</span><span class="sxs-lookup"><span data-stu-id="c3012-626">2</span></span>

<span data-ttu-id="c3012-627">3</span><span class="sxs-lookup"><span data-stu-id="c3012-627">3</span></span>

<span data-ttu-id="c3012-628">4</span><span class="sxs-lookup"><span data-stu-id="c3012-628">4</span></span>

<span data-ttu-id="c3012-629">5</span><span class="sxs-lookup"><span data-stu-id="c3012-629">5</span></span>

<span data-ttu-id="c3012-630">6</span><span class="sxs-lookup"><span data-stu-id="c3012-630">6</span></span>

<span data-ttu-id="c3012-631">7</span><span class="sxs-lookup"><span data-stu-id="c3012-631">7</span></span>

<span data-ttu-id="c3012-632">8</span><span class="sxs-lookup"><span data-stu-id="c3012-632">8</span></span>

<span data-ttu-id="c3012-633">9</span><span class="sxs-lookup"><span data-stu-id="c3012-633">9</span></span>

<span data-ttu-id="c3012-634">3</span><span class="sxs-lookup"><span data-stu-id="c3012-634">3</span></span><br/> <span data-ttu-id="c3012-635">0</span><span class="sxs-lookup"><span data-stu-id="c3012-635">0</span></span><br/>

<span data-ttu-id="c3012-636">1</span><span class="sxs-lookup"><span data-stu-id="c3012-636">1</span></span>

<span data-ttu-id="c3012-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="c3012-637">Hi32</span></span>

<span data-ttu-id="c3012-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="c3012-638">Lo32</span></span>

<span data-ttu-id="c3012-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="c3012-639">Mid32</span></span>



 

<span data-ttu-id="c3012-640">**Hi32**: os mais de 32 bits do número inteiro de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="c3012-641">**Lo32**: os mais baixos 32 bits do número inteiro de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="c3012-642">**Mid32**: os bits do meio 32 do número inteiro de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="c3012-643">vetor VT 2.2.1.1.1.2 \_</span><span class="sxs-lookup"><span data-stu-id="c3012-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="c3012-644">O \_ vetor VT é usado para passar matrizes unidimensionais.</span><span class="sxs-lookup"><span data-stu-id="c3012-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="c3012-645">0</span><span class="sxs-lookup"><span data-stu-id="c3012-645">0</span></span>

<span data-ttu-id="c3012-646">1</span><span class="sxs-lookup"><span data-stu-id="c3012-646">1</span></span>

<span data-ttu-id="c3012-647">2</span><span class="sxs-lookup"><span data-stu-id="c3012-647">2</span></span>

<span data-ttu-id="c3012-648">3</span><span class="sxs-lookup"><span data-stu-id="c3012-648">3</span></span>

<span data-ttu-id="c3012-649">4</span><span class="sxs-lookup"><span data-stu-id="c3012-649">4</span></span>

<span data-ttu-id="c3012-650">5</span><span class="sxs-lookup"><span data-stu-id="c3012-650">5</span></span>

<span data-ttu-id="c3012-651">6</span><span class="sxs-lookup"><span data-stu-id="c3012-651">6</span></span>

<span data-ttu-id="c3012-652">7</span><span class="sxs-lookup"><span data-stu-id="c3012-652">7</span></span>

<span data-ttu-id="c3012-653">8</span><span class="sxs-lookup"><span data-stu-id="c3012-653">8</span></span>

<span data-ttu-id="c3012-654">9</span><span class="sxs-lookup"><span data-stu-id="c3012-654">9</span></span>

<span data-ttu-id="c3012-655">1</span><span class="sxs-lookup"><span data-stu-id="c3012-655">1</span></span><br/> <span data-ttu-id="c3012-656">0</span><span class="sxs-lookup"><span data-stu-id="c3012-656">0</span></span><br/>

<span data-ttu-id="c3012-657">1</span><span class="sxs-lookup"><span data-stu-id="c3012-657">1</span></span>

<span data-ttu-id="c3012-658">2</span><span class="sxs-lookup"><span data-stu-id="c3012-658">2</span></span>

<span data-ttu-id="c3012-659">3</span><span class="sxs-lookup"><span data-stu-id="c3012-659">3</span></span>

<span data-ttu-id="c3012-660">4</span><span class="sxs-lookup"><span data-stu-id="c3012-660">4</span></span>

<span data-ttu-id="c3012-661">5</span><span class="sxs-lookup"><span data-stu-id="c3012-661">5</span></span>

<span data-ttu-id="c3012-662">6</span><span class="sxs-lookup"><span data-stu-id="c3012-662">6</span></span>

<span data-ttu-id="c3012-663">7</span><span class="sxs-lookup"><span data-stu-id="c3012-663">7</span></span>

<span data-ttu-id="c3012-664">8</span><span class="sxs-lookup"><span data-stu-id="c3012-664">8</span></span>

<span data-ttu-id="c3012-665">9</span><span class="sxs-lookup"><span data-stu-id="c3012-665">9</span></span>

<span data-ttu-id="c3012-666">2</span><span class="sxs-lookup"><span data-stu-id="c3012-666">2</span></span><br/> <span data-ttu-id="c3012-667">0</span><span class="sxs-lookup"><span data-stu-id="c3012-667">0</span></span><br/>

<span data-ttu-id="c3012-668">1</span><span class="sxs-lookup"><span data-stu-id="c3012-668">1</span></span>

<span data-ttu-id="c3012-669">2</span><span class="sxs-lookup"><span data-stu-id="c3012-669">2</span></span>

<span data-ttu-id="c3012-670">3</span><span class="sxs-lookup"><span data-stu-id="c3012-670">3</span></span>

<span data-ttu-id="c3012-671">4</span><span class="sxs-lookup"><span data-stu-id="c3012-671">4</span></span>

<span data-ttu-id="c3012-672">5</span><span class="sxs-lookup"><span data-stu-id="c3012-672">5</span></span>

<span data-ttu-id="c3012-673">6</span><span class="sxs-lookup"><span data-stu-id="c3012-673">6</span></span>

<span data-ttu-id="c3012-674">7</span><span class="sxs-lookup"><span data-stu-id="c3012-674">7</span></span>

<span data-ttu-id="c3012-675">8</span><span class="sxs-lookup"><span data-stu-id="c3012-675">8</span></span>

<span data-ttu-id="c3012-676">9</span><span class="sxs-lookup"><span data-stu-id="c3012-676">9</span></span>

<span data-ttu-id="c3012-677">3</span><span class="sxs-lookup"><span data-stu-id="c3012-677">3</span></span><br/> <span data-ttu-id="c3012-678">0</span><span class="sxs-lookup"><span data-stu-id="c3012-678">0</span></span><br/>

<span data-ttu-id="c3012-679">1</span><span class="sxs-lookup"><span data-stu-id="c3012-679">1</span></span>

<span data-ttu-id="c3012-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="c3012-680">vVectorElements</span></span>

<span data-ttu-id="c3012-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="c3012-681">vVectorData</span></span>



 

<span data-ttu-id="c3012-682">**vVectorElements**: inteiro de 32 bits sem sinal, indicando o número de elementos no campo vVectorData.</span><span class="sxs-lookup"><span data-stu-id="c3012-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="c3012-683">**vVectorData**: uma matriz de itens que têm um tipo indicado por vType com o bit 0x1000 limpo.</span><span class="sxs-lookup"><span data-stu-id="c3012-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="c3012-684">O tamanho de um item de comprimento fixo individual pode ser obtido da tabela de tipos de dados de comprimento fixo, conforme especificado na seção 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="c3012-685">O comprimento desse campo, em bytes, pode ser calculado multiplicando vVectorElements pelo tamanho de um item individual.</span><span class="sxs-lookup"><span data-stu-id="c3012-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="c3012-686">Para tipos de dados de comprimento variável, vVectorData contém uma sequência de tipos simples com marshaling consecutivo em que o tipo é indicado por vType com o bit 0x1000 limpo.</span><span class="sxs-lookup"><span data-stu-id="c3012-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="c3012-687">Isso inclui um caso especial indicado pela variante da \_ matriz \| VT vType VT \_ (ou seja, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="c3012-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="c3012-688">Os elementos no campo vVectorData devem ser separados por 0 a 3 bytes de preenchimento, de modo que cada elemento comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa matriz.</span><span class="sxs-lookup"><span data-stu-id="c3012-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="c3012-689">Se os bytes de preenchimento estiverem presentes, o valor que eles contêm será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="c3012-690">O conteúdo dos bytes de preenchimento deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-691">Para um vType definido como \_ variante de matriz VT de VT \| \_ , o tipo de itens nesta sequência é CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="c3012-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="c3012-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="c3012-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="c3012-693">SAFEARRAY é usado para passar matrizes multidimensionais.</span><span class="sxs-lookup"><span data-stu-id="c3012-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="c3012-694">A estrutura contém informações de tamanho de matriz, bem como os dados na matriz.</span><span class="sxs-lookup"><span data-stu-id="c3012-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="c3012-695">0</span><span class="sxs-lookup"><span data-stu-id="c3012-695">0</span></span>

<span data-ttu-id="c3012-696">1</span><span class="sxs-lookup"><span data-stu-id="c3012-696">1</span></span>

<span data-ttu-id="c3012-697">2</span><span class="sxs-lookup"><span data-stu-id="c3012-697">2</span></span>

<span data-ttu-id="c3012-698">3</span><span class="sxs-lookup"><span data-stu-id="c3012-698">3</span></span>

<span data-ttu-id="c3012-699">4</span><span class="sxs-lookup"><span data-stu-id="c3012-699">4</span></span>

<span data-ttu-id="c3012-700">5</span><span class="sxs-lookup"><span data-stu-id="c3012-700">5</span></span>

<span data-ttu-id="c3012-701">6</span><span class="sxs-lookup"><span data-stu-id="c3012-701">6</span></span>

<span data-ttu-id="c3012-702">7</span><span class="sxs-lookup"><span data-stu-id="c3012-702">7</span></span>

<span data-ttu-id="c3012-703">8</span><span class="sxs-lookup"><span data-stu-id="c3012-703">8</span></span>

<span data-ttu-id="c3012-704">9</span><span class="sxs-lookup"><span data-stu-id="c3012-704">9</span></span>

<span data-ttu-id="c3012-705">1</span><span class="sxs-lookup"><span data-stu-id="c3012-705">1</span></span><br/> <span data-ttu-id="c3012-706">0</span><span class="sxs-lookup"><span data-stu-id="c3012-706">0</span></span><br/>

<span data-ttu-id="c3012-707">1</span><span class="sxs-lookup"><span data-stu-id="c3012-707">1</span></span>

<span data-ttu-id="c3012-708">2</span><span class="sxs-lookup"><span data-stu-id="c3012-708">2</span></span>

<span data-ttu-id="c3012-709">3</span><span class="sxs-lookup"><span data-stu-id="c3012-709">3</span></span>

<span data-ttu-id="c3012-710">4</span><span class="sxs-lookup"><span data-stu-id="c3012-710">4</span></span>

<span data-ttu-id="c3012-711">5</span><span class="sxs-lookup"><span data-stu-id="c3012-711">5</span></span>

<span data-ttu-id="c3012-712">6</span><span class="sxs-lookup"><span data-stu-id="c3012-712">6</span></span>

<span data-ttu-id="c3012-713">7</span><span class="sxs-lookup"><span data-stu-id="c3012-713">7</span></span>

<span data-ttu-id="c3012-714">8</span><span class="sxs-lookup"><span data-stu-id="c3012-714">8</span></span>

<span data-ttu-id="c3012-715">9</span><span class="sxs-lookup"><span data-stu-id="c3012-715">9</span></span>

<span data-ttu-id="c3012-716">2</span><span class="sxs-lookup"><span data-stu-id="c3012-716">2</span></span><br/> <span data-ttu-id="c3012-717">0</span><span class="sxs-lookup"><span data-stu-id="c3012-717">0</span></span><br/>

<span data-ttu-id="c3012-718">1</span><span class="sxs-lookup"><span data-stu-id="c3012-718">1</span></span>

<span data-ttu-id="c3012-719">2</span><span class="sxs-lookup"><span data-stu-id="c3012-719">2</span></span>

<span data-ttu-id="c3012-720">3</span><span class="sxs-lookup"><span data-stu-id="c3012-720">3</span></span>

<span data-ttu-id="c3012-721">4</span><span class="sxs-lookup"><span data-stu-id="c3012-721">4</span></span>

<span data-ttu-id="c3012-722">5</span><span class="sxs-lookup"><span data-stu-id="c3012-722">5</span></span>

<span data-ttu-id="c3012-723">6</span><span class="sxs-lookup"><span data-stu-id="c3012-723">6</span></span>

<span data-ttu-id="c3012-724">7</span><span class="sxs-lookup"><span data-stu-id="c3012-724">7</span></span>

<span data-ttu-id="c3012-725">8</span><span class="sxs-lookup"><span data-stu-id="c3012-725">8</span></span>

<span data-ttu-id="c3012-726">9</span><span class="sxs-lookup"><span data-stu-id="c3012-726">9</span></span>

<span data-ttu-id="c3012-727">3</span><span class="sxs-lookup"><span data-stu-id="c3012-727">3</span></span><br/> <span data-ttu-id="c3012-728">0</span><span class="sxs-lookup"><span data-stu-id="c3012-728">0</span></span><br/>

<span data-ttu-id="c3012-729">1</span><span class="sxs-lookup"><span data-stu-id="c3012-729">1</span></span>

<span data-ttu-id="c3012-730">cDims</span><span class="sxs-lookup"><span data-stu-id="c3012-730">cDims</span></span>

<span data-ttu-id="c3012-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="c3012-731">fFeatures</span></span>

<span data-ttu-id="c3012-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="c3012-732">cbElements</span></span>

<span data-ttu-id="c3012-733">Rgsabound (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-733">Rgsabound (variable)</span></span>

<span data-ttu-id="c3012-734">vData (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-734">vData (variable)</span></span>



 

<span data-ttu-id="c3012-735">**cDims**: inteiro de 16 bits não assinado, indicando o número de dimensões da matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="c3012-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="c3012-736">**fFeatures**: um tele-bit de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="c3012-737">Os valores representam recursos, definidos por aplicativos de camada superior e devem ser ignorados.</span><span class="sxs-lookup"><span data-stu-id="c3012-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="c3012-738">**cbElements**: um inteiro de 32 bits sem sinal especificando o tamanho de cada elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="c3012-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="c3012-739">**Rgsabound**: uma matriz que contém uma estrutura SAFEARRAYBOUND, conforme especificado na seção 2.2.1.1.1.4, por dimensão em SafeArray.</span><span class="sxs-lookup"><span data-stu-id="c3012-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="c3012-740">Essa matriz tem a dimensão mais à esquerda primeiro e a dimensão mais à direita por último.</span><span class="sxs-lookup"><span data-stu-id="c3012-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="c3012-741">**vData**: um vetor de itens empacotados de um tipo específico, indicado pelo VType do CBaseStorageVariant que o contém, com o bit 0x2000 limpo.</span><span class="sxs-lookup"><span data-stu-id="c3012-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="c3012-742">o vData é empacotado de forma semelhante ao \_ vetor VT, conforme especificado na seção 2.2.1.1.1.2, com a diferença de que o número de itens não é armazenado na frente do vetor.</span><span class="sxs-lookup"><span data-stu-id="c3012-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="c3012-743">Em vez disso, o número de itens é calculado multiplicando-se o valor cElements por todos os limites de matrizes seguros fornecidos no campo rgsabound.</span><span class="sxs-lookup"><span data-stu-id="c3012-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="c3012-744">Os elementos são armazenados em um vetor em ordem de dimensões, iterando começando com a dimensão mais à direita.</span><span class="sxs-lookup"><span data-stu-id="c3012-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="c3012-745">O diagrama a seguir representa visualmente uma matriz bidimensional de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c3012-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="c3012-746">A primeira dimensão tem cElements igual a 4 (representada horizontalmente) e lLbound igual a 0, e a segunda dimensão tem cElements igual a 2 (representada verticalmente) e lLbound igual a 0.</span><span class="sxs-lookup"><span data-stu-id="c3012-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="c3012-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-747">0x00000001</span></span> | <span data-ttu-id="c3012-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-748">0x00000002</span></span> | <span data-ttu-id="c3012-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-749">0x00000003</span></span> | <span data-ttu-id="c3012-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3012-750">0x00000005</span></span> |
| <span data-ttu-id="c3012-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3012-751">0x00000007</span></span> | <span data-ttu-id="c3012-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3012-752">0x00000011</span></span> | <span data-ttu-id="c3012-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c3012-753">0x00000013</span></span> | <span data-ttu-id="c3012-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="c3012-754">0x00000017</span></span> |



 

<span data-ttu-id="c3012-755">Usando o diagrama acima, vData conterá a seguinte sequência: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (Iterando primeiro pela dimensão mais à direita e, em seguida, incrementando a próxima dimensão).</span><span class="sxs-lookup"><span data-stu-id="c3012-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="c3012-756">O rgsabound anterior (que registra cElements e LBound) seria: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="c3012-757">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="c3012-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="c3012-758">A estrutura SAFEARRAYBOUND representa os limites de uma dimensão de um SAFEARRAY ou SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="c3012-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="c3012-759">Seu formato é:</span><span class="sxs-lookup"><span data-stu-id="c3012-759">Its format is:</span></span>



<span data-ttu-id="c3012-760">0</span><span class="sxs-lookup"><span data-stu-id="c3012-760">0</span></span>

<span data-ttu-id="c3012-761">1</span><span class="sxs-lookup"><span data-stu-id="c3012-761">1</span></span>

<span data-ttu-id="c3012-762">2</span><span class="sxs-lookup"><span data-stu-id="c3012-762">2</span></span>

<span data-ttu-id="c3012-763">3</span><span class="sxs-lookup"><span data-stu-id="c3012-763">3</span></span>

<span data-ttu-id="c3012-764">4</span><span class="sxs-lookup"><span data-stu-id="c3012-764">4</span></span>

<span data-ttu-id="c3012-765">5</span><span class="sxs-lookup"><span data-stu-id="c3012-765">5</span></span>

<span data-ttu-id="c3012-766">6</span><span class="sxs-lookup"><span data-stu-id="c3012-766">6</span></span>

<span data-ttu-id="c3012-767">7</span><span class="sxs-lookup"><span data-stu-id="c3012-767">7</span></span>

<span data-ttu-id="c3012-768">8</span><span class="sxs-lookup"><span data-stu-id="c3012-768">8</span></span>

<span data-ttu-id="c3012-769">9</span><span class="sxs-lookup"><span data-stu-id="c3012-769">9</span></span>

<span data-ttu-id="c3012-770">1</span><span class="sxs-lookup"><span data-stu-id="c3012-770">1</span></span><br/> <span data-ttu-id="c3012-771">0</span><span class="sxs-lookup"><span data-stu-id="c3012-771">0</span></span><br/>

<span data-ttu-id="c3012-772">1</span><span class="sxs-lookup"><span data-stu-id="c3012-772">1</span></span>

<span data-ttu-id="c3012-773">2</span><span class="sxs-lookup"><span data-stu-id="c3012-773">2</span></span>

<span data-ttu-id="c3012-774">3</span><span class="sxs-lookup"><span data-stu-id="c3012-774">3</span></span>

<span data-ttu-id="c3012-775">4</span><span class="sxs-lookup"><span data-stu-id="c3012-775">4</span></span>

<span data-ttu-id="c3012-776">5</span><span class="sxs-lookup"><span data-stu-id="c3012-776">5</span></span>

<span data-ttu-id="c3012-777">6</span><span class="sxs-lookup"><span data-stu-id="c3012-777">6</span></span>

<span data-ttu-id="c3012-778">7</span><span class="sxs-lookup"><span data-stu-id="c3012-778">7</span></span>

<span data-ttu-id="c3012-779">8</span><span class="sxs-lookup"><span data-stu-id="c3012-779">8</span></span>

<span data-ttu-id="c3012-780">9</span><span class="sxs-lookup"><span data-stu-id="c3012-780">9</span></span>

<span data-ttu-id="c3012-781">2</span><span class="sxs-lookup"><span data-stu-id="c3012-781">2</span></span><br/> <span data-ttu-id="c3012-782">0</span><span class="sxs-lookup"><span data-stu-id="c3012-782">0</span></span><br/>

<span data-ttu-id="c3012-783">1</span><span class="sxs-lookup"><span data-stu-id="c3012-783">1</span></span>

<span data-ttu-id="c3012-784">2</span><span class="sxs-lookup"><span data-stu-id="c3012-784">2</span></span>

<span data-ttu-id="c3012-785">3</span><span class="sxs-lookup"><span data-stu-id="c3012-785">3</span></span>

<span data-ttu-id="c3012-786">4</span><span class="sxs-lookup"><span data-stu-id="c3012-786">4</span></span>

<span data-ttu-id="c3012-787">5</span><span class="sxs-lookup"><span data-stu-id="c3012-787">5</span></span>

<span data-ttu-id="c3012-788">6</span><span class="sxs-lookup"><span data-stu-id="c3012-788">6</span></span>

<span data-ttu-id="c3012-789">7</span><span class="sxs-lookup"><span data-stu-id="c3012-789">7</span></span>

<span data-ttu-id="c3012-790">8</span><span class="sxs-lookup"><span data-stu-id="c3012-790">8</span></span>

<span data-ttu-id="c3012-791">9</span><span class="sxs-lookup"><span data-stu-id="c3012-791">9</span></span>

<span data-ttu-id="c3012-792">3</span><span class="sxs-lookup"><span data-stu-id="c3012-792">3</span></span><br/> <span data-ttu-id="c3012-793">0</span><span class="sxs-lookup"><span data-stu-id="c3012-793">0</span></span><br/>

<span data-ttu-id="c3012-794">1</span><span class="sxs-lookup"><span data-stu-id="c3012-794">1</span></span>

<span data-ttu-id="c3012-795">cElements</span><span class="sxs-lookup"><span data-stu-id="c3012-795">cElements</span></span>

<span data-ttu-id="c3012-796">lLbound</span><span class="sxs-lookup"><span data-stu-id="c3012-796">lLbound</span></span>



 

<span data-ttu-id="c3012-797">**cElements**: um inteiro sem sinal de 32 bits, especificando o número de elementos na dimensão.</span><span class="sxs-lookup"><span data-stu-id="c3012-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="c3012-798">**lLbound**: um inteiro sem sinal de 32 bits, especificando o limite inferior da dimensão.</span><span class="sxs-lookup"><span data-stu-id="c3012-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="c3012-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="c3012-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="c3012-800">SAFEARRAY2 é usado para passar matrizes multidimensionais em SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="c3012-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="c3012-801">A estrutura contém informações de limite, bem como os dados.</span><span class="sxs-lookup"><span data-stu-id="c3012-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="c3012-802">0</span><span class="sxs-lookup"><span data-stu-id="c3012-802">0</span></span>

<span data-ttu-id="c3012-803">1</span><span class="sxs-lookup"><span data-stu-id="c3012-803">1</span></span>

<span data-ttu-id="c3012-804">2</span><span class="sxs-lookup"><span data-stu-id="c3012-804">2</span></span>

<span data-ttu-id="c3012-805">3</span><span class="sxs-lookup"><span data-stu-id="c3012-805">3</span></span>

<span data-ttu-id="c3012-806">4</span><span class="sxs-lookup"><span data-stu-id="c3012-806">4</span></span>

<span data-ttu-id="c3012-807">5</span><span class="sxs-lookup"><span data-stu-id="c3012-807">5</span></span>

<span data-ttu-id="c3012-808">6</span><span class="sxs-lookup"><span data-stu-id="c3012-808">6</span></span>

<span data-ttu-id="c3012-809">7</span><span class="sxs-lookup"><span data-stu-id="c3012-809">7</span></span>

<span data-ttu-id="c3012-810">8</span><span class="sxs-lookup"><span data-stu-id="c3012-810">8</span></span>

<span data-ttu-id="c3012-811">9</span><span class="sxs-lookup"><span data-stu-id="c3012-811">9</span></span>

<span data-ttu-id="c3012-812">1</span><span class="sxs-lookup"><span data-stu-id="c3012-812">1</span></span><br/> <span data-ttu-id="c3012-813">0</span><span class="sxs-lookup"><span data-stu-id="c3012-813">0</span></span><br/>

<span data-ttu-id="c3012-814">1</span><span class="sxs-lookup"><span data-stu-id="c3012-814">1</span></span>

<span data-ttu-id="c3012-815">2</span><span class="sxs-lookup"><span data-stu-id="c3012-815">2</span></span>

<span data-ttu-id="c3012-816">3</span><span class="sxs-lookup"><span data-stu-id="c3012-816">3</span></span>

<span data-ttu-id="c3012-817">4</span><span class="sxs-lookup"><span data-stu-id="c3012-817">4</span></span>

<span data-ttu-id="c3012-818">5</span><span class="sxs-lookup"><span data-stu-id="c3012-818">5</span></span>

<span data-ttu-id="c3012-819">6</span><span class="sxs-lookup"><span data-stu-id="c3012-819">6</span></span>

<span data-ttu-id="c3012-820">7</span><span class="sxs-lookup"><span data-stu-id="c3012-820">7</span></span>

<span data-ttu-id="c3012-821">8</span><span class="sxs-lookup"><span data-stu-id="c3012-821">8</span></span>

<span data-ttu-id="c3012-822">9</span><span class="sxs-lookup"><span data-stu-id="c3012-822">9</span></span>

<span data-ttu-id="c3012-823">2</span><span class="sxs-lookup"><span data-stu-id="c3012-823">2</span></span><br/> <span data-ttu-id="c3012-824">0</span><span class="sxs-lookup"><span data-stu-id="c3012-824">0</span></span><br/>

<span data-ttu-id="c3012-825">1</span><span class="sxs-lookup"><span data-stu-id="c3012-825">1</span></span>

<span data-ttu-id="c3012-826">2</span><span class="sxs-lookup"><span data-stu-id="c3012-826">2</span></span>

<span data-ttu-id="c3012-827">3</span><span class="sxs-lookup"><span data-stu-id="c3012-827">3</span></span>

<span data-ttu-id="c3012-828">4</span><span class="sxs-lookup"><span data-stu-id="c3012-828">4</span></span>

<span data-ttu-id="c3012-829">5</span><span class="sxs-lookup"><span data-stu-id="c3012-829">5</span></span>

<span data-ttu-id="c3012-830">6</span><span class="sxs-lookup"><span data-stu-id="c3012-830">6</span></span>

<span data-ttu-id="c3012-831">7</span><span class="sxs-lookup"><span data-stu-id="c3012-831">7</span></span>

<span data-ttu-id="c3012-832">8</span><span class="sxs-lookup"><span data-stu-id="c3012-832">8</span></span>

<span data-ttu-id="c3012-833">9</span><span class="sxs-lookup"><span data-stu-id="c3012-833">9</span></span>

<span data-ttu-id="c3012-834">3</span><span class="sxs-lookup"><span data-stu-id="c3012-834">3</span></span><br/> <span data-ttu-id="c3012-835">0</span><span class="sxs-lookup"><span data-stu-id="c3012-835">0</span></span><br/>

<span data-ttu-id="c3012-836">1</span><span class="sxs-lookup"><span data-stu-id="c3012-836">1</span></span>

<span data-ttu-id="c3012-837">cDims</span><span class="sxs-lookup"><span data-stu-id="c3012-837">cDims</span></span>

<span data-ttu-id="c3012-838">Rgsabound (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-838">Rgsabound (variable)</span></span>

<span data-ttu-id="c3012-839">vData (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-839">vData (variable)</span></span>



 

<span data-ttu-id="c3012-840">**cDims**: inteiro de 32 bits sem sinal, indicando o número de dimensões de SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="c3012-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="c3012-841">**Rgsabound**: uma matriz que contém uma estrutura SAFEARRAYBOUND, conforme especificado na seção 2.2.1.1.1.4 por dimensão no SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="c3012-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="c3012-842">Essa matriz tem a dimensão mais à esquerda primeiro e a dimensão mais à direita por último.</span><span class="sxs-lookup"><span data-stu-id="c3012-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="c3012-843">**vData**: um vetor de itens empacotados de um tipo específico, indicado pelo DWTYPE da SERIALIZEDPROPERTYVALUE que o contém, com o bit 0x2000 limpo.</span><span class="sxs-lookup"><span data-stu-id="c3012-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="c3012-844">O formato de vData é o mesmo que o especificado para o campo vData de SAFEARRAY na seção 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="c3012-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="c3012-845">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="c3012-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="c3012-846">A estrutura CFullPropSpec contém um GUID de conjunto de propriedades e um identificador de propriedade para identificar exclusivamente a propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="c3012-847">0</span><span class="sxs-lookup"><span data-stu-id="c3012-847">0</span></span>

<span data-ttu-id="c3012-848">1</span><span class="sxs-lookup"><span data-stu-id="c3012-848">1</span></span>

<span data-ttu-id="c3012-849">2</span><span class="sxs-lookup"><span data-stu-id="c3012-849">2</span></span>

<span data-ttu-id="c3012-850">3</span><span class="sxs-lookup"><span data-stu-id="c3012-850">3</span></span>

<span data-ttu-id="c3012-851">4</span><span class="sxs-lookup"><span data-stu-id="c3012-851">4</span></span>

<span data-ttu-id="c3012-852">5</span><span class="sxs-lookup"><span data-stu-id="c3012-852">5</span></span>

<span data-ttu-id="c3012-853">6</span><span class="sxs-lookup"><span data-stu-id="c3012-853">6</span></span>

<span data-ttu-id="c3012-854">7</span><span class="sxs-lookup"><span data-stu-id="c3012-854">7</span></span>

<span data-ttu-id="c3012-855">8</span><span class="sxs-lookup"><span data-stu-id="c3012-855">8</span></span>

<span data-ttu-id="c3012-856">9</span><span class="sxs-lookup"><span data-stu-id="c3012-856">9</span></span>

<span data-ttu-id="c3012-857">1</span><span class="sxs-lookup"><span data-stu-id="c3012-857">1</span></span><br/> <span data-ttu-id="c3012-858">0</span><span class="sxs-lookup"><span data-stu-id="c3012-858">0</span></span><br/>

<span data-ttu-id="c3012-859">1</span><span class="sxs-lookup"><span data-stu-id="c3012-859">1</span></span>

<span data-ttu-id="c3012-860">2</span><span class="sxs-lookup"><span data-stu-id="c3012-860">2</span></span>

<span data-ttu-id="c3012-861">3</span><span class="sxs-lookup"><span data-stu-id="c3012-861">3</span></span>

<span data-ttu-id="c3012-862">4</span><span class="sxs-lookup"><span data-stu-id="c3012-862">4</span></span>

<span data-ttu-id="c3012-863">5</span><span class="sxs-lookup"><span data-stu-id="c3012-863">5</span></span>

<span data-ttu-id="c3012-864">6</span><span class="sxs-lookup"><span data-stu-id="c3012-864">6</span></span>

<span data-ttu-id="c3012-865">7</span><span class="sxs-lookup"><span data-stu-id="c3012-865">7</span></span>

<span data-ttu-id="c3012-866">8</span><span class="sxs-lookup"><span data-stu-id="c3012-866">8</span></span>

<span data-ttu-id="c3012-867">9</span><span class="sxs-lookup"><span data-stu-id="c3012-867">9</span></span>

<span data-ttu-id="c3012-868">2</span><span class="sxs-lookup"><span data-stu-id="c3012-868">2</span></span><br/> <span data-ttu-id="c3012-869">0</span><span class="sxs-lookup"><span data-stu-id="c3012-869">0</span></span><br/>

<span data-ttu-id="c3012-870">1</span><span class="sxs-lookup"><span data-stu-id="c3012-870">1</span></span>

<span data-ttu-id="c3012-871">2</span><span class="sxs-lookup"><span data-stu-id="c3012-871">2</span></span>

<span data-ttu-id="c3012-872">3</span><span class="sxs-lookup"><span data-stu-id="c3012-872">3</span></span>

<span data-ttu-id="c3012-873">4</span><span class="sxs-lookup"><span data-stu-id="c3012-873">4</span></span>

<span data-ttu-id="c3012-874">5</span><span class="sxs-lookup"><span data-stu-id="c3012-874">5</span></span>

<span data-ttu-id="c3012-875">6</span><span class="sxs-lookup"><span data-stu-id="c3012-875">6</span></span>

<span data-ttu-id="c3012-876">7</span><span class="sxs-lookup"><span data-stu-id="c3012-876">7</span></span>

<span data-ttu-id="c3012-877">8</span><span class="sxs-lookup"><span data-stu-id="c3012-877">8</span></span>

<span data-ttu-id="c3012-878">9</span><span class="sxs-lookup"><span data-stu-id="c3012-878">9</span></span>

<span data-ttu-id="c3012-879">3</span><span class="sxs-lookup"><span data-stu-id="c3012-879">3</span></span><br/> <span data-ttu-id="c3012-880">0</span><span class="sxs-lookup"><span data-stu-id="c3012-880">0</span></span><br/>

<span data-ttu-id="c3012-881">1</span><span class="sxs-lookup"><span data-stu-id="c3012-881">1</span></span>

<span data-ttu-id="c3012-882">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="c3012-882">\_guidPropSet</span></span>

<span data-ttu-id="c3012-883">...</span><span class="sxs-lookup"><span data-stu-id="c3012-883">...</span></span>

<span data-ttu-id="c3012-884">...</span><span class="sxs-lookup"><span data-stu-id="c3012-884">...</span></span>

<span data-ttu-id="c3012-885">...</span><span class="sxs-lookup"><span data-stu-id="c3012-885">...</span></span>

<span data-ttu-id="c3012-886">ulKind</span><span class="sxs-lookup"><span data-stu-id="c3012-886">ulKind</span></span>

<span data-ttu-id="c3012-887">PrSpec</span><span class="sxs-lookup"><span data-stu-id="c3012-887">PrSpec</span></span>

<span data-ttu-id="c3012-888">Nome da propriedade (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-888">Property name (variable)</span></span>



 

<span data-ttu-id="c3012-889">**\_ guidPropSet**: o GUID do conjunto de propriedades ao qual a propriedade pertence.</span><span class="sxs-lookup"><span data-stu-id="c3012-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="c3012-890">**ulKind**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3012-891">Um dos seguintes valores abaixo, que indica o conteúdo de PrSpec.</span><span class="sxs-lookup"><span data-stu-id="c3012-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="c3012-892">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-892">Value</span></span>                                            | <span data-ttu-id="c3012-893">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-894">\_LPWSTR PRSPEC</span><span class="sxs-lookup"><span data-stu-id="c3012-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="c3012-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-895">0x00000000</span></span><br/> | <span data-ttu-id="c3012-896">O campo PrSpec especifica o número de caracteres não nulos no campo nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="c3012-897">\_Propid PRSPEC</span><span class="sxs-lookup"><span data-stu-id="c3012-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="c3012-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-898">0x00000001</span></span><br/>  | <span data-ttu-id="c3012-899">O campo PrSpec especifica a ID da propriedade (PROPID).</span><span class="sxs-lookup"><span data-stu-id="c3012-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="c3012-900">**PrSpec**: um inteiro sem sinal de 32 bits com um significado, conforme indicado pelo campo ulKind.</span><span class="sxs-lookup"><span data-stu-id="c3012-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="c3012-901">**Nome da propriedade**: se ulKind for definido como PRSPEC \_ Propid, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="c3012-902">Se ulKind for definido como PRSPEC \_ LPWStr, esse campo deverá conter uma matriz que não diferencia maiúsculas de minúsculas de caracteres Unicode não nulos de PRSPEC, contendo o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="c3012-903">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="c3012-904">A estrutura CContentRestriction contém uma cadeia de caracteres para corresponder a uma propriedade no cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3012-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="c3012-905">0</span><span class="sxs-lookup"><span data-stu-id="c3012-905">0</span></span>

<span data-ttu-id="c3012-906">1</span><span class="sxs-lookup"><span data-stu-id="c3012-906">1</span></span>

<span data-ttu-id="c3012-907">2</span><span class="sxs-lookup"><span data-stu-id="c3012-907">2</span></span>

<span data-ttu-id="c3012-908">3</span><span class="sxs-lookup"><span data-stu-id="c3012-908">3</span></span>

<span data-ttu-id="c3012-909">4</span><span class="sxs-lookup"><span data-stu-id="c3012-909">4</span></span>

<span data-ttu-id="c3012-910">5</span><span class="sxs-lookup"><span data-stu-id="c3012-910">5</span></span>

<span data-ttu-id="c3012-911">6</span><span class="sxs-lookup"><span data-stu-id="c3012-911">6</span></span>

<span data-ttu-id="c3012-912">7</span><span class="sxs-lookup"><span data-stu-id="c3012-912">7</span></span>

<span data-ttu-id="c3012-913">8</span><span class="sxs-lookup"><span data-stu-id="c3012-913">8</span></span>

<span data-ttu-id="c3012-914">9</span><span class="sxs-lookup"><span data-stu-id="c3012-914">9</span></span>

<span data-ttu-id="c3012-915">1</span><span class="sxs-lookup"><span data-stu-id="c3012-915">1</span></span><br/> <span data-ttu-id="c3012-916">0</span><span class="sxs-lookup"><span data-stu-id="c3012-916">0</span></span><br/>

<span data-ttu-id="c3012-917">1</span><span class="sxs-lookup"><span data-stu-id="c3012-917">1</span></span>

<span data-ttu-id="c3012-918">2</span><span class="sxs-lookup"><span data-stu-id="c3012-918">2</span></span>

<span data-ttu-id="c3012-919">3</span><span class="sxs-lookup"><span data-stu-id="c3012-919">3</span></span>

<span data-ttu-id="c3012-920">4</span><span class="sxs-lookup"><span data-stu-id="c3012-920">4</span></span>

<span data-ttu-id="c3012-921">5</span><span class="sxs-lookup"><span data-stu-id="c3012-921">5</span></span>

<span data-ttu-id="c3012-922">6</span><span class="sxs-lookup"><span data-stu-id="c3012-922">6</span></span>

<span data-ttu-id="c3012-923">7</span><span class="sxs-lookup"><span data-stu-id="c3012-923">7</span></span>

<span data-ttu-id="c3012-924">8</span><span class="sxs-lookup"><span data-stu-id="c3012-924">8</span></span>

<span data-ttu-id="c3012-925">9</span><span class="sxs-lookup"><span data-stu-id="c3012-925">9</span></span>

<span data-ttu-id="c3012-926">2</span><span class="sxs-lookup"><span data-stu-id="c3012-926">2</span></span><br/> <span data-ttu-id="c3012-927">0</span><span class="sxs-lookup"><span data-stu-id="c3012-927">0</span></span><br/>

<span data-ttu-id="c3012-928">1</span><span class="sxs-lookup"><span data-stu-id="c3012-928">1</span></span>

<span data-ttu-id="c3012-929">2</span><span class="sxs-lookup"><span data-stu-id="c3012-929">2</span></span>

<span data-ttu-id="c3012-930">3</span><span class="sxs-lookup"><span data-stu-id="c3012-930">3</span></span>

<span data-ttu-id="c3012-931">4</span><span class="sxs-lookup"><span data-stu-id="c3012-931">4</span></span>

<span data-ttu-id="c3012-932">5</span><span class="sxs-lookup"><span data-stu-id="c3012-932">5</span></span>

<span data-ttu-id="c3012-933">6</span><span class="sxs-lookup"><span data-stu-id="c3012-933">6</span></span>

<span data-ttu-id="c3012-934">7</span><span class="sxs-lookup"><span data-stu-id="c3012-934">7</span></span>

<span data-ttu-id="c3012-935">8</span><span class="sxs-lookup"><span data-stu-id="c3012-935">8</span></span>

<span data-ttu-id="c3012-936">9</span><span class="sxs-lookup"><span data-stu-id="c3012-936">9</span></span>

<span data-ttu-id="c3012-937">3</span><span class="sxs-lookup"><span data-stu-id="c3012-937">3</span></span><br/> <span data-ttu-id="c3012-938">0</span><span class="sxs-lookup"><span data-stu-id="c3012-938">0</span></span><br/>

<span data-ttu-id="c3012-939">1</span><span class="sxs-lookup"><span data-stu-id="c3012-939">1</span></span>

<span data-ttu-id="c3012-940">\_Propriedade (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-940">\_Property (variable)</span></span>

<span data-ttu-id="c3012-941">...</span><span class="sxs-lookup"><span data-stu-id="c3012-941">...</span></span>

<span data-ttu-id="c3012-942">Padding1 (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-942">Padding1 (variable)</span></span>

<span data-ttu-id="c3012-943">Cc</span><span class="sxs-lookup"><span data-stu-id="c3012-943">Cc</span></span>

<span data-ttu-id="c3012-944">\_pwcsPhrase (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="c3012-945">...</span><span class="sxs-lookup"><span data-stu-id="c3012-945">...</span></span>

<span data-ttu-id="c3012-946">Padding2 (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-946">Padding2 (variable)</span></span>

<span data-ttu-id="c3012-947">lcid</span><span class="sxs-lookup"><span data-stu-id="c3012-947">lcid</span></span>

<span data-ttu-id="c3012-948">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="c3012-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="c3012-949">**\_ Propriedade**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="c3012-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="c3012-950">Este campo indica a propriedade na qual executar uma operação de correspondência.</span><span class="sxs-lookup"><span data-stu-id="c3012-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="c3012-951">**Padding1**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3012-952">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="c3012-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3012-953">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3012-954">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-955">**CC**: um inteiro de 32 bits sem sinal, especificando o número de caracteres no \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="c3012-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="c3012-956">**\_ pwcsPhrase**: uma cadeia de caracteres Unicode não terminada em nulo que representa a palavra ou frase para corresponder à propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="c3012-957">Este campo não deve estar vazio.</span><span class="sxs-lookup"><span data-stu-id="c3012-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="c3012-958">O campo Cc contém o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c3012-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="c3012-959">**Padding2**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3012-960">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="c3012-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3012-961">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3012-962">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-963">**LCID**: um inteiro sem sinal de 32 bits, indicando a localidade de \_ pwcsPhrase, conforme especificado em \[ MS-GPSI \] Apêndice A.</span><span class="sxs-lookup"><span data-stu-id="c3012-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="c3012-964">**\_ ulGenerateMethod**: um inteiro sem sinal de 32 bits, especificando o método a ser usado ao gerar formulários alternativos de palavra</span><span class="sxs-lookup"><span data-stu-id="c3012-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="c3012-965">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-965">Value</span></span>                                                       | <span data-ttu-id="c3012-966">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-967">GERAR \_ método \_ exato</span><span class="sxs-lookup"><span data-stu-id="c3012-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="c3012-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-968">0x00000000</span></span><br/>    | <span data-ttu-id="c3012-969">Correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="c3012-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c3012-970">GERAR \_ prefixo de método \_</span><span class="sxs-lookup"><span data-stu-id="c3012-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="c3012-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-971">0x00000001</span></span> <br/>  | <span data-ttu-id="c3012-972">Correspondência de prefixo.</span><span class="sxs-lookup"><span data-stu-id="c3012-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c3012-973">GERAR \_ método \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="c3012-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="c3012-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-974">0x00000002</span></span><br/> | <span data-ttu-id="c3012-975">Faz a correspondência de inflexões de uma palavra.</span><span class="sxs-lookup"><span data-stu-id="c3012-975">Matches inflections of a word.</span></span> <span data-ttu-id="c3012-976">Uma inflexão de uma palavra é uma variante da palavra raiz na mesma parte da fala que foi modificada de acordo com as regras linguísticas de um determinado idioma.</span><span class="sxs-lookup"><span data-stu-id="c3012-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="c3012-977">Por exemplo, as inflexidades do verbo "nada" em inglês incluem "nada", "nada", "nada" e "Swam".</span><span class="sxs-lookup"><span data-stu-id="c3012-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="c3012-978">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="c3012-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="c3012-979">A estrutura CKey contém um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="c3012-980">0</span><span class="sxs-lookup"><span data-stu-id="c3012-980">0</span></span>

<span data-ttu-id="c3012-981">1</span><span class="sxs-lookup"><span data-stu-id="c3012-981">1</span></span>

<span data-ttu-id="c3012-982">2</span><span class="sxs-lookup"><span data-stu-id="c3012-982">2</span></span>

<span data-ttu-id="c3012-983">3</span><span class="sxs-lookup"><span data-stu-id="c3012-983">3</span></span>

<span data-ttu-id="c3012-984">4</span><span class="sxs-lookup"><span data-stu-id="c3012-984">4</span></span>

<span data-ttu-id="c3012-985">5</span><span class="sxs-lookup"><span data-stu-id="c3012-985">5</span></span>

<span data-ttu-id="c3012-986">6</span><span class="sxs-lookup"><span data-stu-id="c3012-986">6</span></span>

<span data-ttu-id="c3012-987">7</span><span class="sxs-lookup"><span data-stu-id="c3012-987">7</span></span>

<span data-ttu-id="c3012-988">8</span><span class="sxs-lookup"><span data-stu-id="c3012-988">8</span></span>

<span data-ttu-id="c3012-989">9</span><span class="sxs-lookup"><span data-stu-id="c3012-989">9</span></span>

<span data-ttu-id="c3012-990">1</span><span class="sxs-lookup"><span data-stu-id="c3012-990">1</span></span><br/> <span data-ttu-id="c3012-991">0</span><span class="sxs-lookup"><span data-stu-id="c3012-991">0</span></span><br/>

<span data-ttu-id="c3012-992">1</span><span class="sxs-lookup"><span data-stu-id="c3012-992">1</span></span>

<span data-ttu-id="c3012-993">2</span><span class="sxs-lookup"><span data-stu-id="c3012-993">2</span></span>

<span data-ttu-id="c3012-994">3</span><span class="sxs-lookup"><span data-stu-id="c3012-994">3</span></span>

<span data-ttu-id="c3012-995">4</span><span class="sxs-lookup"><span data-stu-id="c3012-995">4</span></span>

<span data-ttu-id="c3012-996">5</span><span class="sxs-lookup"><span data-stu-id="c3012-996">5</span></span>

<span data-ttu-id="c3012-997">6</span><span class="sxs-lookup"><span data-stu-id="c3012-997">6</span></span>

<span data-ttu-id="c3012-998">7</span><span class="sxs-lookup"><span data-stu-id="c3012-998">7</span></span>

<span data-ttu-id="c3012-999">8</span><span class="sxs-lookup"><span data-stu-id="c3012-999">8</span></span>

<span data-ttu-id="c3012-1000">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1000">9</span></span>

<span data-ttu-id="c3012-1001">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1001">2</span></span><br/> <span data-ttu-id="c3012-1002">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1002">0</span></span><br/>

<span data-ttu-id="c3012-1003">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1003">1</span></span>

<span data-ttu-id="c3012-1004">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1004">2</span></span>

<span data-ttu-id="c3012-1005">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1005">3</span></span>

<span data-ttu-id="c3012-1006">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1006">4</span></span>

<span data-ttu-id="c3012-1007">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1007">5</span></span>

<span data-ttu-id="c3012-1008">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1008">6</span></span>

<span data-ttu-id="c3012-1009">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1009">7</span></span>

<span data-ttu-id="c3012-1010">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1010">8</span></span>

<span data-ttu-id="c3012-1011">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1011">9</span></span>

<span data-ttu-id="c3012-1012">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1012">3</span></span><br/> <span data-ttu-id="c3012-1013">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1013">0</span></span><br/>

<span data-ttu-id="c3012-1014">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1014">1</span></span>

<span data-ttu-id="c3012-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="c3012-1015">PROPID</span></span>

<span data-ttu-id="c3012-1016">CB</span><span class="sxs-lookup"><span data-stu-id="c3012-1016">Cb</span></span>

<span data-ttu-id="c3012-1017">buf (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1017">buf (variable)</span></span>



 

<span data-ttu-id="c3012-1018">**Propid**: um inteiro sem sinal de 32 bits, que representa a ID da propriedade, conforme discutido na seção 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="c3012-1019">Os valores bem conhecidos são:</span><span class="sxs-lookup"><span data-stu-id="c3012-1019">Well-known values are:</span></span>



| <span data-ttu-id="c3012-1020">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1020">Value</span></span>      | <span data-ttu-id="c3012-1021">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="c3012-1022">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c3012-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="c3012-1023">Representa uma ID de propriedade inválida e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="c3012-1024">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="c3012-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="c3012-1025">Representa uma ID de propriedade inválida e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="c3012-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-1026">0x00000000</span></span> | <span data-ttu-id="c3012-1027">Representa qualquer ID de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="c3012-1028">**CB**: um inteiro sem sinal de 32 bits contendo o comprimento de buf, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="c3012-1029">**buf**: uma sequência de bytes que representa o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="c3012-1030">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="c3012-1031">A estrutura CInternalPropertyRestriction contém um valor de propriedade para corresponder a uma operação.</span><span class="sxs-lookup"><span data-stu-id="c3012-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="c3012-1032">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1032">0</span></span>

<span data-ttu-id="c3012-1033">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1033">1</span></span>

<span data-ttu-id="c3012-1034">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1034">2</span></span>

<span data-ttu-id="c3012-1035">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1035">3</span></span>

<span data-ttu-id="c3012-1036">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1036">4</span></span>

<span data-ttu-id="c3012-1037">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1037">5</span></span>

<span data-ttu-id="c3012-1038">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1038">6</span></span>

<span data-ttu-id="c3012-1039">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1039">7</span></span>

<span data-ttu-id="c3012-1040">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1040">8</span></span>

<span data-ttu-id="c3012-1041">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1041">9</span></span>

<span data-ttu-id="c3012-1042">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1042">1</span></span><br/> <span data-ttu-id="c3012-1043">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1043">0</span></span><br/>

<span data-ttu-id="c3012-1044">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1044">1</span></span>

<span data-ttu-id="c3012-1045">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1045">2</span></span>

<span data-ttu-id="c3012-1046">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1046">3</span></span>

<span data-ttu-id="c3012-1047">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1047">4</span></span>

<span data-ttu-id="c3012-1048">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1048">5</span></span>

<span data-ttu-id="c3012-1049">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1049">6</span></span>

<span data-ttu-id="c3012-1050">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1050">7</span></span>

<span data-ttu-id="c3012-1051">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1051">8</span></span>

<span data-ttu-id="c3012-1052">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1052">9</span></span>

<span data-ttu-id="c3012-1053">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1053">2</span></span><br/> <span data-ttu-id="c3012-1054">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1054">0</span></span><br/>

<span data-ttu-id="c3012-1055">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1055">1</span></span>

<span data-ttu-id="c3012-1056">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1056">2</span></span>

<span data-ttu-id="c3012-1057">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1057">3</span></span>

<span data-ttu-id="c3012-1058">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1058">4</span></span>

<span data-ttu-id="c3012-1059">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1059">5</span></span>

<span data-ttu-id="c3012-1060">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1060">6</span></span>

<span data-ttu-id="c3012-1061">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1061">7</span></span>

<span data-ttu-id="c3012-1062">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1062">8</span></span>

<span data-ttu-id="c3012-1063">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1063">9</span></span>

<span data-ttu-id="c3012-1064">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1064">3</span></span><br/> <span data-ttu-id="c3012-1065">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1065">0</span></span><br/>

<span data-ttu-id="c3012-1066">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1066">1</span></span>

<span data-ttu-id="c3012-1067">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="c3012-1067">\_relop</span></span>

<span data-ttu-id="c3012-1068">\_pessoal</span><span class="sxs-lookup"><span data-stu-id="c3012-1068">\_pid</span></span>

<span data-ttu-id="c3012-1069">\_prval (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1069">\_prval (variable)</span></span>

<span data-ttu-id="c3012-1070">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="c3012-1070">restrictionPresent</span></span>

<span data-ttu-id="c3012-1071">nextRestriction (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="c3012-1072">**\_ RelOp**: um inteiro de 32 bits especificando a relação a ser executada na propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="c3012-1073">DEVE ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c3012-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="c3012-1074">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1074">Value</span></span>                 | <span data-ttu-id="c3012-1075">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-1076">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="c3012-1077">Uma comparação menor que.</span><span class="sxs-lookup"><span data-stu-id="c3012-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3012-1078">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="c3012-1079">Uma comparação menor que ou igual a.</span><span class="sxs-lookup"><span data-stu-id="c3012-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="c3012-1080">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="c3012-1081">Uma comparação maior que.</span><span class="sxs-lookup"><span data-stu-id="c3012-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="c3012-1082">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="c3012-1083">Uma comparação maior que ou igual a.</span><span class="sxs-lookup"><span data-stu-id="c3012-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="c3012-1084">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="c3012-1085">Uma comparação de igualdade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3012-1086">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3012-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="c3012-1087">Uma comparação diferente de.</span><span class="sxs-lookup"><span data-stu-id="c3012-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3012-1088">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="c3012-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="c3012-1089">Uma comparação de expressão regular.</span><span class="sxs-lookup"><span data-stu-id="c3012-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="c3012-1090">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3012-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="c3012-1091">Um operador e bit que retorna o operando à direita.</span><span class="sxs-lookup"><span data-stu-id="c3012-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="c3012-1092">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3012-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="c3012-1093">Um valor bit e AND que retorna um Value diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c3012-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="c3012-1094">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="c3012-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="c3012-1095">A operação deve ser executada em uma coluna de um conjunto de linhas e só será verdadeira se a operação for verdadeira para todas as linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="c3012-1096">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="c3012-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="c3012-1097">A operação deve ser executada em uma coluna de um conjunto de linhas e será true se a operação for verdadeira para qualquer linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="c3012-1098">**\_ pid**: um inteiro de 32 bits sem sinal, representando a ID da propriedade (consulte Propid na seção 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="c3012-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="c3012-1099">**\_ prval**: um CBaseStorageVariant que contém o valor a ser relacionado à propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="c3012-1100">**restrictionPresent**: um valor de byte que indica se o campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="c3012-1101">DEVE ser definido como 0x00 ou 0x01.</span><span class="sxs-lookup"><span data-stu-id="c3012-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="c3012-1102">Se definido como 0x01, restrictionPresent indica que o campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="c3012-1103">Se definido como 0x00, restrictionPresent indica que o campo nextRestriction não está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="c3012-1104">**nextRestriction**: uma estrutura CRestriction, conforme especificado na seção 2.2.1.16, especificando uma restrição adicional.</span><span class="sxs-lookup"><span data-stu-id="c3012-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="c3012-1105">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="c3012-1106">A estrutura CNatLanguageRestriction contém uma **consulta de linguagem natural** correspondente a uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="c3012-1107">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1107">0</span></span>

<span data-ttu-id="c3012-1108">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1108">1</span></span>

<span data-ttu-id="c3012-1109">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1109">2</span></span>

<span data-ttu-id="c3012-1110">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1110">3</span></span>

<span data-ttu-id="c3012-1111">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1111">4</span></span>

<span data-ttu-id="c3012-1112">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1112">5</span></span>

<span data-ttu-id="c3012-1113">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1113">6</span></span>

<span data-ttu-id="c3012-1114">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1114">7</span></span>

<span data-ttu-id="c3012-1115">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1115">8</span></span>

<span data-ttu-id="c3012-1116">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1116">9</span></span>

<span data-ttu-id="c3012-1117">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1117">1</span></span><br/> <span data-ttu-id="c3012-1118">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1118">0</span></span><br/>

<span data-ttu-id="c3012-1119">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1119">1</span></span>

<span data-ttu-id="c3012-1120">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1120">2</span></span>

<span data-ttu-id="c3012-1121">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1121">3</span></span>

<span data-ttu-id="c3012-1122">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1122">4</span></span>

<span data-ttu-id="c3012-1123">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1123">5</span></span>

<span data-ttu-id="c3012-1124">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1124">6</span></span>

<span data-ttu-id="c3012-1125">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1125">7</span></span>

<span data-ttu-id="c3012-1126">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1126">8</span></span>

<span data-ttu-id="c3012-1127">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1127">9</span></span>

<span data-ttu-id="c3012-1128">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1128">2</span></span><br/> <span data-ttu-id="c3012-1129">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1129">0</span></span><br/>

<span data-ttu-id="c3012-1130">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1130">1</span></span>

<span data-ttu-id="c3012-1131">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1131">2</span></span>

<span data-ttu-id="c3012-1132">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1132">3</span></span>

<span data-ttu-id="c3012-1133">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1133">4</span></span>

<span data-ttu-id="c3012-1134">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1134">5</span></span>

<span data-ttu-id="c3012-1135">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1135">6</span></span>

<span data-ttu-id="c3012-1136">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1136">7</span></span>

<span data-ttu-id="c3012-1137">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1137">8</span></span>

<span data-ttu-id="c3012-1138">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1138">9</span></span>

<span data-ttu-id="c3012-1139">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1139">3</span></span><br/> <span data-ttu-id="c3012-1140">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1140">0</span></span><br/>

<span data-ttu-id="c3012-1141">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1141">1</span></span>

<span data-ttu-id="c3012-1142">\_Propriedade (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1142">\_Property (variable)</span></span>

<span data-ttu-id="c3012-1143">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1143">...</span></span>

<span data-ttu-id="c3012-1144">\_preenchimento \_ de CC (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="c3012-1145">Cc</span><span class="sxs-lookup"><span data-stu-id="c3012-1145">Cc</span></span>

<span data-ttu-id="c3012-1146">\_pwcsPhrase (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="c3012-1147">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1147">...</span></span>

<span data-ttu-id="c3012-1148">\_\_LCID de preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="c3012-1149">Lcid</span><span class="sxs-lookup"><span data-stu-id="c3012-1149">Lcid</span></span>



 

<span data-ttu-id="c3012-1150">**\_ Propriedade**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="c3012-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="c3012-1151">Este campo indica a propriedade na qual executar a operação de correspondência.</span><span class="sxs-lookup"><span data-stu-id="c3012-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="c3012-1152">**\_ preenchimento \_ CC**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3012-1153">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="c3012-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3012-1154">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3012-1155">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-1156">**CC**: um inteiro de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3012-1157">O número de caracteres no \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="c3012-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="c3012-1158">**\_ pwcsPhrase**: uma cadeia de caracteres Unicode não terminada em nulo que representa a palavra ou frase para corresponder à propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="c3012-1159">Não deve ficar vazio.</span><span class="sxs-lookup"><span data-stu-id="c3012-1159">MUST NOT be empty.</span></span> <span data-ttu-id="c3012-1160">O campo Cc contém o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c3012-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="c3012-1161">**\_ \_ LCID de preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3012-1162">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="c3012-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3012-1163">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3012-1164">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-1165">**LCID**: um inteiro de 32 bits sem sinal indicando a localidade de \_ pwcsPhrase, conforme especificado no \[ Apêndice a do MS-GPSI \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="c3012-1166">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="c3012-1167">A estrutura CNodeRestriction contém uma matriz de nós de **árvore de comando** que especificam as restrições para a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="c3012-1168">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1168">0</span></span>

<span data-ttu-id="c3012-1169">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1169">1</span></span>

<span data-ttu-id="c3012-1170">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1170">2</span></span>

<span data-ttu-id="c3012-1171">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1171">3</span></span>

<span data-ttu-id="c3012-1172">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1172">4</span></span>

<span data-ttu-id="c3012-1173">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1173">5</span></span>

<span data-ttu-id="c3012-1174">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1174">6</span></span>

<span data-ttu-id="c3012-1175">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1175">7</span></span>

<span data-ttu-id="c3012-1176">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1176">8</span></span>

<span data-ttu-id="c3012-1177">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1177">9</span></span>

<span data-ttu-id="c3012-1178">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1178">1</span></span><br/> <span data-ttu-id="c3012-1179">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1179">0</span></span><br/>

<span data-ttu-id="c3012-1180">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1180">1</span></span>

<span data-ttu-id="c3012-1181">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1181">2</span></span>

<span data-ttu-id="c3012-1182">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1182">3</span></span>

<span data-ttu-id="c3012-1183">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1183">4</span></span>

<span data-ttu-id="c3012-1184">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1184">5</span></span>

<span data-ttu-id="c3012-1185">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1185">6</span></span>

<span data-ttu-id="c3012-1186">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1186">7</span></span>

<span data-ttu-id="c3012-1187">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1187">8</span></span>

<span data-ttu-id="c3012-1188">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1188">9</span></span>

<span data-ttu-id="c3012-1189">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1189">2</span></span><br/> <span data-ttu-id="c3012-1190">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1190">0</span></span><br/>

<span data-ttu-id="c3012-1191">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1191">1</span></span>

<span data-ttu-id="c3012-1192">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1192">2</span></span>

<span data-ttu-id="c3012-1193">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1193">3</span></span>

<span data-ttu-id="c3012-1194">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1194">4</span></span>

<span data-ttu-id="c3012-1195">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1195">5</span></span>

<span data-ttu-id="c3012-1196">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1196">6</span></span>

<span data-ttu-id="c3012-1197">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1197">7</span></span>

<span data-ttu-id="c3012-1198">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1198">8</span></span>

<span data-ttu-id="c3012-1199">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1199">9</span></span>

<span data-ttu-id="c3012-1200">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1200">3</span></span><br/> <span data-ttu-id="c3012-1201">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1201">0</span></span><br/>

<span data-ttu-id="c3012-1202">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1202">1</span></span>

<span data-ttu-id="c3012-1203">\_cNode</span><span class="sxs-lookup"><span data-stu-id="c3012-1203">\_cNode</span></span>

<span data-ttu-id="c3012-1204">\_paNode (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="c3012-1205">**\_ cNode**: um inteiro sem sinal de 32 bits especificando o número de estruturas CRestriction contidas no \_ campo paNode.</span><span class="sxs-lookup"><span data-stu-id="c3012-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="c3012-1206">**\_ paNode**: uma matriz de estruturas CRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="c3012-1207">As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa matriz.</span><span class="sxs-lookup"><span data-stu-id="c3012-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="c3012-1208">Se os bytes de preenchimento estiverem presentes, o valor que eles contêm será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="c3012-1209">O conteúdo dos bytes de preenchimento deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="c3012-1210">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="c3012-1211">A estrutura COccRestriction contém o local de uma palavra em uma frase.</span><span class="sxs-lookup"><span data-stu-id="c3012-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="c3012-1212">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1212">0</span></span>

<span data-ttu-id="c3012-1213">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1213">1</span></span>

<span data-ttu-id="c3012-1214">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1214">2</span></span>

<span data-ttu-id="c3012-1215">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1215">3</span></span>

<span data-ttu-id="c3012-1216">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1216">4</span></span>

<span data-ttu-id="c3012-1217">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1217">5</span></span>

<span data-ttu-id="c3012-1218">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1218">6</span></span>

<span data-ttu-id="c3012-1219">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1219">7</span></span>

<span data-ttu-id="c3012-1220">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1220">8</span></span>

<span data-ttu-id="c3012-1221">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1221">9</span></span>

<span data-ttu-id="c3012-1222">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1222">1</span></span><br/> <span data-ttu-id="c3012-1223">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1223">0</span></span><br/>

<span data-ttu-id="c3012-1224">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1224">1</span></span>

<span data-ttu-id="c3012-1225">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1225">2</span></span>

<span data-ttu-id="c3012-1226">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1226">3</span></span>

<span data-ttu-id="c3012-1227">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1227">4</span></span>

<span data-ttu-id="c3012-1228">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1228">5</span></span>

<span data-ttu-id="c3012-1229">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1229">6</span></span>

<span data-ttu-id="c3012-1230">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1230">7</span></span>

<span data-ttu-id="c3012-1231">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1231">8</span></span>

<span data-ttu-id="c3012-1232">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1232">9</span></span>

<span data-ttu-id="c3012-1233">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1233">2</span></span><br/> <span data-ttu-id="c3012-1234">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1234">0</span></span><br/>

<span data-ttu-id="c3012-1235">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1235">1</span></span>

<span data-ttu-id="c3012-1236">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1236">2</span></span>

<span data-ttu-id="c3012-1237">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1237">3</span></span>

<span data-ttu-id="c3012-1238">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1238">4</span></span>

<span data-ttu-id="c3012-1239">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1239">5</span></span>

<span data-ttu-id="c3012-1240">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1240">6</span></span>

<span data-ttu-id="c3012-1241">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1241">7</span></span>

<span data-ttu-id="c3012-1242">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1242">8</span></span>

<span data-ttu-id="c3012-1243">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1243">9</span></span>

<span data-ttu-id="c3012-1244">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1244">3</span></span><br/> <span data-ttu-id="c3012-1245">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1245">0</span></span><br/>

<span data-ttu-id="c3012-1246">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1246">1</span></span>

<span data-ttu-id="c3012-1247">\_OCC</span><span class="sxs-lookup"><span data-stu-id="c3012-1247">\_occ</span></span>

<span data-ttu-id="c3012-1248">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="c3012-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="c3012-1249">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="c3012-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="c3012-1250">**\_ OCC**: um inteiro de 32 bits sem sinal especificando o deslocamento da palavra em uma cadeia de caracteres de consulta, em unidades de palavras.</span><span class="sxs-lookup"><span data-stu-id="c3012-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="c3012-1251">Uma palavra, conforme usada nesta especificação, é uma unidade de linguagem em qualquer localidade que tenha significado.</span><span class="sxs-lookup"><span data-stu-id="c3012-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="c3012-1252">**\_ cPrevNoiseWords**: um inteiro sem sinal de 32 bits contendo o número de **palavras de ruído** que ocorrem entre esta palavra e a palavra anterior na frase.</span><span class="sxs-lookup"><span data-stu-id="c3012-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="c3012-1253">**\_ cNextNoiseWords**: um inteiro sem sinal de 32 bits contendo o número de palavras de ruído que ocorrem entre esta palavra e a próxima palavra na frase.</span><span class="sxs-lookup"><span data-stu-id="c3012-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="c3012-1254">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="c3012-1255">A estrutura CPropertyRestriction contém um valor de propriedade para corresponder a uma operação.</span><span class="sxs-lookup"><span data-stu-id="c3012-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="c3012-1256">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1256">0</span></span>

<span data-ttu-id="c3012-1257">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1257">1</span></span>

<span data-ttu-id="c3012-1258">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1258">2</span></span>

<span data-ttu-id="c3012-1259">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1259">3</span></span>

<span data-ttu-id="c3012-1260">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1260">4</span></span>

<span data-ttu-id="c3012-1261">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1261">5</span></span>

<span data-ttu-id="c3012-1262">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1262">6</span></span>

<span data-ttu-id="c3012-1263">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1263">7</span></span>

<span data-ttu-id="c3012-1264">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1264">8</span></span>

<span data-ttu-id="c3012-1265">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1265">9</span></span>

<span data-ttu-id="c3012-1266">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1266">1</span></span><br/> <span data-ttu-id="c3012-1267">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1267">0</span></span><br/>

<span data-ttu-id="c3012-1268">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1268">1</span></span>

<span data-ttu-id="c3012-1269">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1269">2</span></span>

<span data-ttu-id="c3012-1270">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1270">3</span></span>

<span data-ttu-id="c3012-1271">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1271">4</span></span>

<span data-ttu-id="c3012-1272">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1272">5</span></span>

<span data-ttu-id="c3012-1273">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1273">6</span></span>

<span data-ttu-id="c3012-1274">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1274">7</span></span>

<span data-ttu-id="c3012-1275">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1275">8</span></span>

<span data-ttu-id="c3012-1276">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1276">9</span></span>

<span data-ttu-id="c3012-1277">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1277">2</span></span><br/> <span data-ttu-id="c3012-1278">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1278">0</span></span><br/>

<span data-ttu-id="c3012-1279">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1279">1</span></span>

<span data-ttu-id="c3012-1280">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1280">2</span></span>

<span data-ttu-id="c3012-1281">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1281">3</span></span>

<span data-ttu-id="c3012-1282">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1282">4</span></span>

<span data-ttu-id="c3012-1283">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1283">5</span></span>

<span data-ttu-id="c3012-1284">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1284">6</span></span>

<span data-ttu-id="c3012-1285">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1285">7</span></span>

<span data-ttu-id="c3012-1286">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1286">8</span></span>

<span data-ttu-id="c3012-1287">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1287">9</span></span>

<span data-ttu-id="c3012-1288">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1288">3</span></span><br/> <span data-ttu-id="c3012-1289">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1289">0</span></span><br/>

<span data-ttu-id="c3012-1290">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1290">1</span></span>

<span data-ttu-id="c3012-1291">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="c3012-1291">\_relop</span></span>

<span data-ttu-id="c3012-1292">\_Propriedade (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1292">\_Property (variable)</span></span>

<span data-ttu-id="c3012-1293">\_prval (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="c3012-1294">**\_ RelOp**: um inteiro de 32 bits sem sinal especificando a relação a ser executada na propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="c3012-1295">DEVE ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3012-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="c3012-1296">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1296">Value</span></span>                 | <span data-ttu-id="c3012-1297">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-1298">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="c3012-1299">Uma comparação menor que.</span><span class="sxs-lookup"><span data-stu-id="c3012-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3012-1300">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="c3012-1301">Uma comparação menor que ou igual a.</span><span class="sxs-lookup"><span data-stu-id="c3012-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="c3012-1302">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="c3012-1303">Uma comparação maior que.</span><span class="sxs-lookup"><span data-stu-id="c3012-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="c3012-1304">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="c3012-1305">Uma comparação maior que ou igual a.</span><span class="sxs-lookup"><span data-stu-id="c3012-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="c3012-1306">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="c3012-1307">Uma comparação de igualdade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3012-1308">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3012-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="c3012-1309">Uma comparação diferente de.</span><span class="sxs-lookup"><span data-stu-id="c3012-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3012-1310">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="c3012-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="c3012-1311">Uma comparação de expressão regular.</span><span class="sxs-lookup"><span data-stu-id="c3012-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="c3012-1312">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3012-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="c3012-1313">Um operador e bit que retorna o operando à direita.</span><span class="sxs-lookup"><span data-stu-id="c3012-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="c3012-1314">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3012-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="c3012-1315">Um valor bit e AND que retorna um Value diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c3012-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="c3012-1316">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="c3012-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="c3012-1317">A operação deve ser executada em uma coluna de um conjunto de linhas e só será verdadeira se a operação for verdadeira para todas as linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="c3012-1318">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="c3012-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="c3012-1319">A operação deve ser executada em uma coluna de um conjunto de linhas e será true se a operação for verdadeira para qualquer linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="c3012-1320">**\_ Propriedade**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.2, indicando a propriedade na qual executar uma operação de correspondência.</span><span class="sxs-lookup"><span data-stu-id="c3012-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="c3012-1321">**\_ prval**: uma estrutura CBaseStorageVariant, conforme especificado na seção 2.2.1.1, que contém o valor a ser relacionado à propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="c3012-1322">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="c3012-1323">A estrutura CRangeRestriction contém uma restrição em um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="c3012-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="c3012-1324">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1324">0</span></span>

<span data-ttu-id="c3012-1325">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1325">1</span></span>

<span data-ttu-id="c3012-1326">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1326">2</span></span>

<span data-ttu-id="c3012-1327">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1327">3</span></span>

<span data-ttu-id="c3012-1328">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1328">4</span></span>

<span data-ttu-id="c3012-1329">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1329">5</span></span>

<span data-ttu-id="c3012-1330">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1330">6</span></span>

<span data-ttu-id="c3012-1331">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1331">7</span></span>

<span data-ttu-id="c3012-1332">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1332">8</span></span>

<span data-ttu-id="c3012-1333">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1333">9</span></span>

<span data-ttu-id="c3012-1334">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1334">1</span></span><br/> <span data-ttu-id="c3012-1335">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1335">0</span></span><br/>

<span data-ttu-id="c3012-1336">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1336">1</span></span>

<span data-ttu-id="c3012-1337">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1337">2</span></span>

<span data-ttu-id="c3012-1338">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1338">3</span></span>

<span data-ttu-id="c3012-1339">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1339">4</span></span>

<span data-ttu-id="c3012-1340">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1340">5</span></span>

<span data-ttu-id="c3012-1341">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1341">6</span></span>

<span data-ttu-id="c3012-1342">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1342">7</span></span>

<span data-ttu-id="c3012-1343">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1343">8</span></span>

<span data-ttu-id="c3012-1344">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1344">9</span></span>

<span data-ttu-id="c3012-1345">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1345">2</span></span><br/> <span data-ttu-id="c3012-1346">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1346">0</span></span><br/>

<span data-ttu-id="c3012-1347">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1347">1</span></span>

<span data-ttu-id="c3012-1348">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1348">2</span></span>

<span data-ttu-id="c3012-1349">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1349">3</span></span>

<span data-ttu-id="c3012-1350">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1350">4</span></span>

<span data-ttu-id="c3012-1351">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1351">5</span></span>

<span data-ttu-id="c3012-1352">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1352">6</span></span>

<span data-ttu-id="c3012-1353">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1353">7</span></span>

<span data-ttu-id="c3012-1354">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1354">8</span></span>

<span data-ttu-id="c3012-1355">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1355">9</span></span>

<span data-ttu-id="c3012-1356">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1356">3</span></span><br/> <span data-ttu-id="c3012-1357">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1357">0</span></span><br/>

<span data-ttu-id="c3012-1358">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1358">1</span></span>

<span data-ttu-id="c3012-1359">\_keystart (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="c3012-1360">\_keyEnd (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="c3012-1361">**\_ keystart**: uma estrutura CKey, conforme especificado na seção 2.2.1.4, que contém o início do intervalo.</span><span class="sxs-lookup"><span data-stu-id="c3012-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="c3012-1362">**\_ keyEnd**: uma estrutura CKey que contém o final do intervalo.</span><span class="sxs-lookup"><span data-stu-id="c3012-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="c3012-1363">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="c3012-1364">A estrutura CScopeRestriction contém uma restrição nos arquivos a serem pesquisados</span><span class="sxs-lookup"><span data-stu-id="c3012-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="c3012-1365">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1365">0</span></span>

<span data-ttu-id="c3012-1366">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1366">1</span></span>

<span data-ttu-id="c3012-1367">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1367">2</span></span>

<span data-ttu-id="c3012-1368">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1368">3</span></span>

<span data-ttu-id="c3012-1369">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1369">4</span></span>

<span data-ttu-id="c3012-1370">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1370">5</span></span>

<span data-ttu-id="c3012-1371">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1371">6</span></span>

<span data-ttu-id="c3012-1372">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1372">7</span></span>

<span data-ttu-id="c3012-1373">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1373">8</span></span>

<span data-ttu-id="c3012-1374">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1374">9</span></span>

<span data-ttu-id="c3012-1375">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1375">1</span></span><br/> <span data-ttu-id="c3012-1376">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1376">0</span></span><br/>

<span data-ttu-id="c3012-1377">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1377">1</span></span>

<span data-ttu-id="c3012-1378">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1378">2</span></span>

<span data-ttu-id="c3012-1379">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1379">3</span></span>

<span data-ttu-id="c3012-1380">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1380">4</span></span>

<span data-ttu-id="c3012-1381">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1381">5</span></span>

<span data-ttu-id="c3012-1382">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1382">6</span></span>

<span data-ttu-id="c3012-1383">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1383">7</span></span>

<span data-ttu-id="c3012-1384">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1384">8</span></span>

<span data-ttu-id="c3012-1385">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1385">9</span></span>

<span data-ttu-id="c3012-1386">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1386">2</span></span><br/> <span data-ttu-id="c3012-1387">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1387">0</span></span><br/>

<span data-ttu-id="c3012-1388">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1388">1</span></span>

<span data-ttu-id="c3012-1389">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1389">2</span></span>

<span data-ttu-id="c3012-1390">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1390">3</span></span>

<span data-ttu-id="c3012-1391">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1391">4</span></span>

<span data-ttu-id="c3012-1392">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1392">5</span></span>

<span data-ttu-id="c3012-1393">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1393">6</span></span>

<span data-ttu-id="c3012-1394">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1394">7</span></span>

<span data-ttu-id="c3012-1395">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1395">8</span></span>

<span data-ttu-id="c3012-1396">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1396">9</span></span>

<span data-ttu-id="c3012-1397">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1397">3</span></span><br/> <span data-ttu-id="c3012-1398">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1398">0</span></span><br/>

<span data-ttu-id="c3012-1399">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1399">1</span></span>

<span data-ttu-id="c3012-1400">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="c3012-1400">CcLowerPath</span></span>

<span data-ttu-id="c3012-1401">\_lowerPath (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="c3012-1402">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1402">...</span></span>

<span data-ttu-id="c3012-1403">\_preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1403">\_padding ( variable)</span></span>

<span data-ttu-id="c3012-1404">\_muito</span><span class="sxs-lookup"><span data-stu-id="c3012-1404">\_length</span></span>

<span data-ttu-id="c3012-1405">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="c3012-1405">\_fRecursive</span></span>

<span data-ttu-id="c3012-1406">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="c3012-1406">\_fVirtual</span></span>



 

<span data-ttu-id="c3012-1407">**CcLowerPath**: um inteiro sem sinal de 32 bits contendo o número de caracteres Unicode no \_ campo lowerPath.</span><span class="sxs-lookup"><span data-stu-id="c3012-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="c3012-1408">**\_ lowerPath**: uma cadeia de caracteres Unicode não terminada em nulo que representa o **caminho** para o qual a consulta deve ser restrita.</span><span class="sxs-lookup"><span data-stu-id="c3012-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="c3012-1409">O campo CcLowerPath contém o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c3012-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="c3012-1410">**\_ preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3012-1411">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="c3012-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3012-1412">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3012-1413">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-1414">**\_ comprimento**: um inteiro sem sinal de 32 bits contendo o comprimento de \_ LowerPath, em caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3012-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="c3012-1415">DEVE ser o mesmo valor que CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="c3012-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="c3012-1416">**\_ fRecursive**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3012-1417">DEVE ser definido como 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="c3012-1418">Se definido como 0x00000001, o servidor deve examinar recursivamente todos os subdiretórios do caminho.</span><span class="sxs-lookup"><span data-stu-id="c3012-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="c3012-1419">Se definido como 0x00000000, o servidor não examinará nenhum subdiretório.</span><span class="sxs-lookup"><span data-stu-id="c3012-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="c3012-1420">**\_ fVirtual**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3012-1421">DEVE ser definido como 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="c3012-1422">Se definido como 0x00000001, \_ lowerPath é um caminho virtual (o Uniform Resource Locator (URL) associado a um diretório físico no sistema de arquivos) para um site da Web.</span><span class="sxs-lookup"><span data-stu-id="c3012-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="c3012-1423">Se definido como 0x00000000, \_ lowerPath é um caminho do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c3012-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="c3012-1424">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="c3012-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="c3012-1425">A estrutura CSort identifica uma coluna a ser classificada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="c3012-1426">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1426">0</span></span>

<span data-ttu-id="c3012-1427">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1427">1</span></span>

<span data-ttu-id="c3012-1428">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1428">2</span></span>

<span data-ttu-id="c3012-1429">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1429">3</span></span>

<span data-ttu-id="c3012-1430">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1430">4</span></span>

<span data-ttu-id="c3012-1431">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1431">5</span></span>

<span data-ttu-id="c3012-1432">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1432">6</span></span>

<span data-ttu-id="c3012-1433">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1433">7</span></span>

<span data-ttu-id="c3012-1434">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1434">8</span></span>

<span data-ttu-id="c3012-1435">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1435">9</span></span>

<span data-ttu-id="c3012-1436">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1436">1</span></span><br/> <span data-ttu-id="c3012-1437">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1437">0</span></span><br/>

<span data-ttu-id="c3012-1438">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1438">1</span></span>

<span data-ttu-id="c3012-1439">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1439">2</span></span>

<span data-ttu-id="c3012-1440">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1440">3</span></span>

<span data-ttu-id="c3012-1441">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1441">4</span></span>

<span data-ttu-id="c3012-1442">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1442">5</span></span>

<span data-ttu-id="c3012-1443">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1443">6</span></span>

<span data-ttu-id="c3012-1444">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1444">7</span></span>

<span data-ttu-id="c3012-1445">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1445">8</span></span>

<span data-ttu-id="c3012-1446">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1446">9</span></span>

<span data-ttu-id="c3012-1447">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1447">2</span></span><br/> <span data-ttu-id="c3012-1448">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1448">0</span></span><br/>

<span data-ttu-id="c3012-1449">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1449">1</span></span>

<span data-ttu-id="c3012-1450">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1450">2</span></span>

<span data-ttu-id="c3012-1451">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1451">3</span></span>

<span data-ttu-id="c3012-1452">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1452">4</span></span>

<span data-ttu-id="c3012-1453">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1453">5</span></span>

<span data-ttu-id="c3012-1454">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1454">6</span></span>

<span data-ttu-id="c3012-1455">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1455">7</span></span>

<span data-ttu-id="c3012-1456">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1456">8</span></span>

<span data-ttu-id="c3012-1457">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1457">9</span></span>

<span data-ttu-id="c3012-1458">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1458">3</span></span><br/> <span data-ttu-id="c3012-1459">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1459">0</span></span><br/>

<span data-ttu-id="c3012-1460">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1460">1</span></span>

<span data-ttu-id="c3012-1461">pidColumn</span><span class="sxs-lookup"><span data-stu-id="c3012-1461">pidColumn</span></span>

<span data-ttu-id="c3012-1462">dwOrd</span><span class="sxs-lookup"><span data-stu-id="c3012-1462">dwOrder</span></span>

<span data-ttu-id="c3012-1463">locale</span><span class="sxs-lookup"><span data-stu-id="c3012-1463">locale</span></span>



 

<span data-ttu-id="c3012-1464">**pidColumn**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3012-1465">O número da coluna pela qual classificar.</span><span class="sxs-lookup"><span data-stu-id="c3012-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="c3012-1466">**dwOrder**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3012-1467">DEVE ser um dos valores a seguir, especificando como classificar com base na coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="c3012-1468">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1468">Value</span></span>                        | <span data-ttu-id="c3012-1469">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-1470">CONSULTAR \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="c3012-1471">As linhas devem ser classificadas em ordem crescente com base nos valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="c3012-1472">CONSULTA \_ descendente 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="c3012-1473">As linhas devem ser classificadas em ordem decrescente com base nos valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="c3012-1474">**localidade**: um inteiro de 32 bits sem sinal indicando a localidade, conforme especificado no \[ Apêndice a do MS-GPSI \] , da coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="c3012-1475">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="c3012-1476">A estrutura CSynRestriction contém uma palavra ou seus sinônimos para uma frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="c3012-1477">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1477">0</span></span>

<span data-ttu-id="c3012-1478">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1478">1</span></span>

<span data-ttu-id="c3012-1479">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1479">2</span></span>

<span data-ttu-id="c3012-1480">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1480">3</span></span>

<span data-ttu-id="c3012-1481">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1481">4</span></span>

<span data-ttu-id="c3012-1482">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1482">5</span></span>

<span data-ttu-id="c3012-1483">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1483">6</span></span>

<span data-ttu-id="c3012-1484">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1484">7</span></span>

<span data-ttu-id="c3012-1485">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1485">8</span></span>

<span data-ttu-id="c3012-1486">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1486">9</span></span>

<span data-ttu-id="c3012-1487">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1487">1</span></span><br/> <span data-ttu-id="c3012-1488">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1488">0</span></span><br/>

<span data-ttu-id="c3012-1489">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1489">1</span></span>

<span data-ttu-id="c3012-1490">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1490">2</span></span>

<span data-ttu-id="c3012-1491">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1491">3</span></span>

<span data-ttu-id="c3012-1492">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1492">4</span></span>

<span data-ttu-id="c3012-1493">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1493">5</span></span>

<span data-ttu-id="c3012-1494">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1494">6</span></span>

<span data-ttu-id="c3012-1495">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1495">7</span></span>

<span data-ttu-id="c3012-1496">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1496">8</span></span>

<span data-ttu-id="c3012-1497">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1497">9</span></span>

<span data-ttu-id="c3012-1498">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1498">2</span></span><br/> <span data-ttu-id="c3012-1499">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1499">0</span></span><br/>

<span data-ttu-id="c3012-1500">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1500">1</span></span>

<span data-ttu-id="c3012-1501">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1501">2</span></span>

<span data-ttu-id="c3012-1502">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1502">3</span></span>

<span data-ttu-id="c3012-1503">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1503">4</span></span>

<span data-ttu-id="c3012-1504">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1504">5</span></span>

<span data-ttu-id="c3012-1505">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1505">6</span></span>

<span data-ttu-id="c3012-1506">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1506">7</span></span>

<span data-ttu-id="c3012-1507">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1507">8</span></span>

<span data-ttu-id="c3012-1508">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1508">9</span></span>

<span data-ttu-id="c3012-1509">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1509">3</span></span><br/> <span data-ttu-id="c3012-1510">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1510">0</span></span><br/>

<span data-ttu-id="c3012-1511">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1511">1</span></span>

<span data-ttu-id="c3012-1512">Restrição</span><span class="sxs-lookup"><span data-stu-id="c3012-1512">Restriction</span></span>

<span data-ttu-id="c3012-1513">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1513">...</span></span>

<span data-ttu-id="c3012-1514">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1514">...</span></span>

<span data-ttu-id="c3012-1515">cKey</span><span class="sxs-lookup"><span data-stu-id="c3012-1515">cKey</span></span>

<span data-ttu-id="c3012-1516">\_keyarray (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="c3012-1517">\_ISRANGE</span><span class="sxs-lookup"><span data-stu-id="c3012-1517">\_isRange</span></span>



 

<span data-ttu-id="c3012-1518">**Restrição**: uma estrutura COccRestriction que especifica o local da palavra.</span><span class="sxs-lookup"><span data-stu-id="c3012-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="c3012-1519">**cKey**: um inteiro sem sinal de 32 bits especificando o número de elementos na \_ matriz keyarray.</span><span class="sxs-lookup"><span data-stu-id="c3012-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="c3012-1520">**\_ keyarray**: uma matriz de estruturas CKey que especificam uma palavra e seus sinônimos.</span><span class="sxs-lookup"><span data-stu-id="c3012-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="c3012-1521">**\_ ISRANGE**: se definido como 0x01, as chaves são prefixos para correspondência.</span><span class="sxs-lookup"><span data-stu-id="c3012-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="c3012-1522">Se definido como 0x00, as chaves são valores exatos para corresponder.</span><span class="sxs-lookup"><span data-stu-id="c3012-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="c3012-1523">\_ISRANGE não deve ser definido para nenhum outro valor.</span><span class="sxs-lookup"><span data-stu-id="c3012-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="c3012-1524">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="c3012-1525">A estrutura CVectorRestriction contém uma operação ponderada ou em um nó de árvore de comandos.</span><span class="sxs-lookup"><span data-stu-id="c3012-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="c3012-1526">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1526">0</span></span>

<span data-ttu-id="c3012-1527">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1527">1</span></span>

<span data-ttu-id="c3012-1528">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1528">2</span></span>

<span data-ttu-id="c3012-1529">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1529">3</span></span>

<span data-ttu-id="c3012-1530">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1530">4</span></span>

<span data-ttu-id="c3012-1531">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1531">5</span></span>

<span data-ttu-id="c3012-1532">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1532">6</span></span>

<span data-ttu-id="c3012-1533">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1533">7</span></span>

<span data-ttu-id="c3012-1534">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1534">8</span></span>

<span data-ttu-id="c3012-1535">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1535">9</span></span>

<span data-ttu-id="c3012-1536">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1536">1</span></span><br/> <span data-ttu-id="c3012-1537">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1537">0</span></span><br/>

<span data-ttu-id="c3012-1538">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1538">1</span></span>

<span data-ttu-id="c3012-1539">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1539">2</span></span>

<span data-ttu-id="c3012-1540">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1540">3</span></span>

<span data-ttu-id="c3012-1541">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1541">4</span></span>

<span data-ttu-id="c3012-1542">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1542">5</span></span>

<span data-ttu-id="c3012-1543">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1543">6</span></span>

<span data-ttu-id="c3012-1544">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1544">7</span></span>

<span data-ttu-id="c3012-1545">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1545">8</span></span>

<span data-ttu-id="c3012-1546">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1546">9</span></span>

<span data-ttu-id="c3012-1547">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1547">2</span></span><br/> <span data-ttu-id="c3012-1548">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1548">0</span></span><br/>

<span data-ttu-id="c3012-1549">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1549">1</span></span>

<span data-ttu-id="c3012-1550">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1550">2</span></span>

<span data-ttu-id="c3012-1551">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1551">3</span></span>

<span data-ttu-id="c3012-1552">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1552">4</span></span>

<span data-ttu-id="c3012-1553">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1553">5</span></span>

<span data-ttu-id="c3012-1554">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1554">6</span></span>

<span data-ttu-id="c3012-1555">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1555">7</span></span>

<span data-ttu-id="c3012-1556">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1556">8</span></span>

<span data-ttu-id="c3012-1557">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1557">9</span></span>

<span data-ttu-id="c3012-1558">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1558">3</span></span><br/> <span data-ttu-id="c3012-1559">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1559">0</span></span><br/>

<span data-ttu-id="c3012-1560">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1560">1</span></span>

<span data-ttu-id="c3012-1561">\_Pres (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1561">\_pres (variable)</span></span>

<span data-ttu-id="c3012-1562">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1562">...</span></span>

<span data-ttu-id="c3012-1563">\_preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1563">\_padding (variable)</span></span>

<span data-ttu-id="c3012-1564">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="c3012-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="c3012-1565">**\_ Pres**: uma árvore de comandos CNodeRestriction na qual uma classificação ou operação deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="c3012-1566">**\_ preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3012-1567">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="c3012-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3012-1568">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3012-1569">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-1570">**\_ ulRankMethod**: um inteiro sem sinal de 32 bits especificando um algoritmo de classificação.</span><span class="sxs-lookup"><span data-stu-id="c3012-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="c3012-1571">DEVE ser definido como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3012-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="c3012-1572">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1572">Value</span></span>                            | <span data-ttu-id="c3012-1573">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="c3012-1574">Classificação de vetor \_ \_ mín. 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="c3012-1575">Usar Salt de algoritmo mínimo \[ \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="c3012-1576">Classificação de vetor \_ \_ máx. 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="c3012-1577">Use o Salt máximo do algoritmo \[ \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="c3012-1578">\_0x00000002 interno de classificação de vetor \_</span><span class="sxs-lookup"><span data-stu-id="c3012-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="c3012-1579">Usar a saltização do algoritmo de produto interno \[ \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="c3012-1580">\_0x00000003 de classificação de vetor \_</span><span class="sxs-lookup"><span data-stu-id="c3012-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="c3012-1581">Use a saltização do algoritmo de coeficiente de um \[ \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="c3012-1582">Classificação de vetor \_ \_ Jaccard 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="c3012-1583">Use a saltização do algoritmo de coeficiente Jaccard \[ \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="c3012-1584">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="c3012-1585">A estrutura CWordRestriction contém uma palavra para uma frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="c3012-1586">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1586">0</span></span>

<span data-ttu-id="c3012-1587">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1587">1</span></span>

<span data-ttu-id="c3012-1588">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1588">2</span></span>

<span data-ttu-id="c3012-1589">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1589">3</span></span>

<span data-ttu-id="c3012-1590">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1590">4</span></span>

<span data-ttu-id="c3012-1591">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1591">5</span></span>

<span data-ttu-id="c3012-1592">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1592">6</span></span>

<span data-ttu-id="c3012-1593">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1593">7</span></span>

<span data-ttu-id="c3012-1594">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1594">8</span></span>

<span data-ttu-id="c3012-1595">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1595">9</span></span>

<span data-ttu-id="c3012-1596">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1596">1</span></span><br/> <span data-ttu-id="c3012-1597">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1597">0</span></span><br/>

<span data-ttu-id="c3012-1598">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1598">1</span></span>

<span data-ttu-id="c3012-1599">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1599">2</span></span>

<span data-ttu-id="c3012-1600">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1600">3</span></span>

<span data-ttu-id="c3012-1601">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1601">4</span></span>

<span data-ttu-id="c3012-1602">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1602">5</span></span>

<span data-ttu-id="c3012-1603">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1603">6</span></span>

<span data-ttu-id="c3012-1604">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1604">7</span></span>

<span data-ttu-id="c3012-1605">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1605">8</span></span>

<span data-ttu-id="c3012-1606">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1606">9</span></span>

<span data-ttu-id="c3012-1607">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1607">2</span></span><br/> <span data-ttu-id="c3012-1608">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1608">0</span></span><br/>

<span data-ttu-id="c3012-1609">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1609">1</span></span>

<span data-ttu-id="c3012-1610">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1610">2</span></span>

<span data-ttu-id="c3012-1611">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1611">3</span></span>

<span data-ttu-id="c3012-1612">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1612">4</span></span>

<span data-ttu-id="c3012-1613">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1613">5</span></span>

<span data-ttu-id="c3012-1614">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1614">6</span></span>

<span data-ttu-id="c3012-1615">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1615">7</span></span>

<span data-ttu-id="c3012-1616">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1616">8</span></span>

<span data-ttu-id="c3012-1617">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1617">9</span></span>

<span data-ttu-id="c3012-1618">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1618">3</span></span><br/> <span data-ttu-id="c3012-1619">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1619">0</span></span><br/>

<span data-ttu-id="c3012-1620">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1620">1</span></span>

<span data-ttu-id="c3012-1621">restriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1621">restriction</span></span>

<span data-ttu-id="c3012-1622">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1622">...</span></span>

<span data-ttu-id="c3012-1623">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1623">...</span></span>

<span data-ttu-id="c3012-1624">\_chave (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1624">\_key (variable)</span></span>

<span data-ttu-id="c3012-1625">\_ISRANGE</span><span class="sxs-lookup"><span data-stu-id="c3012-1625">\_isRange</span></span>



 

<span data-ttu-id="c3012-1626">**restrição**: uma estrutura COccRestriction que especifica o local da palavra.</span><span class="sxs-lookup"><span data-stu-id="c3012-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="c3012-1627">**\_ chave**: uma estrutura CKey que especifica uma palavra.</span><span class="sxs-lookup"><span data-stu-id="c3012-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="c3012-1628">**\_ ISRANGE**: se definido como 0x01, a chave é um prefixo a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="c3012-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="c3012-1629">Se definido como 0x00, a chave é um valor exato a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="c3012-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="c3012-1630">\_ISRANGE não deve ser definido como qualquer outro valor.</span><span class="sxs-lookup"><span data-stu-id="c3012-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="c3012-1631">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="c3012-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="c3012-1632">A estrutura CRestriction contém um nó de uma árvore de comando de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="c3012-1633">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1633">0</span></span>

<span data-ttu-id="c3012-1634">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1634">1</span></span>

<span data-ttu-id="c3012-1635">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1635">2</span></span>

<span data-ttu-id="c3012-1636">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1636">3</span></span>

<span data-ttu-id="c3012-1637">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1637">4</span></span>

<span data-ttu-id="c3012-1638">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1638">5</span></span>

<span data-ttu-id="c3012-1639">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1639">6</span></span>

<span data-ttu-id="c3012-1640">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1640">7</span></span>

<span data-ttu-id="c3012-1641">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1641">8</span></span>

<span data-ttu-id="c3012-1642">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1642">9</span></span>

<span data-ttu-id="c3012-1643">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1643">1</span></span><br/> <span data-ttu-id="c3012-1644">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1644">0</span></span><br/>

<span data-ttu-id="c3012-1645">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1645">1</span></span>

<span data-ttu-id="c3012-1646">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1646">2</span></span>

<span data-ttu-id="c3012-1647">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1647">3</span></span>

<span data-ttu-id="c3012-1648">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1648">4</span></span>

<span data-ttu-id="c3012-1649">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1649">5</span></span>

<span data-ttu-id="c3012-1650">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1650">6</span></span>

<span data-ttu-id="c3012-1651">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1651">7</span></span>

<span data-ttu-id="c3012-1652">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1652">8</span></span>

<span data-ttu-id="c3012-1653">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1653">9</span></span>

<span data-ttu-id="c3012-1654">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1654">2</span></span><br/> <span data-ttu-id="c3012-1655">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1655">0</span></span><br/>

<span data-ttu-id="c3012-1656">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1656">1</span></span>

<span data-ttu-id="c3012-1657">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1657">2</span></span>

<span data-ttu-id="c3012-1658">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1658">3</span></span>

<span data-ttu-id="c3012-1659">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1659">4</span></span>

<span data-ttu-id="c3012-1660">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1660">5</span></span>

<span data-ttu-id="c3012-1661">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1661">6</span></span>

<span data-ttu-id="c3012-1662">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1662">7</span></span>

<span data-ttu-id="c3012-1663">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1663">8</span></span>

<span data-ttu-id="c3012-1664">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1664">9</span></span>

<span data-ttu-id="c3012-1665">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1665">3</span></span><br/> <span data-ttu-id="c3012-1666">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1666">0</span></span><br/>

<span data-ttu-id="c3012-1667">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1667">1</span></span>

<span data-ttu-id="c3012-1668">\_ulType</span><span class="sxs-lookup"><span data-stu-id="c3012-1668">\_ulType</span></span>

<span data-ttu-id="c3012-1669">Peso</span><span class="sxs-lookup"><span data-stu-id="c3012-1669">Weight</span></span>

<span data-ttu-id="c3012-1670">Restrição</span><span class="sxs-lookup"><span data-stu-id="c3012-1670">Restriction</span></span>



 

<span data-ttu-id="c3012-1671">**\_ ulType**: um inteiro de 32 bits sem sinal indicando o tipo de restrição usado para o nó da árvore de comandos.</span><span class="sxs-lookup"><span data-stu-id="c3012-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="c3012-1672">DEVE ser definido como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3012-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="c3012-1673">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1673">Value</span></span>                    | <span data-ttu-id="c3012-1674">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-1675">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="c3012-1676">O nó representa uma palavra de ruído em uma consulta de vetor.</span><span class="sxs-lookup"><span data-stu-id="c3012-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="c3012-1677">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="c3012-1678">O nó contém um CNodeRestriction no qual uma operação AND lógica deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="c3012-1679">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="c3012-1680">O nó contém um CNodeRestriction no qual uma operação OR lógica deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="c3012-1681">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="c3012-1682">O nó contém um CRestriction no qual uma operação NOT deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="c3012-1683">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="c3012-1684">O nó contém um CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="c3012-1685">RTProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3012-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="c3012-1686">O nó contém um CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="c3012-1687">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="c3012-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="c3012-1688">O nó contém um CNodeRestriction no qual uma classificação de proximidade deve ser executada,</span><span class="sxs-lookup"><span data-stu-id="c3012-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="c3012-1689">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3012-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="c3012-1690">O nó contém um CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="c3012-1691">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3012-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="c3012-1692">O nó contém um CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="c3012-1693">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="c3012-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="c3012-1694">O nó contém um CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="c3012-1695">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="c3012-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="c3012-1696">O nó contém um CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="c3012-1697">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="c3012-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="c3012-1698">O nó contém um CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="c3012-1699">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="c3012-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="c3012-1700">O nó contém um CNodeRestriction no qual uma correspondência de frase deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="c3012-1701">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="c3012-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="c3012-1702">O nó contém um CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="c3012-1703">RTWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c3012-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="c3012-1704">O nó contém um CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="c3012-1705">**Peso**: um inteiro sem sinal de 32 bits que representa o peso do nó.</span><span class="sxs-lookup"><span data-stu-id="c3012-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="c3012-1706">Weight indica a importância do nó em relação a outros nós na árvore de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="c3012-1707">Valores de peso mais alto são mais importantes.</span><span class="sxs-lookup"><span data-stu-id="c3012-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="c3012-1708">**Restrição**: o tipo de restrição para o nó da árvore de comandos.</span><span class="sxs-lookup"><span data-stu-id="c3012-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="c3012-1709">A sintaxe deve ser conforme indicado pelo \_ campo ulType.</span><span class="sxs-lookup"><span data-stu-id="c3012-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="c3012-1710">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="c3012-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="c3012-1711">A estrutura CColumnSet especifica os números de coluna a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="c3012-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="c3012-1712">Essa estrutura é sempre usada em referência a uma estrutura CPidMapper específica (seção 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="c3012-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="c3012-1713">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1713">0</span></span>

<span data-ttu-id="c3012-1714">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1714">1</span></span>

<span data-ttu-id="c3012-1715">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1715">2</span></span>

<span data-ttu-id="c3012-1716">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1716">3</span></span>

<span data-ttu-id="c3012-1717">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1717">4</span></span>

<span data-ttu-id="c3012-1718">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1718">5</span></span>

<span data-ttu-id="c3012-1719">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1719">6</span></span>

<span data-ttu-id="c3012-1720">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1720">7</span></span>

<span data-ttu-id="c3012-1721">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1721">8</span></span>

<span data-ttu-id="c3012-1722">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1722">9</span></span>

<span data-ttu-id="c3012-1723">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1723">1</span></span><br/> <span data-ttu-id="c3012-1724">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1724">0</span></span><br/>

<span data-ttu-id="c3012-1725">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1725">1</span></span>

<span data-ttu-id="c3012-1726">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1726">2</span></span>

<span data-ttu-id="c3012-1727">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1727">3</span></span>

<span data-ttu-id="c3012-1728">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1728">4</span></span>

<span data-ttu-id="c3012-1729">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1729">5</span></span>

<span data-ttu-id="c3012-1730">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1730">6</span></span>

<span data-ttu-id="c3012-1731">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1731">7</span></span>

<span data-ttu-id="c3012-1732">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1732">8</span></span>

<span data-ttu-id="c3012-1733">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1733">9</span></span>

<span data-ttu-id="c3012-1734">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1734">2</span></span><br/> <span data-ttu-id="c3012-1735">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1735">0</span></span><br/>

<span data-ttu-id="c3012-1736">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1736">1</span></span>

<span data-ttu-id="c3012-1737">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1737">2</span></span>

<span data-ttu-id="c3012-1738">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1738">3</span></span>

<span data-ttu-id="c3012-1739">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1739">4</span></span>

<span data-ttu-id="c3012-1740">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1740">5</span></span>

<span data-ttu-id="c3012-1741">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1741">6</span></span>

<span data-ttu-id="c3012-1742">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1742">7</span></span>

<span data-ttu-id="c3012-1743">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1743">8</span></span>

<span data-ttu-id="c3012-1744">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1744">9</span></span>

<span data-ttu-id="c3012-1745">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1745">3</span></span><br/> <span data-ttu-id="c3012-1746">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1746">0</span></span><br/>

<span data-ttu-id="c3012-1747">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1747">1</span></span>

<span data-ttu-id="c3012-1748">count</span><span class="sxs-lookup"><span data-stu-id="c3012-1748">count</span></span>

<span data-ttu-id="c3012-1749">índices (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1749">indexes (variable)</span></span>



 

<span data-ttu-id="c3012-1750">**Count**: um inteiro de 32 bits sem sinal especificando o número de elementos na matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="c3012-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="c3012-1751">**índices**: matriz de inteiros sem sinal de 4 bytes que representam índices baseados em zero na matriz aPropSpec na estrutura CPidMapper correspondente.</span><span class="sxs-lookup"><span data-stu-id="c3012-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="c3012-1752">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="c3012-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="c3012-1753">A estrutura CCategorizationSet contém informações sobre o agrupamento de um conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="c3012-1754">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1754">0</span></span>

<span data-ttu-id="c3012-1755">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1755">1</span></span>

<span data-ttu-id="c3012-1756">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1756">2</span></span>

<span data-ttu-id="c3012-1757">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1757">3</span></span>

<span data-ttu-id="c3012-1758">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1758">4</span></span>

<span data-ttu-id="c3012-1759">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1759">5</span></span>

<span data-ttu-id="c3012-1760">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1760">6</span></span>

<span data-ttu-id="c3012-1761">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1761">7</span></span>

<span data-ttu-id="c3012-1762">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1762">8</span></span>

<span data-ttu-id="c3012-1763">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1763">9</span></span>

<span data-ttu-id="c3012-1764">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1764">1</span></span><br/> <span data-ttu-id="c3012-1765">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1765">0</span></span><br/>

<span data-ttu-id="c3012-1766">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1766">1</span></span>

<span data-ttu-id="c3012-1767">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1767">2</span></span>

<span data-ttu-id="c3012-1768">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1768">3</span></span>

<span data-ttu-id="c3012-1769">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1769">4</span></span>

<span data-ttu-id="c3012-1770">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1770">5</span></span>

<span data-ttu-id="c3012-1771">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1771">6</span></span>

<span data-ttu-id="c3012-1772">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1772">7</span></span>

<span data-ttu-id="c3012-1773">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1773">8</span></span>

<span data-ttu-id="c3012-1774">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1774">9</span></span>

<span data-ttu-id="c3012-1775">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1775">2</span></span><br/> <span data-ttu-id="c3012-1776">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1776">0</span></span><br/>

<span data-ttu-id="c3012-1777">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1777">1</span></span>

<span data-ttu-id="c3012-1778">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1778">2</span></span>

<span data-ttu-id="c3012-1779">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1779">3</span></span>

<span data-ttu-id="c3012-1780">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1780">4</span></span>

<span data-ttu-id="c3012-1781">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1781">5</span></span>

<span data-ttu-id="c3012-1782">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1782">6</span></span>

<span data-ttu-id="c3012-1783">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1783">7</span></span>

<span data-ttu-id="c3012-1784">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1784">8</span></span>

<span data-ttu-id="c3012-1785">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1785">9</span></span>

<span data-ttu-id="c3012-1786">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1786">3</span></span><br/> <span data-ttu-id="c3012-1787">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1787">0</span></span><br/>

<span data-ttu-id="c3012-1788">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1788">1</span></span>

<span data-ttu-id="c3012-1789">count</span><span class="sxs-lookup"><span data-stu-id="c3012-1789">count</span></span>

<span data-ttu-id="c3012-1790">Categorias (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1790">categories (variable)</span></span>



 

<span data-ttu-id="c3012-1791">**Count**: um inteiro sem sinal de 32 bits contendo o número de elementos na matriz Categories.</span><span class="sxs-lookup"><span data-stu-id="c3012-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="c3012-1792">**categorias**: matriz de estruturas CCategorizationSpec especificando o agrupamento da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="c3012-1793">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="c3012-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="c3012-1794">A estrutura CCategorizationSpec contém um agrupamento para um conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="c3012-1795">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1795">0</span></span>

<span data-ttu-id="c3012-1796">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1796">1</span></span>

<span data-ttu-id="c3012-1797">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1797">2</span></span>

<span data-ttu-id="c3012-1798">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1798">3</span></span>

<span data-ttu-id="c3012-1799">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1799">4</span></span>

<span data-ttu-id="c3012-1800">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1800">5</span></span>

<span data-ttu-id="c3012-1801">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1801">6</span></span>

<span data-ttu-id="c3012-1802">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1802">7</span></span>

<span data-ttu-id="c3012-1803">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1803">8</span></span>

<span data-ttu-id="c3012-1804">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1804">9</span></span>

<span data-ttu-id="c3012-1805">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1805">1</span></span><br/> <span data-ttu-id="c3012-1806">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1806">0</span></span><br/>

<span data-ttu-id="c3012-1807">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1807">1</span></span>

<span data-ttu-id="c3012-1808">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1808">2</span></span>

<span data-ttu-id="c3012-1809">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1809">3</span></span>

<span data-ttu-id="c3012-1810">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1810">4</span></span>

<span data-ttu-id="c3012-1811">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1811">5</span></span>

<span data-ttu-id="c3012-1812">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1812">6</span></span>

<span data-ttu-id="c3012-1813">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1813">7</span></span>

<span data-ttu-id="c3012-1814">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1814">8</span></span>

<span data-ttu-id="c3012-1815">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1815">9</span></span>

<span data-ttu-id="c3012-1816">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1816">2</span></span><br/> <span data-ttu-id="c3012-1817">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1817">0</span></span><br/>

<span data-ttu-id="c3012-1818">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1818">1</span></span>

<span data-ttu-id="c3012-1819">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1819">2</span></span>

<span data-ttu-id="c3012-1820">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1820">3</span></span>

<span data-ttu-id="c3012-1821">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1821">4</span></span>

<span data-ttu-id="c3012-1822">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1822">5</span></span>

<span data-ttu-id="c3012-1823">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1823">6</span></span>

<span data-ttu-id="c3012-1824">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1824">7</span></span>

<span data-ttu-id="c3012-1825">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1825">8</span></span>

<span data-ttu-id="c3012-1826">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1826">9</span></span>

<span data-ttu-id="c3012-1827">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1827">3</span></span><br/> <span data-ttu-id="c3012-1828">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1828">0</span></span><br/>

<span data-ttu-id="c3012-1829">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1829">1</span></span>

<span data-ttu-id="c3012-1830">\_csColumns (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="c3012-1831">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="c3012-1831">\_ulCategType</span></span>



 

<span data-ttu-id="c3012-1832">**\_ csColumns**: uma estrutura CColumnSet que indica as colunas pelas quais agrupar a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="c3012-1833">**\_ ulCategType**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3012-1834">DEVE ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="c3012-1835">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="c3012-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="c3012-1836">A estrutura CDbColId contém uma coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="c3012-1837">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1837">0</span></span>

<span data-ttu-id="c3012-1838">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1838">1</span></span>

<span data-ttu-id="c3012-1839">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1839">2</span></span>

<span data-ttu-id="c3012-1840">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1840">3</span></span>

<span data-ttu-id="c3012-1841">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1841">4</span></span>

<span data-ttu-id="c3012-1842">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1842">5</span></span>

<span data-ttu-id="c3012-1843">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1843">6</span></span>

<span data-ttu-id="c3012-1844">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1844">7</span></span>

<span data-ttu-id="c3012-1845">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1845">8</span></span>

<span data-ttu-id="c3012-1846">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1846">9</span></span>

<span data-ttu-id="c3012-1847">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1847">1</span></span><br/> <span data-ttu-id="c3012-1848">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1848">0</span></span><br/>

<span data-ttu-id="c3012-1849">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1849">1</span></span>

<span data-ttu-id="c3012-1850">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1850">2</span></span>

<span data-ttu-id="c3012-1851">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1851">3</span></span>

<span data-ttu-id="c3012-1852">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1852">4</span></span>

<span data-ttu-id="c3012-1853">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1853">5</span></span>

<span data-ttu-id="c3012-1854">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1854">6</span></span>

<span data-ttu-id="c3012-1855">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1855">7</span></span>

<span data-ttu-id="c3012-1856">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1856">8</span></span>

<span data-ttu-id="c3012-1857">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1857">9</span></span>

<span data-ttu-id="c3012-1858">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1858">2</span></span><br/> <span data-ttu-id="c3012-1859">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1859">0</span></span><br/>

<span data-ttu-id="c3012-1860">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1860">1</span></span>

<span data-ttu-id="c3012-1861">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1861">2</span></span>

<span data-ttu-id="c3012-1862">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1862">3</span></span>

<span data-ttu-id="c3012-1863">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1863">4</span></span>

<span data-ttu-id="c3012-1864">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1864">5</span></span>

<span data-ttu-id="c3012-1865">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1865">6</span></span>

<span data-ttu-id="c3012-1866">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1866">7</span></span>

<span data-ttu-id="c3012-1867">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1867">8</span></span>

<span data-ttu-id="c3012-1868">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1868">9</span></span>

<span data-ttu-id="c3012-1869">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1869">3</span></span><br/> <span data-ttu-id="c3012-1870">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1870">0</span></span><br/>

<span data-ttu-id="c3012-1871">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1871">1</span></span>

<span data-ttu-id="c3012-1872">eKind</span><span class="sxs-lookup"><span data-stu-id="c3012-1872">eKind</span></span>

<span data-ttu-id="c3012-1873">GUID</span><span class="sxs-lookup"><span data-stu-id="c3012-1873">GUID</span></span>

<span data-ttu-id="c3012-1874">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1874">...</span></span>

<span data-ttu-id="c3012-1875">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1875">...</span></span>

<span data-ttu-id="c3012-1876">...</span><span class="sxs-lookup"><span data-stu-id="c3012-1876">...</span></span>

<span data-ttu-id="c3012-1877">ulId</span><span class="sxs-lookup"><span data-stu-id="c3012-1877">ulId</span></span>

<span data-ttu-id="c3012-1878">vString (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1878">vString (variable)</span></span>



 

<span data-ttu-id="c3012-1879">**eKind**: deve ser definido como um dos valores abaixo que indica o conteúdo de GUID e vValue.</span><span class="sxs-lookup"><span data-stu-id="c3012-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="c3012-1880">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1880">Value</span></span>                            | <span data-ttu-id="c3012-1881">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-1882">Nome do GUID do DBKIND \_ \_ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="c3012-1883">vString contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="c3012-1884">\_GUID DBKIND \_ Propid 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="c3012-1885">ulId contém um inteiro de 4 bytes que indica a ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="c3012-1886">Nome do DBKIND \_ PGUID \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="c3012-1887">vString contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1887">vString contains a property name.</span></span> <span data-ttu-id="c3012-1888">Esse valor deve ser tratado da mesma forma que o \_ nome do GUID DBKIND \_ .</span><span class="sxs-lookup"><span data-stu-id="c3012-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="c3012-1889">DBKIND \_ PGUID \_ Propid 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="c3012-1890">ulId contém um inteiro de 4 bytes que indica a ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="c3012-1891">Esse valor deve ser o mesmo que o DBKIND \_ GUID \_ Propid.</span><span class="sxs-lookup"><span data-stu-id="c3012-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="c3012-1892">**GUID**: o GUID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="c3012-1893">**ulId**: se EKIND for DBKIND \_ GUID \_ Propid ou DBKIND \_ PGUID \_ Propid, esse campo conterá um inteiro não assinado, especificando a ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="c3012-1894">Se eKind for DBKIND \_ \_ nome do GUID ou DBKIND \_ PGUID \_ nome, esse campo conterá um inteiro sem sinal especificando o número de caracteres Unicode contidos no campo vString.</span><span class="sxs-lookup"><span data-stu-id="c3012-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="c3012-1895">**vString**: uma cadeia de caracteres Unicode não terminada em nulo que representa o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="c3012-1896">Ele deve ser omitido a menos que o campo eKind seja definido como DBKIND \_ nome do GUID \_ ou DBKIND \_ PGUID \_ .</span><span class="sxs-lookup"><span data-stu-id="c3012-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="c3012-1897">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="c3012-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="c3012-1898">A estrutura CDbProp contém uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="c3012-1899">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1899">0</span></span>

<span data-ttu-id="c3012-1900">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1900">1</span></span>

<span data-ttu-id="c3012-1901">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1901">2</span></span>

<span data-ttu-id="c3012-1902">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1902">3</span></span>

<span data-ttu-id="c3012-1903">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1903">4</span></span>

<span data-ttu-id="c3012-1904">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1904">5</span></span>

<span data-ttu-id="c3012-1905">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1905">6</span></span>

<span data-ttu-id="c3012-1906">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1906">7</span></span>

<span data-ttu-id="c3012-1907">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1907">8</span></span>

<span data-ttu-id="c3012-1908">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1908">9</span></span>

<span data-ttu-id="c3012-1909">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1909">1</span></span><br/> <span data-ttu-id="c3012-1910">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1910">0</span></span><br/>

<span data-ttu-id="c3012-1911">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1911">1</span></span>

<span data-ttu-id="c3012-1912">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1912">2</span></span>

<span data-ttu-id="c3012-1913">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1913">3</span></span>

<span data-ttu-id="c3012-1914">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1914">4</span></span>

<span data-ttu-id="c3012-1915">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1915">5</span></span>

<span data-ttu-id="c3012-1916">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1916">6</span></span>

<span data-ttu-id="c3012-1917">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1917">7</span></span>

<span data-ttu-id="c3012-1918">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1918">8</span></span>

<span data-ttu-id="c3012-1919">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1919">9</span></span>

<span data-ttu-id="c3012-1920">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1920">2</span></span><br/> <span data-ttu-id="c3012-1921">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1921">0</span></span><br/>

<span data-ttu-id="c3012-1922">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1922">1</span></span>

<span data-ttu-id="c3012-1923">2</span><span class="sxs-lookup"><span data-stu-id="c3012-1923">2</span></span>

<span data-ttu-id="c3012-1924">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1924">3</span></span>

<span data-ttu-id="c3012-1925">4</span><span class="sxs-lookup"><span data-stu-id="c3012-1925">4</span></span>

<span data-ttu-id="c3012-1926">5</span><span class="sxs-lookup"><span data-stu-id="c3012-1926">5</span></span>

<span data-ttu-id="c3012-1927">6</span><span class="sxs-lookup"><span data-stu-id="c3012-1927">6</span></span>

<span data-ttu-id="c3012-1928">7</span><span class="sxs-lookup"><span data-stu-id="c3012-1928">7</span></span>

<span data-ttu-id="c3012-1929">8</span><span class="sxs-lookup"><span data-stu-id="c3012-1929">8</span></span>

<span data-ttu-id="c3012-1930">9</span><span class="sxs-lookup"><span data-stu-id="c3012-1930">9</span></span>

<span data-ttu-id="c3012-1931">3</span><span class="sxs-lookup"><span data-stu-id="c3012-1931">3</span></span><br/> <span data-ttu-id="c3012-1932">0</span><span class="sxs-lookup"><span data-stu-id="c3012-1932">0</span></span><br/>

<span data-ttu-id="c3012-1933">1</span><span class="sxs-lookup"><span data-stu-id="c3012-1933">1</span></span>

<span data-ttu-id="c3012-1934">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="c3012-1934">DBPROPID</span></span>

<span data-ttu-id="c3012-1935">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="c3012-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="c3012-1936">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="c3012-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="c3012-1937">colid (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1937">colid (variable)</span></span>

<span data-ttu-id="c3012-1938">vValue (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-1938">vValue (variable)</span></span>



 

<span data-ttu-id="c3012-1939">**DBPROPID**: um inteiro sem sinal de 32 bits, indicando a ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="c3012-1940">**DBPROPOPTIONS** : deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="c3012-1941">**DBPROPSTATUS**: deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="c3012-1942">**colid**: uma estrutura CDbColId, conforme especificado na seção 2.2.1.20, indicando a coluna à qual a propriedade se aplica.</span><span class="sxs-lookup"><span data-stu-id="c3012-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="c3012-1943">**vValue**: um CBaseStorageVariant que contém o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="c3012-1944">Propriedades de 2.2.1.21.1</span><span class="sxs-lookup"><span data-stu-id="c3012-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="c3012-1945">Esta seção detalha as propriedades que são usadas pelo CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="c3012-1946">Essas propriedades são agrupadas em três conjuntos de propriedades, ident 2.2.1.21.1 ified no campo guidPropertySet da estrutura CDbPropSet (seção 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="c3012-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="c3012-1947">A tabela a seguir lista as propriedades que fazem parte do \_ conjunto de propriedades DBPROPSET FSCIFRMWRK \_ ext.</span><span class="sxs-lookup"><span data-stu-id="c3012-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="c3012-1948">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1948">Value</span></span>                                  | <span data-ttu-id="c3012-1949">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-1950">\_Nome do catálogo de CI DBPROP \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="c3012-1951">Especifica o nome do catálogo ou catálogos a serem consultados.</span><span class="sxs-lookup"><span data-stu-id="c3012-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="c3012-1952">O valor deve ser um ' VT \_ LPWSTR ' ou um \_ LPWSTR de vetor VT de VT \| \_</span><span class="sxs-lookup"><span data-stu-id="c3012-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="c3012-1953">DBPROP \_ CI \_ include \_ escopos 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="c3012-1954">Especifica um ou mais caminhos a serem incluídos na consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="c3012-1955">O valor deve ser um ou um LPWStr de vetor VT de VT \_ ou VT \_ \| \_ .</span><span class="sxs-lookup"><span data-stu-id="c3012-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="c3012-1956">\_Sinalizadores de escopo de CI DBPROP \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="c3012-1957">Especifica como os caminhos especificados pela propriedade DBPROP \_ CI \_ include \_ escopos devem ser tratados.</span><span class="sxs-lookup"><span data-stu-id="c3012-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="c3012-1958">O valor deve ser um VT \_ I4 ou um i4 de vetor VT de VT \_ \| \_ .</span><span class="sxs-lookup"><span data-stu-id="c3012-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="c3012-1959">\_Tipo de \_ consulta DBPROP CI \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3012-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="c3012-1960">Especifica o tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-1960">Specifies the type of query.</span></span> <span data-ttu-id="c3012-1961">O CDbColId deve ser definido para DB \_ nullid.</span><span class="sxs-lookup"><span data-stu-id="c3012-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="c3012-1962">A tabela a seguir lista os sinalizadores para a \_ Propriedade Flags de escopo de CI DBPROP \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="c3012-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="c3012-1963">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1963">Value</span></span>                     | <span data-ttu-id="c3012-1964">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-1965">CONSULTA de \_ 0x01 profunda</span><span class="sxs-lookup"><span data-stu-id="c3012-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="c3012-1966">Se definido, indica que os arquivos no diretório de escopo e todos os subdiretórios estão incluídos nos resultados.</span><span class="sxs-lookup"><span data-stu-id="c3012-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="c3012-1967">Se claro, somente os arquivos no diretório de escopo serão incluídos nos resultados.</span><span class="sxs-lookup"><span data-stu-id="c3012-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="c3012-1968">Não deve ser combinado com a consulta \_ profunda.</span><span class="sxs-lookup"><span data-stu-id="c3012-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="c3012-1969">CONSULTAR \_ \_ caminho virtual 0x02</span><span class="sxs-lookup"><span data-stu-id="c3012-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="c3012-1970">Se definido, indica que o escopo é um caminho virtual.</span><span class="sxs-lookup"><span data-stu-id="c3012-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="c3012-1971">Se claro, indica que o escopo é um diretório físico.</span><span class="sxs-lookup"><span data-stu-id="c3012-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="c3012-1972">A tabela a seguir lista os tipos de consulta para \_ a \_ propriedade tipo de consulta CI DBPROP \_ :</span><span class="sxs-lookup"><span data-stu-id="c3012-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="c3012-1973">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1973">Value</span></span>                     | <span data-ttu-id="c3012-1974">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-1975">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="c3012-1976">Uma consulta regular.</span><span class="sxs-lookup"><span data-stu-id="c3012-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="c3012-1977">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="c3012-1978">A consulta está solicitando uma lista das raízes virtuais do catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="c3012-1979">Esse valor requer privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="c3012-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="c3012-1980">CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="c3012-1981">A consulta está solicitando uma lista de todas as propriedades com suporte no serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="c3012-1982">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="c3012-1983">A consulta é uma operação administrativa.</span><span class="sxs-lookup"><span data-stu-id="c3012-1983">The query is an administrative operation.</span></span> <span data-ttu-id="c3012-1984">Esse valor requer privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="c3012-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="c3012-1985">A tabela a seguir lista as propriedades que fazem parte do \_ conjunto de propriedades DBPROPSET QUERYEXT.</span><span class="sxs-lookup"><span data-stu-id="c3012-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="c3012-1986">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-1986">Value</span></span>                                      | <span data-ttu-id="c3012-1987">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-1988">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="c3012-1989">Especifica como o serviço de indexação é para lidar com consultas lentas.</span><span class="sxs-lookup"><span data-stu-id="c3012-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="c3012-1990">O valor deve ser um VT \_ bool.</span><span class="sxs-lookup"><span data-stu-id="c3012-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="c3012-1991">Se for TRUE, o servidor poderá reprovar essas consultas.</span><span class="sxs-lookup"><span data-stu-id="c3012-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="c3012-1992">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="c3012-1993">Indica se o serviço de indexação é para executar a remoção de resultados.</span><span class="sxs-lookup"><span data-stu-id="c3012-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="c3012-1994">Se for verdadeiro, o servidor deve considerar a realização de recorte de resultados de uma maneira que Otimize o tempo de resposta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="c3012-1995">O valor deve ser um VT \_ bool.</span><span class="sxs-lookup"><span data-stu-id="c3012-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="c3012-1996">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="c3012-1997">Indica se o cliente oferece suporte a \_ tipos de dados de vetor VT.</span><span class="sxs-lookup"><span data-stu-id="c3012-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="c3012-1998">Se for TRUE, o cliente dará suporte a um \_ vetor VT; se for false, o servidor será Converter \_ tipos de dados de vetor VT em \_ tipos de dados de matriz VT.</span><span class="sxs-lookup"><span data-stu-id="c3012-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="c3012-1999">O valor deve ser um VT \_ bool.</span><span class="sxs-lookup"><span data-stu-id="c3012-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="c3012-2000">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3012-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="c3012-2001">Indica as correspondências de linha a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="c3012-2002">Se for TRUE, o servidor será retornar o primeiro conjunto de linhas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="c3012-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="c3012-2003">Se for FALSE, as melhores linhas correspondentes deverão ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="c3012-2004">O valor deve ser um VT \_ bool.</span><span class="sxs-lookup"><span data-stu-id="c3012-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="c3012-2005">A tabela a seguir lista as propriedades que fazem parte do \_ conjunto de propriedades DBPROPSET CIFRMWRKCORE \_ ext.</span><span class="sxs-lookup"><span data-stu-id="c3012-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="c3012-2006">Valor/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="c3012-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="c3012-2007">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-2008">DBPROP do \_ computador 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="c3012-2009">Especifica os nomes dos computadores nos quais uma consulta deve ser processada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="c3012-2010">O valor deve ser VT \_ BSTR ou VT \_ array \| VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="c3012-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="c3012-2011">DBPROP \_ \_ 0x00000003 CLSID do cliente</span><span class="sxs-lookup"><span data-stu-id="c3012-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="c3012-2012">Especifica uma constante de conexão para o serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="c3012-2013">O valor deve ser um VT \_ CLSID contendo 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="c3012-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="c3012-2014">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="c3012-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="c3012-2015">A estrutura CDbPropSet contém um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3012-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="c3012-2016">Observe que o primeiro campo é de tamanho fixo, mas não pode ser alinhado em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="c3012-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="c3012-2017">No entanto, o campo cProperties é alinhado como tal e, portanto, o formato é descrito da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="c3012-2018">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2018">0</span></span>

<span data-ttu-id="c3012-2019">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2019">1</span></span>

<span data-ttu-id="c3012-2020">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2020">2</span></span>

<span data-ttu-id="c3012-2021">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2021">3</span></span>

<span data-ttu-id="c3012-2022">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2022">4</span></span>

<span data-ttu-id="c3012-2023">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2023">5</span></span>

<span data-ttu-id="c3012-2024">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2024">6</span></span>

<span data-ttu-id="c3012-2025">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2025">7</span></span>

<span data-ttu-id="c3012-2026">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2026">8</span></span>

<span data-ttu-id="c3012-2027">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2027">9</span></span>

<span data-ttu-id="c3012-2028">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2028">1</span></span><br/> <span data-ttu-id="c3012-2029">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2029">0</span></span><br/>

<span data-ttu-id="c3012-2030">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2030">1</span></span>

<span data-ttu-id="c3012-2031">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2031">2</span></span>

<span data-ttu-id="c3012-2032">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2032">3</span></span>

<span data-ttu-id="c3012-2033">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2033">4</span></span>

<span data-ttu-id="c3012-2034">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2034">5</span></span>

<span data-ttu-id="c3012-2035">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2035">6</span></span>

<span data-ttu-id="c3012-2036">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2036">7</span></span>

<span data-ttu-id="c3012-2037">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2037">8</span></span>

<span data-ttu-id="c3012-2038">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2038">9</span></span>

<span data-ttu-id="c3012-2039">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2039">2</span></span><br/> <span data-ttu-id="c3012-2040">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2040">0</span></span><br/>

<span data-ttu-id="c3012-2041">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2041">1</span></span>

<span data-ttu-id="c3012-2042">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2042">2</span></span>

<span data-ttu-id="c3012-2043">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2043">3</span></span>

<span data-ttu-id="c3012-2044">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2044">4</span></span>

<span data-ttu-id="c3012-2045">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2045">5</span></span>

<span data-ttu-id="c3012-2046">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2046">6</span></span>

<span data-ttu-id="c3012-2047">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2047">7</span></span>

<span data-ttu-id="c3012-2048">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2048">8</span></span>

<span data-ttu-id="c3012-2049">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2049">9</span></span>

<span data-ttu-id="c3012-2050">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2050">3</span></span><br/> <span data-ttu-id="c3012-2051">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2051">0</span></span><br/>

<span data-ttu-id="c3012-2052">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2052">1</span></span>

<span data-ttu-id="c3012-2053">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="c3012-2053">guidPropertySet</span></span>

<span data-ttu-id="c3012-2054">...</span><span class="sxs-lookup"><span data-stu-id="c3012-2054">...</span></span>

<span data-ttu-id="c3012-2055">...</span><span class="sxs-lookup"><span data-stu-id="c3012-2055">...</span></span>

<span data-ttu-id="c3012-2056">...</span><span class="sxs-lookup"><span data-stu-id="c3012-2056">...</span></span>

<span data-ttu-id="c3012-2057">...</span><span class="sxs-lookup"><span data-stu-id="c3012-2057">...</span></span>

<span data-ttu-id="c3012-2058">\_preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-2058">\_padding (variable)</span></span>

<span data-ttu-id="c3012-2059">cProperties</span><span class="sxs-lookup"><span data-stu-id="c3012-2059">cProperties</span></span>

<span data-ttu-id="c3012-2060">aProps (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-2060">aProps (variable)</span></span>



 

<span data-ttu-id="c3012-2061">**guidPropertySet**: um GUID que identifica o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3012-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="c3012-2062">DEVE ser definido como o formato binário correspondente a um dos valores a seguir (mostrados no formulário de representação da cadeia de caracteres), identificando o conjunto de propriedades dos campos contidos no campo aProps.</span><span class="sxs-lookup"><span data-stu-id="c3012-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="c3012-2063">Valor/GUID</span><span class="sxs-lookup"><span data-stu-id="c3012-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="c3012-2064">Nome</span><span class="sxs-lookup"><span data-stu-id="c3012-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="c3012-2065">DBPROPSET \_ FSCIFRMWRK \_ ext</span><span class="sxs-lookup"><span data-stu-id="c3012-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="c3012-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="c3012-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="c3012-2067">Conjunto de propriedades da estrutura de índice de conteúdo do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="c3012-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="c3012-2068">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="c3012-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="c3012-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="c3012-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="c3012-2070">Conjunto de propriedades de extensão de consulta</span><span class="sxs-lookup"><span data-stu-id="c3012-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="c3012-2071">DBPROPSET \_ CIFRMWRKCORE \_ ext</span><span class="sxs-lookup"><span data-stu-id="c3012-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="c3012-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="c3012-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="c3012-2073">Conjunto de propriedades principais do content index Framework</span><span class="sxs-lookup"><span data-stu-id="c3012-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="c3012-2074">**\_ preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3012-2075">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="c3012-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3012-2076">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3012-2077">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-2078">**cProperties**: um inteiro sem sinal de 32 bits contendo o número de elementos na matriz aProps.</span><span class="sxs-lookup"><span data-stu-id="c3012-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="c3012-2079">**aProps**: uma matriz de estruturas CDbProp, conforme especificado na seção 0, que contém propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3012-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="c3012-2080">As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa matriz.</span><span class="sxs-lookup"><span data-stu-id="c3012-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="c3012-2081">Se os bytes de preenchimento estiverem presentes, o valor que eles contêm será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="c3012-2082">O conteúdo dos bytes de preenchimento deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="c3012-2083">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="c3012-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="c3012-2084">A estrutura CPidMapper contém uma matriz de IDs de propriedade especificando as propriedades a serem retornadas em um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="c3012-2085">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2085">0</span></span>

<span data-ttu-id="c3012-2086">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2086">1</span></span>

<span data-ttu-id="c3012-2087">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2087">2</span></span>

<span data-ttu-id="c3012-2088">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2088">3</span></span>

<span data-ttu-id="c3012-2089">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2089">4</span></span>

<span data-ttu-id="c3012-2090">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2090">5</span></span>

<span data-ttu-id="c3012-2091">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2091">6</span></span>

<span data-ttu-id="c3012-2092">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2092">7</span></span>

<span data-ttu-id="c3012-2093">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2093">8</span></span>

<span data-ttu-id="c3012-2094">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2094">9</span></span>

<span data-ttu-id="c3012-2095">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2095">1</span></span><br/> <span data-ttu-id="c3012-2096">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2096">0</span></span><br/>

<span data-ttu-id="c3012-2097">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2097">1</span></span>

<span data-ttu-id="c3012-2098">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2098">2</span></span>

<span data-ttu-id="c3012-2099">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2099">3</span></span>

<span data-ttu-id="c3012-2100">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2100">4</span></span>

<span data-ttu-id="c3012-2101">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2101">5</span></span>

<span data-ttu-id="c3012-2102">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2102">6</span></span>

<span data-ttu-id="c3012-2103">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2103">7</span></span>

<span data-ttu-id="c3012-2104">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2104">8</span></span>

<span data-ttu-id="c3012-2105">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2105">9</span></span>

<span data-ttu-id="c3012-2106">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2106">2</span></span><br/> <span data-ttu-id="c3012-2107">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2107">0</span></span><br/>

<span data-ttu-id="c3012-2108">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2108">1</span></span>

<span data-ttu-id="c3012-2109">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2109">2</span></span>

<span data-ttu-id="c3012-2110">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2110">3</span></span>

<span data-ttu-id="c3012-2111">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2111">4</span></span>

<span data-ttu-id="c3012-2112">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2112">5</span></span>

<span data-ttu-id="c3012-2113">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2113">6</span></span>

<span data-ttu-id="c3012-2114">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2114">7</span></span>

<span data-ttu-id="c3012-2115">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2115">8</span></span>

<span data-ttu-id="c3012-2116">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2116">9</span></span>

<span data-ttu-id="c3012-2117">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2117">3</span></span><br/> <span data-ttu-id="c3012-2118">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2118">0</span></span><br/>

<span data-ttu-id="c3012-2119">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2119">1</span></span>

<span data-ttu-id="c3012-2120">count</span><span class="sxs-lookup"><span data-stu-id="c3012-2120">count</span></span>

<span data-ttu-id="c3012-2121">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="c3012-2121">aPropSpec</span></span>

<span data-ttu-id="c3012-2122">... Ela</span><span class="sxs-lookup"><span data-stu-id="c3012-2122">... (variable)</span></span>



 

<span data-ttu-id="c3012-2123">**Count**: um inteiro sem sinal de 32 bits contendo o número de elementos na matriz aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="c3012-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="c3012-2124">**aPropSpec**: matriz de estruturas CFullPropSpec que indica as propriedades a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="c3012-2125">As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura tenha um alinhamento de 4 bytes desde o início de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="c3012-2126">Esses bytes de preenchimento podem ser qualquer valor arbitrário e devem ser ignorados no recebimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="c3012-2127">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="c3012-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="c3012-2128">A estrutura CRowSeekAt contém o deslocamento no qual recuperar linhas em uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="c3012-2129">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2129">0</span></span>

<span data-ttu-id="c3012-2130">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2130">1</span></span>

<span data-ttu-id="c3012-2131">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2131">2</span></span>

<span data-ttu-id="c3012-2132">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2132">3</span></span>

<span data-ttu-id="c3012-2133">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2133">4</span></span>

<span data-ttu-id="c3012-2134">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2134">5</span></span>

<span data-ttu-id="c3012-2135">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2135">6</span></span>

<span data-ttu-id="c3012-2136">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2136">7</span></span>

<span data-ttu-id="c3012-2137">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2137">8</span></span>

<span data-ttu-id="c3012-2138">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2138">9</span></span>

<span data-ttu-id="c3012-2139">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2139">1</span></span><br/> <span data-ttu-id="c3012-2140">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2140">0</span></span><br/>

<span data-ttu-id="c3012-2141">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2141">1</span></span>

<span data-ttu-id="c3012-2142">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2142">2</span></span>

<span data-ttu-id="c3012-2143">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2143">3</span></span>

<span data-ttu-id="c3012-2144">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2144">4</span></span>

<span data-ttu-id="c3012-2145">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2145">5</span></span>

<span data-ttu-id="c3012-2146">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2146">6</span></span>

<span data-ttu-id="c3012-2147">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2147">7</span></span>

<span data-ttu-id="c3012-2148">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2148">8</span></span>

<span data-ttu-id="c3012-2149">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2149">9</span></span>

<span data-ttu-id="c3012-2150">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2150">2</span></span><br/> <span data-ttu-id="c3012-2151">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2151">0</span></span><br/>

<span data-ttu-id="c3012-2152">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2152">1</span></span>

<span data-ttu-id="c3012-2153">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2153">2</span></span>

<span data-ttu-id="c3012-2154">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2154">3</span></span>

<span data-ttu-id="c3012-2155">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2155">4</span></span>

<span data-ttu-id="c3012-2156">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2156">5</span></span>

<span data-ttu-id="c3012-2157">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2157">6</span></span>

<span data-ttu-id="c3012-2158">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2158">7</span></span>

<span data-ttu-id="c3012-2159">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2159">8</span></span>

<span data-ttu-id="c3012-2160">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2160">9</span></span>

<span data-ttu-id="c3012-2161">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2161">3</span></span><br/> <span data-ttu-id="c3012-2162">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2162">0</span></span><br/>

<span data-ttu-id="c3012-2163">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2163">1</span></span>

<span data-ttu-id="c3012-2164">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="c3012-2164">\_hRegion</span></span>

<span data-ttu-id="c3012-2165">\_cskip</span><span class="sxs-lookup"><span data-stu-id="c3012-2165">\_cskip</span></span>

<span data-ttu-id="c3012-2166">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="c3012-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="c3012-2167">**\_ hRegion**: deve ser definido como 0x00000000 e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="c3012-2168">**\_ cskip**: um inteiro sem sinal de 32 bits contendo o número de linhas a serem ignoradas no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="c3012-2169">**\_ bmkOffset**: um valor de 32 bits que representa o identificador do **indicador** que indica a posição inicial a partir da qual ignorar o número de linhas especificado em \_ cskip, antes de iniciar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="c3012-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="c3012-2170">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="c3012-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="c3012-2171">A estrutura CRowSeekAtRatio identifica o ponto no qual iniciar a recuperação para uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="c3012-2172">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2172">0</span></span>

<span data-ttu-id="c3012-2173">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2173">1</span></span>

<span data-ttu-id="c3012-2174">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2174">2</span></span>

<span data-ttu-id="c3012-2175">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2175">3</span></span>

<span data-ttu-id="c3012-2176">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2176">4</span></span>

<span data-ttu-id="c3012-2177">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2177">5</span></span>

<span data-ttu-id="c3012-2178">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2178">6</span></span>

<span data-ttu-id="c3012-2179">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2179">7</span></span>

<span data-ttu-id="c3012-2180">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2180">8</span></span>

<span data-ttu-id="c3012-2181">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2181">9</span></span>

<span data-ttu-id="c3012-2182">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2182">1</span></span><br/> <span data-ttu-id="c3012-2183">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2183">0</span></span><br/>

<span data-ttu-id="c3012-2184">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2184">1</span></span>

<span data-ttu-id="c3012-2185">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2185">2</span></span>

<span data-ttu-id="c3012-2186">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2186">3</span></span>

<span data-ttu-id="c3012-2187">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2187">4</span></span>

<span data-ttu-id="c3012-2188">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2188">5</span></span>

<span data-ttu-id="c3012-2189">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2189">6</span></span>

<span data-ttu-id="c3012-2190">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2190">7</span></span>

<span data-ttu-id="c3012-2191">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2191">8</span></span>

<span data-ttu-id="c3012-2192">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2192">9</span></span>

<span data-ttu-id="c3012-2193">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2193">2</span></span><br/> <span data-ttu-id="c3012-2194">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2194">0</span></span><br/>

<span data-ttu-id="c3012-2195">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2195">1</span></span>

<span data-ttu-id="c3012-2196">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2196">2</span></span>

<span data-ttu-id="c3012-2197">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2197">3</span></span>

<span data-ttu-id="c3012-2198">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2198">4</span></span>

<span data-ttu-id="c3012-2199">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2199">5</span></span>

<span data-ttu-id="c3012-2200">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2200">6</span></span>

<span data-ttu-id="c3012-2201">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2201">7</span></span>

<span data-ttu-id="c3012-2202">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2202">8</span></span>

<span data-ttu-id="c3012-2203">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2203">9</span></span>

<span data-ttu-id="c3012-2204">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2204">3</span></span><br/> <span data-ttu-id="c3012-2205">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2205">0</span></span><br/>

<span data-ttu-id="c3012-2206">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2206">1</span></span>

<span data-ttu-id="c3012-2207">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="c3012-2207">CiTblChapt</span></span>

<span data-ttu-id="c3012-2208">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="c3012-2208">\_hRegion</span></span>

<span data-ttu-id="c3012-2209">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="c3012-2209">\_ulNumerator</span></span>

<span data-ttu-id="c3012-2210">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="c3012-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="c3012-2211">**CiTblChapt**: um inteiro de 32 bits sem sinal indicando o capítulo do conjunto de linhas do qual recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="c3012-2212">**\_ hRegion**: deve ser definido como 0x00000000 e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="c3012-2213">**\_ ulNumerator**: inteiro de 32 bits sem sinal que representa o numerador da proporção de linhas no capítulo no qual iniciar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="c3012-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="c3012-2214">**\_ ulDenominator**: inteiro de 32 bits sem sinal que representa o denominador da proporção de linhas no capítulo no qual iniciar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="c3012-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="c3012-2215">DEVE ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="c3012-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="c3012-2216">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="c3012-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="c3012-2217">A estrutura CRowSeekByBookmark identifica os indicadores dos quais começar a recuperar linhas para uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="c3012-2218">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2218">0</span></span>

<span data-ttu-id="c3012-2219">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2219">1</span></span>

<span data-ttu-id="c3012-2220">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2220">2</span></span>

<span data-ttu-id="c3012-2221">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2221">3</span></span>

<span data-ttu-id="c3012-2222">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2222">4</span></span>

<span data-ttu-id="c3012-2223">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2223">5</span></span>

<span data-ttu-id="c3012-2224">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2224">6</span></span>

<span data-ttu-id="c3012-2225">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2225">7</span></span>

<span data-ttu-id="c3012-2226">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2226">8</span></span>

<span data-ttu-id="c3012-2227">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2227">9</span></span>

<span data-ttu-id="c3012-2228">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2228">1</span></span><br/> <span data-ttu-id="c3012-2229">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2229">0</span></span><br/>

<span data-ttu-id="c3012-2230">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2230">1</span></span>

<span data-ttu-id="c3012-2231">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2231">2</span></span>

<span data-ttu-id="c3012-2232">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2232">3</span></span>

<span data-ttu-id="c3012-2233">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2233">4</span></span>

<span data-ttu-id="c3012-2234">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2234">5</span></span>

<span data-ttu-id="c3012-2235">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2235">6</span></span>

<span data-ttu-id="c3012-2236">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2236">7</span></span>

<span data-ttu-id="c3012-2237">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2237">8</span></span>

<span data-ttu-id="c3012-2238">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2238">9</span></span>

<span data-ttu-id="c3012-2239">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2239">2</span></span><br/> <span data-ttu-id="c3012-2240">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2240">0</span></span><br/>

<span data-ttu-id="c3012-2241">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2241">1</span></span>

<span data-ttu-id="c3012-2242">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2242">2</span></span>

<span data-ttu-id="c3012-2243">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2243">3</span></span>

<span data-ttu-id="c3012-2244">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2244">4</span></span>

<span data-ttu-id="c3012-2245">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2245">5</span></span>

<span data-ttu-id="c3012-2246">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2246">6</span></span>

<span data-ttu-id="c3012-2247">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2247">7</span></span>

<span data-ttu-id="c3012-2248">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2248">8</span></span>

<span data-ttu-id="c3012-2249">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2249">9</span></span>

<span data-ttu-id="c3012-2250">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2250">3</span></span><br/> <span data-ttu-id="c3012-2251">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2251">0</span></span><br/>

<span data-ttu-id="c3012-2252">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2252">1</span></span>

<span data-ttu-id="c3012-2253">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="c3012-2253">\_hRegion</span></span>

<span data-ttu-id="c3012-2254">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="c3012-2254">\_cBookmarks</span></span>

<span data-ttu-id="c3012-2255">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="c3012-2255">\_maxRet</span></span>

<span data-ttu-id="c3012-2256">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="c3012-2256">\_cValidRet</span></span>

<span data-ttu-id="c3012-2257">\_aBookmarks (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="c3012-2258">\_ascRet (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="c3012-2259">**\_ hRegion**: deve ser definido como 0x00000000 e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="c3012-2260">**\_ cBookmarks**: inteiro de 32 bits sem sinal representando o número de elementos na \_ matriz aBookmarks.</span><span class="sxs-lookup"><span data-stu-id="c3012-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="c3012-2261">**\_ maxRet**: inteiro de 32 bits sem sinal representando o número de elementos na \_ matriz ascRet.</span><span class="sxs-lookup"><span data-stu-id="c3012-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="c3012-2262">**\_ cValidRet**: inteiro de 32 bits sem sinal que representa o número de elementos na \_ matriz ascRet que são válidos.</span><span class="sxs-lookup"><span data-stu-id="c3012-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="c3012-2263">Elementos válidos foram definidos na matriz, enquanto elementos inválidos são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="c3012-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="c3012-2264">**\_ aBookmarks**: uma matriz de alças de indicador (cada uma representada por 4 bytes), conforme Obtida de uma mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="c3012-2265">**\_ ascRet**: uma matriz de valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c3012-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="c3012-2266">Quando o CRowSeekByBookMark é enviado como parte da solicitação CPMGetRowsIn, o número de entradas na matriz deve ser igual a \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="c3012-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="c3012-2267">Quando enviado pelo cliente, os valores devem ser definidos como zero e o servidor deve ignorar o conteúdo da matriz.</span><span class="sxs-lookup"><span data-stu-id="c3012-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="c3012-2268">Quando enviado pelo servidor (como parte da mensagem CPMGetRowsOut), os valores na matriz indicam o status do resultado para cada recuperação de linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="c3012-2269">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="c3012-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="c3012-2270">A estrutura CRowSeekNext contém o número de linhas a serem ignoradas em uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="c3012-2271">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2271">0</span></span>

<span data-ttu-id="c3012-2272">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2272">1</span></span>

<span data-ttu-id="c3012-2273">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2273">2</span></span>

<span data-ttu-id="c3012-2274">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2274">3</span></span>

<span data-ttu-id="c3012-2275">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2275">4</span></span>

<span data-ttu-id="c3012-2276">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2276">5</span></span>

<span data-ttu-id="c3012-2277">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2277">6</span></span>

<span data-ttu-id="c3012-2278">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2278">7</span></span>

<span data-ttu-id="c3012-2279">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2279">8</span></span>

<span data-ttu-id="c3012-2280">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2280">9</span></span>

<span data-ttu-id="c3012-2281">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2281">1</span></span><br/> <span data-ttu-id="c3012-2282">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2282">0</span></span><br/>

<span data-ttu-id="c3012-2283">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2283">1</span></span>

<span data-ttu-id="c3012-2284">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2284">2</span></span>

<span data-ttu-id="c3012-2285">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2285">3</span></span>

<span data-ttu-id="c3012-2286">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2286">4</span></span>

<span data-ttu-id="c3012-2287">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2287">5</span></span>

<span data-ttu-id="c3012-2288">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2288">6</span></span>

<span data-ttu-id="c3012-2289">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2289">7</span></span>

<span data-ttu-id="c3012-2290">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2290">8</span></span>

<span data-ttu-id="c3012-2291">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2291">9</span></span>

<span data-ttu-id="c3012-2292">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2292">2</span></span><br/> <span data-ttu-id="c3012-2293">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2293">0</span></span><br/>

<span data-ttu-id="c3012-2294">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2294">1</span></span>

<span data-ttu-id="c3012-2295">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2295">2</span></span>

<span data-ttu-id="c3012-2296">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2296">3</span></span>

<span data-ttu-id="c3012-2297">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2297">4</span></span>

<span data-ttu-id="c3012-2298">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2298">5</span></span>

<span data-ttu-id="c3012-2299">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2299">6</span></span>

<span data-ttu-id="c3012-2300">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2300">7</span></span>

<span data-ttu-id="c3012-2301">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2301">8</span></span>

<span data-ttu-id="c3012-2302">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2302">9</span></span>

<span data-ttu-id="c3012-2303">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2303">3</span></span><br/> <span data-ttu-id="c3012-2304">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2304">0</span></span><br/>

<span data-ttu-id="c3012-2305">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2305">1</span></span>

<span data-ttu-id="c3012-2306">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="c3012-2306">CiTblChapt</span></span>

<span data-ttu-id="c3012-2307">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="c3012-2307">\_hRegion</span></span>

<span data-ttu-id="c3012-2308">\_cskip</span><span class="sxs-lookup"><span data-stu-id="c3012-2308">\_cskip</span></span>



 

<span data-ttu-id="c3012-2309">**CiTblChapt**: inteiro de 32 bits sem sinal especificando o capítulo do conjunto de linhas do qual recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="c3012-2310">**\_ hRegion**: deve ser definido como 0x00000000 e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="c3012-2311">**\_ cskip**: inteiro de 32 bits sem sinal representando o número de linhas a serem ignoradas no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="c3012-2312">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="c3012-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="c3012-2313">A estrutura CRowsetProperties contém informações de configuração para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="c3012-2314">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2314">0</span></span>

<span data-ttu-id="c3012-2315">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2315">1</span></span>

<span data-ttu-id="c3012-2316">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2316">2</span></span>

<span data-ttu-id="c3012-2317">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2317">3</span></span>

<span data-ttu-id="c3012-2318">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2318">4</span></span>

<span data-ttu-id="c3012-2319">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2319">5</span></span>

<span data-ttu-id="c3012-2320">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2320">6</span></span>

<span data-ttu-id="c3012-2321">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2321">7</span></span>

<span data-ttu-id="c3012-2322">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2322">8</span></span>

<span data-ttu-id="c3012-2323">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2323">9</span></span>

<span data-ttu-id="c3012-2324">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2324">1</span></span><br/> <span data-ttu-id="c3012-2325">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2325">0</span></span><br/>

<span data-ttu-id="c3012-2326">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2326">1</span></span>

<span data-ttu-id="c3012-2327">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2327">2</span></span>

<span data-ttu-id="c3012-2328">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2328">3</span></span>

<span data-ttu-id="c3012-2329">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2329">4</span></span>

<span data-ttu-id="c3012-2330">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2330">5</span></span>

<span data-ttu-id="c3012-2331">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2331">6</span></span>

<span data-ttu-id="c3012-2332">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2332">7</span></span>

<span data-ttu-id="c3012-2333">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2333">8</span></span>

<span data-ttu-id="c3012-2334">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2334">9</span></span>

<span data-ttu-id="c3012-2335">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2335">2</span></span><br/> <span data-ttu-id="c3012-2336">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2336">0</span></span><br/>

<span data-ttu-id="c3012-2337">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2337">1</span></span>

<span data-ttu-id="c3012-2338">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2338">2</span></span>

<span data-ttu-id="c3012-2339">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2339">3</span></span>

<span data-ttu-id="c3012-2340">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2340">4</span></span>

<span data-ttu-id="c3012-2341">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2341">5</span></span>

<span data-ttu-id="c3012-2342">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2342">6</span></span>

<span data-ttu-id="c3012-2343">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2343">7</span></span>

<span data-ttu-id="c3012-2344">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2344">8</span></span>

<span data-ttu-id="c3012-2345">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2345">9</span></span>

<span data-ttu-id="c3012-2346">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2346">3</span></span><br/> <span data-ttu-id="c3012-2347">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2347">0</span></span><br/>

<span data-ttu-id="c3012-2348">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2348">1</span></span>

<span data-ttu-id="c3012-2349">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="c3012-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="c3012-2350">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="c3012-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="c3012-2351">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="c3012-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="c3012-2352">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="c3012-2352">\_cMaxResults</span></span>

<span data-ttu-id="c3012-2353">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="c3012-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="c3012-2354">**\_ uBooleanOptions**: os 3 bits menos significativos desse campo devem conter um dos três valores a seguir:</span><span class="sxs-lookup"><span data-stu-id="c3012-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="c3012-2355">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-2355">Value</span></span>                  | <span data-ttu-id="c3012-2356">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c3012-2357">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="c3012-2358">O cursor só pode ser movido para frente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="c3012-2359">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="c3012-2360">O cursor pode ser movido para qualquer posição.</span><span class="sxs-lookup"><span data-stu-id="c3012-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="c3012-2361">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3012-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="c3012-2362">O cursor pode ser movido para qualquer posição e busca em qualquer direção.</span><span class="sxs-lookup"><span data-stu-id="c3012-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="c3012-2363">Os bits restantes podem ser claros ou definidos para qualquer combinação dos valores a seguir logicamente ou juntos:</span><span class="sxs-lookup"><span data-stu-id="c3012-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="c3012-2364">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-2364">Value</span></span>                     | <span data-ttu-id="c3012-2365">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-2366">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3012-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="c3012-2367">O cliente não aguardará a conclusão da execução.</span><span class="sxs-lookup"><span data-stu-id="c3012-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="c3012-2368">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="c3012-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="c3012-2369">Retorna as primeiras linhas encontradas, não as melhores correspondências.</span><span class="sxs-lookup"><span data-stu-id="c3012-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="c3012-2370">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="c3012-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="c3012-2371">O servidor não deve descartar linhas até que o cliente seja concluído com uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="c3012-2372">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="c3012-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="c3012-2373">O conjunto de linhas oferece suporte a capítulos.</span><span class="sxs-lookup"><span data-stu-id="c3012-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="c3012-2374">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="c3012-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="c3012-2375">Responda apenas à consulta do índice, não do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c3012-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="c3012-2376">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="c3012-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="c3012-2377">O serviço de indexação é considerar a otimização do tempo de resposta para o cliente ao executar a remoção de resultados.</span><span class="sxs-lookup"><span data-stu-id="c3012-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="c3012-2378">**\_ ulMaxOpenRows**: inteiro de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="c3012-2379">Deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="c3012-2380">Não usado e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="c3012-2381">**\_ ulMemoryUsage**: inteiro de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="c3012-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="c3012-2382">Deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="c3012-2383">Não usado e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="c3012-2384">**\_ cMaxResults**: um inteiro sem sinal de 32 bits especificando o número máximo de linhas que devem ser retornadas para a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="c3012-2385">**\_ cCmdTimeout**: um inteiro sem sinal de 32 bits, especificando o número de segundos em que uma consulta deve atingir o tempo limite e terminar automaticamente, contando desde o momento em que a consulta começa a ser executada no servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="c3012-2386">Um valor de 0x00000000 significa que a consulta não está expirando.</span><span class="sxs-lookup"><span data-stu-id="c3012-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="c3012-2387">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="c3012-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="c3012-2388">A estrutura CRowVariant contém a parte de tamanho fixo de um tipo de dados de comprimento variável armazenado na mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="c3012-2389">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2389">0</span></span>

<span data-ttu-id="c3012-2390">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2390">1</span></span>

<span data-ttu-id="c3012-2391">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2391">2</span></span>

<span data-ttu-id="c3012-2392">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2392">3</span></span>

<span data-ttu-id="c3012-2393">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2393">4</span></span>

<span data-ttu-id="c3012-2394">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2394">5</span></span>

<span data-ttu-id="c3012-2395">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2395">6</span></span>

<span data-ttu-id="c3012-2396">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2396">7</span></span>

<span data-ttu-id="c3012-2397">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2397">8</span></span>

<span data-ttu-id="c3012-2398">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2398">9</span></span>

<span data-ttu-id="c3012-2399">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2399">1</span></span><br/> <span data-ttu-id="c3012-2400">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2400">0</span></span><br/>

<span data-ttu-id="c3012-2401">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2401">1</span></span>

<span data-ttu-id="c3012-2402">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2402">2</span></span>

<span data-ttu-id="c3012-2403">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2403">3</span></span>

<span data-ttu-id="c3012-2404">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2404">4</span></span>

<span data-ttu-id="c3012-2405">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2405">5</span></span>

<span data-ttu-id="c3012-2406">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2406">6</span></span>

<span data-ttu-id="c3012-2407">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2407">7</span></span>

<span data-ttu-id="c3012-2408">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2408">8</span></span>

<span data-ttu-id="c3012-2409">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2409">9</span></span>

<span data-ttu-id="c3012-2410">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2410">2</span></span><br/> <span data-ttu-id="c3012-2411">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2411">0</span></span><br/>

<span data-ttu-id="c3012-2412">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2412">1</span></span>

<span data-ttu-id="c3012-2413">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2413">2</span></span>

<span data-ttu-id="c3012-2414">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2414">3</span></span>

<span data-ttu-id="c3012-2415">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2415">4</span></span>

<span data-ttu-id="c3012-2416">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2416">5</span></span>

<span data-ttu-id="c3012-2417">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2417">6</span></span>

<span data-ttu-id="c3012-2418">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2418">7</span></span>

<span data-ttu-id="c3012-2419">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2419">8</span></span>

<span data-ttu-id="c3012-2420">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2420">9</span></span>

<span data-ttu-id="c3012-2421">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2421">3</span></span><br/> <span data-ttu-id="c3012-2422">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2422">0</span></span><br/>

<span data-ttu-id="c3012-2423">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2423">1</span></span>

<span data-ttu-id="c3012-2424">vType</span><span class="sxs-lookup"><span data-stu-id="c3012-2424">vType</span></span>

<span data-ttu-id="c3012-2425">reserved1</span><span class="sxs-lookup"><span data-stu-id="c3012-2425">reserved1</span></span>

<span data-ttu-id="c3012-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="c3012-2426">reserved2</span></span>

<span data-ttu-id="c3012-2427">Deslocamento (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2427">Offset (optional)</span></span>



 

<span data-ttu-id="c3012-2428">**vType**: um indicador de tipo, que indica o tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="c3012-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="c3012-2429">Ele deve ser um dos valores de VARENUM especificados na seção 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="c3012-2430">**reserved1**: não usado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="c3012-2431">O valor pode ser definido como qualquer valor arbitrário e deve ser ignorado no recebimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="c3012-2432">**reserved2**: não usado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="c3012-2433">O valor pode ser definido como qualquer valor arbitrário e deve ser ignorado no recebimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="c3012-2434">**Offset**: um deslocamento para dados de comprimento variável (por exemplo, uma cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="c3012-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="c3012-2435">Esse deve ser um valor de 32 bits (4 bytes de comprimento) se os deslocamentos de 32 bits estiverem sendo usados (de acordo com as regras na seção 2.2.3.16) ou um valor de 64 byte (8 bytes de comprimento) se os deslocamentos de 64 bits estiverem sendo usados.</span><span class="sxs-lookup"><span data-stu-id="c3012-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="c3012-2436">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="c3012-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="c3012-2437">A estrutura CSortSet contém a ordem de classificação da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="c3012-2438">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2438">0</span></span>

<span data-ttu-id="c3012-2439">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2439">1</span></span>

<span data-ttu-id="c3012-2440">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2440">2</span></span>

<span data-ttu-id="c3012-2441">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2441">3</span></span>

<span data-ttu-id="c3012-2442">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2442">4</span></span>

<span data-ttu-id="c3012-2443">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2443">5</span></span>

<span data-ttu-id="c3012-2444">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2444">6</span></span>

<span data-ttu-id="c3012-2445">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2445">7</span></span>

<span data-ttu-id="c3012-2446">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2446">8</span></span>

<span data-ttu-id="c3012-2447">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2447">9</span></span>

<span data-ttu-id="c3012-2448">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2448">1</span></span><br/> <span data-ttu-id="c3012-2449">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2449">0</span></span><br/>

<span data-ttu-id="c3012-2450">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2450">1</span></span>

<span data-ttu-id="c3012-2451">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2451">2</span></span>

<span data-ttu-id="c3012-2452">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2452">3</span></span>

<span data-ttu-id="c3012-2453">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2453">4</span></span>

<span data-ttu-id="c3012-2454">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2454">5</span></span>

<span data-ttu-id="c3012-2455">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2455">6</span></span>

<span data-ttu-id="c3012-2456">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2456">7</span></span>

<span data-ttu-id="c3012-2457">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2457">8</span></span>

<span data-ttu-id="c3012-2458">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2458">9</span></span>

<span data-ttu-id="c3012-2459">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2459">2</span></span><br/> <span data-ttu-id="c3012-2460">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2460">0</span></span><br/>

<span data-ttu-id="c3012-2461">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2461">1</span></span>

<span data-ttu-id="c3012-2462">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2462">2</span></span>

<span data-ttu-id="c3012-2463">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2463">3</span></span>

<span data-ttu-id="c3012-2464">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2464">4</span></span>

<span data-ttu-id="c3012-2465">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2465">5</span></span>

<span data-ttu-id="c3012-2466">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2466">6</span></span>

<span data-ttu-id="c3012-2467">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2467">7</span></span>

<span data-ttu-id="c3012-2468">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2468">8</span></span>

<span data-ttu-id="c3012-2469">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2469">9</span></span>

<span data-ttu-id="c3012-2470">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2470">3</span></span><br/> <span data-ttu-id="c3012-2471">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2471">0</span></span><br/>

<span data-ttu-id="c3012-2472">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2472">1</span></span>

<span data-ttu-id="c3012-2473">Contagem</span><span class="sxs-lookup"><span data-stu-id="c3012-2473">Count</span></span>

<span data-ttu-id="c3012-2474">sortArray (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="c3012-2475">**Count**: um inteiro sem sinal de 32 bits especificando o número de elementos em sortArray.</span><span class="sxs-lookup"><span data-stu-id="c3012-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="c3012-2476">**sortArray**: uma matriz de estruturas CSort que descreve a ordem na qual os resultados da consulta são classificados.</span><span class="sxs-lookup"><span data-stu-id="c3012-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="c3012-2477">As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura tenha um alinhamento de 4 bytes desde o início de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="c3012-2478">Esses bytes de preenchimento podem ser qualquer valor arbitrário e devem ser ignorados no recebimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="c3012-2479">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="c3012-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="c3012-2480">A estrutura CTableColumn contém uma coluna de uma mensagem CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="c3012-2481">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2481">0</span></span>

<span data-ttu-id="c3012-2482">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2482">1</span></span>

<span data-ttu-id="c3012-2483">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2483">2</span></span>

<span data-ttu-id="c3012-2484">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2484">3</span></span>

<span data-ttu-id="c3012-2485">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2485">4</span></span>

<span data-ttu-id="c3012-2486">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2486">5</span></span>

<span data-ttu-id="c3012-2487">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2487">6</span></span>

<span data-ttu-id="c3012-2488">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2488">7</span></span>

<span data-ttu-id="c3012-2489">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2489">8</span></span>

<span data-ttu-id="c3012-2490">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2490">9</span></span>

<span data-ttu-id="c3012-2491">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2491">1</span></span><br/> <span data-ttu-id="c3012-2492">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2492">0</span></span><br/>

<span data-ttu-id="c3012-2493">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2493">1</span></span>

<span data-ttu-id="c3012-2494">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2494">2</span></span>

<span data-ttu-id="c3012-2495">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2495">3</span></span>

<span data-ttu-id="c3012-2496">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2496">4</span></span>

<span data-ttu-id="c3012-2497">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2497">5</span></span>

<span data-ttu-id="c3012-2498">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2498">6</span></span>

<span data-ttu-id="c3012-2499">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2499">7</span></span>

<span data-ttu-id="c3012-2500">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2500">8</span></span>

<span data-ttu-id="c3012-2501">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2501">9</span></span>

<span data-ttu-id="c3012-2502">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2502">2</span></span><br/> <span data-ttu-id="c3012-2503">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2503">0</span></span><br/>

<span data-ttu-id="c3012-2504">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2504">1</span></span>

<span data-ttu-id="c3012-2505">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2505">2</span></span>

<span data-ttu-id="c3012-2506">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2506">3</span></span>

<span data-ttu-id="c3012-2507">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2507">4</span></span>

<span data-ttu-id="c3012-2508">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2508">5</span></span>

<span data-ttu-id="c3012-2509">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2509">6</span></span>

<span data-ttu-id="c3012-2510">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2510">7</span></span>

<span data-ttu-id="c3012-2511">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2511">8</span></span>

<span data-ttu-id="c3012-2512">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2512">9</span></span>

<span data-ttu-id="c3012-2513">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2513">3</span></span><br/> <span data-ttu-id="c3012-2514">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2514">0</span></span><br/>

<span data-ttu-id="c3012-2515">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2515">1</span></span>

<span data-ttu-id="c3012-2516">PropSpec</span><span class="sxs-lookup"><span data-stu-id="c3012-2516">PropSpec</span></span>

<span data-ttu-id="c3012-2517">... Ela</span><span class="sxs-lookup"><span data-stu-id="c3012-2517">...(variable)</span></span>

<span data-ttu-id="c3012-2518">vType</span><span class="sxs-lookup"><span data-stu-id="c3012-2518">vType</span></span>

<span data-ttu-id="c3012-2519">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="c3012-2519">ValueUsed</span></span>

<span data-ttu-id="c3012-2520">\_padding1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="c3012-2521">ValueOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="c3012-2522">Valores (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2522">ValueSize (optional)</span></span>

<span data-ttu-id="c3012-2523">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="c3012-2523">StatusUsed</span></span>

<span data-ttu-id="c3012-2524">\_padding2 (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="c3012-2525">StatusOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="c3012-2526">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="c3012-2526">LengthUsed</span></span>

<span data-ttu-id="c3012-2527">\_padding3 (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="c3012-2528">LengthOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="c3012-2529">**PropSpec**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="c3012-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="c3012-2530">**vType**: especifica o tipo de valor de dados contido na coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="c3012-2531">Consulte o campo vType na seção 2.2.1.1 para obter a lista de valores para esse campo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="c3012-2532">**ValueUsed**: um campo de um byte que deve ser definido como 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3012-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="c3012-2533">Se definido como 0x01, a coluna será transferida dentro da linha de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="c3012-2534">Se definido como 0x00, o valor da coluna será transferido na seção de comprimento variável no final do buffer.</span><span class="sxs-lookup"><span data-stu-id="c3012-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="c3012-2535">**\_ padding1**: um campo de um byte que deve ser inserido antes de ValueOffset se, sem ele, ValueOffset não começaria em um deslocamento par do início da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="c3012-2536">O valor desse byte é arbitrário e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="c3012-2537">Se ValueUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3012-2538">**ValueOffset**: um inteiro de 2 bytes não assinado que especifica o deslocamento do valor da coluna na linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="c3012-2539">Se ValueUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3012-2540">**Values**: um inteiro de 2 bytes sem sinal especificando o tamanho do valor da coluna em bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="c3012-2541">Se ValueUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3012-2542">**StatusUsed**: um campo de um byte que deve ser definido como 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3012-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="c3012-2543">Se definido como 0x01, o status da coluna será transferido dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="c3012-2544">Se 0x00, o status da coluna não será transferido dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="c3012-2545">**\_ padding2**: um campo de um byte que deve ser inserido antes de StatusOffset se, sem ele, o campo StatusOffset não começaria em um deslocamento par do início da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="c3012-2546">O valor desse byte é arbitrário e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="c3012-2547">Se StatusUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3012-2548">**StatusOffset**: um inteiro de 2 bytes não assinado que especifica o deslocamento do status da coluna na linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="c3012-2549">Se StatusUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3012-2550">**LengthUsed**: um campo de um byte que deve ser definido como 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3012-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="c3012-2551">Se definido como 0x01, o comprimento da coluna é transferido dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="c3012-2552">Se 0x00, o comprimento da coluna não deve ser transferido dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="c3012-2553">**\_ padding3**: um campo de um byte que deve ser inserido antes de LengthOffset se, sem ele, LengthOffset não começaria em um deslocamento par do início de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="c3012-2554">O valor desse byte é arbitrário e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="c3012-2555">Se LengthUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3012-2556">**LengthOffset**: um inteiro de 2 bytes não assinado que especifica o deslocamento do comprimento da coluna na linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="c3012-2557">Se LengthUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="c3012-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="c3012-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="c3012-2559">A estrutura SERIALIZEDPROPERTYVALUE contém um valor serializado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="c3012-2560">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2560">0</span></span>

<span data-ttu-id="c3012-2561">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2561">1</span></span>

<span data-ttu-id="c3012-2562">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2562">2</span></span>

<span data-ttu-id="c3012-2563">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2563">3</span></span>

<span data-ttu-id="c3012-2564">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2564">4</span></span>

<span data-ttu-id="c3012-2565">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2565">5</span></span>

<span data-ttu-id="c3012-2566">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2566">6</span></span>

<span data-ttu-id="c3012-2567">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2567">7</span></span>

<span data-ttu-id="c3012-2568">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2568">8</span></span>

<span data-ttu-id="c3012-2569">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2569">9</span></span>

<span data-ttu-id="c3012-2570">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2570">1</span></span><br/> <span data-ttu-id="c3012-2571">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2571">0</span></span><br/>

<span data-ttu-id="c3012-2572">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2572">1</span></span>

<span data-ttu-id="c3012-2573">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2573">2</span></span>

<span data-ttu-id="c3012-2574">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2574">3</span></span>

<span data-ttu-id="c3012-2575">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2575">4</span></span>

<span data-ttu-id="c3012-2576">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2576">5</span></span>

<span data-ttu-id="c3012-2577">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2577">6</span></span>

<span data-ttu-id="c3012-2578">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2578">7</span></span>

<span data-ttu-id="c3012-2579">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2579">8</span></span>

<span data-ttu-id="c3012-2580">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2580">9</span></span>

<span data-ttu-id="c3012-2581">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2581">2</span></span><br/> <span data-ttu-id="c3012-2582">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2582">0</span></span><br/>

<span data-ttu-id="c3012-2583">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2583">1</span></span>

<span data-ttu-id="c3012-2584">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2584">2</span></span>

<span data-ttu-id="c3012-2585">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2585">3</span></span>

<span data-ttu-id="c3012-2586">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2586">4</span></span>

<span data-ttu-id="c3012-2587">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2587">5</span></span>

<span data-ttu-id="c3012-2588">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2588">6</span></span>

<span data-ttu-id="c3012-2589">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2589">7</span></span>

<span data-ttu-id="c3012-2590">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2590">8</span></span>

<span data-ttu-id="c3012-2591">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2591">9</span></span>

<span data-ttu-id="c3012-2592">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2592">3</span></span><br/> <span data-ttu-id="c3012-2593">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2593">0</span></span><br/>

<span data-ttu-id="c3012-2594">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2594">1</span></span>

<span data-ttu-id="c3012-2595">dwType</span><span class="sxs-lookup"><span data-stu-id="c3012-2595">dwType</span></span>

<span data-ttu-id="c3012-2596">RGB (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-2596">rgb (variable)</span></span>



 

<span data-ttu-id="c3012-2597">**dwType**: um dos tipos variantes, definidos na seção 2.2.1.1, que podem ser combinados com modificadores de tipo Variant.</span><span class="sxs-lookup"><span data-stu-id="c3012-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="c3012-2598">Para todos os tipos de variantes, exceto aqueles combinados com \_ a matriz VT, SERIALIZEDPROPERTYVALUE tem o mesmo layout que CBaseStorageVariant, conforme especificado na seção 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="c3012-2599">Se o tipo Variant for combinado com o \_ modificador de tipo de matriz VT, SAFEARRAY2, especificado na seção 2.2.1.2.1.1, será usado em vez de SAFEARRAY no campo vValue de CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="c3012-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="c3012-2600">**RGB**: valor serializado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="c3012-2601">Veja detalhes de serialização para vValue em 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="c3012-2602">Cabeçalhos de mensagem 2.2.2</span><span class="sxs-lookup"><span data-stu-id="c3012-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="c3012-2603">Todas as mensagens do protocolo de serviço de indexação de conteúdo têm um cabeçalho de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="c3012-2604">Veja abaixo um diagrama que mostra o formato de cabeçalho da mensagem do protocolo de serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="c3012-2605">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2605">0</span></span>

<span data-ttu-id="c3012-2606">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2606">1</span></span>

<span data-ttu-id="c3012-2607">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2607">2</span></span>

<span data-ttu-id="c3012-2608">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2608">3</span></span>

<span data-ttu-id="c3012-2609">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2609">4</span></span>

<span data-ttu-id="c3012-2610">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2610">5</span></span>

<span data-ttu-id="c3012-2611">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2611">6</span></span>

<span data-ttu-id="c3012-2612">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2612">7</span></span>

<span data-ttu-id="c3012-2613">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2613">8</span></span>

<span data-ttu-id="c3012-2614">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2614">9</span></span>

<span data-ttu-id="c3012-2615">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2615">1</span></span><br/> <span data-ttu-id="c3012-2616">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2616">0</span></span><br/>

<span data-ttu-id="c3012-2617">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2617">1</span></span>

<span data-ttu-id="c3012-2618">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2618">2</span></span>

<span data-ttu-id="c3012-2619">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2619">3</span></span>

<span data-ttu-id="c3012-2620">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2620">4</span></span>

<span data-ttu-id="c3012-2621">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2621">5</span></span>

<span data-ttu-id="c3012-2622">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2622">6</span></span>

<span data-ttu-id="c3012-2623">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2623">7</span></span>

<span data-ttu-id="c3012-2624">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2624">8</span></span>

<span data-ttu-id="c3012-2625">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2625">9</span></span>

<span data-ttu-id="c3012-2626">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2626">2</span></span><br/> <span data-ttu-id="c3012-2627">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2627">0</span></span><br/>

<span data-ttu-id="c3012-2628">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2628">1</span></span>

<span data-ttu-id="c3012-2629">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2629">2</span></span>

<span data-ttu-id="c3012-2630">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2630">3</span></span>

<span data-ttu-id="c3012-2631">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2631">4</span></span>

<span data-ttu-id="c3012-2632">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2632">5</span></span>

<span data-ttu-id="c3012-2633">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2633">6</span></span>

<span data-ttu-id="c3012-2634">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2634">7</span></span>

<span data-ttu-id="c3012-2635">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2635">8</span></span>

<span data-ttu-id="c3012-2636">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2636">9</span></span>

<span data-ttu-id="c3012-2637">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2637">3</span></span><br/> <span data-ttu-id="c3012-2638">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2638">0</span></span><br/>

<span data-ttu-id="c3012-2639">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2639">1</span></span>

<span data-ttu-id="c3012-2640">\_MSG</span><span class="sxs-lookup"><span data-stu-id="c3012-2640">\_msg</span></span>

<span data-ttu-id="c3012-2641">\_Estado</span><span class="sxs-lookup"><span data-stu-id="c3012-2641">\_status</span></span>

<span data-ttu-id="c3012-2642">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="c3012-2642">\_ulChecksum</span></span>

<span data-ttu-id="c3012-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="c3012-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="c3012-2644">\_**msg**: um inteiro de 32 bits que identifica o tipo de mensagem após o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="c3012-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="c3012-2645">A tabela a seguir lista as mensagens do protocolo de serviço de indexação de conteúdo e os valores inteiros especificados para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="c3012-2646">Conforme mostrado na tabela, alguns valores identificam 2 mensagens na tabela.</span><span class="sxs-lookup"><span data-stu-id="c3012-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="c3012-2647">Nessas instâncias, a mensagem após o cabeçalho pode ser identificada pela direção do fluxo de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3012-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="c3012-2648">Se a direção for cliente para servidor, a mensagem com "in" acrescentado ao nome da mensagem será indicada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="c3012-2649">Se a direção for servidor para cliente, a mensagem com "out" anexado ao nome da mensagem será indicada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="c3012-2650">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-2650">Value</span></span>      | <span data-ttu-id="c3012-2651">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="c3012-2652">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="c3012-2652">0x000000C8</span></span> | <span data-ttu-id="c3012-2653">CPMConnectIn ou CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="c3012-2654">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="c3012-2654">0x000000C9</span></span> | <span data-ttu-id="c3012-2655">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="c3012-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="c3012-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="c3012-2656">0x000000CA</span></span> | <span data-ttu-id="c3012-2657">CPMCreateQueryIn ou CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="c3012-2658">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="c3012-2658">0x000000CB</span></span> | <span data-ttu-id="c3012-2659">CPMFreeCursorIn ou CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="c3012-2660">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="c3012-2660">0x000000CC</span></span> | <span data-ttu-id="c3012-2661">CPMGetRowsIn ou CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="c3012-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="c3012-2662">0x000000CD</span></span> | <span data-ttu-id="c3012-2663">CPMRatioFinishedIn ou CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="c3012-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="c3012-2664">0x000000CE</span></span> | <span data-ttu-id="c3012-2665">CPMCompareBmkIn ou CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="c3012-2666">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="c3012-2666">0x000000CF</span></span> | <span data-ttu-id="c3012-2667">CPMGetApproximatePositionIn ou CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="c3012-2668">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="c3012-2668">0x000000D0</span></span> | <span data-ttu-id="c3012-2669">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="c3012-2670">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="c3012-2670">0x000000D1</span></span> | <span data-ttu-id="c3012-2671">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="c3012-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="c3012-2672">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="c3012-2672">0x000000D2</span></span> | <span data-ttu-id="c3012-2673">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="c3012-2674">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="c3012-2674">0x000000D7</span></span> | <span data-ttu-id="c3012-2675">CPMGetQueryStatusIn ou CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="c3012-2676">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="c3012-2676">0x000000D9</span></span> | <span data-ttu-id="c3012-2677">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="c3012-2678">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="c3012-2678">0x000000E1</span></span> | <span data-ttu-id="c3012-2679">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="c3012-2680">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="c3012-2680">0x000000E4</span></span> | <span data-ttu-id="c3012-2681">CPMFetchValueIn ou CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="c3012-2682">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="c3012-2682">0x000000E6</span></span> | <span data-ttu-id="c3012-2683">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="c3012-2684">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="c3012-2684">0x000000E7</span></span> | <span data-ttu-id="c3012-2685">CPMGetQueryStatusExIn ou PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="c3012-2686">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="c3012-2686">0x000000E8</span></span> | <span data-ttu-id="c3012-2687">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="c3012-2688">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="c3012-2688">0x000000E9</span></span> | <span data-ttu-id="c3012-2689">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="c3012-2690">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="c3012-2690">0x000000EC</span></span> | <span data-ttu-id="c3012-2691">CPMSetCatStateIn ou CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="c3012-2692">\_**status**: um HRESULT \[ MS-sys \] , que indica o status da operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="c3012-2693">*Comportamento do Windows: o cliente sempre define o \_ campo status como 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="c3012-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="c3012-2694">**\_ ulChecksum**: o \_ ulChecksum deve ser calculado conforme especificado na seção 3.2.4 para as seguintes mensagens:</span><span class="sxs-lookup"><span data-stu-id="c3012-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="c3012-2695">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="c3012-2696">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="c3012-2697">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="c3012-2698">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="c3012-2699">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="c3012-2700">Para todas as outras mensagens, \_ ULCHECKSUM deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="c3012-2701">Um cliente deve ignorar o \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="c3012-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="c3012-2702">**\_ ulReserved2**: deve ser definido como 0 e ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="c3012-2703">mensagens 2.2.3</span><span class="sxs-lookup"><span data-stu-id="c3012-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="c3012-2704">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="c3012-2705">A mensagem CPMCiStateInOut contém informações sobre o estado do serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="c3012-2706">O formato da mensagem CPMCiStateInOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-2707">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2707">0</span></span>

<span data-ttu-id="c3012-2708">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2708">1</span></span>

<span data-ttu-id="c3012-2709">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2709">2</span></span>

<span data-ttu-id="c3012-2710">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2710">3</span></span>

<span data-ttu-id="c3012-2711">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2711">4</span></span>

<span data-ttu-id="c3012-2712">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2712">5</span></span>

<span data-ttu-id="c3012-2713">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2713">6</span></span>

<span data-ttu-id="c3012-2714">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2714">7</span></span>

<span data-ttu-id="c3012-2715">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2715">8</span></span>

<span data-ttu-id="c3012-2716">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2716">9</span></span>

<span data-ttu-id="c3012-2717">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2717">1</span></span><br/> <span data-ttu-id="c3012-2718">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2718">0</span></span><br/>

<span data-ttu-id="c3012-2719">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2719">1</span></span>

<span data-ttu-id="c3012-2720">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2720">2</span></span>

<span data-ttu-id="c3012-2721">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2721">3</span></span>

<span data-ttu-id="c3012-2722">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2722">4</span></span>

<span data-ttu-id="c3012-2723">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2723">5</span></span>

<span data-ttu-id="c3012-2724">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2724">6</span></span>

<span data-ttu-id="c3012-2725">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2725">7</span></span>

<span data-ttu-id="c3012-2726">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2726">8</span></span>

<span data-ttu-id="c3012-2727">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2727">9</span></span>

<span data-ttu-id="c3012-2728">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2728">2</span></span><br/> <span data-ttu-id="c3012-2729">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2729">0</span></span><br/>

<span data-ttu-id="c3012-2730">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2730">1</span></span>

<span data-ttu-id="c3012-2731">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2731">2</span></span>

<span data-ttu-id="c3012-2732">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2732">3</span></span>

<span data-ttu-id="c3012-2733">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2733">4</span></span>

<span data-ttu-id="c3012-2734">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2734">5</span></span>

<span data-ttu-id="c3012-2735">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2735">6</span></span>

<span data-ttu-id="c3012-2736">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2736">7</span></span>

<span data-ttu-id="c3012-2737">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2737">8</span></span>

<span data-ttu-id="c3012-2738">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2738">9</span></span>

<span data-ttu-id="c3012-2739">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2739">3</span></span><br/> <span data-ttu-id="c3012-2740">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2740">0</span></span><br/>

<span data-ttu-id="c3012-2741">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2741">1</span></span>

<span data-ttu-id="c3012-2742">cbStruct</span><span class="sxs-lookup"><span data-stu-id="c3012-2742">cbStruct</span></span>

<span data-ttu-id="c3012-2743">cWordList</span><span class="sxs-lookup"><span data-stu-id="c3012-2743">cWordList</span></span>

<span data-ttu-id="c3012-2744">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="c3012-2744">cPersistentIndex</span></span>

<span data-ttu-id="c3012-2745">cQueries</span><span class="sxs-lookup"><span data-stu-id="c3012-2745">cQueries</span></span>

<span data-ttu-id="c3012-2746">cDocuments</span><span class="sxs-lookup"><span data-stu-id="c3012-2746">cDocuments</span></span>

<span data-ttu-id="c3012-2747">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="c3012-2747">cFreshTest</span></span>

<span data-ttu-id="c3012-2748">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="c3012-2748">dwMergeProgress</span></span>

<span data-ttu-id="c3012-2749">Imóveis</span><span class="sxs-lookup"><span data-stu-id="c3012-2749">eState</span></span>

<span data-ttu-id="c3012-2750">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="c3012-2750">cFilteredDocuments</span></span>

<span data-ttu-id="c3012-2751">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="c3012-2751">cTotalDocuments</span></span>

<span data-ttu-id="c3012-2752">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="c3012-2752">cPendingScans</span></span>

<span data-ttu-id="c3012-2753">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="c3012-2753">dwIndexSize</span></span>

<span data-ttu-id="c3012-2754">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="c3012-2754">cUniqueKeys</span></span>

<span data-ttu-id="c3012-2755">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="c3012-2755">cSecQDocuments</span></span>

<span data-ttu-id="c3012-2756">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="c3012-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="c3012-2757">**cbStruct**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3012-2758">O tamanho em bytes desta mensagem (excluindo o cabeçalho comum).</span><span class="sxs-lookup"><span data-stu-id="c3012-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="c3012-2759">DEVE ser definido como 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="c3012-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="c3012-2760">**cWordList**: um inteiro de 32 bits sem sinal indicando a contagem de índices iniciais criados para documentos indexados recentemente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="c3012-2761">**cPersistentIndex**: um inteiro de 32 bits sem sinal indicando a contagem de índices persistentes.</span><span class="sxs-lookup"><span data-stu-id="c3012-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="c3012-2762">**cQueries**: um inteiro de 32 bits sem sinal indicando um número de consultas em execução ativamente.</span><span class="sxs-lookup"><span data-stu-id="c3012-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="c3012-2763">**cDocuments**: um inteiro de 32 bits sem sinal indicando o número total de documentos aguardando para serem indexados.</span><span class="sxs-lookup"><span data-stu-id="c3012-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="c3012-2764">**cFreshTest**: um inteiro sem sinal de 32 bits que indica o número de documentos exclusivos com informações em índices que não são totalmente otimizados para desempenho.</span><span class="sxs-lookup"><span data-stu-id="c3012-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="c3012-2765">**dwMergeProgress**: inteiro de 32 bits sem sinal especificando a porcentagem de conclusão da otimização total atual de índices, se a otimização estiver em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="c3012-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="c3012-2766">DEVE ser menor ou igual a 100.</span><span class="sxs-lookup"><span data-stu-id="c3012-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="c3012-2767">**imobiliária**: estado da indexação de conteúdo, conforme fornecido por uma ou mais das \_ constantes de estado de CI \_ \* , definidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3012-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="c3012-2768">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-2768">Value</span></span>                                         | <span data-ttu-id="c3012-2769">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-2770">\_Mesclagem de sombra de estado de CI \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="c3012-2771">O serviço de indexação está no processo de otimização de alguns dos índices para reduzir o uso de memória e melhorar o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="c3012-2772">\_ \_ Mesclagem mestra de estado CI \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="c3012-2773">O serviço de indexação está no processo de Otimização total para todos os índices.</span><span class="sxs-lookup"><span data-stu-id="c3012-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c3012-2774">\_Exame de conteúdo de estado CI \_ \_ \_ necessário 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="c3012-2775">Alguns documentos no índice foram alterados e o serviço de indexação precisa determinar quais foram adicionados, alterados ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="c3012-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c3012-2776">CI \_ estado \_ recozimento \_ mesclar 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3012-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="c3012-2777">O serviço de indexação está no processo de otimização de índices para reduzir o uso de memória e melhorar o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="c3012-2778">Esse processo é mais abrangente do que aquele identificado pelo valor de \_ mesclagem de sombra de estado de CI \_ \_ , mas não é tão abrangente quanto o especificado pelo \_ valor de \_ mesclagem mestre de estado CI \_ .</span><span class="sxs-lookup"><span data-stu-id="c3012-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="c3012-2779">Essas otimizações são específicas da implementação, pois dependem da maneira como os dados são armazenados internamente; as otimizações não afetam o protocolo de nenhuma forma que não seja o tempo de resposta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="c3012-2780">\_Verificação de estado CI \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3012-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="c3012-2781">O serviço de indexação está examinando um diretório ou um conjunto de diretórios para ver se algum arquivo foi adicionado, excluído ou atualizado desde a última vez em que o diretório foi indexado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c3012-2782">O \_ estado de CI \_ recuperando 0x00000020</span><span class="sxs-lookup"><span data-stu-id="c3012-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="c3012-2783">O serviço está sendo iniciado a partir do último estado salvo e está no processo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c3012-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c3012-2784">\_0x00000080 de \_ memória insuficiente do estado de CI \_</span><span class="sxs-lookup"><span data-stu-id="c3012-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="c3012-2785">A maior parte da memória virtual do servidor está em uso.</span><span class="sxs-lookup"><span data-stu-id="c3012-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c3012-2786">Estado de CI de \_ \_ alta \_ e/s 0x00000100</span><span class="sxs-lookup"><span data-stu-id="c3012-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="c3012-2787">O nível de atividade de entrada/saída (e/s) no servidor é relativamente alto.</span><span class="sxs-lookup"><span data-stu-id="c3012-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="c3012-2788">\_Mesclagem mestra de estado CI em \_ \_ \_ pausa 0x00000200</span><span class="sxs-lookup"><span data-stu-id="c3012-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="c3012-2789">O processo de otimização completa de todos os índices que estavam em andamento foi pausado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="c3012-2790">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c3012-2791">\_ \_ 0x00000400 somente leitura do estado CI \_</span><span class="sxs-lookup"><span data-stu-id="c3012-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="c3012-2792">A parte do serviço de indexação que obtém novos documentos para o índice foi pausada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="c3012-2793">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c3012-2794">Estado de CI de \_ \_ energia da bateria \_ 0x00000800</span><span class="sxs-lookup"><span data-stu-id="c3012-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="c3012-2795">A parte do serviço de indexação que obtém novos documentos para o índice foi pausada para conservar o tempo de vida da bateria, mas ainda responde às consultas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="c3012-2796">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c3012-2797">0x00001000 de usuário de estado de CI \_ \_ \_ ativo</span><span class="sxs-lookup"><span data-stu-id="c3012-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="c3012-2798">A parte do serviço de indexação que obtém novos documentos para o índice foi pausada devido à alta atividade pelo usuário (teclado ou mouse), mas ainda responde às consultas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="c3012-2799">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="c3012-2800">Estado de CI \_ \_ iniciando 0x00002000</span><span class="sxs-lookup"><span data-stu-id="c3012-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="c3012-2801">O serviço está iniciando.</span><span class="sxs-lookup"><span data-stu-id="c3012-2801">The service is starting.</span></span> <span data-ttu-id="c3012-2802">As consultas podem ser executadas, mas a verificação e a notificação ainda não foram habilitadas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="c3012-2803">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c3012-2804">\_Estado CI \_ lendo \_ USNs 0x00004000</span><span class="sxs-lookup"><span data-stu-id="c3012-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="c3012-2805">O serviço não leu o log mantido pelo sistema de arquivos para manter o controle das alterações em arquivos ou diretórios em um volume, de modo que o índice pode não estar atualizado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="c3012-2806">**cFilteredDocuments**: um inteiro de 32 bits sem sinal indicando o número de documentos indexados desde que a indexação de conteúdo foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="c3012-2807">**cTotalDocuments**: um inteiro de 32 bits sem sinal indicando o número total de documentos no sistema.</span><span class="sxs-lookup"><span data-stu-id="c3012-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="c3012-2808">**cPendingScans**: um inteiro de 32 bits sem sinal indicando o número de operações pendentes de indexação de alto nível.</span><span class="sxs-lookup"><span data-stu-id="c3012-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="c3012-2809">O significado desse valor é específico do provedor, mas números maiores são esperados para indicar que mais indexação permanece.</span><span class="sxs-lookup"><span data-stu-id="c3012-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="c3012-2810">*Comportamento do Windows*: esse valor geralmente é zero, exceto imediatamente após a indexação ter sido iniciada ou após o estouro de uma fila de notificação.</span><span class="sxs-lookup"><span data-stu-id="c3012-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="c3012-2811">**dwIndexSize**: um inteiro de 32 bits sem sinal indicando o tamanho, em megabytes, do índice (excluindo o cache de propriedades).</span><span class="sxs-lookup"><span data-stu-id="c3012-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="c3012-2812">**cUniqueKeys**: um inteiro de 32 bits sem sinal indicando o número aproximado de chaves exclusivas no catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="c3012-2813">**cSecQDocuments**: um inteiro de 32 bits sem sinal indicando o número de documentos que o serviço de indexação tentará indexar devido a uma falha durante a tentativa de indexação inicial.</span><span class="sxs-lookup"><span data-stu-id="c3012-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="c3012-2814">**dwPropCacheSize**: um inteiro de 32 bits sem sinal indicando o tamanho, em megabytes, do cache de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="c3012-2815">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="c3012-2816">A mensagem CPMSetCatStateIn define o estado de um catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="c3012-2817">O formato da mensagem CPMSetCatStateIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-2818">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2818">0</span></span>

<span data-ttu-id="c3012-2819">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2819">1</span></span>

<span data-ttu-id="c3012-2820">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2820">2</span></span>

<span data-ttu-id="c3012-2821">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2821">3</span></span>

<span data-ttu-id="c3012-2822">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2822">4</span></span>

<span data-ttu-id="c3012-2823">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2823">5</span></span>

<span data-ttu-id="c3012-2824">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2824">6</span></span>

<span data-ttu-id="c3012-2825">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2825">7</span></span>

<span data-ttu-id="c3012-2826">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2826">8</span></span>

<span data-ttu-id="c3012-2827">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2827">9</span></span>

<span data-ttu-id="c3012-2828">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2828">1</span></span><br/> <span data-ttu-id="c3012-2829">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2829">0</span></span><br/>

<span data-ttu-id="c3012-2830">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2830">1</span></span>

<span data-ttu-id="c3012-2831">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2831">2</span></span>

<span data-ttu-id="c3012-2832">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2832">3</span></span>

<span data-ttu-id="c3012-2833">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2833">4</span></span>

<span data-ttu-id="c3012-2834">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2834">5</span></span>

<span data-ttu-id="c3012-2835">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2835">6</span></span>

<span data-ttu-id="c3012-2836">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2836">7</span></span>

<span data-ttu-id="c3012-2837">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2837">8</span></span>

<span data-ttu-id="c3012-2838">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2838">9</span></span>

<span data-ttu-id="c3012-2839">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2839">2</span></span><br/> <span data-ttu-id="c3012-2840">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2840">0</span></span><br/>

<span data-ttu-id="c3012-2841">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2841">1</span></span>

<span data-ttu-id="c3012-2842">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2842">2</span></span>

<span data-ttu-id="c3012-2843">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2843">3</span></span>

<span data-ttu-id="c3012-2844">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2844">4</span></span>

<span data-ttu-id="c3012-2845">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2845">5</span></span>

<span data-ttu-id="c3012-2846">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2846">6</span></span>

<span data-ttu-id="c3012-2847">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2847">7</span></span>

<span data-ttu-id="c3012-2848">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2848">8</span></span>

<span data-ttu-id="c3012-2849">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2849">9</span></span>

<span data-ttu-id="c3012-2850">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2850">3</span></span><br/> <span data-ttu-id="c3012-2851">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2851">0</span></span><br/>

<span data-ttu-id="c3012-2852">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2852">1</span></span>

<span data-ttu-id="c3012-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="c3012-2853">\_partID</span></span>

<span data-ttu-id="c3012-2854">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="c3012-2854">\_dwNewState</span></span>

<span data-ttu-id="c3012-2855">\_CatName (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="c3012-2856">**\_ partid**: deve ser definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="c3012-2857">**\_ dwNewState**: deve ser definido como um dos valores a seguir, indicando o novo estado do catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="c3012-2858">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-2858">Value</span></span>                         | <span data-ttu-id="c3012-2859">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-2860">CICAT \_ parou 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="c3012-2861">O catálogo está parado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2861">The catalog is stopped.</span></span> <span data-ttu-id="c3012-2862">Esse Estado significa que nenhum arquivo novo deve ser indexado e nenhuma consulta de pesquisa será processada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="c3012-2863">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="c3012-2864">O catálogo é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c3012-2864">The catalog is read-only.</span></span> <span data-ttu-id="c3012-2865">Nenhum arquivo novo deve ser indexado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="c3012-2866">CICAT \_ gravável 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="c3012-2867">O catálogo é gravável.</span><span class="sxs-lookup"><span data-stu-id="c3012-2867">The catalog is writable.</span></span> <span data-ttu-id="c3012-2868">Novos arquivos podem ser indexados e consultas de pesquisa devem ser processadas.</span><span class="sxs-lookup"><span data-stu-id="c3012-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="c3012-2869">CICAT \_ sem \_ 0x00000008 de consulta</span><span class="sxs-lookup"><span data-stu-id="c3012-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="c3012-2870">O catálogo não está disponível para consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="c3012-2871">CICAT \_ obter \_ estado 0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3012-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="c3012-2872">O estado do catálogo não deve ser alterado, somente recuperado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="c3012-2873">CICAT \_ tudo \_ aberto 0x00000020</span><span class="sxs-lookup"><span data-stu-id="c3012-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="c3012-2874">Uma verificação para ver se todos os catálogos foram iniciados.</span><span class="sxs-lookup"><span data-stu-id="c3012-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="c3012-2875">Nesse caso, o \_ campo dwOldState enviado na resposta CPMSetCatStateOut a essa mensagem será relatado como diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c3012-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="c3012-2876">**\_ CatName**: o nome do catálogo que deve ter seu estado modificado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="c3012-2877">O nome deve ser uma cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="c3012-2878">Esse campo deve ser omitido se \_ dwNewState for definido como CICAT \_ tudo \_ aberto.</span><span class="sxs-lookup"><span data-stu-id="c3012-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="c3012-2879">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="c3012-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="c3012-2880">A mensagem CPMSetCatStateOut é uma resposta a uma mensagem CPMSetCatStateIn com o estado antigo do catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="c3012-2881">O formato da mensagem CPMSetCatStateOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-2882">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2882">0</span></span>

<span data-ttu-id="c3012-2883">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2883">1</span></span>

<span data-ttu-id="c3012-2884">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2884">2</span></span>

<span data-ttu-id="c3012-2885">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2885">3</span></span>

<span data-ttu-id="c3012-2886">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2886">4</span></span>

<span data-ttu-id="c3012-2887">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2887">5</span></span>

<span data-ttu-id="c3012-2888">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2888">6</span></span>

<span data-ttu-id="c3012-2889">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2889">7</span></span>

<span data-ttu-id="c3012-2890">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2890">8</span></span>

<span data-ttu-id="c3012-2891">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2891">9</span></span>

<span data-ttu-id="c3012-2892">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2892">1</span></span><br/> <span data-ttu-id="c3012-2893">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2893">0</span></span><br/>

<span data-ttu-id="c3012-2894">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2894">1</span></span>

<span data-ttu-id="c3012-2895">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2895">2</span></span>

<span data-ttu-id="c3012-2896">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2896">3</span></span>

<span data-ttu-id="c3012-2897">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2897">4</span></span>

<span data-ttu-id="c3012-2898">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2898">5</span></span>

<span data-ttu-id="c3012-2899">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2899">6</span></span>

<span data-ttu-id="c3012-2900">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2900">7</span></span>

<span data-ttu-id="c3012-2901">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2901">8</span></span>

<span data-ttu-id="c3012-2902">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2902">9</span></span>

<span data-ttu-id="c3012-2903">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2903">2</span></span><br/> <span data-ttu-id="c3012-2904">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2904">0</span></span><br/>

<span data-ttu-id="c3012-2905">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2905">1</span></span>

<span data-ttu-id="c3012-2906">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2906">2</span></span>

<span data-ttu-id="c3012-2907">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2907">3</span></span>

<span data-ttu-id="c3012-2908">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2908">4</span></span>

<span data-ttu-id="c3012-2909">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2909">5</span></span>

<span data-ttu-id="c3012-2910">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2910">6</span></span>

<span data-ttu-id="c3012-2911">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2911">7</span></span>

<span data-ttu-id="c3012-2912">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2912">8</span></span>

<span data-ttu-id="c3012-2913">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2913">9</span></span>

<span data-ttu-id="c3012-2914">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2914">3</span></span><br/> <span data-ttu-id="c3012-2915">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2915">0</span></span><br/>

<span data-ttu-id="c3012-2916">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2916">1</span></span>

<span data-ttu-id="c3012-2917">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="c3012-2917">\_dwOldState</span></span>



 

<span data-ttu-id="c3012-2918">**\_ dwOldState**: um dos valores a seguir, indicando o estado antigo do catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="c3012-2919">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-2919">Value</span></span>                       | <span data-ttu-id="c3012-2920">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="c3012-2921">CICAT \_ parou 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="c3012-2922">O catálogo está parado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="c3012-2923">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="c3012-2924">O catálogo é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c3012-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="c3012-2925">CICAT \_ gravável 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="c3012-2926">O catálogo é gravável.</span><span class="sxs-lookup"><span data-stu-id="c3012-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="c3012-2927">CICAT \_ sem \_ 0x00000008 de consulta</span><span class="sxs-lookup"><span data-stu-id="c3012-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="c3012-2928">O catálogo não está disponível para consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="c3012-2929">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="c3012-2930">A mensagem CPMUpdateDocumentsIn direciona o servidor para indexar o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="c3012-2931">O servidor responderá com o cabeçalho da mensagem CPMUpdateDocumentsOut, com os resultados da solicitação contida no \_ campo status do cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="c3012-2932">O formato da mensagem CPMUpdateDocumentsIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-2933">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2933">0</span></span>

<span data-ttu-id="c3012-2934">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2934">1</span></span>

<span data-ttu-id="c3012-2935">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2935">2</span></span>

<span data-ttu-id="c3012-2936">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2936">3</span></span>

<span data-ttu-id="c3012-2937">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2937">4</span></span>

<span data-ttu-id="c3012-2938">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2938">5</span></span>

<span data-ttu-id="c3012-2939">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2939">6</span></span>

<span data-ttu-id="c3012-2940">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2940">7</span></span>

<span data-ttu-id="c3012-2941">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2941">8</span></span>

<span data-ttu-id="c3012-2942">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2942">9</span></span>

<span data-ttu-id="c3012-2943">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2943">1</span></span><br/> <span data-ttu-id="c3012-2944">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2944">0</span></span><br/>

<span data-ttu-id="c3012-2945">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2945">1</span></span>

<span data-ttu-id="c3012-2946">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2946">2</span></span>

<span data-ttu-id="c3012-2947">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2947">3</span></span>

<span data-ttu-id="c3012-2948">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2948">4</span></span>

<span data-ttu-id="c3012-2949">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2949">5</span></span>

<span data-ttu-id="c3012-2950">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2950">6</span></span>

<span data-ttu-id="c3012-2951">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2951">7</span></span>

<span data-ttu-id="c3012-2952">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2952">8</span></span>

<span data-ttu-id="c3012-2953">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2953">9</span></span>

<span data-ttu-id="c3012-2954">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2954">2</span></span><br/> <span data-ttu-id="c3012-2955">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2955">0</span></span><br/>

<span data-ttu-id="c3012-2956">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2956">1</span></span>

<span data-ttu-id="c3012-2957">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2957">2</span></span>

<span data-ttu-id="c3012-2958">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2958">3</span></span>

<span data-ttu-id="c3012-2959">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2959">4</span></span>

<span data-ttu-id="c3012-2960">5</span><span class="sxs-lookup"><span data-stu-id="c3012-2960">5</span></span>

<span data-ttu-id="c3012-2961">6</span><span class="sxs-lookup"><span data-stu-id="c3012-2961">6</span></span>

<span data-ttu-id="c3012-2962">7</span><span class="sxs-lookup"><span data-stu-id="c3012-2962">7</span></span>

<span data-ttu-id="c3012-2963">8</span><span class="sxs-lookup"><span data-stu-id="c3012-2963">8</span></span>

<span data-ttu-id="c3012-2964">9</span><span class="sxs-lookup"><span data-stu-id="c3012-2964">9</span></span>

<span data-ttu-id="c3012-2965">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2965">3</span></span><br/> <span data-ttu-id="c3012-2966">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2966">0</span></span><br/>

<span data-ttu-id="c3012-2967">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2967">1</span></span>

<span data-ttu-id="c3012-2968">\_sinalizador (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2968">\_flag (optional)</span></span>

<span data-ttu-id="c3012-2969">\_fRootPath (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="c3012-2970">RootPath (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="c3012-2971">**\_ sinalizador**: o tipo de atualização a ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="c3012-2972">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3012-2973">Esse campo deve ser definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c3012-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="c3012-2974">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-2974">Value</span></span>                  | <span data-ttu-id="c3012-2975">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c3012-2976">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="c3012-2977">Uma atualização incremental deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="c3012-2978">UPD \_ completo 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="c3012-2979">Uma atualização completa deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="c3012-2980">UPD \_ init 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="c3012-2981">Uma nova inicialização deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="c3012-2982">**\_ fRootPath**: um valor booliano que indica se o campo RootPath especifica um caminho no qual executar a atualização.</span><span class="sxs-lookup"><span data-stu-id="c3012-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="c3012-2983">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3012-2984">Esse campo deve ser definido como 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="c3012-2985">Se definido como 0x00000001, um caminho no qual executar a atualização será incluído em RootPath.</span><span class="sxs-lookup"><span data-stu-id="c3012-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="c3012-2986">Se definido como 0x00000000, a atualização será executada em todos os caminhos indexados.</span><span class="sxs-lookup"><span data-stu-id="c3012-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="c3012-2987">**RootPath**: o nome do caminho a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c3012-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="c3012-2988">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3012-2989">O nome deve ser uma cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="c3012-2990">Esse campo deve ser omitido se \_ fRootPath for definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="c3012-2991">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="c3012-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="c3012-2992">A mensagem CPMForceMergeIn solicita que um servidor execute qualquer manutenção necessária para melhorar o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="c3012-2993">O servidor responderá com o cabeçalho da mensagem CPMForceMergeIn, com os resultados da solicitação contida no \_ campo status.</span><span class="sxs-lookup"><span data-stu-id="c3012-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="c3012-2994">O formato da mensagem CPMForceMergeIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-2995">0</span><span class="sxs-lookup"><span data-stu-id="c3012-2995">0</span></span>

<span data-ttu-id="c3012-2996">1</span><span class="sxs-lookup"><span data-stu-id="c3012-2996">1</span></span>

<span data-ttu-id="c3012-2997">2</span><span class="sxs-lookup"><span data-stu-id="c3012-2997">2</span></span>

<span data-ttu-id="c3012-2998">3</span><span class="sxs-lookup"><span data-stu-id="c3012-2998">3</span></span>

<span data-ttu-id="c3012-2999">4</span><span class="sxs-lookup"><span data-stu-id="c3012-2999">4</span></span>

<span data-ttu-id="c3012-3000">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3000">5</span></span>

<span data-ttu-id="c3012-3001">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3001">6</span></span>

<span data-ttu-id="c3012-3002">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3002">7</span></span>

<span data-ttu-id="c3012-3003">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3003">8</span></span>

<span data-ttu-id="c3012-3004">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3004">9</span></span>

<span data-ttu-id="c3012-3005">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3005">1</span></span><br/> <span data-ttu-id="c3012-3006">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3006">0</span></span><br/>

<span data-ttu-id="c3012-3007">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3007">1</span></span>

<span data-ttu-id="c3012-3008">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3008">2</span></span>

<span data-ttu-id="c3012-3009">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3009">3</span></span>

<span data-ttu-id="c3012-3010">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3010">4</span></span>

<span data-ttu-id="c3012-3011">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3011">5</span></span>

<span data-ttu-id="c3012-3012">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3012">6</span></span>

<span data-ttu-id="c3012-3013">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3013">7</span></span>

<span data-ttu-id="c3012-3014">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3014">8</span></span>

<span data-ttu-id="c3012-3015">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3015">9</span></span>

<span data-ttu-id="c3012-3016">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3016">2</span></span><br/> <span data-ttu-id="c3012-3017">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3017">0</span></span><br/>

<span data-ttu-id="c3012-3018">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3018">1</span></span>

<span data-ttu-id="c3012-3019">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3019">2</span></span>

<span data-ttu-id="c3012-3020">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3020">3</span></span>

<span data-ttu-id="c3012-3021">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3021">4</span></span>

<span data-ttu-id="c3012-3022">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3022">5</span></span>

<span data-ttu-id="c3012-3023">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3023">6</span></span>

<span data-ttu-id="c3012-3024">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3024">7</span></span>

<span data-ttu-id="c3012-3025">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3025">8</span></span>

<span data-ttu-id="c3012-3026">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3026">9</span></span>

<span data-ttu-id="c3012-3027">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3027">3</span></span><br/> <span data-ttu-id="c3012-3028">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3028">0</span></span><br/>

<span data-ttu-id="c3012-3029">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3029">1</span></span>

<span data-ttu-id="c3012-3030">\_partid (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="c3012-3031">**\_ partid**: esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3012-3032">Quando esse campo estiver presente, ele deverá ser definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="c3012-3033">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="c3012-3034">A mensagem CPMConnectIn inicia uma sessão entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="c3012-3035">O formato da mensagem CPMConnectIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-3036">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3036">0</span></span>

<span data-ttu-id="c3012-3037">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3037">1</span></span>

<span data-ttu-id="c3012-3038">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3038">2</span></span>

<span data-ttu-id="c3012-3039">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3039">3</span></span>

<span data-ttu-id="c3012-3040">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3040">4</span></span>

<span data-ttu-id="c3012-3041">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3041">5</span></span>

<span data-ttu-id="c3012-3042">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3042">6</span></span>

<span data-ttu-id="c3012-3043">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3043">7</span></span>

<span data-ttu-id="c3012-3044">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3044">8</span></span>

<span data-ttu-id="c3012-3045">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3045">9</span></span>

<span data-ttu-id="c3012-3046">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3046">1</span></span><br/> <span data-ttu-id="c3012-3047">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3047">0</span></span><br/>

<span data-ttu-id="c3012-3048">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3048">1</span></span>

<span data-ttu-id="c3012-3049">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3049">2</span></span>

<span data-ttu-id="c3012-3050">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3050">3</span></span>

<span data-ttu-id="c3012-3051">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3051">4</span></span>

<span data-ttu-id="c3012-3052">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3052">5</span></span>

<span data-ttu-id="c3012-3053">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3053">6</span></span>

<span data-ttu-id="c3012-3054">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3054">7</span></span>

<span data-ttu-id="c3012-3055">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3055">8</span></span>

<span data-ttu-id="c3012-3056">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3056">9</span></span>

<span data-ttu-id="c3012-3057">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3057">2</span></span><br/> <span data-ttu-id="c3012-3058">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3058">0</span></span><br/>

<span data-ttu-id="c3012-3059">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3059">1</span></span>

<span data-ttu-id="c3012-3060">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3060">2</span></span>

<span data-ttu-id="c3012-3061">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3061">3</span></span>

<span data-ttu-id="c3012-3062">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3062">4</span></span>

<span data-ttu-id="c3012-3063">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3063">5</span></span>

<span data-ttu-id="c3012-3064">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3064">6</span></span>

<span data-ttu-id="c3012-3065">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3065">7</span></span>

<span data-ttu-id="c3012-3066">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3066">8</span></span>

<span data-ttu-id="c3012-3067">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3067">9</span></span>

<span data-ttu-id="c3012-3068">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3068">3</span></span><br/> <span data-ttu-id="c3012-3069">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3069">0</span></span><br/>

<span data-ttu-id="c3012-3070">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3070">1</span></span>

<span data-ttu-id="c3012-3071">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="c3012-3071">\_iClientVersion</span></span>

<span data-ttu-id="c3012-3072">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="c3012-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="c3012-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="c3012-3073">\_cbBlob1</span></span>

<span data-ttu-id="c3012-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="c3012-3074">\_cbBlob2</span></span>

<span data-ttu-id="c3012-3075">\_margem</span><span class="sxs-lookup"><span data-stu-id="c3012-3075">\_padding</span></span>

<span data-ttu-id="c3012-3076">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3076">...</span></span>

<span data-ttu-id="c3012-3077">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3077">...</span></span>

<span data-ttu-id="c3012-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="c3012-3078">MachineName</span></span>

<span data-ttu-id="c3012-3079">... Ela</span><span class="sxs-lookup"><span data-stu-id="c3012-3079">... (variable)</span></span>

<span data-ttu-id="c3012-3080">UserName</span><span class="sxs-lookup"><span data-stu-id="c3012-3080">UserName</span></span>

<span data-ttu-id="c3012-3081">... Ela</span><span class="sxs-lookup"><span data-stu-id="c3012-3081">... (variable)</span></span>

<span data-ttu-id="c3012-3082">\_paddingcPropSets (opcional, variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="c3012-3083">cPropSets</span><span class="sxs-lookup"><span data-stu-id="c3012-3083">cPropSets</span></span>

<span data-ttu-id="c3012-3084">PropertySet1 (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="c3012-3085">PropertySet2 (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="c3012-3086">\_paddingExtPropset (opcional, variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="c3012-3087">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="c3012-3087">cExtPropSet</span></span>

<span data-ttu-id="c3012-3088">aPropertySets (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="c3012-3089">**\_ iClientVersion**: um inteiro de 32 bits que indica se o servidor deve validar o valor de soma de verificação especificado no \_ campo ulChecksum dos cabeçalhos de mensagem para as mensagens enviadas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="c3012-3090">Se o \_ campo iClientVersion for definido como 0x00000008 ou superior, o servidor deverá validar o \_ valor do campo ulChecksum para as seguintes mensagens:</span><span class="sxs-lookup"><span data-stu-id="c3012-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="c3012-3091">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="c3012-3092">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="c3012-3093">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="c3012-3094">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="c3012-3095">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="c3012-3096">Para obter detalhes sobre como o servidor valida o valor especificado pelo cliente no campo ulChecksum para as mensagens listadas acima, consulte a seção 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="c3012-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="c3012-3097">Se o valor for maior que 0x00000008, o cliente será considerado capaz de manipular deslocamentos de 64 bits em mensagens CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="c3012-3098">Consulte a seção 2.2.3.16 para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="c3012-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="c3012-3099">*Comportamento do Windows: em clientes Windows, o iClientVersion é definido da seguinte maneira*:</span><span class="sxs-lookup"><span data-stu-id="c3012-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="c3012-3100">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-3100">Value</span></span>      | <span data-ttu-id="c3012-3101">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="c3012-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3012-3102">0x00000005</span></span> | <span data-ttu-id="c3012-3103">O sistema operacional do cliente é o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c3012-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="c3012-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3012-3104">0x00000008</span></span> | <span data-ttu-id="c3012-3105">O sistema operacional do cliente é o Windows XP de 32 bits ou o Windows Server 2003 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="c3012-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="c3012-3106">0x00010008</span></span> | <span data-ttu-id="c3012-3107">O sistema operacional do cliente é o Windows XP de 64 bits ou o Windows Server 2003 de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="c3012-3108">\_**fClientIsRemote**: um valor booliano que indica se o cliente está sendo executado em um computador diferente do servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="c3012-3109">DEVE ser definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="c3012-3110">\_**cbBlob1**: um inteiro de 32 bits sem sinal indicando o tamanho em bytes dos campos CPropSet, PropertySet1 e PropertySet2, combinados.</span><span class="sxs-lookup"><span data-stu-id="c3012-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="c3012-3111">\_**cbBlob2**: um inteiro de 32 bits sem sinal indicando o tamanho em bytes dos campos CExPropSet e aPropertySet, combinados.</span><span class="sxs-lookup"><span data-stu-id="c3012-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="c3012-3112">\_**preenchimento**: 12 bytes de preenchimento que podem conter valores arbitrários e devem ser ignorados.</span><span class="sxs-lookup"><span data-stu-id="c3012-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="c3012-3113">**MachineName**: o nome do computador do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="c3012-3114">A cadeia de caracteres de nome deve ser uma matriz com terminação nula de menos de 512 caracteres Unicode, incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="c3012-3115">**Username**: uma cadeia de caracteres que representa o nome de usuário da pessoa que está executando o aplicativo que invocou esse protocolo.</span><span class="sxs-lookup"><span data-stu-id="c3012-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="c3012-3116">A cadeia de caracteres de nome deve ser uma matriz com terminação nula de menos de 512 caracteres Unicode quando concatenada com MachineName.</span><span class="sxs-lookup"><span data-stu-id="c3012-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="c3012-3117">**\_ paddingcPropSets**: esse campo deve ter de 0 a 7 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="c3012-3118">O número de bytes deve ser o número necessário para fazer o deslocamento de bytes do campo cPropSets do início da mensagem que contém essa estrutura ser um múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="c3012-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="c3012-3119">O valor dos bytes pode ser qualquer valor arbitrário e deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-3120">**cPropSets**: um inteiro de 32 bits sem sinal indicando o número de estruturas CDbPropSet após este campo.</span><span class="sxs-lookup"><span data-stu-id="c3012-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="c3012-3121">Esse valor deve ser definido como 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="c3012-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="c3012-3122">**PropertySet1**: uma estrutura CDbPropSet com guidPropertySet que contém DBPROPSET \_ FSCIFRMWRK \_ ext (consulte A seção 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="c3012-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="c3012-3123">**PropertySet2**: uma estrutura CDbPropSet com guidPropertySet que contém DBPROPSET \_ CIFRMWRKCORE \_ ext (consulte A seção 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="c3012-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="c3012-3124">\_**PaddingExtPropset**: esse campo deve ter de 0 a 7 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="c3012-3125">O número de bytes deve ser o número necessário para fazer o deslocamento de bytes do campo cExtPropSets do início da mensagem que contém essa estrutura ser um múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="c3012-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="c3012-3126">O valor dos bytes pode ser qualquer valor arbitrário e deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-3127">**cExtPropSet**: um inteiro de 32 bits sem sinal indicando o número de estruturas CDbPropSet após este campo.</span><span class="sxs-lookup"><span data-stu-id="c3012-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="c3012-3128">**aPropertySets**: uma matriz de estruturas CDbPropSet especificando outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3012-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="c3012-3129">O número de elementos nesta matriz deve ser igual a cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="c3012-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="c3012-3130">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="c3012-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="c3012-3131">A mensagem CPMConnectOut contém uma resposta a uma mensagem CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="c3012-3132">O formato da mensagem CPMConnectOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-3133">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3133">0</span></span>

<span data-ttu-id="c3012-3134">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3134">1</span></span>

<span data-ttu-id="c3012-3135">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3135">2</span></span>

<span data-ttu-id="c3012-3136">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3136">3</span></span>

<span data-ttu-id="c3012-3137">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3137">4</span></span>

<span data-ttu-id="c3012-3138">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3138">5</span></span>

<span data-ttu-id="c3012-3139">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3139">6</span></span>

<span data-ttu-id="c3012-3140">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3140">7</span></span>

<span data-ttu-id="c3012-3141">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3141">8</span></span>

<span data-ttu-id="c3012-3142">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3142">9</span></span>

<span data-ttu-id="c3012-3143">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3143">1</span></span><br/> <span data-ttu-id="c3012-3144">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3144">0</span></span><br/>

<span data-ttu-id="c3012-3145">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3145">1</span></span>

<span data-ttu-id="c3012-3146">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3146">2</span></span>

<span data-ttu-id="c3012-3147">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3147">3</span></span>

<span data-ttu-id="c3012-3148">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3148">4</span></span>

<span data-ttu-id="c3012-3149">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3149">5</span></span>

<span data-ttu-id="c3012-3150">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3150">6</span></span>

<span data-ttu-id="c3012-3151">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3151">7</span></span>

<span data-ttu-id="c3012-3152">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3152">8</span></span>

<span data-ttu-id="c3012-3153">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3153">9</span></span>

<span data-ttu-id="c3012-3154">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3154">2</span></span><br/> <span data-ttu-id="c3012-3155">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3155">0</span></span><br/>

<span data-ttu-id="c3012-3156">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3156">1</span></span>

<span data-ttu-id="c3012-3157">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3157">2</span></span>

<span data-ttu-id="c3012-3158">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3158">3</span></span>

<span data-ttu-id="c3012-3159">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3159">4</span></span>

<span data-ttu-id="c3012-3160">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3160">5</span></span>

<span data-ttu-id="c3012-3161">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3161">6</span></span>

<span data-ttu-id="c3012-3162">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3162">7</span></span>

<span data-ttu-id="c3012-3163">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3163">8</span></span>

<span data-ttu-id="c3012-3164">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3164">9</span></span>

<span data-ttu-id="c3012-3165">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3165">3</span></span><br/> <span data-ttu-id="c3012-3166">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3166">0</span></span><br/>

<span data-ttu-id="c3012-3167">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3167">1</span></span>

<span data-ttu-id="c3012-3168">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="c3012-3168">\_serverVersion</span></span>

<span data-ttu-id="c3012-3169">\_reservado (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="c3012-3170">**\_ serverVersion**:</span><span class="sxs-lookup"><span data-stu-id="c3012-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="c3012-3171">Um inteiro de 32 bits, indicando se o servidor pode dar suporte a deslocamentos de 64 bits *.*</span><span class="sxs-lookup"><span data-stu-id="c3012-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="c3012-3172">Consulte a seção 2.2.3.16 para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="c3012-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="c3012-3173">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-3173">Value</span></span>      | <span data-ttu-id="c3012-3174">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="c3012-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3012-3175">0x00000007</span></span> | <span data-ttu-id="c3012-3176">O servidor só pode enviar deslocamentos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="c3012-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="c3012-3177">0x00010007</span></span> | <span data-ttu-id="c3012-3178">O servidor pode enviar deslocamentos de 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="c3012-3179">**\_ reservado**: reservado.</span><span class="sxs-lookup"><span data-stu-id="c3012-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="c3012-3180">O servidor pode enviar um número arbitrário de valores arbitrários e o cliente deve ignorar esses valores, se houver.</span><span class="sxs-lookup"><span data-stu-id="c3012-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="c3012-3181">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="c3012-3182">A mensagem CPMCreateQueryIn cria uma nova consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="c3012-3183">O formato da mensagem CPMCreateQueryIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-3184">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3184">0</span></span>

<span data-ttu-id="c3012-3185">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3185">1</span></span>

<span data-ttu-id="c3012-3186">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3186">2</span></span>

<span data-ttu-id="c3012-3187">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3187">3</span></span>

<span data-ttu-id="c3012-3188">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3188">4</span></span>

<span data-ttu-id="c3012-3189">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3189">5</span></span>

<span data-ttu-id="c3012-3190">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3190">6</span></span>

<span data-ttu-id="c3012-3191">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3191">7</span></span>

<span data-ttu-id="c3012-3192">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3192">8</span></span>

<span data-ttu-id="c3012-3193">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3193">9</span></span>

<span data-ttu-id="c3012-3194">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3194">1</span></span><br/> <span data-ttu-id="c3012-3195">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3195">0</span></span><br/>

<span data-ttu-id="c3012-3196">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3196">1</span></span>

<span data-ttu-id="c3012-3197">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3197">2</span></span>

<span data-ttu-id="c3012-3198">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3198">3</span></span>

<span data-ttu-id="c3012-3199">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3199">4</span></span>

<span data-ttu-id="c3012-3200">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3200">5</span></span>

<span data-ttu-id="c3012-3201">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3201">6</span></span>

<span data-ttu-id="c3012-3202">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3202">7</span></span>

<span data-ttu-id="c3012-3203">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3203">8</span></span>

<span data-ttu-id="c3012-3204">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3204">9</span></span>

<span data-ttu-id="c3012-3205">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3205">2</span></span><br/> <span data-ttu-id="c3012-3206">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3206">0</span></span><br/>

<span data-ttu-id="c3012-3207">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3207">1</span></span>

<span data-ttu-id="c3012-3208">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3208">2</span></span>

<span data-ttu-id="c3012-3209">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3209">3</span></span>

<span data-ttu-id="c3012-3210">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3210">4</span></span>

<span data-ttu-id="c3012-3211">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3211">5</span></span>

<span data-ttu-id="c3012-3212">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3212">6</span></span>

<span data-ttu-id="c3012-3213">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3213">7</span></span>

<span data-ttu-id="c3012-3214">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3214">8</span></span>

<span data-ttu-id="c3012-3215">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3215">9</span></span>

<span data-ttu-id="c3012-3216">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3216">3</span></span><br/> <span data-ttu-id="c3012-3217">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3217">0</span></span><br/>

<span data-ttu-id="c3012-3218">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3218">1</span></span>

<span data-ttu-id="c3012-3219">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c3012-3219">Size</span></span>

<span data-ttu-id="c3012-3220">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="c3012-3220">CColumnSetPresent</span></span>

<span data-ttu-id="c3012-3221">Colunaset (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="c3012-3222">... Ela</span><span class="sxs-lookup"><span data-stu-id="c3012-3222">... (variable)</span></span>

<span data-ttu-id="c3012-3223">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="c3012-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="c3012-3224">Restrição (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3224">Restriction (optional)</span></span>

<span data-ttu-id="c3012-3225">... Ela</span><span class="sxs-lookup"><span data-stu-id="c3012-3225">... (variable)</span></span>

<span data-ttu-id="c3012-3226">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="c3012-3226">CSortSetPresent</span></span>

<span data-ttu-id="c3012-3227">Tipo de classificação (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3227">SortSet (optional)</span></span>

<span data-ttu-id="c3012-3228">... Ela</span><span class="sxs-lookup"><span data-stu-id="c3012-3228">... (variable)</span></span>

<span data-ttu-id="c3012-3229">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="c3012-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="c3012-3230">CategorizationSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="c3012-3231">... Ela</span><span class="sxs-lookup"><span data-stu-id="c3012-3231">... (variable)</span></span>

<span data-ttu-id="c3012-3232">Conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="c3012-3232">RowSetProperties</span></span>

<span data-ttu-id="c3012-3233">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3233">...</span></span>

<span data-ttu-id="c3012-3234">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3234">...</span></span>

<span data-ttu-id="c3012-3235">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3235">...</span></span>

<span data-ttu-id="c3012-3236">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3236">...</span></span>

<span data-ttu-id="c3012-3237">PidMapper (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="c3012-3238">**Tamanho**: um inteiro de 32 bits sem sinal indicando o número de bytes desde o início deste campo até o final da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="c3012-3239">**CColumnSetPresent**: um campo de byte que indica se o campo ColumnSet está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="c3012-3240">Esse campo deve ser definido como 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3012-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="c3012-3241">Se definido como 0x01, o campo CColumnSet deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="c3012-3242">Se definido como 0x00, ele deve estar ausente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="c3012-3243">**ColumnSet**: uma estrutura CColumnSet que contém os números de coluna nos quais as propriedades de CPidMapper serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="c3012-3244">**CRestrictionPresent**: um campo de byte que indica se o campo de restrição está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="c3012-3245">Se definido como qualquer valor diferente de zero, o campo de restrição deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="c3012-3246">Se definido como 0x00, a restrição deverá estar ausente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="c3012-3247">**Restrição**: uma estrutura CRestriction que contém a árvore de comandos da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="c3012-3248">**CSortSetPresent**: um campo de byte que indica se o campo de classificação está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="c3012-3249">Se definido como qualquer valor diferente de zero, o campo Sortset deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="c3012-3250">Se definido como 0x00, Sortset deve estar ausente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="c3012-3251">**Sortset**: uma estrutura CSortSet que indica a ordem de classificação da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="c3012-3252">**CCategorizationSetPresent**: um campo de byte que indica se o campo CCategorizationSet está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="c3012-3253">Se definido como qualquer valor diferente de zero, o campo CCategorizationSet deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="c3012-3254">Se definido como 0x00, CCategorizationSet deve estar ausente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="c3012-3255">**CCategorizationSet**: uma estrutura CCategorizationSet que contém os grupos para a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="c3012-3256">**Conjunto de linhas**: uma estrutura CRowsetProperties que fornece informações de configuração para a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="c3012-3257">**PidMapper**: uma estrutura CPidMapper que contém propriedades para retornar em um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="c3012-3258">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="c3012-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="c3012-3259">A mensagem CPMCreateQueryOut contém uma resposta a uma mensagem CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="c3012-3260">O formato da mensagem CPMCreateQueryOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-3261">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3261">0</span></span>

<span data-ttu-id="c3012-3262">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3262">1</span></span>

<span data-ttu-id="c3012-3263">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3263">2</span></span>

<span data-ttu-id="c3012-3264">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3264">3</span></span>

<span data-ttu-id="c3012-3265">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3265">4</span></span>

<span data-ttu-id="c3012-3266">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3266">5</span></span>

<span data-ttu-id="c3012-3267">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3267">6</span></span>

<span data-ttu-id="c3012-3268">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3268">7</span></span>

<span data-ttu-id="c3012-3269">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3269">8</span></span>

<span data-ttu-id="c3012-3270">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3270">9</span></span>

<span data-ttu-id="c3012-3271">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3271">1</span></span><br/> <span data-ttu-id="c3012-3272">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3272">0</span></span><br/>

<span data-ttu-id="c3012-3273">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3273">1</span></span>

<span data-ttu-id="c3012-3274">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3274">2</span></span>

<span data-ttu-id="c3012-3275">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3275">3</span></span>

<span data-ttu-id="c3012-3276">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3276">4</span></span>

<span data-ttu-id="c3012-3277">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3277">5</span></span>

<span data-ttu-id="c3012-3278">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3278">6</span></span>

<span data-ttu-id="c3012-3279">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3279">7</span></span>

<span data-ttu-id="c3012-3280">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3280">8</span></span>

<span data-ttu-id="c3012-3281">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3281">9</span></span>

<span data-ttu-id="c3012-3282">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3282">2</span></span><br/> <span data-ttu-id="c3012-3283">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3283">0</span></span><br/>

<span data-ttu-id="c3012-3284">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3284">1</span></span>

<span data-ttu-id="c3012-3285">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3285">2</span></span>

<span data-ttu-id="c3012-3286">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3286">3</span></span>

<span data-ttu-id="c3012-3287">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3287">4</span></span>

<span data-ttu-id="c3012-3288">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3288">5</span></span>

<span data-ttu-id="c3012-3289">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3289">6</span></span>

<span data-ttu-id="c3012-3290">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3290">7</span></span>

<span data-ttu-id="c3012-3291">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3291">8</span></span>

<span data-ttu-id="c3012-3292">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3292">9</span></span>

<span data-ttu-id="c3012-3293">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3293">3</span></span><br/> <span data-ttu-id="c3012-3294">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3294">0</span></span><br/>

<span data-ttu-id="c3012-3295">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3295">1</span></span>

<span data-ttu-id="c3012-3296">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="c3012-3296">\_fTrueSequential</span></span>

<span data-ttu-id="c3012-3297">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="c3012-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="c3012-3298">aCursors</span><span class="sxs-lookup"><span data-stu-id="c3012-3298">aCursors</span></span>



 

<span data-ttu-id="c3012-3299">**\_ fTrueSequential**: um valor booliano informativo que indica se a consulta pode ser esperada para fornecer resultados mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="c3012-3300">Quando definido como 0x00000001 para a consulta fornecida em CPMCreateQueryIn, o servidor pode usar o índice de forma que os resultados da consulta provavelmente serão entregues mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="c3012-3301">Quando definido como 0x00000000, haveria uma latência maior no fornecimento dos resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="c3012-3302">Não deve ser definido como qualquer outro valor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="c3012-3303">**\_ fWorkIdUnique**: um valor booliano que indica se os identificadores de documento apontados pelos cursores são exclusivos durante os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="c3012-3304">Se definido como 0x00000001, os identificadores são exclusivos.</span><span class="sxs-lookup"><span data-stu-id="c3012-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="c3012-3305">Se definido como 0x00000000, eles serão exclusivos somente em todo o conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="c3012-3306">**aCursors**: uma matriz de inteiros de 32 bits sem sinal representando os identificadores para cursores, com o número de elementos igual ao número de categorias no campo CategorizationSet da mensagem CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="c3012-3307">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="c3012-3308">A mensagem CPMGetQueryStatusIn solicita o status de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="c3012-3309">O formato da mensagem CPMGetQueryStatusIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-3310">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3310">0</span></span>

<span data-ttu-id="c3012-3311">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3311">1</span></span>

<span data-ttu-id="c3012-3312">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3312">2</span></span>

<span data-ttu-id="c3012-3313">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3313">3</span></span>

<span data-ttu-id="c3012-3314">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3314">4</span></span>

<span data-ttu-id="c3012-3315">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3315">5</span></span>

<span data-ttu-id="c3012-3316">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3316">6</span></span>

<span data-ttu-id="c3012-3317">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3317">7</span></span>

<span data-ttu-id="c3012-3318">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3318">8</span></span>

<span data-ttu-id="c3012-3319">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3319">9</span></span>

<span data-ttu-id="c3012-3320">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3320">1</span></span><br/> <span data-ttu-id="c3012-3321">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3321">0</span></span><br/>

<span data-ttu-id="c3012-3322">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3322">1</span></span>

<span data-ttu-id="c3012-3323">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3323">2</span></span>

<span data-ttu-id="c3012-3324">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3324">3</span></span>

<span data-ttu-id="c3012-3325">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3325">4</span></span>

<span data-ttu-id="c3012-3326">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3326">5</span></span>

<span data-ttu-id="c3012-3327">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3327">6</span></span>

<span data-ttu-id="c3012-3328">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3328">7</span></span>

<span data-ttu-id="c3012-3329">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3329">8</span></span>

<span data-ttu-id="c3012-3330">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3330">9</span></span>

<span data-ttu-id="c3012-3331">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3331">2</span></span><br/> <span data-ttu-id="c3012-3332">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3332">0</span></span><br/>

<span data-ttu-id="c3012-3333">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3333">1</span></span>

<span data-ttu-id="c3012-3334">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3334">2</span></span>

<span data-ttu-id="c3012-3335">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3335">3</span></span>

<span data-ttu-id="c3012-3336">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3336">4</span></span>

<span data-ttu-id="c3012-3337">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3337">5</span></span>

<span data-ttu-id="c3012-3338">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3338">6</span></span>

<span data-ttu-id="c3012-3339">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3339">7</span></span>

<span data-ttu-id="c3012-3340">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3340">8</span></span>

<span data-ttu-id="c3012-3341">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3341">9</span></span>

<span data-ttu-id="c3012-3342">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3342">3</span></span><br/> <span data-ttu-id="c3012-3343">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3343">0</span></span><br/>

<span data-ttu-id="c3012-3344">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3344">1</span></span>

<span data-ttu-id="c3012-3345">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3012-3345">\_hCursor</span></span>



 

<span data-ttu-id="c3012-3346">**\_ hCursor**: um inteiro sem sinal de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual recuperar informações de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="c3012-3347">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="c3012-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="c3012-3348">A mensagem CPMGetQueryStatusOut responde a uma mensagem CPMGetQueryStatusIn com o status da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="c3012-3349">O formato da mensagem CPMGetQueryStatusOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-3350">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3350">0</span></span>

<span data-ttu-id="c3012-3351">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3351">1</span></span>

<span data-ttu-id="c3012-3352">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3352">2</span></span>

<span data-ttu-id="c3012-3353">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3353">3</span></span>

<span data-ttu-id="c3012-3354">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3354">4</span></span>

<span data-ttu-id="c3012-3355">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3355">5</span></span>

<span data-ttu-id="c3012-3356">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3356">6</span></span>

<span data-ttu-id="c3012-3357">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3357">7</span></span>

<span data-ttu-id="c3012-3358">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3358">8</span></span>

<span data-ttu-id="c3012-3359">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3359">9</span></span>

<span data-ttu-id="c3012-3360">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3360">1</span></span><br/> <span data-ttu-id="c3012-3361">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3361">0</span></span><br/>

<span data-ttu-id="c3012-3362">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3362">1</span></span>

<span data-ttu-id="c3012-3363">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3363">2</span></span>

<span data-ttu-id="c3012-3364">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3364">3</span></span>

<span data-ttu-id="c3012-3365">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3365">4</span></span>

<span data-ttu-id="c3012-3366">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3366">5</span></span>

<span data-ttu-id="c3012-3367">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3367">6</span></span>

<span data-ttu-id="c3012-3368">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3368">7</span></span>

<span data-ttu-id="c3012-3369">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3369">8</span></span>

<span data-ttu-id="c3012-3370">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3370">9</span></span>

<span data-ttu-id="c3012-3371">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3371">2</span></span><br/> <span data-ttu-id="c3012-3372">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3372">0</span></span><br/>

<span data-ttu-id="c3012-3373">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3373">1</span></span>

<span data-ttu-id="c3012-3374">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3374">2</span></span>

<span data-ttu-id="c3012-3375">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3375">3</span></span>

<span data-ttu-id="c3012-3376">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3376">4</span></span>

<span data-ttu-id="c3012-3377">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3377">5</span></span>

<span data-ttu-id="c3012-3378">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3378">6</span></span>

<span data-ttu-id="c3012-3379">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3379">7</span></span>

<span data-ttu-id="c3012-3380">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3380">8</span></span>

<span data-ttu-id="c3012-3381">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3381">9</span></span>

<span data-ttu-id="c3012-3382">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3382">3</span></span><br/> <span data-ttu-id="c3012-3383">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3383">0</span></span><br/>

<span data-ttu-id="c3012-3384">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3384">1</span></span>

<span data-ttu-id="c3012-3385">\_Status</span><span class="sxs-lookup"><span data-stu-id="c3012-3385">\_Status</span></span>



 

<span data-ttu-id="c3012-3386">**\_ Status**: uma bitmask de valores definida nas tabelas abaixo, que descreve a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="c3012-3387">A tabela a seguir lista \_ \* os valores de stat obtidos com a execução de uma operação and bit a bit no \_ status com 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="c3012-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="c3012-3388">O resultado deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="c3012-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="c3012-3389">Constante</span><span class="sxs-lookup"><span data-stu-id="c3012-3389">Constant</span></span>                 | <span data-ttu-id="c3012-3390">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-3391">STAT \_ ocupado 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="c3012-3392">A consulta assíncrona ainda está em execução.</span><span class="sxs-lookup"><span data-stu-id="c3012-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="c3012-3393">Erro de STAT \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="c3012-3394">A consulta está em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="c3012-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="c3012-3395">STAT \_ concluído 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="c3012-3396">A consulta foi concluída.</span><span class="sxs-lookup"><span data-stu-id="c3012-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="c3012-3397">STAT \_ Refresh 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="c3012-3398">A consulta foi concluída, mas as atualizações estão resultando em computação de consulta adicional.</span><span class="sxs-lookup"><span data-stu-id="c3012-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="c3012-3399">A tabela a seguir lista bits de estatística adicionais \_ \* que podem ser definidos de forma independente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="c3012-3400">Constante</span><span class="sxs-lookup"><span data-stu-id="c3012-3400">Constant</span></span>                                    | <span data-ttu-id="c3012-3401">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3012-3402">STATar \_ palavras de ruído \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3012-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="c3012-3403">Palavras de ruído foram substituídas por caracteres curinga na consulta de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c3012-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="c3012-3404">\_Conteúdo \_ de stat fora \_ da \_ Data 0x00000020</span><span class="sxs-lookup"><span data-stu-id="c3012-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="c3012-3405">Os resultados da consulta podem estar incorretos porque a consulta envolvia arquivos modificados, mas não indexados.</span><span class="sxs-lookup"><span data-stu-id="c3012-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="c3012-3406">STAT \_ Atualizar \_ 0x00000040 incompleta</span><span class="sxs-lookup"><span data-stu-id="c3012-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="c3012-3407">Os resultados da consulta podem estar incorretos porque a consulta envolvia arquivos modificados e reindexados cujo conteúdo não foi incluído.</span><span class="sxs-lookup"><span data-stu-id="c3012-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="c3012-3408">0x00000080 de consulta de conteúdo de STAT \_ \_ \_ incompleto</span><span class="sxs-lookup"><span data-stu-id="c3012-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="c3012-3409">A consulta de conteúdo era muito complexa para concluir ou requerido a enumeração em vez de usar o índice de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c3012-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="c3012-3410">O \_ limite de tempo de stat \_ \_ excedeu 0x00000100</span><span class="sxs-lookup"><span data-stu-id="c3012-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="c3012-3411">Os resultados da consulta podem estar incorretos porque o tempo de execução da consulta atingiu o tempo máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="c3012-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="c3012-3412">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="c3012-3413">A mensagem CPMGetQueryStatusExIn solicita o status de uma consulta e informações adicionais, como o número de documentos que foram indexados, o número de documentos restantes a serem indexados e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c3012-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="c3012-3414">O formato da mensagem CPMGetQueryStatusExIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-3415">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3415">0</span></span>

<span data-ttu-id="c3012-3416">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3416">1</span></span>

<span data-ttu-id="c3012-3417">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3417">2</span></span>

<span data-ttu-id="c3012-3418">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3418">3</span></span>

<span data-ttu-id="c3012-3419">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3419">4</span></span>

<span data-ttu-id="c3012-3420">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3420">5</span></span>

<span data-ttu-id="c3012-3421">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3421">6</span></span>

<span data-ttu-id="c3012-3422">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3422">7</span></span>

<span data-ttu-id="c3012-3423">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3423">8</span></span>

<span data-ttu-id="c3012-3424">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3424">9</span></span>

<span data-ttu-id="c3012-3425">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3425">1</span></span><br/> <span data-ttu-id="c3012-3426">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3426">0</span></span><br/>

<span data-ttu-id="c3012-3427">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3427">1</span></span>

<span data-ttu-id="c3012-3428">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3428">2</span></span>

<span data-ttu-id="c3012-3429">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3429">3</span></span>

<span data-ttu-id="c3012-3430">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3430">4</span></span>

<span data-ttu-id="c3012-3431">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3431">5</span></span>

<span data-ttu-id="c3012-3432">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3432">6</span></span>

<span data-ttu-id="c3012-3433">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3433">7</span></span>

<span data-ttu-id="c3012-3434">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3434">8</span></span>

<span data-ttu-id="c3012-3435">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3435">9</span></span>

<span data-ttu-id="c3012-3436">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3436">2</span></span><br/> <span data-ttu-id="c3012-3437">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3437">0</span></span><br/>

<span data-ttu-id="c3012-3438">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3438">1</span></span>

<span data-ttu-id="c3012-3439">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3439">2</span></span>

<span data-ttu-id="c3012-3440">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3440">3</span></span>

<span data-ttu-id="c3012-3441">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3441">4</span></span>

<span data-ttu-id="c3012-3442">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3442">5</span></span>

<span data-ttu-id="c3012-3443">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3443">6</span></span>

<span data-ttu-id="c3012-3444">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3444">7</span></span>

<span data-ttu-id="c3012-3445">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3445">8</span></span>

<span data-ttu-id="c3012-3446">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3446">9</span></span>

<span data-ttu-id="c3012-3447">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3447">3</span></span><br/> <span data-ttu-id="c3012-3448">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3448">0</span></span><br/>

<span data-ttu-id="c3012-3449">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3449">1</span></span>

<span data-ttu-id="c3012-3450">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3012-3450">\_hCursor</span></span>

<span data-ttu-id="c3012-3451">\_bmk</span><span class="sxs-lookup"><span data-stu-id="c3012-3451">\_bmk</span></span>



 

<span data-ttu-id="c3012-3452">**\_ hCursor**: um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual recuperar informações de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="c3012-3453">**\_ BMK**: um valor de 32 bits que indica o identificador de um indicador cuja posição deve ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="c3012-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="c3012-3454">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="c3012-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="c3012-3455">A mensagem CPMGetQueryStatusExOut responde a uma mensagem CPMGetQueryStatusExIn com o status da consulta e outras informações de status, conforme descrito no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3012-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="c3012-3456">O formato da mensagem CPMGetQueryStatusExOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-3457">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3457">0</span></span>

<span data-ttu-id="c3012-3458">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3458">1</span></span>

<span data-ttu-id="c3012-3459">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3459">2</span></span>

<span data-ttu-id="c3012-3460">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3460">3</span></span>

<span data-ttu-id="c3012-3461">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3461">4</span></span>

<span data-ttu-id="c3012-3462">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3462">5</span></span>

<span data-ttu-id="c3012-3463">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3463">6</span></span>

<span data-ttu-id="c3012-3464">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3464">7</span></span>

<span data-ttu-id="c3012-3465">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3465">8</span></span>

<span data-ttu-id="c3012-3466">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3466">9</span></span>

<span data-ttu-id="c3012-3467">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3467">1</span></span><br/> <span data-ttu-id="c3012-3468">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3468">0</span></span><br/>

<span data-ttu-id="c3012-3469">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3469">1</span></span>

<span data-ttu-id="c3012-3470">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3470">2</span></span>

<span data-ttu-id="c3012-3471">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3471">3</span></span>

<span data-ttu-id="c3012-3472">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3472">4</span></span>

<span data-ttu-id="c3012-3473">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3473">5</span></span>

<span data-ttu-id="c3012-3474">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3474">6</span></span>

<span data-ttu-id="c3012-3475">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3475">7</span></span>

<span data-ttu-id="c3012-3476">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3476">8</span></span>

<span data-ttu-id="c3012-3477">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3477">9</span></span>

<span data-ttu-id="c3012-3478">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3478">2</span></span><br/> <span data-ttu-id="c3012-3479">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3479">0</span></span><br/>

<span data-ttu-id="c3012-3480">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3480">1</span></span>

<span data-ttu-id="c3012-3481">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3481">2</span></span>

<span data-ttu-id="c3012-3482">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3482">3</span></span>

<span data-ttu-id="c3012-3483">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3483">4</span></span>

<span data-ttu-id="c3012-3484">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3484">5</span></span>

<span data-ttu-id="c3012-3485">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3485">6</span></span>

<span data-ttu-id="c3012-3486">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3486">7</span></span>

<span data-ttu-id="c3012-3487">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3487">8</span></span>

<span data-ttu-id="c3012-3488">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3488">9</span></span>

<span data-ttu-id="c3012-3489">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3489">3</span></span><br/> <span data-ttu-id="c3012-3490">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3490">0</span></span><br/>

<span data-ttu-id="c3012-3491">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3491">1</span></span>

<span data-ttu-id="c3012-3492">\_Status</span><span class="sxs-lookup"><span data-stu-id="c3012-3492">\_Status</span></span>

<span data-ttu-id="c3012-3493">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="c3012-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="c3012-3494">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="c3012-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="c3012-3495">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="c3012-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="c3012-3496">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="c3012-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="c3012-3497">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="c3012-3497">\_iRowBmk</span></span>

<span data-ttu-id="c3012-3498">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="c3012-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="c3012-3499">**\_ Status**: um dos stats \_ \* valores especificados na seção 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="c3012-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="c3012-3500">**\_ cFilteredDocuments**: um inteiro sem sinal de 32 bits indicando o número de documentos que foram indexados</span><span class="sxs-lookup"><span data-stu-id="c3012-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="c3012-3501">**\_ cDocumentsToFilter**: um inteiro de 32 bits sem sinal indicando o número de documentos que ainda permanecem para serem indexados.</span><span class="sxs-lookup"><span data-stu-id="c3012-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="c3012-3502">**\_ dwRatioFinishedDenominator**: um inteiro de 32 bits sem sinal indicando o denominador da proporção de documentos que a consulta concluiu o processamento.</span><span class="sxs-lookup"><span data-stu-id="c3012-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="c3012-3503">**\_ dwRatioFinishedNumerator**: um inteiro de 32 bits sem sinal indicando o numerador da proporção de documentos que a consulta concluiu o processamento.</span><span class="sxs-lookup"><span data-stu-id="c3012-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="c3012-3504">**\_ iRowBmk**: um inteiro de 32 bits sem sinal indicando a posição aproximada do indicador no conjunto de linhas em termos de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="c3012-3505">**\_ cRowsTotal**: um inteiro de 32 bits sem sinal especificando o número total de linhas no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="c3012-3506">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="c3012-3507">A mensagem CPMSetBindingsIn solicita a associação de colunas a um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="c3012-3508">O servidor responderá à mensagem de solicitação CPMSetBindingsIn usando a seção de cabeçalho da mensagem CPMBindingsIn com os resultados da solicitação contida no \_ campo status.</span><span class="sxs-lookup"><span data-stu-id="c3012-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="c3012-3509">O formato da mensagem CPMSetBindingsIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-3510">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3510">0</span></span>

<span data-ttu-id="c3012-3511">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3511">1</span></span>

<span data-ttu-id="c3012-3512">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3512">2</span></span>

<span data-ttu-id="c3012-3513">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3513">3</span></span>

<span data-ttu-id="c3012-3514">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3514">4</span></span>

<span data-ttu-id="c3012-3515">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3515">5</span></span>

<span data-ttu-id="c3012-3516">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3516">6</span></span>

<span data-ttu-id="c3012-3517">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3517">7</span></span>

<span data-ttu-id="c3012-3518">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3518">8</span></span>

<span data-ttu-id="c3012-3519">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3519">9</span></span>

<span data-ttu-id="c3012-3520">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3520">1</span></span><br/> <span data-ttu-id="c3012-3521">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3521">0</span></span><br/>

<span data-ttu-id="c3012-3522">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3522">1</span></span>

<span data-ttu-id="c3012-3523">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3523">2</span></span>

<span data-ttu-id="c3012-3524">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3524">3</span></span>

<span data-ttu-id="c3012-3525">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3525">4</span></span>

<span data-ttu-id="c3012-3526">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3526">5</span></span>

<span data-ttu-id="c3012-3527">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3527">6</span></span>

<span data-ttu-id="c3012-3528">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3528">7</span></span>

<span data-ttu-id="c3012-3529">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3529">8</span></span>

<span data-ttu-id="c3012-3530">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3530">9</span></span>

<span data-ttu-id="c3012-3531">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3531">2</span></span><br/> <span data-ttu-id="c3012-3532">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3532">0</span></span><br/>

<span data-ttu-id="c3012-3533">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3533">1</span></span>

<span data-ttu-id="c3012-3534">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3534">2</span></span>

<span data-ttu-id="c3012-3535">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3535">3</span></span>

<span data-ttu-id="c3012-3536">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3536">4</span></span>

<span data-ttu-id="c3012-3537">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3537">5</span></span>

<span data-ttu-id="c3012-3538">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3538">6</span></span>

<span data-ttu-id="c3012-3539">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3539">7</span></span>

<span data-ttu-id="c3012-3540">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3540">8</span></span>

<span data-ttu-id="c3012-3541">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3541">9</span></span>

<span data-ttu-id="c3012-3542">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3542">3</span></span><br/> <span data-ttu-id="c3012-3543">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3543">0</span></span><br/>

<span data-ttu-id="c3012-3544">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3544">1</span></span>

<span data-ttu-id="c3012-3545">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="c3012-3546">\_cbRow (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="c3012-3547">\_cbBindingDesc (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="c3012-3548">\_fictício (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3548">\_dummy (optional)</span></span>

<span data-ttu-id="c3012-3549">cColumns (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3549">cColumns (optional)</span></span>

<span data-ttu-id="c3012-3550">aColumns (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="c3012-3551">**\_ hCursor**: um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a linha para a qual definir associações.</span><span class="sxs-lookup"><span data-stu-id="c3012-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="c3012-3552">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3012-3553">**\_ cbRow**: um inteiro de 32 bits sem sinal indicando o tamanho, em bytes, de uma linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="c3012-3554">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3012-3555">**\_ cbBindingDesc**: um inteiro de 32 bits sem sinal indicando o comprimento, em bytes, dos campos que seguem o \_ campo fictício.</span><span class="sxs-lookup"><span data-stu-id="c3012-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="c3012-3556">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3012-3557">**\_ fictícia**: Este campo não é usado e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3012-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="c3012-3558">Ele pode ser definido como qualquer valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="c3012-3559">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3012-3560">**cColumns**: um inteiro de 32 bits sem sinal indicando o número de elementos na matriz aColumns.</span><span class="sxs-lookup"><span data-stu-id="c3012-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="c3012-3561">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3012-3562">**aColumns**: uma matriz de estruturas CTableColumn que descreve as colunas de uma linha no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="c3012-3563">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3012-3564">As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura tenha um alinhamento de 4 bytes desde o início de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="c3012-3565">Esses bytes de preenchimento podem ser qualquer valor arbitrário e devem ser ignorados no recebimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="c3012-3566">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="c3012-3567">A mensagem CPMGetRowsIn solicita linhas de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="c3012-3568">O formato da mensagem CPMGetRowsIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-3569">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3569">0</span></span>

<span data-ttu-id="c3012-3570">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3570">1</span></span>

<span data-ttu-id="c3012-3571">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3571">2</span></span>

<span data-ttu-id="c3012-3572">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3572">3</span></span>

<span data-ttu-id="c3012-3573">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3573">4</span></span>

<span data-ttu-id="c3012-3574">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3574">5</span></span>

<span data-ttu-id="c3012-3575">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3575">6</span></span>

<span data-ttu-id="c3012-3576">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3576">7</span></span>

<span data-ttu-id="c3012-3577">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3577">8</span></span>

<span data-ttu-id="c3012-3578">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3578">9</span></span>

<span data-ttu-id="c3012-3579">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3579">1</span></span><br/> <span data-ttu-id="c3012-3580">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3580">0</span></span><br/>

<span data-ttu-id="c3012-3581">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3581">1</span></span>

<span data-ttu-id="c3012-3582">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3582">2</span></span>

<span data-ttu-id="c3012-3583">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3583">3</span></span>

<span data-ttu-id="c3012-3584">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3584">4</span></span>

<span data-ttu-id="c3012-3585">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3585">5</span></span>

<span data-ttu-id="c3012-3586">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3586">6</span></span>

<span data-ttu-id="c3012-3587">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3587">7</span></span>

<span data-ttu-id="c3012-3588">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3588">8</span></span>

<span data-ttu-id="c3012-3589">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3589">9</span></span>

<span data-ttu-id="c3012-3590">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3590">2</span></span><br/> <span data-ttu-id="c3012-3591">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3591">0</span></span><br/>

<span data-ttu-id="c3012-3592">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3592">1</span></span>

<span data-ttu-id="c3012-3593">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3593">2</span></span>

<span data-ttu-id="c3012-3594">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3594">3</span></span>

<span data-ttu-id="c3012-3595">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3595">4</span></span>

<span data-ttu-id="c3012-3596">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3596">5</span></span>

<span data-ttu-id="c3012-3597">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3597">6</span></span>

<span data-ttu-id="c3012-3598">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3598">7</span></span>

<span data-ttu-id="c3012-3599">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3599">8</span></span>

<span data-ttu-id="c3012-3600">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3600">9</span></span>

<span data-ttu-id="c3012-3601">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3601">3</span></span><br/> <span data-ttu-id="c3012-3602">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3602">0</span></span><br/>

<span data-ttu-id="c3012-3603">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3603">1</span></span>

<span data-ttu-id="c3012-3604">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3012-3604">\_hCursor</span></span>

<span data-ttu-id="c3012-3605">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="c3012-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="c3012-3606">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="c3012-3606">\_cbRowWidth</span></span>

<span data-ttu-id="c3012-3607">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="c3012-3607">\_cbSeek</span></span>

<span data-ttu-id="c3012-3608">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="c3012-3608">\_cbReserved</span></span>

<span data-ttu-id="c3012-3609">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="c3012-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="c3012-3610">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="c3012-3610">\_ulClientBase</span></span>

<span data-ttu-id="c3012-3611">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="c3012-3611">\_fBwdFetch</span></span>

<span data-ttu-id="c3012-3612">eType</span><span class="sxs-lookup"><span data-stu-id="c3012-3612">eType</span></span>

<span data-ttu-id="c3012-3613">\_chapt</span><span class="sxs-lookup"><span data-stu-id="c3012-3613">\_chapt</span></span>

<span data-ttu-id="c3012-3614">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="c3012-3614">SeekDescription</span></span>

<span data-ttu-id="c3012-3615">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3615">...</span></span>

<span data-ttu-id="c3012-3616">... Ela</span><span class="sxs-lookup"><span data-stu-id="c3012-3616">... (variable)</span></span>



 

<span data-ttu-id="c3012-3617">**\_ hCursor**: um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="c3012-3618">**\_ cRowsToTransfer**: um inteiro sem sinal de 32 bits que indica o número máximo de linhas que o cliente deseja receber em resposta a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="c3012-3619">**\_ cbRowWidth**: um inteiro de 32 bits sem sinal indicando o comprimento de uma linha, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="c3012-3620">**\_ cbSeek**: um inteiro de 32 bits sem sinal indicando o tamanho da mensagem que começa com ETYPE.</span><span class="sxs-lookup"><span data-stu-id="c3012-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="c3012-3621">**\_ cbReserved**: um inteiro não assinado de 32 bits que indica o tamanho, em bytes, de uma mensagem CPMGetRowsOut (sem os campos Rows e SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="c3012-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="c3012-3622">Esse valor neste campo é adicionado ao valor do \_ campo cbSeek e, em seguida, é usado para calcular o deslocamento do campo de linhas na mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="c3012-3623">**\_ cbReadBuffer**: um inteiro sem sinal de 32 bits, que deve ser definido como o máximo do valor de \_ cbRowWidth ou 1000 vezes o valor de \_ cRowsToTransfer, arredondado para o múltiplo byte mais próximo de 512.</span><span class="sxs-lookup"><span data-stu-id="c3012-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="c3012-3624">O valor não deve exceder 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="c3012-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="c3012-3625">**\_ ulClientBase**: um inteiro de 32 bits sem sinal indicando o valor de base a ser usado para cálculos de ponteiro no buffer de linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="c3012-3626">Se os deslocamentos de 64 bits estiverem sendo usados, o campo reserved2 do cabeçalho da mensagem será usado como o 32 superior-bits e o \_ ulClientBase como os 32 menores bits de um valor de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="c3012-3627">Consulte a seção 2.2.3.16 para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="c3012-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="c3012-3628">**\_ fBwdFetch**: um inteiro de 32 bits sem sinal indicando a ordem na qual buscar as linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="c3012-3629">Se definido como 0x00000001, as linhas serão buscadas na ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="c3012-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="c3012-3630">Se definido como 0x00000000, as linhas serão buscadas na ordem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="c3012-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="c3012-3631">Não deve ser definido para nenhum outro valor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="c3012-3632">**ETYPE**: um inteiro sem sinal de 32 bits contendo um dos valores a seguir para indicar o tipo de operação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="c3012-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="c3012-3633">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-3633">Value</span></span>                         | <span data-ttu-id="c3012-3634">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="c3012-3635">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="c3012-3636">SeekDescription contém uma estrutura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="c3012-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="c3012-3637">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="c3012-3638">SeekDescription contém uma estrutura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="c3012-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="c3012-3639">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="c3012-3640">SeekDescription contém uma estrutura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="c3012-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="c3012-3641">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="c3012-3642">SeekDescription contém uma estrutura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="c3012-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="c3012-3643">**\_ chapt**: um valor de 32 bits que representa o identificador do capítulo do conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="c3012-3644">**SeekDescription**: esse campo deve conter uma estrutura do tipo indicado pelo valor de ETYPE.</span><span class="sxs-lookup"><span data-stu-id="c3012-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="c3012-3645">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="c3012-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="c3012-3646">A mensagem CPMGetRowsOut responde a uma mensagem CPMGetRowsIn com as linhas de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="c3012-3647">Os servidores devem Formatar deslocamentos para tipos de dados de comprimento variável no campo linhas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="c3012-3648">O cliente indicou que era um sistema de 32 bits (0x00000008 ou menos no campo iClientVersion de CPMConnectIn): os deslocamentos são inteiros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="c3012-3649">O cliente indicou que era um sistema de 64 bits ( \_ iClientVersion > 0x00000008 no CPMConnectIn) e o servidor indicou que era um sistema de 32 bits ( \_ serverVersion definido como 0X00000007 em CPMConnectOut): os deslocamentos são inteiros de 32 bits</span><span class="sxs-lookup"><span data-stu-id="c3012-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="c3012-3650">O cliente indicou que era um sistema de 64 bits ( \_ iClientVersion > 0x00000008 no CPMConnectIn) e o servidor indicou que era um sistema de 64 bits ( \_ serverVersion definido como 0X00010007 em CPMConnectOut): os deslocamentos são inteiros de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c3012-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="c3012-3651">O formato da mensagem CPMGetRowsOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-3652">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3652">0</span></span>

<span data-ttu-id="c3012-3653">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3653">1</span></span>

<span data-ttu-id="c3012-3654">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3654">2</span></span>

<span data-ttu-id="c3012-3655">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3655">3</span></span>

<span data-ttu-id="c3012-3656">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3656">4</span></span>

<span data-ttu-id="c3012-3657">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3657">5</span></span>

<span data-ttu-id="c3012-3658">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3658">6</span></span>

<span data-ttu-id="c3012-3659">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3659">7</span></span>

<span data-ttu-id="c3012-3660">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3660">8</span></span>

<span data-ttu-id="c3012-3661">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3661">9</span></span>

<span data-ttu-id="c3012-3662">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3662">1</span></span><br/> <span data-ttu-id="c3012-3663">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3663">0</span></span><br/>

<span data-ttu-id="c3012-3664">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3664">1</span></span>

<span data-ttu-id="c3012-3665">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3665">2</span></span>

<span data-ttu-id="c3012-3666">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3666">3</span></span>

<span data-ttu-id="c3012-3667">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3667">4</span></span>

<span data-ttu-id="c3012-3668">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3668">5</span></span>

<span data-ttu-id="c3012-3669">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3669">6</span></span>

<span data-ttu-id="c3012-3670">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3670">7</span></span>

<span data-ttu-id="c3012-3671">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3671">8</span></span>

<span data-ttu-id="c3012-3672">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3672">9</span></span>

<span data-ttu-id="c3012-3673">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3673">2</span></span><br/> <span data-ttu-id="c3012-3674">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3674">0</span></span><br/>

<span data-ttu-id="c3012-3675">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3675">1</span></span>

<span data-ttu-id="c3012-3676">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3676">2</span></span>

<span data-ttu-id="c3012-3677">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3677">3</span></span>

<span data-ttu-id="c3012-3678">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3678">4</span></span>

<span data-ttu-id="c3012-3679">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3679">5</span></span>

<span data-ttu-id="c3012-3680">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3680">6</span></span>

<span data-ttu-id="c3012-3681">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3681">7</span></span>

<span data-ttu-id="c3012-3682">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3682">8</span></span>

<span data-ttu-id="c3012-3683">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3683">9</span></span>

<span data-ttu-id="c3012-3684">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3684">3</span></span><br/> <span data-ttu-id="c3012-3685">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3685">0</span></span><br/>

<span data-ttu-id="c3012-3686">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3686">1</span></span>

<span data-ttu-id="c3012-3687">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="c3012-3687">\_cRowsReturned</span></span>

<span data-ttu-id="c3012-3688">eType</span><span class="sxs-lookup"><span data-stu-id="c3012-3688">eType</span></span>

<span data-ttu-id="c3012-3689">\_chapt</span><span class="sxs-lookup"><span data-stu-id="c3012-3689">\_chapt</span></span>

<span data-ttu-id="c3012-3690">SeekDescription (opcional, variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="c3012-3691">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3691">...</span></span>

<span data-ttu-id="c3012-3692">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3692">...</span></span>

<span data-ttu-id="c3012-3693">paddingRows (opcional, variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="c3012-3694">Linhas</span><span class="sxs-lookup"><span data-stu-id="c3012-3694">Rows</span></span>



 

<span data-ttu-id="c3012-3695">**\_ cRowsReturned**: um inteiro de 32 bits sem sinal indicando o número de linhas retornadas em linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="c3012-3696">**ETYPE**: um inteiro sem sinal de 32 bits contendo um dos seguintes valores para indicar o tipo de operação de busca a ser executada</span><span class="sxs-lookup"><span data-stu-id="c3012-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="c3012-3697">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-3697">Value</span></span>                         | <span data-ttu-id="c3012-3698">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="c3012-3699">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="c3012-3700">Sem SeekDescription, ignore o campo SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="c3012-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="c3012-3701">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="c3012-3702">SeekDescription contém uma estrutura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="c3012-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="c3012-3703">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="c3012-3704">SeekDescription contém uma estrutura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="c3012-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="c3012-3705">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="c3012-3706">SeekDescription contém uma estrutura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="c3012-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="c3012-3707">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="c3012-3708">SeekDescription contém uma estrutura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="c3012-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="c3012-3709">**\_ chapt**: um valor de 32 bits que representa o identificador do capítulo do conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="c3012-3710">**SeekDescription**: esse campo deve conter uma estrutura do tipo indicado pelo campo ETYPE.</span><span class="sxs-lookup"><span data-stu-id="c3012-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="c3012-3711">**paddingRows**: esse campo deve ter comprimento suficiente (0 a \_ cbReserved-1 bytes) para preencher o campo de linhas para o \_ deslocamento de cbReserved do início de uma mensagem, em que \_ cbReserved é o valor na mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="c3012-3712">Os bytes de preenchimento usados nesse campo podem ser de qualquer valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="c3012-3713">Este campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3012-3714">**Linhas**: dados de linha, são formatados conforme prescrito pelas informações de coluna na mensagem CPMSetBindingsIn mais recente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="c3012-3715">As linhas devem ser armazenadas na ordem de encaminhamento (por exemplo, linha 1 antes da linha 2).</span><span class="sxs-lookup"><span data-stu-id="c3012-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="c3012-3716">Colunas de tamanho fixo devem ser armazenadas nos deslocamentos especificados pela mensagem CPMSetBindingsIn mais recente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="c3012-3717">Colunas de tamanho variável (por exemplo, cadeias de caracteres) devem ser armazenadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="c3012-3718">A variável de dados em si (por exemplo, a cadeia de caracteres) é armazenada perto do final do buffer em ordem decrescente (por exemplo, a coleção de todos os dados da variável para a linha 1 está no final, linha 2 mais próxima, etc.).</span><span class="sxs-lookup"><span data-stu-id="c3012-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="c3012-3719">A área de tamanho fixo (no início do buffer de linha) deve conter um CRowVariant para cada coluna, armazenado no deslocamento especificado na mensagem de CPMSetBindingsIn mais recente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="c3012-3720">vType deve conter o tipo de dados (ex: VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="c3012-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="c3012-3721">Se, conforme determinado pelas regras no início da seção, esta seção, os deslocamentos de 32 bits estão sendo usados, o campo de deslocamento em CRowVariant deve conter um valor de 32 bits que é o deslocamento dos dados da variável do início da mensagem CPMGetRowsOut, mais o valor de \_ ulClientBase especificado na mensagem de CPMGetRowsIn mais recente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="c3012-3722">Se os deslocamentos de 64 bits estiverem sendo usados, o campo de deslocamento em CRowVariant deverá conter um valor de 64 bits que é o deslocamento do início da mensagem CPMGetRowsOut, adicionado a um valor de 64 bits composto por meio de \_ ulClientBase como baixo 32-bits e \_ ulReserved2 como o alto 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="c3012-3723">Por exemplo, se a mensagem CPMSetBindingsIn especificou duas colunas-size (VT \_ i4) e Title (VT \_ LPWSTR)-e \_ ulClientBase de CPMGetRowsIn for 0x10000, duas linhas aparecerão da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="c3012-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="c3012-3724">A seção marcada em cinza é a parte de comprimento fixo do buffer.</span><span class="sxs-lookup"><span data-stu-id="c3012-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![exemplo de mensagem cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="c3012-3726">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="c3012-3727">A mensagem CPMRatioFinishedIn solicita a porcentagem de conclusão de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="c3012-3728">O formato da mensagem CPMRatioFinishedIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-3729">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3729">0</span></span>

<span data-ttu-id="c3012-3730">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3730">1</span></span>

<span data-ttu-id="c3012-3731">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3731">2</span></span>

<span data-ttu-id="c3012-3732">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3732">3</span></span>

<span data-ttu-id="c3012-3733">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3733">4</span></span>

<span data-ttu-id="c3012-3734">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3734">5</span></span>

<span data-ttu-id="c3012-3735">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3735">6</span></span>

<span data-ttu-id="c3012-3736">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3736">7</span></span>

<span data-ttu-id="c3012-3737">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3737">8</span></span>

<span data-ttu-id="c3012-3738">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3738">9</span></span>

<span data-ttu-id="c3012-3739">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3739">1</span></span><br/> <span data-ttu-id="c3012-3740">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3740">0</span></span><br/>

<span data-ttu-id="c3012-3741">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3741">1</span></span>

<span data-ttu-id="c3012-3742">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3742">2</span></span>

<span data-ttu-id="c3012-3743">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3743">3</span></span>

<span data-ttu-id="c3012-3744">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3744">4</span></span>

<span data-ttu-id="c3012-3745">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3745">5</span></span>

<span data-ttu-id="c3012-3746">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3746">6</span></span>

<span data-ttu-id="c3012-3747">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3747">7</span></span>

<span data-ttu-id="c3012-3748">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3748">8</span></span>

<span data-ttu-id="c3012-3749">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3749">9</span></span>

<span data-ttu-id="c3012-3750">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3750">2</span></span><br/> <span data-ttu-id="c3012-3751">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3751">0</span></span><br/>

<span data-ttu-id="c3012-3752">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3752">1</span></span>

<span data-ttu-id="c3012-3753">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3753">2</span></span>

<span data-ttu-id="c3012-3754">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3754">3</span></span>

<span data-ttu-id="c3012-3755">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3755">4</span></span>

<span data-ttu-id="c3012-3756">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3756">5</span></span>

<span data-ttu-id="c3012-3757">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3757">6</span></span>

<span data-ttu-id="c3012-3758">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3758">7</span></span>

<span data-ttu-id="c3012-3759">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3759">8</span></span>

<span data-ttu-id="c3012-3760">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3760">9</span></span>

<span data-ttu-id="c3012-3761">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3761">3</span></span><br/> <span data-ttu-id="c3012-3762">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3762">0</span></span><br/>

<span data-ttu-id="c3012-3763">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3763">1</span></span>

<span data-ttu-id="c3012-3764">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3012-3764">\_hCursor</span></span>

<span data-ttu-id="c3012-3765">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="c3012-3765">\_fQuick</span></span>



 

<span data-ttu-id="c3012-3766">**\_ hCursor**: o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual solicitar informações de conclusão.</span><span class="sxs-lookup"><span data-stu-id="c3012-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="c3012-3767">**\_ fQuick**: deve ser definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="c3012-3768">Não usado e deve ser ignorado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="c3012-3769">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="c3012-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="c3012-3770">A mensagem CPMRatioFinishedOut responde a uma mensagem CPMRatioFinishedIn com a taxa de conclusão de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="c3012-3771">O formato da mensagem CPMRatioFinishedOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-3772">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3772">0</span></span>

<span data-ttu-id="c3012-3773">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3773">1</span></span>

<span data-ttu-id="c3012-3774">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3774">2</span></span>

<span data-ttu-id="c3012-3775">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3775">3</span></span>

<span data-ttu-id="c3012-3776">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3776">4</span></span>

<span data-ttu-id="c3012-3777">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3777">5</span></span>

<span data-ttu-id="c3012-3778">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3778">6</span></span>

<span data-ttu-id="c3012-3779">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3779">7</span></span>

<span data-ttu-id="c3012-3780">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3780">8</span></span>

<span data-ttu-id="c3012-3781">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3781">9</span></span>

<span data-ttu-id="c3012-3782">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3782">1</span></span><br/> <span data-ttu-id="c3012-3783">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3783">0</span></span><br/>

<span data-ttu-id="c3012-3784">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3784">1</span></span>

<span data-ttu-id="c3012-3785">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3785">2</span></span>

<span data-ttu-id="c3012-3786">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3786">3</span></span>

<span data-ttu-id="c3012-3787">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3787">4</span></span>

<span data-ttu-id="c3012-3788">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3788">5</span></span>

<span data-ttu-id="c3012-3789">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3789">6</span></span>

<span data-ttu-id="c3012-3790">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3790">7</span></span>

<span data-ttu-id="c3012-3791">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3791">8</span></span>

<span data-ttu-id="c3012-3792">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3792">9</span></span>

<span data-ttu-id="c3012-3793">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3793">2</span></span><br/> <span data-ttu-id="c3012-3794">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3794">0</span></span><br/>

<span data-ttu-id="c3012-3795">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3795">1</span></span>

<span data-ttu-id="c3012-3796">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3796">2</span></span>

<span data-ttu-id="c3012-3797">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3797">3</span></span>

<span data-ttu-id="c3012-3798">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3798">4</span></span>

<span data-ttu-id="c3012-3799">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3799">5</span></span>

<span data-ttu-id="c3012-3800">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3800">6</span></span>

<span data-ttu-id="c3012-3801">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3801">7</span></span>

<span data-ttu-id="c3012-3802">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3802">8</span></span>

<span data-ttu-id="c3012-3803">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3803">9</span></span>

<span data-ttu-id="c3012-3804">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3804">3</span></span><br/> <span data-ttu-id="c3012-3805">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3805">0</span></span><br/>

<span data-ttu-id="c3012-3806">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3806">1</span></span>

<span data-ttu-id="c3012-3807">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="c3012-3807">\_ ulNumerator</span></span>

<span data-ttu-id="c3012-3808">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="c3012-3808">\_ulDenominator</span></span>

<span data-ttu-id="c3012-3809">\_Rapina</span><span class="sxs-lookup"><span data-stu-id="c3012-3809">\_cRows</span></span>

<span data-ttu-id="c3012-3810">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="c3012-3810">\_fNewRows</span></span>



 

<span data-ttu-id="c3012-3811">**\_ ulNumerator**: um inteiro de 32 bits sem sinal indicando o numerador da taxa de conclusão em termos de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="c3012-3812">**\_ ulDenominator**: um inteiro de 32 bits sem sinal indicando o denominador da taxa de conclusão em termos de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="c3012-3813">DEVE ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="c3012-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="c3012-3814">**\_ galinha**: um inteiro de 32 bits sem sinal indicando o número total de linhas para a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="c3012-3815">**\_ fNewRows**: um valor booliano que indica se há novas linhas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c3012-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="c3012-3816">Um valor 0x00000001 indica que novas linhas estão disponíveis no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="c3012-3817">Um valor 0x00000000 indica que o conjunto de linhas não contém nenhuma linha nova.</span><span class="sxs-lookup"><span data-stu-id="c3012-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="c3012-3818">Este campo não deve ser definido para nenhum outro valor.</span><span class="sxs-lookup"><span data-stu-id="c3012-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="c3012-3819">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="c3012-3820">A mensagem CPMFetchValueIn solicita um valor de propriedade muito grande para retornar em um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="c3012-3821">Conforme especificado na seção 3.2.4.2.5, essa mensagem é enviada repetidamente para recuperar todos os bytes da propriedade, atualizando \_ cbSoFar para cada, até que o \_ campo fMoreExists da mensagem CPMFetchValueOut seja definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="c3012-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="c3012-3822">O formato da mensagem CPMFetchValueIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-3823">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3823">0</span></span>

<span data-ttu-id="c3012-3824">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3824">1</span></span>

<span data-ttu-id="c3012-3825">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3825">2</span></span>

<span data-ttu-id="c3012-3826">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3826">3</span></span>

<span data-ttu-id="c3012-3827">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3827">4</span></span>

<span data-ttu-id="c3012-3828">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3828">5</span></span>

<span data-ttu-id="c3012-3829">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3829">6</span></span>

<span data-ttu-id="c3012-3830">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3830">7</span></span>

<span data-ttu-id="c3012-3831">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3831">8</span></span>

<span data-ttu-id="c3012-3832">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3832">9</span></span>

<span data-ttu-id="c3012-3833">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3833">1</span></span><br/> <span data-ttu-id="c3012-3834">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3834">0</span></span><br/>

<span data-ttu-id="c3012-3835">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3835">1</span></span>

<span data-ttu-id="c3012-3836">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3836">2</span></span>

<span data-ttu-id="c3012-3837">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3837">3</span></span>

<span data-ttu-id="c3012-3838">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3838">4</span></span>

<span data-ttu-id="c3012-3839">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3839">5</span></span>

<span data-ttu-id="c3012-3840">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3840">6</span></span>

<span data-ttu-id="c3012-3841">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3841">7</span></span>

<span data-ttu-id="c3012-3842">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3842">8</span></span>

<span data-ttu-id="c3012-3843">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3843">9</span></span>

<span data-ttu-id="c3012-3844">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3844">2</span></span><br/> <span data-ttu-id="c3012-3845">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3845">0</span></span><br/>

<span data-ttu-id="c3012-3846">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3846">1</span></span>

<span data-ttu-id="c3012-3847">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3847">2</span></span>

<span data-ttu-id="c3012-3848">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3848">3</span></span>

<span data-ttu-id="c3012-3849">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3849">4</span></span>

<span data-ttu-id="c3012-3850">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3850">5</span></span>

<span data-ttu-id="c3012-3851">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3851">6</span></span>

<span data-ttu-id="c3012-3852">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3852">7</span></span>

<span data-ttu-id="c3012-3853">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3853">8</span></span>

<span data-ttu-id="c3012-3854">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3854">9</span></span>

<span data-ttu-id="c3012-3855">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3855">3</span></span><br/> <span data-ttu-id="c3012-3856">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3856">0</span></span><br/>

<span data-ttu-id="c3012-3857">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3857">1</span></span>

<span data-ttu-id="c3012-3858">\_wid</span><span class="sxs-lookup"><span data-stu-id="c3012-3858">\_wid</span></span>

<span data-ttu-id="c3012-3859">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="c3012-3859">\_cbSoFar</span></span>

<span data-ttu-id="c3012-3860">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="c3012-3860">\_cbPropSpec</span></span>

<span data-ttu-id="c3012-3861">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="c3012-3861">\_cbChunk</span></span>

<span data-ttu-id="c3012-3862">PropSpec (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3862">PropSpec (variable)</span></span>

<span data-ttu-id="c3012-3863">...</span><span class="sxs-lookup"><span data-stu-id="c3012-3863">...</span></span>

<span data-ttu-id="c3012-3864">\_preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="c3012-3865">**\_ wid**: um inteiro sem sinal de 32 bits que representa a ID do documento que identifica o documento para o qual uma propriedade deve ser buscada.</span><span class="sxs-lookup"><span data-stu-id="c3012-3865">**\_wid**: A 32-bit unsigned integer representing the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="c3012-3866">**\_ cbSoFar**: um inteiro sem sinal de 32 bits contendo o número de bytes transferidos anteriormente para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="c3012-3867">DEVE ser definido como 0x00000000 na primeira mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="c3012-3868">**\_ cbPropSpec**: um inteiro sem sinal de 32 bits contendo o tamanho do campo PropSpec, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="c3012-3869">**\_ cbChunk**: um inteiro sem sinal de 32 bits contendo o número máximo de bytes que o remetente pode aceitar em uma mensagem CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="c3012-3870">*Comportamento do Windows: esse campo é definido como 0x00004000 para todas as versões do Windows.*</span><span class="sxs-lookup"><span data-stu-id="c3012-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="c3012-3871">**PropSpec**: uma estrutura CFullPropSpec que especifica a propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="c3012-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="c3012-3872">**\_ preenchimento**: esse campo deve ter o comprimento necessário (de 0 a 3 bytes) para preencher a mensagem para um múltiplo de 4 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c3012-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="c3012-3873">O valor dos bytes de preenchimento pode ser qualquer valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="c3012-3874">Este campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="c3012-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="c3012-3875">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="c3012-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="c3012-3876">A mensagem CPMFetchValueOut responde a uma mensagem CPMFetchValueIn com um valor de propriedade de uma consulta anterior.</span><span class="sxs-lookup"><span data-stu-id="c3012-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="c3012-3877">Conforme especificado na seção 3.1.5.2.8, essa mensagem é enviada após cada mensagem de CPMFetchValueIn até que todos os bytes da propriedade sejam transferidos.</span><span class="sxs-lookup"><span data-stu-id="c3012-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="c3012-3878">O formato da mensagem CPMFetchValueOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-3879">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3879">0</span></span>

<span data-ttu-id="c3012-3880">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3880">1</span></span>

<span data-ttu-id="c3012-3881">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3881">2</span></span>

<span data-ttu-id="c3012-3882">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3882">3</span></span>

<span data-ttu-id="c3012-3883">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3883">4</span></span>

<span data-ttu-id="c3012-3884">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3884">5</span></span>

<span data-ttu-id="c3012-3885">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3885">6</span></span>

<span data-ttu-id="c3012-3886">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3886">7</span></span>

<span data-ttu-id="c3012-3887">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3887">8</span></span>

<span data-ttu-id="c3012-3888">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3888">9</span></span>

<span data-ttu-id="c3012-3889">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3889">1</span></span><br/> <span data-ttu-id="c3012-3890">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3890">0</span></span><br/>

<span data-ttu-id="c3012-3891">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3891">1</span></span>

<span data-ttu-id="c3012-3892">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3892">2</span></span>

<span data-ttu-id="c3012-3893">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3893">3</span></span>

<span data-ttu-id="c3012-3894">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3894">4</span></span>

<span data-ttu-id="c3012-3895">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3895">5</span></span>

<span data-ttu-id="c3012-3896">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3896">6</span></span>

<span data-ttu-id="c3012-3897">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3897">7</span></span>

<span data-ttu-id="c3012-3898">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3898">8</span></span>

<span data-ttu-id="c3012-3899">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3899">9</span></span>

<span data-ttu-id="c3012-3900">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3900">2</span></span><br/> <span data-ttu-id="c3012-3901">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3901">0</span></span><br/>

<span data-ttu-id="c3012-3902">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3902">1</span></span>

<span data-ttu-id="c3012-3903">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3903">2</span></span>

<span data-ttu-id="c3012-3904">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3904">3</span></span>

<span data-ttu-id="c3012-3905">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3905">4</span></span>

<span data-ttu-id="c3012-3906">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3906">5</span></span>

<span data-ttu-id="c3012-3907">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3907">6</span></span>

<span data-ttu-id="c3012-3908">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3908">7</span></span>

<span data-ttu-id="c3012-3909">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3909">8</span></span>

<span data-ttu-id="c3012-3910">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3910">9</span></span>

<span data-ttu-id="c3012-3911">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3911">3</span></span><br/> <span data-ttu-id="c3012-3912">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3912">0</span></span><br/>

<span data-ttu-id="c3012-3913">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3913">1</span></span>

<span data-ttu-id="c3012-3914">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="c3012-3914">\_cbValue</span></span>

<span data-ttu-id="c3012-3915">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="c3012-3915">\_fMoreExists</span></span>

<span data-ttu-id="c3012-3916">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="c3012-3916">\_fValueExists</span></span>

<span data-ttu-id="c3012-3917">vType</span><span class="sxs-lookup"><span data-stu-id="c3012-3917">vType</span></span>

<span data-ttu-id="c3012-3918">vValue (variável)</span><span class="sxs-lookup"><span data-stu-id="c3012-3918">vValue (variable)</span></span>



 

<span data-ttu-id="c3012-3919">**\_ cbValue**: um inteiro sem sinal de 32 bits contendo o tamanho total, em bytes em vValue.</span><span class="sxs-lookup"><span data-stu-id="c3012-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="c3012-3920">**\_ fMoreExists**: um valor booliano que indica se há mensagens CPMFetchValueOut adicionais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c3012-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="c3012-3921">Se definido como 0x00000001, há mensagens CPMFetchValueOut adicionais.</span><span class="sxs-lookup"><span data-stu-id="c3012-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="c3012-3922">Se definido como 0x00000000, não há nenhuma mensagem CPMFetchValueOut adicional disponível.</span><span class="sxs-lookup"><span data-stu-id="c3012-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="c3012-3923">**\_ fValueExists**: um valor booliano que indica se há um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="c3012-3924">Se definido como 0x00000001, um valor para a propriedade existirá.</span><span class="sxs-lookup"><span data-stu-id="c3012-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="c3012-3925">Se definido como 0x00000000, um valor para a propriedade não existe.</span><span class="sxs-lookup"><span data-stu-id="c3012-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="c3012-3926">**vType**: um valor da enumeração VarEnum, consulte a seção 2.2.1.1 para obter detalhes, descrevendo o tipo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="c3012-3927">**vValue**: uma parte de uma matriz de bytes que contém uma estrutura SERIALIZEDPROPERTYVALUE, conforme especificado na seção 2.2.1.32, em que o deslocamento do início da parte é o valor de \_ cbSoFar em CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="c3012-3928">O comprimento da parte, indicado pelo \_ campo cbValue, deve ser igual ao valor de \_ CbChunk em CPMFetchValueIn se \_ fMoreExists for definido como 0x00000001 e deve ser menor ou igual ao valor de \_ cbChunk caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c3012-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="c3012-3929">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="c3012-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="c3012-3930">A mensagem CPMGetNotify solicita que o cliente seja notificado das alterações de conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="c3012-3931">A mensagem não deve incluir um corpo; somente o cabeçalho da mensagem, conforme especificado na seção 2.2.2, deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="c3012-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="c3012-3932">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="c3012-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="c3012-3933">A mensagem CPMSendNotifyOut notifica o cliente sobre uma alteração nos resultados de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="c3012-3934">Essa mensagem é enviada somente quando ocorre uma alteração.</span><span class="sxs-lookup"><span data-stu-id="c3012-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="c3012-3935">O formato da mensagem CPMSendNotifyOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-3936">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3936">0</span></span>

<span data-ttu-id="c3012-3937">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3937">1</span></span>

<span data-ttu-id="c3012-3938">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3938">2</span></span>

<span data-ttu-id="c3012-3939">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3939">3</span></span>

<span data-ttu-id="c3012-3940">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3940">4</span></span>

<span data-ttu-id="c3012-3941">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3941">5</span></span>

<span data-ttu-id="c3012-3942">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3942">6</span></span>

<span data-ttu-id="c3012-3943">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3943">7</span></span>

<span data-ttu-id="c3012-3944">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3944">8</span></span>

<span data-ttu-id="c3012-3945">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3945">9</span></span>

<span data-ttu-id="c3012-3946">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3946">1</span></span><br/> <span data-ttu-id="c3012-3947">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3947">0</span></span><br/>

<span data-ttu-id="c3012-3948">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3948">1</span></span>

<span data-ttu-id="c3012-3949">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3949">2</span></span>

<span data-ttu-id="c3012-3950">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3950">3</span></span>

<span data-ttu-id="c3012-3951">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3951">4</span></span>

<span data-ttu-id="c3012-3952">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3952">5</span></span>

<span data-ttu-id="c3012-3953">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3953">6</span></span>

<span data-ttu-id="c3012-3954">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3954">7</span></span>

<span data-ttu-id="c3012-3955">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3955">8</span></span>

<span data-ttu-id="c3012-3956">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3956">9</span></span>

<span data-ttu-id="c3012-3957">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3957">2</span></span><br/> <span data-ttu-id="c3012-3958">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3958">0</span></span><br/>

<span data-ttu-id="c3012-3959">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3959">1</span></span>

<span data-ttu-id="c3012-3960">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3960">2</span></span>

<span data-ttu-id="c3012-3961">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3961">3</span></span>

<span data-ttu-id="c3012-3962">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3962">4</span></span>

<span data-ttu-id="c3012-3963">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3963">5</span></span>

<span data-ttu-id="c3012-3964">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3964">6</span></span>

<span data-ttu-id="c3012-3965">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3965">7</span></span>

<span data-ttu-id="c3012-3966">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3966">8</span></span>

<span data-ttu-id="c3012-3967">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3967">9</span></span>

<span data-ttu-id="c3012-3968">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3968">3</span></span><br/> <span data-ttu-id="c3012-3969">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3969">0</span></span><br/>

<span data-ttu-id="c3012-3970">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3970">1</span></span>

<span data-ttu-id="c3012-3971">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="c3012-3971">\_watchNotify</span></span>



 

<span data-ttu-id="c3012-3972">**\_ watchNotify**: a alteração para a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="c3012-3973">DEVE ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c3012-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="c3012-3974">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-3974">Value</span></span>                                     | <span data-ttu-id="c3012-3975">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c3012-3976">DBWATCHNOTIFY \_ linhaschanged 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="c3012-3977">O número de linhas no conjunto de linhas de consulta foi alterado.</span><span class="sxs-lookup"><span data-stu-id="c3012-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="c3012-3978">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="c3012-3979">A consulta foi concluída.</span><span class="sxs-lookup"><span data-stu-id="c3012-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="c3012-3980">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="c3012-3981">A consulta foi executada novamente.</span><span class="sxs-lookup"><span data-stu-id="c3012-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="c3012-3982">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="c3012-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="c3012-3983">A mensagem CPMGetApproximatePositionIn solicita a posição aproximada de um indicador em um capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="c3012-3984">O formato da mensagem CPMGetApproximatePositionIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-3985">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3985">0</span></span>

<span data-ttu-id="c3012-3986">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3986">1</span></span>

<span data-ttu-id="c3012-3987">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3987">2</span></span>

<span data-ttu-id="c3012-3988">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3988">3</span></span>

<span data-ttu-id="c3012-3989">4</span><span class="sxs-lookup"><span data-stu-id="c3012-3989">4</span></span>

<span data-ttu-id="c3012-3990">5</span><span class="sxs-lookup"><span data-stu-id="c3012-3990">5</span></span>

<span data-ttu-id="c3012-3991">6</span><span class="sxs-lookup"><span data-stu-id="c3012-3991">6</span></span>

<span data-ttu-id="c3012-3992">7</span><span class="sxs-lookup"><span data-stu-id="c3012-3992">7</span></span>

<span data-ttu-id="c3012-3993">8</span><span class="sxs-lookup"><span data-stu-id="c3012-3993">8</span></span>

<span data-ttu-id="c3012-3994">9</span><span class="sxs-lookup"><span data-stu-id="c3012-3994">9</span></span>

<span data-ttu-id="c3012-3995">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3995">1</span></span><br/> <span data-ttu-id="c3012-3996">0</span><span class="sxs-lookup"><span data-stu-id="c3012-3996">0</span></span><br/>

<span data-ttu-id="c3012-3997">1</span><span class="sxs-lookup"><span data-stu-id="c3012-3997">1</span></span>

<span data-ttu-id="c3012-3998">2</span><span class="sxs-lookup"><span data-stu-id="c3012-3998">2</span></span>

<span data-ttu-id="c3012-3999">3</span><span class="sxs-lookup"><span data-stu-id="c3012-3999">3</span></span>

<span data-ttu-id="c3012-4000">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4000">4</span></span>

<span data-ttu-id="c3012-4001">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4001">5</span></span>

<span data-ttu-id="c3012-4002">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4002">6</span></span>

<span data-ttu-id="c3012-4003">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4003">7</span></span>

<span data-ttu-id="c3012-4004">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4004">8</span></span>

<span data-ttu-id="c3012-4005">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4005">9</span></span>

<span data-ttu-id="c3012-4006">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4006">2</span></span><br/> <span data-ttu-id="c3012-4007">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4007">0</span></span><br/>

<span data-ttu-id="c3012-4008">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4008">1</span></span>

<span data-ttu-id="c3012-4009">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4009">2</span></span>

<span data-ttu-id="c3012-4010">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4010">3</span></span>

<span data-ttu-id="c3012-4011">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4011">4</span></span>

<span data-ttu-id="c3012-4012">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4012">5</span></span>

<span data-ttu-id="c3012-4013">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4013">6</span></span>

<span data-ttu-id="c3012-4014">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4014">7</span></span>

<span data-ttu-id="c3012-4015">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4015">8</span></span>

<span data-ttu-id="c3012-4016">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4016">9</span></span>

<span data-ttu-id="c3012-4017">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4017">3</span></span><br/> <span data-ttu-id="c3012-4018">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4018">0</span></span><br/>

<span data-ttu-id="c3012-4019">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4019">1</span></span>

<span data-ttu-id="c3012-4020">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3012-4020">\_hCursor</span></span>

<span data-ttu-id="c3012-4021">\_chapt</span><span class="sxs-lookup"><span data-stu-id="c3012-4021">\_chapt</span></span>

<span data-ttu-id="c3012-4022">\_bmk</span><span class="sxs-lookup"><span data-stu-id="c3012-4022">\_bmk</span></span>



 

<span data-ttu-id="c3012-4023">**\_ hCursor**: um valor de 32 bits que representa o cursor de consulta obtido de CPMCreateQueryOut para o conjunto de linhas que contém o indicador.</span><span class="sxs-lookup"><span data-stu-id="c3012-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="c3012-4024">**\_ chapt**: um valor de 32 bits que representa o identificador para o capítulo que contém o indicador.</span><span class="sxs-lookup"><span data-stu-id="c3012-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="c3012-4025">**\_ BMK**: um valor de 32 bits que representa o identificador para o indicador para o qual recuperar a posição aproximada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="c3012-4026">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="c3012-4027">A mensagem CPMGetApproximatePositionOut responde a uma mensagem CPMGetApproximatePositionIn que descreve a posição aproximada do indicador no capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="c3012-4028">O formato da mensagem CPMGetApproximatePositionOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-4029">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4029">0</span></span>

<span data-ttu-id="c3012-4030">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4030">1</span></span>

<span data-ttu-id="c3012-4031">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4031">2</span></span>

<span data-ttu-id="c3012-4032">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4032">3</span></span>

<span data-ttu-id="c3012-4033">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4033">4</span></span>

<span data-ttu-id="c3012-4034">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4034">5</span></span>

<span data-ttu-id="c3012-4035">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4035">6</span></span>

<span data-ttu-id="c3012-4036">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4036">7</span></span>

<span data-ttu-id="c3012-4037">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4037">8</span></span>

<span data-ttu-id="c3012-4038">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4038">9</span></span>

<span data-ttu-id="c3012-4039">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4039">1</span></span><br/> <span data-ttu-id="c3012-4040">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4040">0</span></span><br/>

<span data-ttu-id="c3012-4041">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4041">1</span></span>

<span data-ttu-id="c3012-4042">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4042">2</span></span>

<span data-ttu-id="c3012-4043">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4043">3</span></span>

<span data-ttu-id="c3012-4044">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4044">4</span></span>

<span data-ttu-id="c3012-4045">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4045">5</span></span>

<span data-ttu-id="c3012-4046">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4046">6</span></span>

<span data-ttu-id="c3012-4047">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4047">7</span></span>

<span data-ttu-id="c3012-4048">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4048">8</span></span>

<span data-ttu-id="c3012-4049">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4049">9</span></span>

<span data-ttu-id="c3012-4050">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4050">2</span></span><br/> <span data-ttu-id="c3012-4051">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4051">0</span></span><br/>

<span data-ttu-id="c3012-4052">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4052">1</span></span>

<span data-ttu-id="c3012-4053">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4053">2</span></span>

<span data-ttu-id="c3012-4054">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4054">3</span></span>

<span data-ttu-id="c3012-4055">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4055">4</span></span>

<span data-ttu-id="c3012-4056">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4056">5</span></span>

<span data-ttu-id="c3012-4057">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4057">6</span></span>

<span data-ttu-id="c3012-4058">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4058">7</span></span>

<span data-ttu-id="c3012-4059">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4059">8</span></span>

<span data-ttu-id="c3012-4060">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4060">9</span></span>

<span data-ttu-id="c3012-4061">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4061">3</span></span><br/> <span data-ttu-id="c3012-4062">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4062">0</span></span><br/>

<span data-ttu-id="c3012-4063">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4063">1</span></span>

<span data-ttu-id="c3012-4064">\_numerator</span><span class="sxs-lookup"><span data-stu-id="c3012-4064">\_numerator</span></span>

<span data-ttu-id="c3012-4065">\_denominator</span><span class="sxs-lookup"><span data-stu-id="c3012-4065">\_denominator</span></span>



 

<span data-ttu-id="c3012-4066">**\_ numerador**: um inteiro de 32 bits sem sinal contendo o número de linha do indicador no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="c3012-4067">Se não houver linhas, esse campo deverá ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="c3012-4068">**\_ denominador**: um inteiro sem sinal de 32 bits contendo o número de linhas no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="c3012-4069">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="c3012-4070">A mensagem CPMCompareBmkIn solicita uma comparação de dois indicadores em um capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="c3012-4071">O formato da mensagem CPMCompareBmkIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-4072">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4072">0</span></span>

<span data-ttu-id="c3012-4073">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4073">1</span></span>

<span data-ttu-id="c3012-4074">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4074">2</span></span>

<span data-ttu-id="c3012-4075">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4075">3</span></span>

<span data-ttu-id="c3012-4076">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4076">4</span></span>

<span data-ttu-id="c3012-4077">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4077">5</span></span>

<span data-ttu-id="c3012-4078">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4078">6</span></span>

<span data-ttu-id="c3012-4079">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4079">7</span></span>

<span data-ttu-id="c3012-4080">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4080">8</span></span>

<span data-ttu-id="c3012-4081">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4081">9</span></span>

<span data-ttu-id="c3012-4082">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4082">1</span></span><br/> <span data-ttu-id="c3012-4083">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4083">0</span></span><br/>

<span data-ttu-id="c3012-4084">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4084">1</span></span>

<span data-ttu-id="c3012-4085">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4085">2</span></span>

<span data-ttu-id="c3012-4086">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4086">3</span></span>

<span data-ttu-id="c3012-4087">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4087">4</span></span>

<span data-ttu-id="c3012-4088">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4088">5</span></span>

<span data-ttu-id="c3012-4089">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4089">6</span></span>

<span data-ttu-id="c3012-4090">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4090">7</span></span>

<span data-ttu-id="c3012-4091">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4091">8</span></span>

<span data-ttu-id="c3012-4092">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4092">9</span></span>

<span data-ttu-id="c3012-4093">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4093">2</span></span><br/> <span data-ttu-id="c3012-4094">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4094">0</span></span><br/>

<span data-ttu-id="c3012-4095">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4095">1</span></span>

<span data-ttu-id="c3012-4096">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4096">2</span></span>

<span data-ttu-id="c3012-4097">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4097">3</span></span>

<span data-ttu-id="c3012-4098">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4098">4</span></span>

<span data-ttu-id="c3012-4099">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4099">5</span></span>

<span data-ttu-id="c3012-4100">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4100">6</span></span>

<span data-ttu-id="c3012-4101">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4101">7</span></span>

<span data-ttu-id="c3012-4102">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4102">8</span></span>

<span data-ttu-id="c3012-4103">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4103">9</span></span>

<span data-ttu-id="c3012-4104">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4104">3</span></span><br/> <span data-ttu-id="c3012-4105">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4105">0</span></span><br/>

<span data-ttu-id="c3012-4106">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4106">1</span></span>

<span data-ttu-id="c3012-4107">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3012-4107">\_hCursor</span></span>

<span data-ttu-id="c3012-4108">\_chapt</span><span class="sxs-lookup"><span data-stu-id="c3012-4108">\_chapt</span></span>

<span data-ttu-id="c3012-4109">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="c3012-4109">\_bmkFirst</span></span>

<span data-ttu-id="c3012-4110">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="c3012-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="c3012-4111">\_**hCursor**: um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut para o conjunto de linhas que contém os indicadores.</span><span class="sxs-lookup"><span data-stu-id="c3012-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="c3012-4112">\_**chapt**: um valor de 32 bits que representa o identificador do capítulo que contém os indicadores a serem comparados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="c3012-4113">\_**bmkFirst**: um valor de 32 bits que representa o identificador para o primeiro indicador a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="c3012-4114">\_**bmkSecond**: um valor de 32 bits que representa o identificador para o segundo indicador a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="c3012-4115">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="c3012-4116">A mensagem CPMCompareBmkOut responde a uma mensagem CPMCompareBmkIn com a comparação dos dois indicadores no capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="c3012-4117">O formato da mensagem CPMCompareBmkOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-4118">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4118">0</span></span>

<span data-ttu-id="c3012-4119">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4119">1</span></span>

<span data-ttu-id="c3012-4120">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4120">2</span></span>

<span data-ttu-id="c3012-4121">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4121">3</span></span>

<span data-ttu-id="c3012-4122">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4122">4</span></span>

<span data-ttu-id="c3012-4123">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4123">5</span></span>

<span data-ttu-id="c3012-4124">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4124">6</span></span>

<span data-ttu-id="c3012-4125">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4125">7</span></span>

<span data-ttu-id="c3012-4126">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4126">8</span></span>

<span data-ttu-id="c3012-4127">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4127">9</span></span>

<span data-ttu-id="c3012-4128">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4128">1</span></span><br/> <span data-ttu-id="c3012-4129">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4129">0</span></span><br/>

<span data-ttu-id="c3012-4130">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4130">1</span></span>

<span data-ttu-id="c3012-4131">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4131">2</span></span>

<span data-ttu-id="c3012-4132">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4132">3</span></span>

<span data-ttu-id="c3012-4133">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4133">4</span></span>

<span data-ttu-id="c3012-4134">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4134">5</span></span>

<span data-ttu-id="c3012-4135">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4135">6</span></span>

<span data-ttu-id="c3012-4136">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4136">7</span></span>

<span data-ttu-id="c3012-4137">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4137">8</span></span>

<span data-ttu-id="c3012-4138">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4138">9</span></span>

<span data-ttu-id="c3012-4139">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4139">2</span></span><br/> <span data-ttu-id="c3012-4140">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4140">0</span></span><br/>

<span data-ttu-id="c3012-4141">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4141">1</span></span>

<span data-ttu-id="c3012-4142">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4142">2</span></span>

<span data-ttu-id="c3012-4143">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4143">3</span></span>

<span data-ttu-id="c3012-4144">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4144">4</span></span>

<span data-ttu-id="c3012-4145">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4145">5</span></span>

<span data-ttu-id="c3012-4146">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4146">6</span></span>

<span data-ttu-id="c3012-4147">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4147">7</span></span>

<span data-ttu-id="c3012-4148">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4148">8</span></span>

<span data-ttu-id="c3012-4149">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4149">9</span></span>

<span data-ttu-id="c3012-4150">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4150">3</span></span><br/> <span data-ttu-id="c3012-4151">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4151">0</span></span><br/>

<span data-ttu-id="c3012-4152">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4152">1</span></span>

<span data-ttu-id="c3012-4153">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="c3012-4153">\_dwComparison</span></span>



 

<span data-ttu-id="c3012-4154">\_**dwComparison**: um dos valores a seguir, indicando as posições relativas dos dois indicadores no capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="c3012-4155">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-4155">Value</span></span>                               | <span data-ttu-id="c3012-4156">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="c3012-4157">DBCOMPARE \_ lt 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="c3012-4158">O primeiro indicador está posicionado antes do segundo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="c3012-4159">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3012-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="c3012-4160">O primeiro indicador tem a mesma posição que o segundo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="c3012-4161">DBCOMPARE \_ gt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3012-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="c3012-4162">O primeiro indicador é posicionado após o segundo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="c3012-4163">DBCOMPARE \_ ne 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3012-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="c3012-4164">O primeiro indicador não tem a mesma posição que o segundo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="c3012-4165">DBCOMPARE não \_ comparável 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3012-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="c3012-4166">O primeiro indicador não é comparável ao segundo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="c3012-4167">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="c3012-4168">A mensagem CPMRestartPositionIn move a posição de busca para um cursor para o início do capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="c3012-4169">Conforme especificado na seção 3.1.5.2.12, o servidor responderá usando a mesma mensagem, com os resultados da solicitação contida no \_ campo status do cabeçalho CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="c3012-4170">O formato da mensagem CPMRestartPositionIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-4171">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4171">0</span></span>

<span data-ttu-id="c3012-4172">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4172">1</span></span>

<span data-ttu-id="c3012-4173">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4173">2</span></span>

<span data-ttu-id="c3012-4174">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4174">3</span></span>

<span data-ttu-id="c3012-4175">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4175">4</span></span>

<span data-ttu-id="c3012-4176">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4176">5</span></span>

<span data-ttu-id="c3012-4177">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4177">6</span></span>

<span data-ttu-id="c3012-4178">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4178">7</span></span>

<span data-ttu-id="c3012-4179">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4179">8</span></span>

<span data-ttu-id="c3012-4180">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4180">9</span></span>

<span data-ttu-id="c3012-4181">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4181">1</span></span><br/> <span data-ttu-id="c3012-4182">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4182">0</span></span><br/>

<span data-ttu-id="c3012-4183">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4183">1</span></span>

<span data-ttu-id="c3012-4184">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4184">2</span></span>

<span data-ttu-id="c3012-4185">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4185">3</span></span>

<span data-ttu-id="c3012-4186">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4186">4</span></span>

<span data-ttu-id="c3012-4187">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4187">5</span></span>

<span data-ttu-id="c3012-4188">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4188">6</span></span>

<span data-ttu-id="c3012-4189">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4189">7</span></span>

<span data-ttu-id="c3012-4190">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4190">8</span></span>

<span data-ttu-id="c3012-4191">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4191">9</span></span>

<span data-ttu-id="c3012-4192">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4192">2</span></span><br/> <span data-ttu-id="c3012-4193">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4193">0</span></span><br/>

<span data-ttu-id="c3012-4194">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4194">1</span></span>

<span data-ttu-id="c3012-4195">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4195">2</span></span>

<span data-ttu-id="c3012-4196">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4196">3</span></span>

<span data-ttu-id="c3012-4197">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4197">4</span></span>

<span data-ttu-id="c3012-4198">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4198">5</span></span>

<span data-ttu-id="c3012-4199">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4199">6</span></span>

<span data-ttu-id="c3012-4200">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4200">7</span></span>

<span data-ttu-id="c3012-4201">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4201">8</span></span>

<span data-ttu-id="c3012-4202">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4202">9</span></span>

<span data-ttu-id="c3012-4203">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4203">3</span></span><br/> <span data-ttu-id="c3012-4204">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4204">0</span></span><br/>

<span data-ttu-id="c3012-4205">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4205">1</span></span>

<span data-ttu-id="c3012-4206">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="c3012-4207">\_chapt (opcional)</span><span class="sxs-lookup"><span data-stu-id="c3012-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="c3012-4208">**\_ hCursor**: um valor de 32 bits que representa o identificador, obtido de uma mensagem CPMCreateQueryOut, que identifica a consulta para a qual a posição deve ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="c3012-4209">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3012-4210">**\_ chapt**: um valor de 32 bits que representa o identificador de um capítulo do qual recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="c3012-4211">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="c3012-4212">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="c3012-4213">A mensagem CPMFreeCursorIn solicita o lançamento de um cursor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="c3012-4214">O formato da mensagem CPMFreeCursorIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="c3012-4215">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4215">0</span></span>

<span data-ttu-id="c3012-4216">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4216">1</span></span>

<span data-ttu-id="c3012-4217">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4217">2</span></span>

<span data-ttu-id="c3012-4218">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4218">3</span></span>

<span data-ttu-id="c3012-4219">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4219">4</span></span>

<span data-ttu-id="c3012-4220">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4220">5</span></span>

<span data-ttu-id="c3012-4221">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4221">6</span></span>

<span data-ttu-id="c3012-4222">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4222">7</span></span>

<span data-ttu-id="c3012-4223">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4223">8</span></span>

<span data-ttu-id="c3012-4224">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4224">9</span></span>

<span data-ttu-id="c3012-4225">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4225">1</span></span><br/> <span data-ttu-id="c3012-4226">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4226">0</span></span><br/>

<span data-ttu-id="c3012-4227">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4227">1</span></span>

<span data-ttu-id="c3012-4228">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4228">2</span></span>

<span data-ttu-id="c3012-4229">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4229">3</span></span>

<span data-ttu-id="c3012-4230">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4230">4</span></span>

<span data-ttu-id="c3012-4231">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4231">5</span></span>

<span data-ttu-id="c3012-4232">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4232">6</span></span>

<span data-ttu-id="c3012-4233">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4233">7</span></span>

<span data-ttu-id="c3012-4234">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4234">8</span></span>

<span data-ttu-id="c3012-4235">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4235">9</span></span>

<span data-ttu-id="c3012-4236">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4236">2</span></span><br/> <span data-ttu-id="c3012-4237">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4237">0</span></span><br/>

<span data-ttu-id="c3012-4238">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4238">1</span></span>

<span data-ttu-id="c3012-4239">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4239">2</span></span>

<span data-ttu-id="c3012-4240">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4240">3</span></span>

<span data-ttu-id="c3012-4241">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4241">4</span></span>

<span data-ttu-id="c3012-4242">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4242">5</span></span>

<span data-ttu-id="c3012-4243">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4243">6</span></span>

<span data-ttu-id="c3012-4244">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4244">7</span></span>

<span data-ttu-id="c3012-4245">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4245">8</span></span>

<span data-ttu-id="c3012-4246">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4246">9</span></span>

<span data-ttu-id="c3012-4247">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4247">3</span></span><br/> <span data-ttu-id="c3012-4248">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4248">0</span></span><br/>

<span data-ttu-id="c3012-4249">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4249">1</span></span>

<span data-ttu-id="c3012-4250">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3012-4250">\_hCursor</span></span>



 

<span data-ttu-id="c3012-4251">**\_ hCursor**: um valor de 32 bits que representa o identificador do cursor a partir da mensagem CPMCreateQueryOut a ser liberada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="c3012-4252">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="c3012-4253">A mensagem CPMFreeCursorOut responde a uma mensagem CPMFreeCursorIn com os resultados de liberar um cursor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="c3012-4254">O formato da mensagem CPMFreeCursorOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="c3012-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="c3012-4255">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4255">0</span></span>

<span data-ttu-id="c3012-4256">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4256">1</span></span>

<span data-ttu-id="c3012-4257">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4257">2</span></span>

<span data-ttu-id="c3012-4258">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4258">3</span></span>

<span data-ttu-id="c3012-4259">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4259">4</span></span>

<span data-ttu-id="c3012-4260">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4260">5</span></span>

<span data-ttu-id="c3012-4261">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4261">6</span></span>

<span data-ttu-id="c3012-4262">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4262">7</span></span>

<span data-ttu-id="c3012-4263">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4263">8</span></span>

<span data-ttu-id="c3012-4264">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4264">9</span></span>

<span data-ttu-id="c3012-4265">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4265">1</span></span><br/> <span data-ttu-id="c3012-4266">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4266">0</span></span><br/>

<span data-ttu-id="c3012-4267">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4267">1</span></span>

<span data-ttu-id="c3012-4268">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4268">2</span></span>

<span data-ttu-id="c3012-4269">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4269">3</span></span>

<span data-ttu-id="c3012-4270">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4270">4</span></span>

<span data-ttu-id="c3012-4271">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4271">5</span></span>

<span data-ttu-id="c3012-4272">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4272">6</span></span>

<span data-ttu-id="c3012-4273">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4273">7</span></span>

<span data-ttu-id="c3012-4274">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4274">8</span></span>

<span data-ttu-id="c3012-4275">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4275">9</span></span>

<span data-ttu-id="c3012-4276">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4276">2</span></span><br/> <span data-ttu-id="c3012-4277">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4277">0</span></span><br/>

<span data-ttu-id="c3012-4278">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4278">1</span></span>

<span data-ttu-id="c3012-4279">2</span><span class="sxs-lookup"><span data-stu-id="c3012-4279">2</span></span>

<span data-ttu-id="c3012-4280">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4280">3</span></span>

<span data-ttu-id="c3012-4281">4</span><span class="sxs-lookup"><span data-stu-id="c3012-4281">4</span></span>

<span data-ttu-id="c3012-4282">5</span><span class="sxs-lookup"><span data-stu-id="c3012-4282">5</span></span>

<span data-ttu-id="c3012-4283">6</span><span class="sxs-lookup"><span data-stu-id="c3012-4283">6</span></span>

<span data-ttu-id="c3012-4284">7</span><span class="sxs-lookup"><span data-stu-id="c3012-4284">7</span></span>

<span data-ttu-id="c3012-4285">8</span><span class="sxs-lookup"><span data-stu-id="c3012-4285">8</span></span>

<span data-ttu-id="c3012-4286">9</span><span class="sxs-lookup"><span data-stu-id="c3012-4286">9</span></span>

<span data-ttu-id="c3012-4287">3</span><span class="sxs-lookup"><span data-stu-id="c3012-4287">3</span></span><br/> <span data-ttu-id="c3012-4288">0</span><span class="sxs-lookup"><span data-stu-id="c3012-4288">0</span></span><br/>

<span data-ttu-id="c3012-4289">1</span><span class="sxs-lookup"><span data-stu-id="c3012-4289">1</span></span>

<span data-ttu-id="c3012-4290">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="c3012-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="c3012-4291">**\_ cCursorsRemaining**: um inteiro de 32 bits sem sinal indicando o número de cursores que ainda estão em uso para a consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="c3012-4292">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="c3012-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="c3012-4293">A mensagem CPMDisconnect finaliza a conexão com o servidor</span><span class="sxs-lookup"><span data-stu-id="c3012-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="c3012-4294">A mensagem não deve incluir um corpo; somente o cabeçalho da mensagem, conforme especificado na seção 2.2.2, deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="c3012-4295">erros de 2.2.4</span><span class="sxs-lookup"><span data-stu-id="c3012-4295">2.2.4 Errors</span></span>

<span data-ttu-id="c3012-4296">Todas as mensagens do protocolo de serviço de indexação de conteúdo devem retornar 0x00000000 em caso de sucesso; caso contrário, eles retornam um código de erro de 32 bits diferente de zero, que pode ser um valor HRESULT ou NTSTATUS (consulte a seção 1,8).</span><span class="sxs-lookup"><span data-stu-id="c3012-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="c3012-4297">Se um buffer for muito pequeno para se ajustar a um resultado, um código de status de STATUS \_ insuficiente de \_ recursos (0XC0000009A) deverá ser retornado e a operação com falha deverá ser repetida com um buffer maior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="c3012-4298">Todos os outros valores de erro devem ser tratados da mesma.</span><span class="sxs-lookup"><span data-stu-id="c3012-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="c3012-4299">(Observe que, no momento, os espaços de numeração HRESULT e NTSTATUS não se sobrepõem, exceto com valores de significado idêntico, mas mesmo que eles tenham que estar em conflito no futuro, isso não causaria nenhum problema de protocolo, contanto que o valor do STATUS \_ Recursos insuficientes \_ permanecem exclusivos, pois todos os outros valores de erro são tratados da mesma maneira.)</span><span class="sxs-lookup"><span data-stu-id="c3012-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="c3012-4300">3 Detalhes do protocolo</span><span class="sxs-lookup"><span data-stu-id="c3012-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="c3012-4301">3,1 detalhes do servidor</span><span class="sxs-lookup"><span data-stu-id="c3012-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="c3012-4302">3,2 detalhes do cliente</span><span class="sxs-lookup"><span data-stu-id="c3012-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="c3012-4303">Solicitações de mensagens CISP para consultar remotamente os catálogos de serviço de indexação não exigem nenhuma sequência específica.</span><span class="sxs-lookup"><span data-stu-id="c3012-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="c3012-4304">É recomendável que a camada mais alta obedeça a uma sequência de mensagens significativa, no entanto, para mensagens recebidas dessa sequência ou com dados inválidos, o servidor responderá com um erro.</span><span class="sxs-lookup"><span data-stu-id="c3012-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="c3012-4305">Algumas mensagens também dependem da camada superior, fornecendo dados válidos que foram recebidos nas mensagens anteriores na sequência.</span><span class="sxs-lookup"><span data-stu-id="c3012-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="c3012-4306">Uma sequência de mensagens típica para uma consulta simples de um cliente para um computador remoto é ilustrada no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3012-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![sequência de mensagens para consulta simples](images/protocoldetails.jpg)

<span data-ttu-id="c3012-4308">As mensagens representadas no diagrama anterior representam um subconjunto de todas as mensagens CISP usadas para consultar um catálogo de serviço de indexação remota.</span><span class="sxs-lookup"><span data-stu-id="c3012-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="c3012-4309">3,1 detalhes do servidor</span><span class="sxs-lookup"><span data-stu-id="c3012-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="c3012-4310">3.1.1 Modelo de dados abstratos</span><span class="sxs-lookup"><span data-stu-id="c3012-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="c3012-4311">A seção a seguir especifica os dados e o estado mantidos pelo servidor CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="c3012-4312">Os dados fornecidos aqui são para facilitar a explicação de como o protocolo se comporta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="c3012-4313">Esta seção não exige que as implementações sigam esse modelo, desde que seu comportamento externo seja consistente com o descrito neste documento.</span><span class="sxs-lookup"><span data-stu-id="c3012-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="c3012-4314">Um serviço de indexação que implementa o CISP deve manter os seguintes elementos de dados abstratos:</span><span class="sxs-lookup"><span data-stu-id="c3012-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="c3012-4315">A lista de clientes conectados ao servidor</span><span class="sxs-lookup"><span data-stu-id="c3012-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="c3012-4316">Informações sobre cada cliente, que inclui:</span><span class="sxs-lookup"><span data-stu-id="c3012-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="c3012-4317">Versão do cliente (conforme indicado na mensagem CPMConnectIn especificada na seção 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="c3012-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="c3012-4318">Catálogo associado ao cliente (por uma mensagem CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="c3012-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="c3012-4319">Propriedades de cliente adicionais, conforme especificado na seção 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="c3012-4320">Consulta de pesquisa do cliente</span><span class="sxs-lookup"><span data-stu-id="c3012-4320">Client's search query</span></span>
    -   <span data-ttu-id="c3012-4321">Lista de identificadores de cursor para a consulta e a posição no conjunto de resultados para cada identificador.</span><span class="sxs-lookup"><span data-stu-id="c3012-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="c3012-4322">Conjunto atual de associações</span><span class="sxs-lookup"><span data-stu-id="c3012-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="c3012-4323">Status atual da consulta que inclui (para cada cursor):</span><span class="sxs-lookup"><span data-stu-id="c3012-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="c3012-4324">Número de linhas no resultado da consulta</span><span class="sxs-lookup"><span data-stu-id="c3012-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="c3012-4325">Numerador e denominador da conclusão da consulta</span><span class="sxs-lookup"><span data-stu-id="c3012-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="c3012-4326">Último número de linhas, relatadas pela mensagem CPMRatioFinishedOut mais recente para este cursor</span><span class="sxs-lookup"><span data-stu-id="c3012-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="c3012-4327">Se a consulta é monitorada pelo servidor para alterações nos resultados da consulta e se ela é monitorada, o que mudou nos resultados da consulta desde que ele foi relatado pela última vez no cliente por CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="c3012-4328">A lista de capítulos manipula, servida por essa consulta, um cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="c3012-4329">Lista de identificadores de indicadores para cada cursor, servidas por essa consulta a um cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="c3012-4330">O estado atual do serviço de indexação, que pode ser "não inicializado", "em execução" ou "desligando".</span><span class="sxs-lookup"><span data-stu-id="c3012-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="c3012-4331">Observe que a maior parte do servidor de horário está no estado "em execução".</span><span class="sxs-lookup"><span data-stu-id="c3012-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="c3012-4332">A seguir está o diagrama de máquina de estado para o servidor:</span><span class="sxs-lookup"><span data-stu-id="c3012-4332">Following is the state machine diagram for the server:</span></span>

    ![diagrama de máquina de estado do servidor de serviço de indexação](images/abstractdatamodel.jpg)

-   <span data-ttu-id="c3012-4334">Informações por catálogo: número de documentos indexados, tamanho do índice, número de chaves exclusivas, etc (consulte a seção 2.2.3.1 para obter a lista completa), estado (que corresponde aos valores de dwNewState na seção 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="c3012-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="c3012-4335">Para cada idioma com suporte, um banco de dados de variações de palavras, conforme discutido na seção 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="c3012-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="c3012-4336">3.1.2 Temporizadores</span><span class="sxs-lookup"><span data-stu-id="c3012-4336">3.1.2 Timers</span></span>

<span data-ttu-id="c3012-4337">Nenhum temporizador de protocolo é necessário.</span><span class="sxs-lookup"><span data-stu-id="c3012-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="c3012-4338">3.1.3 Inicialização</span><span class="sxs-lookup"><span data-stu-id="c3012-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="c3012-4339">Na inicialização, o servidor deve definir seu estado como "não inicializado" e começar a escutar mensagens no pipe nomeado especificado na seção 1,9.</span><span class="sxs-lookup"><span data-stu-id="c3012-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="c3012-4340">Depois de fazer qualquer outra inicialização interna, ela deve fazer a transição para o estado "em execução".</span><span class="sxs-lookup"><span data-stu-id="c3012-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="c3012-4341">3.1.4 Eventos disparados de camada superior</span><span class="sxs-lookup"><span data-stu-id="c3012-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="c3012-4342">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c3012-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="c3012-4343">Processamento de mensagens 3.1.5 e regras de sequenciamento</span><span class="sxs-lookup"><span data-stu-id="c3012-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="c3012-4344">Sempre que ocorrer um erro durante o processamento de uma mensagem enviada por um cliente, o servidor deverá relatar um erro de volta ao cliente da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="c3012-4345">Parar o processamento da mensagem enviada pelo cliente</span><span class="sxs-lookup"><span data-stu-id="c3012-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="c3012-4346">Responda com o cabeçalho da mensagem (somente) da mensagem enviada pelo cliente, mantendo o \_ campo msg intacto.</span><span class="sxs-lookup"><span data-stu-id="c3012-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="c3012-4347">Defina o \_ campo status para o valor do código de erro.</span><span class="sxs-lookup"><span data-stu-id="c3012-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="c3012-4348">Quando uma mensagem chega, o servidor deve verificar o \_ valor do campo msg para ver se ele é um tipo conhecido (consulte a seção 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="c3012-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="c3012-4349">Se o tipo não for conhecido, ele deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="c3012-4350">O servidor deve validar o \_ valor do campo ulChecksum se o tipo de mensagem for um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="c3012-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="c3012-4351">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="c3012-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="c3012-4352">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="c3012-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="c3012-4353">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="c3012-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="c3012-4354">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="c3012-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="c3012-4355">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="c3012-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="c3012-4356">Para validar o \_ valor do campo ulChecksum, o servidor deve verificar o valor especificado pelo cliente no \_ campo iClientVersion da mensagem CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="c3012-4357">Se o \_ campo iClientVersion não estiver definido como 0x00000008 e o \_ campo ulChecksum não estiver definido como 0x00000000, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="c3012-4358">O servidor não deve validar o \_ campo ulChecksum para clientes defina o \_ campo iClientVersion com um valor menor que 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="c3012-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="c3012-4359">Se o \_ valor do campo iClientVersionfield for 0x00000008 ou superior, o servidor deverá validar que o \_ campo ulChecksum foi calculado conforme especificado na seção 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="c3012-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="c3012-4360">Se o \_ valor de ulChecksum for inválido, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0XC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="c3012-4361">Em seguida, o servidor verifica em qual estado ele está.</span><span class="sxs-lookup"><span data-stu-id="c3012-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="c3012-4362">Se seu estado for "não inicializado", o servidor deverá relatar \_ um \_ erro CI E não \_ inicializado (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="c3012-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="c3012-4363">Se o estado for "desligando", o servidor deverá relatar \_ um \_ erro de desligamento CI E Shutdown (0x80041812).</span><span class="sxs-lookup"><span data-stu-id="c3012-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="c3012-4364">Depois que um cabeçalho for determinado como válido e o servidor estar no estado "em execução", o processamento adicional específico à mensagem deverá ser feito conforme especificado nas subseções abaixo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="c3012-4365">Gerenciamento de catálogo do serviço de indexação remota do 3.1.5.1</span><span class="sxs-lookup"><span data-stu-id="c3012-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="c3012-4366">3.1.5.1.1 recebendo uma solicitação CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="c3012-4367">Quando o servidor recebe uma solicitação de mensagem CPMCIStateInOut do cliente, o servidor deve primeiro verificar se o cliente está em uma lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="c3012-4368">Se o cliente não estiver na lista, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="c3012-4369">Caso contrário, ele deve responder ao cliente com uma mensagem CPMCIStateInOut, preenchendo-o com informações sobre o catálogo associado do cliente, conforme especificado na seção 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="c3012-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="c3012-4370">3.1.5.1.2 recebendo uma solicitação CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="c3012-4371">Quando o servidor recebe uma solicitação de mensagem CPMSetCatStateIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4372">Verifique se o cliente tem acesso administrativo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4372">Check that client has administrative access.</span></span> <span data-ttu-id="c3012-4373">Se o cliente não tiver acesso administrativo, o servidor deverá relatar um erro de STATUS de \_ acesso \_ negado (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="c3012-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="c3012-4374">Se \_ dwNewState não for igual a CICAT \_ todos \_ abertos, altere o estado do catálogo especificado no campo CatName conforme especificado pelo \_ campo dwNewState.</span><span class="sxs-lookup"><span data-stu-id="c3012-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="c3012-4375">Consulte a seção 2.2.3.2 para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="c3012-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="c3012-4376">Se o servidor não localizar um catálogo com o nome especificado no campo CatName, o servidor deverá retornar um \_ erro de parâmetro inválido \_ (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4377">Responda ao cliente com uma mensagem CPMSetCatStateOut, em que \_ DWOLDSTATE deve ser definido como o estado anterior do catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="c3012-4378">Se \_ dwNewState for igual a CICAT \_ todos \_ abertos, o servidor deverá verificar o status de todos os catálogos e, se todos eles forem iniciados, ele deverá definir \_ dwOldState como 0x00000001 e, caso contrário, definirá \_ dwOldState como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="c3012-4379">3.1.5.1.3 recebendo uma solicitação CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="c3012-4380">Quando o servidor recebe uma solicitação de mensagem CPMUpdateDocumentsIn, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4381">Verifique se o cliente está em uma lista de clientes conectados (que têm um catálogo associado).</span><span class="sxs-lookup"><span data-stu-id="c3012-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="c3012-4382">Se o cliente não estiver na lista, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4383">Verifique se o cliente tem acesso administrativo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4383">Check that client has administrative access.</span></span> <span data-ttu-id="c3012-4384">Se o cliente não tiver acesso administrativo ao servidor, o servidor deverá relatar um erro de STATUS de \_ acesso \_ negado (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="c3012-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="c3012-4385">Inicie o processo de indexação do caminho especificado pelo cliente, fazendo uma verificação completa ou incremental, dependendo do valor do \_ campo sinalizador na mensagem CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="c3012-4386">Se o caminho não tiver sido indexado anteriormente, ele deverá ser adicionado à coleção de locais indexados e uma verificação completa realizada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="c3012-4387">Se um valor ilegal do \_ campo flag for especificado, o servidor deverá agir como se o \_ sinalizador fosse definido como UPD \_ init e executar uma verificação completa.</span><span class="sxs-lookup"><span data-stu-id="c3012-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="c3012-4388">Esta operação deve ser executada no catálogo associado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="c3012-4389">Responda ao cliente com o cabeçalho da mensagem para o CPMUpdateDocumentsIn e defina o \_ campo status para os resultados da solicitação.</span><span class="sxs-lookup"><span data-stu-id="c3012-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="c3012-4390">3.1.5.1.4 recebendo uma solicitação CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="c3012-4391">Quando o servidor recebe uma solicitação de mensagem CPMForceMergeIn, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4392">Verifique se o cliente está em uma lista de clientes conectados (que têm um catálogo associado).</span><span class="sxs-lookup"><span data-stu-id="c3012-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="c3012-4393">Se o cliente não estiver na lista, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4394">Verifique se o cliente tem acesso administrativo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4394">Check that client has administrative access.</span></span> <span data-ttu-id="c3012-4395">Se o cliente não tiver acesso administrativo, o servidor deverá relatar um erro de STATUS de \_ acesso \_ negado (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="c3012-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="c3012-4396">Inicie qualquer processo de manutenção necessário para melhorar o desempenho de consulta em um catálogo, associado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="c3012-4397">Responda ao cliente com um cabeçalho de mensagem para o CPMForceMergeIn e defina o \_ campo status para os resultados da solicitação.</span><span class="sxs-lookup"><span data-stu-id="c3012-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="c3012-4398">Observe que o processo de manutenção é assíncrono e pode continuar depois que o cliente recebe a mensagem de resposta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="c3012-4399">Esse processo não afeta diretamente o protocolo de nenhuma forma (além do tempo de resposta).</span><span class="sxs-lookup"><span data-stu-id="c3012-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="c3012-4400">Consulta do serviço de indexação remota do 3.1.5.2</span><span class="sxs-lookup"><span data-stu-id="c3012-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="c3012-4401">3.1.5.2.1 recebendo uma solicitação CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="c3012-4402">Quando o servidor recebe uma solicitação CPMConnectIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4403">Verifique se o cliente está na lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="c3012-4404">Se esse for o caso, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4405">Verifica se o catálogo especificado existe e não está no estado parado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="c3012-4406">Se esse não for o caso, o servidor deverá ter um erro de CI \_ E \_ nenhum \_ catálogo (0x8004181D) de relatório.</span><span class="sxs-lookup"><span data-stu-id="c3012-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="c3012-4407">Adicione o cliente à lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="c3012-4408">Associe o catálogo ao cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="c3012-4409">Armazene as informações passadas na mensagem CPMConnectIn (como nome do catálogo, versão do cliente, etc.) no estado do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="c3012-4410">Responda ao cliente com uma mensagem CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="c3012-4411">3.1.5.2.2 recebendo uma solicitação CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="c3012-4412">Quando o servidor recebe uma solicitação de mensagem CPMCreateQueryIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4413">Verifique se o cliente está na lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="c3012-4414">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4415">Verifique se o cliente já tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="c3012-4416">Se esse for o caso, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4417">Verifique se o catálogo associado ao cliente está no estado que permite que a consulta seja processada (CICAT \_ ReadOnly ou CICAT \_ gravável).</span><span class="sxs-lookup"><span data-stu-id="c3012-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="c3012-4418">Se esse não for o caso, o servidor deverá relatar um \_ erro de \_ 0x8004160C (consulta S sem \_ consulta).</span><span class="sxs-lookup"><span data-stu-id="c3012-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="c3012-4419">Analise o conjunto de restrições, as ordens de classificação e os agrupamentos especificados na consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="c3012-4420">Se o servidor encontrar um erro, ele deverá relatar um erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="c3012-4421">Se essa etapa falhar por qualquer outro motivo, o servidor deverá relatar o erro encontrado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="c3012-4422">Para obter informações sobre erros de consulta de serviço de indexação, consulte \[ msdn-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="c3012-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="c3012-4423">Salve a consulta de pesquisa no estado do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="c3012-4424">Faça qualquer preparação necessária para atender linhas a um cliente e associar a consulta a identificadores de cursor apropriados (dependendo das informações passadas na mensagem CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="c3012-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="c3012-4425">Adicione esses identificadores à lista de identificadores de cursor do cliente e inicialize as listas de identificadores e indicadores de capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="c3012-4426">Inicializar a lista de identificadores de capítulo para cada cursor nesta consulta para DB \_ NULL \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="c3012-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="c3012-4427">Inicializar a lista de identificadores de indicadores para cada cursor nesta consulta para um conjunto de DBBMK \_ First e DBBMK \_ Last.</span><span class="sxs-lookup"><span data-stu-id="c3012-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="c3012-4428">Marque a consulta como não monitorado para alterações.</span><span class="sxs-lookup"><span data-stu-id="c3012-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="c3012-4429">Inicialize o número de linhas para o número de linhas calculado no momento (que pode ser 0 se a consulta não começar a ser executada ou algum número se a consulta estiver em um processo de execução) e inicialize o numerador e o denominador da conclusão da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="c3012-4430">Responda ao cliente com uma mensagem CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="c3012-4431">3.1.5.2.3 recebendo uma solicitação CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="c3012-4432">Quando o servidor recebe uma solicitação de mensagem CPMGetQueryStatusIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4433">Verifique se o cliente tem a consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3012-4434">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4435">Verifique se a alça do cursor está em uma lista de identificadores de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="c3012-4436">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4437">Prepare uma mensagem CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="c3012-4438">O servidor deve recuperar o status da consulta atual e defini-lo no \_ campo QStatus (consulte 2.2.3.11 para obter os valores possíveis).</span><span class="sxs-lookup"><span data-stu-id="c3012-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="c3012-4439">Se essa etapa falhar por algum motivo, o servidor deverá relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="c3012-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3012-4440">Responda ao cliente com a mensagem CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="c3012-4441">3.1.5.2.4 recebendo uma solicitação CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="c3012-4442">Quando o servidor recebe uma solicitação de mensagem CPMGetQueryStatusExIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4443">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3012-4444">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4445">Verifique se o identificador de cursor passado está em uma lista de identificadores de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="c3012-4446">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4447">Prepare uma mensagem CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="c3012-4448">O servidor deve recuperar o status da consulta atual e o progresso da consulta e definir QStatus (consulte 2.2.3.11 para obter os valores possíveis), \_ dwRatioFinishedDenominator e \_ dwRatioFinishedNumerator, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="c3012-4449">Em seguida, ele deve definir o número de linhas nos resultados da consulta para \_ cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="c3012-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="c3012-4450">Se essa etapa falhar por qualquer motivo, o servidor deverá relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3012-4451">Recupere informações sobre o catálogo do cliente e preencha \_ cFilteredDocuments e \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="c3012-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="c3012-4452">Se essa etapa falhar por algum motivo, o servidor deverá relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3012-4453">Recupere a posição do indicador indicada pelo identificador no \_ campo BMK e preencha o \_ campo iRowBmk restante na mensagem CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="c3012-4454">Se essa etapa falhar por qualquer motivo, o servidor deverá relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3012-4455">Responda ao cliente com a mensagem CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="c3012-4456">3.1.5.2.5 recebendo uma solicitação CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="c3012-4457">Quando o servidor recebe uma solicitação de mensagem CPMRatioFinishedIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4458">Verifique se o cliente tem a consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3012-4459">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4460">Verifique se o identificador de cursor passado está na lista de identificadores de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="c3012-4461">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4462">Prepare uma mensagem CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="c3012-4463">O servidor deve recuperar o status de consulta do cliente e preencher os \_ campos ulNumerator, \_ ulDenominator e \_ galinha.</span><span class="sxs-lookup"><span data-stu-id="c3012-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="c3012-4464">Se essa etapa falhar por algum motivo, o servidor deverá relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3012-4465">Se \_ galinha for igual ao último número relatado de linhas para essa consulta, defina \_ fNewRows como 0x00000000, caso contrário, defina-o como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="c3012-4466">Atualize o último número relatado de linhas para essa consulta para o valor de \_ galinha.</span><span class="sxs-lookup"><span data-stu-id="c3012-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="c3012-4467">Responda ao cliente com a mensagem CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="c3012-4468">3.1.5.2.6 recebendo uma solicitação CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="c3012-4469">Quando o servidor recebe uma solicitação de mensagem CPMSetBindingsIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4470">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3012-4471">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4472">Verifique se o identificador de cursor passado está na lista de identificadores de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="c3012-4473">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4474">Verifique se as informações de associações são válidas (ou seja, a coluna pelo menos especifica o valor, o comprimento ou o status a ser retornado; nenhuma sobreposição em associações para valor, comprimento ou status; e valor, comprimento e status se ajustam ao tamanho da linha especificado) e se não relatar um erro de DB \_ e \_ BADBINDINFO (0x80040E08).</span><span class="sxs-lookup"><span data-stu-id="c3012-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="c3012-4475">Salve as informações de associação associadas às colunas especificadas no campo aColumns.</span><span class="sxs-lookup"><span data-stu-id="c3012-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="c3012-4476">Se essa etapa falhar por algum motivo, o servidor deverá relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3012-4477">Responda ao cliente com um cabeçalho de mensagem (somente) com \_ msg definido como CPMSetBindingsIn e \_ o status definido como os resultados da associação especificada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="c3012-4478">3.1.5.2.7 recebendo uma solicitação CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="c3012-4479">Quando o servidor recebe uma solicitação de mensagem CPMGetRowsIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4480">Verifique se o cliente tem a consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3012-4481">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4482">Verifique se o identificador do cursor passado está em athelist dos identificadores do cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="c3012-4483">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4484">Verifique se o cliente tem um conjunto atual de associações.</span><span class="sxs-lookup"><span data-stu-id="c3012-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="c3012-4485">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4486">Prepare uma mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="c3012-4487">O servidor deve posicionar o cursor nos resultados da consulta, conforme indicado pela descrição de busca.</span><span class="sxs-lookup"><span data-stu-id="c3012-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="c3012-4488">Se essa etapa falhar por algum motivo, o servidor deverá relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3012-4489">Busque quantas linhas couber em um buffer, o tamanho que é indicado por \_ cbReadBuffer, mas não mais do que indicado por \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="c3012-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="c3012-4490">Ao buscar linhas, o servidor deve comparar cada tipo de valor de propriedade da coluna selecionada ao tipo especificado no conjunto atual de associações do cliente (seção 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="c3012-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="c3012-4491">Se o tipo na associação não for VT \_ Variant, o servidor deverá tentar converter o valor da propriedade da coluna para esse tipo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="c3012-4492">Caso contrário, se o \_ sinalizador DBPROP USEEXTENDEDDBTYPES for definido no conjunto de propriedades DBPROPSET QUERYEXT do cliente \_ ou se o valor da propriedade da coluna não for um \_ tipo de vetor VT, o valor da propriedade deverá ser retornado em seu tipo normal.</span><span class="sxs-lookup"><span data-stu-id="c3012-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="c3012-4493">Se nenhum desses for o caso (ou seja, o servidor tiver um tipo de \_ vetor VT e o cliente não oferecer suporte ao \_ vetor VT), o servidor deverá tentar convertê-lo em um \_ tipo de matriz VT da seguinte maneira: VT \_ i8, VT \_ UI8, VT \_ FILETIME e os elementos da \_ matriz VT CLSID não podem ser convertidos e, em vez disso, falha; \_ \_ Os elementos de matriz de LPWSTR e VT LPSTR devem ser convertidos em VT \_ BSTR; os elementos de matriz de todos os outros tipos devem permanecer inalterados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="c3012-4494">Por fim, se as colunas de linha contiverem identificadores de capítulo ou identificadores de indicador, o servidor deverá atualizar as listas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="c3012-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="c3012-4495">Se essa etapa falhar por algum motivo, o servidor deverá relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3012-4496">Armazene o número real de linhas buscadas em \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="c3012-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="c3012-4497">Copie a descrição de busca e o campo de capítulo de CPMGetRowsIn para uma mensagem CPMGetRowsOut a ser enviada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="c3012-4498">Armazene as linhas buscadas no campo linhas (consulte a observação sobre o byte de status abaixo e a seção 2.2.3.16 na estrutura do campo linhas).</span><span class="sxs-lookup"><span data-stu-id="c3012-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="c3012-4499">Responda ao cliente com a mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="c3012-4500">Observação no campo byte de status:</span><span class="sxs-lookup"><span data-stu-id="c3012-4500">Note on status byte field:</span></span>

<span data-ttu-id="c3012-4501">Se StatusUsed for definido como 0x01 no CTableColumn da mensagem CPMSetBindingIn para a coluna, o servidor deverá definir o byte de status (que está localizado em StatusOffset do início da linha) para essa coluna como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c3012-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="c3012-4502">Valor</span><span class="sxs-lookup"><span data-stu-id="c3012-4502">Value</span></span> | <span data-ttu-id="c3012-4503">Significado</span><span class="sxs-lookup"><span data-stu-id="c3012-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="c3012-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="c3012-4504">0x00</span></span>  | <span data-ttu-id="c3012-4505">StatusOK</span><span class="sxs-lookup"><span data-stu-id="c3012-4505">StatusOK</span></span>       |
| <span data-ttu-id="c3012-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="c3012-4506">0x01</span></span>  | <span data-ttu-id="c3012-4507">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="c3012-4507">StatusDeferred</span></span> |
| <span data-ttu-id="c3012-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="c3012-4508">0x02</span></span>  | <span data-ttu-id="c3012-4509">StatusNull</span><span class="sxs-lookup"><span data-stu-id="c3012-4509">StatusNull</span></span>     |



 

<span data-ttu-id="c3012-4510">Se o valor da propriedade estiver ausente para essa linha, o servidor deverá definir o byte de status como StatusNull.</span><span class="sxs-lookup"><span data-stu-id="c3012-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="c3012-4511">Se o valor for muito grande para ser transferido na mensagem CPMGetRowsOut, o servidor deverá definir o byte de status para StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="c3012-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="c3012-4512">Caso contrário, o servidor deve definir o byte de status como StatusOK.</span><span class="sxs-lookup"><span data-stu-id="c3012-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="c3012-4513">3.1.5.2.8 recebendo uma solicitação CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="c3012-4514">Quando o servidor recebe uma solicitação de mensagem CPMFetchValueIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4515">Verifique se o cliente tem a consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3012-4516">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4517">Prepare uma mensagem CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="c3012-4518">Se essa etapa falhar por algum motivo, o servidor deverá relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="c3012-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3012-4519">Localize o documento indicado pelo \_ campo wid e verifique se a ID de propriedade deste documento (posteriormente referenciada como ' valor da propriedade ') indicada pela estrutura PropSpec está disponível para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="c3012-4520">Se esse valor não estiver disponível, o servidor deverá definir \_ fValueExists como 0x00000000 e, caso contrário, definirá \_ fValueExists como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="c3012-4521">Se essa etapa falhar por algum motivo, o servidor deverá relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="c3012-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3012-4522">Se \_ fValueExists for igual a 0x00000001, o servidor deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="c3012-4523">Serialize o valor da propriedade para uma estrutura SERIALIZEDPROPERTYVALUE e copie, começando do \_ deslocamento de cbSoFar, no máximo \_ cbChunk bytes (mas não após o final da propriedade serializada) para vValue campo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="c3012-4524">Se essa etapa falhar por qualquer motivo, o servidor deverá relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="c3012-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="c3012-4525">Defina \_ cbValue como o número de bytes copiados na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="c3012-4526">Defina vType como o tipo de Propriedade do valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="c3012-4527">Se o comprimento da propriedade serializada for maior que \_ cbSoFar adicionado a \_ cbValue, defina \_ fMoreExists como 0x00000001, caso contrário, defina-o como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="c3012-4528">Responder ao cliente com a mensagem CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="c3012-4529">3.1.5.2.9 recebendo uma solicitação CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="c3012-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="c3012-4530">Quando o servidor recebe uma mensagem CPMGetNotify de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4531">Verifique se o cliente tem a consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3012-4532">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4533">Se não houvesse nenhuma alteração no conjunto de resultados da consulta desde a última mensagem de CPMSendNotifyOut para esse cliente, ou se a consulta não for atualmente monitorada para alterações no conjunto de resultados, o servidor deverá responder com a mensagem CPMGetNotify e começar a monitorar a consulta em busca de alterações no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="c3012-4534">Se, em um momento posterior, houver uma alteração no conjunto de resultados da consulta, o servidor deverá enviar exatamente uma mensagem CPMSendNotifyOut para o cliente e deve especificar a alteração no \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="c3012-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="c3012-4535">Se houver alterações no conjunto de resultados da consulta desde a última mensagem CPMSendNotifyOut, o servidor deverá responder com CPMSendNotifyOut e deverá especificar a alteração no \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="c3012-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="c3012-4536">Observe que, no caso de muitas alterações nos resultados da consulta, DBWATCHNOTIFY \_ rowschanged tem prioridade (ou seja, se a consulta foi feita, executada novamente e, em seguida, o número de linhas alteradas e a consulta foi feita novamente, o evento relatado seria DBWATCHNOTIFY \_ rowschanged).</span><span class="sxs-lookup"><span data-stu-id="c3012-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="c3012-4537">3.1.5.2.10 recebendo uma solicitação CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="c3012-4538">Quando o servidor recebe uma solicitação de mensagem CPMGetApproximatePositionIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4539">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3012-4540">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4541">Verifique se a alça do cursor, o identificador do capítulo e o identificador do indicador aprovado estão nas listas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="c3012-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="c3012-4542">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4543">Localize uma linha que esteja associada ao identificador de indicador nos resultados da consulta e aproximar a posição da linha no conjunto de linhas, referenciada pelo identificador de capítulo, e determine o numerador e o denominador para a posição.</span><span class="sxs-lookup"><span data-stu-id="c3012-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="c3012-4544">Observe que, quando o identificador do capítulo é DB \_ NULL \_ HCHAPTER, o capítulo correspondente é o principal conjunto de linhas da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="c3012-4545">Se essa etapa falhar por algum motivo, o servidor deverá relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="c3012-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3012-4546">Responda ao cliente com uma mensagem CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="c3012-4547">3.1.5.2.11 recebendo uma solicitação CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="c3012-4548">Quando o servidor recebe uma solicitação de mensagem CPMCompareBmkIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4549">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3012-4550">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4551">Verifique se a alça do cursor, o identificador do capítulo e os identificadores de indicador passados estão nas listas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="c3012-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="c3012-4552">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4553">Prepare uma mensagem CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="c3012-4554">Se as alças de indicador forem iguais, \_ DWCOMPARISON deverá ser definido como DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="c3012-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="c3012-4555">Caso contrário, se um dos indicadores identificadores for DBBMK \_ First ou DBBMK \_ Last, \_ dwComparison deverá ser definido como DBCOMPARE \_ ne.</span><span class="sxs-lookup"><span data-stu-id="c3012-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="c3012-4556">Caso contrário, o servidor deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="c3012-4557">Localizar linhas que são referenciadas por cada identificador de indicador nos resultados da consulta</span><span class="sxs-lookup"><span data-stu-id="c3012-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="c3012-4558">Se qualquer uma das linhas não estiver no capítulo indicado pelo identificador de capítulo em CPMCompareBmkIn, \_ DWCOMPARISON deverá ser definido como DBCOMPARE não \_ comparável.</span><span class="sxs-lookup"><span data-stu-id="c3012-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="c3012-4559">Caso contrário, quando ambas as linhas estiverem no mesmo capítulo, o servidor deverá aproximar uma posição dessas linhas no conjunto de linhas referido pela alça deste capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="c3012-4560">Em seguida, ele deve comparar valores de posição e definir \_ dwComparison como DBCOMPARE \_ lt se a posição da primeira linha for menor que a posição da segunda linha; caso contrário, \_ dwComparison deverá ser definido como DBCOMPARE \_ gt.</span><span class="sxs-lookup"><span data-stu-id="c3012-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="c3012-4561">Responda ao cliente com a mensagem CPMCompareBmkOut preenchida.</span><span class="sxs-lookup"><span data-stu-id="c3012-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="c3012-4562">3.1.5.2.12 recebendo uma solicitação CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="c3012-4563">Quando o servidor recebe a solicitação de mensagem CPMRestartPositionIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4564">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3012-4565">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4566">Verifique se o identificador do cursor e o identificador do capítulo aprovado estão nas listas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="c3012-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="c3012-4567">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4568">Mova o cursor para o início do capítulo, identificado pelo identificador de capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="c3012-4569">Observe que, quando o identificador do capítulo é DB \_ NULL \_ HCHAPTER, o capítulo correspondente é o principal conjunto de linhas da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="c3012-4570">Se essa etapa falhar por algum motivo, o servidor deverá relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="c3012-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3012-4571">Responda ao cliente com uma mensagem CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="c3012-4572">3.1.5.2.13 recebendo uma solicitação CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="c3012-4573">Quando o servidor recebe uma solicitação de mensagem CPMFreeCursorIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4574">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="c3012-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3012-4575">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="c3012-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3012-4576">Verifique se o identificador de cursor passado está na lista de identificadores de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="c3012-4577">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="c3012-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3012-4578">Libere o cursor e os recursos associados (consulte a seção 3.1.1 para obter a lista completa) para esse identificador de cursor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="c3012-4579">Remova o cursor da lista de cursores para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="c3012-4580">Responda com uma mensagem CPMFreeCursorOut, definindo o \_ campo cCursorsRemaining com o número de cursores restantes.</span><span class="sxs-lookup"><span data-stu-id="c3012-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="c3012-4581">na lista deste cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4581">in this client's list.</span></span>
-   <span data-ttu-id="c3012-4582">Se não houver mais cursores para esse cliente, o servidor deverá liberar a consulta e os recursos associados (consulte a seção 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="c3012-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="c3012-4583">3.1.5.2.14 recebendo uma solicitação CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="c3012-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="c3012-4584">Quando o servidor recebe uma solicitação de mensagem CPMDisconnect do cliente, o servidor deve remover o cliente da lista de clientes conectados e liberar todos os recursos associados ao cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="c3012-4585">Eventos de timer 3.1.6</span><span class="sxs-lookup"><span data-stu-id="c3012-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="c3012-4586">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c3012-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="c3012-4587">3.1.7 outros eventos locais</span><span class="sxs-lookup"><span data-stu-id="c3012-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="c3012-4588">Quando o servidor é interrompido, ele deve primeiro fazer a transição para o estado "desligando".</span><span class="sxs-lookup"><span data-stu-id="c3012-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="c3012-4589">Em seguida, ele deve parar de escutar o pipe, executar outras tarefas de desligamento específicas da implementação e, em seguida, fazer a transição para o estado "Stopped".</span><span class="sxs-lookup"><span data-stu-id="c3012-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="c3012-4590">3,2 detalhes do cliente</span><span class="sxs-lookup"><span data-stu-id="c3012-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="c3012-4591">3.2.1 modelo de dados abstratos</span><span class="sxs-lookup"><span data-stu-id="c3012-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="c3012-4592">A seção a seguir especifica os dados e o estado mantidos pelo cliente do protocolo do serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="c3012-4593">Os dados fornecidos são para facilitar a explicação de como o protocolo se comporta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="c3012-4594">Esta seção não exige que as implementações sigam esse modelo, desde que seu comportamento externo seja consistente com o descrito neste documento.</span><span class="sxs-lookup"><span data-stu-id="c3012-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="c3012-4595">Um cliente tem o seguinte estado abstrato:</span><span class="sxs-lookup"><span data-stu-id="c3012-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="c3012-4596">**Última mensagem enviada**: uma cópia da última mensagem enviada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="c3012-4597">**Valor da propriedade atual**: um valor parcial de uma propriedade "adiada", que está no processo de ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="c3012-4598">**Bytes atuais recebidos**: o número de bytes recebidos para o valor da propriedade atual até o momento.</span><span class="sxs-lookup"><span data-stu-id="c3012-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="c3012-4599">**Estado de conexão do pipe nomeado**: uma conexão com o servidor</span><span class="sxs-lookup"><span data-stu-id="c3012-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="c3012-4600">temporizadores de 3.2.2</span><span class="sxs-lookup"><span data-stu-id="c3012-4600">3.2.2 Timers</span></span>

<span data-ttu-id="c3012-4601">Nenhum temporizador de protocolo é necessário.</span><span class="sxs-lookup"><span data-stu-id="c3012-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="c3012-4602">inicialização do 3.2.3</span><span class="sxs-lookup"><span data-stu-id="c3012-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="c3012-4603">Nenhuma ação é executada até que uma solicitação de camada superior seja recebida.</span><span class="sxs-lookup"><span data-stu-id="c3012-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="c3012-4604">Eventos disparados Higher-Layer 3.2.4</span><span class="sxs-lookup"><span data-stu-id="c3012-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="c3012-4605">Quando uma solicitação é recebida de uma camada superior, o cliente deve criar uma conexão de pipe nomeado para o servidor, usando os detalhes especificados na seção 2,1.</span><span class="sxs-lookup"><span data-stu-id="c3012-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="c3012-4606">Se não for possível fazer isso, a solicitação de camada superior deverá ter falhado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="c3012-4607">Ou seja, no caso de uma falha ao se conectar, é responsabilidade do nível mais alto tentar novamente, se desejado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="c3012-4608">Um cabeçalho deve ser semipendente com campos definidos conforme especificado na seção 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="c3012-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="c3012-4609">Para mensagens que são especificadas como exigindo uma soma de verificação diferente de zero, o \_ valor de ULCHECKSUM deve ser calculado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="c3012-4610">O conteúdo da mensagem após o \_ campo ulReserved2 no cabeçalho da mensagem deve ser interpretado como uma sequência de inteiros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="c3012-4611">O cliente deve calcular a soma dos valores numéricos fornecidos por esses inteiros.</span><span class="sxs-lookup"><span data-stu-id="c3012-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="c3012-4612">Calcule o XOR bit a bit desse valor com 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="c3012-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="c3012-4613">Subtraia o valor fornecido pela \_ mensagem do valor que resulta do XOR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="c3012-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="c3012-4614">Gerenciamento de catálogo do serviço de indexação remota do 3.2.4.1</span><span class="sxs-lookup"><span data-stu-id="c3012-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="c3012-4615">Cada mensagem é disparada por uma solicitação da camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="c3012-4616">Não há nenhuma sequência de mensagens imposta pelo cliente para solicitações de mensagens CISP para gerenciar catálogos remotamente, mas (com exceção de uma mensagem CPMSetCatStateIn) o servidor responderá com êxito somente se o cliente tiver se conectado anteriormente por meio de uma mensagem CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="c3012-4617">3.2.4.1.1 enviando uma solicitação CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="c3012-4618">Normalmente, a camada superior solicita que o cliente de protocolo envie uma mensagem CPMCiStateInOut quando requer informações sobre a indexação de serviços no servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="c3012-4619">Quando solicitado a enviar esta mensagem, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4620">Envie uma mensagem CPMCiStateInOut conforme especificado na seção 2.2.3.1 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="c3012-4621">Aguarde para receber a mensagem CPMCiStateInOut do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3012-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3012-4622">Relate o valor do \_ campo status da resposta e, se tiver êxito, a estrutura informativa de volta à camada mais alta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="c3012-4623">3.2.4.1.2 enviando uma solicitação CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="c3012-4624">Normalmente, a camada superior solicita que o cliente de protocolo envie uma mensagem CPMSetCatStateIn quando requer informações sobre um catálogo ou todos os catálogos.</span><span class="sxs-lookup"><span data-stu-id="c3012-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="c3012-4625">Para essa mensagem, a camada superior precisa fornecer ao cliente de protocolo um valor para \_ dwNewState e, se necessário, o nome do catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="c3012-4626">Quando solicitado a enviar esta mensagem, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4627">Envie uma mensagem CPMSetCatStateIn conforme especificado em 2.2.3.2 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="c3012-4628">Aguarde para receber uma mensagem CPMSetCatStateOut do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3012-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3012-4629">Relate o valor do \_ campo status da resposta e, se tiver sido bem-sucedida, o \_ dwOldState de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="c3012-4630">3.2.4.1.3 enviando uma solicitação CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="c3012-4631">A camada mais alta normalmente solicita o envio dessa mensagem quando precisa atualizar documentos no caminho existente ou adicionar um novo caminho de arquivo ao índice.</span><span class="sxs-lookup"><span data-stu-id="c3012-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="c3012-4632">Portanto, a camada mais alta é fornecer o caminho e o tipo de uma verificação, que é especificado como na seção 2.2.3.4, em que uma atualização incremental ou completa é destinada a caminhos existentes, e a nova inicialização é destinada a novos caminhos.</span><span class="sxs-lookup"><span data-stu-id="c3012-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="c3012-4633">Para atender à solicitação de camada superior, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4634">Envie uma mensagem CPMUpdateDocumentsIn conforme especificado na seção 2.2.3.4 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="c3012-4635">Aguarde para receber a mensagem CPMUpdateDocumentsIn de volta do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3012-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3012-4636">Relate o valor do \_ campo status da resposta de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="c3012-4637">3.2.4.1.4 enviando uma solicitação CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="c3012-4638">Normalmente, as solicitações de camada mais alta para enviar essa mensagem quando há necessidade de melhorar o desempenho da consulta ou fazem parte da manutenção agendada do serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="c3012-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="c3012-4639">Para atender à camada mais alta, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4640">Envie a mensagem CPMForceMergeIn conforme especificado pela seção 2.2.3.5 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="c3012-4641">Aguarde para receber uma mensagem CPMUpdateDocumentsIn de volta do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3012-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3012-4642">Relate o valor do \_ campo status da resposta de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="c3012-4643">Mensagens de consulta do catálogo de serviço de indexação remota do 3.2.4.2</span><span class="sxs-lookup"><span data-stu-id="c3012-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="c3012-4644">Com exceção de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, há uma relação um-para-um entre as mensagens CISP e as solicitações de camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="c3012-4645">Para as duas exceções mencionadas acima, pode haver várias mensagens geradas pelo cliente para atender aos requisitos de tamanho ou para recuperar uma propriedade completa.</span><span class="sxs-lookup"><span data-stu-id="c3012-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="c3012-4646">Normalmente, a camada superior controla todas as informações específicas de consulta (como identificadores de cursor abertos, valores válidos para identificadores de indicador e capítulo, valores de wid para valores de propriedade adiados, etc.) e também controla se o cliente está em um estado conectado, mas isso não é imposto de nenhuma forma pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="c3012-4647">Para fins ilustrativos, a parte de cliente do diagrama na seção 3 ilustra essa sequência para uma consulta de serviço de indexação simples.</span><span class="sxs-lookup"><span data-stu-id="c3012-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="c3012-4648">3.2.4.2.1 enviando uma solicitação CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="c3012-4649">Essa mensagem é normalmente a primeira solicitação da camada superior (como se o cliente não estiver conectado, o servidor falhará na maioria das mensagens com exceção de CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="c3012-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="c3012-4650">O nível mais alto fornece ao cliente de protocolo as informações necessárias para se conectar.</span><span class="sxs-lookup"><span data-stu-id="c3012-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="c3012-4651">Para atender à camada mais alta, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4652">Preencha a mensagem, usando informações que o cliente de camada superior forneceu (consulte a seção 2.2.3.6) em \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 e aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="c3012-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="c3012-4653">Defina \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet e cExtPropSet conforme especificado em 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="c3012-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="c3012-4654">Defina a soma de verificação no \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="c3012-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="c3012-4655">Envie a mensagem CPMConnectIn para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="c3012-4656">Aguarde para receber uma mensagem CPMConnectOut de volta do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3012-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3012-4657">Relate o valor do \_ campo status da resposta e, se tiver sido bem-sucedida, o \_ serverVersion de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="c3012-4658">Para fins informativos, espera-se que as camadas mais altas normalmente realizem as seguintes ações após a conexão bem-sucedida, mas elas não são impostas pelo cliente CISP:</span><span class="sxs-lookup"><span data-stu-id="c3012-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="c3012-4659">Usar mensagens de gerenciamento de catálogo de serviço de indexação remota para tarefas administrativas</span><span class="sxs-lookup"><span data-stu-id="c3012-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="c3012-4660">Use uma solicitação CPMCreateQueryIn para criar uma consulta de pesquisa com a finalidade de recuperar os resultados do catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="c3012-4661">3.2.4.2.2 enviando uma solicitação CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="c3012-4662">A camada superior normalmente fornecerá informações para a criação da consulta quando o cliente do protocolo estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="c3012-4663">A camada superior fornece ao cliente um conjunto de restrições, conjunto de colunas, regras de ordem de classificação e conjunto de categorização (cada um deles pode ser omitido), propriedades de conjunto de linhas e estrutura do mapeador de ID de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3012-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="c3012-4664">Quando essa solicitação é recebida de uma camada superior, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4665">Prepare um CPMCreateQueryOut da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="c3012-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="c3012-4666">Se um conjunto de colunas estiver presente, defina CColumnsSetPreset como 0x01 e preencha o campo Columnsset.</span><span class="sxs-lookup"><span data-stu-id="c3012-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="c3012-4667">Se houver restrições, defina CRestrictionPresent como 0x01 e preencha o campo de restrição.</span><span class="sxs-lookup"><span data-stu-id="c3012-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="c3012-4668">Se um conjunto de classificação estiver presente, preencha o campo de classificação.</span><span class="sxs-lookup"><span data-stu-id="c3012-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="c3012-4669">Se um conjunto de categorização estiver presente, defina CSortSetPresent como 0x01 e preencha o campo CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="c3012-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="c3012-4670">Definir o restante dos campos conforme especificado em 2.2.3.8</span><span class="sxs-lookup"><span data-stu-id="c3012-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="c3012-4671">Calcule \_ o campo ulCheckSum no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="c3012-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="c3012-4672">Envie a mensagem CPMCreateQueryIn para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="c3012-4673">Aguarde para receber a mensagem CPMCreateQueryOut (consulte os detalhes na seção 3.2.5.1.1), descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3012-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3012-4674">Relate o valor do \_ campo status da resposta e, se tiver êxito, a matriz de identificadores de cursor e valores Boolianos informativos (conforme especificado em 2.2.3.9) de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="c3012-4675">3.2.4.2.3 enviando uma solicitação CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="c3012-4676">Normalmente, a camada superior definirá associações para cada coluna a ser retornada nas linhas quando ela já tiver um identificador de cursor válido (depois de receber CPMCreateQueryOut com êxito, consulte a seção 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="c3012-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="c3012-4677">O valor mais alto é esperado para fornecer uma matriz de estruturas CTableColumn, conforme especificado na seção 2.2.4.31, para o campo aColumns e um identificador de cursor válido.</span><span class="sxs-lookup"><span data-stu-id="c3012-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="c3012-4678">Quando essa solicitação é recebida da camada superior, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4679">Calcule o número de estruturas CTableColumn na matriz aColumns e defina o campo cColumns com esse valor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="c3012-4680">Calcule o tamanho total em bytes dos campos cColumns e aColumns e defina o \_ campo cbBindingDesc com esse valor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="c3012-4681">Defina os campos especificados na mensagem CPMSetBindingsIn para os valores fornecidos pela camada de aplicativo superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="c3012-4682">Defina o \_ campo ulChecksum para o valor calculado conforme especificado na seção 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="c3012-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="c3012-4683">Envie a mensagem CPMSetBindignsIn concluída para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="c3012-4684">Aguarde para receber uma mensagem CPMSetBindingsIn do servidor, descartando outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3012-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="c3012-4685">Indique o status do \_ campo status da resposta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="c3012-4686">Para fins informativos, espera-se que as camadas mais altas normalmente solicitem que um cliente envie uma mensagem CPMGetRowsIn, mas isso não é imposto pelo protocolo de serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="c3012-4687">3.2.4.2.4 enviando uma solicitação CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="c3012-4688">Quando a camada mais alta estiver prestes a receber informações de linhas, ele fornecerá ao cliente de protocolo com o cursor e o identificador do capítulo válidos e fornecerá a descrição de busca apropriada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="c3012-4689">Normalmente, espera-se que uma camada mais alta faça isso quando tem um cursor e/ou identificador de capítulo válido, e as associações foram definidas com a mensagem CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="c3012-4690">Para acessar o conjunto de linhas em um capítulo, a camada mais alta é usar o identificador de capítulo recebido do servidor em uma mensagem CPMGetRowsOut anterior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="c3012-4691">Quando essa solicitação é recebida da camada superior, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4692">Determine qual valor inteiro sem sinal deve ser especificado para o \_ campo cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="c3012-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="c3012-4693">Para determinar esse valor, o cliente deve obter o valor máximo do seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="c3012-4694">1000 vezes o valor do campo c \_ RowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="c3012-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="c3012-4695">Valor de \_ cbRowWidth, arredondado para o múltiplo de 512 bytes mais próximo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="c3012-4696">Pegue os dois valores acima, até o limite de 16K.</span><span class="sxs-lookup"><span data-stu-id="c3012-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="c3012-4697">Nos casos em que uma única linha é maior que 16K, o servidor não pode retornar resultados para essa consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="c3012-4698">Especifique uma base de cliente para dados de linha de tamanho variável no espaço de endereço de cliente no \_ campo ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="c3012-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="c3012-4699">*Comportamento do Windows: para um cliente de 32 bits conversando com um servidor de 32 bits ou um cliente de 64 bits conversando com um servidor de 64 bits, esse valor é definido como um endereço de memória do buffer de recebimento no processo do aplicativo. Isso permite que os ponteiros, recebidos no campo de linhas de CPMGetRowsOut, sejam ponteiros de memória corretos em um processo de aplicativo cliente. Caso contrário, ele será definido como 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="c3012-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="c3012-4700">Calcule o tamanho da descrição de busca e defina-a no \_ campo cbSeek.</span><span class="sxs-lookup"><span data-stu-id="c3012-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="c3012-4701">Defina o valor de cbReserved (que atuaria como um deslocamento para o início das linhas) para o valor de \_ cbSeek Plus 0x14.</span><span class="sxs-lookup"><span data-stu-id="c3012-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="c3012-4702">Envie uma mensagem CPMConnectIn conforme especificado em 2.2.3.15 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="c3012-4703">3.2.4.2.5 enviando uma solicitação CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="c3012-4704">Se o cliente receber uma resposta CPMGetRowsOut do servidor com o campo status da coluna definido como StatusDeferred (0x01), isso significa que o valor da propriedade não foi incluído no campo linhas da mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="c3012-4705">Nesse caso, a camada mais alta normalmente solicita que o cliente de protocolo recupere o valor por meio da mensagem CPMFetchValueIn e fornece o valor de PropSpec e \_ wid para uma propriedade adiada, que o cliente de protocolo deve usar na primeira mensagem CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="c3012-4706">Se esta for a primeira mensagem CPMFetchValueIn que o cliente enviou para solicitar a propriedade especificada, o cliente deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4707">Defina todos os campos em uma mensagem conforme especificado na seção 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="c3012-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="c3012-4708">Defina \_ cbSoFar como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="c3012-4709">Defina os bytes atuais recebidos como 0.</span><span class="sxs-lookup"><span data-stu-id="c3012-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="c3012-4710">Envie a mensagem CPMFetchValueIn para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="c3012-4711">3.2.4.2.6 enviando uma solicitação CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="c3012-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="c3012-4712">Quando o nível mais alto não estiver mais usando a consulta de pesquisa, ele poderá liberar os recursos no servidor solicitando que o cliente envie uma mensagem CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="c3012-4713">Quando essa solicitação é recebida, o cliente deve enviar uma mensagem CPMFreeCursorIn conforme especificado em 2.2.3.28 para o servidor, contendo o identificador especificado pela camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="c3012-4714">3.2.4.2.7 enviando uma mensagem CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="c3012-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="c3012-4715">Se a camada superior não tiver mais consultas para o serviço de indexação, para liberar mais recursos do servidor, o aplicativo poderá solicitar que o cliente envie uma mensagem CPMDisconnect ao servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="c3012-4716">Quando essa consulta é recebida, o cliente deve simplesmente enviar a mensagem conforme solicitado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="c3012-4717">Não há resposta a essa mensagem do servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="c3012-4718">Processamento de mensagens 3.2.5 e regras de sequenciamento</span><span class="sxs-lookup"><span data-stu-id="c3012-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="c3012-4719">Quando o cliente recebe uma resposta de mensagem do servidor, o cliente deve usar a última mensagem enviada para determinar se a mensagem recebida do servidor é a esperada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="c3012-4720">Todas as mensagens com \_ o campo msg diferente da que está na última mensagem de envio devem ser ignoradas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="c3012-4721">3.2.5.1 recebendo uma resposta CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="c3012-4722">Quando o cliente recebe uma resposta de mensagem CPMCreateQueryOut do servidor, o cliente deve retornar o \_ status e (se o status for com êxito) os valores de ponteiro de volta para uma camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="c3012-4723">Todas as ações adicionais são até a camada mais alta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="c3012-4724">Como a camada mais alta reconhece a estrutura de consulta, ela sempre esperará o número correto de identificadores de cursor a serem retornados na mensagem CPMCreateOueryOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="c3012-4725">As alças de cursor são retornadas na seguinte ordem: o primeiro identificador é para o conjunto de linhas sem capítulos, o segundo é para o primeiro conjunto de linhas com capítulo (que é o agrupamento de resultados com base na primeira categoria especificada no campo CategorizationSet da mensagem CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="c3012-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="c3012-4726">Para fins informativos, espera-se que camadas mais altas possam realizar as seguintes ações, mas elas não são impostas pelo cliente CISP:</span><span class="sxs-lookup"><span data-stu-id="c3012-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="c3012-4727">Use CPMSetBindingsIn para definir associações para colunas individuais e executar ações subsequentes no caminho de consulta</span><span class="sxs-lookup"><span data-stu-id="c3012-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="c3012-4728">Use CPMGetQueryStatusIn para verificar o progresso da execução de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="c3012-4729">Use CPMRatioFinishedIn para solicitar o percentual de conclusão da consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="c3012-4730">3.2.5.2 recebendo uma resposta CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="c3012-4731">Quando o cliente recebe uma resposta de mensagem CPMGetRowsOut do servidor, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4732">Verifique se o \_ campo status no cabeçalho indica êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="c3012-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="c3012-4733">Se o \_ valor de status for \_ buffer de status \_ muito \_ pequeno (0xC0000023), o cliente deverá verificar o estado da última mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="c3012-4734">Se não contiver uma mensagem CPMGetRowsIn, a mensagem recebida deverá ser silenciosamente ignorada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="c3012-4735">Caso contrário, o cliente deve enviar ao servidor uma nova mensagem CPMGetRowsIn com todos os campos idênticos ao armazenado, exceto que o \_ CBREADBUFFER deve ser aumentado em 512 (mas não em maior que 0x4000).</span><span class="sxs-lookup"><span data-stu-id="c3012-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="c3012-4736">Se o \_ status for um buffer de status \_ \_ muito \_ pequeno (0xC0000023), e a última mensagem enviada já tiver \_ CBREADBUFFER igual a 0x4000 cliente deverá relatar o erro até o nível mais alto.</span><span class="sxs-lookup"><span data-stu-id="c3012-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="c3012-4737">Se o \_ valor de status for qualquer outro valor de erro, o cliente deverá indicar a falha até a camada mais alta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="c3012-4738">Se o \_ valor de status indicar êxito, os resultados deverão ser indicados até a camada mais alta solicitando as informações e outras ações serão até a camada mais alta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="c3012-4739">Para fins informativos, espera-se que as camadas mais altas normalmente realizem as seguintes ações, mas elas não são impostas pelo cliente do protocolo de serviço de indexação de conteúdo:</span><span class="sxs-lookup"><span data-stu-id="c3012-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="c3012-4740">Se os valores em linhas representarem as IDs de documento, o capítulo ou indicador tratará que a camada mais alta normalmente as armazenará para uso em operações subsequentes, que envolvem IDs de documento válidas, identificadores de capítulo ou indicador.</span><span class="sxs-lookup"><span data-stu-id="c3012-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="c3012-4741">A camada superior normalmente armazenará ou exibirá ou usará os dados de valores de linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="c3012-4742">Para os valores que foram marcados como camada mais alta adiada, o valor será obtido usando mensagens CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="c3012-4743">A descrição de busca é retornada para uma camada mais alta também e pode ser reutilizada ou examinada pela camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="c3012-4744">Para fins informativos, se a camada superior solicitou identificadores para capítulos e indicadores que foram recebidos nas linhas, ele pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="c3012-4745">Use CPMGetQueryStatusExIn para verificar o progresso da execução de uma consulta, bem como informações de status adicionais, como o número de documentos filtrados, os documentos restantes a serem filtrados, a taxa de documentos processados pela consulta, o número total de linhas na consulta e a posição do indicador no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="c3012-4746">Use CPMGetNotify para solicitar que o servidor notifique o cliente sobre as alterações de conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="c3012-4747">Use CPMGetApproximatePositionIn para solicitar a posição aproximada de um indicador em um capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="c3012-4748">Use CPMCompareBmkIn para solicitar uma comparação de dois indicadores em um capítulo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="c3012-4749">Use CPMRestartPositionIn, para o servidor, para alterar o local do cursor para o início do conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="c3012-4750">3.2.5.3 recebendo uma resposta CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="c3012-4751">Quando o cliente recebe uma resposta de mensagem CPMGetRowsOut do servidor, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3012-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3012-4752">Verifique se o \_ campo status no cabeçalho indica êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="c3012-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="c3012-4753">Em caso de falha, notifique a camada mais alta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="c3012-4754">Caso contrário, continue abaixo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="c3012-4755">Verifique \_ fValueExist e, se definido como 0x00000000, notifique a camada superior de que o valor não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="c3012-4756">Caso contrário, acrescente \_ cbValue bytes de vValue ao valor da propriedade atual.</span><span class="sxs-lookup"><span data-stu-id="c3012-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="c3012-4757">Se \_ \_ fMoreExists for definido como 0x00000001, incrementar os \_ bytes atuais recebidos por \_ cbValue e enviar uma mensagem CPMFetchValueIn para o servidor, definindo \_ CbSoFar como o valor dos bytes atuais recebidos, \_ cbPropSpec para zero e \_ cbChunk para o tamanho do buffer desejado pela camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="c3012-4758">Se \_ fMoreExists for definido como 0x00000000, então, indique o valor da Propriedade do valor da propriedade atual para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="c3012-4759">3.2.5.4 recebendo uma resposta CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="c3012-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="c3012-4760">Quando o cliente recebe uma resposta de mensagem CPMFreeCursorOut bem-sucedida do servidor, o cliente deve retornar o \_ valor de cCursorsRemaining para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="c3012-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="c3012-4761">As informações a seguir são fornecidas apenas para fins informativos e não são impostas pelo cliente CISP.</span><span class="sxs-lookup"><span data-stu-id="c3012-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="c3012-4762">Espera-se que a camada superior acompanhe as alças do cursor e não use aquelas que já foram liberadas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="c3012-4763">Depois que o número de \_ cCursorsRemaining é igual a 0x00000000, a camada superior pode usar a conexão para especificar outra consulta (usando uma mensagem CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="c3012-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="c3012-4764">Eventos de timer 3.2.6</span><span class="sxs-lookup"><span data-stu-id="c3012-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="c3012-4765">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c3012-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="c3012-4766">3.2.7 outros eventos locais</span><span class="sxs-lookup"><span data-stu-id="c3012-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="c3012-4767">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c3012-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="c3012-4768">4 Exemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="c3012-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="c3012-4769">4,1 exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3012-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="c3012-4770">4,2 exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3012-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="c3012-4771">4,1 exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3012-4771">4.1 Example 1</span></span>

<span data-ttu-id="c3012-4772">No exemplo a seguir, consideramos um cenário no qual o usuário JOHN no computador A deseja obter os tamanhos dos arquivos que contêm a palavra "Microsoft" do conjunto de documentos armazenados no servidor X no sistema de catálogo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="c3012-4773">Vamos supor que o computador A está executando um sistema operacional Windows XP de 32 bits e o computador X está executando um sistema operacional Windows Server 2003 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c3012-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="c3012-4774">O usuário inicia um aplicativo de pesquisa e insere a consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3012-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="c3012-4775">O aplicativo, por sua vez, passa a consulta de pesquisa para o cliente de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c3012-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="c3012-4776">O cliente de protocolo estabelece uma conexão com o servidor de indexação X. O cliente de protocolo usa o pipe de pipe nomeado \\ \\ CI \_ SKADS para se conectar ao servidor X sobre SMB.</span><span class="sxs-lookup"><span data-stu-id="c3012-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="c3012-4777">Em seguida, o cliente de protocolo prepara uma mensagem CPMConnectIn com os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c3012-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="c3012-4778">O cabeçalho da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4779">**\_ msg** é definido como 0x000000C8, indicando que se trata de uma mensagem CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="c3012-4780">o **\_ status** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3012-4781">**\_ ulChecksum** contém a soma de verificação, calculada conforme especificado na seção 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="c3012-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="c3012-4782">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3012-4783">O corpo da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4784">**\_ iClientVersion** é definido como 0x00000008, indicando que o servidor é para validar o campo de soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="c3012-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="c3012-4785">**\_ fClientIsRemote** é definido como 0x00000001, indicando que o servidor é um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="c3012-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="c3012-4786">**\_ cbBlob1** é definido como o tamanho, em bytes, dos campos cPropSet, PropertySet1 e PropertySet2 combinados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="c3012-4787">**\_ cbBlob2** é definido como 0x00000004 (ou seja, nenhum conjunto de propriedades extra).</span><span class="sxs-lookup"><span data-stu-id="c3012-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="c3012-4788">**MachineName** é definido como a.</span><span class="sxs-lookup"><span data-stu-id="c3012-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="c3012-4789">O **nome de usuário** é definido como João.</span><span class="sxs-lookup"><span data-stu-id="c3012-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="c3012-4790">**cPropSets** é definido como 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="c3012-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="c3012-4791">O campo **PropertySet1** é do tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="c3012-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="c3012-4792">A estrutura CDbPropSet que consiste no campo PropertySet1 é populada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="c3012-4793">O campo **GuidPropSet** é definido como A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ ext).</span><span class="sxs-lookup"><span data-stu-id="c3012-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="c3012-4794">o campo **cProperties** está definido como 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="c3012-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="c3012-4795">o campo **aProps** é uma matriz de estruturas CDbProp.</span><span class="sxs-lookup"><span data-stu-id="c3012-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="c3012-4796">Para o **elemento \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="c3012-4797">**PropId** é definido como 0X00000002 (DBPROP \_ CI \_ Catalog \_ name).</span><span class="sxs-lookup"><span data-stu-id="c3012-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="c3012-4798">**DBPROPOPTIONS** é definido como 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="c3012-4799">**DBPROPSTATUS** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3012-4800">Para o elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3012-4801">**eKind** é definido como 0X00000001 (DBKIND \_ GUID \_ Propid)</span><span class="sxs-lookup"><span data-stu-id="c3012-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="c3012-4802">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3012-4803">**ulID** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3012-4804">Para o elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="c3012-4805">**vType** é definido como 0X001F (VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="c3012-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="c3012-4806">**vValue** é definido como "System", o nome do catálogo desejado.</span><span class="sxs-lookup"><span data-stu-id="c3012-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="c3012-4807">Para o **elemento \[ aProps \] 1** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="c3012-4808">**PropId** é definido como 0x00000007 ( \_ tipo de \_ consulta CI DBPROP \_ )</span><span class="sxs-lookup"><span data-stu-id="c3012-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="c3012-4809">**DBPROPOPTIONS** é definido como 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="c3012-4810">**DBPROPSTATUS** é definido to0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="c3012-4811">Para o elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3012-4812">**eKind** é definido como 0X00000001 (DBKIND \_ GUID \_ Propid).</span><span class="sxs-lookup"><span data-stu-id="c3012-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="c3012-4813">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3012-4814">**ulID** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3012-4815">Para o elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="c3012-4816">**vType** é definido como 0X0003 (VT \_ i4).</span><span class="sxs-lookup"><span data-stu-id="c3012-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="c3012-4817">**vValue** é definido como 0x00000000 (CiNormal), o que significa que é uma consulta regular.</span><span class="sxs-lookup"><span data-stu-id="c3012-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="c3012-4818">Para o **elemento \[ aProps \] 2** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="c3012-4819">**PropId** é definido como 0x00000004 ( \_ sinalizadores de escopo de CI DBPROP \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="c3012-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="c3012-4820">**DBPROPOPTIONS** é definido como 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="c3012-4821">**DBPROPSTATUS** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3012-4822">Para o elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3012-4823">**eKind** é definido como 0X00000001 (DBKIND \_ GUID \_ Propid).</span><span class="sxs-lookup"><span data-stu-id="c3012-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="c3012-4824">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3012-4825">**ulID** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3012-4826">Para o elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="c3012-4827">**vType**: 0X1003 (VT \_ vector \| VT \_ i4)</span><span class="sxs-lookup"><span data-stu-id="c3012-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="c3012-4828">**vValue**: 0x00000001/0x00000001 (um elemento com valor 1), significando subpastas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="c3012-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="c3012-4829">Para o **elemento \[ aProps \] 3** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="c3012-4830">**PropId**: 0X00000003 (DBPROP \_ CI \_ include \_ escopos)</span><span class="sxs-lookup"><span data-stu-id="c3012-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="c3012-4831">**DBPROPOPTIONS**: 0x0000000</span><span class="sxs-lookup"><span data-stu-id="c3012-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="c3012-4832">**DBPROPSTATUS**: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="c3012-4833">Para o elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3012-4834">**eKind** é definido como 0X00000001 (DBKIND \_ GUID \_ Propid).</span><span class="sxs-lookup"><span data-stu-id="c3012-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="c3012-4835">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3012-4836">**ulID** é definido como 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="c3012-4837">Para o elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="c3012-4838">**vType** é definido como 0x101F (o LPWStr do ' VT \_ vector \| VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="c3012-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="c3012-4839">**vValue** é definido como 0x00000001/0x00000002/" \\ " (um elemento com uma cadeia de caracteres de 2 caracteres terminada em nulo), o que significa o escopo raiz.</span><span class="sxs-lookup"><span data-stu-id="c3012-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="c3012-4840">O campo **PropertySet2** é do tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="c3012-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="c3012-4841">A estrutura CDbPropSet que consiste no campo PropertySet1 é populada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="c3012-4842">**GuidPropSet** é definido como AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ ext).</span><span class="sxs-lookup"><span data-stu-id="c3012-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="c3012-4843">o campo **cProperties** está definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="c3012-4844">O campo **aProps** é uma matriz de estruturas CDbProp.</span><span class="sxs-lookup"><span data-stu-id="c3012-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="c3012-4845">Para o **elemento \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="c3012-4846">**PropId** é definido como 0x00000002 ( \_ máquina DBPROP).</span><span class="sxs-lookup"><span data-stu-id="c3012-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="c3012-4847">**DBPROPOPTIONS** é definido como 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="c3012-4848">**DBPROPSTATUS** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3012-4849">Para o elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3012-4850">**eKind** é definido como 0X00000001 (DBKIND \_ GUID \_ Propid),</span><span class="sxs-lookup"><span data-stu-id="c3012-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="c3012-4851">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="c3012-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3012-4852">**ulID** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3012-4853">Para o elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="c3012-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="c3012-4854">**vType**: 0X0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="c3012-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="c3012-4855">**vValue**: 0x04/"X" (4 bytes/cadeia de caracteres Unicode terminada em nulo), significando "X"-nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="c3012-4856">o campo **cExtPropSet** está definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3012-4857">a matriz **aPropertySets** não existe.</span><span class="sxs-lookup"><span data-stu-id="c3012-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="c3012-4858">Vários campos de preenchimento são preenchidos conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="c3012-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="c3012-4859">A mensagem é enviada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="c3012-4860">O servidor verifica se o **\_ ulChecksum** está correto, verifica se o usuário está autorizado a fazer essa solicitação e responde com uma mensagem CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="c3012-4861">O cabeçalho da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4862">**\_ msg** é definido como 0x000000C8, indicando que se trata de uma mensagem CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="c3012-4863">**\_ status** é definido como 0x0000000 indicando êxito.</span><span class="sxs-lookup"><span data-stu-id="c3012-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="c3012-4864">**\_ ulChecksum** é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="c3012-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="c3012-4865">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3012-4866">O corpo da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4867">o campo **\_ serverVersion** é definido como 0X00000007 (windows XP de 32 bits ou 32 bits Windows Server 2003).</span><span class="sxs-lookup"><span data-stu-id="c3012-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="c3012-4868">os campos **\_ reservados** são preenchidos com dados arbitrários.</span><span class="sxs-lookup"><span data-stu-id="c3012-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="c3012-4869">O cliente prepara uma mensagem CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="c3012-4870">O cabeçalho da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4871">**\_ msg** é definido como 0x000000CA, indicando que se trata de uma mensagem CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="c3012-4872">o **\_ status** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3012-4873">**\_ ulChecksum** contém a soma de verificação, computada de acordo com 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="c3012-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="c3012-4874">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3012-4875">O corpo da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4876">O campo **tamanho** é definido como o tamanho do restante da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="c3012-4877">O campo **CColumnSetPresent** é definido como 0x01.</span><span class="sxs-lookup"><span data-stu-id="c3012-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="c3012-4878">O campo **ColumnSet** é do tipo CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="c3012-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="c3012-4879">A estrutura CColumnSet composta por esse campo é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="c3012-4880">o campo **\_ contagem** é definido como 0x00000001 indicando que uma coluna é retornada.</span><span class="sxs-lookup"><span data-stu-id="c3012-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="c3012-4881">a matriz de **índices** é 0x00000000 indicando a primeira entrada em \_ aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="c3012-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="c3012-4882">O campo **CRestrictionPresent** é definido como 0x01, indicando que o campo de **restrição** está presente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="c3012-4883">O campo de **restrição** é do tipo CRestriction e é definido como:</span><span class="sxs-lookup"><span data-stu-id="c3012-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="c3012-4884">**\_ ulType** é definido como 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="c3012-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="c3012-4885">**\_ Weight** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3012-4886">O restante do campo contém uma estrutura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="c3012-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="c3012-4887">A **\_ Propriedade** é definida como GUID B725F130-47EF-101A-A5F1-02608c9eebac/0X00000001 (para PRSPEC \_ Propid)/0x13, que representa o corpo do documento.</span><span class="sxs-lookup"><span data-stu-id="c3012-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="c3012-4888">**\_ CC** é definido como 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="c3012-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="c3012-4889">**\_ pwcsphrase** é definido como a cadeia de caracteres "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="c3012-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="c3012-4890">**\_ LCID** é definido como 0X409 (para inglês).</span><span class="sxs-lookup"><span data-stu-id="c3012-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="c3012-4891">**\_ ulGenerateMethod** é definido como 0x00000000 (correspondência exata).</span><span class="sxs-lookup"><span data-stu-id="c3012-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="c3012-4892">**CSortPresent** é definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3012-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="c3012-4893">**CCategorizationSetPresent** é definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3012-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="c3012-4894">Conjunto de **linhas** é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="c3012-4895">**\_ uBooleanOptions** é definido como 0x00000001 (sequencial).</span><span class="sxs-lookup"><span data-stu-id="c3012-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="c3012-4896">**\_ ulMaxOpenRows** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3012-4897">**\_ ulMemoryUsage** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3012-4898">\_**cMaxResults** é definido como 0x00000100 (retorna no máximo 256 linhas).</span><span class="sxs-lookup"><span data-stu-id="c3012-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="c3012-4899">**\_ cCmdTimeOut** é definido como 0x00000000 (nunca Timeout).</span><span class="sxs-lookup"><span data-stu-id="c3012-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="c3012-4900">**PidMapper** é definido como:</span><span class="sxs-lookup"><span data-stu-id="c3012-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="c3012-4901">**\_ Count** está definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="c3012-4902">**\_ aPropSpec** é definido como GUID B725F130-47EF-101A-a5-F1-02608C9EEBAC/0X00000001 (para PRSPEC \_ Propid)/0x0000000c que representa a propriedade tamanho do arquivo do Windows.</span><span class="sxs-lookup"><span data-stu-id="c3012-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="c3012-4903">O servidor o processa e responde com uma mensagem CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="c3012-4904">O cabeçalho da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4905">**\_ msg** é definido como 0x000000CA, indicando que se trata de uma mensagem CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="c3012-4906">o **\_ status** é definido como êxito.</span><span class="sxs-lookup"><span data-stu-id="c3012-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="c3012-4907">**\_ ulChecksum** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="c3012-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="c3012-4908">**\_ ulReserved2** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="c3012-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="c3012-4909">O corpo da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4910">**\_ fTrueSeqeuntial** é definido como 0x00000000, indicando que a consulta pode usar um índice.</span><span class="sxs-lookup"><span data-stu-id="c3012-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="c3012-4911">**\_ fWorkIdUnique** é definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="c3012-4912">A matriz **aCursors** contém apenas um elemento, representando um identificador de cursor para essa consulta.</span><span class="sxs-lookup"><span data-stu-id="c3012-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="c3012-4913">O valor depende do estado do servidor.</span><span class="sxs-lookup"><span data-stu-id="c3012-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="c3012-4914">Vamos supor que o valor retornado seja 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="c3012-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="c3012-4915">O cliente emite uma mensagem de solicitação CPMSetBindingsIn para definir o formato de uma linha.</span><span class="sxs-lookup"><span data-stu-id="c3012-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="c3012-4916">O cabeçalho da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4917">**\_ msg** é definido como 0x000000D0, indicando que se trata de uma mensagem CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="c3012-4918">o **\_ status** é definido como êxito.</span><span class="sxs-lookup"><span data-stu-id="c3012-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="c3012-4919">**\_ ulChecksum** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="c3012-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="c3012-4920">**\_ ulReserved2** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="c3012-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="c3012-4921">O corpo da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4922">**\_ hCursor** é definido como 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="c3012-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="c3012-4923">**\_ cbRow** é definido como 0x10 (grande o suficiente para ajustar as colunas).</span><span class="sxs-lookup"><span data-stu-id="c3012-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="c3012-4924">**\_ cbBindingDesc** é definido como o tamanho dos campos **\_ cColumns** e **\_ aColumns** combinados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="c3012-4925">**\_ cColumns** é definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="c3012-4926">a matriz **\_ aColumns** está definida para conter uma estrutura CTableColumn que contém:</span><span class="sxs-lookup"><span data-stu-id="c3012-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="c3012-4927">**\_ PropSpec** é definido como GUID b725f130-47ef-101A-a5-F1-02608c9eebac/0X00000001 (para PRSPEC \_ Propid)/0x0000000c que representa a propriedade tamanho do arquivo do Windows.</span><span class="sxs-lookup"><span data-stu-id="c3012-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="c3012-4928">**\_ vType** é definido como 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="c3012-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="c3012-4929">**\_ ValueUsed** é definido como 0x01 (coluna transferida na linha).</span><span class="sxs-lookup"><span data-stu-id="c3012-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="c3012-4930">**\_ ValueOffset** é definido como 0x0002 (no início da linha).</span><span class="sxs-lookup"><span data-stu-id="c3012-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="c3012-4931">**\_ Values** é definido como 0x08 (tamanho de um VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="c3012-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="c3012-4932">**\_ StatusUsed** é definido como 0x01.</span><span class="sxs-lookup"><span data-stu-id="c3012-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="c3012-4933">**\_ StatusOffset** é definido como 0x0A.</span><span class="sxs-lookup"><span data-stu-id="c3012-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="c3012-4934">**\_ LengthUsed** é definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3012-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="c3012-4935">O servidor o processa e responde com uma mensagem CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="c3012-4936">O cabeçalho da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4937">**\_ msg** está definido como 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="c3012-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="c3012-4938">o **\_ status** é definido como êxito.</span><span class="sxs-lookup"><span data-stu-id="c3012-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="c3012-4939">**\_ ulChecksum** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="c3012-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="c3012-4940">**\_ ulReserved2** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="c3012-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="c3012-4941">O cliente emite uma mensagem de solicitação CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="c3012-4942">Vamos supor que o cliente esteja preparado para aceitar 100 linhas neste ponto e as queira em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="c3012-4943">O cabeçalho da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4944">**\_ msg** é definido como 0x000000CC, indicando que se trata de uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="c3012-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="c3012-4945">o **\_ status** é definido como 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3012-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="c3012-4946">**\_ ulChecksum** contém a soma de verificação, computada de acordo com a seção 0.</span><span class="sxs-lookup"><span data-stu-id="c3012-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="c3012-4947">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3012-4948">O corpo da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4949">**\_ hCursor** é definido como 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="c3012-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="c3012-4950">**\_ cRowsToTransfer** é definido como 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="c3012-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="c3012-4951">**\_ cRowWidth** é definido como 0x00000010 (de associações).</span><span class="sxs-lookup"><span data-stu-id="c3012-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="c3012-4952">**\_ cbSeek** é definido como 0x14, que é o tamanho dos campos ETYPE, \_ chapt e CRowSeekNext combinados.</span><span class="sxs-lookup"><span data-stu-id="c3012-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="c3012-4953">**\_ cbReserved** é definido como 0x18 (0x14 Plus \_ cbSeek).</span><span class="sxs-lookup"><span data-stu-id="c3012-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="c3012-4954">**\_ cbReadBuffer** é definido como 0x800 (0x64 \* 0x10 arredondado para o próximo múltiplo de 0x200).</span><span class="sxs-lookup"><span data-stu-id="c3012-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="c3012-4955">**\_ ulClientBase** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3012-4956">**\_ fBwdfetch** é definido como 0x00000000 indicando que as linhas devem ser buscadas na ordem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="c3012-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="c3012-4957">**ETYPE** é definido como 0x0000001 indicando que o cliente deseja as próximas linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="c3012-4958">o **\_ chapt** é definido como 0 (não é um resultado do capítulo).</span><span class="sxs-lookup"><span data-stu-id="c3012-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="c3012-4959">**SeekDescription** é definido como CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="c3012-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="c3012-4960">A estrutura CRowSeekNext contém os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c3012-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="c3012-4961">**CiTblChapt** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3012-4962">**\_ hRegion** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3012-4963">**\_ cSkip** é definido como 0, indicando que o cliente não deseja ignorar linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="c3012-4964">O servidor o processa e responde com uma mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="c3012-4965">Vamos supor que o servidor encontrou 100 documentos que contêm a palavra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="c3012-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="c3012-4966">O cabeçalho da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4967">**\_ msg** é definido como 0x000000CC, indicando que se trata de uma mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="c3012-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="c3012-4968">o **\_ status** é definido como êxito.</span><span class="sxs-lookup"><span data-stu-id="c3012-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="c3012-4969">**\_ ulChecksum** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3012-4970">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3012-4971">O corpo da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4972">**\_ CRowsReturned** é definido como 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="c3012-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="c3012-4973">**ETYPE** está definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3012-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="c3012-4974">o **\_ chapt** é definido como 0x00000000 (não um resultado de capítulo).</span><span class="sxs-lookup"><span data-stu-id="c3012-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="c3012-4975">**SeekDescription** contém uma estrutura CRowSeekNext, populada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="c3012-4976">**CiTblChapt** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3012-4977">**\_ hRegion** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3012-4978">**\_ cSkip** é definido como 0, indicando que o cliente não deseja ignorar linhas.</span><span class="sxs-lookup"><span data-stu-id="c3012-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="c3012-4979">As **linhas** contêm o tamanho dos documentos 100 que contêm a palavra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="c3012-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="c3012-4980">Como esses são dados de tamanho fixo, eles são simplesmente estruturados como uma lista de 100, inteiros não assinados de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c3012-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="c3012-4981">O cliente envia uma mensagem CPMDisconnect para encerrar a conexão.</span><span class="sxs-lookup"><span data-stu-id="c3012-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="c3012-4982">O cabeçalho da mensagem é preenchido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3012-4983">**\_ msg** é definido como 0x000000C9, indicando que se trata de uma mensagem CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="c3012-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="c3012-4984">o **\_ status** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3012-4985">**\_ ulChecksum** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="c3012-4986">O servidor processa a mensagem e remove todo o estado do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3012-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="c3012-4987">4,2 exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3012-4987">4.2 Example 2</span></span>

<span data-ttu-id="c3012-4988">No exemplo anterior, a consulta era bem simples.</span><span class="sxs-lookup"><span data-stu-id="c3012-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="c3012-4989">Agora, vamos considerar uma consulta um pouco mais complexa.</span><span class="sxs-lookup"><span data-stu-id="c3012-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="c3012-4990">Vamos supor que o usuário deseja recuperar o tamanho dos documentos que contêm as duas palavras a seguir: "Microsoft" e "Office".</span><span class="sxs-lookup"><span data-stu-id="c3012-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="c3012-4991">Isso é especificado alterando o campo de restrição contido na mensagem CPMCreateQueryIn enviada na etapa 5 da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3012-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="c3012-4992">O campo de **restrição** é do tipo CRestriction e é definido como:</span><span class="sxs-lookup"><span data-stu-id="c3012-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="c3012-4993">**\_ ulType** é definido como 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="c3012-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="c3012-4994">**\_ Weight** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="c3012-4995">O restante do campo contém uma estrutura CNodeRestriction:</span><span class="sxs-lookup"><span data-stu-id="c3012-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="c3012-4996">**\_ cNode** é definido como 0x00000002, indicando que há dois nós na matriz paNode.</span><span class="sxs-lookup"><span data-stu-id="c3012-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="c3012-4997">O campo **\_ paNode** é uma matriz de duas estruturas CRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3012-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="c3012-4998">**\_ paNode \[ 0 \]** contém:</span><span class="sxs-lookup"><span data-stu-id="c3012-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="c3012-4999">**\_ ulType** é definido como 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="c3012-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="c3012-5000">**\_ Weight** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3012-5001">O restante do campo contém uma estrutura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="c3012-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="c3012-5002">A **\_ Propriedade** é definida como GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (para PRSPEC \_ Propid)/0x13.</span><span class="sxs-lookup"><span data-stu-id="c3012-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="c3012-5003">**\_ CC** é definido como 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="c3012-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="c3012-5004">**\_ pwcsphrase** é definido como a cadeia de caracteres "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="c3012-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="c3012-5005">**\_ LCID** é definido como 0X409 (para inglês).</span><span class="sxs-lookup"><span data-stu-id="c3012-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="c3012-5006">**\_ ulGenerateMethod** é definido como 0x00000000 (correspondência exata).</span><span class="sxs-lookup"><span data-stu-id="c3012-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="c3012-5007">**\_ paNode \[ 1 \]** contém:</span><span class="sxs-lookup"><span data-stu-id="c3012-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="c3012-5008">**\_ ulType** é definido como 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="c3012-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="c3012-5009">**\_ Weight** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3012-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3012-5010">O restante do campo contém uma estrutura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="c3012-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="c3012-5011">A **\_ Propriedade** é definida como GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (para PRSPEC \_ Propid)/0x13.</span><span class="sxs-lookup"><span data-stu-id="c3012-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="c3012-5012">**\_ CC** é definido como 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="c3012-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="c3012-5013">**\_ pwcsphrase** é definido como a cadeia de caracteres "Office".</span><span class="sxs-lookup"><span data-stu-id="c3012-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="c3012-5014">**\_ LCID** é definido como 0X409 (para inglês).</span><span class="sxs-lookup"><span data-stu-id="c3012-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="c3012-5015">**\_ ulGenerateMethod** é definido como 0x00000000 (correspondência exata).</span><span class="sxs-lookup"><span data-stu-id="c3012-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="c3012-5016">5 Segurança</span><span class="sxs-lookup"><span data-stu-id="c3012-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="c3012-5017">5.1 Considerações de segurança para implementadores</span><span class="sxs-lookup"><span data-stu-id="c3012-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="c3012-5018">Implementações de indexação que indexam conteúdo seguro devem considerar o uso do contexto de usuário fornecido pelo SMB \[ MS-SMB \] para cortar os resultados da pesquisa e retornar somente aqueles acessíveis ao chamador.</span><span class="sxs-lookup"><span data-stu-id="c3012-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="c3012-5019">5.2 Índice de parâmetros de segurança</span><span class="sxs-lookup"><span data-stu-id="c3012-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="c3012-5020">Parâmetro de segurança</span><span class="sxs-lookup"><span data-stu-id="c3012-5020">Security Parameter</span></span>  | <span data-ttu-id="c3012-5021">Seção</span><span class="sxs-lookup"><span data-stu-id="c3012-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="c3012-5022">Nível de representação</span><span class="sxs-lookup"><span data-stu-id="c3012-5022">Impersonation level</span></span> | <span data-ttu-id="c3012-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="c3012-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="c3012-5024">6 índice de comportamento de versão específica</span><span class="sxs-lookup"><span data-stu-id="c3012-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="c3012-5025">Comportamento específico da versão</span><span class="sxs-lookup"><span data-stu-id="c3012-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="c3012-5026">Seção</span><span class="sxs-lookup"><span data-stu-id="c3012-5026">Section</span></span>   | <span data-ttu-id="c3012-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c3012-5027">Windows 2000</span></span> | <span data-ttu-id="c3012-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c3012-5028">Windows XP</span></span> | <span data-ttu-id="c3012-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3012-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="c3012-5030">Esse protocolo é implementado no Windows 2000, no Windows XP, no Windows Server 2003 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3012-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="c3012-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="c3012-5031">1.3.2</span></span>     | <span data-ttu-id="c3012-5032">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5032">X</span></span>            | <span data-ttu-id="c3012-5033">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5033">X</span></span>          | <span data-ttu-id="c3012-5034">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5034">X</span></span>                   |
| <span data-ttu-id="c3012-5035">Normalmente, os aplicativos interagem com um wrapper de interface OLE DB</span><span class="sxs-lookup"><span data-stu-id="c3012-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="c3012-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="c3012-5036">1.4</span></span>       | <span data-ttu-id="c3012-5037">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5037">X</span></span>            | <span data-ttu-id="c3012-5038">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5038">X</span></span>          | <span data-ttu-id="c3012-5039">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5039">X</span></span>                   |
| <span data-ttu-id="c3012-5040">Valores de NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="c3012-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="c3012-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="c3012-5041">1.8</span></span>       | <span data-ttu-id="c3012-5042">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5042">X</span></span>            | <span data-ttu-id="c3012-5043">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5043">X</span></span>          | <span data-ttu-id="c3012-5044">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5044">X</span></span>                   |
| <span data-ttu-id="c3012-5045">O cliente define o \_ campo status em cada cabeçalho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3012-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="c3012-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="c3012-5046">2.2.2</span></span>     | <span data-ttu-id="c3012-5047">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5047">X</span></span>            | <span data-ttu-id="c3012-5048">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5048">X</span></span>          | <span data-ttu-id="c3012-5049">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5049">X</span></span>                   |
| <span data-ttu-id="c3012-5050">o valor de cPendingScans geralmente é zero</span><span class="sxs-lookup"><span data-stu-id="c3012-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="c3012-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="c3012-5051">2.2.3.1</span></span>   | <span data-ttu-id="c3012-5052">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5052">X</span></span>            | <span data-ttu-id="c3012-5053">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5053">X</span></span>          | <span data-ttu-id="c3012-5054">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5054">X</span></span>                   |
| <span data-ttu-id="c3012-5055">valor de iClientVersion</span><span class="sxs-lookup"><span data-stu-id="c3012-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="c3012-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="c3012-5056">2.2.3.6</span></span>   | <span data-ttu-id="c3012-5057">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5057">X</span></span>            | <span data-ttu-id="c3012-5058">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5058">X</span></span>          | <span data-ttu-id="c3012-5059">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5059">X</span></span>                   |
| <span data-ttu-id="c3012-5060">\_valor de cbChunk</span><span class="sxs-lookup"><span data-stu-id="c3012-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="c3012-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="c3012-5061">2.2.3.19</span></span>  | <span data-ttu-id="c3012-5062">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5062">X</span></span>            | <span data-ttu-id="c3012-5063">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5063">X</span></span>          | <span data-ttu-id="c3012-5064">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5064">X</span></span>                   |
| <span data-ttu-id="c3012-5065">endereços de memória de 32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="c3012-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="c3012-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="c3012-5066">3.2.4.2.4</span></span> | <span data-ttu-id="c3012-5067">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5067">X</span></span>            | <span data-ttu-id="c3012-5068">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5068">X</span></span>          | <span data-ttu-id="c3012-5069">X</span><span class="sxs-lookup"><span data-stu-id="c3012-5069">X</span></span>                   |



 

 

 





