---
title: Protocolo de serviços de indexação de conteúdo
description: Este documento é uma especificação do Protocolo de Serviço de Indexação de Conteúdo.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14573dac5a7a6818234c086d05b52e5b81c2a1c1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119731"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="6dadd-103">Protocolo de serviços de indexação de conteúdo</span><span class="sxs-lookup"><span data-stu-id="6dadd-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="6dadd-104">O Windows Desktop Search 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6dadd-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6dadd-105">Em versões posteriores, use [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6dadd-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="6dadd-106">Especificação de protocolo, versão 0.12</span><span class="sxs-lookup"><span data-stu-id="6dadd-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="6dadd-107">1 Introdução</span><span class="sxs-lookup"><span data-stu-id="6dadd-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="6dadd-108">1.1 Glossário</span><span class="sxs-lookup"><span data-stu-id="6dadd-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="6dadd-109">1.2 Referências</span><span class="sxs-lookup"><span data-stu-id="6dadd-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="6dadd-110">1.3 Visão geral do protocolo (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="6dadd-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="6dadd-111">1.4 Relacionamento com outros protocolos</span><span class="sxs-lookup"><span data-stu-id="6dadd-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="6dadd-112">1.5 Pré-requisitos e pré-condições</span><span class="sxs-lookup"><span data-stu-id="6dadd-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="6dadd-113">1.6 Applicability Statement</span><span class="sxs-lookup"><span data-stu-id="6dadd-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="6dadd-114">1.7 Controle de versão e negociação de capacidade</span><span class="sxs-lookup"><span data-stu-id="6dadd-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="6dadd-115">1.8 Campos extensíveis para fornecedor</span><span class="sxs-lookup"><span data-stu-id="6dadd-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="6dadd-116">1.9 Atribuições standard</span><span class="sxs-lookup"><span data-stu-id="6dadd-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="6dadd-117">2 Mensagens</span><span class="sxs-lookup"><span data-stu-id="6dadd-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="6dadd-118">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="6dadd-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="6dadd-119">2.2 Sintaxe da mensagem</span><span class="sxs-lookup"><span data-stu-id="6dadd-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="6dadd-120">3 Detalhes do protocolo</span><span class="sxs-lookup"><span data-stu-id="6dadd-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="6dadd-121">3.1 Detalhes do servidor</span><span class="sxs-lookup"><span data-stu-id="6dadd-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="6dadd-122">3.2 Detalhes do cliente</span><span class="sxs-lookup"><span data-stu-id="6dadd-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="6dadd-123">4 Exemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="6dadd-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="6dadd-124">4.1 Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6dadd-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="6dadd-125">4.2 Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6dadd-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="6dadd-126">5 Segurança</span><span class="sxs-lookup"><span data-stu-id="6dadd-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="6dadd-127">5.1 Considerações de segurança para implementadores</span><span class="sxs-lookup"><span data-stu-id="6dadd-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="6dadd-128">5.2 Índice de parâmetros de segurança</span><span class="sxs-lookup"><span data-stu-id="6dadd-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="6dadd-129">6 Índice de comportamento específico da versão</span><span class="sxs-lookup"><span data-stu-id="6dadd-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="6dadd-130">Este documento é uma especificação do Protocolo de Serviço de Indexação de Conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="6dadd-131">A documentação do WSPP (Workgroup Server Protocol Program) destina-se a ser usada em conjunto com a documentação de padrões públicos, a arte de programação de rede e os conceitos de sistemas distribuídos do grupo de trabalho do Windows e pressupo que o leitor está familiarizado com o material mencionado acima ou tem acesso imediato a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="6dadd-132">Uma especificação de protocolo WSPP não exige o uso de ferramentas de programação da Microsoft ou ambientes de programação para que um licença desenvolva uma implementação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="6dadd-133">Os licenças que têm acesso a ambientes e ferramentas de programação da Microsoft são gratuitos para tirar proveito deles.</span><span class="sxs-lookup"><span data-stu-id="6dadd-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="6dadd-134">1 Introdução</span><span class="sxs-lookup"><span data-stu-id="6dadd-134">1 Introduction</span></span>

-   [<span data-ttu-id="6dadd-135">1.1 Glossário</span><span class="sxs-lookup"><span data-stu-id="6dadd-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="6dadd-136">1.2 Referências</span><span class="sxs-lookup"><span data-stu-id="6dadd-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="6dadd-137">1.3 Visão geral do protocolo (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="6dadd-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="6dadd-138">1.4 Relacionamento com outros protocolos</span><span class="sxs-lookup"><span data-stu-id="6dadd-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="6dadd-139">1.5 Pré-requisitos e pré-condições</span><span class="sxs-lookup"><span data-stu-id="6dadd-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="6dadd-140">1.6 Applicability Statement</span><span class="sxs-lookup"><span data-stu-id="6dadd-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="6dadd-141">1.7 Controle de versão e negociação de capacidade</span><span class="sxs-lookup"><span data-stu-id="6dadd-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="6dadd-142">1.8 Campos extensíveis para fornecedor</span><span class="sxs-lookup"><span data-stu-id="6dadd-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="6dadd-143">1.9 Atribuições standard</span><span class="sxs-lookup"><span data-stu-id="6dadd-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="6dadd-144">1.1 Glossário</span><span class="sxs-lookup"><span data-stu-id="6dadd-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="6dadd-145">Os seguintes termos são definidos na seção Glossário \[ do MS-SYS: \]</span><span class="sxs-lookup"><span data-stu-id="6dadd-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="6dadd-146">GUID</span><span class="sxs-lookup"><span data-stu-id="6dadd-146">GUID</span></span>
> -   <span data-ttu-id="6dadd-147">Little Endian</span><span class="sxs-lookup"><span data-stu-id="6dadd-147">Little Endian</span></span>
> -   <span data-ttu-id="6dadd-148">Pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="6dadd-148">Named Pipe</span></span>
> -   <span data-ttu-id="6dadd-149">Caminho</span><span class="sxs-lookup"><span data-stu-id="6dadd-149">Path</span></span>

 

<span data-ttu-id="6dadd-150">**Associação:** uma solicitação para incluir uma coluna **específica** em um conjuntos **de linhas retornado.**</span><span class="sxs-lookup"><span data-stu-id="6dadd-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="6dadd-151">A **associação** especifica uma propriedade a ser incluída nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="6dadd-152">**Indicador:** um marcador que identifica exclusivamente uma linha dentro de um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="6dadd-153">**Catálogo:** a unidade de nível mais alto da organização no serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="6dadd-154">Ele representa um conjunto de documentos indexados nos quais as consultas podem ser executadas usando o Protocolo de Serviço de Indexação de Conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="6dadd-155">**Categoria:** um grupo hierárquico de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="6dadd-156">Por exemplo, um resultado de consulta que contém colunas de autor e título pode ser categorizado com base no autor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="6dadd-157">Cada grupo de linhas que contém o mesmo valor para autor constituiria uma categoria.</span><span class="sxs-lookup"><span data-stu-id="6dadd-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="6dadd-158">**Capítulo** : um intervalo **de linhas dentro** de um conjunto de **linhas** .</span><span class="sxs-lookup"><span data-stu-id="6dadd-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="6dadd-159">**Coluna**: o contêiner para um único tipo de informação em uma **linha** .</span><span class="sxs-lookup"><span data-stu-id="6dadd-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="6dadd-160">As colunas são mapeadas para nomes de propriedade e  especificam quais propriedades são usadas para os elementos da árvore de comandos da consulta **de** pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="6dadd-161">**Árvore de** Comandos: uma combinação de **restrições,** **categorias** e **ordens de classificação** especificadas para a consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="6dadd-162">**Cursor**: uma entidade usada como um  mecanismo para trabalhar  com uma linha ou um pequeno bloco de linhas por vez em um conjunto de dados retornados em um conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="6dadd-163">Um **cursor** é posicionado em uma única **linha dentro** do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="6dadd-164">Depois que **o cursor** é posicionado em uma linha, as operações podem ser **executadas** nessa linha **ou** em um bloco de linhas começando nessa posição.</span><span class="sxs-lookup"><span data-stu-id="6dadd-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="6dadd-165">**Identificador:** um token que pode ser usado para identificar e acessar **cursores** , **capítulos** e **indicadores** .</span><span class="sxs-lookup"><span data-stu-id="6dadd-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="6dadd-166">**Índice:** uma estrutura persistente que contém o conteúdo de texto retirado dos arquivos por um **serviço de indexação** .</span><span class="sxs-lookup"><span data-stu-id="6dadd-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="6dadd-167">Isso inclui a lista de palavras, que são armazenadas junto com o nome do arquivo que contém, o local da palavra e **a localidade** .</span><span class="sxs-lookup"><span data-stu-id="6dadd-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="6dadd-168">**Indexação:** o processo de extrair texto e propriedades de arquivos e armazenar os valores extraídos nos índices **(para** texto) e o **cache** de propriedades (para propriedades).</span><span class="sxs-lookup"><span data-stu-id="6dadd-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="6dadd-169">**Serviço de Indexação:** um serviço que cria **catálogos indexados** para o conteúdo e as propriedades dos sistemas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="6dadd-170">Os aplicativos podem pesquisar nos catálogos informações dos arquivos no sistema de arquivos indexado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="6dadd-171">**Localidade :** um identificador, conforme especificado no \[ Apêndice A do MS-GPSI, que especifica as \] preferências relacionadas ao idioma.</span><span class="sxs-lookup"><span data-stu-id="6dadd-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="6dadd-172">Essas preferências indicam como datas e horas devem ser formatadas, os itens devem ser ordenados em ordem alfabética, cadeias de caracteres devem ser comparadas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6dadd-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="6dadd-173">**Consulta de linguagem natural:** uma consulta construída usando linguagem humana em vez da sintaxe de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="6dadd-174">**Palavra de** ruído: uma palavra ignorada pelo serviço  de indexação quando presente nas restrições especificadas para a consulta de pesquisa porque ela tem pouco valor discriminatório.</span><span class="sxs-lookup"><span data-stu-id="6dadd-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="6dadd-175">Os exemplos em inglês incluem "a", "and" e "the".</span><span class="sxs-lookup"><span data-stu-id="6dadd-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="6dadd-176">**Cache de** propriedades: um cache de propriedades de arquivo extraídas por um **serviço de indexação** .</span><span class="sxs-lookup"><span data-stu-id="6dadd-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="6dadd-177">**Indexação de** propriedade: o  processo  de criação de um índice de propriedades de tipo de valor de um documento, incluindo autor, assunto, tipo, contagem de palavras, contagem de páginas impressas e qualquer outra propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="6dadd-178">**Restrição:** um conjunto de condições que um arquivo deve atender para ser incluído nos resultados da pesquisa retornados pelo serviço de **indexação** em resposta a uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="6dadd-179">Uma **restrição** restringe o foco de uma consulta de pesquisa, limitando os arquivos que o serviço de **indexação** incluirá nos resultados da pesquisa somente àqueles que corresponderem às condições.</span><span class="sxs-lookup"><span data-stu-id="6dadd-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="6dadd-180">**Linha**: a coleção de **colunas** , que contém os valores de propriedade  que descrevem um único arquivo do conjunto de arquivos que corresponderam às restrições especificadas na consulta de pesquisa enviada ao serviço **de indexação** .</span><span class="sxs-lookup"><span data-stu-id="6dadd-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="6dadd-181">**Conjunto de** linhas: um conjunto **de linhas retornado** nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="6dadd-182">**Ordem de** Classificação: o conjunto de regras em uma consulta de pesquisa que define a ordenação de linhas no resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="6dadd-183">Cada regra consiste em uma propriedade (nome, tamanho etc.) e uma direção para a ordenação (crescente ou decrescente).</span><span class="sxs-lookup"><span data-stu-id="6dadd-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="6dadd-184">Várias regras são aplicadas sequencialmente</span><span class="sxs-lookup"><span data-stu-id="6dadd-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="6dadd-185">**Propriedade de tipo de** texto: uma propriedade que descreve o conteúdo de um documento e tem apenas texto não formatado associado ao seu nome.</span><span class="sxs-lookup"><span data-stu-id="6dadd-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="6dadd-186">**Propriedade de tipo de** valor: uma propriedade que descreve um único atributo de um documento inteiro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="6dadd-187">Uma propriedade de tipo de valor tem uma ID de tipo de dados e um valor desse tipo de dados associado a seu nome.</span><span class="sxs-lookup"><span data-stu-id="6dadd-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="6dadd-188">**Raiz Virtual:** um caminho alternativo para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="6dadd-189">Uma pasta física pode ter zero ou mais raízes virtuais.</span><span class="sxs-lookup"><span data-stu-id="6dadd-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="6dadd-190">Os caminhos que começam com uma raiz virtual são chamados de caminhos virtuais.</span><span class="sxs-lookup"><span data-stu-id="6dadd-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="6dadd-191">Por exemplo, /server/vanityroot pode ser uma raiz virtual de C: \\ pasta web do \\ IIS1. \\</span><span class="sxs-lookup"><span data-stu-id="6dadd-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="6dadd-192">Em seguida, o arquivo C: pasta web do IIS1default.htm teria um caminho \\ \\ virtual de \\ \\ /server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="6dadd-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="6dadd-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** esses termos (em todos os limites) são usados conforme descrito em \[ RFC2119 \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="6dadd-194">Todas as instruções de comportamento opcional utilizam PODE, DEVERIA OU NÃO DEVERIA.</span><span class="sxs-lookup"><span data-stu-id="6dadd-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="6dadd-195">1.2 Referências</span><span class="sxs-lookup"><span data-stu-id="6dadd-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="6dadd-196">1.2.1 Referências normativas</span><span class="sxs-lookup"><span data-stu-id="6dadd-196">1.2.1 Normative References</span></span>

<span data-ttu-id="6dadd-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, outubro de 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="6dadd-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="6dadd-198">\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", junho de 2006.</span><span class="sxs-lookup"><span data-stu-id="6dadd-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="6dadd-199">\[MS-GPSI \] Microsoft Corporation, "extensão Política de Grupo de Instalação de Software", junho de 2006.</span><span class="sxs-lookup"><span data-stu-id="6dadd-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="6dadd-200">\[MS-SMB \] Microsoft Corporation, "Protocolo SMB (Bloco de Mensagens do Microsoft Server) e Extensões", maio de 2006.</span><span class="sxs-lookup"><span data-stu-id="6dadd-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="6dadd-201">\[MS-SYS \] Microsoft Corporation, "visão geral do sistema v4", julho de 2006.</span><span class="sxs-lookup"><span data-stu-id="6dadd-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="6dadd-202">\[Sale \] saltize, G., "processamento de texto automático: a análise de transformação e a recuperação de informações por computador", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="6dadd-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="6dadd-203">\[UNICODE \] consórcio Unicode, "o padrão Unicode, versão 2,0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="6dadd-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="6dadd-204">1.2.2 Referências informativas</span><span class="sxs-lookup"><span data-stu-id="6dadd-204">1.2.2 Informative References</span></span>

<span data-ttu-id="6dadd-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="6dadd-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="6dadd-206">\[MSDN-QUERYERR \] Microsoft Corporation, valores de Query-Execution, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="6dadd-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="6dadd-207">1,3 visão geral do protocolo (Sinopse)</span><span class="sxs-lookup"><span data-stu-id="6dadd-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="6dadd-208">Um **serviço de indexação** de conteúdo ajuda a organizar com eficiência os recursos extraídos de uma coleção de documentos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="6dadd-209">O CISP (Content Indexing Service Protocol) permite que um cliente se comunique com um servidor que hospeda um serviço de indexação para emitir consultas e permitir que um administrador gerencie o servidor de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="6dadd-210">Ao processar arquivos, um serviço de indexação analisa um conjunto de documentos e reorganiza seu conteúdo de forma que **as propriedades** desses documentos possam ser retornadas de forma eficiente em resposta a consultas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="6dadd-211">Uma coleção de documentos que podem ser consultados abrange um **Catálogo** .</span><span class="sxs-lookup"><span data-stu-id="6dadd-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="6dadd-212">Um catálogo pode conter um **índice** (para referência rápida a texto) e um **cache de propriedades** (para recuperação rápida de valores de propriedade).</span><span class="sxs-lookup"><span data-stu-id="6dadd-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="6dadd-213">Conceitualmente, um catálogo consiste em uma "tabela" lógica de propriedades com o texto ou o valor e a localidade correspondente armazenada em **colunas** da tabela.</span><span class="sxs-lookup"><span data-stu-id="6dadd-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="6dadd-214">Cada "linha" da tabela corresponde a um documento separado no escopo do catálogo e cada "coluna" da tabela corresponde a uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="6dadd-215">As tarefas específicas executadas pelo CISP são agrupadas em duas áreas funcionais:</span><span class="sxs-lookup"><span data-stu-id="6dadd-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="6dadd-216">Administração remota da indexação de catálogos de serviço,</span><span class="sxs-lookup"><span data-stu-id="6dadd-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="6dadd-217">Consulta remota de catálogos de serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="6dadd-218">Tarefas de administração remota do 1.3.1</span><span class="sxs-lookup"><span data-stu-id="6dadd-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="6dadd-219">O CISP habilita as seguintes tarefas de gerenciamento de catálogo do serviço de indexação de um cliente:</span><span class="sxs-lookup"><span data-stu-id="6dadd-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="6dadd-220">Consulte o estado atual de um catálogo de serviço de indexação no servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="6dadd-221">Atualize o estado de um catálogo de serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="6dadd-222">Inicie o processo de indexação para um determinado conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="6dadd-223">Inicie a otimização de um índice para melhorar o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="6dadd-224">Todas as tarefas de administração remota seguem um modelo simples de solicitação/resposta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="6dadd-225">Nenhum estado é mantido no cliente para qualquer chamada de administração e chamadas administrativas podem ser feitas em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="6dadd-226">Consulta remota 1.3.2</span><span class="sxs-lookup"><span data-stu-id="6dadd-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="6dadd-227">O CISP permite que os clientes executem consultas de pesquisa em um servidor remoto que hospeda um serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="6dadd-228">O envio de uma consulta de pesquisa é um processo de várias etapas iniciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="6dadd-229">As etapas são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="6dadd-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="6dadd-230">O cliente solicita uma conexão a um servidor que hospeda um serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="6dadd-231">O cliente envia os parâmetros para a consulta de pesquisa, que incluem:</span><span class="sxs-lookup"><span data-stu-id="6dadd-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="6dadd-232">As **restrições** para especificar quais documentos devem ser incluídos e/ou excluídos dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="6dadd-233">A ordem na qual os resultados da pesquisa devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="6dadd-234">As colunas a serem retornadas no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="6dadd-235">O número máximo de **linhas** que devem ser retornadas para a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="6dadd-236">O tempo máximo para a execução da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="6dadd-237">Depois que o servidor tiver confirmado a solicitação do cliente para iniciar a consulta, o cliente poderá solicitar informações de status sobre a consulta, mas essa não é uma etapa necessária.</span><span class="sxs-lookup"><span data-stu-id="6dadd-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="6dadd-238">O cliente especifica quais propriedades o servidor deve incluir nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="6dadd-239">O cliente solicita um conjunto de resultados do servidor e o servidor responde enviando ao cliente os valores de propriedade dos arquivos que foram incluídos nos resultados para a consulta de pesquisa do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="6dadd-240">Se o valor de uma propriedade for muito grande para caber em um único buffer de resposta, o servidor não enviará a propriedade, mas, em vez disso, definirá o status da propriedade como adiada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="6dadd-241">Em seguida, o cliente solicita o valor da propriedade separadamente usando uma série de solicitações para partes sucessivas do valor e, em seguida, retoma a solicitação de outros valores.</span><span class="sxs-lookup"><span data-stu-id="6dadd-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="6dadd-242">Depois que o cliente for concluído com a consulta de pesquisa e não exigir mais resultados adicionais, o cliente entrará em contato com o servidor para liberar a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="6dadd-243">Depois que o servidor tiver lançado a consulta, o cliente poderá enviar uma solicitação para desconectar-se do servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="6dadd-244">A conexão é fechada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-244">The connection is then closed.</span></span> <span data-ttu-id="6dadd-245">Como alternativa, o cliente pode emitir outra consulta e repetir a sequência da etapa 2.</span><span class="sxs-lookup"><span data-stu-id="6dadd-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="6dadd-246">Comportamento do Windows: esse protocolo é implementado no Windows 2000, no Windows XP, no Windows Server 2003 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6dadd-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="6dadd-247">1.4 Relacionamento com outros protocolos</span><span class="sxs-lookup"><span data-stu-id="6dadd-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="6dadd-248">O CISP se baseia no protocolo SMB \[ MS-SMB \] para transporte de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dadd-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="6dadd-249">Nenhum outro protocolo depende diretamente do protocolo de serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="6dadd-250">*Comportamento do Windows: normalmente, os aplicativos interagem com um wrapper de interface OLE DB \[ msdn-OLEDB \] (por exemplo, um cliente de protocolo) e não diretamente com o protocolo.*</span><span class="sxs-lookup"><span data-stu-id="6dadd-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="6dadd-251">1,5 pré-requisitos e pré-condições</span><span class="sxs-lookup"><span data-stu-id="6dadd-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="6dadd-252">Supõe-se que o cliente tenha obtido o nome do servidor e um nome de catálogo antes que esse protocolo seja invocado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="6dadd-253">Como um cliente faz isso está fora do escopo desta especificação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="6dadd-254">Também pressupõe-se que o cliente e o servidor tenham uma associação de segurança utilizável com pipes nomeados \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="6dadd-255">1.6 Applicability Statement</span><span class="sxs-lookup"><span data-stu-id="6dadd-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="6dadd-256">O CISP é projetado para consultar e gerenciar catálogos em um servidor remoto a partir de um cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="6dadd-257">O CISP foi preterido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6dadd-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="6dadd-258">1.7 Controle de versão e negociação de capacidade</span><span class="sxs-lookup"><span data-stu-id="6dadd-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="6dadd-259">Esse protocolo não possui controle de versão ou mecanismos de negociação de capacidade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="6dadd-260">1.8 Campos extensíveis para fornecedor</span><span class="sxs-lookup"><span data-stu-id="6dadd-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="6dadd-261">Esse protocolo usa HRESULTs que são extensíveis pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="6dadd-262">Os fornecedores são livres para escolher seus próprios valores para esse campo, desde que o C bit (0x20000000) esteja definido conforme especificado na seção 4.1.1 do \[ MS-sys \] , indicando que ele é um código de cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="6dadd-263">Esse protocolo também usa valores de NTSTATUS obtidos do espaço de número NTSTATUS definido em \[ MS-sys \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="6dadd-264">Os fornecedores devem reutilizar esses valores com o significado indicado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="6dadd-265">Escolher qualquer outro valor executará o risco de uma colisão no futuro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="6dadd-266">*Comportamento do Windows: o Windows usa apenas os valores especificados na seção 4.1.3 do \[ MS-sys \] .*</span><span class="sxs-lookup"><span data-stu-id="6dadd-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="6dadd-267">IDs da propriedade 1.8.1</span><span class="sxs-lookup"><span data-stu-id="6dadd-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="6dadd-268">As propriedades são representadas por IDs conhecidas como IDs de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="6dadd-269">Cada propriedade deve ter um identificador global exclusivo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="6dadd-270">Esse identificador consiste em um **GUID** que representa uma coleção de propriedades chamada um conjunto de propriedades, além de uma cadeia de caracteres ou um inteiro de 32 bits para identificar a propriedade dentro do conjunto.</span><span class="sxs-lookup"><span data-stu-id="6dadd-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="6dadd-271">Se o formulário inteiro da ID for usado, os valores 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE serão considerados inválidos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="6dadd-272">Os fornecedores podem garantir que suas propriedades sejam definidas exclusivamente colocando-as em um conjunto de propriedades definido por seu próprio GUID.</span><span class="sxs-lookup"><span data-stu-id="6dadd-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="6dadd-273">1.9 Atribuições standard</span><span class="sxs-lookup"><span data-stu-id="6dadd-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="6dadd-274">Esse protocolo não tem nenhuma atribuição de padrões, somente atribuições privadas feitas pela Microsoft usando os procedimentos de alocação especificados em outros protocolos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="6dadd-275">A Microsoft alocou esse protocolo como um pipe nomeado, conforme especificado em \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="6dadd-276">A atribuição é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-276">The assignment is:</span></span>



| <span data-ttu-id="6dadd-277">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6dadd-277">Parameter</span></span> | <span data-ttu-id="6dadd-278">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-278">Value</span></span>             | <span data-ttu-id="6dadd-279">Referência</span><span class="sxs-lookup"><span data-stu-id="6dadd-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="6dadd-280">Nome do pipe</span><span class="sxs-lookup"><span data-stu-id="6dadd-280">Pipe name</span></span> | <span data-ttu-id="6dadd-281">\\\\SKADS de CI de pipe \_</span><span class="sxs-lookup"><span data-stu-id="6dadd-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="6dadd-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="6dadd-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="6dadd-283">2 Mensagens</span><span class="sxs-lookup"><span data-stu-id="6dadd-283">2 Messages</span></span>

-   [<span data-ttu-id="6dadd-284">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="6dadd-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="6dadd-285">2.2 Sintaxe da mensagem</span><span class="sxs-lookup"><span data-stu-id="6dadd-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="6dadd-286">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="6dadd-286">2.1 Transport</span></span>

<span data-ttu-id="6dadd-287">Todas as mensagens devem ser transportadas usando um pipe nomeado, conforme especificado em \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="6dadd-288">O seguinte nome de pipe é usado:</span><span class="sxs-lookup"><span data-stu-id="6dadd-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="6dadd-289">\\\\SKADS de CI de pipe \_</span><span class="sxs-lookup"><span data-stu-id="6dadd-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="6dadd-290">Esse protocolo usa o protocolo de pipe nomeado SMB subjacente para recuperar a identidade do chamador que fez a conexão, conforme especificado na seção 2.2.8 do \[ MS-SMB \] ; o cliente deve definir a identificação de segurança \_ como o ImpersonationLevel na solicitação para abrir o pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="6dadd-291">2.2 Sintaxe da mensagem</span><span class="sxs-lookup"><span data-stu-id="6dadd-291">2.2 Message Syntax</span></span>

<span data-ttu-id="6dadd-292">Várias estruturas e mensagens nas seções a seguir referem-se aos identificadores de capítulo ou indicador.</span><span class="sxs-lookup"><span data-stu-id="6dadd-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="6dadd-293">Um identificador é uma estrutura opaca de longa de 32 bits que identifica exclusivamente um capítulo ou indicador.</span><span class="sxs-lookup"><span data-stu-id="6dadd-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="6dadd-294">Normalmente, os aplicativos cliente recebem valores de identificador por meio de chamadas de método; no entanto, há vários valores bem conhecidos que não precisam ser obtidos de um servidor, o significado do que é especificado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="6dadd-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="6dadd-295">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-295">Value</span></span>                         | <span data-ttu-id="6dadd-296">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-297">DB \_ NULL \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="6dadd-298">Um capítulo manipula o conjunto de linhas sem capítulos, que contém todos os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="6dadd-299">DBBMK \_ primeiro 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="6dadd-300">Um identificador de indicador para um indicador que identifica a primeira linha no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="6dadd-301">DBBMK \_ último 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="6dadd-302">Um identificador de indicador para um indicador que identifica a última linha no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="6dadd-303">estruturas 2.2.1</span><span class="sxs-lookup"><span data-stu-id="6dadd-303">2.2.1 Structures</span></span>

<span data-ttu-id="6dadd-304">Esta seção detalha as estruturas de dados que são definidas e usadas pelo CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="6dadd-305">Todos os inteiros de 2, 4 e 8 bytes assinados e não assinados nas seguintes estruturas devem ser transferidos em ordem de byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="6dadd-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="6dadd-306">A tabela a seguir resume as estruturas de dados definidas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="6dadd-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="6dadd-307">Estrutura</span><span class="sxs-lookup"><span data-stu-id="6dadd-307">Structure</span></span>                    | <span data-ttu-id="6dadd-308">Descrição</span><span class="sxs-lookup"><span data-stu-id="6dadd-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="6dadd-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="6dadd-310">Contém o valor no qual executar uma operação de correspondência para uma propriedade especificada em uma estrutura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="6dadd-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="6dadd-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="6dadd-312">Contém uma matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="6dadd-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="6dadd-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="6dadd-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="6dadd-314">Representa os limites de uma dimensão de uma matriz especificada em uma estrutura SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="6dadd-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="6dadd-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="6dadd-315">CFullPropSpec</span></span>                | <span data-ttu-id="6dadd-316">Contém uma especificação de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="6dadd-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-317">CContentRestriction</span></span>          | <span data-ttu-id="6dadd-318">Contém uma cadeia de caracteres para corresponder a um valor de propriedade no cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dadd-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="6dadd-319">CKey</span><span class="sxs-lookup"><span data-stu-id="6dadd-319">CKey</span></span>                         | <span data-ttu-id="6dadd-320">Contém um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="6dadd-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="6dadd-322">Contém um valor de propriedade para corresponder a uma operação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="6dadd-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="6dadd-324">Contém uma correspondência de consulta de idioma natural para uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="6dadd-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-325">CNodeRestriction</span></span>             | <span data-ttu-id="6dadd-326">Contém uma matriz de nós de árvore de comando especificando as restrições para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="6dadd-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-327">COccRestriction</span></span>              | <span data-ttu-id="6dadd-328">Contém o local de uma palavra em uma frase.</span><span class="sxs-lookup"><span data-stu-id="6dadd-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="6dadd-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-329">CPropertyRestriction</span></span>         | <span data-ttu-id="6dadd-330">Contém um valor de propriedade para corresponder a uma operação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="6dadd-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-331">CRangeRestriction</span></span>            | <span data-ttu-id="6dadd-332">Contém uma restrição em um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="6dadd-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="6dadd-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-333">CScopeRestriction</span></span>            | <span data-ttu-id="6dadd-334">Contém uma restrição sobre os arquivos a serem pesquisados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="6dadd-335">CSort</span><span class="sxs-lookup"><span data-stu-id="6dadd-335">CSort</span></span>                        | <span data-ttu-id="6dadd-336">Identifica uma coluna a ser classificada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="6dadd-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-337">CSynRestriction</span></span>              | <span data-ttu-id="6dadd-338">Contém uma palavra ou seus sinônimos para uma frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="6dadd-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-339">CVectorRestriction</span></span>           | <span data-ttu-id="6dadd-340">Contém uma operação ponderada ou em um nó de árvore de comandos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="6dadd-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-341">CWordRestriction</span></span>             | <span data-ttu-id="6dadd-342">Contém uma palavra para uma frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="6dadd-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-343">CRestriction</span></span>                 | <span data-ttu-id="6dadd-344">Contém um nó de uma árvore de comando de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="6dadd-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-345">CColumnSet</span></span>                   | <span data-ttu-id="6dadd-346">Indica o número de colunas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="6dadd-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-347">CCategorizationSet</span></span>           | <span data-ttu-id="6dadd-348">Contém informações sobre o agrupamento de um conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="6dadd-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="6dadd-349">CCategorizationSpec</span></span>          | <span data-ttu-id="6dadd-350">Contém uma definição de categorias nas quais os resultados da consulta serão categorizados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="6dadd-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="6dadd-351">CDbColId</span></span>                     | <span data-ttu-id="6dadd-352">Contém uma coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="6dadd-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="6dadd-353">CDbProp</span></span>                      | <span data-ttu-id="6dadd-354">Contém uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="6dadd-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-355">CDbPropSet</span></span>                   | <span data-ttu-id="6dadd-356">Contém um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dadd-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="6dadd-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="6dadd-357">CPidMapper</span></span>                   | <span data-ttu-id="6dadd-358">Contém uma matriz de IDs de propriedade especificando as propriedades a serem retornadas em um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="6dadd-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="6dadd-359">CRowSeekAt</span></span>                   | <span data-ttu-id="6dadd-360">Contém o deslocamento no qual recuperar linhas em uma mensagem CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="6dadd-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="6dadd-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="6dadd-362">Identifica o ponto no qual iniciar a recuperação para uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="6dadd-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="6dadd-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="6dadd-364">Identifica os indicadores dos quais recuperar linhas para uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="6dadd-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="6dadd-365">CRowSeekNext</span></span>                 | <span data-ttu-id="6dadd-366">Contém o número de linhas a serem ignoradas em uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="6dadd-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="6dadd-367">CRowsetProperties</span></span>            | <span data-ttu-id="6dadd-368">Contém as informações de configuração de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="6dadd-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-369">CSortSet</span></span>                     | <span data-ttu-id="6dadd-370">Contém a ordem de classificação para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="6dadd-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="6dadd-371">CTableColumn</span></span>                 | <span data-ttu-id="6dadd-372">Contém uma coluna para a mensagem CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="6dadd-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="6dadd-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="6dadd-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="6dadd-374">Contém um valor serializado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="6dadd-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="6dadd-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="6dadd-376">A estrutura CBaseStorageVariant contém o valor no qual executar uma operação de correspondência para uma propriedade especificada na estrutura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="6dadd-377">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-377">0</span></span>

<span data-ttu-id="6dadd-378">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-378">1</span></span>

<span data-ttu-id="6dadd-379">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-379">2</span></span>

<span data-ttu-id="6dadd-380">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-380">3</span></span>

<span data-ttu-id="6dadd-381">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-381">4</span></span>

<span data-ttu-id="6dadd-382">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-382">5</span></span>

<span data-ttu-id="6dadd-383">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-383">6</span></span>

<span data-ttu-id="6dadd-384">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-384">7</span></span>

<span data-ttu-id="6dadd-385">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-385">8</span></span>

<span data-ttu-id="6dadd-386">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-386">9</span></span>

<span data-ttu-id="6dadd-387">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-387">1</span></span><br/> <span data-ttu-id="6dadd-388">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-388">0</span></span><br/>

<span data-ttu-id="6dadd-389">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-389">1</span></span>

<span data-ttu-id="6dadd-390">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-390">2</span></span>

<span data-ttu-id="6dadd-391">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-391">3</span></span>

<span data-ttu-id="6dadd-392">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-392">4</span></span>

<span data-ttu-id="6dadd-393">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-393">5</span></span>

<span data-ttu-id="6dadd-394">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-394">6</span></span>

<span data-ttu-id="6dadd-395">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-395">7</span></span>

<span data-ttu-id="6dadd-396">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-396">8</span></span>

<span data-ttu-id="6dadd-397">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-397">9</span></span>

<span data-ttu-id="6dadd-398">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-398">2</span></span><br/> <span data-ttu-id="6dadd-399">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-399">0</span></span><br/>

<span data-ttu-id="6dadd-400">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-400">1</span></span>

<span data-ttu-id="6dadd-401">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-401">2</span></span>

<span data-ttu-id="6dadd-402">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-402">3</span></span>

<span data-ttu-id="6dadd-403">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-403">4</span></span>

<span data-ttu-id="6dadd-404">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-404">5</span></span>

<span data-ttu-id="6dadd-405">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-405">6</span></span>

<span data-ttu-id="6dadd-406">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-406">7</span></span>

<span data-ttu-id="6dadd-407">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-407">8</span></span>

<span data-ttu-id="6dadd-408">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-408">9</span></span>

<span data-ttu-id="6dadd-409">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-409">3</span></span><br/> <span data-ttu-id="6dadd-410">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-410">0</span></span><br/>

<span data-ttu-id="6dadd-411">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-411">1</span></span>

<span data-ttu-id="6dadd-412">vType</span><span class="sxs-lookup"><span data-stu-id="6dadd-412">vType</span></span>

<span data-ttu-id="6dadd-413">vData1</span><span class="sxs-lookup"><span data-stu-id="6dadd-413">vData1</span></span>

<span data-ttu-id="6dadd-414">vData2</span><span class="sxs-lookup"><span data-stu-id="6dadd-414">vData2</span></span>

<span data-ttu-id="6dadd-415">vValue (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-415">vValue (variable)</span></span>



 

<span data-ttu-id="6dadd-416">**vType:** um indicador de tipo que indica o tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="6dadd-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="6dadd-417">Ele DEVE ser um dos valores VARENUM especificados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dadd-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="6dadd-418">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-418">Value</span></span>                 | <span data-ttu-id="6dadd-419">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-420">VT \_ EMPTY (0x0000)</span><span class="sxs-lookup"><span data-stu-id="6dadd-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="6dadd-421">vValue não está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="6dadd-422">VT \_ NULL (0x0001)</span><span class="sxs-lookup"><span data-stu-id="6dadd-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="6dadd-423">vValue não está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="6dadd-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="6dadd-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="6dadd-425">Um inteiro de um byte com sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="6dadd-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="6dadd-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="6dadd-427">Um inteiro de um byte sem sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="6dadd-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="6dadd-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="6dadd-429">Um inteiro de dois bytes com sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="6dadd-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="6dadd-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="6dadd-431">Um inteiro de dois bytes sem sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="6dadd-432">VT \_ BOOL (0x000B)</span><span class="sxs-lookup"><span data-stu-id="6dadd-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="6dadd-433">Um valor booliana; um inteiro de 2 byte que contém 0x0000 (FALSE) ou 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="6dadd-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="6dadd-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="6dadd-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="6dadd-435">Um inteiro de quatro bytes com sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="6dadd-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="6dadd-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="6dadd-437">Um inteiro de quatro bytes sem sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="6dadd-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="6dadd-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="6dadd-439">Um número de ponto flutuante IEEE de 32 bits, conforme definido em \[ IEEE754. \]</span><span class="sxs-lookup"><span data-stu-id="6dadd-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="6dadd-440">VT \_ INT (0x0016)</span><span class="sxs-lookup"><span data-stu-id="6dadd-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="6dadd-441">Um inteiro de quatro bytes com sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="6dadd-442">VT \_ UINT (0x0017)</span><span class="sxs-lookup"><span data-stu-id="6dadd-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="6dadd-443">Um inteiro de quatro bytes sem sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="6dadd-444">ERRO de VT \_ (0x000A)</span><span class="sxs-lookup"><span data-stu-id="6dadd-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="6dadd-445">Um inteiro sem sinal de 4 byte que contém um HRESULT, conforme especificado em \[ MS-SYS \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="6dadd-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="6dadd-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="6dadd-447">Um inteiro com sinal de 8 byte.</span><span class="sxs-lookup"><span data-stu-id="6dadd-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="6dadd-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="6dadd-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="6dadd-449">Um inteiro de oito bytes sem sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="6dadd-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="6dadd-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="6dadd-451">Um número de ponto flutuante IEEE de 64 bits conforme definido em \[ IEEE754. \]</span><span class="sxs-lookup"><span data-stu-id="6dadd-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="6dadd-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="6dadd-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="6dadd-453">Um inteiro de complemento de dois de 8 byte (dimensionado em 10.000).</span><span class="sxs-lookup"><span data-stu-id="6dadd-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="6dadd-454">DATA DA VT \_ (0x0007)</span><span class="sxs-lookup"><span data-stu-id="6dadd-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="6dadd-455">Um número de ponto flutuante de 64 bits que representa o número de dias desde 00:00:00 em 31 de dezembro de 1899 (Tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="6dadd-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="6dadd-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="6dadd-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="6dadd-457">Um inteiro de 64 bits que representa o número de intervalos de 100 nanossegundos desde 00:00:00 em 1º de janeiro de 1601 (Tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="6dadd-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="6dadd-458">DECIMAL da VT \_ (0x000E)</span><span class="sxs-lookup"><span data-stu-id="6dadd-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="6dadd-459">Uma estrutura DECIMAL, conforme especificado na seção 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="6dadd-460">CLSID da VT \_ (0x0048)</span><span class="sxs-lookup"><span data-stu-id="6dadd-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="6dadd-461">Um valor binário de 16 byte que contém um GUID.</span><span class="sxs-lookup"><span data-stu-id="6dadd-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="6dadd-462">BLOB de VT \_ (0x0041)</span><span class="sxs-lookup"><span data-stu-id="6dadd-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="6dadd-463">Uma contagem de inteiros sem sinal de 4 bytes no blob, seguida por muitos bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="6dadd-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="6dadd-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="6dadd-465">Uma contagem de inteiros sem sinal de 4 bytes na cadeia de caracteres, seguida por uma cadeia de caracteres, conforme especificado abaixo em vValue.</span><span class="sxs-lookup"><span data-stu-id="6dadd-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="6dadd-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="6dadd-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="6dadd-467">Uma cadeia de caracteres ANSI terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="6dadd-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="6dadd-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="6dadd-469">Uma cadeia de caracteres UNICODE Unicode terminada \[ em \] nulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="6dadd-470">VT \_ VARIANT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="6dadd-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="6dadd-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="6dadd-471">CBaseStorageVariant.</span></span> <span data-ttu-id="6dadd-472">DEVE ser combinado com um modificador de tipo de VT \_ ARRAY ou VT \_ VECTOR.</span><span class="sxs-lookup"><span data-stu-id="6dadd-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="6dadd-473">A tabela a seguir especifica os modificadores de tipo para vType.</span><span class="sxs-lookup"><span data-stu-id="6dadd-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="6dadd-474">Os modificadores de tipo podem ser binários ORed com vType, para alterar o significado de vValue para indicar que ele é um dos dois tipos de matriz possíveis.</span><span class="sxs-lookup"><span data-stu-id="6dadd-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="6dadd-475">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-475">Value</span></span>               | <span data-ttu-id="6dadd-476">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-477">VT \_ VECTOR (0x1000)</span><span class="sxs-lookup"><span data-stu-id="6dadd-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="6dadd-478">Se o indicador de tipo for combinado com vT VECTOR usando um operador OR, vValue será uma matriz contada de valores \_ do tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="6dadd-479">Consulte a seção 2.2.1.1.1.2 para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="6dadd-480">Esse modificador de tipo NÃO DEVE ser combinado com os seguintes tipos: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, \_ VT BLOB, OBJETO \_ BLOB \_ VT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="6dadd-481">MATRIZ VT \_ (0x2000)</span><span class="sxs-lookup"><span data-stu-id="6dadd-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="6dadd-482">Se o indicador de tipo for combinado com VT ARRAY por um operador OR, o valor será um SAFEARRAY (conforme especificado na seção \_ 2.2.1.1.1.3) que contém valores do tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="6dadd-483">Esse modificador de tipo NÃO DEVE ser combinado com os seguintes tipos: VT \_ I8, VT \_ UI8, VT \_ FILETIME, \_ CLSID VT, \_ BLOB VT, OBJETO \_ DE BLOB \_ VT, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="6dadd-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="6dadd-484">**vData1:** quando vType é VT DECIMAL, o valor desse campo é especificado como o campo Escala na \_ seção 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="6dadd-485">Para todos os outros vTypes, o valor DEVE ser definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="6dadd-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="6dadd-486">**vData2:** quando vType é VT DECIMAL, o valor desse campo é especificado como o campo Entrar na \_ seção 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="6dadd-487">Para todos os outros vTypes, o valor DEVE ser definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="6dadd-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="6dadd-488">**vValue:** o valor da operação de match.</span><span class="sxs-lookup"><span data-stu-id="6dadd-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="6dadd-489">A sintaxe DEVE ser conforme indicado no campo vType.</span><span class="sxs-lookup"><span data-stu-id="6dadd-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="6dadd-490">A tabela a seguir resume os tamanhos do campo vValue, dependendo do campo vType para tipos de dados de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="6dadd-491">O tamanho é em bytes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-491">The size is in bytes.</span></span>



| <span data-ttu-id="6dadd-492">vType</span><span class="sxs-lookup"><span data-stu-id="6dadd-492">vType</span></span>                                                   | <span data-ttu-id="6dadd-493">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6dadd-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="6dadd-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="6dadd-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="6dadd-495">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-495">1</span></span>    |
| <span data-ttu-id="6dadd-496">VT \_ I2, VT \_ UI2, VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="6dadd-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="6dadd-497">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-497">2</span></span>    |
| <span data-ttu-id="6dadd-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, ERRO de VT \_</span><span class="sxs-lookup"><span data-stu-id="6dadd-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="6dadd-499">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-499">4</span></span>    |
| <span data-ttu-id="6dadd-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="6dadd-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="6dadd-501">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-501">8</span></span>    |
| <span data-ttu-id="6dadd-502">VT \_ DECIMAL, \_ CLSID da VT</span><span class="sxs-lookup"><span data-stu-id="6dadd-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="6dadd-503">16</span><span class="sxs-lookup"><span data-stu-id="6dadd-503">16</span></span>   |



 

<span data-ttu-id="6dadd-504">Se vType for definido como \_ VT BLOB, VT BSTR ou VT LPSTR, a estrutura de vValue será \_ especificada no diagrama a \_ seguir:</span><span class="sxs-lookup"><span data-stu-id="6dadd-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="6dadd-505">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-505">0</span></span>

<span data-ttu-id="6dadd-506">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-506">1</span></span>

<span data-ttu-id="6dadd-507">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-507">2</span></span>

<span data-ttu-id="6dadd-508">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-508">3</span></span>

<span data-ttu-id="6dadd-509">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-509">4</span></span>

<span data-ttu-id="6dadd-510">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-510">5</span></span>

<span data-ttu-id="6dadd-511">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-511">6</span></span>

<span data-ttu-id="6dadd-512">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-512">7</span></span>

<span data-ttu-id="6dadd-513">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-513">8</span></span>

<span data-ttu-id="6dadd-514">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-514">9</span></span>

<span data-ttu-id="6dadd-515">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-515">1</span></span><br/> <span data-ttu-id="6dadd-516">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-516">0</span></span><br/>

<span data-ttu-id="6dadd-517">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-517">1</span></span>

<span data-ttu-id="6dadd-518">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-518">2</span></span>

<span data-ttu-id="6dadd-519">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-519">3</span></span>

<span data-ttu-id="6dadd-520">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-520">4</span></span>

<span data-ttu-id="6dadd-521">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-521">5</span></span>

<span data-ttu-id="6dadd-522">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-522">6</span></span>

<span data-ttu-id="6dadd-523">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-523">7</span></span>

<span data-ttu-id="6dadd-524">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-524">8</span></span>

<span data-ttu-id="6dadd-525">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-525">9</span></span>

<span data-ttu-id="6dadd-526">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-526">2</span></span><br/> <span data-ttu-id="6dadd-527">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-527">0</span></span><br/>

<span data-ttu-id="6dadd-528">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-528">1</span></span>

<span data-ttu-id="6dadd-529">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-529">2</span></span>

<span data-ttu-id="6dadd-530">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-530">3</span></span>

<span data-ttu-id="6dadd-531">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-531">4</span></span>

<span data-ttu-id="6dadd-532">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-532">5</span></span>

<span data-ttu-id="6dadd-533">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-533">6</span></span>

<span data-ttu-id="6dadd-534">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-534">7</span></span>

<span data-ttu-id="6dadd-535">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-535">8</span></span>

<span data-ttu-id="6dadd-536">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-536">9</span></span>

<span data-ttu-id="6dadd-537">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-537">3</span></span><br/> <span data-ttu-id="6dadd-538">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-538">0</span></span><br/>

<span data-ttu-id="6dadd-539">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-539">1</span></span>

<span data-ttu-id="6dadd-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="6dadd-540">cbSize</span></span>

<span data-ttu-id="6dadd-541">blobData (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="6dadd-542">**cbSize:** inteiro de 32 bits sem sinal, indicando o tamanho do campo blobData em bytes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="6dadd-543">Se vType for definido como VT BSTR ou \_ VT LPSTR, cbSize DEVERÁ ser definido como 0x00000000 quando a cadeia de caracteres representada for uma cadeia de caracteres \_ vazia.</span><span class="sxs-lookup"><span data-stu-id="6dadd-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="6dadd-544">**blobData:** DEVE ser de comprimento cbSize em bytes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="6dadd-545">Para vType definido como BLOB de \_ VT, esse campo são dados de blob binário opacos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="6dadd-546">Para vType definido como VT BSTR, esse campo é um conjunto de caracteres em um \_ conjunto de caracteres selecionado por OEM.</span><span class="sxs-lookup"><span data-stu-id="6dadd-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="6dadd-547">O cliente e o servidor DEVEM ser configurados para ter conjuntos de caracteres interoperáveis (fora da banda do protocolo).</span><span class="sxs-lookup"><span data-stu-id="6dadd-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="6dadd-548">Não há nenhum requisito de que ela seja terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="6dadd-549">Para vType definido como VT LPSTR, esse campo é uma cadeia de caracteres terminada em nulo em um conjunto de caracteres selecionado \_ OEM.</span><span class="sxs-lookup"><span data-stu-id="6dadd-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="6dadd-550">O cliente e o servidor DEVEM ser configurados para ter conjuntos de caracteres interoperáveis (fora da banda do protocolo).</span><span class="sxs-lookup"><span data-stu-id="6dadd-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="6dadd-551">Se vType for definido como VT \_ LPWSTR, a estrutura de vValue será especificada no diagrama a seguir:</span><span class="sxs-lookup"><span data-stu-id="6dadd-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="6dadd-552">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-552">0</span></span>

<span data-ttu-id="6dadd-553">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-553">1</span></span>

<span data-ttu-id="6dadd-554">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-554">2</span></span>

<span data-ttu-id="6dadd-555">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-555">3</span></span>

<span data-ttu-id="6dadd-556">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-556">4</span></span>

<span data-ttu-id="6dadd-557">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-557">5</span></span>

<span data-ttu-id="6dadd-558">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-558">6</span></span>

<span data-ttu-id="6dadd-559">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-559">7</span></span>

<span data-ttu-id="6dadd-560">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-560">8</span></span>

<span data-ttu-id="6dadd-561">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-561">9</span></span>

<span data-ttu-id="6dadd-562">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-562">1</span></span><br/> <span data-ttu-id="6dadd-563">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-563">0</span></span><br/>

<span data-ttu-id="6dadd-564">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-564">1</span></span>

<span data-ttu-id="6dadd-565">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-565">2</span></span>

<span data-ttu-id="6dadd-566">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-566">3</span></span>

<span data-ttu-id="6dadd-567">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-567">4</span></span>

<span data-ttu-id="6dadd-568">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-568">5</span></span>

<span data-ttu-id="6dadd-569">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-569">6</span></span>

<span data-ttu-id="6dadd-570">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-570">7</span></span>

<span data-ttu-id="6dadd-571">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-571">8</span></span>

<span data-ttu-id="6dadd-572">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-572">9</span></span>

<span data-ttu-id="6dadd-573">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-573">2</span></span><br/> <span data-ttu-id="6dadd-574">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-574">0</span></span><br/>

<span data-ttu-id="6dadd-575">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-575">1</span></span>

<span data-ttu-id="6dadd-576">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-576">2</span></span>

<span data-ttu-id="6dadd-577">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-577">3</span></span>

<span data-ttu-id="6dadd-578">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-578">4</span></span>

<span data-ttu-id="6dadd-579">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-579">5</span></span>

<span data-ttu-id="6dadd-580">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-580">6</span></span>

<span data-ttu-id="6dadd-581">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-581">7</span></span>

<span data-ttu-id="6dadd-582">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-582">8</span></span>

<span data-ttu-id="6dadd-583">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-583">9</span></span>

<span data-ttu-id="6dadd-584">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-584">3</span></span><br/> <span data-ttu-id="6dadd-585">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-585">0</span></span><br/>

<span data-ttu-id="6dadd-586">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-586">1</span></span>

<span data-ttu-id="6dadd-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="6dadd-587">ccLen</span></span>

<span data-ttu-id="6dadd-588">cadeia de caracteres (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-588">string (variable, optional)</span></span>



 

<span data-ttu-id="6dadd-589">**ccLen:** inteiro de 32 bits sem sinal, indicando o tamanho do campo de cadeia de caracteres em caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="6dadd-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="6dadd-590">DEVE ser definido como 0x00000000 para uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="6dadd-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="6dadd-591">**cadeia** de caracteres : cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="6dadd-592">2.2.1.1.1 Estruturas CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="6dadd-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="6dadd-593">As estruturas a seguir são usadas na estrutura CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="6dadd-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="6dadd-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="6dadd-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="6dadd-595">DECIMAL é usado para representar um valor numérico exato com uma precisão fixa e uma escala fixa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="6dadd-596">Quando vType é definido como VT DECIMAL (0x0000E), os campos \_ vData1 e vData2 de CBaseStorageVariant DEVEM ser interpretados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6dadd-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="6dadd-597">**vData1:** o número de dígitos à direita do ponto decimal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="6dadd-598">DEVE estar no intervalo de 0 a 28.</span><span class="sxs-lookup"><span data-stu-id="6dadd-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="6dadd-599">**vData2:** o sinal do valor numérico.</span><span class="sxs-lookup"><span data-stu-id="6dadd-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="6dadd-600">Definido como 0x00 se for positivo, 0x80 se for negativo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="6dadd-601">O formato do campo vValue é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-601">The format of the vValue field is:</span></span>



<span data-ttu-id="6dadd-602">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-602">0</span></span>

<span data-ttu-id="6dadd-603">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-603">1</span></span>

<span data-ttu-id="6dadd-604">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-604">2</span></span>

<span data-ttu-id="6dadd-605">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-605">3</span></span>

<span data-ttu-id="6dadd-606">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-606">4</span></span>

<span data-ttu-id="6dadd-607">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-607">5</span></span>

<span data-ttu-id="6dadd-608">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-608">6</span></span>

<span data-ttu-id="6dadd-609">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-609">7</span></span>

<span data-ttu-id="6dadd-610">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-610">8</span></span>

<span data-ttu-id="6dadd-611">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-611">9</span></span>

<span data-ttu-id="6dadd-612">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-612">1</span></span><br/> <span data-ttu-id="6dadd-613">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-613">0</span></span><br/>

<span data-ttu-id="6dadd-614">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-614">1</span></span>

<span data-ttu-id="6dadd-615">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-615">2</span></span>

<span data-ttu-id="6dadd-616">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-616">3</span></span>

<span data-ttu-id="6dadd-617">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-617">4</span></span>

<span data-ttu-id="6dadd-618">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-618">5</span></span>

<span data-ttu-id="6dadd-619">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-619">6</span></span>

<span data-ttu-id="6dadd-620">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-620">7</span></span>

<span data-ttu-id="6dadd-621">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-621">8</span></span>

<span data-ttu-id="6dadd-622">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-622">9</span></span>

<span data-ttu-id="6dadd-623">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-623">2</span></span><br/> <span data-ttu-id="6dadd-624">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-624">0</span></span><br/>

<span data-ttu-id="6dadd-625">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-625">1</span></span>

<span data-ttu-id="6dadd-626">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-626">2</span></span>

<span data-ttu-id="6dadd-627">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-627">3</span></span>

<span data-ttu-id="6dadd-628">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-628">4</span></span>

<span data-ttu-id="6dadd-629">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-629">5</span></span>

<span data-ttu-id="6dadd-630">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-630">6</span></span>

<span data-ttu-id="6dadd-631">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-631">7</span></span>

<span data-ttu-id="6dadd-632">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-632">8</span></span>

<span data-ttu-id="6dadd-633">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-633">9</span></span>

<span data-ttu-id="6dadd-634">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-634">3</span></span><br/> <span data-ttu-id="6dadd-635">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-635">0</span></span><br/>

<span data-ttu-id="6dadd-636">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-636">1</span></span>

<span data-ttu-id="6dadd-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="6dadd-637">Hi32</span></span>

<span data-ttu-id="6dadd-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="6dadd-638">Lo32</span></span>

<span data-ttu-id="6dadd-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="6dadd-639">Mid32</span></span>



 

<span data-ttu-id="6dadd-640">**Hi32**: os mais de 32 bits do número inteiro de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="6dadd-641">**Lo32**: os mais baixos 32 bits do número inteiro de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="6dadd-642">**Mid32**: os bits do meio 32 do número inteiro de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="6dadd-643">vetor VT 2.2.1.1.1.2 \_</span><span class="sxs-lookup"><span data-stu-id="6dadd-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="6dadd-644">O \_ vetor VT é usado para passar matrizes unidimensionais.</span><span class="sxs-lookup"><span data-stu-id="6dadd-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="6dadd-645">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-645">0</span></span>

<span data-ttu-id="6dadd-646">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-646">1</span></span>

<span data-ttu-id="6dadd-647">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-647">2</span></span>

<span data-ttu-id="6dadd-648">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-648">3</span></span>

<span data-ttu-id="6dadd-649">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-649">4</span></span>

<span data-ttu-id="6dadd-650">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-650">5</span></span>

<span data-ttu-id="6dadd-651">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-651">6</span></span>

<span data-ttu-id="6dadd-652">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-652">7</span></span>

<span data-ttu-id="6dadd-653">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-653">8</span></span>

<span data-ttu-id="6dadd-654">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-654">9</span></span>

<span data-ttu-id="6dadd-655">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-655">1</span></span><br/> <span data-ttu-id="6dadd-656">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-656">0</span></span><br/>

<span data-ttu-id="6dadd-657">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-657">1</span></span>

<span data-ttu-id="6dadd-658">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-658">2</span></span>

<span data-ttu-id="6dadd-659">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-659">3</span></span>

<span data-ttu-id="6dadd-660">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-660">4</span></span>

<span data-ttu-id="6dadd-661">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-661">5</span></span>

<span data-ttu-id="6dadd-662">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-662">6</span></span>

<span data-ttu-id="6dadd-663">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-663">7</span></span>

<span data-ttu-id="6dadd-664">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-664">8</span></span>

<span data-ttu-id="6dadd-665">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-665">9</span></span>

<span data-ttu-id="6dadd-666">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-666">2</span></span><br/> <span data-ttu-id="6dadd-667">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-667">0</span></span><br/>

<span data-ttu-id="6dadd-668">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-668">1</span></span>

<span data-ttu-id="6dadd-669">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-669">2</span></span>

<span data-ttu-id="6dadd-670">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-670">3</span></span>

<span data-ttu-id="6dadd-671">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-671">4</span></span>

<span data-ttu-id="6dadd-672">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-672">5</span></span>

<span data-ttu-id="6dadd-673">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-673">6</span></span>

<span data-ttu-id="6dadd-674">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-674">7</span></span>

<span data-ttu-id="6dadd-675">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-675">8</span></span>

<span data-ttu-id="6dadd-676">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-676">9</span></span>

<span data-ttu-id="6dadd-677">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-677">3</span></span><br/> <span data-ttu-id="6dadd-678">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-678">0</span></span><br/>

<span data-ttu-id="6dadd-679">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-679">1</span></span>

<span data-ttu-id="6dadd-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="6dadd-680">vVectorElements</span></span>

<span data-ttu-id="6dadd-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="6dadd-681">vVectorData</span></span>



 

<span data-ttu-id="6dadd-682">**vVectorElements**: inteiro de 32 bits sem sinal, indicando o número de elementos no campo vVectorData.</span><span class="sxs-lookup"><span data-stu-id="6dadd-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="6dadd-683">**vVectorData**: uma matriz de itens que têm um tipo indicado por vType com o bit 0x1000 limpo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="6dadd-684">O tamanho de um item de comprimento fixo individual pode ser obtido da tabela de tipos de dados de comprimento fixo, conforme especificado na seção 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="6dadd-685">O comprimento desse campo, em bytes, pode ser calculado multiplicando vVectorElements pelo tamanho de um item individual.</span><span class="sxs-lookup"><span data-stu-id="6dadd-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="6dadd-686">Para tipos de dados de comprimento variável, vVectorData contém uma sequência de tipos simples com marshaling consecutivo em que o tipo é indicado por vType com o bit 0x1000 limpo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="6dadd-687">Isso inclui um caso especial indicado pela variante da \_ matriz \| VT vType VT \_ (ou seja, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="6dadd-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="6dadd-688">Os elementos no campo vVectorData devem ser separados por 0 a 3 bytes de preenchimento, de modo que cada elemento comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa matriz.</span><span class="sxs-lookup"><span data-stu-id="6dadd-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="6dadd-689">Se os bytes de preenchimento estiverem presentes, o valor que eles contêm será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="6dadd-690">O conteúdo dos bytes de preenchimento deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-691">Para um vType definido como \_ variante de matriz VT de VT \| \_ , o tipo de itens nesta sequência é CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="6dadd-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="6dadd-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="6dadd-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="6dadd-693">SAFEARRAY é usado para passar matrizes multidimensionais.</span><span class="sxs-lookup"><span data-stu-id="6dadd-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="6dadd-694">A estrutura contém informações de tamanho de matriz, bem como os dados na matriz.</span><span class="sxs-lookup"><span data-stu-id="6dadd-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="6dadd-695">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-695">0</span></span>

<span data-ttu-id="6dadd-696">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-696">1</span></span>

<span data-ttu-id="6dadd-697">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-697">2</span></span>

<span data-ttu-id="6dadd-698">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-698">3</span></span>

<span data-ttu-id="6dadd-699">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-699">4</span></span>

<span data-ttu-id="6dadd-700">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-700">5</span></span>

<span data-ttu-id="6dadd-701">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-701">6</span></span>

<span data-ttu-id="6dadd-702">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-702">7</span></span>

<span data-ttu-id="6dadd-703">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-703">8</span></span>

<span data-ttu-id="6dadd-704">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-704">9</span></span>

<span data-ttu-id="6dadd-705">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-705">1</span></span><br/> <span data-ttu-id="6dadd-706">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-706">0</span></span><br/>

<span data-ttu-id="6dadd-707">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-707">1</span></span>

<span data-ttu-id="6dadd-708">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-708">2</span></span>

<span data-ttu-id="6dadd-709">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-709">3</span></span>

<span data-ttu-id="6dadd-710">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-710">4</span></span>

<span data-ttu-id="6dadd-711">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-711">5</span></span>

<span data-ttu-id="6dadd-712">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-712">6</span></span>

<span data-ttu-id="6dadd-713">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-713">7</span></span>

<span data-ttu-id="6dadd-714">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-714">8</span></span>

<span data-ttu-id="6dadd-715">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-715">9</span></span>

<span data-ttu-id="6dadd-716">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-716">2</span></span><br/> <span data-ttu-id="6dadd-717">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-717">0</span></span><br/>

<span data-ttu-id="6dadd-718">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-718">1</span></span>

<span data-ttu-id="6dadd-719">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-719">2</span></span>

<span data-ttu-id="6dadd-720">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-720">3</span></span>

<span data-ttu-id="6dadd-721">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-721">4</span></span>

<span data-ttu-id="6dadd-722">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-722">5</span></span>

<span data-ttu-id="6dadd-723">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-723">6</span></span>

<span data-ttu-id="6dadd-724">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-724">7</span></span>

<span data-ttu-id="6dadd-725">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-725">8</span></span>

<span data-ttu-id="6dadd-726">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-726">9</span></span>

<span data-ttu-id="6dadd-727">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-727">3</span></span><br/> <span data-ttu-id="6dadd-728">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-728">0</span></span><br/>

<span data-ttu-id="6dadd-729">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-729">1</span></span>

<span data-ttu-id="6dadd-730">cDims</span><span class="sxs-lookup"><span data-stu-id="6dadd-730">cDims</span></span>

<span data-ttu-id="6dadd-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="6dadd-731">fFeatures</span></span>

<span data-ttu-id="6dadd-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="6dadd-732">cbElements</span></span>

<span data-ttu-id="6dadd-733">Rgsabound (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-733">Rgsabound (variable)</span></span>

<span data-ttu-id="6dadd-734">vData (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-734">vData (variable)</span></span>



 

<span data-ttu-id="6dadd-735">**cDims**: inteiro de 16 bits não assinado, indicando o número de dimensões da matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="6dadd-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="6dadd-736">**fFeatures**: um tele-bit de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="6dadd-737">Os valores representam recursos, definidos por aplicativos de camada superior e devem ser ignorados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="6dadd-738">**cbElements**: um inteiro de 32 bits sem sinal especificando o tamanho de cada elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="6dadd-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="6dadd-739">**Rgsabound**: uma matriz que contém uma estrutura SAFEARRAYBOUND, conforme especificado na seção 2.2.1.1.1.4, por dimensão em SafeArray.</span><span class="sxs-lookup"><span data-stu-id="6dadd-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="6dadd-740">Essa matriz tem a dimensão mais à esquerda primeiro e a dimensão mais à direita por último.</span><span class="sxs-lookup"><span data-stu-id="6dadd-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="6dadd-741">**vData**: um vetor de itens empacotados de um tipo específico, indicado pelo VType do CBaseStorageVariant que o contém, com o bit 0x2000 limpo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="6dadd-742">o vData é empacotado de forma semelhante ao \_ vetor VT, conforme especificado na seção 2.2.1.1.1.2, com a diferença de que o número de itens não é armazenado na frente do vetor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="6dadd-743">Em vez disso, o número de itens é calculado multiplicando-se o valor cElements por todos os limites de matrizes seguros fornecidos no campo rgsabound.</span><span class="sxs-lookup"><span data-stu-id="6dadd-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="6dadd-744">Os elementos são armazenados em um vetor em ordem de dimensões, iterando começando com a dimensão mais à direita.</span><span class="sxs-lookup"><span data-stu-id="6dadd-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="6dadd-745">O diagrama a seguir representa visualmente uma matriz bidimensional de exemplo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="6dadd-746">A primeira dimensão tem cElements igual a 4 (representada horizontalmente) e lLbound igual a 0, e a segunda dimensão tem cElements igual a 2 (representada verticalmente) e lLbound igual a 0.</span><span class="sxs-lookup"><span data-stu-id="6dadd-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="6dadd-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-747">0x00000001</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="6dadd-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-748">0x00000002</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="6dadd-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-749">0x00000003</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="6dadd-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6dadd-750">0x00000005</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="6dadd-751">:: Row:::</span><span class="sxs-lookup"><span data-stu-id="6dadd-751">::row:::</span></span>
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

<span data-ttu-id="6dadd-752">Usando o diagrama acima, vData conterá a seguinte sequência: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (Iterando primeiro pela dimensão mais à direita e, em seguida, incrementando a próxima dimensão).</span><span class="sxs-lookup"><span data-stu-id="6dadd-752">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="6dadd-753">O rgsabound anterior (que registra cElements e LBound) seria: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-753">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="6dadd-754">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="6dadd-754">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="6dadd-755">A estrutura SAFEARRAYBOUND representa os limites de uma dimensão de um SAFEARRAY ou SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="6dadd-755">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="6dadd-756">Seu formato é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-756">Its format is:</span></span>



<span data-ttu-id="6dadd-757">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-757">0</span></span>

<span data-ttu-id="6dadd-758">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-758">1</span></span>

<span data-ttu-id="6dadd-759">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-759">2</span></span>

<span data-ttu-id="6dadd-760">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-760">3</span></span>

<span data-ttu-id="6dadd-761">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-761">4</span></span>

<span data-ttu-id="6dadd-762">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-762">5</span></span>

<span data-ttu-id="6dadd-763">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-763">6</span></span>

<span data-ttu-id="6dadd-764">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-764">7</span></span>

<span data-ttu-id="6dadd-765">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-765">8</span></span>

<span data-ttu-id="6dadd-766">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-766">9</span></span>

<span data-ttu-id="6dadd-767">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-767">1</span></span><br/> <span data-ttu-id="6dadd-768">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-768">0</span></span><br/>

<span data-ttu-id="6dadd-769">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-769">1</span></span>

<span data-ttu-id="6dadd-770">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-770">2</span></span>

<span data-ttu-id="6dadd-771">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-771">3</span></span>

<span data-ttu-id="6dadd-772">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-772">4</span></span>

<span data-ttu-id="6dadd-773">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-773">5</span></span>

<span data-ttu-id="6dadd-774">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-774">6</span></span>

<span data-ttu-id="6dadd-775">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-775">7</span></span>

<span data-ttu-id="6dadd-776">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-776">8</span></span>

<span data-ttu-id="6dadd-777">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-777">9</span></span>

<span data-ttu-id="6dadd-778">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-778">2</span></span><br/> <span data-ttu-id="6dadd-779">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-779">0</span></span><br/>

<span data-ttu-id="6dadd-780">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-780">1</span></span>

<span data-ttu-id="6dadd-781">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-781">2</span></span>

<span data-ttu-id="6dadd-782">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-782">3</span></span>

<span data-ttu-id="6dadd-783">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-783">4</span></span>

<span data-ttu-id="6dadd-784">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-784">5</span></span>

<span data-ttu-id="6dadd-785">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-785">6</span></span>

<span data-ttu-id="6dadd-786">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-786">7</span></span>

<span data-ttu-id="6dadd-787">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-787">8</span></span>

<span data-ttu-id="6dadd-788">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-788">9</span></span>

<span data-ttu-id="6dadd-789">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-789">3</span></span><br/> <span data-ttu-id="6dadd-790">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-790">0</span></span><br/>

<span data-ttu-id="6dadd-791">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-791">1</span></span>

<span data-ttu-id="6dadd-792">cElements</span><span class="sxs-lookup"><span data-stu-id="6dadd-792">cElements</span></span>

<span data-ttu-id="6dadd-793">lLbound</span><span class="sxs-lookup"><span data-stu-id="6dadd-793">lLbound</span></span>



 

<span data-ttu-id="6dadd-794">**cElements**: um inteiro sem sinal de 32 bits, especificando o número de elementos na dimensão.</span><span class="sxs-lookup"><span data-stu-id="6dadd-794">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="6dadd-795">**lLbound**: um inteiro sem sinal de 32 bits, especificando o limite inferior da dimensão.</span><span class="sxs-lookup"><span data-stu-id="6dadd-795">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="6dadd-796">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="6dadd-796">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="6dadd-797">SAFEARRAY2 é usado para passar matrizes multidimensionais em SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="6dadd-797">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="6dadd-798">A estrutura contém informações de limite, bem como os dados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-798">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="6dadd-799">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-799">0</span></span>

<span data-ttu-id="6dadd-800">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-800">1</span></span>

<span data-ttu-id="6dadd-801">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-801">2</span></span>

<span data-ttu-id="6dadd-802">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-802">3</span></span>

<span data-ttu-id="6dadd-803">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-803">4</span></span>

<span data-ttu-id="6dadd-804">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-804">5</span></span>

<span data-ttu-id="6dadd-805">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-805">6</span></span>

<span data-ttu-id="6dadd-806">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-806">7</span></span>

<span data-ttu-id="6dadd-807">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-807">8</span></span>

<span data-ttu-id="6dadd-808">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-808">9</span></span>

<span data-ttu-id="6dadd-809">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-809">1</span></span><br/> <span data-ttu-id="6dadd-810">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-810">0</span></span><br/>

<span data-ttu-id="6dadd-811">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-811">1</span></span>

<span data-ttu-id="6dadd-812">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-812">2</span></span>

<span data-ttu-id="6dadd-813">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-813">3</span></span>

<span data-ttu-id="6dadd-814">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-814">4</span></span>

<span data-ttu-id="6dadd-815">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-815">5</span></span>

<span data-ttu-id="6dadd-816">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-816">6</span></span>

<span data-ttu-id="6dadd-817">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-817">7</span></span>

<span data-ttu-id="6dadd-818">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-818">8</span></span>

<span data-ttu-id="6dadd-819">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-819">9</span></span>

<span data-ttu-id="6dadd-820">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-820">2</span></span><br/> <span data-ttu-id="6dadd-821">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-821">0</span></span><br/>

<span data-ttu-id="6dadd-822">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-822">1</span></span>

<span data-ttu-id="6dadd-823">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-823">2</span></span>

<span data-ttu-id="6dadd-824">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-824">3</span></span>

<span data-ttu-id="6dadd-825">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-825">4</span></span>

<span data-ttu-id="6dadd-826">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-826">5</span></span>

<span data-ttu-id="6dadd-827">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-827">6</span></span>

<span data-ttu-id="6dadd-828">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-828">7</span></span>

<span data-ttu-id="6dadd-829">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-829">8</span></span>

<span data-ttu-id="6dadd-830">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-830">9</span></span>

<span data-ttu-id="6dadd-831">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-831">3</span></span><br/> <span data-ttu-id="6dadd-832">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-832">0</span></span><br/>

<span data-ttu-id="6dadd-833">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-833">1</span></span>

<span data-ttu-id="6dadd-834">cDims</span><span class="sxs-lookup"><span data-stu-id="6dadd-834">cDims</span></span>

<span data-ttu-id="6dadd-835">Rgsabound (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-835">Rgsabound (variable)</span></span>

<span data-ttu-id="6dadd-836">vData (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-836">vData (variable)</span></span>



 

<span data-ttu-id="6dadd-837">**cDims:** inteiro de 32 bits sem sinal, indicando o número de dimensões do SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="6dadd-837">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="6dadd-838">**Rgsabound:** uma matriz que contém uma estrutura SAFEARRAYBOUND, conforme especificado na seção 2.2.1.1.1.4 por dimensão em SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="6dadd-838">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="6dadd-839">Essa matriz tem a dimensão mais à esquerda primeiro e a dimensão mais à direita por último.</span><span class="sxs-lookup"><span data-stu-id="6dadd-839">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="6dadd-840">**vData:** um vetor de itens com marshaling de um tipo específico, indicado pelo dwType do que contém SERIALIZEDPROPERTYVALUE, com o bit 0x2000 limpo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-840">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="6dadd-841">O formato de vData igual ao especificado para o campo vData de SAFEARRAY na Seção 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="6dadd-841">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="6dadd-842">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="6dadd-842">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="6dadd-843">A estrutura CFullPropSpec contém um GUID do conjunto de propriedades e um identificador de propriedade para identificar exclusivamente a propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-843">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="6dadd-844">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-844">0</span></span>

<span data-ttu-id="6dadd-845">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-845">1</span></span>

<span data-ttu-id="6dadd-846">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-846">2</span></span>

<span data-ttu-id="6dadd-847">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-847">3</span></span>

<span data-ttu-id="6dadd-848">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-848">4</span></span>

<span data-ttu-id="6dadd-849">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-849">5</span></span>

<span data-ttu-id="6dadd-850">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-850">6</span></span>

<span data-ttu-id="6dadd-851">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-851">7</span></span>

<span data-ttu-id="6dadd-852">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-852">8</span></span>

<span data-ttu-id="6dadd-853">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-853">9</span></span>

<span data-ttu-id="6dadd-854">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-854">1</span></span><br/> <span data-ttu-id="6dadd-855">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-855">0</span></span><br/>

<span data-ttu-id="6dadd-856">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-856">1</span></span>

<span data-ttu-id="6dadd-857">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-857">2</span></span>

<span data-ttu-id="6dadd-858">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-858">3</span></span>

<span data-ttu-id="6dadd-859">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-859">4</span></span>

<span data-ttu-id="6dadd-860">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-860">5</span></span>

<span data-ttu-id="6dadd-861">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-861">6</span></span>

<span data-ttu-id="6dadd-862">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-862">7</span></span>

<span data-ttu-id="6dadd-863">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-863">8</span></span>

<span data-ttu-id="6dadd-864">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-864">9</span></span>

<span data-ttu-id="6dadd-865">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-865">2</span></span><br/> <span data-ttu-id="6dadd-866">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-866">0</span></span><br/>

<span data-ttu-id="6dadd-867">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-867">1</span></span>

<span data-ttu-id="6dadd-868">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-868">2</span></span>

<span data-ttu-id="6dadd-869">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-869">3</span></span>

<span data-ttu-id="6dadd-870">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-870">4</span></span>

<span data-ttu-id="6dadd-871">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-871">5</span></span>

<span data-ttu-id="6dadd-872">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-872">6</span></span>

<span data-ttu-id="6dadd-873">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-873">7</span></span>

<span data-ttu-id="6dadd-874">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-874">8</span></span>

<span data-ttu-id="6dadd-875">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-875">9</span></span>

<span data-ttu-id="6dadd-876">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-876">3</span></span><br/> <span data-ttu-id="6dadd-877">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-877">0</span></span><br/>

<span data-ttu-id="6dadd-878">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-878">1</span></span>

<span data-ttu-id="6dadd-879">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-879">\_guidPropSet</span></span>

<span data-ttu-id="6dadd-880">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-880">...</span></span>

<span data-ttu-id="6dadd-881">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-881">...</span></span>

<span data-ttu-id="6dadd-882">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-882">...</span></span>

<span data-ttu-id="6dadd-883">ulKind</span><span class="sxs-lookup"><span data-stu-id="6dadd-883">ulKind</span></span>

<span data-ttu-id="6dadd-884">PrSpec</span><span class="sxs-lookup"><span data-stu-id="6dadd-884">PrSpec</span></span>

<span data-ttu-id="6dadd-885">Nome da propriedade (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-885">Property name (variable)</span></span>



 

<span data-ttu-id="6dadd-886">**\_ guidPropSet:** o GUID do conjunto de propriedades ao qual a propriedade pertence.</span><span class="sxs-lookup"><span data-stu-id="6dadd-886">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="6dadd-887">**ulKind:** um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-887">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="6dadd-888">Um dos seguintes valores abaixo, que indica o conteúdo de PrSpec.</span><span class="sxs-lookup"><span data-stu-id="6dadd-888">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="6dadd-889">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-889">Value</span></span>                                            | <span data-ttu-id="6dadd-890">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-890">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-891">PRSPEC \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="6dadd-891">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="6dadd-892">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-892">0x00000000</span></span><br/> | <span data-ttu-id="6dadd-893">O campo PrSpec especifica o número de caracteres não NULL no campo Nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-893">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="6dadd-894">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="6dadd-894">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="6dadd-895">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-895">0x00000001</span></span><br/>  | <span data-ttu-id="6dadd-896">O campo PrSpec especifica a ID da propriedade (PROPID).</span><span class="sxs-lookup"><span data-stu-id="6dadd-896">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="6dadd-897">**PrSpec:** um inteiro sem sinal de 32 bits com um significado conforme indicado pelo campo ulKind.</span><span class="sxs-lookup"><span data-stu-id="6dadd-897">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="6dadd-898">**Nome da** propriedade: se ulKind for definido como PRSPEC \_ PROPID, esse campo NÃO DEVERÁ estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-898">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="6dadd-899">Se ulKind for definido como PRSPEC LPWSTR, esse campo DEVERÁ conter uma matriz de caracteres Unicode não nulos PrSpec, contendo o nome da \_ propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-899">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="6dadd-900">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-900">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="6dadd-901">A estrutura CContentRestriction contém uma cadeia de caracteres para corresponder a uma propriedade no cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dadd-901">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="6dadd-902">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-902">0</span></span>

<span data-ttu-id="6dadd-903">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-903">1</span></span>

<span data-ttu-id="6dadd-904">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-904">2</span></span>

<span data-ttu-id="6dadd-905">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-905">3</span></span>

<span data-ttu-id="6dadd-906">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-906">4</span></span>

<span data-ttu-id="6dadd-907">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-907">5</span></span>

<span data-ttu-id="6dadd-908">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-908">6</span></span>

<span data-ttu-id="6dadd-909">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-909">7</span></span>

<span data-ttu-id="6dadd-910">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-910">8</span></span>

<span data-ttu-id="6dadd-911">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-911">9</span></span>

<span data-ttu-id="6dadd-912">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-912">1</span></span><br/> <span data-ttu-id="6dadd-913">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-913">0</span></span><br/>

<span data-ttu-id="6dadd-914">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-914">1</span></span>

<span data-ttu-id="6dadd-915">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-915">2</span></span>

<span data-ttu-id="6dadd-916">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-916">3</span></span>

<span data-ttu-id="6dadd-917">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-917">4</span></span>

<span data-ttu-id="6dadd-918">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-918">5</span></span>

<span data-ttu-id="6dadd-919">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-919">6</span></span>

<span data-ttu-id="6dadd-920">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-920">7</span></span>

<span data-ttu-id="6dadd-921">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-921">8</span></span>

<span data-ttu-id="6dadd-922">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-922">9</span></span>

<span data-ttu-id="6dadd-923">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-923">2</span></span><br/> <span data-ttu-id="6dadd-924">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-924">0</span></span><br/>

<span data-ttu-id="6dadd-925">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-925">1</span></span>

<span data-ttu-id="6dadd-926">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-926">2</span></span>

<span data-ttu-id="6dadd-927">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-927">3</span></span>

<span data-ttu-id="6dadd-928">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-928">4</span></span>

<span data-ttu-id="6dadd-929">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-929">5</span></span>

<span data-ttu-id="6dadd-930">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-930">6</span></span>

<span data-ttu-id="6dadd-931">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-931">7</span></span>

<span data-ttu-id="6dadd-932">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-932">8</span></span>

<span data-ttu-id="6dadd-933">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-933">9</span></span>

<span data-ttu-id="6dadd-934">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-934">3</span></span><br/> <span data-ttu-id="6dadd-935">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-935">0</span></span><br/>

<span data-ttu-id="6dadd-936">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-936">1</span></span>

<span data-ttu-id="6dadd-937">\_Propriedade (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-937">\_Property (variable)</span></span>

<span data-ttu-id="6dadd-938">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-938">...</span></span>

<span data-ttu-id="6dadd-939">Padding1 (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-939">Padding1 (variable)</span></span>

<span data-ttu-id="6dadd-940">Cc</span><span class="sxs-lookup"><span data-stu-id="6dadd-940">Cc</span></span>

<span data-ttu-id="6dadd-941">\_pwcsPhrase (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-941">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="6dadd-942">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-942">...</span></span>

<span data-ttu-id="6dadd-943">Padding2 (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-943">Padding2 (variable)</span></span>

<span data-ttu-id="6dadd-944">lcid</span><span class="sxs-lookup"><span data-stu-id="6dadd-944">lcid</span></span>

<span data-ttu-id="6dadd-945">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="6dadd-945">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="6dadd-946">**\_ Propriedade**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="6dadd-946">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="6dadd-947">Este campo indica a propriedade na qual executar uma operação de correspondência.</span><span class="sxs-lookup"><span data-stu-id="6dadd-947">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="6dadd-948">**Padding1**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-948">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="6dadd-949">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-949">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="6dadd-950">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-950">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="6dadd-951">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-951">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-952">**CC**: um inteiro de 32 bits sem sinal, especificando o número de caracteres no \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="6dadd-952">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="6dadd-953">**\_ pwcsPhrase**: uma cadeia de caracteres Unicode não terminada em nulo que representa a palavra ou frase para corresponder à propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-953">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="6dadd-954">Este campo não deve estar vazio.</span><span class="sxs-lookup"><span data-stu-id="6dadd-954">This field MUST NOT be empty.</span></span> <span data-ttu-id="6dadd-955">O campo Cc contém o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6dadd-955">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="6dadd-956">**Padding2**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-956">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="6dadd-957">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-957">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="6dadd-958">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-958">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="6dadd-959">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-959">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-960">**LCID**: um inteiro sem sinal de 32 bits, indicando a localidade de \_ pwcsPhrase, conforme especificado em \[ MS-GPSI \] Apêndice A.</span><span class="sxs-lookup"><span data-stu-id="6dadd-960">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="6dadd-961">**\_ ulGenerateMethod**: um inteiro sem sinal de 32 bits, especificando o método a ser usado ao gerar formulários alternativos de palavra</span><span class="sxs-lookup"><span data-stu-id="6dadd-961">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="6dadd-962">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-962">Value</span></span>                                                       | <span data-ttu-id="6dadd-963">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-963">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-964">GERAR \_ método \_ exato</span><span class="sxs-lookup"><span data-stu-id="6dadd-964">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="6dadd-965">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-965">0x00000000</span></span><br/>    | <span data-ttu-id="6dadd-966">Correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="6dadd-966">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6dadd-967">GERAR \_ prefixo de método \_</span><span class="sxs-lookup"><span data-stu-id="6dadd-967">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="6dadd-968">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-968">0x00000001</span></span> <br/>  | <span data-ttu-id="6dadd-969">Correspondência de prefixo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-969">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="6dadd-970">GERAR \_ método \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="6dadd-970">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="6dadd-971">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-971">0x00000002</span></span><br/> | <span data-ttu-id="6dadd-972">Faz a correspondência de inflexões de uma palavra.</span><span class="sxs-lookup"><span data-stu-id="6dadd-972">Matches inflections of a word.</span></span> <span data-ttu-id="6dadd-973">Uma inflexão de uma palavra é uma variante da palavra raiz na mesma parte da fala que foi modificada de acordo com as regras linguísticas de um determinado idioma.</span><span class="sxs-lookup"><span data-stu-id="6dadd-973">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="6dadd-974">Por exemplo, as inflexidades do verbo "nada" em inglês incluem "nada", "nada", "nada" e "Swam".</span><span class="sxs-lookup"><span data-stu-id="6dadd-974">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="6dadd-975">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="6dadd-975">2.2.1.4 CKey</span></span>

<span data-ttu-id="6dadd-976">A estrutura CKey contém um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-976">The CKey structure contains a property value.</span></span>



<span data-ttu-id="6dadd-977">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-977">0</span></span>

<span data-ttu-id="6dadd-978">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-978">1</span></span>

<span data-ttu-id="6dadd-979">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-979">2</span></span>

<span data-ttu-id="6dadd-980">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-980">3</span></span>

<span data-ttu-id="6dadd-981">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-981">4</span></span>

<span data-ttu-id="6dadd-982">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-982">5</span></span>

<span data-ttu-id="6dadd-983">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-983">6</span></span>

<span data-ttu-id="6dadd-984">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-984">7</span></span>

<span data-ttu-id="6dadd-985">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-985">8</span></span>

<span data-ttu-id="6dadd-986">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-986">9</span></span>

<span data-ttu-id="6dadd-987">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-987">1</span></span><br/> <span data-ttu-id="6dadd-988">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-988">0</span></span><br/>

<span data-ttu-id="6dadd-989">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-989">1</span></span>

<span data-ttu-id="6dadd-990">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-990">2</span></span>

<span data-ttu-id="6dadd-991">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-991">3</span></span>

<span data-ttu-id="6dadd-992">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-992">4</span></span>

<span data-ttu-id="6dadd-993">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-993">5</span></span>

<span data-ttu-id="6dadd-994">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-994">6</span></span>

<span data-ttu-id="6dadd-995">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-995">7</span></span>

<span data-ttu-id="6dadd-996">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-996">8</span></span>

<span data-ttu-id="6dadd-997">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-997">9</span></span>

<span data-ttu-id="6dadd-998">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-998">2</span></span><br/> <span data-ttu-id="6dadd-999">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-999">0</span></span><br/>

<span data-ttu-id="6dadd-1000">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1000">1</span></span>

<span data-ttu-id="6dadd-1001">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1001">2</span></span>

<span data-ttu-id="6dadd-1002">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1002">3</span></span>

<span data-ttu-id="6dadd-1003">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1003">4</span></span>

<span data-ttu-id="6dadd-1004">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1004">5</span></span>

<span data-ttu-id="6dadd-1005">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1005">6</span></span>

<span data-ttu-id="6dadd-1006">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1006">7</span></span>

<span data-ttu-id="6dadd-1007">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1007">8</span></span>

<span data-ttu-id="6dadd-1008">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1008">9</span></span>

<span data-ttu-id="6dadd-1009">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1009">3</span></span><br/> <span data-ttu-id="6dadd-1010">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1010">0</span></span><br/>

<span data-ttu-id="6dadd-1011">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1011">1</span></span>

<span data-ttu-id="6dadd-1012">Propid</span><span class="sxs-lookup"><span data-stu-id="6dadd-1012">PROPID</span></span>

<span data-ttu-id="6dadd-1013">Cb</span><span class="sxs-lookup"><span data-stu-id="6dadd-1013">Cb</span></span>

<span data-ttu-id="6dadd-1014">buf (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1014">buf (variable)</span></span>



 

<span data-ttu-id="6dadd-1015">**PROPID:** um inteiro sem sinal de 32 bits, que representa a ID da propriedade, conforme discutido na seção 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1015">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="6dadd-1016">Os valores conhecidos são:</span><span class="sxs-lookup"><span data-stu-id="6dadd-1016">Well-known values are:</span></span>



| <span data-ttu-id="6dadd-1017">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1017">Value</span></span>      | <span data-ttu-id="6dadd-1018">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1018">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="6dadd-1019">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="6dadd-1019">0xFFFFFFFF</span></span> | <span data-ttu-id="6dadd-1020">Representa uma ID de propriedade inválida e NÃO DEVE ser usado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1020">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="6dadd-1021">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="6dadd-1021">0xFFFFFFFE</span></span> | <span data-ttu-id="6dadd-1022">Representa uma ID de propriedade inválida e NÃO DEVE ser usado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1022">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="6dadd-1023">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-1023">0x00000000</span></span> | <span data-ttu-id="6dadd-1024">Representa qualquer ID de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1024">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="6dadd-1025">**Cb:** um inteiro sem sinal de 32 bits que contém o comprimento de buf, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1025">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="6dadd-1026">**buf**: uma sequência de bytes que representa o valor da propriedade .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1026">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="6dadd-1027">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1027">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="6dadd-1028">A estrutura CInternalPropertyRestriction contém um valor da propriedade para corresponder a uma operação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1028">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="6dadd-1029">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1029">0</span></span>

<span data-ttu-id="6dadd-1030">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1030">1</span></span>

<span data-ttu-id="6dadd-1031">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1031">2</span></span>

<span data-ttu-id="6dadd-1032">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1032">3</span></span>

<span data-ttu-id="6dadd-1033">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1033">4</span></span>

<span data-ttu-id="6dadd-1034">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1034">5</span></span>

<span data-ttu-id="6dadd-1035">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1035">6</span></span>

<span data-ttu-id="6dadd-1036">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1036">7</span></span>

<span data-ttu-id="6dadd-1037">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1037">8</span></span>

<span data-ttu-id="6dadd-1038">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1038">9</span></span>

<span data-ttu-id="6dadd-1039">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1039">1</span></span><br/> <span data-ttu-id="6dadd-1040">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1040">0</span></span><br/>

<span data-ttu-id="6dadd-1041">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1041">1</span></span>

<span data-ttu-id="6dadd-1042">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1042">2</span></span>

<span data-ttu-id="6dadd-1043">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1043">3</span></span>

<span data-ttu-id="6dadd-1044">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1044">4</span></span>

<span data-ttu-id="6dadd-1045">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1045">5</span></span>

<span data-ttu-id="6dadd-1046">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1046">6</span></span>

<span data-ttu-id="6dadd-1047">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1047">7</span></span>

<span data-ttu-id="6dadd-1048">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1048">8</span></span>

<span data-ttu-id="6dadd-1049">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1049">9</span></span>

<span data-ttu-id="6dadd-1050">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1050">2</span></span><br/> <span data-ttu-id="6dadd-1051">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1051">0</span></span><br/>

<span data-ttu-id="6dadd-1052">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1052">1</span></span>

<span data-ttu-id="6dadd-1053">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1053">2</span></span>

<span data-ttu-id="6dadd-1054">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1054">3</span></span>

<span data-ttu-id="6dadd-1055">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1055">4</span></span>

<span data-ttu-id="6dadd-1056">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1056">5</span></span>

<span data-ttu-id="6dadd-1057">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1057">6</span></span>

<span data-ttu-id="6dadd-1058">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1058">7</span></span>

<span data-ttu-id="6dadd-1059">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1059">8</span></span>

<span data-ttu-id="6dadd-1060">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1060">9</span></span>

<span data-ttu-id="6dadd-1061">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1061">3</span></span><br/> <span data-ttu-id="6dadd-1062">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1062">0</span></span><br/>

<span data-ttu-id="6dadd-1063">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1063">1</span></span>

<span data-ttu-id="6dadd-1064">\_reope</span><span class="sxs-lookup"><span data-stu-id="6dadd-1064">\_relop</span></span>

<span data-ttu-id="6dadd-1065">\_Pid</span><span class="sxs-lookup"><span data-stu-id="6dadd-1065">\_pid</span></span>

<span data-ttu-id="6dadd-1066">\_prval (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1066">\_prval (variable)</span></span>

<span data-ttu-id="6dadd-1067">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="6dadd-1067">restrictionPresent</span></span>

<span data-ttu-id="6dadd-1068">nextRestriction (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1068">nextRestriction (variable)</span></span>



 

<span data-ttu-id="6dadd-1069">**\_ reope:** um inteiro de 32 bits que especifica a relação a ser executar na propriedade .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1069">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="6dadd-1070">DEVE ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6dadd-1070">MUST be one of the following values:</span></span>



| <span data-ttu-id="6dadd-1071">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1071">Value</span></span>                 | <span data-ttu-id="6dadd-1072">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1072">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-1073">PrLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-1073">PRLT 0x00000000</span></span>       | <span data-ttu-id="6dadd-1074">Uma comparação menor que.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1074">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="6dadd-1075">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-1075">PRLE 0x00000001</span></span>       | <span data-ttu-id="6dadd-1076">Uma comparação menor ou igual a.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1076">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="6dadd-1077">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-1077">PRGT 0x00000002</span></span>       | <span data-ttu-id="6dadd-1078">Uma comparação maior que.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1078">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="6dadd-1079">PrGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-1079">PRGE 0x00000003</span></span>       | <span data-ttu-id="6dadd-1080">Uma comparação maior ou igual a.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1080">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="6dadd-1081">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-1081">PREQ 0x00000004</span></span>       | <span data-ttu-id="6dadd-1082">Uma comparação de igualdade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1082">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="6dadd-1083">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="6dadd-1083">PRNE 0x00000005</span></span>       | <span data-ttu-id="6dadd-1084">Uma comparação não igual.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1084">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="6dadd-1085">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="6dadd-1085">PRRE 0x00000006</span></span>       | <span data-ttu-id="6dadd-1086">Uma comparação de expressão regular.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1086">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="6dadd-1087">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="6dadd-1087">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="6dadd-1088">Um AND bit a bit que retorna o operand direito.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1088">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="6dadd-1089">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="6dadd-1089">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="6dadd-1090">Um AND bit a bit que retorna um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1090">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="6dadd-1091">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="6dadd-1091">PRAll 0x00000100</span></span>      | <span data-ttu-id="6dadd-1092">A operação deve ser executada em uma coluna de um conjuntos de linhas e só será verdadeira se a operação for verdadeira para todas as linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1092">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="6dadd-1093">PrAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="6dadd-1093">PRAny 0x00000200</span></span>      | <span data-ttu-id="6dadd-1094">A operação deve ser executada em uma coluna de um conjuntos de linhas e será verdadeira se a operação for verdadeira para qualquer linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1094">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="6dadd-1095">**\_ pid:** um inteiro sem sinal de 32 bits, que representa a ID da propriedade (consulte PROPID na seção 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="6dadd-1095">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="6dadd-1096">**\_ prval:** um CBaseStorageVariant que contém o valor a ser relacionado à propriedade .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1096">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="6dadd-1097">**restrictionPresent:** um valor de byte que indica se o campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1097">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="6dadd-1098">DEVE ser definido como 0x00 ou 0x01.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1098">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="6dadd-1099">Se definido como 0x01, restrictionPresent indica que o campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1099">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="6dadd-1100">Se definido como 0x00, restrictionPresent indica que o campo nextRestriction não está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1100">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="6dadd-1101">**nextRestriction:** uma estrutura CRestriction, conforme especificado na seção 2.2.1.16, especificando uma restrição posterior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1101">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="6dadd-1102">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1102">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="6dadd-1103">A estrutura CNatLanguageRestriction contém uma combinação de consulta **de idioma natural** para uma propriedade .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1103">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="6dadd-1104">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1104">0</span></span>

<span data-ttu-id="6dadd-1105">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1105">1</span></span>

<span data-ttu-id="6dadd-1106">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1106">2</span></span>

<span data-ttu-id="6dadd-1107">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1107">3</span></span>

<span data-ttu-id="6dadd-1108">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1108">4</span></span>

<span data-ttu-id="6dadd-1109">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1109">5</span></span>

<span data-ttu-id="6dadd-1110">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1110">6</span></span>

<span data-ttu-id="6dadd-1111">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1111">7</span></span>

<span data-ttu-id="6dadd-1112">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1112">8</span></span>

<span data-ttu-id="6dadd-1113">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1113">9</span></span>

<span data-ttu-id="6dadd-1114">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1114">1</span></span><br/> <span data-ttu-id="6dadd-1115">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1115">0</span></span><br/>

<span data-ttu-id="6dadd-1116">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1116">1</span></span>

<span data-ttu-id="6dadd-1117">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1117">2</span></span>

<span data-ttu-id="6dadd-1118">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1118">3</span></span>

<span data-ttu-id="6dadd-1119">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1119">4</span></span>

<span data-ttu-id="6dadd-1120">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1120">5</span></span>

<span data-ttu-id="6dadd-1121">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1121">6</span></span>

<span data-ttu-id="6dadd-1122">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1122">7</span></span>

<span data-ttu-id="6dadd-1123">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1123">8</span></span>

<span data-ttu-id="6dadd-1124">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1124">9</span></span>

<span data-ttu-id="6dadd-1125">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1125">2</span></span><br/> <span data-ttu-id="6dadd-1126">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1126">0</span></span><br/>

<span data-ttu-id="6dadd-1127">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1127">1</span></span>

<span data-ttu-id="6dadd-1128">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1128">2</span></span>

<span data-ttu-id="6dadd-1129">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1129">3</span></span>

<span data-ttu-id="6dadd-1130">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1130">4</span></span>

<span data-ttu-id="6dadd-1131">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1131">5</span></span>

<span data-ttu-id="6dadd-1132">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1132">6</span></span>

<span data-ttu-id="6dadd-1133">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1133">7</span></span>

<span data-ttu-id="6dadd-1134">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1134">8</span></span>

<span data-ttu-id="6dadd-1135">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1135">9</span></span>

<span data-ttu-id="6dadd-1136">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1136">3</span></span><br/> <span data-ttu-id="6dadd-1137">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1137">0</span></span><br/>

<span data-ttu-id="6dadd-1138">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1138">1</span></span>

<span data-ttu-id="6dadd-1139">\_Propriedade (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1139">\_Property (variable)</span></span>

<span data-ttu-id="6dadd-1140">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1140">...</span></span>

<span data-ttu-id="6dadd-1141">\_preenchimento \_ de CC (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1141">\_padding\_cc (variable)</span></span>

<span data-ttu-id="6dadd-1142">Cc</span><span class="sxs-lookup"><span data-stu-id="6dadd-1142">Cc</span></span>

<span data-ttu-id="6dadd-1143">\_pwcsPhrase (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1143">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="6dadd-1144">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1144">...</span></span>

<span data-ttu-id="6dadd-1145">\_\_LCID de preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1145">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="6dadd-1146">Lcid</span><span class="sxs-lookup"><span data-stu-id="6dadd-1146">Lcid</span></span>



 

<span data-ttu-id="6dadd-1147">**\_ Propriedade**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1147">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="6dadd-1148">Este campo indica a propriedade na qual executar a operação de correspondência.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1148">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="6dadd-1149">**\_ preenchimento \_ CC**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1149">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="6dadd-1150">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1150">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="6dadd-1151">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1151">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="6dadd-1152">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1152">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-1153">**CC**: um inteiro de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1153">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="6dadd-1154">O número de caracteres no \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1154">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="6dadd-1155">**\_ pwcsPhrase**: uma cadeia de caracteres Unicode não terminada em nulo que representa a palavra ou frase para corresponder à propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1155">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="6dadd-1156">Não deve ficar vazio.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1156">MUST NOT be empty.</span></span> <span data-ttu-id="6dadd-1157">O campo Cc contém o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1157">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="6dadd-1158">**\_ \_ LCID de preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1158">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="6dadd-1159">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1159">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="6dadd-1160">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1160">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="6dadd-1161">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1161">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-1162">**LCID**: um inteiro de 32 bits sem sinal indicando a localidade de \_ pwcsPhrase, conforme especificado no \[ Apêndice a do MS-GPSI \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1162">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="6dadd-1163">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1163">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="6dadd-1164">A estrutura CNodeRestriction contém uma matriz de nós de **árvore de comando** que especificam as restrições para a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1164">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="6dadd-1165">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1165">0</span></span>

<span data-ttu-id="6dadd-1166">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1166">1</span></span>

<span data-ttu-id="6dadd-1167">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1167">2</span></span>

<span data-ttu-id="6dadd-1168">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1168">3</span></span>

<span data-ttu-id="6dadd-1169">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1169">4</span></span>

<span data-ttu-id="6dadd-1170">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1170">5</span></span>

<span data-ttu-id="6dadd-1171">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1171">6</span></span>

<span data-ttu-id="6dadd-1172">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1172">7</span></span>

<span data-ttu-id="6dadd-1173">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1173">8</span></span>

<span data-ttu-id="6dadd-1174">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1174">9</span></span>

<span data-ttu-id="6dadd-1175">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1175">1</span></span><br/> <span data-ttu-id="6dadd-1176">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1176">0</span></span><br/>

<span data-ttu-id="6dadd-1177">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1177">1</span></span>

<span data-ttu-id="6dadd-1178">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1178">2</span></span>

<span data-ttu-id="6dadd-1179">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1179">3</span></span>

<span data-ttu-id="6dadd-1180">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1180">4</span></span>

<span data-ttu-id="6dadd-1181">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1181">5</span></span>

<span data-ttu-id="6dadd-1182">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1182">6</span></span>

<span data-ttu-id="6dadd-1183">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1183">7</span></span>

<span data-ttu-id="6dadd-1184">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1184">8</span></span>

<span data-ttu-id="6dadd-1185">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1185">9</span></span>

<span data-ttu-id="6dadd-1186">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1186">2</span></span><br/> <span data-ttu-id="6dadd-1187">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1187">0</span></span><br/>

<span data-ttu-id="6dadd-1188">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1188">1</span></span>

<span data-ttu-id="6dadd-1189">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1189">2</span></span>

<span data-ttu-id="6dadd-1190">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1190">3</span></span>

<span data-ttu-id="6dadd-1191">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1191">4</span></span>

<span data-ttu-id="6dadd-1192">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1192">5</span></span>

<span data-ttu-id="6dadd-1193">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1193">6</span></span>

<span data-ttu-id="6dadd-1194">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1194">7</span></span>

<span data-ttu-id="6dadd-1195">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1195">8</span></span>

<span data-ttu-id="6dadd-1196">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1196">9</span></span>

<span data-ttu-id="6dadd-1197">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1197">3</span></span><br/> <span data-ttu-id="6dadd-1198">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1198">0</span></span><br/>

<span data-ttu-id="6dadd-1199">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1199">1</span></span>

<span data-ttu-id="6dadd-1200">\_cNode</span><span class="sxs-lookup"><span data-stu-id="6dadd-1200">\_cNode</span></span>

<span data-ttu-id="6dadd-1201">\_paNode (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1201">\_paNode (variable)</span></span>



 

<span data-ttu-id="6dadd-1202">**\_ cNode**: um inteiro sem sinal de 32 bits especificando o número de estruturas CRestriction contidas no \_ campo paNode.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1202">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="6dadd-1203">**\_ paNode**: uma matriz de estruturas CRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1203">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="6dadd-1204">As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa matriz.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1204">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="6dadd-1205">Se os bytes de preenchimento estiverem presentes, o valor que eles contêm será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1205">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="6dadd-1206">O conteúdo dos bytes de preenchimento deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1206">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="6dadd-1207">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1207">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="6dadd-1208">A estrutura COccRestriction contém o local de uma palavra em uma frase.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1208">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="6dadd-1209">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1209">0</span></span>

<span data-ttu-id="6dadd-1210">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1210">1</span></span>

<span data-ttu-id="6dadd-1211">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1211">2</span></span>

<span data-ttu-id="6dadd-1212">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1212">3</span></span>

<span data-ttu-id="6dadd-1213">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1213">4</span></span>

<span data-ttu-id="6dadd-1214">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1214">5</span></span>

<span data-ttu-id="6dadd-1215">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1215">6</span></span>

<span data-ttu-id="6dadd-1216">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1216">7</span></span>

<span data-ttu-id="6dadd-1217">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1217">8</span></span>

<span data-ttu-id="6dadd-1218">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1218">9</span></span>

<span data-ttu-id="6dadd-1219">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1219">1</span></span><br/> <span data-ttu-id="6dadd-1220">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1220">0</span></span><br/>

<span data-ttu-id="6dadd-1221">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1221">1</span></span>

<span data-ttu-id="6dadd-1222">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1222">2</span></span>

<span data-ttu-id="6dadd-1223">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1223">3</span></span>

<span data-ttu-id="6dadd-1224">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1224">4</span></span>

<span data-ttu-id="6dadd-1225">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1225">5</span></span>

<span data-ttu-id="6dadd-1226">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1226">6</span></span>

<span data-ttu-id="6dadd-1227">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1227">7</span></span>

<span data-ttu-id="6dadd-1228">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1228">8</span></span>

<span data-ttu-id="6dadd-1229">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1229">9</span></span>

<span data-ttu-id="6dadd-1230">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1230">2</span></span><br/> <span data-ttu-id="6dadd-1231">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1231">0</span></span><br/>

<span data-ttu-id="6dadd-1232">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1232">1</span></span>

<span data-ttu-id="6dadd-1233">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1233">2</span></span>

<span data-ttu-id="6dadd-1234">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1234">3</span></span>

<span data-ttu-id="6dadd-1235">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1235">4</span></span>

<span data-ttu-id="6dadd-1236">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1236">5</span></span>

<span data-ttu-id="6dadd-1237">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1237">6</span></span>

<span data-ttu-id="6dadd-1238">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1238">7</span></span>

<span data-ttu-id="6dadd-1239">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1239">8</span></span>

<span data-ttu-id="6dadd-1240">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1240">9</span></span>

<span data-ttu-id="6dadd-1241">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1241">3</span></span><br/> <span data-ttu-id="6dadd-1242">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1242">0</span></span><br/>

<span data-ttu-id="6dadd-1243">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1243">1</span></span>

<span data-ttu-id="6dadd-1244">\_Occ</span><span class="sxs-lookup"><span data-stu-id="6dadd-1244">\_occ</span></span>

<span data-ttu-id="6dadd-1245">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="6dadd-1245">\_cPrevNoiseWords</span></span>

<span data-ttu-id="6dadd-1246">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="6dadd-1246">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="6dadd-1247">**\_ occ:** um inteiro sem sinal de 32 bits que especifica o deslocamento da palavra em uma cadeia de caracteres de consulta, em unidades de palavras.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1247">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="6dadd-1248">Uma palavra, conforme usada nesta especificação, é uma unidade de linguagem em qualquer localidade que tem significado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1248">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="6dadd-1249">**\_ cPrevNoiseWords:** um inteiro sem sinal de 32  bits que contém o número de palavras de ruído que ocorrem entre essa palavra e a palavra anterior na frase.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1249">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="6dadd-1250">**\_ cNextNoiseWords:** um inteiro sem sinal de 32 bits que contém o número de palavras de ruído que ocorrem entre essa palavra e a próxima palavra na frase.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1250">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="6dadd-1251">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1251">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="6dadd-1252">A estrutura CPropertyRestriction contém um valor da propriedade para corresponder a uma operação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1252">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="6dadd-1253">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1253">0</span></span>

<span data-ttu-id="6dadd-1254">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1254">1</span></span>

<span data-ttu-id="6dadd-1255">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1255">2</span></span>

<span data-ttu-id="6dadd-1256">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1256">3</span></span>

<span data-ttu-id="6dadd-1257">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1257">4</span></span>

<span data-ttu-id="6dadd-1258">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1258">5</span></span>

<span data-ttu-id="6dadd-1259">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1259">6</span></span>

<span data-ttu-id="6dadd-1260">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1260">7</span></span>

<span data-ttu-id="6dadd-1261">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1261">8</span></span>

<span data-ttu-id="6dadd-1262">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1262">9</span></span>

<span data-ttu-id="6dadd-1263">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1263">1</span></span><br/> <span data-ttu-id="6dadd-1264">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1264">0</span></span><br/>

<span data-ttu-id="6dadd-1265">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1265">1</span></span>

<span data-ttu-id="6dadd-1266">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1266">2</span></span>

<span data-ttu-id="6dadd-1267">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1267">3</span></span>

<span data-ttu-id="6dadd-1268">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1268">4</span></span>

<span data-ttu-id="6dadd-1269">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1269">5</span></span>

<span data-ttu-id="6dadd-1270">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1270">6</span></span>

<span data-ttu-id="6dadd-1271">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1271">7</span></span>

<span data-ttu-id="6dadd-1272">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1272">8</span></span>

<span data-ttu-id="6dadd-1273">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1273">9</span></span>

<span data-ttu-id="6dadd-1274">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1274">2</span></span><br/> <span data-ttu-id="6dadd-1275">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1275">0</span></span><br/>

<span data-ttu-id="6dadd-1276">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1276">1</span></span>

<span data-ttu-id="6dadd-1277">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1277">2</span></span>

<span data-ttu-id="6dadd-1278">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1278">3</span></span>

<span data-ttu-id="6dadd-1279">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1279">4</span></span>

<span data-ttu-id="6dadd-1280">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1280">5</span></span>

<span data-ttu-id="6dadd-1281">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1281">6</span></span>

<span data-ttu-id="6dadd-1282">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1282">7</span></span>

<span data-ttu-id="6dadd-1283">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1283">8</span></span>

<span data-ttu-id="6dadd-1284">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1284">9</span></span>

<span data-ttu-id="6dadd-1285">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1285">3</span></span><br/> <span data-ttu-id="6dadd-1286">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1286">0</span></span><br/>

<span data-ttu-id="6dadd-1287">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1287">1</span></span>

<span data-ttu-id="6dadd-1288">\_reope</span><span class="sxs-lookup"><span data-stu-id="6dadd-1288">\_relop</span></span>

<span data-ttu-id="6dadd-1289">\_Propriedade (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1289">\_Property (variable)</span></span>

<span data-ttu-id="6dadd-1290">\_prval (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1290">\_prval (variable)</span></span>



 

<span data-ttu-id="6dadd-1291">**\_ relop:** um inteiro sem sinal de 32 bits que especifica a relação a ser executar na propriedade .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1291">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="6dadd-1292">DEVE ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1292">MUST be one of the following values.</span></span>



| <span data-ttu-id="6dadd-1293">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1293">Value</span></span>                 | <span data-ttu-id="6dadd-1294">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1294">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-1295">PrLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-1295">PRLT 0x00000000</span></span>       | <span data-ttu-id="6dadd-1296">Uma comparação menor que.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1296">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="6dadd-1297">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-1297">PRLE 0x00000001</span></span>       | <span data-ttu-id="6dadd-1298">Uma comparação menor ou igual a.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1298">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="6dadd-1299">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-1299">PRGT 0x00000002</span></span>       | <span data-ttu-id="6dadd-1300">Uma comparação maior que.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1300">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="6dadd-1301">PrGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-1301">PRGE 0x00000003</span></span>       | <span data-ttu-id="6dadd-1302">Uma comparação maior ou igual a.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1302">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="6dadd-1303">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-1303">PREQ 0x00000004</span></span>       | <span data-ttu-id="6dadd-1304">Uma comparação de igualdade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1304">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="6dadd-1305">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="6dadd-1305">PRNE 0x00000005</span></span>       | <span data-ttu-id="6dadd-1306">Uma comparação não igual.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1306">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="6dadd-1307">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="6dadd-1307">PRRE 0x00000006</span></span>       | <span data-ttu-id="6dadd-1308">Uma comparação de expressão regular.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1308">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="6dadd-1309">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="6dadd-1309">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="6dadd-1310">Um operador e bit que retorna o operando à direita.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1310">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="6dadd-1311">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="6dadd-1311">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="6dadd-1312">Um valor bit e AND que retorna um Value diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1312">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="6dadd-1313">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="6dadd-1313">PRAll 0x00000100</span></span>      | <span data-ttu-id="6dadd-1314">A operação deve ser executada em uma coluna de um conjunto de linhas e só será verdadeira se a operação for verdadeira para todas as linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1314">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="6dadd-1315">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="6dadd-1315">PRAny 0x00000200</span></span>      | <span data-ttu-id="6dadd-1316">A operação deve ser executada em uma coluna de um conjunto de linhas e será true se a operação for verdadeira para qualquer linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1316">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="6dadd-1317">**\_ Propriedade**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.2, indicando a propriedade na qual executar uma operação de correspondência.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1317">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="6dadd-1318">**\_ prval**: uma estrutura CBaseStorageVariant, conforme especificado na seção 2.2.1.1, que contém o valor a ser relacionado à propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1318">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="6dadd-1319">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1319">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="6dadd-1320">A estrutura CRangeRestriction contém uma restrição em um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1320">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="6dadd-1321">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1321">0</span></span>

<span data-ttu-id="6dadd-1322">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1322">1</span></span>

<span data-ttu-id="6dadd-1323">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1323">2</span></span>

<span data-ttu-id="6dadd-1324">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1324">3</span></span>

<span data-ttu-id="6dadd-1325">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1325">4</span></span>

<span data-ttu-id="6dadd-1326">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1326">5</span></span>

<span data-ttu-id="6dadd-1327">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1327">6</span></span>

<span data-ttu-id="6dadd-1328">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1328">7</span></span>

<span data-ttu-id="6dadd-1329">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1329">8</span></span>

<span data-ttu-id="6dadd-1330">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1330">9</span></span>

<span data-ttu-id="6dadd-1331">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1331">1</span></span><br/> <span data-ttu-id="6dadd-1332">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1332">0</span></span><br/>

<span data-ttu-id="6dadd-1333">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1333">1</span></span>

<span data-ttu-id="6dadd-1334">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1334">2</span></span>

<span data-ttu-id="6dadd-1335">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1335">3</span></span>

<span data-ttu-id="6dadd-1336">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1336">4</span></span>

<span data-ttu-id="6dadd-1337">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1337">5</span></span>

<span data-ttu-id="6dadd-1338">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1338">6</span></span>

<span data-ttu-id="6dadd-1339">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1339">7</span></span>

<span data-ttu-id="6dadd-1340">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1340">8</span></span>

<span data-ttu-id="6dadd-1341">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1341">9</span></span>

<span data-ttu-id="6dadd-1342">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1342">2</span></span><br/> <span data-ttu-id="6dadd-1343">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1343">0</span></span><br/>

<span data-ttu-id="6dadd-1344">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1344">1</span></span>

<span data-ttu-id="6dadd-1345">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1345">2</span></span>

<span data-ttu-id="6dadd-1346">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1346">3</span></span>

<span data-ttu-id="6dadd-1347">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1347">4</span></span>

<span data-ttu-id="6dadd-1348">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1348">5</span></span>

<span data-ttu-id="6dadd-1349">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1349">6</span></span>

<span data-ttu-id="6dadd-1350">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1350">7</span></span>

<span data-ttu-id="6dadd-1351">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1351">8</span></span>

<span data-ttu-id="6dadd-1352">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1352">9</span></span>

<span data-ttu-id="6dadd-1353">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1353">3</span></span><br/> <span data-ttu-id="6dadd-1354">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1354">0</span></span><br/>

<span data-ttu-id="6dadd-1355">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1355">1</span></span>

<span data-ttu-id="6dadd-1356">\_keystart (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1356">\_keyStart (variable)</span></span>

<span data-ttu-id="6dadd-1357">\_keyEnd (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1357">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="6dadd-1358">**\_ keystart**: uma estrutura CKey, conforme especificado na seção 2.2.1.4, que contém o início do intervalo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1358">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="6dadd-1359">**\_ keyEnd**: uma estrutura CKey que contém o final do intervalo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1359">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="6dadd-1360">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1360">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="6dadd-1361">A estrutura CScopeRestriction contém uma restrição nos arquivos a serem pesquisados</span><span class="sxs-lookup"><span data-stu-id="6dadd-1361">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="6dadd-1362">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1362">0</span></span>

<span data-ttu-id="6dadd-1363">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1363">1</span></span>

<span data-ttu-id="6dadd-1364">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1364">2</span></span>

<span data-ttu-id="6dadd-1365">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1365">3</span></span>

<span data-ttu-id="6dadd-1366">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1366">4</span></span>

<span data-ttu-id="6dadd-1367">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1367">5</span></span>

<span data-ttu-id="6dadd-1368">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1368">6</span></span>

<span data-ttu-id="6dadd-1369">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1369">7</span></span>

<span data-ttu-id="6dadd-1370">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1370">8</span></span>

<span data-ttu-id="6dadd-1371">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1371">9</span></span>

<span data-ttu-id="6dadd-1372">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1372">1</span></span><br/> <span data-ttu-id="6dadd-1373">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1373">0</span></span><br/>

<span data-ttu-id="6dadd-1374">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1374">1</span></span>

<span data-ttu-id="6dadd-1375">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1375">2</span></span>

<span data-ttu-id="6dadd-1376">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1376">3</span></span>

<span data-ttu-id="6dadd-1377">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1377">4</span></span>

<span data-ttu-id="6dadd-1378">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1378">5</span></span>

<span data-ttu-id="6dadd-1379">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1379">6</span></span>

<span data-ttu-id="6dadd-1380">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1380">7</span></span>

<span data-ttu-id="6dadd-1381">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1381">8</span></span>

<span data-ttu-id="6dadd-1382">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1382">9</span></span>

<span data-ttu-id="6dadd-1383">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1383">2</span></span><br/> <span data-ttu-id="6dadd-1384">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1384">0</span></span><br/>

<span data-ttu-id="6dadd-1385">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1385">1</span></span>

<span data-ttu-id="6dadd-1386">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1386">2</span></span>

<span data-ttu-id="6dadd-1387">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1387">3</span></span>

<span data-ttu-id="6dadd-1388">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1388">4</span></span>

<span data-ttu-id="6dadd-1389">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1389">5</span></span>

<span data-ttu-id="6dadd-1390">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1390">6</span></span>

<span data-ttu-id="6dadd-1391">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1391">7</span></span>

<span data-ttu-id="6dadd-1392">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1392">8</span></span>

<span data-ttu-id="6dadd-1393">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1393">9</span></span>

<span data-ttu-id="6dadd-1394">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1394">3</span></span><br/> <span data-ttu-id="6dadd-1395">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1395">0</span></span><br/>

<span data-ttu-id="6dadd-1396">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1396">1</span></span>

<span data-ttu-id="6dadd-1397">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="6dadd-1397">CcLowerPath</span></span>

<span data-ttu-id="6dadd-1398">\_lowerPath (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1398">\_lowerPath (variable)</span></span>

<span data-ttu-id="6dadd-1399">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1399">...</span></span>

<span data-ttu-id="6dadd-1400">\_preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1400">\_padding ( variable)</span></span>

<span data-ttu-id="6dadd-1401">\_muito</span><span class="sxs-lookup"><span data-stu-id="6dadd-1401">\_length</span></span>

<span data-ttu-id="6dadd-1402">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="6dadd-1402">\_fRecursive</span></span>

<span data-ttu-id="6dadd-1403">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="6dadd-1403">\_fVirtual</span></span>



 

<span data-ttu-id="6dadd-1404">**CcLowerPath**: um inteiro sem sinal de 32 bits contendo o número de caracteres Unicode no \_ campo lowerPath.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1404">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="6dadd-1405">**\_ lowerPath**: uma cadeia de caracteres Unicode não terminada em nulo que representa o **caminho** para o qual a consulta deve ser restrita.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1405">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="6dadd-1406">O campo CcLowerPath contém o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1406">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="6dadd-1407">**\_ preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1407">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="6dadd-1408">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1408">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="6dadd-1409">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1409">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="6dadd-1410">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1410">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-1411">**\_ comprimento**: um inteiro sem sinal de 32 bits contendo o comprimento de \_ LowerPath, em caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1411">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="6dadd-1412">DEVE ser o mesmo valor que CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1412">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="6dadd-1413">**\_ fRecursive**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1413">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="6dadd-1414">DEVE ser definido como 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1414">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="6dadd-1415">Se definido como 0x00000001, o servidor deve examinar recursivamente todos os subdiretórios do caminho.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1415">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="6dadd-1416">Se definido como 0x00000000, o servidor não examinará nenhum subdiretório.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1416">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="6dadd-1417">**\_ fVirtual**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1417">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="6dadd-1418">DEVE ser definido como 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1418">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="6dadd-1419">Se definido como 0x00000001, \_ lowerPath é um caminho virtual (o Uniform Resource Locator (URL) associado a um diretório físico no sistema de arquivos) para um site da Web.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1419">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="6dadd-1420">Se definido como 0x00000000, \_ lowerPath é um caminho do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1420">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="6dadd-1421">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="6dadd-1421">2.2.1.12 CSort</span></span>

<span data-ttu-id="6dadd-1422">A estrutura CSort identifica uma coluna a ser classificada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1422">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="6dadd-1423">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1423">0</span></span>

<span data-ttu-id="6dadd-1424">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1424">1</span></span>

<span data-ttu-id="6dadd-1425">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1425">2</span></span>

<span data-ttu-id="6dadd-1426">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1426">3</span></span>

<span data-ttu-id="6dadd-1427">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1427">4</span></span>

<span data-ttu-id="6dadd-1428">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1428">5</span></span>

<span data-ttu-id="6dadd-1429">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1429">6</span></span>

<span data-ttu-id="6dadd-1430">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1430">7</span></span>

<span data-ttu-id="6dadd-1431">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1431">8</span></span>

<span data-ttu-id="6dadd-1432">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1432">9</span></span>

<span data-ttu-id="6dadd-1433">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1433">1</span></span><br/> <span data-ttu-id="6dadd-1434">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1434">0</span></span><br/>

<span data-ttu-id="6dadd-1435">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1435">1</span></span>

<span data-ttu-id="6dadd-1436">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1436">2</span></span>

<span data-ttu-id="6dadd-1437">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1437">3</span></span>

<span data-ttu-id="6dadd-1438">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1438">4</span></span>

<span data-ttu-id="6dadd-1439">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1439">5</span></span>

<span data-ttu-id="6dadd-1440">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1440">6</span></span>

<span data-ttu-id="6dadd-1441">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1441">7</span></span>

<span data-ttu-id="6dadd-1442">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1442">8</span></span>

<span data-ttu-id="6dadd-1443">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1443">9</span></span>

<span data-ttu-id="6dadd-1444">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1444">2</span></span><br/> <span data-ttu-id="6dadd-1445">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1445">0</span></span><br/>

<span data-ttu-id="6dadd-1446">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1446">1</span></span>

<span data-ttu-id="6dadd-1447">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1447">2</span></span>

<span data-ttu-id="6dadd-1448">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1448">3</span></span>

<span data-ttu-id="6dadd-1449">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1449">4</span></span>

<span data-ttu-id="6dadd-1450">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1450">5</span></span>

<span data-ttu-id="6dadd-1451">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1451">6</span></span>

<span data-ttu-id="6dadd-1452">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1452">7</span></span>

<span data-ttu-id="6dadd-1453">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1453">8</span></span>

<span data-ttu-id="6dadd-1454">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1454">9</span></span>

<span data-ttu-id="6dadd-1455">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1455">3</span></span><br/> <span data-ttu-id="6dadd-1456">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1456">0</span></span><br/>

<span data-ttu-id="6dadd-1457">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1457">1</span></span>

<span data-ttu-id="6dadd-1458">pidColumn</span><span class="sxs-lookup"><span data-stu-id="6dadd-1458">pidColumn</span></span>

<span data-ttu-id="6dadd-1459">dwOrd</span><span class="sxs-lookup"><span data-stu-id="6dadd-1459">dwOrder</span></span>

<span data-ttu-id="6dadd-1460">localidade</span><span class="sxs-lookup"><span data-stu-id="6dadd-1460">locale</span></span>



 

<span data-ttu-id="6dadd-1461">**pidColumn**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1461">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="6dadd-1462">O número da coluna pela qual classificar.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1462">The number of the column to sort by.</span></span>

<span data-ttu-id="6dadd-1463">**dwOrder**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1463">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="6dadd-1464">DEVE ser um dos valores a seguir, especificando como classificar com base na coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1464">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="6dadd-1465">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1465">Value</span></span>                        | <span data-ttu-id="6dadd-1466">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1466">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-1467">CONSULTAR \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-1467">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="6dadd-1468">As linhas devem ser classificadas em ordem crescente com base nos valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1468">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="6dadd-1469">CONSULTA \_ descendente 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-1469">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="6dadd-1470">As linhas devem ser classificadas em ordem decrescente com base nos valores da coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1470">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="6dadd-1471">**localidade**: um inteiro de 32 bits sem sinal indicando a localidade, conforme especificado no \[ Apêndice a do MS-GPSI \] , da coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1471">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="6dadd-1472">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1472">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="6dadd-1473">A estrutura CSynRestriction contém uma palavra ou seus sinônimos para uma frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1473">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="6dadd-1474">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1474">0</span></span>

<span data-ttu-id="6dadd-1475">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1475">1</span></span>

<span data-ttu-id="6dadd-1476">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1476">2</span></span>

<span data-ttu-id="6dadd-1477">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1477">3</span></span>

<span data-ttu-id="6dadd-1478">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1478">4</span></span>

<span data-ttu-id="6dadd-1479">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1479">5</span></span>

<span data-ttu-id="6dadd-1480">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1480">6</span></span>

<span data-ttu-id="6dadd-1481">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1481">7</span></span>

<span data-ttu-id="6dadd-1482">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1482">8</span></span>

<span data-ttu-id="6dadd-1483">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1483">9</span></span>

<span data-ttu-id="6dadd-1484">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1484">1</span></span><br/> <span data-ttu-id="6dadd-1485">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1485">0</span></span><br/>

<span data-ttu-id="6dadd-1486">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1486">1</span></span>

<span data-ttu-id="6dadd-1487">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1487">2</span></span>

<span data-ttu-id="6dadd-1488">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1488">3</span></span>

<span data-ttu-id="6dadd-1489">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1489">4</span></span>

<span data-ttu-id="6dadd-1490">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1490">5</span></span>

<span data-ttu-id="6dadd-1491">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1491">6</span></span>

<span data-ttu-id="6dadd-1492">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1492">7</span></span>

<span data-ttu-id="6dadd-1493">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1493">8</span></span>

<span data-ttu-id="6dadd-1494">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1494">9</span></span>

<span data-ttu-id="6dadd-1495">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1495">2</span></span><br/> <span data-ttu-id="6dadd-1496">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1496">0</span></span><br/>

<span data-ttu-id="6dadd-1497">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1497">1</span></span>

<span data-ttu-id="6dadd-1498">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1498">2</span></span>

<span data-ttu-id="6dadd-1499">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1499">3</span></span>

<span data-ttu-id="6dadd-1500">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1500">4</span></span>

<span data-ttu-id="6dadd-1501">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1501">5</span></span>

<span data-ttu-id="6dadd-1502">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1502">6</span></span>

<span data-ttu-id="6dadd-1503">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1503">7</span></span>

<span data-ttu-id="6dadd-1504">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1504">8</span></span>

<span data-ttu-id="6dadd-1505">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1505">9</span></span>

<span data-ttu-id="6dadd-1506">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1506">3</span></span><br/> <span data-ttu-id="6dadd-1507">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1507">0</span></span><br/>

<span data-ttu-id="6dadd-1508">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1508">1</span></span>

<span data-ttu-id="6dadd-1509">Restrição</span><span class="sxs-lookup"><span data-stu-id="6dadd-1509">Restriction</span></span>

<span data-ttu-id="6dadd-1510">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1510">...</span></span>

<span data-ttu-id="6dadd-1511">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1511">...</span></span>

<span data-ttu-id="6dadd-1512">cKey</span><span class="sxs-lookup"><span data-stu-id="6dadd-1512">cKey</span></span>

<span data-ttu-id="6dadd-1513">\_keyarray (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1513">\_keyArray (variable)</span></span>

<span data-ttu-id="6dadd-1514">\_ISRANGE</span><span class="sxs-lookup"><span data-stu-id="6dadd-1514">\_isRange</span></span>



 

<span data-ttu-id="6dadd-1515">**Restrição**: uma estrutura COccRestriction que especifica o local da palavra.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1515">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="6dadd-1516">**cKey**: um inteiro sem sinal de 32 bits especificando o número de elementos na \_ matriz keyarray.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1516">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="6dadd-1517">**\_ keyarray**: uma matriz de estruturas CKey que especificam uma palavra e seus sinônimos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1517">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="6dadd-1518">**\_ ISRANGE**: se definido como 0x01, as chaves são prefixos para correspondência.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1518">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="6dadd-1519">Se definido como 0x00, as chaves são valores exatos para corresponder.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1519">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="6dadd-1520">\_ISRANGE não deve ser definido para nenhum outro valor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1520">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="6dadd-1521">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1521">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="6dadd-1522">A estrutura CVectorRestriction contém uma operação ponderada ou em um nó de árvore de comandos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1522">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="6dadd-1523">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1523">0</span></span>

<span data-ttu-id="6dadd-1524">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1524">1</span></span>

<span data-ttu-id="6dadd-1525">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1525">2</span></span>

<span data-ttu-id="6dadd-1526">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1526">3</span></span>

<span data-ttu-id="6dadd-1527">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1527">4</span></span>

<span data-ttu-id="6dadd-1528">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1528">5</span></span>

<span data-ttu-id="6dadd-1529">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1529">6</span></span>

<span data-ttu-id="6dadd-1530">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1530">7</span></span>

<span data-ttu-id="6dadd-1531">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1531">8</span></span>

<span data-ttu-id="6dadd-1532">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1532">9</span></span>

<span data-ttu-id="6dadd-1533">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1533">1</span></span><br/> <span data-ttu-id="6dadd-1534">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1534">0</span></span><br/>

<span data-ttu-id="6dadd-1535">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1535">1</span></span>

<span data-ttu-id="6dadd-1536">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1536">2</span></span>

<span data-ttu-id="6dadd-1537">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1537">3</span></span>

<span data-ttu-id="6dadd-1538">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1538">4</span></span>

<span data-ttu-id="6dadd-1539">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1539">5</span></span>

<span data-ttu-id="6dadd-1540">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1540">6</span></span>

<span data-ttu-id="6dadd-1541">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1541">7</span></span>

<span data-ttu-id="6dadd-1542">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1542">8</span></span>

<span data-ttu-id="6dadd-1543">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1543">9</span></span>

<span data-ttu-id="6dadd-1544">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1544">2</span></span><br/> <span data-ttu-id="6dadd-1545">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1545">0</span></span><br/>

<span data-ttu-id="6dadd-1546">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1546">1</span></span>

<span data-ttu-id="6dadd-1547">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1547">2</span></span>

<span data-ttu-id="6dadd-1548">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1548">3</span></span>

<span data-ttu-id="6dadd-1549">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1549">4</span></span>

<span data-ttu-id="6dadd-1550">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1550">5</span></span>

<span data-ttu-id="6dadd-1551">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1551">6</span></span>

<span data-ttu-id="6dadd-1552">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1552">7</span></span>

<span data-ttu-id="6dadd-1553">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1553">8</span></span>

<span data-ttu-id="6dadd-1554">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1554">9</span></span>

<span data-ttu-id="6dadd-1555">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1555">3</span></span><br/> <span data-ttu-id="6dadd-1556">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1556">0</span></span><br/>

<span data-ttu-id="6dadd-1557">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1557">1</span></span>

<span data-ttu-id="6dadd-1558">\_Pres (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1558">\_pres (variable)</span></span>

<span data-ttu-id="6dadd-1559">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1559">...</span></span>

<span data-ttu-id="6dadd-1560">\_preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1560">\_padding (variable)</span></span>

<span data-ttu-id="6dadd-1561">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="6dadd-1561">\_ulRankMethod</span></span>



 

<span data-ttu-id="6dadd-1562">**\_ Pres**: uma árvore de comandos CNodeRestriction na qual uma classificação ou operação deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1562">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="6dadd-1563">**\_ preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1563">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="6dadd-1564">O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1564">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="6dadd-1565">Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1565">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="6dadd-1566">O conteúdo deste campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1566">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-1567">**\_ ulRankMethod**: um inteiro sem sinal de 32 bits especificando um algoritmo de classificação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1567">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="6dadd-1568">DEVE ser definido como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1568">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="6dadd-1569">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1569">Value</span></span>                            | <span data-ttu-id="6dadd-1570">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1570">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="6dadd-1571">Classificação de vetor \_ \_ mín. 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-1571">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="6dadd-1572">Usar Salt de algoritmo mínimo \[ \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1572">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="6dadd-1573">Classificação de vetor \_ \_ máx. 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-1573">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="6dadd-1574">Use o Salt máximo do algoritmo \[ \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1574">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="6dadd-1575">\_0x00000002 interno de classificação de vetor \_</span><span class="sxs-lookup"><span data-stu-id="6dadd-1575">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="6dadd-1576">Usar a saltização do algoritmo de produto interno \[ \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1576">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="6dadd-1577">\_0x00000003 de classificação de vetor \_</span><span class="sxs-lookup"><span data-stu-id="6dadd-1577">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="6dadd-1578">Use a saltização do algoritmo de coeficiente de um \[ \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1578">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="6dadd-1579">Classificação de vetor \_ \_ Jaccard 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-1579">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="6dadd-1580">Use a saltização do algoritmo de coeficiente Jaccard \[ \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1580">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="6dadd-1581">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1581">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="6dadd-1582">A estrutura CWordRestriction contém uma palavra para uma frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1582">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="6dadd-1583">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1583">0</span></span>

<span data-ttu-id="6dadd-1584">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1584">1</span></span>

<span data-ttu-id="6dadd-1585">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1585">2</span></span>

<span data-ttu-id="6dadd-1586">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1586">3</span></span>

<span data-ttu-id="6dadd-1587">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1587">4</span></span>

<span data-ttu-id="6dadd-1588">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1588">5</span></span>

<span data-ttu-id="6dadd-1589">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1589">6</span></span>

<span data-ttu-id="6dadd-1590">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1590">7</span></span>

<span data-ttu-id="6dadd-1591">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1591">8</span></span>

<span data-ttu-id="6dadd-1592">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1592">9</span></span>

<span data-ttu-id="6dadd-1593">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1593">1</span></span><br/> <span data-ttu-id="6dadd-1594">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1594">0</span></span><br/>

<span data-ttu-id="6dadd-1595">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1595">1</span></span>

<span data-ttu-id="6dadd-1596">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1596">2</span></span>

<span data-ttu-id="6dadd-1597">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1597">3</span></span>

<span data-ttu-id="6dadd-1598">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1598">4</span></span>

<span data-ttu-id="6dadd-1599">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1599">5</span></span>

<span data-ttu-id="6dadd-1600">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1600">6</span></span>

<span data-ttu-id="6dadd-1601">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1601">7</span></span>

<span data-ttu-id="6dadd-1602">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1602">8</span></span>

<span data-ttu-id="6dadd-1603">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1603">9</span></span>

<span data-ttu-id="6dadd-1604">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1604">2</span></span><br/> <span data-ttu-id="6dadd-1605">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1605">0</span></span><br/>

<span data-ttu-id="6dadd-1606">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1606">1</span></span>

<span data-ttu-id="6dadd-1607">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1607">2</span></span>

<span data-ttu-id="6dadd-1608">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1608">3</span></span>

<span data-ttu-id="6dadd-1609">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1609">4</span></span>

<span data-ttu-id="6dadd-1610">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1610">5</span></span>

<span data-ttu-id="6dadd-1611">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1611">6</span></span>

<span data-ttu-id="6dadd-1612">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1612">7</span></span>

<span data-ttu-id="6dadd-1613">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1613">8</span></span>

<span data-ttu-id="6dadd-1614">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1614">9</span></span>

<span data-ttu-id="6dadd-1615">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1615">3</span></span><br/> <span data-ttu-id="6dadd-1616">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1616">0</span></span><br/>

<span data-ttu-id="6dadd-1617">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1617">1</span></span>

<span data-ttu-id="6dadd-1618">restriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1618">restriction</span></span>

<span data-ttu-id="6dadd-1619">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1619">...</span></span>

<span data-ttu-id="6dadd-1620">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1620">...</span></span>

<span data-ttu-id="6dadd-1621">\_key (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1621">\_key (variable)</span></span>

<span data-ttu-id="6dadd-1622">\_isRange</span><span class="sxs-lookup"><span data-stu-id="6dadd-1622">\_isRange</span></span>



 

<span data-ttu-id="6dadd-1623">**restriction:** uma estrutura COccRestriction que especifica o local da palavra.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1623">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="6dadd-1624">**\_ key:** uma estrutura CKey especificando uma palavra.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1624">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="6dadd-1625">**\_ isRange:** se definido como 0x01, a chave será um prefixo para corresponder.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1625">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="6dadd-1626">Se definido como 0x00, a chave será um valor exato para corresponder.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1626">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="6dadd-1627">\_isRange NÃO DEVE ser definido como nenhum outro valor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1627">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="6dadd-1628">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="6dadd-1628">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="6dadd-1629">A estrutura CRestriction contém um nó de uma árvore de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1629">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="6dadd-1630">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1630">0</span></span>

<span data-ttu-id="6dadd-1631">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1631">1</span></span>

<span data-ttu-id="6dadd-1632">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1632">2</span></span>

<span data-ttu-id="6dadd-1633">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1633">3</span></span>

<span data-ttu-id="6dadd-1634">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1634">4</span></span>

<span data-ttu-id="6dadd-1635">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1635">5</span></span>

<span data-ttu-id="6dadd-1636">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1636">6</span></span>

<span data-ttu-id="6dadd-1637">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1637">7</span></span>

<span data-ttu-id="6dadd-1638">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1638">8</span></span>

<span data-ttu-id="6dadd-1639">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1639">9</span></span>

<span data-ttu-id="6dadd-1640">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1640">1</span></span><br/> <span data-ttu-id="6dadd-1641">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1641">0</span></span><br/>

<span data-ttu-id="6dadd-1642">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1642">1</span></span>

<span data-ttu-id="6dadd-1643">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1643">2</span></span>

<span data-ttu-id="6dadd-1644">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1644">3</span></span>

<span data-ttu-id="6dadd-1645">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1645">4</span></span>

<span data-ttu-id="6dadd-1646">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1646">5</span></span>

<span data-ttu-id="6dadd-1647">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1647">6</span></span>

<span data-ttu-id="6dadd-1648">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1648">7</span></span>

<span data-ttu-id="6dadd-1649">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1649">8</span></span>

<span data-ttu-id="6dadd-1650">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1650">9</span></span>

<span data-ttu-id="6dadd-1651">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1651">2</span></span><br/> <span data-ttu-id="6dadd-1652">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1652">0</span></span><br/>

<span data-ttu-id="6dadd-1653">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1653">1</span></span>

<span data-ttu-id="6dadd-1654">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1654">2</span></span>

<span data-ttu-id="6dadd-1655">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1655">3</span></span>

<span data-ttu-id="6dadd-1656">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1656">4</span></span>

<span data-ttu-id="6dadd-1657">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1657">5</span></span>

<span data-ttu-id="6dadd-1658">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1658">6</span></span>

<span data-ttu-id="6dadd-1659">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1659">7</span></span>

<span data-ttu-id="6dadd-1660">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1660">8</span></span>

<span data-ttu-id="6dadd-1661">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1661">9</span></span>

<span data-ttu-id="6dadd-1662">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1662">3</span></span><br/> <span data-ttu-id="6dadd-1663">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1663">0</span></span><br/>

<span data-ttu-id="6dadd-1664">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1664">1</span></span>

<span data-ttu-id="6dadd-1665">\_ulType</span><span class="sxs-lookup"><span data-stu-id="6dadd-1665">\_ulType</span></span>

<span data-ttu-id="6dadd-1666">Peso</span><span class="sxs-lookup"><span data-stu-id="6dadd-1666">Weight</span></span>

<span data-ttu-id="6dadd-1667">Restrição</span><span class="sxs-lookup"><span data-stu-id="6dadd-1667">Restriction</span></span>



 

<span data-ttu-id="6dadd-1668">**\_ ulType:** um inteiro sem sinal de 32 bits que indica o tipo de restrição usado para o nó da árvore de comandos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1668">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="6dadd-1669">DEVE ser definido como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1669">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="6dadd-1670">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1670">Value</span></span>                    | <span data-ttu-id="6dadd-1671">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1671">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-1672">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-1672">RTNone 0x00000000</span></span>        | <span data-ttu-id="6dadd-1673">O nó representa uma palavra de ruído em uma consulta de vetor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1673">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="6dadd-1674">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-1674">RTAnd 0x00000001</span></span>         | <span data-ttu-id="6dadd-1675">O nó contém uma CNodeRestriction na qual uma operação AND lógica a ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1675">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="6dadd-1676">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-1676">RTOr 0x00000002</span></span>          | <span data-ttu-id="6dadd-1677">O nó contém uma CNodeRestriction na qual uma operação OR lógica deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1677">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="6dadd-1678">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-1678">RTNot 0x00000003</span></span>         | <span data-ttu-id="6dadd-1679">O nó contém uma CRestriction na qual uma operação NOT deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1679">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="6dadd-1680">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-1680">RTContent 0x00000004</span></span>     | <span data-ttu-id="6dadd-1681">O nó contém um CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1681">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="6dadd-1682">RTProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="6dadd-1682">RTProperty 0x00000005</span></span>    | <span data-ttu-id="6dadd-1683">O nó contém uma CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1683">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="6dadd-1684">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="6dadd-1684">RTProximity 0x00000006</span></span>   | <span data-ttu-id="6dadd-1685">O nó contém uma CNodeRestriction na qual uma classificação de proximidade deve ser executada,</span><span class="sxs-lookup"><span data-stu-id="6dadd-1685">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="6dadd-1686">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="6dadd-1686">RTVector 0x00000007</span></span>      | <span data-ttu-id="6dadd-1687">O nó contém um CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1687">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="6dadd-1688">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="6dadd-1688">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="6dadd-1689">O nó contém uma CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1689">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="6dadd-1690">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="6dadd-1690">RTScope 0x00000009</span></span>       | <span data-ttu-id="6dadd-1691">O nó contém um CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1691">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="6dadd-1692">PrAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="6dadd-1692">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="6dadd-1693">O nó contém um CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1693">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="6dadd-1694">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="6dadd-1694">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="6dadd-1695">O nó contém um CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1695">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="6dadd-1696">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="6dadd-1696">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="6dadd-1697">O nó contém uma CNodeRestriction na qual uma combinação de frases deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1697">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="6dadd-1698">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="6dadd-1698">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="6dadd-1699">O nó contém uma CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1699">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="6dadd-1700">RTWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="6dadd-1700">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="6dadd-1701">O nó contém uma CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1701">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="6dadd-1702">**Peso:** um inteiro sem sinal de 32 bits que representa o peso do nó.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1702">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="6dadd-1703">Peso indica a importância do nó em relação a outros nós na árvore de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1703">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="6dadd-1704">Valores de peso mais altos são mais importantes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1704">Higher weight values are more important.</span></span>

<span data-ttu-id="6dadd-1705">**Restrição:** o tipo de restrição para o nó da árvore de comandos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1705">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="6dadd-1706">A sintaxe DEVE ser conforme indicado pelo \_ campo ulType.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1706">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="6dadd-1707">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-1707">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="6dadd-1708">A estrutura CColumnSet especifica os números de coluna a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1708">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="6dadd-1709">Essa estrutura é sempre usada em referência a uma estrutura CPidMapper específica (seção 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="6dadd-1709">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="6dadd-1710">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1710">0</span></span>

<span data-ttu-id="6dadd-1711">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1711">1</span></span>

<span data-ttu-id="6dadd-1712">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1712">2</span></span>

<span data-ttu-id="6dadd-1713">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1713">3</span></span>

<span data-ttu-id="6dadd-1714">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1714">4</span></span>

<span data-ttu-id="6dadd-1715">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1715">5</span></span>

<span data-ttu-id="6dadd-1716">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1716">6</span></span>

<span data-ttu-id="6dadd-1717">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1717">7</span></span>

<span data-ttu-id="6dadd-1718">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1718">8</span></span>

<span data-ttu-id="6dadd-1719">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1719">9</span></span>

<span data-ttu-id="6dadd-1720">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1720">1</span></span><br/> <span data-ttu-id="6dadd-1721">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1721">0</span></span><br/>

<span data-ttu-id="6dadd-1722">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1722">1</span></span>

<span data-ttu-id="6dadd-1723">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1723">2</span></span>

<span data-ttu-id="6dadd-1724">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1724">3</span></span>

<span data-ttu-id="6dadd-1725">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1725">4</span></span>

<span data-ttu-id="6dadd-1726">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1726">5</span></span>

<span data-ttu-id="6dadd-1727">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1727">6</span></span>

<span data-ttu-id="6dadd-1728">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1728">7</span></span>

<span data-ttu-id="6dadd-1729">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1729">8</span></span>

<span data-ttu-id="6dadd-1730">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1730">9</span></span>

<span data-ttu-id="6dadd-1731">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1731">2</span></span><br/> <span data-ttu-id="6dadd-1732">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1732">0</span></span><br/>

<span data-ttu-id="6dadd-1733">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1733">1</span></span>

<span data-ttu-id="6dadd-1734">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1734">2</span></span>

<span data-ttu-id="6dadd-1735">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1735">3</span></span>

<span data-ttu-id="6dadd-1736">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1736">4</span></span>

<span data-ttu-id="6dadd-1737">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1737">5</span></span>

<span data-ttu-id="6dadd-1738">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1738">6</span></span>

<span data-ttu-id="6dadd-1739">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1739">7</span></span>

<span data-ttu-id="6dadd-1740">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1740">8</span></span>

<span data-ttu-id="6dadd-1741">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1741">9</span></span>

<span data-ttu-id="6dadd-1742">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1742">3</span></span><br/> <span data-ttu-id="6dadd-1743">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1743">0</span></span><br/>

<span data-ttu-id="6dadd-1744">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1744">1</span></span>

<span data-ttu-id="6dadd-1745">count</span><span class="sxs-lookup"><span data-stu-id="6dadd-1745">count</span></span>

<span data-ttu-id="6dadd-1746">índices (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1746">indexes (variable)</span></span>



 

<span data-ttu-id="6dadd-1747">**Count**: um inteiro de 32 bits sem sinal especificando o número de elementos na matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1747">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="6dadd-1748">**índices**: matriz de inteiros sem sinal de 4 bytes que representam índices baseados em zero na matriz aPropSpec na estrutura CPidMapper correspondente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1748">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="6dadd-1749">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-1749">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="6dadd-1750">A estrutura CCategorizationSet contém informações sobre o agrupamento de um conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1750">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="6dadd-1751">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1751">0</span></span>

<span data-ttu-id="6dadd-1752">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1752">1</span></span>

<span data-ttu-id="6dadd-1753">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1753">2</span></span>

<span data-ttu-id="6dadd-1754">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1754">3</span></span>

<span data-ttu-id="6dadd-1755">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1755">4</span></span>

<span data-ttu-id="6dadd-1756">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1756">5</span></span>

<span data-ttu-id="6dadd-1757">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1757">6</span></span>

<span data-ttu-id="6dadd-1758">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1758">7</span></span>

<span data-ttu-id="6dadd-1759">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1759">8</span></span>

<span data-ttu-id="6dadd-1760">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1760">9</span></span>

<span data-ttu-id="6dadd-1761">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1761">1</span></span><br/> <span data-ttu-id="6dadd-1762">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1762">0</span></span><br/>

<span data-ttu-id="6dadd-1763">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1763">1</span></span>

<span data-ttu-id="6dadd-1764">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1764">2</span></span>

<span data-ttu-id="6dadd-1765">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1765">3</span></span>

<span data-ttu-id="6dadd-1766">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1766">4</span></span>

<span data-ttu-id="6dadd-1767">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1767">5</span></span>

<span data-ttu-id="6dadd-1768">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1768">6</span></span>

<span data-ttu-id="6dadd-1769">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1769">7</span></span>

<span data-ttu-id="6dadd-1770">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1770">8</span></span>

<span data-ttu-id="6dadd-1771">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1771">9</span></span>

<span data-ttu-id="6dadd-1772">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1772">2</span></span><br/> <span data-ttu-id="6dadd-1773">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1773">0</span></span><br/>

<span data-ttu-id="6dadd-1774">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1774">1</span></span>

<span data-ttu-id="6dadd-1775">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1775">2</span></span>

<span data-ttu-id="6dadd-1776">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1776">3</span></span>

<span data-ttu-id="6dadd-1777">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1777">4</span></span>

<span data-ttu-id="6dadd-1778">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1778">5</span></span>

<span data-ttu-id="6dadd-1779">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1779">6</span></span>

<span data-ttu-id="6dadd-1780">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1780">7</span></span>

<span data-ttu-id="6dadd-1781">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1781">8</span></span>

<span data-ttu-id="6dadd-1782">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1782">9</span></span>

<span data-ttu-id="6dadd-1783">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1783">3</span></span><br/> <span data-ttu-id="6dadd-1784">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1784">0</span></span><br/>

<span data-ttu-id="6dadd-1785">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1785">1</span></span>

<span data-ttu-id="6dadd-1786">count</span><span class="sxs-lookup"><span data-stu-id="6dadd-1786">count</span></span>

<span data-ttu-id="6dadd-1787">Categorias (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1787">categories (variable)</span></span>



 

<span data-ttu-id="6dadd-1788">**Count**: um inteiro sem sinal de 32 bits contendo o número de elementos na matriz Categories.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1788">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="6dadd-1789">**categorias**: matriz de estruturas CCategorizationSpec especificando o agrupamento da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1789">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="6dadd-1790">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="6dadd-1790">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="6dadd-1791">A estrutura CCategorizationSpec contém um agrupamento para um conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1791">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="6dadd-1792">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1792">0</span></span>

<span data-ttu-id="6dadd-1793">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1793">1</span></span>

<span data-ttu-id="6dadd-1794">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1794">2</span></span>

<span data-ttu-id="6dadd-1795">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1795">3</span></span>

<span data-ttu-id="6dadd-1796">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1796">4</span></span>

<span data-ttu-id="6dadd-1797">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1797">5</span></span>

<span data-ttu-id="6dadd-1798">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1798">6</span></span>

<span data-ttu-id="6dadd-1799">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1799">7</span></span>

<span data-ttu-id="6dadd-1800">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1800">8</span></span>

<span data-ttu-id="6dadd-1801">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1801">9</span></span>

<span data-ttu-id="6dadd-1802">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1802">1</span></span><br/> <span data-ttu-id="6dadd-1803">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1803">0</span></span><br/>

<span data-ttu-id="6dadd-1804">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1804">1</span></span>

<span data-ttu-id="6dadd-1805">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1805">2</span></span>

<span data-ttu-id="6dadd-1806">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1806">3</span></span>

<span data-ttu-id="6dadd-1807">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1807">4</span></span>

<span data-ttu-id="6dadd-1808">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1808">5</span></span>

<span data-ttu-id="6dadd-1809">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1809">6</span></span>

<span data-ttu-id="6dadd-1810">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1810">7</span></span>

<span data-ttu-id="6dadd-1811">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1811">8</span></span>

<span data-ttu-id="6dadd-1812">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1812">9</span></span>

<span data-ttu-id="6dadd-1813">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1813">2</span></span><br/> <span data-ttu-id="6dadd-1814">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1814">0</span></span><br/>

<span data-ttu-id="6dadd-1815">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1815">1</span></span>

<span data-ttu-id="6dadd-1816">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1816">2</span></span>

<span data-ttu-id="6dadd-1817">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1817">3</span></span>

<span data-ttu-id="6dadd-1818">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1818">4</span></span>

<span data-ttu-id="6dadd-1819">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1819">5</span></span>

<span data-ttu-id="6dadd-1820">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1820">6</span></span>

<span data-ttu-id="6dadd-1821">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1821">7</span></span>

<span data-ttu-id="6dadd-1822">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1822">8</span></span>

<span data-ttu-id="6dadd-1823">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1823">9</span></span>

<span data-ttu-id="6dadd-1824">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1824">3</span></span><br/> <span data-ttu-id="6dadd-1825">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1825">0</span></span><br/>

<span data-ttu-id="6dadd-1826">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1826">1</span></span>

<span data-ttu-id="6dadd-1827">\_csColumns (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1827">\_csColumns (variable)</span></span>

<span data-ttu-id="6dadd-1828">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="6dadd-1828">\_ulCategType</span></span>



 

<span data-ttu-id="6dadd-1829">**\_ csColumns:** uma estrutura CColumnSet que indica as colunas pelas quais agrupar a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1829">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="6dadd-1830">**\_ ulCategType:** um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1830">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="6dadd-1831">DEVE ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1831">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="6dadd-1832">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="6dadd-1832">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="6dadd-1833">A estrutura CDbColId contém uma coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1833">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="6dadd-1834">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1834">0</span></span>

<span data-ttu-id="6dadd-1835">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1835">1</span></span>

<span data-ttu-id="6dadd-1836">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1836">2</span></span>

<span data-ttu-id="6dadd-1837">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1837">3</span></span>

<span data-ttu-id="6dadd-1838">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1838">4</span></span>

<span data-ttu-id="6dadd-1839">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1839">5</span></span>

<span data-ttu-id="6dadd-1840">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1840">6</span></span>

<span data-ttu-id="6dadd-1841">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1841">7</span></span>

<span data-ttu-id="6dadd-1842">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1842">8</span></span>

<span data-ttu-id="6dadd-1843">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1843">9</span></span>

<span data-ttu-id="6dadd-1844">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1844">1</span></span><br/> <span data-ttu-id="6dadd-1845">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1845">0</span></span><br/>

<span data-ttu-id="6dadd-1846">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1846">1</span></span>

<span data-ttu-id="6dadd-1847">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1847">2</span></span>

<span data-ttu-id="6dadd-1848">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1848">3</span></span>

<span data-ttu-id="6dadd-1849">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1849">4</span></span>

<span data-ttu-id="6dadd-1850">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1850">5</span></span>

<span data-ttu-id="6dadd-1851">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1851">6</span></span>

<span data-ttu-id="6dadd-1852">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1852">7</span></span>

<span data-ttu-id="6dadd-1853">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1853">8</span></span>

<span data-ttu-id="6dadd-1854">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1854">9</span></span>

<span data-ttu-id="6dadd-1855">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1855">2</span></span><br/> <span data-ttu-id="6dadd-1856">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1856">0</span></span><br/>

<span data-ttu-id="6dadd-1857">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1857">1</span></span>

<span data-ttu-id="6dadd-1858">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1858">2</span></span>

<span data-ttu-id="6dadd-1859">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1859">3</span></span>

<span data-ttu-id="6dadd-1860">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1860">4</span></span>

<span data-ttu-id="6dadd-1861">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1861">5</span></span>

<span data-ttu-id="6dadd-1862">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1862">6</span></span>

<span data-ttu-id="6dadd-1863">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1863">7</span></span>

<span data-ttu-id="6dadd-1864">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1864">8</span></span>

<span data-ttu-id="6dadd-1865">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1865">9</span></span>

<span data-ttu-id="6dadd-1866">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1866">3</span></span><br/> <span data-ttu-id="6dadd-1867">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1867">0</span></span><br/>

<span data-ttu-id="6dadd-1868">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1868">1</span></span>

<span data-ttu-id="6dadd-1869">eKind</span><span class="sxs-lookup"><span data-stu-id="6dadd-1869">eKind</span></span>

<span data-ttu-id="6dadd-1870">GUID</span><span class="sxs-lookup"><span data-stu-id="6dadd-1870">GUID</span></span>

<span data-ttu-id="6dadd-1871">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1871">...</span></span>

<span data-ttu-id="6dadd-1872">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1872">...</span></span>

<span data-ttu-id="6dadd-1873">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-1873">...</span></span>

<span data-ttu-id="6dadd-1874">ulId</span><span class="sxs-lookup"><span data-stu-id="6dadd-1874">ulId</span></span>

<span data-ttu-id="6dadd-1875">vString (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1875">vString (variable)</span></span>



 

<span data-ttu-id="6dadd-1876">**eKind**: DEVE ser definido como um dos valores abaixo que indica o conteúdo de GUID e vValue.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1876">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="6dadd-1877">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1877">Value</span></span>                            | <span data-ttu-id="6dadd-1878">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1878">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-1879">NOME DO GUID DBKIND \_ \_ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-1879">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="6dadd-1880">vString contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1880">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="6dadd-1881">DBKIND \_ GUID \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-1881">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="6dadd-1882">ulId contém um inteiro de 4 byte que indica a ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1882">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="6dadd-1883">DBKIND \_ PGUID \_ NAME 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-1883">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="6dadd-1884">vString contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1884">vString contains a property name.</span></span> <span data-ttu-id="6dadd-1885">Esse valor DEVE ser tratado da mesma forma que DBKIND \_ GUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1885">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="6dadd-1886">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-1886">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="6dadd-1887">ulId contém um inteiro de 4 byte que indica a ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1887">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="6dadd-1888">Esse valor DEVE ser o mesmo que DBKIND \_ GUID \_ PROPID.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1888">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="6dadd-1889">**GUID:** o GUID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1889">**GUID**: The property GUID.</span></span>

<span data-ttu-id="6dadd-1890">**ulId**: se eKind for DBKIND GUID PROPID ou DBKIND PGUID PROPID, esse campo conterá um inteiro sem \_ \_ \_ \_ sinal, especificando a ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1890">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="6dadd-1891">Se eKind for DBKIND GUID NAME ou DBKIND PGUID NAME, esse campo conterá um inteiro sem sinal especificando o número de caracteres Unicode contidos no campo \_ \_ \_ \_ vString.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1891">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="6dadd-1892">**vString:** uma cadeia de caracteres Unicode não terminada em nulo que representa o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1892">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="6dadd-1893">Ele DEVE ser omitido, a menos que o campo eKind esteja definido como DBKIND \_ GUID \_ NAME ou DBKIND \_ PGUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1893">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="6dadd-1894">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="6dadd-1894">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="6dadd-1895">A estrutura CDbProp contém uma propriedade .</span><span class="sxs-lookup"><span data-stu-id="6dadd-1895">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="6dadd-1896">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1896">0</span></span>

<span data-ttu-id="6dadd-1897">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1897">1</span></span>

<span data-ttu-id="6dadd-1898">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1898">2</span></span>

<span data-ttu-id="6dadd-1899">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1899">3</span></span>

<span data-ttu-id="6dadd-1900">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1900">4</span></span>

<span data-ttu-id="6dadd-1901">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1901">5</span></span>

<span data-ttu-id="6dadd-1902">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1902">6</span></span>

<span data-ttu-id="6dadd-1903">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1903">7</span></span>

<span data-ttu-id="6dadd-1904">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1904">8</span></span>

<span data-ttu-id="6dadd-1905">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1905">9</span></span>

<span data-ttu-id="6dadd-1906">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1906">1</span></span><br/> <span data-ttu-id="6dadd-1907">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1907">0</span></span><br/>

<span data-ttu-id="6dadd-1908">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1908">1</span></span>

<span data-ttu-id="6dadd-1909">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1909">2</span></span>

<span data-ttu-id="6dadd-1910">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1910">3</span></span>

<span data-ttu-id="6dadd-1911">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1911">4</span></span>

<span data-ttu-id="6dadd-1912">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1912">5</span></span>

<span data-ttu-id="6dadd-1913">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1913">6</span></span>

<span data-ttu-id="6dadd-1914">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1914">7</span></span>

<span data-ttu-id="6dadd-1915">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1915">8</span></span>

<span data-ttu-id="6dadd-1916">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1916">9</span></span>

<span data-ttu-id="6dadd-1917">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1917">2</span></span><br/> <span data-ttu-id="6dadd-1918">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1918">0</span></span><br/>

<span data-ttu-id="6dadd-1919">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1919">1</span></span>

<span data-ttu-id="6dadd-1920">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-1920">2</span></span>

<span data-ttu-id="6dadd-1921">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1921">3</span></span>

<span data-ttu-id="6dadd-1922">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-1922">4</span></span>

<span data-ttu-id="6dadd-1923">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-1923">5</span></span>

<span data-ttu-id="6dadd-1924">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-1924">6</span></span>

<span data-ttu-id="6dadd-1925">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-1925">7</span></span>

<span data-ttu-id="6dadd-1926">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-1926">8</span></span>

<span data-ttu-id="6dadd-1927">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-1927">9</span></span>

<span data-ttu-id="6dadd-1928">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-1928">3</span></span><br/> <span data-ttu-id="6dadd-1929">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-1929">0</span></span><br/>

<span data-ttu-id="6dadd-1930">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-1930">1</span></span>

<span data-ttu-id="6dadd-1931">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="6dadd-1931">DBPROPID</span></span>

<span data-ttu-id="6dadd-1932">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="6dadd-1932">DBPROPOPTIONS</span></span>

<span data-ttu-id="6dadd-1933">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="6dadd-1933">DBPROPSTATUS</span></span>

<span data-ttu-id="6dadd-1934">colid (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1934">colid (variable)</span></span>

<span data-ttu-id="6dadd-1935">vValue (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-1935">vValue (variable)</span></span>



 

<span data-ttu-id="6dadd-1936">**DBPROPID:** um inteiro sem sinal de 32 bits, indicando a ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1936">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="6dadd-1937">**DBPROPOPTIONS:** deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1937">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="6dadd-1938">**DBPROPSTATUS:** deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1938">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="6dadd-1939">**colid**: uma estrutura CDbColId, conforme especificado na seção 2.2.1.20, indicando a coluna à qual a propriedade se aplica.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1939">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="6dadd-1940">**vValue:** um CBaseStorageVariant que contém o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1940">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="6dadd-1941">2.2.1.21.1 Propriedades</span><span class="sxs-lookup"><span data-stu-id="6dadd-1941">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="6dadd-1942">Esta seção detalha as propriedades usadas pelo CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1942">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="6dadd-1943">Essas propriedades são agrupadas em três conjuntos de propriedades, ident2.2.1.21.1, no campo guidPropertySet da estrutura CDbPropSet (Seção 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="6dadd-1943">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="6dadd-1944">A tabela a seguir lista as propriedades que fazem parte do conjunto de propriedades DBPROPSET \_ FSCIFRMWRK \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1944">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="6dadd-1945">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1945">Value</span></span>                                  | <span data-ttu-id="6dadd-1946">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1946">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-1947">NOME DO \_ CATÁLOGO DBPROP CI \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-1947">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="6dadd-1948">Especifica o nome do catálogo ou catálogos a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1948">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="6dadd-1949">O valor DEVE ser um VT \_ LPWSTR ou um \_ VT VECTOR \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="6dadd-1949">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="6dadd-1950">DBPROP \_ CI \_ INCLUDE \_ SCOPES 0X00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-1950">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="6dadd-1951">Especifica um ou mais caminhos a serem incluídos na consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1951">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="6dadd-1952">O valor DEVE ser um VT \_ LPWSTR ou um \_ VT VECTOR \| VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="6dadd-1953">SINALIZADORES DE \_ ESCOPO DE CI \_ \_ DBPROP 0X00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-1953">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="6dadd-1954">Especifica como os caminhos especificados pela propriedade DBPROP \_ CI \_ INCLUDE \_ SCOPES devem ser tratados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1954">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="6dadd-1955">O valor DEVE ser uma VT \_ I4 ou uma \_ VT VECTOR \| VT \_ I4.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1955">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="6dadd-1956">TIPO DE \_ CONSULTA DBPROP CI \_ \_ 0X00000007</span><span class="sxs-lookup"><span data-stu-id="6dadd-1956">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="6dadd-1957">Especifica o tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1957">Specifies the type of query.</span></span> <span data-ttu-id="6dadd-1958">O CDbColId DEVE ser definido como DB \_ NULLID.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1958">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="6dadd-1959">A tabela a seguir lista os sinalizadores para a propriedade DBPROP \_ CI \_ SCOPE \_ FLAGS:</span><span class="sxs-lookup"><span data-stu-id="6dadd-1959">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="6dadd-1960">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1960">Value</span></span>                     | <span data-ttu-id="6dadd-1961">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1961">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-1962">CONSULTA PROFUNDA \_ 0X01</span><span class="sxs-lookup"><span data-stu-id="6dadd-1962">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="6dadd-1963">Se definido, indica que os arquivos no diretório de escopo e todos os subdireários estão incluídos nos resultados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1963">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="6dadd-1964">Se estiver claro, somente os arquivos no diretório de escopo serão incluídos nos resultados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1964">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="6dadd-1965">NÃO DEVE ser combinado com A CONSULTA \_ PROFUNDA.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1965">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="6dadd-1966">CONSULTA DE \_ CAMINHO VIRTUAL \_ 0X02</span><span class="sxs-lookup"><span data-stu-id="6dadd-1966">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="6dadd-1967">Se definido, indica que o escopo é um caminho virtual.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1967">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="6dadd-1968">Se estiver claro, indica que o escopo é um diretório físico.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1968">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="6dadd-1969">A tabela a seguir lista os tipos de consulta para a propriedade DBPROP \_ CI \_ QUERY \_ TYPE:</span><span class="sxs-lookup"><span data-stu-id="6dadd-1969">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="6dadd-1970">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1970">Value</span></span>                     | <span data-ttu-id="6dadd-1971">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1971">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-1972">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-1972">CiNormal 0x00000000</span></span>       | <span data-ttu-id="6dadd-1973">Uma consulta regular.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1973">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="6dadd-1974">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-1974">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="6dadd-1975">A consulta está solicitando uma lista das raízes virtuais do catálogo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1975">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="6dadd-1976">Esse valor requer privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1976">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="6dadd-1977">CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-1977">CiProperties 0x00000003</span></span>   | <span data-ttu-id="6dadd-1978">A consulta está solicitando uma lista de todas as propriedades com suporte pelo serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1978">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="6dadd-1979">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-1979">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="6dadd-1980">A consulta é uma operação administrativa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1980">The query is an administrative operation.</span></span> <span data-ttu-id="6dadd-1981">Esse valor requer privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1981">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="6dadd-1982">A tabela a seguir lista as propriedades que fazem parte do conjunto de propriedades DBPROPSET \_ QUERYEXT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1982">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="6dadd-1983">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-1983">Value</span></span>                                      | <span data-ttu-id="6dadd-1984">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-1984">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-1985">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-1985">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="6dadd-1986">Especifica como o serviço de indexação é para lidar com consultas lentas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1986">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="6dadd-1987">O valor DEVE ser um BOOL de \_ VT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1987">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="6dadd-1988">Se TRUE, o servidor poderá falhar nessas consultas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1988">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="6dadd-1989">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-1989">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="6dadd-1990">Indica se o serviço de indexação deve executar o corte de resultados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1990">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="6dadd-1991">Se TRUE, o servidor deve considerar a execução de corte de resultados de uma maneira que otimize o tempo de resposta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1991">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="6dadd-1992">O valor DEVE ser um BOOL de \_ VT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1992">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="6dadd-1993">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-1993">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="6dadd-1994">Indica se o cliente dá suporte a tipos de dados \_ VECTOR VT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1994">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="6dadd-1995">Se TRUE, o cliente dá suporte a VECTOR VT; se FALSE, o servidor deve converter tipos de dados VECTOR VT em tipos de \_ \_ dados VT \_ ARRAY.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1995">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="6dadd-1996">O valor DEVE ser um BOOL de \_ VT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1996">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="6dadd-1997">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="6dadd-1997">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="6dadd-1998">Indica as correspondeções de linha a retornar.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1998">Indicates the row matches to return.</span></span> <span data-ttu-id="6dadd-1999">Se TRUE, o servidor deve retornar o primeiro conjunto de linhas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-1999">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="6dadd-2000">Se FOR FALSE, as melhores linhas correspondentes deverão ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2000">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="6dadd-2001">O valor DEVE ser um BOOL de \_ VT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2001">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="6dadd-2002">A tabela a seguir lista as propriedades que fazem parte do conjunto de propriedades DBPROPSET \_ CIFRMWRKCORE \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2002">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="6dadd-2003">Value/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="6dadd-2003">Value / DBPROPID</span></span>                 | <span data-ttu-id="6dadd-2004">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-2004">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-2005">DBPROP \_ MACHINE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-2005">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="6dadd-2006">Especifica os nomes dos computadores nos quais uma consulta deve ser processada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2006">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="6dadd-2007">O valor DEVE ser VT \_ BSTR ou VT \_ ARRAY \| VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2007">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="6dadd-2008">DBPROP \_ CLIENT \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-2008">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="6dadd-2009">Especifica uma constante de conexão para o serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2009">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="6dadd-2010">O valor DEVE ser uma CLSID de VT \_ que contém 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2010">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="6dadd-2011">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-2011">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="6dadd-2012">A estrutura CDbPropSet contém um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2012">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="6dadd-2013">Observe que o primeiro campo é de tamanho fixo, mas pode não estar alinhado a um deslocamento que é um múltiplo de 4 byte desde o início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2013">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="6dadd-2014">No entanto, o campo cProperties é alinhado como tal e, portanto, o formato é representado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2014">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="6dadd-2015">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2015">0</span></span>

<span data-ttu-id="6dadd-2016">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2016">1</span></span>

<span data-ttu-id="6dadd-2017">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2017">2</span></span>

<span data-ttu-id="6dadd-2018">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2018">3</span></span>

<span data-ttu-id="6dadd-2019">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2019">4</span></span>

<span data-ttu-id="6dadd-2020">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2020">5</span></span>

<span data-ttu-id="6dadd-2021">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2021">6</span></span>

<span data-ttu-id="6dadd-2022">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2022">7</span></span>

<span data-ttu-id="6dadd-2023">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2023">8</span></span>

<span data-ttu-id="6dadd-2024">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2024">9</span></span>

<span data-ttu-id="6dadd-2025">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2025">1</span></span><br/> <span data-ttu-id="6dadd-2026">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2026">0</span></span><br/>

<span data-ttu-id="6dadd-2027">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2027">1</span></span>

<span data-ttu-id="6dadd-2028">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2028">2</span></span>

<span data-ttu-id="6dadd-2029">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2029">3</span></span>

<span data-ttu-id="6dadd-2030">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2030">4</span></span>

<span data-ttu-id="6dadd-2031">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2031">5</span></span>

<span data-ttu-id="6dadd-2032">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2032">6</span></span>

<span data-ttu-id="6dadd-2033">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2033">7</span></span>

<span data-ttu-id="6dadd-2034">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2034">8</span></span>

<span data-ttu-id="6dadd-2035">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2035">9</span></span>

<span data-ttu-id="6dadd-2036">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2036">2</span></span><br/> <span data-ttu-id="6dadd-2037">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2037">0</span></span><br/>

<span data-ttu-id="6dadd-2038">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2038">1</span></span>

<span data-ttu-id="6dadd-2039">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2039">2</span></span>

<span data-ttu-id="6dadd-2040">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2040">3</span></span>

<span data-ttu-id="6dadd-2041">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2041">4</span></span>

<span data-ttu-id="6dadd-2042">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2042">5</span></span>

<span data-ttu-id="6dadd-2043">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2043">6</span></span>

<span data-ttu-id="6dadd-2044">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2044">7</span></span>

<span data-ttu-id="6dadd-2045">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2045">8</span></span>

<span data-ttu-id="6dadd-2046">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2046">9</span></span>

<span data-ttu-id="6dadd-2047">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2047">3</span></span><br/> <span data-ttu-id="6dadd-2048">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2048">0</span></span><br/>

<span data-ttu-id="6dadd-2049">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2049">1</span></span>

<span data-ttu-id="6dadd-2050">Guidpropertyset</span><span class="sxs-lookup"><span data-stu-id="6dadd-2050">guidPropertySet</span></span>

<span data-ttu-id="6dadd-2051">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-2051">...</span></span>

<span data-ttu-id="6dadd-2052">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-2052">...</span></span>

<span data-ttu-id="6dadd-2053">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-2053">...</span></span>

<span data-ttu-id="6dadd-2054">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-2054">...</span></span>

<span data-ttu-id="6dadd-2055">\_preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2055">\_padding (variable)</span></span>

<span data-ttu-id="6dadd-2056">cProperties</span><span class="sxs-lookup"><span data-stu-id="6dadd-2056">cProperties</span></span>

<span data-ttu-id="6dadd-2057">aProps (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2057">aProps (variable)</span></span>



 

<span data-ttu-id="6dadd-2058">**guidPropertySet:** um GUID que identifica o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2058">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="6dadd-2059">DEVE ser definido como o formulário binário correspondente a um dos valores a seguir (mostrado no formulário de representação de cadeia de caracteres), identificando o conjunto de propriedades das propriedades contidas no campo aProps.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2059">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="6dadd-2060">Valor/GUID</span><span class="sxs-lookup"><span data-stu-id="6dadd-2060">Value / GUID</span></span>                                                                              | <span data-ttu-id="6dadd-2061">Nome</span><span class="sxs-lookup"><span data-stu-id="6dadd-2061">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="6dadd-2062">DBPROPSET \_ FSCIFRMWRK \_ EXT</span><span class="sxs-lookup"><span data-stu-id="6dadd-2062">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="6dadd-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="6dadd-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="6dadd-2064">Conjunto de propriedades da estrutura de índice de conteúdo do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="6dadd-2064">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="6dadd-2065">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="6dadd-2065">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="6dadd-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="6dadd-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="6dadd-2067">Conjunto de propriedades da extensão de consulta</span><span class="sxs-lookup"><span data-stu-id="6dadd-2067">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="6dadd-2068">DBPROPSET \_ CIFRMWRKCORE \_ EXT</span><span class="sxs-lookup"><span data-stu-id="6dadd-2068">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="6dadd-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="6dadd-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="6dadd-2070">Conjunto de propriedades do Content Index Framework Core</span><span class="sxs-lookup"><span data-stu-id="6dadd-2070">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="6dadd-2071">**\_ preenchimento:** esse campo DEVE ter de 0 a 3 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2071">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="6dadd-2072">O comprimento desse campo DEVE ser tal que o campo a seguir comece em um deslocamento que é um múltiplo de 4 bytes do início da mensagem que contém essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2072">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="6dadd-2073">Se esse campo estiver presente (ou seja, comprimento não zero), o valor que ele contém será arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2073">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="6dadd-2074">O conteúdo desse campo DEVE ser ignorado pelo receptor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2074">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-2075">**cProperties:** um inteiro sem sinal de 32 bits que contém o número de elementos na matriz aProps.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2075">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="6dadd-2076">**aProps:** uma matriz de estruturas CDbProp, conforme especificado na seção 0, que contém propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2076">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="6dadd-2077">As estruturas na matriz DEVEM ser separadas por 0 a 3 bytes de preenchimento, de forma que cada estrutura comece em um deslocamento que é um múltiplo de 4 bytes do início da mensagem que contém essa matriz.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2077">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="6dadd-2078">Se bytes de preenchimento estão presentes, o valor que eles contêm é arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2078">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="6dadd-2079">O conteúdo dos bytes de preenchimento DEVE ser ignorado pelo receptor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2079">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="6dadd-2080">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="6dadd-2080">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="6dadd-2081">A estrutura CPidMapper contém uma matriz de IDs de propriedade especificando as propriedades a retornar em um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2081">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="6dadd-2082">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2082">0</span></span>

<span data-ttu-id="6dadd-2083">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2083">1</span></span>

<span data-ttu-id="6dadd-2084">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2084">2</span></span>

<span data-ttu-id="6dadd-2085">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2085">3</span></span>

<span data-ttu-id="6dadd-2086">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2086">4</span></span>

<span data-ttu-id="6dadd-2087">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2087">5</span></span>

<span data-ttu-id="6dadd-2088">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2088">6</span></span>

<span data-ttu-id="6dadd-2089">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2089">7</span></span>

<span data-ttu-id="6dadd-2090">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2090">8</span></span>

<span data-ttu-id="6dadd-2091">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2091">9</span></span>

<span data-ttu-id="6dadd-2092">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2092">1</span></span><br/> <span data-ttu-id="6dadd-2093">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2093">0</span></span><br/>

<span data-ttu-id="6dadd-2094">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2094">1</span></span>

<span data-ttu-id="6dadd-2095">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2095">2</span></span>

<span data-ttu-id="6dadd-2096">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2096">3</span></span>

<span data-ttu-id="6dadd-2097">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2097">4</span></span>

<span data-ttu-id="6dadd-2098">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2098">5</span></span>

<span data-ttu-id="6dadd-2099">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2099">6</span></span>

<span data-ttu-id="6dadd-2100">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2100">7</span></span>

<span data-ttu-id="6dadd-2101">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2101">8</span></span>

<span data-ttu-id="6dadd-2102">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2102">9</span></span>

<span data-ttu-id="6dadd-2103">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2103">2</span></span><br/> <span data-ttu-id="6dadd-2104">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2104">0</span></span><br/>

<span data-ttu-id="6dadd-2105">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2105">1</span></span>

<span data-ttu-id="6dadd-2106">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2106">2</span></span>

<span data-ttu-id="6dadd-2107">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2107">3</span></span>

<span data-ttu-id="6dadd-2108">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2108">4</span></span>

<span data-ttu-id="6dadd-2109">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2109">5</span></span>

<span data-ttu-id="6dadd-2110">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2110">6</span></span>

<span data-ttu-id="6dadd-2111">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2111">7</span></span>

<span data-ttu-id="6dadd-2112">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2112">8</span></span>

<span data-ttu-id="6dadd-2113">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2113">9</span></span>

<span data-ttu-id="6dadd-2114">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2114">3</span></span><br/> <span data-ttu-id="6dadd-2115">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2115">0</span></span><br/>

<span data-ttu-id="6dadd-2116">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2116">1</span></span>

<span data-ttu-id="6dadd-2117">count</span><span class="sxs-lookup"><span data-stu-id="6dadd-2117">count</span></span>

<span data-ttu-id="6dadd-2118">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="6dadd-2118">aPropSpec</span></span>

<span data-ttu-id="6dadd-2119">... (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2119">... (variable)</span></span>



 

<span data-ttu-id="6dadd-2120">**count:** um inteiro sem sinal de 32 bits que contém o número de elementos na matriz aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2120">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="6dadd-2121">**aPropSpec**: matriz de estruturas CFullPropSpec que indica as propriedades a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2121">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="6dadd-2122">As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura tenha um alinhamento de 4 bytes desde o início de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2122">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="6dadd-2123">Esses bytes de preenchimento podem ser qualquer valor arbitrário e devem ser ignorados no recebimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2123">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="6dadd-2124">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="6dadd-2124">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="6dadd-2125">A estrutura CRowSeekAt contém o deslocamento no qual recuperar linhas em uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2125">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="6dadd-2126">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2126">0</span></span>

<span data-ttu-id="6dadd-2127">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2127">1</span></span>

<span data-ttu-id="6dadd-2128">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2128">2</span></span>

<span data-ttu-id="6dadd-2129">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2129">3</span></span>

<span data-ttu-id="6dadd-2130">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2130">4</span></span>

<span data-ttu-id="6dadd-2131">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2131">5</span></span>

<span data-ttu-id="6dadd-2132">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2132">6</span></span>

<span data-ttu-id="6dadd-2133">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2133">7</span></span>

<span data-ttu-id="6dadd-2134">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2134">8</span></span>

<span data-ttu-id="6dadd-2135">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2135">9</span></span>

<span data-ttu-id="6dadd-2136">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2136">1</span></span><br/> <span data-ttu-id="6dadd-2137">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2137">0</span></span><br/>

<span data-ttu-id="6dadd-2138">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2138">1</span></span>

<span data-ttu-id="6dadd-2139">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2139">2</span></span>

<span data-ttu-id="6dadd-2140">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2140">3</span></span>

<span data-ttu-id="6dadd-2141">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2141">4</span></span>

<span data-ttu-id="6dadd-2142">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2142">5</span></span>

<span data-ttu-id="6dadd-2143">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2143">6</span></span>

<span data-ttu-id="6dadd-2144">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2144">7</span></span>

<span data-ttu-id="6dadd-2145">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2145">8</span></span>

<span data-ttu-id="6dadd-2146">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2146">9</span></span>

<span data-ttu-id="6dadd-2147">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2147">2</span></span><br/> <span data-ttu-id="6dadd-2148">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2148">0</span></span><br/>

<span data-ttu-id="6dadd-2149">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2149">1</span></span>

<span data-ttu-id="6dadd-2150">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2150">2</span></span>

<span data-ttu-id="6dadd-2151">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2151">3</span></span>

<span data-ttu-id="6dadd-2152">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2152">4</span></span>

<span data-ttu-id="6dadd-2153">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2153">5</span></span>

<span data-ttu-id="6dadd-2154">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2154">6</span></span>

<span data-ttu-id="6dadd-2155">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2155">7</span></span>

<span data-ttu-id="6dadd-2156">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2156">8</span></span>

<span data-ttu-id="6dadd-2157">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2157">9</span></span>

<span data-ttu-id="6dadd-2158">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2158">3</span></span><br/> <span data-ttu-id="6dadd-2159">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2159">0</span></span><br/>

<span data-ttu-id="6dadd-2160">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2160">1</span></span>

<span data-ttu-id="6dadd-2161">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="6dadd-2161">\_hRegion</span></span>

<span data-ttu-id="6dadd-2162">\_cskip</span><span class="sxs-lookup"><span data-stu-id="6dadd-2162">\_cskip</span></span>

<span data-ttu-id="6dadd-2163">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="6dadd-2163">\_bmkOffset</span></span>



 

<span data-ttu-id="6dadd-2164">**\_ hRegion**: deve ser definido como 0x00000000 e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2164">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="6dadd-2165">**\_ cskip**: um inteiro sem sinal de 32 bits contendo o número de linhas a serem ignoradas no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2165">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="6dadd-2166">**\_ bmkOffset**: um valor de 32 bits que representa o identificador do **indicador** que indica a posição inicial a partir da qual ignorar o número de linhas especificado em \_ cskip, antes de iniciar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2166">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="6dadd-2167">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="6dadd-2167">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="6dadd-2168">A estrutura CRowSeekAtRatio identifica o ponto no qual iniciar a recuperação para uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2168">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="6dadd-2169">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2169">0</span></span>

<span data-ttu-id="6dadd-2170">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2170">1</span></span>

<span data-ttu-id="6dadd-2171">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2171">2</span></span>

<span data-ttu-id="6dadd-2172">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2172">3</span></span>

<span data-ttu-id="6dadd-2173">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2173">4</span></span>

<span data-ttu-id="6dadd-2174">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2174">5</span></span>

<span data-ttu-id="6dadd-2175">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2175">6</span></span>

<span data-ttu-id="6dadd-2176">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2176">7</span></span>

<span data-ttu-id="6dadd-2177">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2177">8</span></span>

<span data-ttu-id="6dadd-2178">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2178">9</span></span>

<span data-ttu-id="6dadd-2179">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2179">1</span></span><br/> <span data-ttu-id="6dadd-2180">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2180">0</span></span><br/>

<span data-ttu-id="6dadd-2181">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2181">1</span></span>

<span data-ttu-id="6dadd-2182">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2182">2</span></span>

<span data-ttu-id="6dadd-2183">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2183">3</span></span>

<span data-ttu-id="6dadd-2184">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2184">4</span></span>

<span data-ttu-id="6dadd-2185">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2185">5</span></span>

<span data-ttu-id="6dadd-2186">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2186">6</span></span>

<span data-ttu-id="6dadd-2187">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2187">7</span></span>

<span data-ttu-id="6dadd-2188">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2188">8</span></span>

<span data-ttu-id="6dadd-2189">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2189">9</span></span>

<span data-ttu-id="6dadd-2190">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2190">2</span></span><br/> <span data-ttu-id="6dadd-2191">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2191">0</span></span><br/>

<span data-ttu-id="6dadd-2192">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2192">1</span></span>

<span data-ttu-id="6dadd-2193">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2193">2</span></span>

<span data-ttu-id="6dadd-2194">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2194">3</span></span>

<span data-ttu-id="6dadd-2195">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2195">4</span></span>

<span data-ttu-id="6dadd-2196">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2196">5</span></span>

<span data-ttu-id="6dadd-2197">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2197">6</span></span>

<span data-ttu-id="6dadd-2198">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2198">7</span></span>

<span data-ttu-id="6dadd-2199">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2199">8</span></span>

<span data-ttu-id="6dadd-2200">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2200">9</span></span>

<span data-ttu-id="6dadd-2201">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2201">3</span></span><br/> <span data-ttu-id="6dadd-2202">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2202">0</span></span><br/>

<span data-ttu-id="6dadd-2203">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2203">1</span></span>

<span data-ttu-id="6dadd-2204">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="6dadd-2204">CiTblChapt</span></span>

<span data-ttu-id="6dadd-2205">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="6dadd-2205">\_hRegion</span></span>

<span data-ttu-id="6dadd-2206">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="6dadd-2206">\_ulNumerator</span></span>

<span data-ttu-id="6dadd-2207">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="6dadd-2207">\_ulDenominator</span></span>



 

<span data-ttu-id="6dadd-2208">**CiTblChapt**: um inteiro de 32 bits sem sinal indicando o capítulo do conjunto de linhas do qual recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2208">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="6dadd-2209">**\_ hRegion**: deve ser definido como 0x00000000 e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2209">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="6dadd-2210">**\_ ulNumerator**: inteiro de 32 bits sem sinal que representa o numerador da proporção de linhas no capítulo no qual iniciar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2210">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="6dadd-2211">**\_ ulDenominator**: inteiro de 32 bits sem sinal que representa o denominador da proporção de linhas no capítulo no qual iniciar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2211">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="6dadd-2212">DEVE ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2212">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="6dadd-2213">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="6dadd-2213">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="6dadd-2214">A estrutura CRowSeekByBookmark identifica os indicadores dos quais começar a recuperar linhas para uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2214">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="6dadd-2215">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2215">0</span></span>

<span data-ttu-id="6dadd-2216">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2216">1</span></span>

<span data-ttu-id="6dadd-2217">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2217">2</span></span>

<span data-ttu-id="6dadd-2218">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2218">3</span></span>

<span data-ttu-id="6dadd-2219">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2219">4</span></span>

<span data-ttu-id="6dadd-2220">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2220">5</span></span>

<span data-ttu-id="6dadd-2221">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2221">6</span></span>

<span data-ttu-id="6dadd-2222">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2222">7</span></span>

<span data-ttu-id="6dadd-2223">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2223">8</span></span>

<span data-ttu-id="6dadd-2224">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2224">9</span></span>

<span data-ttu-id="6dadd-2225">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2225">1</span></span><br/> <span data-ttu-id="6dadd-2226">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2226">0</span></span><br/>

<span data-ttu-id="6dadd-2227">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2227">1</span></span>

<span data-ttu-id="6dadd-2228">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2228">2</span></span>

<span data-ttu-id="6dadd-2229">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2229">3</span></span>

<span data-ttu-id="6dadd-2230">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2230">4</span></span>

<span data-ttu-id="6dadd-2231">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2231">5</span></span>

<span data-ttu-id="6dadd-2232">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2232">6</span></span>

<span data-ttu-id="6dadd-2233">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2233">7</span></span>

<span data-ttu-id="6dadd-2234">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2234">8</span></span>

<span data-ttu-id="6dadd-2235">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2235">9</span></span>

<span data-ttu-id="6dadd-2236">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2236">2</span></span><br/> <span data-ttu-id="6dadd-2237">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2237">0</span></span><br/>

<span data-ttu-id="6dadd-2238">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2238">1</span></span>

<span data-ttu-id="6dadd-2239">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2239">2</span></span>

<span data-ttu-id="6dadd-2240">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2240">3</span></span>

<span data-ttu-id="6dadd-2241">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2241">4</span></span>

<span data-ttu-id="6dadd-2242">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2242">5</span></span>

<span data-ttu-id="6dadd-2243">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2243">6</span></span>

<span data-ttu-id="6dadd-2244">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2244">7</span></span>

<span data-ttu-id="6dadd-2245">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2245">8</span></span>

<span data-ttu-id="6dadd-2246">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2246">9</span></span>

<span data-ttu-id="6dadd-2247">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2247">3</span></span><br/> <span data-ttu-id="6dadd-2248">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2248">0</span></span><br/>

<span data-ttu-id="6dadd-2249">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2249">1</span></span>

<span data-ttu-id="6dadd-2250">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="6dadd-2250">\_hRegion</span></span>

<span data-ttu-id="6dadd-2251">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="6dadd-2251">\_cBookmarks</span></span>

<span data-ttu-id="6dadd-2252">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="6dadd-2252">\_maxRet</span></span>

<span data-ttu-id="6dadd-2253">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="6dadd-2253">\_cValidRet</span></span>

<span data-ttu-id="6dadd-2254">\_aBookmarks (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2254">\_aBookmarks (variable)</span></span>

<span data-ttu-id="6dadd-2255">\_ascRet (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2255">\_ascRet (variable)</span></span>



 

<span data-ttu-id="6dadd-2256">**\_ hRegion**: DEVE ser definido como 0x00000000 e DEVE ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2256">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="6dadd-2257">**\_ cBookmarks:** inteiro de 32 bits sem sinal que representa o número de elementos na \_ matriz aBookmarks.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2257">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="6dadd-2258">**\_ maxRet:** inteiro de 32 bits sem sinal que representa o número de elementos na \_ matriz ascRet.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2258">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="6dadd-2259">**\_ cValidRet:** inteiro de 32 bits sem sinal que representa o número de elementos na \_ matriz ascRet que são válidos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2259">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="6dadd-2260">Elementos válidos foram definidos na matriz, enquanto elementos inválidos são indefinido.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2260">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="6dadd-2261">**\_ aBookmarks:** uma matriz de alças de indicador (cada uma representada por 4 bytes), conforme obtido de uma mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2261">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="6dadd-2262">**\_ ascRet:** uma matriz de valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2262">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="6dadd-2263">Quando o CRowSeekByBookMark é enviado como parte da solicitação CPMGetRowsIn, o número de entradas na matriz DEVE ser igual a \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2263">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="6dadd-2264">Quando enviados pelo cliente, os valores DEVEM ser definidos como zero e o servidor DEVE ignorar o conteúdo da matriz.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2264">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="6dadd-2265">Quando enviados pelo servidor (como parte da mensagem CPMGetRowsOut), os valores na matriz indicam o status do resultado para cada recuperação de linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2265">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="6dadd-2266">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="6dadd-2266">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="6dadd-2267">A estrutura CRowSeekNext contém o número de linhas a ignorar em uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2267">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="6dadd-2268">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2268">0</span></span>

<span data-ttu-id="6dadd-2269">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2269">1</span></span>

<span data-ttu-id="6dadd-2270">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2270">2</span></span>

<span data-ttu-id="6dadd-2271">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2271">3</span></span>

<span data-ttu-id="6dadd-2272">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2272">4</span></span>

<span data-ttu-id="6dadd-2273">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2273">5</span></span>

<span data-ttu-id="6dadd-2274">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2274">6</span></span>

<span data-ttu-id="6dadd-2275">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2275">7</span></span>

<span data-ttu-id="6dadd-2276">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2276">8</span></span>

<span data-ttu-id="6dadd-2277">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2277">9</span></span>

<span data-ttu-id="6dadd-2278">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2278">1</span></span><br/> <span data-ttu-id="6dadd-2279">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2279">0</span></span><br/>

<span data-ttu-id="6dadd-2280">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2280">1</span></span>

<span data-ttu-id="6dadd-2281">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2281">2</span></span>

<span data-ttu-id="6dadd-2282">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2282">3</span></span>

<span data-ttu-id="6dadd-2283">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2283">4</span></span>

<span data-ttu-id="6dadd-2284">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2284">5</span></span>

<span data-ttu-id="6dadd-2285">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2285">6</span></span>

<span data-ttu-id="6dadd-2286">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2286">7</span></span>

<span data-ttu-id="6dadd-2287">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2287">8</span></span>

<span data-ttu-id="6dadd-2288">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2288">9</span></span>

<span data-ttu-id="6dadd-2289">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2289">2</span></span><br/> <span data-ttu-id="6dadd-2290">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2290">0</span></span><br/>

<span data-ttu-id="6dadd-2291">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2291">1</span></span>

<span data-ttu-id="6dadd-2292">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2292">2</span></span>

<span data-ttu-id="6dadd-2293">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2293">3</span></span>

<span data-ttu-id="6dadd-2294">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2294">4</span></span>

<span data-ttu-id="6dadd-2295">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2295">5</span></span>

<span data-ttu-id="6dadd-2296">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2296">6</span></span>

<span data-ttu-id="6dadd-2297">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2297">7</span></span>

<span data-ttu-id="6dadd-2298">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2298">8</span></span>

<span data-ttu-id="6dadd-2299">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2299">9</span></span>

<span data-ttu-id="6dadd-2300">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2300">3</span></span><br/> <span data-ttu-id="6dadd-2301">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2301">0</span></span><br/>

<span data-ttu-id="6dadd-2302">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2302">1</span></span>

<span data-ttu-id="6dadd-2303">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="6dadd-2303">CiTblChapt</span></span>

<span data-ttu-id="6dadd-2304">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="6dadd-2304">\_hRegion</span></span>

<span data-ttu-id="6dadd-2305">\_cskip</span><span class="sxs-lookup"><span data-stu-id="6dadd-2305">\_cskip</span></span>



 

<span data-ttu-id="6dadd-2306">**CiTblChapt:** inteiro de 32 bits sem sinal especificando o capítulo de conjuntos de linhas do qual recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2306">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="6dadd-2307">**\_ hRegion**: DEVE ser definido como 0x00000000 e DEVE ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2307">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="6dadd-2308">**\_ cskip:** inteiro de 32 bits sem sinal que representa o número de linhas a ignorar no conjuntos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2308">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="6dadd-2309">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="6dadd-2309">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="6dadd-2310">A estrutura CRowsetProperties contém informações de configuração para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2310">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="6dadd-2311">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2311">0</span></span>

<span data-ttu-id="6dadd-2312">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2312">1</span></span>

<span data-ttu-id="6dadd-2313">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2313">2</span></span>

<span data-ttu-id="6dadd-2314">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2314">3</span></span>

<span data-ttu-id="6dadd-2315">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2315">4</span></span>

<span data-ttu-id="6dadd-2316">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2316">5</span></span>

<span data-ttu-id="6dadd-2317">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2317">6</span></span>

<span data-ttu-id="6dadd-2318">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2318">7</span></span>

<span data-ttu-id="6dadd-2319">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2319">8</span></span>

<span data-ttu-id="6dadd-2320">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2320">9</span></span>

<span data-ttu-id="6dadd-2321">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2321">1</span></span><br/> <span data-ttu-id="6dadd-2322">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2322">0</span></span><br/>

<span data-ttu-id="6dadd-2323">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2323">1</span></span>

<span data-ttu-id="6dadd-2324">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2324">2</span></span>

<span data-ttu-id="6dadd-2325">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2325">3</span></span>

<span data-ttu-id="6dadd-2326">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2326">4</span></span>

<span data-ttu-id="6dadd-2327">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2327">5</span></span>

<span data-ttu-id="6dadd-2328">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2328">6</span></span>

<span data-ttu-id="6dadd-2329">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2329">7</span></span>

<span data-ttu-id="6dadd-2330">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2330">8</span></span>

<span data-ttu-id="6dadd-2331">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2331">9</span></span>

<span data-ttu-id="6dadd-2332">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2332">2</span></span><br/> <span data-ttu-id="6dadd-2333">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2333">0</span></span><br/>

<span data-ttu-id="6dadd-2334">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2334">1</span></span>

<span data-ttu-id="6dadd-2335">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2335">2</span></span>

<span data-ttu-id="6dadd-2336">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2336">3</span></span>

<span data-ttu-id="6dadd-2337">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2337">4</span></span>

<span data-ttu-id="6dadd-2338">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2338">5</span></span>

<span data-ttu-id="6dadd-2339">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2339">6</span></span>

<span data-ttu-id="6dadd-2340">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2340">7</span></span>

<span data-ttu-id="6dadd-2341">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2341">8</span></span>

<span data-ttu-id="6dadd-2342">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2342">9</span></span>

<span data-ttu-id="6dadd-2343">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2343">3</span></span><br/> <span data-ttu-id="6dadd-2344">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2344">0</span></span><br/>

<span data-ttu-id="6dadd-2345">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2345">1</span></span>

<span data-ttu-id="6dadd-2346">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="6dadd-2346">\_uBooleanOptions</span></span>

<span data-ttu-id="6dadd-2347">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="6dadd-2347">\_ulMaxOpenRows</span></span>

<span data-ttu-id="6dadd-2348">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="6dadd-2348">\_ulMemoryUsage</span></span>

<span data-ttu-id="6dadd-2349">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="6dadd-2349">\_cMaxResults</span></span>

<span data-ttu-id="6dadd-2350">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="6dadd-2350">\_cCmdTimeout</span></span>



 

<span data-ttu-id="6dadd-2351">**\_ uBooleanOptions:** os três bits menos significativos desse campo DEVEM conter um dos três valores a seguir:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2351">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="6dadd-2352">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-2352">Value</span></span>                  | <span data-ttu-id="6dadd-2353">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-2353">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6dadd-2354">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-2354">eSequential 0x00000001</span></span> | <span data-ttu-id="6dadd-2355">O cursor só pode ser movido para frente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2355">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="6dadd-2356">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-2356">eLocatable 0x00000003</span></span>  | <span data-ttu-id="6dadd-2357">O cursor pode ser movido para qualquer posição.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2357">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="6dadd-2358">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="6dadd-2358">eScrollable 0x00000007</span></span> | <span data-ttu-id="6dadd-2359">O cursor pode ser movido para qualquer posição e buscar em qualquer direção.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2359">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="6dadd-2360">Os bits restantes podem ser claros ou definidos como qualquer combinação dos seguintes valores logicamente OR'd juntos:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2360">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="6dadd-2361">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-2361">Value</span></span>                     | <span data-ttu-id="6dadd-2362">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-2362">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-2363">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="6dadd-2363">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="6dadd-2364">O cliente não aguardará a conclusão da execução.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2364">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="6dadd-2365">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="6dadd-2365">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="6dadd-2366">Retornar as primeiras linhas encontradas, não as melhores.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2366">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="6dadd-2367">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="6dadd-2367">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="6dadd-2368">O servidor NÃO DEVE descartar linhas até que o cliente seja feito com uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2368">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="6dadd-2369">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="6dadd-2369">eChaptered 0x00000800</span></span>     | <span data-ttu-id="6dadd-2370">O rowset dá suporte a capítulos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2370">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="6dadd-2371">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="6dadd-2371">eUseCI 0x00001000</span></span>         | <span data-ttu-id="6dadd-2372">Responda apenas à consulta do índice, não do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2372">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="6dadd-2373">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="6dadd-2373">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="6dadd-2374">O serviço de indexação é considerar a otimização do tempo de resposta para o cliente ao executar a remoção de resultados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2374">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="6dadd-2375">**\_ ulMaxOpenRows:** inteiro de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2375">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="6dadd-2376">Deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2376">Must be set to 0x00000000.</span></span> <span data-ttu-id="6dadd-2377">Não usado e DEVE ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2377">Not used and MUST be ignored.</span></span>

<span data-ttu-id="6dadd-2378">**\_ ulMemoryUsage:** inteiro de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2378">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="6dadd-2379">Deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="6dadd-2380">Não usado e DEVE ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="6dadd-2381">**\_ cMaxResults:** um inteiro sem sinal de 32 bits que especifica o número máximo de linhas que devem ser retornadas para a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2381">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="6dadd-2382">**\_ cCmdTimeout:** um inteiro sem sinal de 32 bits, especificando o número de segundos em que uma consulta deve ser encerrada e encerrada automaticamente, contando a partir do momento em que a consulta começa a ser executada no servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2382">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="6dadd-2383">Um valor de 0x00000000 significa que a consulta não deve ter o tempo máximo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2383">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="6dadd-2384">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="6dadd-2384">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="6dadd-2385">A estrutura CRowVariant contém a parte de tamanho fixo de um tipo de dados de comprimento variável armazenado na mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2385">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="6dadd-2386">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2386">0</span></span>

<span data-ttu-id="6dadd-2387">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2387">1</span></span>

<span data-ttu-id="6dadd-2388">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2388">2</span></span>

<span data-ttu-id="6dadd-2389">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2389">3</span></span>

<span data-ttu-id="6dadd-2390">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2390">4</span></span>

<span data-ttu-id="6dadd-2391">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2391">5</span></span>

<span data-ttu-id="6dadd-2392">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2392">6</span></span>

<span data-ttu-id="6dadd-2393">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2393">7</span></span>

<span data-ttu-id="6dadd-2394">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2394">8</span></span>

<span data-ttu-id="6dadd-2395">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2395">9</span></span>

<span data-ttu-id="6dadd-2396">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2396">1</span></span><br/> <span data-ttu-id="6dadd-2397">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2397">0</span></span><br/>

<span data-ttu-id="6dadd-2398">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2398">1</span></span>

<span data-ttu-id="6dadd-2399">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2399">2</span></span>

<span data-ttu-id="6dadd-2400">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2400">3</span></span>

<span data-ttu-id="6dadd-2401">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2401">4</span></span>

<span data-ttu-id="6dadd-2402">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2402">5</span></span>

<span data-ttu-id="6dadd-2403">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2403">6</span></span>

<span data-ttu-id="6dadd-2404">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2404">7</span></span>

<span data-ttu-id="6dadd-2405">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2405">8</span></span>

<span data-ttu-id="6dadd-2406">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2406">9</span></span>

<span data-ttu-id="6dadd-2407">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2407">2</span></span><br/> <span data-ttu-id="6dadd-2408">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2408">0</span></span><br/>

<span data-ttu-id="6dadd-2409">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2409">1</span></span>

<span data-ttu-id="6dadd-2410">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2410">2</span></span>

<span data-ttu-id="6dadd-2411">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2411">3</span></span>

<span data-ttu-id="6dadd-2412">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2412">4</span></span>

<span data-ttu-id="6dadd-2413">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2413">5</span></span>

<span data-ttu-id="6dadd-2414">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2414">6</span></span>

<span data-ttu-id="6dadd-2415">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2415">7</span></span>

<span data-ttu-id="6dadd-2416">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2416">8</span></span>

<span data-ttu-id="6dadd-2417">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2417">9</span></span>

<span data-ttu-id="6dadd-2418">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2418">3</span></span><br/> <span data-ttu-id="6dadd-2419">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2419">0</span></span><br/>

<span data-ttu-id="6dadd-2420">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2420">1</span></span>

<span data-ttu-id="6dadd-2421">vType</span><span class="sxs-lookup"><span data-stu-id="6dadd-2421">vType</span></span>

<span data-ttu-id="6dadd-2422">reserved1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2422">reserved1</span></span>

<span data-ttu-id="6dadd-2423">reserved2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2423">reserved2</span></span>

<span data-ttu-id="6dadd-2424">Deslocamento (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2424">Offset (optional)</span></span>



 

<span data-ttu-id="6dadd-2425">**vType**: um indicador de tipo, que indica o tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2425">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="6dadd-2426">Ele deve ser um dos valores de VARENUM especificados na seção 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2426">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="6dadd-2427">**reserved1**: não usado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2427">**reserved1**: Not used.</span></span> <span data-ttu-id="6dadd-2428">O valor pode ser definido como qualquer valor arbitrário e deve ser ignorado no recebimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2428">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="6dadd-2429">**reserved2**: não usado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2429">**reserved2**: Not used.</span></span> <span data-ttu-id="6dadd-2430">O valor pode ser definido como qualquer valor arbitrário e deve ser ignorado no recebimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2430">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="6dadd-2431">**Offset**: um deslocamento para dados de comprimento variável (por exemplo, uma cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="6dadd-2431">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="6dadd-2432">Esse deve ser um valor de 32 bits (4 bytes de comprimento) se os deslocamentos de 32 bits estiverem sendo usados (de acordo com as regras na seção 2.2.3.16) ou um valor de 64 byte (8 bytes de comprimento) se os deslocamentos de 64 bits estiverem sendo usados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2432">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="6dadd-2433">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-2433">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="6dadd-2434">A estrutura CSortSet contém a ordem de classificação da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2434">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="6dadd-2435">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2435">0</span></span>

<span data-ttu-id="6dadd-2436">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2436">1</span></span>

<span data-ttu-id="6dadd-2437">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2437">2</span></span>

<span data-ttu-id="6dadd-2438">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2438">3</span></span>

<span data-ttu-id="6dadd-2439">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2439">4</span></span>

<span data-ttu-id="6dadd-2440">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2440">5</span></span>

<span data-ttu-id="6dadd-2441">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2441">6</span></span>

<span data-ttu-id="6dadd-2442">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2442">7</span></span>

<span data-ttu-id="6dadd-2443">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2443">8</span></span>

<span data-ttu-id="6dadd-2444">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2444">9</span></span>

<span data-ttu-id="6dadd-2445">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2445">1</span></span><br/> <span data-ttu-id="6dadd-2446">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2446">0</span></span><br/>

<span data-ttu-id="6dadd-2447">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2447">1</span></span>

<span data-ttu-id="6dadd-2448">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2448">2</span></span>

<span data-ttu-id="6dadd-2449">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2449">3</span></span>

<span data-ttu-id="6dadd-2450">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2450">4</span></span>

<span data-ttu-id="6dadd-2451">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2451">5</span></span>

<span data-ttu-id="6dadd-2452">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2452">6</span></span>

<span data-ttu-id="6dadd-2453">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2453">7</span></span>

<span data-ttu-id="6dadd-2454">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2454">8</span></span>

<span data-ttu-id="6dadd-2455">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2455">9</span></span>

<span data-ttu-id="6dadd-2456">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2456">2</span></span><br/> <span data-ttu-id="6dadd-2457">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2457">0</span></span><br/>

<span data-ttu-id="6dadd-2458">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2458">1</span></span>

<span data-ttu-id="6dadd-2459">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2459">2</span></span>

<span data-ttu-id="6dadd-2460">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2460">3</span></span>

<span data-ttu-id="6dadd-2461">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2461">4</span></span>

<span data-ttu-id="6dadd-2462">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2462">5</span></span>

<span data-ttu-id="6dadd-2463">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2463">6</span></span>

<span data-ttu-id="6dadd-2464">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2464">7</span></span>

<span data-ttu-id="6dadd-2465">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2465">8</span></span>

<span data-ttu-id="6dadd-2466">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2466">9</span></span>

<span data-ttu-id="6dadd-2467">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2467">3</span></span><br/> <span data-ttu-id="6dadd-2468">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2468">0</span></span><br/>

<span data-ttu-id="6dadd-2469">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2469">1</span></span>

<span data-ttu-id="6dadd-2470">Contagem</span><span class="sxs-lookup"><span data-stu-id="6dadd-2470">Count</span></span>

<span data-ttu-id="6dadd-2471">sortArray (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2471">sortArray (variable)</span></span>



 

<span data-ttu-id="6dadd-2472">**Count**: um inteiro sem sinal de 32 bits especificando o número de elementos em sortArray.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2472">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="6dadd-2473">**sortArray**: uma matriz de estruturas CSort que descreve a ordem na qual os resultados da consulta são classificados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2473">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="6dadd-2474">As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura tenha um alinhamento de 4 bytes desde o início de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2474">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="6dadd-2475">Esses bytes de preenchimento podem ser qualquer valor arbitrário e devem ser ignorados no recebimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2475">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="6dadd-2476">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2476">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="6dadd-2477">A estrutura CTableColumn contém uma coluna de uma mensagem CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2477">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="6dadd-2478">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2478">0</span></span>

<span data-ttu-id="6dadd-2479">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2479">1</span></span>

<span data-ttu-id="6dadd-2480">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2480">2</span></span>

<span data-ttu-id="6dadd-2481">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2481">3</span></span>

<span data-ttu-id="6dadd-2482">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2482">4</span></span>

<span data-ttu-id="6dadd-2483">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2483">5</span></span>

<span data-ttu-id="6dadd-2484">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2484">6</span></span>

<span data-ttu-id="6dadd-2485">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2485">7</span></span>

<span data-ttu-id="6dadd-2486">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2486">8</span></span>

<span data-ttu-id="6dadd-2487">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2487">9</span></span>

<span data-ttu-id="6dadd-2488">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2488">1</span></span><br/> <span data-ttu-id="6dadd-2489">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2489">0</span></span><br/>

<span data-ttu-id="6dadd-2490">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2490">1</span></span>

<span data-ttu-id="6dadd-2491">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2491">2</span></span>

<span data-ttu-id="6dadd-2492">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2492">3</span></span>

<span data-ttu-id="6dadd-2493">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2493">4</span></span>

<span data-ttu-id="6dadd-2494">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2494">5</span></span>

<span data-ttu-id="6dadd-2495">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2495">6</span></span>

<span data-ttu-id="6dadd-2496">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2496">7</span></span>

<span data-ttu-id="6dadd-2497">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2497">8</span></span>

<span data-ttu-id="6dadd-2498">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2498">9</span></span>

<span data-ttu-id="6dadd-2499">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2499">2</span></span><br/> <span data-ttu-id="6dadd-2500">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2500">0</span></span><br/>

<span data-ttu-id="6dadd-2501">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2501">1</span></span>

<span data-ttu-id="6dadd-2502">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2502">2</span></span>

<span data-ttu-id="6dadd-2503">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2503">3</span></span>

<span data-ttu-id="6dadd-2504">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2504">4</span></span>

<span data-ttu-id="6dadd-2505">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2505">5</span></span>

<span data-ttu-id="6dadd-2506">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2506">6</span></span>

<span data-ttu-id="6dadd-2507">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2507">7</span></span>

<span data-ttu-id="6dadd-2508">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2508">8</span></span>

<span data-ttu-id="6dadd-2509">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2509">9</span></span>

<span data-ttu-id="6dadd-2510">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2510">3</span></span><br/> <span data-ttu-id="6dadd-2511">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2511">0</span></span><br/>

<span data-ttu-id="6dadd-2512">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2512">1</span></span>

<span data-ttu-id="6dadd-2513">PropSpec</span><span class="sxs-lookup"><span data-stu-id="6dadd-2513">PropSpec</span></span>

<span data-ttu-id="6dadd-2514">... Ela</span><span class="sxs-lookup"><span data-stu-id="6dadd-2514">...(variable)</span></span>

<span data-ttu-id="6dadd-2515">vType</span><span class="sxs-lookup"><span data-stu-id="6dadd-2515">vType</span></span>

<span data-ttu-id="6dadd-2516">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="6dadd-2516">ValueUsed</span></span>

<span data-ttu-id="6dadd-2517">\_padding1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2517">\_padding1 (optional)</span></span>

<span data-ttu-id="6dadd-2518">ValueOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2518">ValueOffset (optional)</span></span>

<span data-ttu-id="6dadd-2519">Valores (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2519">ValueSize (optional)</span></span>

<span data-ttu-id="6dadd-2520">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="6dadd-2520">StatusUsed</span></span>

<span data-ttu-id="6dadd-2521">\_padding2 (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2521">\_padding2 (optional)</span></span>

<span data-ttu-id="6dadd-2522">StatusOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2522">StatusOffset (optional)</span></span>

<span data-ttu-id="6dadd-2523">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="6dadd-2523">LengthUsed</span></span>

<span data-ttu-id="6dadd-2524">\_padding3 (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2524">\_padding3 (optional)</span></span>

<span data-ttu-id="6dadd-2525">LengthOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2525">LengthOffset (optional)</span></span>



 

<span data-ttu-id="6dadd-2526">**PropSpec**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2526">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="6dadd-2527">**vType**: especifica o tipo de valor de dados contido na coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2527">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="6dadd-2528">Consulte o campo vType na seção 2.2.1.1 para obter a lista de valores para esse campo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2528">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="6dadd-2529">**ValueUsed**: um campo de um byte que deve ser definido como 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2529">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="6dadd-2530">Se definido como 0x01, a coluna será transferida dentro da linha de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2530">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="6dadd-2531">Se definido como 0x00, o valor da coluna será transferido na seção de comprimento variável no final do buffer.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2531">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="6dadd-2532">**\_ padding1**: um campo de um byte que deve ser inserido antes de ValueOffset se, sem ele, ValueOffset não começaria em um deslocamento par do início da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2532">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="6dadd-2533">O valor desse byte é arbitrário e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2533">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="6dadd-2534">Se ValueUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2534">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="6dadd-2535">**ValueOffset**: um inteiro de 2 bytes não assinado que especifica o deslocamento do valor da coluna na linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2535">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="6dadd-2536">Se ValueUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2536">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="6dadd-2537">**Values**: um inteiro de 2 bytes sem sinal especificando o tamanho do valor da coluna em bytes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2537">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="6dadd-2538">Se ValueUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2538">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="6dadd-2539">**StatusUsed**: um campo de um byte que deve ser definido como 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2539">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="6dadd-2540">Se definido como 0x01, o status da coluna será transferido dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2540">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="6dadd-2541">Se 0x00, o status da coluna não será transferido dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2541">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="6dadd-2542">**\_ padding2**: um campo de um byte que deve ser inserido antes de StatusOffset se, sem ele, o campo StatusOffset não começaria em um deslocamento par do início da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2542">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="6dadd-2543">O valor desse byte é arbitrário e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2543">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="6dadd-2544">Se StatusUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2544">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="6dadd-2545">**StatusOffset**: um inteiro de 2 bytes não assinado que especifica o deslocamento do status da coluna na linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2545">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="6dadd-2546">Se StatusUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2546">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="6dadd-2547">**LengthUsed**: um campo de um byte que deve ser definido como 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2547">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="6dadd-2548">Se definido como 0x01, o comprimento da coluna é transferido dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2548">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="6dadd-2549">Se 0x00, o comprimento da coluna não deve ser transferido dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2549">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="6dadd-2550">**\_ padding3**: um campo de um byte que deve ser inserido antes de LengthOffset se, sem ele, LengthOffset não começaria em um deslocamento par do início de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2550">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="6dadd-2551">O valor desse byte é arbitrário e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2551">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="6dadd-2552">Se LengthUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2552">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="6dadd-2553">**LengthOffset**: um inteiro de 2 bytes não assinado que especifica o deslocamento do comprimento da coluna na linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2553">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="6dadd-2554">Se LengthUsed for definido como 0x00, esse campo não deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2554">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="6dadd-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="6dadd-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="6dadd-2556">A estrutura SERIALIZEDPROPERTYVALUE contém um valor serializado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2556">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="6dadd-2557">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2557">0</span></span>

<span data-ttu-id="6dadd-2558">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2558">1</span></span>

<span data-ttu-id="6dadd-2559">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2559">2</span></span>

<span data-ttu-id="6dadd-2560">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2560">3</span></span>

<span data-ttu-id="6dadd-2561">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2561">4</span></span>

<span data-ttu-id="6dadd-2562">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2562">5</span></span>

<span data-ttu-id="6dadd-2563">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2563">6</span></span>

<span data-ttu-id="6dadd-2564">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2564">7</span></span>

<span data-ttu-id="6dadd-2565">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2565">8</span></span>

<span data-ttu-id="6dadd-2566">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2566">9</span></span>

<span data-ttu-id="6dadd-2567">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2567">1</span></span><br/> <span data-ttu-id="6dadd-2568">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2568">0</span></span><br/>

<span data-ttu-id="6dadd-2569">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2569">1</span></span>

<span data-ttu-id="6dadd-2570">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2570">2</span></span>

<span data-ttu-id="6dadd-2571">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2571">3</span></span>

<span data-ttu-id="6dadd-2572">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2572">4</span></span>

<span data-ttu-id="6dadd-2573">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2573">5</span></span>

<span data-ttu-id="6dadd-2574">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2574">6</span></span>

<span data-ttu-id="6dadd-2575">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2575">7</span></span>

<span data-ttu-id="6dadd-2576">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2576">8</span></span>

<span data-ttu-id="6dadd-2577">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2577">9</span></span>

<span data-ttu-id="6dadd-2578">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2578">2</span></span><br/> <span data-ttu-id="6dadd-2579">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2579">0</span></span><br/>

<span data-ttu-id="6dadd-2580">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2580">1</span></span>

<span data-ttu-id="6dadd-2581">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2581">2</span></span>

<span data-ttu-id="6dadd-2582">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2582">3</span></span>

<span data-ttu-id="6dadd-2583">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2583">4</span></span>

<span data-ttu-id="6dadd-2584">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2584">5</span></span>

<span data-ttu-id="6dadd-2585">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2585">6</span></span>

<span data-ttu-id="6dadd-2586">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2586">7</span></span>

<span data-ttu-id="6dadd-2587">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2587">8</span></span>

<span data-ttu-id="6dadd-2588">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2588">9</span></span>

<span data-ttu-id="6dadd-2589">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2589">3</span></span><br/> <span data-ttu-id="6dadd-2590">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2590">0</span></span><br/>

<span data-ttu-id="6dadd-2591">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2591">1</span></span>

<span data-ttu-id="6dadd-2592">dwType</span><span class="sxs-lookup"><span data-stu-id="6dadd-2592">dwType</span></span>

<span data-ttu-id="6dadd-2593">RGB (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2593">rgb (variable)</span></span>



 

<span data-ttu-id="6dadd-2594">**dwType**: um dos tipos variantes, definidos na seção 2.2.1.1, que podem ser combinados com modificadores de tipo Variant.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2594">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="6dadd-2595">Para todos os tipos de variantes, exceto aqueles combinados com \_ a matriz VT, SERIALIZEDPROPERTYVALUE tem o mesmo layout que CBaseStorageVariant, conforme especificado na seção 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2595">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="6dadd-2596">Se o tipo Variant for combinado com o \_ modificador de tipo de matriz VT, SAFEARRAY2, especificado na seção 2.2.1.2.1.1, será usado em vez de SAFEARRAY no campo vValue de CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2596">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="6dadd-2597">**RGB**: valor serializado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2597">**rgb**: Serialized value.</span></span> <span data-ttu-id="6dadd-2598">Veja detalhes de serialização para vValue em 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2598">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="6dadd-2599">Cabeçalhos de mensagem 2.2.2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2599">2.2.2 Message Headers</span></span>

<span data-ttu-id="6dadd-2600">Todas as mensagens do protocolo de serviço de indexação de conteúdo têm um cabeçalho de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2600">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="6dadd-2601">Veja abaixo um diagrama que mostra o formato de cabeçalho da mensagem do protocolo de serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2601">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="6dadd-2602">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2602">0</span></span>

<span data-ttu-id="6dadd-2603">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2603">1</span></span>

<span data-ttu-id="6dadd-2604">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2604">2</span></span>

<span data-ttu-id="6dadd-2605">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2605">3</span></span>

<span data-ttu-id="6dadd-2606">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2606">4</span></span>

<span data-ttu-id="6dadd-2607">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2607">5</span></span>

<span data-ttu-id="6dadd-2608">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2608">6</span></span>

<span data-ttu-id="6dadd-2609">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2609">7</span></span>

<span data-ttu-id="6dadd-2610">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2610">8</span></span>

<span data-ttu-id="6dadd-2611">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2611">9</span></span>

<span data-ttu-id="6dadd-2612">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2612">1</span></span><br/> <span data-ttu-id="6dadd-2613">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2613">0</span></span><br/>

<span data-ttu-id="6dadd-2614">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2614">1</span></span>

<span data-ttu-id="6dadd-2615">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2615">2</span></span>

<span data-ttu-id="6dadd-2616">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2616">3</span></span>

<span data-ttu-id="6dadd-2617">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2617">4</span></span>

<span data-ttu-id="6dadd-2618">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2618">5</span></span>

<span data-ttu-id="6dadd-2619">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2619">6</span></span>

<span data-ttu-id="6dadd-2620">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2620">7</span></span>

<span data-ttu-id="6dadd-2621">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2621">8</span></span>

<span data-ttu-id="6dadd-2622">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2622">9</span></span>

<span data-ttu-id="6dadd-2623">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2623">2</span></span><br/> <span data-ttu-id="6dadd-2624">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2624">0</span></span><br/>

<span data-ttu-id="6dadd-2625">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2625">1</span></span>

<span data-ttu-id="6dadd-2626">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2626">2</span></span>

<span data-ttu-id="6dadd-2627">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2627">3</span></span>

<span data-ttu-id="6dadd-2628">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2628">4</span></span>

<span data-ttu-id="6dadd-2629">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2629">5</span></span>

<span data-ttu-id="6dadd-2630">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2630">6</span></span>

<span data-ttu-id="6dadd-2631">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2631">7</span></span>

<span data-ttu-id="6dadd-2632">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2632">8</span></span>

<span data-ttu-id="6dadd-2633">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2633">9</span></span>

<span data-ttu-id="6dadd-2634">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2634">3</span></span><br/> <span data-ttu-id="6dadd-2635">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2635">0</span></span><br/>

<span data-ttu-id="6dadd-2636">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2636">1</span></span>

<span data-ttu-id="6dadd-2637">\_MSG</span><span class="sxs-lookup"><span data-stu-id="6dadd-2637">\_msg</span></span>

<span data-ttu-id="6dadd-2638">\_Estado</span><span class="sxs-lookup"><span data-stu-id="6dadd-2638">\_status</span></span>

<span data-ttu-id="6dadd-2639">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="6dadd-2639">\_ulChecksum</span></span>

<span data-ttu-id="6dadd-2640">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2640">\_ulReserved2</span></span>



 

<span data-ttu-id="6dadd-2641">\_**msg**: um inteiro de 32 bits que identifica o tipo de mensagem após o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2641">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="6dadd-2642">A tabela a seguir lista as mensagens do protocolo de serviço de indexação de conteúdo e os valores inteiros especificados para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2642">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="6dadd-2643">Conforme mostrado na tabela, alguns valores identificam 2 mensagens na tabela.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2643">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="6dadd-2644">Nessas instâncias, a mensagem após o cabeçalho pode ser identificada pela direção do fluxo de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2644">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="6dadd-2645">Se a direção for cliente para servidor, a mensagem com "in" acrescentado ao nome da mensagem será indicada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2645">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="6dadd-2646">Se a direção for servidor para cliente, a mensagem com "out" anexado ao nome da mensagem será indicada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2646">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="6dadd-2647">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-2647">Value</span></span>      | <span data-ttu-id="6dadd-2648">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-2648">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="6dadd-2649">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2649">0x000000C8</span></span> | <span data-ttu-id="6dadd-2650">CPMConnectIn ou CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2650">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="6dadd-2651">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2651">0x000000C9</span></span> | <span data-ttu-id="6dadd-2652">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="6dadd-2652">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="6dadd-2653">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="6dadd-2653">0x000000CA</span></span> | <span data-ttu-id="6dadd-2654">CPMCreateQueryIn ou CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2654">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="6dadd-2655">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="6dadd-2655">0x000000CB</span></span> | <span data-ttu-id="6dadd-2656">CPMFreeCursorIn ou CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2656">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="6dadd-2657">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="6dadd-2657">0x000000CC</span></span> | <span data-ttu-id="6dadd-2658">CPMGetRowsIn ou CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2658">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="6dadd-2659">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="6dadd-2659">0x000000CD</span></span> | <span data-ttu-id="6dadd-2660">CPMRatioFinishedIn ou CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2660">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="6dadd-2661">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="6dadd-2661">0x000000CE</span></span> | <span data-ttu-id="6dadd-2662">CPMCompareBmkIn ou CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2662">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="6dadd-2663">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="6dadd-2663">0x000000CF</span></span> | <span data-ttu-id="6dadd-2664">CPMGetApproximatePositionIn ou CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2664">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="6dadd-2665">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2665">0x000000D0</span></span> | <span data-ttu-id="6dadd-2666">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2666">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="6dadd-2667">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2667">0x000000D1</span></span> | <span data-ttu-id="6dadd-2668">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="6dadd-2668">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="6dadd-2669">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2669">0x000000D2</span></span> | <span data-ttu-id="6dadd-2670">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2670">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="6dadd-2671">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2671">0x000000D7</span></span> | <span data-ttu-id="6dadd-2672">CPMGetQueryStatusIn ou CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2672">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="6dadd-2673">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2673">0x000000D9</span></span> | <span data-ttu-id="6dadd-2674">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2674">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="6dadd-2675">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2675">0x000000E1</span></span> | <span data-ttu-id="6dadd-2676">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2676">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="6dadd-2677">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2677">0x000000E4</span></span> | <span data-ttu-id="6dadd-2678">CPMFetchValueIn ou CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2678">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="6dadd-2679">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2679">0x000000E6</span></span> | <span data-ttu-id="6dadd-2680">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2680">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="6dadd-2681">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2681">0x000000E7</span></span> | <span data-ttu-id="6dadd-2682">CPMGetQueryStatusExIn ou PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2682">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="6dadd-2683">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2683">0x000000E8</span></span> | <span data-ttu-id="6dadd-2684">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2684">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="6dadd-2685">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2685">0x000000E9</span></span> | <span data-ttu-id="6dadd-2686">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2686">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="6dadd-2687">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="6dadd-2687">0x000000EC</span></span> | <span data-ttu-id="6dadd-2688">CPMSetCatStateIn ou CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2688">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="6dadd-2689">\_**status**: um HRESULT \[ MS-sys \] , que indica o status da operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2689">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="6dadd-2690">*Comportamento do Windows: o cliente sempre define o \_ campo status como 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="6dadd-2690">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="6dadd-2691">**\_ ulChecksum**: o \_ ulChecksum deve ser calculado conforme especificado na seção 3.2.4 para as seguintes mensagens:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2691">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="6dadd-2692">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2692">CPMConnectIn</span></span>
-   <span data-ttu-id="6dadd-2693">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2693">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="6dadd-2694">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2694">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="6dadd-2695">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2695">CPMGetRowsIn</span></span>
-   <span data-ttu-id="6dadd-2696">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2696">CPMFetchValueIn</span></span>

<span data-ttu-id="6dadd-2697">Para todas as outras mensagens, \_ ULCHECKSUM deve ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2697">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="6dadd-2698">Um cliente deve ignorar o \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2698">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="6dadd-2699">**\_ ulReserved2**: deve ser definido como 0 e ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2699">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="6dadd-2700">mensagens 2.2.3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2700">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="6dadd-2701">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2701">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="6dadd-2702">A mensagem CPMCiStateInOut contém informações sobre o estado do serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2702">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="6dadd-2703">O formato da mensagem CPMCiStateInOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2703">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-2704">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2704">0</span></span>

<span data-ttu-id="6dadd-2705">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2705">1</span></span>

<span data-ttu-id="6dadd-2706">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2706">2</span></span>

<span data-ttu-id="6dadd-2707">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2707">3</span></span>

<span data-ttu-id="6dadd-2708">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2708">4</span></span>

<span data-ttu-id="6dadd-2709">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2709">5</span></span>

<span data-ttu-id="6dadd-2710">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2710">6</span></span>

<span data-ttu-id="6dadd-2711">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2711">7</span></span>

<span data-ttu-id="6dadd-2712">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2712">8</span></span>

<span data-ttu-id="6dadd-2713">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2713">9</span></span>

<span data-ttu-id="6dadd-2714">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2714">1</span></span><br/> <span data-ttu-id="6dadd-2715">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2715">0</span></span><br/>

<span data-ttu-id="6dadd-2716">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2716">1</span></span>

<span data-ttu-id="6dadd-2717">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2717">2</span></span>

<span data-ttu-id="6dadd-2718">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2718">3</span></span>

<span data-ttu-id="6dadd-2719">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2719">4</span></span>

<span data-ttu-id="6dadd-2720">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2720">5</span></span>

<span data-ttu-id="6dadd-2721">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2721">6</span></span>

<span data-ttu-id="6dadd-2722">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2722">7</span></span>

<span data-ttu-id="6dadd-2723">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2723">8</span></span>

<span data-ttu-id="6dadd-2724">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2724">9</span></span>

<span data-ttu-id="6dadd-2725">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2725">2</span></span><br/> <span data-ttu-id="6dadd-2726">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2726">0</span></span><br/>

<span data-ttu-id="6dadd-2727">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2727">1</span></span>

<span data-ttu-id="6dadd-2728">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2728">2</span></span>

<span data-ttu-id="6dadd-2729">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2729">3</span></span>

<span data-ttu-id="6dadd-2730">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2730">4</span></span>

<span data-ttu-id="6dadd-2731">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2731">5</span></span>

<span data-ttu-id="6dadd-2732">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2732">6</span></span>

<span data-ttu-id="6dadd-2733">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2733">7</span></span>

<span data-ttu-id="6dadd-2734">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2734">8</span></span>

<span data-ttu-id="6dadd-2735">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2735">9</span></span>

<span data-ttu-id="6dadd-2736">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2736">3</span></span><br/> <span data-ttu-id="6dadd-2737">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2737">0</span></span><br/>

<span data-ttu-id="6dadd-2738">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2738">1</span></span>

<span data-ttu-id="6dadd-2739">cbStruct</span><span class="sxs-lookup"><span data-stu-id="6dadd-2739">cbStruct</span></span>

<span data-ttu-id="6dadd-2740">cWordList</span><span class="sxs-lookup"><span data-stu-id="6dadd-2740">cWordList</span></span>

<span data-ttu-id="6dadd-2741">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="6dadd-2741">cPersistentIndex</span></span>

<span data-ttu-id="6dadd-2742">cQueries</span><span class="sxs-lookup"><span data-stu-id="6dadd-2742">cQueries</span></span>

<span data-ttu-id="6dadd-2743">cDocuments</span><span class="sxs-lookup"><span data-stu-id="6dadd-2743">cDocuments</span></span>

<span data-ttu-id="6dadd-2744">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="6dadd-2744">cFreshTest</span></span>

<span data-ttu-id="6dadd-2745">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="6dadd-2745">dwMergeProgress</span></span>

<span data-ttu-id="6dadd-2746">Imóveis</span><span class="sxs-lookup"><span data-stu-id="6dadd-2746">eState</span></span>

<span data-ttu-id="6dadd-2747">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="6dadd-2747">cFilteredDocuments</span></span>

<span data-ttu-id="6dadd-2748">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="6dadd-2748">cTotalDocuments</span></span>

<span data-ttu-id="6dadd-2749">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="6dadd-2749">cPendingScans</span></span>

<span data-ttu-id="6dadd-2750">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="6dadd-2750">dwIndexSize</span></span>

<span data-ttu-id="6dadd-2751">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="6dadd-2751">cUniqueKeys</span></span>

<span data-ttu-id="6dadd-2752">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="6dadd-2752">cSecQDocuments</span></span>

<span data-ttu-id="6dadd-2753">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="6dadd-2753">dwPropCacheSize</span></span>



 

<span data-ttu-id="6dadd-2754">**cbStruct**: um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2754">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="6dadd-2755">O tamanho em bytes desta mensagem (excluindo o cabeçalho comum).</span><span class="sxs-lookup"><span data-stu-id="6dadd-2755">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="6dadd-2756">DEVE ser definido como 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2756">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="6dadd-2757">**cWordList**: um inteiro de 32 bits sem sinal indicando a contagem de índices iniciais criados para documentos indexados recentemente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2757">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="6dadd-2758">**cPersistentIndex**: um inteiro de 32 bits sem sinal indicando a contagem de índices persistentes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2758">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="6dadd-2759">**cQueries**: um inteiro de 32 bits sem sinal indicando um número de consultas em execução ativamente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2759">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="6dadd-2760">**cDocuments**: um inteiro de 32 bits sem sinal indicando o número total de documentos aguardando para serem indexados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2760">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="6dadd-2761">**cFreshTest**: um inteiro sem sinal de 32 bits que indica o número de documentos exclusivos com informações em índices que não são totalmente otimizados para desempenho.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2761">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="6dadd-2762">**dwMergeProgress**: inteiro de 32 bits sem sinal especificando a porcentagem de conclusão da otimização total atual de índices, se a otimização estiver em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2762">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="6dadd-2763">DEVE ser menor ou igual a 100.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2763">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="6dadd-2764">**imobiliária**: estado da indexação de conteúdo, conforme fornecido por uma ou mais das \_ constantes de estado de CI \_ \* , definidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2764">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="6dadd-2765">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-2765">Value</span></span>                                         | <span data-ttu-id="6dadd-2766">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-2766">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-2767">\_Mesclagem de sombra de estado de CI \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-2767">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="6dadd-2768">O serviço de indexação está no processo de otimização de alguns dos índices para reduzir o uso de memória e melhorar o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2768">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="6dadd-2769">\_ \_ Mesclagem mestra de estado CI \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-2769">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="6dadd-2770">O serviço de indexação está no processo de Otimização total para todos os índices.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2770">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6dadd-2771">\_Exame de conteúdo de estado CI \_ \_ \_ necessário 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-2771">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="6dadd-2772">Alguns documentos no índice foram alterados e o serviço de indexação precisa determinar quais foram adicionados, alterados ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2772">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6dadd-2773">CI \_ estado \_ recozimento \_ mesclar 0x00000008</span><span class="sxs-lookup"><span data-stu-id="6dadd-2773">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="6dadd-2774">O serviço de indexação está no processo de otimização de índices para reduzir o uso de memória e melhorar o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2774">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="6dadd-2775">Esse processo é mais abrangente do que aquele identificado pelo valor de \_ mesclagem de sombra de estado de CI \_ \_ , mas não é tão abrangente quanto o especificado pelo \_ valor de \_ mesclagem mestre de estado CI \_ .</span><span class="sxs-lookup"><span data-stu-id="6dadd-2775">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="6dadd-2776">Essas otimizações são específicas da implementação, pois dependem da maneira como os dados são armazenados internamente; as otimizações não afetam o protocolo de nenhuma forma que não seja o tempo de resposta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2776">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="6dadd-2777">\_Verificação de estado CI \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dadd-2777">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="6dadd-2778">O serviço de indexação está examinando um diretório ou um conjunto de diretórios para ver se algum arquivo foi adicionado, excluído ou atualizado desde a última vez em que o diretório foi indexado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2778">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6dadd-2779">O \_ estado de CI \_ recuperando 0x00000020</span><span class="sxs-lookup"><span data-stu-id="6dadd-2779">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="6dadd-2780">O serviço está sendo iniciado a partir do último estado salvo e está no processo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2780">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6dadd-2781">\_0x00000080 de \_ memória insuficiente do estado de CI \_</span><span class="sxs-lookup"><span data-stu-id="6dadd-2781">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="6dadd-2782">A maior parte da memória virtual do servidor está em uso.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2782">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6dadd-2783">Estado de CI de \_ \_ alta \_ e/s 0x00000100</span><span class="sxs-lookup"><span data-stu-id="6dadd-2783">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="6dadd-2784">O nível de atividade de entrada/saída (e/s) no servidor é relativamente alto.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2784">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6dadd-2785">\_Mesclagem mestra de estado CI em \_ \_ \_ pausa 0x00000200</span><span class="sxs-lookup"><span data-stu-id="6dadd-2785">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="6dadd-2786">O processo de otimização completa de todos os índices que estavam em andamento foi pausado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2786">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="6dadd-2787">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2787">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6dadd-2788">\_ \_ 0x00000400 somente leitura do estado CI \_</span><span class="sxs-lookup"><span data-stu-id="6dadd-2788">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="6dadd-2789">A parte do serviço de indexação que obtém novos documentos para o índice foi pausada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2789">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="6dadd-2790">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6dadd-2791">Estado de CI de \_ \_ energia da bateria \_ 0x00000800</span><span class="sxs-lookup"><span data-stu-id="6dadd-2791">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="6dadd-2792">A parte do serviço de indexação que obtém novos documentos para o índice foi pausada para conservar o tempo de vida da bateria, mas ainda responde às consultas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2792">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="6dadd-2793">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6dadd-2794">0x00001000 de usuário de estado de CI \_ \_ \_ ativo</span><span class="sxs-lookup"><span data-stu-id="6dadd-2794">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="6dadd-2795">A parte do serviço de indexação que obtém novos documentos para o índice foi pausada devido à alta atividade pelo usuário (teclado ou mouse), mas ainda responde às consultas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2795">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="6dadd-2796">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="6dadd-2797">Estado de CI \_ \_ iniciando 0x00002000</span><span class="sxs-lookup"><span data-stu-id="6dadd-2797">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="6dadd-2798">O serviço está iniciando.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2798">The service is starting.</span></span> <span data-ttu-id="6dadd-2799">As consultas podem ser executadas, mas a verificação e a notificação ainda não foram habilitadas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2799">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="6dadd-2800">Isso é fornecido apenas para fins informativos e não afeta CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2800">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="6dadd-2801">\_Estado CI \_ lendo \_ USNs 0x00004000</span><span class="sxs-lookup"><span data-stu-id="6dadd-2801">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="6dadd-2802">O serviço não leu o log mantido pelo sistema de arquivos para manter o controle das alterações em arquivos ou diretórios em um volume, de modo que o índice pode não estar atualizado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2802">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="6dadd-2803">**cFilteredDocuments**: um inteiro de 32 bits sem sinal indicando o número de documentos indexados desde que a indexação de conteúdo foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2803">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="6dadd-2804">**cTotalDocuments**: um inteiro de 32 bits sem sinal indicando o número total de documentos no sistema.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2804">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="6dadd-2805">**cPendingScans**: um inteiro de 32 bits sem sinal indicando o número de operações pendentes de indexação de alto nível.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2805">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="6dadd-2806">O significado desse valor é específico do provedor, mas números maiores são esperados para indicar que mais indexação permanece.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2806">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="6dadd-2807">*Comportamento do Windows*: esse valor geralmente é zero, exceto imediatamente após a indexação ter sido iniciada ou após o estouro de uma fila de notificação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2807">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="6dadd-2808">**dwIndexSize**: um inteiro de 32 bits sem sinal indicando o tamanho, em megabytes, do índice (excluindo o cache de propriedades).</span><span class="sxs-lookup"><span data-stu-id="6dadd-2808">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="6dadd-2809">**cUniqueKeys**: um inteiro de 32 bits sem sinal indicando o número aproximado de chaves exclusivas no catálogo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2809">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="6dadd-2810">**cSecQDocuments**: um inteiro de 32 bits sem sinal indicando o número de documentos que o serviço de indexação tentará indexar devido a uma falha durante a tentativa de indexação inicial.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2810">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="6dadd-2811">**dwPropCacheSize**: um inteiro de 32 bits sem sinal indicando o tamanho, em megabytes, do cache de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2811">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="6dadd-2812">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2812">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="6dadd-2813">A mensagem CPMSetCatStateIn define o estado de um catálogo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2813">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="6dadd-2814">O formato da mensagem CPMSetCatStateIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2814">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-2815">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2815">0</span></span>

<span data-ttu-id="6dadd-2816">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2816">1</span></span>

<span data-ttu-id="6dadd-2817">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2817">2</span></span>

<span data-ttu-id="6dadd-2818">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2818">3</span></span>

<span data-ttu-id="6dadd-2819">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2819">4</span></span>

<span data-ttu-id="6dadd-2820">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2820">5</span></span>

<span data-ttu-id="6dadd-2821">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2821">6</span></span>

<span data-ttu-id="6dadd-2822">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2822">7</span></span>

<span data-ttu-id="6dadd-2823">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2823">8</span></span>

<span data-ttu-id="6dadd-2824">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2824">9</span></span>

<span data-ttu-id="6dadd-2825">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2825">1</span></span><br/> <span data-ttu-id="6dadd-2826">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2826">0</span></span><br/>

<span data-ttu-id="6dadd-2827">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2827">1</span></span>

<span data-ttu-id="6dadd-2828">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2828">2</span></span>

<span data-ttu-id="6dadd-2829">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2829">3</span></span>

<span data-ttu-id="6dadd-2830">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2830">4</span></span>

<span data-ttu-id="6dadd-2831">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2831">5</span></span>

<span data-ttu-id="6dadd-2832">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2832">6</span></span>

<span data-ttu-id="6dadd-2833">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2833">7</span></span>

<span data-ttu-id="6dadd-2834">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2834">8</span></span>

<span data-ttu-id="6dadd-2835">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2835">9</span></span>

<span data-ttu-id="6dadd-2836">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2836">2</span></span><br/> <span data-ttu-id="6dadd-2837">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2837">0</span></span><br/>

<span data-ttu-id="6dadd-2838">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2838">1</span></span>

<span data-ttu-id="6dadd-2839">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2839">2</span></span>

<span data-ttu-id="6dadd-2840">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2840">3</span></span>

<span data-ttu-id="6dadd-2841">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2841">4</span></span>

<span data-ttu-id="6dadd-2842">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2842">5</span></span>

<span data-ttu-id="6dadd-2843">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2843">6</span></span>

<span data-ttu-id="6dadd-2844">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2844">7</span></span>

<span data-ttu-id="6dadd-2845">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2845">8</span></span>

<span data-ttu-id="6dadd-2846">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2846">9</span></span>

<span data-ttu-id="6dadd-2847">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2847">3</span></span><br/> <span data-ttu-id="6dadd-2848">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2848">0</span></span><br/>

<span data-ttu-id="6dadd-2849">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2849">1</span></span>

<span data-ttu-id="6dadd-2850">\_partID</span><span class="sxs-lookup"><span data-stu-id="6dadd-2850">\_partID</span></span>

<span data-ttu-id="6dadd-2851">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="6dadd-2851">\_dwNewState</span></span>

<span data-ttu-id="6dadd-2852">\_CatName (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2852">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="6dadd-2853">**\_ partID**: DEVE ser definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2853">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="6dadd-2854">**\_ dwNewState**: DEVE ser definido como um dos seguintes valores, indicando o novo estado do catálogo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2854">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="6dadd-2855">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-2855">Value</span></span>                         | <span data-ttu-id="6dadd-2856">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-2856">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-2857">CICAT \_ PARADO 0X00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-2857">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="6dadd-2858">O catálogo é interrompido.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2858">The catalog is stopped.</span></span> <span data-ttu-id="6dadd-2859">Esse estado significa que nenhum novo arquivo deve ser indexado e nenhuma consulta de pesquisa deve ser processada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2859">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="6dadd-2860">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-2860">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="6dadd-2861">O catálogo é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2861">The catalog is read-only.</span></span> <span data-ttu-id="6dadd-2862">Nenhum arquivo novo deve ser indexado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2862">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="6dadd-2863">CICAT \_ WRITABLE 0X00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-2863">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="6dadd-2864">O catálogo pode ser escrito.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2864">The catalog is writable.</span></span> <span data-ttu-id="6dadd-2865">Novos arquivos podem ser indexados e as consultas de pesquisa devem ser processadas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2865">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="6dadd-2866">CICAT \_ NO \_ QUERY 0X00000008</span><span class="sxs-lookup"><span data-stu-id="6dadd-2866">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="6dadd-2867">O catálogo não está disponível para consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2867">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="6dadd-2868">CICAT \_ GET \_ STATE 0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dadd-2868">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="6dadd-2869">O estado do catálogo não deve ser alterado, apenas recuperado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2869">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="6dadd-2870">CICAT \_ ALL \_ OPENED 0X00000020</span><span class="sxs-lookup"><span data-stu-id="6dadd-2870">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="6dadd-2871">Uma verificação para ver se todos os catálogos foram iniciados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2871">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="6dadd-2872">Nesse caso, o campo dwOldState enviado na resposta CPMSetCatStateOut para essa mensagem \_ será relatado como diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2872">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="6dadd-2873">**\_ CatName:** o nome do catálogo que deve ter seu estado modificado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2873">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="6dadd-2874">O nome DEVE ser uma cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2874">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="6dadd-2875">Esse campo DEVERÁ ser omitido se \_ dwNewState estiver definido como CICAT \_ ALL \_ OPENED.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2875">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="6dadd-2876">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-2876">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="6dadd-2877">A mensagem CPMSetCatStateOut é uma resposta a uma mensagem CPMSetCatStateIn com o estado antigo do catálogo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2877">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="6dadd-2878">O formato da mensagem CPMSetCatStateOut que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2878">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-2879">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2879">0</span></span>

<span data-ttu-id="6dadd-2880">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2880">1</span></span>

<span data-ttu-id="6dadd-2881">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2881">2</span></span>

<span data-ttu-id="6dadd-2882">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2882">3</span></span>

<span data-ttu-id="6dadd-2883">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2883">4</span></span>

<span data-ttu-id="6dadd-2884">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2884">5</span></span>

<span data-ttu-id="6dadd-2885">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2885">6</span></span>

<span data-ttu-id="6dadd-2886">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2886">7</span></span>

<span data-ttu-id="6dadd-2887">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2887">8</span></span>

<span data-ttu-id="6dadd-2888">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2888">9</span></span>

<span data-ttu-id="6dadd-2889">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2889">1</span></span><br/> <span data-ttu-id="6dadd-2890">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2890">0</span></span><br/>

<span data-ttu-id="6dadd-2891">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2891">1</span></span>

<span data-ttu-id="6dadd-2892">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2892">2</span></span>

<span data-ttu-id="6dadd-2893">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2893">3</span></span>

<span data-ttu-id="6dadd-2894">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2894">4</span></span>

<span data-ttu-id="6dadd-2895">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2895">5</span></span>

<span data-ttu-id="6dadd-2896">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2896">6</span></span>

<span data-ttu-id="6dadd-2897">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2897">7</span></span>

<span data-ttu-id="6dadd-2898">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2898">8</span></span>

<span data-ttu-id="6dadd-2899">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2899">9</span></span>

<span data-ttu-id="6dadd-2900">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2900">2</span></span><br/> <span data-ttu-id="6dadd-2901">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2901">0</span></span><br/>

<span data-ttu-id="6dadd-2902">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2902">1</span></span>

<span data-ttu-id="6dadd-2903">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2903">2</span></span>

<span data-ttu-id="6dadd-2904">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2904">3</span></span>

<span data-ttu-id="6dadd-2905">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2905">4</span></span>

<span data-ttu-id="6dadd-2906">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2906">5</span></span>

<span data-ttu-id="6dadd-2907">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2907">6</span></span>

<span data-ttu-id="6dadd-2908">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2908">7</span></span>

<span data-ttu-id="6dadd-2909">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2909">8</span></span>

<span data-ttu-id="6dadd-2910">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2910">9</span></span>

<span data-ttu-id="6dadd-2911">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2911">3</span></span><br/> <span data-ttu-id="6dadd-2912">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2912">0</span></span><br/>

<span data-ttu-id="6dadd-2913">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2913">1</span></span>

<span data-ttu-id="6dadd-2914">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="6dadd-2914">\_dwOldState</span></span>



 

<span data-ttu-id="6dadd-2915">**\_ dwOldState:** um dos valores a seguir, indicando o estado antigo do catálogo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2915">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="6dadd-2916">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-2916">Value</span></span>                       | <span data-ttu-id="6dadd-2917">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-2917">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="6dadd-2918">CICAT \_ PARADO 0X00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-2918">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="6dadd-2919">O catálogo é interrompido.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2919">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="6dadd-2920">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-2920">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="6dadd-2921">O catálogo é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2921">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="6dadd-2922">CICAT \_ gravável 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-2922">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="6dadd-2923">O catálogo é gravável.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2923">The catalog is writable.</span></span>                   |
| <span data-ttu-id="6dadd-2924">CICAT \_ sem \_ 0x00000008 de consulta</span><span class="sxs-lookup"><span data-stu-id="6dadd-2924">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="6dadd-2925">O catálogo não está disponível para consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2925">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="6dadd-2926">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2926">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="6dadd-2927">A mensagem CPMUpdateDocumentsIn direciona o servidor para indexar o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2927">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="6dadd-2928">O servidor responderá com o cabeçalho da mensagem CPMUpdateDocumentsOut, com os resultados da solicitação contida no \_ campo status do cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2928">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="6dadd-2929">O formato da mensagem CPMUpdateDocumentsIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2929">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-2930">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2930">0</span></span>

<span data-ttu-id="6dadd-2931">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2931">1</span></span>

<span data-ttu-id="6dadd-2932">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2932">2</span></span>

<span data-ttu-id="6dadd-2933">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2933">3</span></span>

<span data-ttu-id="6dadd-2934">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2934">4</span></span>

<span data-ttu-id="6dadd-2935">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2935">5</span></span>

<span data-ttu-id="6dadd-2936">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2936">6</span></span>

<span data-ttu-id="6dadd-2937">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2937">7</span></span>

<span data-ttu-id="6dadd-2938">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2938">8</span></span>

<span data-ttu-id="6dadd-2939">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2939">9</span></span>

<span data-ttu-id="6dadd-2940">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2940">1</span></span><br/> <span data-ttu-id="6dadd-2941">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2941">0</span></span><br/>

<span data-ttu-id="6dadd-2942">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2942">1</span></span>

<span data-ttu-id="6dadd-2943">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2943">2</span></span>

<span data-ttu-id="6dadd-2944">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2944">3</span></span>

<span data-ttu-id="6dadd-2945">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2945">4</span></span>

<span data-ttu-id="6dadd-2946">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2946">5</span></span>

<span data-ttu-id="6dadd-2947">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2947">6</span></span>

<span data-ttu-id="6dadd-2948">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2948">7</span></span>

<span data-ttu-id="6dadd-2949">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2949">8</span></span>

<span data-ttu-id="6dadd-2950">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2950">9</span></span>

<span data-ttu-id="6dadd-2951">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2951">2</span></span><br/> <span data-ttu-id="6dadd-2952">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2952">0</span></span><br/>

<span data-ttu-id="6dadd-2953">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2953">1</span></span>

<span data-ttu-id="6dadd-2954">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2954">2</span></span>

<span data-ttu-id="6dadd-2955">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2955">3</span></span>

<span data-ttu-id="6dadd-2956">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2956">4</span></span>

<span data-ttu-id="6dadd-2957">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2957">5</span></span>

<span data-ttu-id="6dadd-2958">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2958">6</span></span>

<span data-ttu-id="6dadd-2959">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2959">7</span></span>

<span data-ttu-id="6dadd-2960">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-2960">8</span></span>

<span data-ttu-id="6dadd-2961">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-2961">9</span></span>

<span data-ttu-id="6dadd-2962">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2962">3</span></span><br/> <span data-ttu-id="6dadd-2963">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2963">0</span></span><br/>

<span data-ttu-id="6dadd-2964">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2964">1</span></span>

<span data-ttu-id="6dadd-2965">\_sinalizador (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2965">\_flag (optional)</span></span>

<span data-ttu-id="6dadd-2966">\_fRootPath (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2966">\_fRootPath (optional)</span></span>

<span data-ttu-id="6dadd-2967">RootPath (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-2967">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="6dadd-2968">**\_ sinalizador**: o tipo de atualização a ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2968">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="6dadd-2969">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2969">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="6dadd-2970">Esse campo deve ser definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2970">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="6dadd-2971">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-2971">Value</span></span>                  | <span data-ttu-id="6dadd-2972">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-2972">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="6dadd-2973">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-2973">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="6dadd-2974">Uma atualização incremental deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2974">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="6dadd-2975">UPD \_ completo 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-2975">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="6dadd-2976">Uma atualização completa deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2976">A full update is to be performed.</span></span>         |
| <span data-ttu-id="6dadd-2977">UPD \_ init 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-2977">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="6dadd-2978">Uma nova inicialização deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2978">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="6dadd-2979">**\_ fRootPath**: um valor booliano que indica se o campo RootPath especifica um caminho no qual executar a atualização.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2979">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="6dadd-2980">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2980">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="6dadd-2981">Esse campo deve ser definido como 0x00000001 ou 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2981">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="6dadd-2982">Se definido como 0x00000001, um caminho no qual executar a atualização será incluído em RootPath.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2982">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="6dadd-2983">Se definido como 0x00000000, a atualização será executada em todos os caminhos indexados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2983">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="6dadd-2984">**RootPath**: o nome do caminho a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2984">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="6dadd-2985">Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2985">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="6dadd-2986">O nome deve ser uma cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2986">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="6dadd-2987">Esse campo deve ser omitido se \_ fRootPath for definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2987">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="6dadd-2988">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-2988">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="6dadd-2989">A mensagem CPMForceMergeIn solicita que um servidor execute qualquer manutenção necessária para melhorar o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2989">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="6dadd-2990">O servidor responderá com o cabeçalho da mensagem CPMForceMergeIn, com os resultados da solicitação contida no \_ campo status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-2990">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="6dadd-2991">O formato da mensagem CPMForceMergeIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-2991">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-2992">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-2992">0</span></span>

<span data-ttu-id="6dadd-2993">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-2993">1</span></span>

<span data-ttu-id="6dadd-2994">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-2994">2</span></span>

<span data-ttu-id="6dadd-2995">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-2995">3</span></span>

<span data-ttu-id="6dadd-2996">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-2996">4</span></span>

<span data-ttu-id="6dadd-2997">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-2997">5</span></span>

<span data-ttu-id="6dadd-2998">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-2998">6</span></span>

<span data-ttu-id="6dadd-2999">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-2999">7</span></span>

<span data-ttu-id="6dadd-3000">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3000">8</span></span>

<span data-ttu-id="6dadd-3001">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3001">9</span></span>

<span data-ttu-id="6dadd-3002">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3002">1</span></span><br/> <span data-ttu-id="6dadd-3003">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3003">0</span></span><br/>

<span data-ttu-id="6dadd-3004">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3004">1</span></span>

<span data-ttu-id="6dadd-3005">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3005">2</span></span>

<span data-ttu-id="6dadd-3006">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3006">3</span></span>

<span data-ttu-id="6dadd-3007">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3007">4</span></span>

<span data-ttu-id="6dadd-3008">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3008">5</span></span>

<span data-ttu-id="6dadd-3009">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3009">6</span></span>

<span data-ttu-id="6dadd-3010">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3010">7</span></span>

<span data-ttu-id="6dadd-3011">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3011">8</span></span>

<span data-ttu-id="6dadd-3012">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3012">9</span></span>

<span data-ttu-id="6dadd-3013">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3013">2</span></span><br/> <span data-ttu-id="6dadd-3014">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3014">0</span></span><br/>

<span data-ttu-id="6dadd-3015">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3015">1</span></span>

<span data-ttu-id="6dadd-3016">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3016">2</span></span>

<span data-ttu-id="6dadd-3017">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3017">3</span></span>

<span data-ttu-id="6dadd-3018">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3018">4</span></span>

<span data-ttu-id="6dadd-3019">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3019">5</span></span>

<span data-ttu-id="6dadd-3020">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3020">6</span></span>

<span data-ttu-id="6dadd-3021">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3021">7</span></span>

<span data-ttu-id="6dadd-3022">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3022">8</span></span>

<span data-ttu-id="6dadd-3023">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3023">9</span></span>

<span data-ttu-id="6dadd-3024">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3024">3</span></span><br/> <span data-ttu-id="6dadd-3025">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3025">0</span></span><br/>

<span data-ttu-id="6dadd-3026">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3026">1</span></span>

<span data-ttu-id="6dadd-3027">\_partid (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3027">\_partID (optional)</span></span>



 

<span data-ttu-id="6dadd-3028">**\_ partid**: esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3028">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="6dadd-3029">Quando esse campo estiver presente, ele deverá ser definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3029">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="6dadd-3030">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3030">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="6dadd-3031">A mensagem CPMConnectIn inicia uma sessão entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3031">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="6dadd-3032">O formato da mensagem CPMConnectIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3032">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3033">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3033">0</span></span>

<span data-ttu-id="6dadd-3034">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3034">1</span></span>

<span data-ttu-id="6dadd-3035">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3035">2</span></span>

<span data-ttu-id="6dadd-3036">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3036">3</span></span>

<span data-ttu-id="6dadd-3037">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3037">4</span></span>

<span data-ttu-id="6dadd-3038">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3038">5</span></span>

<span data-ttu-id="6dadd-3039">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3039">6</span></span>

<span data-ttu-id="6dadd-3040">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3040">7</span></span>

<span data-ttu-id="6dadd-3041">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3041">8</span></span>

<span data-ttu-id="6dadd-3042">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3042">9</span></span>

<span data-ttu-id="6dadd-3043">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3043">1</span></span><br/> <span data-ttu-id="6dadd-3044">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3044">0</span></span><br/>

<span data-ttu-id="6dadd-3045">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3045">1</span></span>

<span data-ttu-id="6dadd-3046">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3046">2</span></span>

<span data-ttu-id="6dadd-3047">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3047">3</span></span>

<span data-ttu-id="6dadd-3048">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3048">4</span></span>

<span data-ttu-id="6dadd-3049">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3049">5</span></span>

<span data-ttu-id="6dadd-3050">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3050">6</span></span>

<span data-ttu-id="6dadd-3051">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3051">7</span></span>

<span data-ttu-id="6dadd-3052">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3052">8</span></span>

<span data-ttu-id="6dadd-3053">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3053">9</span></span>

<span data-ttu-id="6dadd-3054">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3054">2</span></span><br/> <span data-ttu-id="6dadd-3055">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3055">0</span></span><br/>

<span data-ttu-id="6dadd-3056">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3056">1</span></span>

<span data-ttu-id="6dadd-3057">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3057">2</span></span>

<span data-ttu-id="6dadd-3058">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3058">3</span></span>

<span data-ttu-id="6dadd-3059">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3059">4</span></span>

<span data-ttu-id="6dadd-3060">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3060">5</span></span>

<span data-ttu-id="6dadd-3061">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3061">6</span></span>

<span data-ttu-id="6dadd-3062">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3062">7</span></span>

<span data-ttu-id="6dadd-3063">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3063">8</span></span>

<span data-ttu-id="6dadd-3064">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3064">9</span></span>

<span data-ttu-id="6dadd-3065">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3065">3</span></span><br/> <span data-ttu-id="6dadd-3066">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3066">0</span></span><br/>

<span data-ttu-id="6dadd-3067">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3067">1</span></span>

<span data-ttu-id="6dadd-3068">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="6dadd-3068">\_iClientVersion</span></span>

<span data-ttu-id="6dadd-3069">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="6dadd-3069">\_fClientIsRemote</span></span>

<span data-ttu-id="6dadd-3070">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3070">\_cbBlob1</span></span>

<span data-ttu-id="6dadd-3071">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3071">\_cbBlob2</span></span>

<span data-ttu-id="6dadd-3072">\_margem</span><span class="sxs-lookup"><span data-stu-id="6dadd-3072">\_padding</span></span>

<span data-ttu-id="6dadd-3073">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3073">...</span></span>

<span data-ttu-id="6dadd-3074">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3074">...</span></span>

<span data-ttu-id="6dadd-3075">MachineName</span><span class="sxs-lookup"><span data-stu-id="6dadd-3075">MachineName</span></span>

<span data-ttu-id="6dadd-3076">... Ela</span><span class="sxs-lookup"><span data-stu-id="6dadd-3076">... (variable)</span></span>

<span data-ttu-id="6dadd-3077">UserName</span><span class="sxs-lookup"><span data-stu-id="6dadd-3077">UserName</span></span>

<span data-ttu-id="6dadd-3078">... Ela</span><span class="sxs-lookup"><span data-stu-id="6dadd-3078">... (variable)</span></span>

<span data-ttu-id="6dadd-3079">\_paddingcPropSets (opcional, variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3079">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="6dadd-3080">cPropSets</span><span class="sxs-lookup"><span data-stu-id="6dadd-3080">cPropSets</span></span>

<span data-ttu-id="6dadd-3081">PropertySet1 (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3081">PropertySet1 (variable)</span></span>

<span data-ttu-id="6dadd-3082">PropertySet2 (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3082">PropertySet2 (variable)</span></span>

<span data-ttu-id="6dadd-3083">\_paddingExtPropset (opcional, variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3083">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="6dadd-3084">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="6dadd-3084">cExtPropSet</span></span>

<span data-ttu-id="6dadd-3085">aPropertySets (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3085">aPropertySets (variable)</span></span>



 

<span data-ttu-id="6dadd-3086">**\_ iClientVersion**: um inteiro de 32 bits que indica se o servidor deve validar o valor de soma de verificação especificado no \_ campo ulChecksum dos cabeçalhos de mensagem para as mensagens enviadas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3086">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="6dadd-3087">Se o \_ campo iClientVersion for definido como 0x00000008 ou superior, o servidor deverá validar o \_ valor do campo ulChecksum para as seguintes mensagens:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3087">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="6dadd-3088">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3088">CPMConnectIn</span></span>
-   <span data-ttu-id="6dadd-3089">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3089">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="6dadd-3090">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3090">CPMFetchValueIn</span></span>
-   <span data-ttu-id="6dadd-3091">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3091">CPMGetRowsIn</span></span>
-   <span data-ttu-id="6dadd-3092">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3092">CPMSetBindingsIn</span></span>

<span data-ttu-id="6dadd-3093">Para obter detalhes sobre como o servidor valida o valor especificado pelo cliente no campo ulChecksum para as mensagens listadas acima, consulte a seção 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3093">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="6dadd-3094">Se o valor for maior que 0x00000008, o cliente será considerado capaz de manipular deslocamentos de 64 bits em mensagens CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3094">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="6dadd-3095">Consulte a seção 2.2.3.16 para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3095">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="6dadd-3096">*Comportamento do Windows: em clientes Windows, o iClientVersion é definido da seguinte maneira*:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3096">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="6dadd-3097">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3097">Value</span></span>      | <span data-ttu-id="6dadd-3098">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-3098">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="6dadd-3099">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6dadd-3099">0x00000005</span></span> | <span data-ttu-id="6dadd-3100">O sistema operacional do cliente é o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3100">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="6dadd-3101">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6dadd-3101">0x00000008</span></span> | <span data-ttu-id="6dadd-3102">O sistema operacional do cliente é o Windows XP de 32 bits ou o Windows Server 2003 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3102">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="6dadd-3103">0x00010008</span><span class="sxs-lookup"><span data-stu-id="6dadd-3103">0x00010008</span></span> | <span data-ttu-id="6dadd-3104">O sistema operacional do cliente é o Windows XP de 64 bits ou o Windows Server 2003 de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3104">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="6dadd-3105">\_**fClientIsRemote**: um valor booliano que indica se o cliente está sendo executado em um computador diferente do servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3105">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="6dadd-3106">DEVE ser definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3106">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="6dadd-3107">\_**cbBlob1**: um inteiro de 32 bits sem sinal indicando o tamanho em bytes dos campos CPropSet, PropertySet1 e PropertySet2, combinados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3107">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="6dadd-3108">\_**cbBlob2**: um inteiro de 32 bits sem sinal indicando o tamanho em bytes dos campos CExPropSet e aPropertySet, combinados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3108">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="6dadd-3109">\_**preenchimento**: 12 bytes de preenchimento que podem conter valores arbitrários e devem ser ignorados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3109">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="6dadd-3110">**MachineName**: o nome do computador do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3110">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="6dadd-3111">A cadeia de caracteres de nome deve ser uma matriz com terminação nula de menos de 512 caracteres Unicode, incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3111">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="6dadd-3112">**Username**: uma cadeia de caracteres que representa o nome de usuário da pessoa que está executando o aplicativo que invocou esse protocolo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3112">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="6dadd-3113">A cadeia de caracteres de nome deve ser uma matriz com terminação nula de menos de 512 caracteres Unicode quando concatenada com MachineName.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3113">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="6dadd-3114">**\_ paddingcPropSets**: esse campo deve ter de 0 a 7 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3114">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="6dadd-3115">O número de bytes deve ser o número necessário para fazer o deslocamento de bytes do campo cPropSets do início da mensagem que contém essa estrutura ser um múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3115">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="6dadd-3116">O valor dos bytes pode ser qualquer valor arbitrário e deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3116">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-3117">**cPropSets**: um inteiro de 32 bits sem sinal indicando o número de estruturas CDbPropSet após este campo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3117">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="6dadd-3118">Esse valor deve ser definido como 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3118">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="6dadd-3119">**PropertySet1**: uma estrutura CDbPropSet com guidPropertySet que contém DBPROPSET \_ FSCIFRMWRK \_ ext (consulte A seção 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="6dadd-3119">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="6dadd-3120">**PropertySet2**: uma estrutura CDbPropSet com guidPropertySet que contém DBPROPSET \_ CIFRMWRKCORE \_ ext (consulte A seção 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="6dadd-3120">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="6dadd-3121">\_**PaddingExtPropset**: esse campo deve ter de 0 a 7 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3121">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="6dadd-3122">O número de bytes deve ser o número necessário para fazer o deslocamento de bytes do campo cExtPropSets do início da mensagem que contém essa estrutura ser um múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3122">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="6dadd-3123">O valor dos bytes pode ser qualquer valor arbitrário e DEVE ser ignorado pelo receptor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3123">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-3124">**cExtPropSet:** um inteiro sem sinal de 32 bits que indica o número de estruturas CDbPropSet após esse campo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3124">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="6dadd-3125">**aPropertySets:** uma matriz de estruturas CDbPropSet especificando outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3125">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="6dadd-3126">O número de elementos nessa matriz DEVE ser igual a cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3126">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="6dadd-3127">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-3127">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="6dadd-3128">A mensagem CPMConnectOut contém uma resposta a uma mensagem CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3128">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="6dadd-3129">O formato da mensagem CPMConnectOut que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3129">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3130">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3130">0</span></span>

<span data-ttu-id="6dadd-3131">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3131">1</span></span>

<span data-ttu-id="6dadd-3132">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3132">2</span></span>

<span data-ttu-id="6dadd-3133">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3133">3</span></span>

<span data-ttu-id="6dadd-3134">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3134">4</span></span>

<span data-ttu-id="6dadd-3135">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3135">5</span></span>

<span data-ttu-id="6dadd-3136">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3136">6</span></span>

<span data-ttu-id="6dadd-3137">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3137">7</span></span>

<span data-ttu-id="6dadd-3138">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3138">8</span></span>

<span data-ttu-id="6dadd-3139">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3139">9</span></span>

<span data-ttu-id="6dadd-3140">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3140">1</span></span><br/> <span data-ttu-id="6dadd-3141">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3141">0</span></span><br/>

<span data-ttu-id="6dadd-3142">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3142">1</span></span>

<span data-ttu-id="6dadd-3143">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3143">2</span></span>

<span data-ttu-id="6dadd-3144">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3144">3</span></span>

<span data-ttu-id="6dadd-3145">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3145">4</span></span>

<span data-ttu-id="6dadd-3146">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3146">5</span></span>

<span data-ttu-id="6dadd-3147">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3147">6</span></span>

<span data-ttu-id="6dadd-3148">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3148">7</span></span>

<span data-ttu-id="6dadd-3149">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3149">8</span></span>

<span data-ttu-id="6dadd-3150">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3150">9</span></span>

<span data-ttu-id="6dadd-3151">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3151">2</span></span><br/> <span data-ttu-id="6dadd-3152">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3152">0</span></span><br/>

<span data-ttu-id="6dadd-3153">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3153">1</span></span>

<span data-ttu-id="6dadd-3154">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3154">2</span></span>

<span data-ttu-id="6dadd-3155">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3155">3</span></span>

<span data-ttu-id="6dadd-3156">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3156">4</span></span>

<span data-ttu-id="6dadd-3157">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3157">5</span></span>

<span data-ttu-id="6dadd-3158">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3158">6</span></span>

<span data-ttu-id="6dadd-3159">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3159">7</span></span>

<span data-ttu-id="6dadd-3160">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3160">8</span></span>

<span data-ttu-id="6dadd-3161">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3161">9</span></span>

<span data-ttu-id="6dadd-3162">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3162">3</span></span><br/> <span data-ttu-id="6dadd-3163">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3163">0</span></span><br/>

<span data-ttu-id="6dadd-3164">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3164">1</span></span>

<span data-ttu-id="6dadd-3165">\_Versão do servidor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3165">\_serverVersion</span></span>

<span data-ttu-id="6dadd-3166">\_reservado (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3166">\_reserved (variable)</span></span>



 

<span data-ttu-id="6dadd-3167">**\_ serverVersion:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-3167">**\_serverVersion**:</span></span>

<span data-ttu-id="6dadd-3168">Um inteiro de 32 bits, indicando se o servidor pode dar suporte a deslocamentos de 64 *bits.*</span><span class="sxs-lookup"><span data-stu-id="6dadd-3168">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="6dadd-3169">Consulte a seção 2.2.3.16 para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3169">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="6dadd-3170">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3170">Value</span></span>      | <span data-ttu-id="6dadd-3171">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-3171">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="6dadd-3172">0x00000007</span><span class="sxs-lookup"><span data-stu-id="6dadd-3172">0x00000007</span></span> | <span data-ttu-id="6dadd-3173">O servidor só pode enviar deslocamentos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3173">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="6dadd-3174">0x00010007</span><span class="sxs-lookup"><span data-stu-id="6dadd-3174">0x00010007</span></span> | <span data-ttu-id="6dadd-3175">O servidor pode enviar deslocamentos de 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3175">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="6dadd-3176">**\_ reservado:** Reservado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3176">**\_reserved**: Reserved.</span></span> <span data-ttu-id="6dadd-3177">O servidor PODE enviar um número arbitrário de valores arbitrários e o cliente DEVERÁ ignorar esses valores se estiver presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3177">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="6dadd-3178">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3178">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="6dadd-3179">A mensagem CPMCreateQueryIn cria uma nova consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3179">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="6dadd-3180">O formato da mensagem CPMCreateQueryIn que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3180">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3181">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3181">0</span></span>

<span data-ttu-id="6dadd-3182">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3182">1</span></span>

<span data-ttu-id="6dadd-3183">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3183">2</span></span>

<span data-ttu-id="6dadd-3184">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3184">3</span></span>

<span data-ttu-id="6dadd-3185">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3185">4</span></span>

<span data-ttu-id="6dadd-3186">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3186">5</span></span>

<span data-ttu-id="6dadd-3187">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3187">6</span></span>

<span data-ttu-id="6dadd-3188">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3188">7</span></span>

<span data-ttu-id="6dadd-3189">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3189">8</span></span>

<span data-ttu-id="6dadd-3190">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3190">9</span></span>

<span data-ttu-id="6dadd-3191">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3191">1</span></span><br/> <span data-ttu-id="6dadd-3192">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3192">0</span></span><br/>

<span data-ttu-id="6dadd-3193">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3193">1</span></span>

<span data-ttu-id="6dadd-3194">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3194">2</span></span>

<span data-ttu-id="6dadd-3195">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3195">3</span></span>

<span data-ttu-id="6dadd-3196">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3196">4</span></span>

<span data-ttu-id="6dadd-3197">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3197">5</span></span>

<span data-ttu-id="6dadd-3198">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3198">6</span></span>

<span data-ttu-id="6dadd-3199">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3199">7</span></span>

<span data-ttu-id="6dadd-3200">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3200">8</span></span>

<span data-ttu-id="6dadd-3201">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3201">9</span></span>

<span data-ttu-id="6dadd-3202">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3202">2</span></span><br/> <span data-ttu-id="6dadd-3203">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3203">0</span></span><br/>

<span data-ttu-id="6dadd-3204">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3204">1</span></span>

<span data-ttu-id="6dadd-3205">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3205">2</span></span>

<span data-ttu-id="6dadd-3206">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3206">3</span></span>

<span data-ttu-id="6dadd-3207">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3207">4</span></span>

<span data-ttu-id="6dadd-3208">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3208">5</span></span>

<span data-ttu-id="6dadd-3209">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3209">6</span></span>

<span data-ttu-id="6dadd-3210">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3210">7</span></span>

<span data-ttu-id="6dadd-3211">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3211">8</span></span>

<span data-ttu-id="6dadd-3212">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3212">9</span></span>

<span data-ttu-id="6dadd-3213">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3213">3</span></span><br/> <span data-ttu-id="6dadd-3214">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3214">0</span></span><br/>

<span data-ttu-id="6dadd-3215">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3215">1</span></span>

<span data-ttu-id="6dadd-3216">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6dadd-3216">Size</span></span>

<span data-ttu-id="6dadd-3217">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="6dadd-3217">CColumnSetPresent</span></span>

<span data-ttu-id="6dadd-3218">ColumnSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3218">ColumnSet (optional)</span></span>

<span data-ttu-id="6dadd-3219">... (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3219">... (variable)</span></span>

<span data-ttu-id="6dadd-3220">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3220">CRestrictionPresent.</span></span>

<span data-ttu-id="6dadd-3221">Restrição (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3221">Restriction (optional)</span></span>

<span data-ttu-id="6dadd-3222">... (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3222">... (variable)</span></span>

<span data-ttu-id="6dadd-3223">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="6dadd-3223">CSortSetPresent</span></span>

<span data-ttu-id="6dadd-3224">SortSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3224">SortSet (optional)</span></span>

<span data-ttu-id="6dadd-3225">... (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3225">... (variable)</span></span>

<span data-ttu-id="6dadd-3226">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="6dadd-3226">CCategorizationSetPresent</span></span>

<span data-ttu-id="6dadd-3227">CategorizationSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3227">CategorizationSet (optional)</span></span>

<span data-ttu-id="6dadd-3228">... (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3228">... (variable)</span></span>

<span data-ttu-id="6dadd-3229">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="6dadd-3229">RowSetProperties</span></span>

<span data-ttu-id="6dadd-3230">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3230">...</span></span>

<span data-ttu-id="6dadd-3231">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3231">...</span></span>

<span data-ttu-id="6dadd-3232">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3232">...</span></span>

<span data-ttu-id="6dadd-3233">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3233">...</span></span>

<span data-ttu-id="6dadd-3234">PidMapper (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3234">PidMapper (variable)</span></span>



 

<span data-ttu-id="6dadd-3235">**Tamanho:** um inteiro sem sinal de 32 bits que indica o número de bytes do início deste campo até o final da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3235">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="6dadd-3236">**CColumnSetPresent:** um campo de byte que indica se o campo ColumnSet está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3236">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="6dadd-3237">Esse campo DEVE ser definido como 0x01 ou 0x00.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3237">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="6dadd-3238">Se definido como 0x01 o campo CColumnSet DEVERÁ estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3238">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="6dadd-3239">Se definido como 0x00, ele DEVERÁ estar ausente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3239">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="6dadd-3240">**ColumnSet:** uma estrutura CColumnSet que contém os números de coluna em que as propriedades de CPidMapper devem ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3240">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="6dadd-3241">**CRestrictionPresent:** um campo de byte que indica se o campo Restrição está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3241">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="6dadd-3242">Se definido como qualquer valor que não seja zero, o campo Restrição DEVERÁ estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3242">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="6dadd-3243">Se definido como 0x00, a restrição DEVERÁ estar ausente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3243">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="6dadd-3244">**Restrição:** uma estrutura CRestriction que contém a árvore de comandos da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3244">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="6dadd-3245">**CSortSetPresent:** um campo de byte que indica se o campo SortSet está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3245">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="6dadd-3246">Se definido como qualquer valor diferente de zero, o campo SortSet DEVERÁ estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3246">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="6dadd-3247">Se definido como 0x00, SortSet DEVERÁ estar ausente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3247">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="6dadd-3248">**SortSet:** uma estrutura CSortSet que indica a ordem de classificação da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3248">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="6dadd-3249">**CCategorizationSetPresent:** um campo de byte que indica se o campo CCategorizationSet está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3249">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="6dadd-3250">Se definido como qualquer valor diferente de zero, o campo CCategorizationSet DEVERÁ estar presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3250">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="6dadd-3251">Se definido como 0x00, CCategorizationSet DEVERÁ estar ausente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3251">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="6dadd-3252">**CCategorizationSet:** uma estrutura CCategorizationSet que contém os grupos para a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3252">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="6dadd-3253">**RowSetProperties:** uma estrutura CRowsetProperties que fornece informações de configuração para a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3253">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="6dadd-3254">**PidMapper:** uma estrutura CPidMapper que contém propriedades a retornar em um conjuntos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3254">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="6dadd-3255">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-3255">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="6dadd-3256">A mensagem CPMCreateQueryOut contém uma resposta a uma mensagem CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3256">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="6dadd-3257">O formato da mensagem CPMCreateQueryOut que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3257">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3258">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3258">0</span></span>

<span data-ttu-id="6dadd-3259">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3259">1</span></span>

<span data-ttu-id="6dadd-3260">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3260">2</span></span>

<span data-ttu-id="6dadd-3261">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3261">3</span></span>

<span data-ttu-id="6dadd-3262">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3262">4</span></span>

<span data-ttu-id="6dadd-3263">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3263">5</span></span>

<span data-ttu-id="6dadd-3264">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3264">6</span></span>

<span data-ttu-id="6dadd-3265">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3265">7</span></span>

<span data-ttu-id="6dadd-3266">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3266">8</span></span>

<span data-ttu-id="6dadd-3267">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3267">9</span></span>

<span data-ttu-id="6dadd-3268">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3268">1</span></span><br/> <span data-ttu-id="6dadd-3269">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3269">0</span></span><br/>

<span data-ttu-id="6dadd-3270">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3270">1</span></span>

<span data-ttu-id="6dadd-3271">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3271">2</span></span>

<span data-ttu-id="6dadd-3272">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3272">3</span></span>

<span data-ttu-id="6dadd-3273">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3273">4</span></span>

<span data-ttu-id="6dadd-3274">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3274">5</span></span>

<span data-ttu-id="6dadd-3275">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3275">6</span></span>

<span data-ttu-id="6dadd-3276">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3276">7</span></span>

<span data-ttu-id="6dadd-3277">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3277">8</span></span>

<span data-ttu-id="6dadd-3278">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3278">9</span></span>

<span data-ttu-id="6dadd-3279">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3279">2</span></span><br/> <span data-ttu-id="6dadd-3280">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3280">0</span></span><br/>

<span data-ttu-id="6dadd-3281">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3281">1</span></span>

<span data-ttu-id="6dadd-3282">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3282">2</span></span>

<span data-ttu-id="6dadd-3283">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3283">3</span></span>

<span data-ttu-id="6dadd-3284">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3284">4</span></span>

<span data-ttu-id="6dadd-3285">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3285">5</span></span>

<span data-ttu-id="6dadd-3286">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3286">6</span></span>

<span data-ttu-id="6dadd-3287">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3287">7</span></span>

<span data-ttu-id="6dadd-3288">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3288">8</span></span>

<span data-ttu-id="6dadd-3289">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3289">9</span></span>

<span data-ttu-id="6dadd-3290">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3290">3</span></span><br/> <span data-ttu-id="6dadd-3291">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3291">0</span></span><br/>

<span data-ttu-id="6dadd-3292">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3292">1</span></span>

<span data-ttu-id="6dadd-3293">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="6dadd-3293">\_fTrueSequential</span></span>

<span data-ttu-id="6dadd-3294">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="6dadd-3294">\_fWorkIdUnique</span></span>

<span data-ttu-id="6dadd-3295">aCursors</span><span class="sxs-lookup"><span data-stu-id="6dadd-3295">aCursors</span></span>



 

<span data-ttu-id="6dadd-3296">**\_ fTrueSequential:** um valor booliano informativo que indica se a consulta pode fornecer resultados mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3296">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="6dadd-3297">Quando definido como 0x00000001 para a consulta fornecida em CPMCreateQueryIn, o servidor pode usar o índice de forma que os resultados da consulta provavelmente serão entregues mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3297">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="6dadd-3298">Quando definido como 0x00000000, haverá uma latência maior na entrega dos resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3298">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="6dadd-3299">NÃO DEVE ser definido como nenhum outro valor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3299">MUST not be set to any other value.</span></span>

<span data-ttu-id="6dadd-3300">**\_ fWorkIdUnique:** um valor booliana que indica se os identificadores de documento apontados pelos cursores são exclusivos em todos os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3300">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="6dadd-3301">Se definido como 0x00000001, os identificadores serão exclusivos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3301">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="6dadd-3302">Se definido como 0x00000000, eles serão exclusivos somente em todo o conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3302">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="6dadd-3303">**aCursors:** uma matriz de inteiros sem sinal de 32 bits que representa os alças para cursores, com o número de elementos iguais ao número de categorias no campo CategorizationSet da mensagem CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3303">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="6dadd-3304">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3304">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="6dadd-3305">A mensagem CPMGetQueryStatusIn solicita o status de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3305">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="6dadd-3306">O formato da mensagem CPMGetQueryStatusIn que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3306">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3307">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3307">0</span></span>

<span data-ttu-id="6dadd-3308">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3308">1</span></span>

<span data-ttu-id="6dadd-3309">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3309">2</span></span>

<span data-ttu-id="6dadd-3310">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3310">3</span></span>

<span data-ttu-id="6dadd-3311">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3311">4</span></span>

<span data-ttu-id="6dadd-3312">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3312">5</span></span>

<span data-ttu-id="6dadd-3313">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3313">6</span></span>

<span data-ttu-id="6dadd-3314">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3314">7</span></span>

<span data-ttu-id="6dadd-3315">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3315">8</span></span>

<span data-ttu-id="6dadd-3316">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3316">9</span></span>

<span data-ttu-id="6dadd-3317">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3317">1</span></span><br/> <span data-ttu-id="6dadd-3318">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3318">0</span></span><br/>

<span data-ttu-id="6dadd-3319">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3319">1</span></span>

<span data-ttu-id="6dadd-3320">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3320">2</span></span>

<span data-ttu-id="6dadd-3321">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3321">3</span></span>

<span data-ttu-id="6dadd-3322">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3322">4</span></span>

<span data-ttu-id="6dadd-3323">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3323">5</span></span>

<span data-ttu-id="6dadd-3324">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3324">6</span></span>

<span data-ttu-id="6dadd-3325">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3325">7</span></span>

<span data-ttu-id="6dadd-3326">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3326">8</span></span>

<span data-ttu-id="6dadd-3327">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3327">9</span></span>

<span data-ttu-id="6dadd-3328">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3328">2</span></span><br/> <span data-ttu-id="6dadd-3329">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3329">0</span></span><br/>

<span data-ttu-id="6dadd-3330">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3330">1</span></span>

<span data-ttu-id="6dadd-3331">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3331">2</span></span>

<span data-ttu-id="6dadd-3332">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3332">3</span></span>

<span data-ttu-id="6dadd-3333">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3333">4</span></span>

<span data-ttu-id="6dadd-3334">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3334">5</span></span>

<span data-ttu-id="6dadd-3335">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3335">6</span></span>

<span data-ttu-id="6dadd-3336">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3336">7</span></span>

<span data-ttu-id="6dadd-3337">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3337">8</span></span>

<span data-ttu-id="6dadd-3338">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3338">9</span></span>

<span data-ttu-id="6dadd-3339">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3339">3</span></span><br/> <span data-ttu-id="6dadd-3340">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3340">0</span></span><br/>

<span data-ttu-id="6dadd-3341">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3341">1</span></span>

<span data-ttu-id="6dadd-3342">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3342">\_hCursor</span></span>



 

<span data-ttu-id="6dadd-3343">**\_ hCursor**: um inteiro sem sinal de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual recuperar informações de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3343">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="6dadd-3344">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-3344">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="6dadd-3345">A mensagem CPMGetQueryStatusOut responde a uma mensagem CPMGetQueryStatusIn com o status da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3345">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="6dadd-3346">O formato da mensagem CPMGetQueryStatusOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3346">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3347">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3347">0</span></span>

<span data-ttu-id="6dadd-3348">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3348">1</span></span>

<span data-ttu-id="6dadd-3349">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3349">2</span></span>

<span data-ttu-id="6dadd-3350">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3350">3</span></span>

<span data-ttu-id="6dadd-3351">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3351">4</span></span>

<span data-ttu-id="6dadd-3352">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3352">5</span></span>

<span data-ttu-id="6dadd-3353">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3353">6</span></span>

<span data-ttu-id="6dadd-3354">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3354">7</span></span>

<span data-ttu-id="6dadd-3355">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3355">8</span></span>

<span data-ttu-id="6dadd-3356">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3356">9</span></span>

<span data-ttu-id="6dadd-3357">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3357">1</span></span><br/> <span data-ttu-id="6dadd-3358">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3358">0</span></span><br/>

<span data-ttu-id="6dadd-3359">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3359">1</span></span>

<span data-ttu-id="6dadd-3360">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3360">2</span></span>

<span data-ttu-id="6dadd-3361">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3361">3</span></span>

<span data-ttu-id="6dadd-3362">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3362">4</span></span>

<span data-ttu-id="6dadd-3363">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3363">5</span></span>

<span data-ttu-id="6dadd-3364">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3364">6</span></span>

<span data-ttu-id="6dadd-3365">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3365">7</span></span>

<span data-ttu-id="6dadd-3366">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3366">8</span></span>

<span data-ttu-id="6dadd-3367">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3367">9</span></span>

<span data-ttu-id="6dadd-3368">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3368">2</span></span><br/> <span data-ttu-id="6dadd-3369">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3369">0</span></span><br/>

<span data-ttu-id="6dadd-3370">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3370">1</span></span>

<span data-ttu-id="6dadd-3371">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3371">2</span></span>

<span data-ttu-id="6dadd-3372">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3372">3</span></span>

<span data-ttu-id="6dadd-3373">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3373">4</span></span>

<span data-ttu-id="6dadd-3374">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3374">5</span></span>

<span data-ttu-id="6dadd-3375">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3375">6</span></span>

<span data-ttu-id="6dadd-3376">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3376">7</span></span>

<span data-ttu-id="6dadd-3377">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3377">8</span></span>

<span data-ttu-id="6dadd-3378">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3378">9</span></span>

<span data-ttu-id="6dadd-3379">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3379">3</span></span><br/> <span data-ttu-id="6dadd-3380">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3380">0</span></span><br/>

<span data-ttu-id="6dadd-3381">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3381">1</span></span>

<span data-ttu-id="6dadd-3382">\_Status</span><span class="sxs-lookup"><span data-stu-id="6dadd-3382">\_Status</span></span>



 

<span data-ttu-id="6dadd-3383">**\_ Status**: uma bitmask de valores definida nas tabelas abaixo, que descreve a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3383">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="6dadd-3384">A tabela a seguir lista \_ \* os valores de stat obtidos com a execução de uma operação and bit a bit no \_ status com 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3384">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="6dadd-3385">O resultado deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3385">The result MUST be one of the following:</span></span>



| <span data-ttu-id="6dadd-3386">Constante</span><span class="sxs-lookup"><span data-stu-id="6dadd-3386">Constant</span></span>                 | <span data-ttu-id="6dadd-3387">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-3387">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-3388">STAT \_ ocupado 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-3388">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="6dadd-3389">A consulta assíncrona ainda está em execução.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3389">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="6dadd-3390">Erro de STAT \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-3390">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="6dadd-3391">A consulta está em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3391">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="6dadd-3392">STAT \_ concluído 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-3392">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="6dadd-3393">A consulta foi concluída.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3393">The query is complete.</span></span>                                                            |
| <span data-ttu-id="6dadd-3394">STAT \_ Refresh 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-3394">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="6dadd-3395">A consulta foi concluída, mas as atualizações estão resultando em computação de consulta adicional.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3395">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="6dadd-3396">A tabela a seguir lista bits de estatística adicionais \_ \* que podem ser definidos de forma independente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3396">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="6dadd-3397">Constante</span><span class="sxs-lookup"><span data-stu-id="6dadd-3397">Constant</span></span>                                    | <span data-ttu-id="6dadd-3398">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-3398">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dadd-3399">STATar \_ palavras de ruído \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dadd-3399">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="6dadd-3400">Palavras de ruído foram substituídas por caracteres curinga na consulta de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3400">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="6dadd-3401">\_Conteúdo \_ de stat fora \_ da \_ Data 0x00000020</span><span class="sxs-lookup"><span data-stu-id="6dadd-3401">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="6dadd-3402">Os resultados da consulta podem estar incorretos porque a consulta envolvia arquivos modificados, mas não indexados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3402">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="6dadd-3403">STAT \_ Atualizar \_ 0x00000040 incompleta</span><span class="sxs-lookup"><span data-stu-id="6dadd-3403">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="6dadd-3404">Os resultados da consulta podem estar incorretos porque a consulta envolvia arquivos modificados e reindexados cujo conteúdo não foi incluído.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3404">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="6dadd-3405">0x00000080 de consulta de conteúdo de STAT \_ \_ \_ incompleto</span><span class="sxs-lookup"><span data-stu-id="6dadd-3405">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="6dadd-3406">A consulta de conteúdo era muito complexa para concluir ou requerido a enumeração em vez de usar o índice de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3406">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="6dadd-3407">O \_ limite de tempo de stat \_ \_ excedeu 0x00000100</span><span class="sxs-lookup"><span data-stu-id="6dadd-3407">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="6dadd-3408">Os resultados da consulta podem estar incorretos porque o tempo de execução da consulta atingiu o tempo máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3408">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="6dadd-3409">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3409">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="6dadd-3410">A mensagem CPMGetQueryStatusExIn solicita o status de uma consulta e informações adicionais, como o número de documentos que foram indexados, o número de documentos restantes a serem indexados e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3410">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="6dadd-3411">O formato da mensagem CPMGetQueryStatusExIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3411">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3412">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3412">0</span></span>

<span data-ttu-id="6dadd-3413">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3413">1</span></span>

<span data-ttu-id="6dadd-3414">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3414">2</span></span>

<span data-ttu-id="6dadd-3415">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3415">3</span></span>

<span data-ttu-id="6dadd-3416">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3416">4</span></span>

<span data-ttu-id="6dadd-3417">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3417">5</span></span>

<span data-ttu-id="6dadd-3418">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3418">6</span></span>

<span data-ttu-id="6dadd-3419">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3419">7</span></span>

<span data-ttu-id="6dadd-3420">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3420">8</span></span>

<span data-ttu-id="6dadd-3421">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3421">9</span></span>

<span data-ttu-id="6dadd-3422">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3422">1</span></span><br/> <span data-ttu-id="6dadd-3423">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3423">0</span></span><br/>

<span data-ttu-id="6dadd-3424">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3424">1</span></span>

<span data-ttu-id="6dadd-3425">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3425">2</span></span>

<span data-ttu-id="6dadd-3426">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3426">3</span></span>

<span data-ttu-id="6dadd-3427">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3427">4</span></span>

<span data-ttu-id="6dadd-3428">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3428">5</span></span>

<span data-ttu-id="6dadd-3429">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3429">6</span></span>

<span data-ttu-id="6dadd-3430">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3430">7</span></span>

<span data-ttu-id="6dadd-3431">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3431">8</span></span>

<span data-ttu-id="6dadd-3432">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3432">9</span></span>

<span data-ttu-id="6dadd-3433">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3433">2</span></span><br/> <span data-ttu-id="6dadd-3434">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3434">0</span></span><br/>

<span data-ttu-id="6dadd-3435">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3435">1</span></span>

<span data-ttu-id="6dadd-3436">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3436">2</span></span>

<span data-ttu-id="6dadd-3437">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3437">3</span></span>

<span data-ttu-id="6dadd-3438">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3438">4</span></span>

<span data-ttu-id="6dadd-3439">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3439">5</span></span>

<span data-ttu-id="6dadd-3440">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3440">6</span></span>

<span data-ttu-id="6dadd-3441">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3441">7</span></span>

<span data-ttu-id="6dadd-3442">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3442">8</span></span>

<span data-ttu-id="6dadd-3443">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3443">9</span></span>

<span data-ttu-id="6dadd-3444">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3444">3</span></span><br/> <span data-ttu-id="6dadd-3445">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3445">0</span></span><br/>

<span data-ttu-id="6dadd-3446">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3446">1</span></span>

<span data-ttu-id="6dadd-3447">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3447">\_hCursor</span></span>

<span data-ttu-id="6dadd-3448">\_bmk</span><span class="sxs-lookup"><span data-stu-id="6dadd-3448">\_bmk</span></span>



 

<span data-ttu-id="6dadd-3449">**\_ hCursor**: um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual recuperar informações de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3449">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="6dadd-3450">**\_ BMK**: um valor de 32 bits que indica o identificador de um indicador cuja posição deve ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3450">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="6dadd-3451">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-3451">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="6dadd-3452">A mensagem CPMGetQueryStatusExOut responde a uma mensagem CPMGetQueryStatusExIn com o status da consulta e outras informações de status, conforme descrito no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3452">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="6dadd-3453">O formato da mensagem CPMGetQueryStatusExOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3453">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3454">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3454">0</span></span>

<span data-ttu-id="6dadd-3455">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3455">1</span></span>

<span data-ttu-id="6dadd-3456">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3456">2</span></span>

<span data-ttu-id="6dadd-3457">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3457">3</span></span>

<span data-ttu-id="6dadd-3458">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3458">4</span></span>

<span data-ttu-id="6dadd-3459">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3459">5</span></span>

<span data-ttu-id="6dadd-3460">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3460">6</span></span>

<span data-ttu-id="6dadd-3461">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3461">7</span></span>

<span data-ttu-id="6dadd-3462">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3462">8</span></span>

<span data-ttu-id="6dadd-3463">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3463">9</span></span>

<span data-ttu-id="6dadd-3464">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3464">1</span></span><br/> <span data-ttu-id="6dadd-3465">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3465">0</span></span><br/>

<span data-ttu-id="6dadd-3466">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3466">1</span></span>

<span data-ttu-id="6dadd-3467">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3467">2</span></span>

<span data-ttu-id="6dadd-3468">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3468">3</span></span>

<span data-ttu-id="6dadd-3469">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3469">4</span></span>

<span data-ttu-id="6dadd-3470">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3470">5</span></span>

<span data-ttu-id="6dadd-3471">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3471">6</span></span>

<span data-ttu-id="6dadd-3472">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3472">7</span></span>

<span data-ttu-id="6dadd-3473">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3473">8</span></span>

<span data-ttu-id="6dadd-3474">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3474">9</span></span>

<span data-ttu-id="6dadd-3475">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3475">2</span></span><br/> <span data-ttu-id="6dadd-3476">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3476">0</span></span><br/>

<span data-ttu-id="6dadd-3477">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3477">1</span></span>

<span data-ttu-id="6dadd-3478">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3478">2</span></span>

<span data-ttu-id="6dadd-3479">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3479">3</span></span>

<span data-ttu-id="6dadd-3480">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3480">4</span></span>

<span data-ttu-id="6dadd-3481">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3481">5</span></span>

<span data-ttu-id="6dadd-3482">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3482">6</span></span>

<span data-ttu-id="6dadd-3483">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3483">7</span></span>

<span data-ttu-id="6dadd-3484">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3484">8</span></span>

<span data-ttu-id="6dadd-3485">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3485">9</span></span>

<span data-ttu-id="6dadd-3486">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3486">3</span></span><br/> <span data-ttu-id="6dadd-3487">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3487">0</span></span><br/>

<span data-ttu-id="6dadd-3488">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3488">1</span></span>

<span data-ttu-id="6dadd-3489">\_Status</span><span class="sxs-lookup"><span data-stu-id="6dadd-3489">\_Status</span></span>

<span data-ttu-id="6dadd-3490">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="6dadd-3490">\_cFilteredDocuments</span></span>

<span data-ttu-id="6dadd-3491">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="6dadd-3491">\_cDocumentsToFilter</span></span>

<span data-ttu-id="6dadd-3492">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="6dadd-3492">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="6dadd-3493">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="6dadd-3493">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="6dadd-3494">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="6dadd-3494">\_iRowBmk</span></span>

<span data-ttu-id="6dadd-3495">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="6dadd-3495">\_cRowsTotal</span></span>



 

<span data-ttu-id="6dadd-3496">**\_ Status**: um dos stats \_ \* valores especificados na seção 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3496">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="6dadd-3497">**\_ cFilteredDocuments**: um inteiro sem sinal de 32 bits indicando o número de documentos que foram indexados</span><span class="sxs-lookup"><span data-stu-id="6dadd-3497">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="6dadd-3498">**\_ cDocumentsToFilter**: um inteiro de 32 bits sem sinal indicando o número de documentos que ainda permanecem para serem indexados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3498">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="6dadd-3499">**\_ dwRatioFinishedDenominator**: um inteiro de 32 bits sem sinal indicando o denominador da proporção de documentos que a consulta concluiu o processamento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3499">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="6dadd-3500">**\_ dwRatioFinishedNumerator**: um inteiro de 32 bits sem sinal indicando o numerador da proporção de documentos que a consulta concluiu o processamento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3500">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="6dadd-3501">**\_ iRowBmk**: um inteiro de 32 bits sem sinal indicando a posição aproximada do indicador no conjunto de linhas em termos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3501">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="6dadd-3502">**\_ cRowsTotal**: um inteiro de 32 bits sem sinal especificando o número total de linhas no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3502">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="6dadd-3503">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3503">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="6dadd-3504">A mensagem CPMSetBindingsIn solicita a associação de colunas a um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3504">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="6dadd-3505">O servidor responderá à mensagem de solicitação CPMSetBindingsIn usando a seção de cabeçalho da mensagem CPMBindingsIn com os resultados da solicitação contida no \_ campo status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3505">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="6dadd-3506">O formato da mensagem CPMSetBindingsIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3506">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3507">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3507">0</span></span>

<span data-ttu-id="6dadd-3508">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3508">1</span></span>

<span data-ttu-id="6dadd-3509">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3509">2</span></span>

<span data-ttu-id="6dadd-3510">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3510">3</span></span>

<span data-ttu-id="6dadd-3511">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3511">4</span></span>

<span data-ttu-id="6dadd-3512">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3512">5</span></span>

<span data-ttu-id="6dadd-3513">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3513">6</span></span>

<span data-ttu-id="6dadd-3514">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3514">7</span></span>

<span data-ttu-id="6dadd-3515">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3515">8</span></span>

<span data-ttu-id="6dadd-3516">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3516">9</span></span>

<span data-ttu-id="6dadd-3517">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3517">1</span></span><br/> <span data-ttu-id="6dadd-3518">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3518">0</span></span><br/>

<span data-ttu-id="6dadd-3519">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3519">1</span></span>

<span data-ttu-id="6dadd-3520">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3520">2</span></span>

<span data-ttu-id="6dadd-3521">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3521">3</span></span>

<span data-ttu-id="6dadd-3522">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3522">4</span></span>

<span data-ttu-id="6dadd-3523">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3523">5</span></span>

<span data-ttu-id="6dadd-3524">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3524">6</span></span>

<span data-ttu-id="6dadd-3525">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3525">7</span></span>

<span data-ttu-id="6dadd-3526">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3526">8</span></span>

<span data-ttu-id="6dadd-3527">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3527">9</span></span>

<span data-ttu-id="6dadd-3528">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3528">2</span></span><br/> <span data-ttu-id="6dadd-3529">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3529">0</span></span><br/>

<span data-ttu-id="6dadd-3530">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3530">1</span></span>

<span data-ttu-id="6dadd-3531">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3531">2</span></span>

<span data-ttu-id="6dadd-3532">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3532">3</span></span>

<span data-ttu-id="6dadd-3533">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3533">4</span></span>

<span data-ttu-id="6dadd-3534">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3534">5</span></span>

<span data-ttu-id="6dadd-3535">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3535">6</span></span>

<span data-ttu-id="6dadd-3536">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3536">7</span></span>

<span data-ttu-id="6dadd-3537">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3537">8</span></span>

<span data-ttu-id="6dadd-3538">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3538">9</span></span>

<span data-ttu-id="6dadd-3539">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3539">3</span></span><br/> <span data-ttu-id="6dadd-3540">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3540">0</span></span><br/>

<span data-ttu-id="6dadd-3541">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3541">1</span></span>

<span data-ttu-id="6dadd-3542">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3542">\_hCursor (optional)</span></span>

<span data-ttu-id="6dadd-3543">\_cbRow (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3543">\_cbRow (optional)</span></span>

<span data-ttu-id="6dadd-3544">\_cbBindingDesc (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3544">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="6dadd-3545">\_fictício (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3545">\_dummy (optional)</span></span>

<span data-ttu-id="6dadd-3546">cColumns (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3546">cColumns (optional)</span></span>

<span data-ttu-id="6dadd-3547">aColumns (variável, opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3547">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="6dadd-3548">**\_ hCursor:** um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a linha para a qual definir as vinculações.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3548">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="6dadd-3549">Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3549">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="6dadd-3550">**\_ cbRow:** um inteiro sem sinal de 32 bits que indica o tamanho, em bytes, de uma linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3550">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="6dadd-3551">Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3551">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="6dadd-3552">**\_ cbBindingDesc:** um inteiro sem sinal de 32 bits que indica o comprimento, em bytes, dos campos após o \_ campo fictício.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3552">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="6dadd-3553">Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3553">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="6dadd-3554">**\_ fictício:** esse campo não está sendo usada e DEVE ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3554">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="6dadd-3555">Ele pode ser definido como qualquer valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3555">It can be set to any arbitrary value.</span></span> <span data-ttu-id="6dadd-3556">Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="6dadd-3557">**cColumns:** um inteiro sem sinal de 32 bits que indica o número de elementos na matriz aColumns.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3557">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="6dadd-3558">Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3558">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="6dadd-3559">**aColumns:** uma matriz das estruturas CTableColumn que descrevem as colunas de uma linha no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3559">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="6dadd-3560">Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3560">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="6dadd-3561">As estruturas na matriz DEVEM ser separadas por 0 a 3 bytes de preenchimento, de forma que cada estrutura tenha um alinhamento de 4 bytes do início de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3561">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="6dadd-3562">Esses bytes de preenchimento podem ser qualquer valor arbitrário e DEVEM ser ignorados no recebimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3562">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="6dadd-3563">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3563">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="6dadd-3564">A mensagem CPMGetRowsIn solicita linhas de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3564">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="6dadd-3565">O formato da mensagem CPMGetRowsIn que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3565">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3566">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3566">0</span></span>

<span data-ttu-id="6dadd-3567">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3567">1</span></span>

<span data-ttu-id="6dadd-3568">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3568">2</span></span>

<span data-ttu-id="6dadd-3569">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3569">3</span></span>

<span data-ttu-id="6dadd-3570">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3570">4</span></span>

<span data-ttu-id="6dadd-3571">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3571">5</span></span>

<span data-ttu-id="6dadd-3572">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3572">6</span></span>

<span data-ttu-id="6dadd-3573">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3573">7</span></span>

<span data-ttu-id="6dadd-3574">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3574">8</span></span>

<span data-ttu-id="6dadd-3575">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3575">9</span></span>

<span data-ttu-id="6dadd-3576">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3576">1</span></span><br/> <span data-ttu-id="6dadd-3577">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3577">0</span></span><br/>

<span data-ttu-id="6dadd-3578">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3578">1</span></span>

<span data-ttu-id="6dadd-3579">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3579">2</span></span>

<span data-ttu-id="6dadd-3580">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3580">3</span></span>

<span data-ttu-id="6dadd-3581">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3581">4</span></span>

<span data-ttu-id="6dadd-3582">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3582">5</span></span>

<span data-ttu-id="6dadd-3583">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3583">6</span></span>

<span data-ttu-id="6dadd-3584">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3584">7</span></span>

<span data-ttu-id="6dadd-3585">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3585">8</span></span>

<span data-ttu-id="6dadd-3586">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3586">9</span></span>

<span data-ttu-id="6dadd-3587">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3587">2</span></span><br/> <span data-ttu-id="6dadd-3588">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3588">0</span></span><br/>

<span data-ttu-id="6dadd-3589">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3589">1</span></span>

<span data-ttu-id="6dadd-3590">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3590">2</span></span>

<span data-ttu-id="6dadd-3591">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3591">3</span></span>

<span data-ttu-id="6dadd-3592">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3592">4</span></span>

<span data-ttu-id="6dadd-3593">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3593">5</span></span>

<span data-ttu-id="6dadd-3594">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3594">6</span></span>

<span data-ttu-id="6dadd-3595">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3595">7</span></span>

<span data-ttu-id="6dadd-3596">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3596">8</span></span>

<span data-ttu-id="6dadd-3597">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3597">9</span></span>

<span data-ttu-id="6dadd-3598">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3598">3</span></span><br/> <span data-ttu-id="6dadd-3599">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3599">0</span></span><br/>

<span data-ttu-id="6dadd-3600">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3600">1</span></span>

<span data-ttu-id="6dadd-3601">\_Hcursor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3601">\_hCursor</span></span>

<span data-ttu-id="6dadd-3602">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="6dadd-3602">\_cRowsToTransfer</span></span>

<span data-ttu-id="6dadd-3603">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="6dadd-3603">\_cbRowWidth</span></span>

<span data-ttu-id="6dadd-3604">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="6dadd-3604">\_cbSeek</span></span>

<span data-ttu-id="6dadd-3605">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="6dadd-3605">\_cbReserved</span></span>

<span data-ttu-id="6dadd-3606">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="6dadd-3606">\_cbReadBuffer</span></span>

<span data-ttu-id="6dadd-3607">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="6dadd-3607">\_ulClientBase</span></span>

<span data-ttu-id="6dadd-3608">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="6dadd-3608">\_fBwdFetch</span></span>

<span data-ttu-id="6dadd-3609">Etype</span><span class="sxs-lookup"><span data-stu-id="6dadd-3609">eType</span></span>

<span data-ttu-id="6dadd-3610">\_chapt</span><span class="sxs-lookup"><span data-stu-id="6dadd-3610">\_chapt</span></span>

<span data-ttu-id="6dadd-3611">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="6dadd-3611">SeekDescription</span></span>

<span data-ttu-id="6dadd-3612">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3612">...</span></span>

<span data-ttu-id="6dadd-3613">... (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3613">... (variable)</span></span>



 

<span data-ttu-id="6dadd-3614">**\_ hCursor:** um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3614">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="6dadd-3615">**\_ cRowsToTransfer:** um inteiro sem sinal de 32 bits que indica o número máximo de linhas que o cliente deseja receber em resposta a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3615">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="6dadd-3616">**\_ cbRowWidth:** um inteiro sem sinal de 32 bits que indica o comprimento de uma linha, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3616">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="6dadd-3617">**\_ cbSeek:** um inteiro sem sinal de 32 bits que indica o tamanho da mensagem que começa com eType.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3617">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="6dadd-3618">**\_ cbReserved:** um inteiro sem sinal de 32 bits que indica o tamanho, em bytes, de uma mensagem CPMGetRowsOut (sem os campos Linhas e SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="6dadd-3618">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="6dadd-3619">Esse valor nesse campo é adicionado ao valor do campo cbSeek e, em seguida, deve ser usado para calcular o deslocamento do campo Linhas na mensagem \_ CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3619">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="6dadd-3620">**\_ cbReadBuffer:** um inteiro sem sinal de 32 bits que DEVE ser definido como o máximo do valor \_ de cbRowWidth ou 1000 vezes o valor de cRowsToTransfer, arredondado para o múltiplo de \_ 512 byte mais próximo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3620">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="6dadd-3621">O valor NÃO DEVE exceder 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3621">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="6dadd-3622">**\_ ulClientBase:** um inteiro sem sinal de 32 bits que indica o valor base a ser usado para cálculos de ponteiro no buffer de linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3622">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="6dadd-3623">Se deslocamentos de 64 bits estão sendo usados, o campo reservado2 do header da mensagem é usado como os 32 bits superiores e ulClientBase como os 32 bits inferiores de um valor de \_ 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3623">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="6dadd-3624">Consulte a seção 2.2.3.16 para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3624">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="6dadd-3625">**\_ fBwdFetch:** um inteiro sem sinal de 32 bits que indica a ordem na qual buscar as linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3625">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="6dadd-3626">Se definido como 0x00000001, as linhas deverão ser buscadas na ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3626">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="6dadd-3627">Se definido como 0x00000000, as linhas deverão ser buscadas na ordem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3627">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="6dadd-3628">Não deve ser definido para nenhum outro valor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3628">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="6dadd-3629">**ETYPE**: um inteiro sem sinal de 32 bits contendo um dos valores a seguir para indicar o tipo de operação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3629">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="6dadd-3630">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3630">Value</span></span>                         | <span data-ttu-id="6dadd-3631">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-3631">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="6dadd-3632">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-3632">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="6dadd-3633">SeekDescription contém uma estrutura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3633">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="6dadd-3634">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-3634">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="6dadd-3635">SeekDescription contém uma estrutura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3635">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="6dadd-3636">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-3636">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="6dadd-3637">SeekDescription contém uma estrutura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3637">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="6dadd-3638">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-3638">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="6dadd-3639">SeekDescription contém uma estrutura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3639">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="6dadd-3640">**\_ chapt**: um valor de 32 bits que representa o identificador do capítulo do conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3640">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="6dadd-3641">**SeekDescription**: esse campo deve conter uma estrutura do tipo indicado pelo valor de ETYPE.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3641">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="6dadd-3642">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-3642">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="6dadd-3643">A mensagem CPMGetRowsOut responde a uma mensagem CPMGetRowsIn com as linhas de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3643">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="6dadd-3644">Os servidores devem Formatar deslocamentos para tipos de dados de comprimento variável no campo linhas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3644">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="6dadd-3645">O cliente indicou que era um sistema de 32 bits (0x00000008 ou menos no campo iClientVersion de CPMConnectIn): os deslocamentos são inteiros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3645">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="6dadd-3646">O cliente indicou que era um sistema de 64 bits ( \_ iClientVersion > 0x00000008 no CPMConnectIn) e o servidor indicou que era um sistema de 32 bits ( \_ serverVersion definido como 0X00000007 em CPMConnectOut): os deslocamentos são inteiros de 32 bits</span><span class="sxs-lookup"><span data-stu-id="6dadd-3646">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="6dadd-3647">O cliente indicou que era um sistema de 64 bits ( \_ iClientVersion > 0x00000008 no CPMConnectIn) e o servidor indicou que era um sistema de 64 bits ( \_ serverVersion definido como 0X00010007 em CPMConnectOut): os deslocamentos são inteiros de 64 bits</span><span class="sxs-lookup"><span data-stu-id="6dadd-3647">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="6dadd-3648">O formato da mensagem CPMGetRowsOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3648">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3649">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3649">0</span></span>

<span data-ttu-id="6dadd-3650">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3650">1</span></span>

<span data-ttu-id="6dadd-3651">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3651">2</span></span>

<span data-ttu-id="6dadd-3652">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3652">3</span></span>

<span data-ttu-id="6dadd-3653">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3653">4</span></span>

<span data-ttu-id="6dadd-3654">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3654">5</span></span>

<span data-ttu-id="6dadd-3655">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3655">6</span></span>

<span data-ttu-id="6dadd-3656">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3656">7</span></span>

<span data-ttu-id="6dadd-3657">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3657">8</span></span>

<span data-ttu-id="6dadd-3658">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3658">9</span></span>

<span data-ttu-id="6dadd-3659">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3659">1</span></span><br/> <span data-ttu-id="6dadd-3660">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3660">0</span></span><br/>

<span data-ttu-id="6dadd-3661">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3661">1</span></span>

<span data-ttu-id="6dadd-3662">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3662">2</span></span>

<span data-ttu-id="6dadd-3663">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3663">3</span></span>

<span data-ttu-id="6dadd-3664">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3664">4</span></span>

<span data-ttu-id="6dadd-3665">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3665">5</span></span>

<span data-ttu-id="6dadd-3666">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3666">6</span></span>

<span data-ttu-id="6dadd-3667">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3667">7</span></span>

<span data-ttu-id="6dadd-3668">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3668">8</span></span>

<span data-ttu-id="6dadd-3669">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3669">9</span></span>

<span data-ttu-id="6dadd-3670">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3670">2</span></span><br/> <span data-ttu-id="6dadd-3671">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3671">0</span></span><br/>

<span data-ttu-id="6dadd-3672">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3672">1</span></span>

<span data-ttu-id="6dadd-3673">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3673">2</span></span>

<span data-ttu-id="6dadd-3674">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3674">3</span></span>

<span data-ttu-id="6dadd-3675">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3675">4</span></span>

<span data-ttu-id="6dadd-3676">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3676">5</span></span>

<span data-ttu-id="6dadd-3677">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3677">6</span></span>

<span data-ttu-id="6dadd-3678">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3678">7</span></span>

<span data-ttu-id="6dadd-3679">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3679">8</span></span>

<span data-ttu-id="6dadd-3680">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3680">9</span></span>

<span data-ttu-id="6dadd-3681">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3681">3</span></span><br/> <span data-ttu-id="6dadd-3682">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3682">0</span></span><br/>

<span data-ttu-id="6dadd-3683">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3683">1</span></span>

<span data-ttu-id="6dadd-3684">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="6dadd-3684">\_cRowsReturned</span></span>

<span data-ttu-id="6dadd-3685">eType</span><span class="sxs-lookup"><span data-stu-id="6dadd-3685">eType</span></span>

<span data-ttu-id="6dadd-3686">\_chapt</span><span class="sxs-lookup"><span data-stu-id="6dadd-3686">\_chapt</span></span>

<span data-ttu-id="6dadd-3687">SeekDescription (opcional, variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3687">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="6dadd-3688">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3688">...</span></span>

<span data-ttu-id="6dadd-3689">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3689">...</span></span>

<span data-ttu-id="6dadd-3690">paddingRows (opcional, variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3690">paddingRows (optional, variable)</span></span>

<span data-ttu-id="6dadd-3691">Linhas</span><span class="sxs-lookup"><span data-stu-id="6dadd-3691">Rows</span></span>



 

<span data-ttu-id="6dadd-3692">**\_ cRowsReturned**: um inteiro de 32 bits sem sinal indicando o número de linhas retornadas em linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3692">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="6dadd-3693">**ETYPE**: um inteiro sem sinal de 32 bits contendo um dos seguintes valores para indicar o tipo de operação de busca a ser executada</span><span class="sxs-lookup"><span data-stu-id="6dadd-3693">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="6dadd-3694">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3694">Value</span></span>                         | <span data-ttu-id="6dadd-3695">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-3695">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="6dadd-3696">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-3696">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="6dadd-3697">Sem SeekDescription, ignore o campo SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3697">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="6dadd-3698">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-3698">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="6dadd-3699">SeekDescription contém uma estrutura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3699">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="6dadd-3700">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-3700">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="6dadd-3701">SeekDescription contém uma estrutura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3701">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="6dadd-3702">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-3702">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="6dadd-3703">SeekDescription contém uma estrutura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3703">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="6dadd-3704">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-3704">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="6dadd-3705">SeekDescription contém uma estrutura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3705">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="6dadd-3706">**\_ chapt**: um valor de 32 bits que representa o identificador do capítulo do conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3706">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="6dadd-3707">**SeekDescription**: esse campo deve conter uma estrutura do tipo indicado pelo campo ETYPE.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3707">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="6dadd-3708">**paddingRows**: esse campo deve ter comprimento suficiente (0 a \_ cbReserved-1 bytes) para preencher o campo de linhas para o \_ deslocamento de cbReserved do início de uma mensagem, em que \_ cbReserved é o valor na mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3708">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="6dadd-3709">Os bytes de preenchimento usados nesse campo podem ser de qualquer valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3709">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="6dadd-3710">Este campo deve ser ignorado pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3710">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="6dadd-3711">**Linhas**: dados de linha, são formatados conforme prescrito pelas informações de coluna na mensagem CPMSetBindingsIn mais recente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3711">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="6dadd-3712">As linhas devem ser armazenadas na ordem de encaminhamento (por exemplo, linha 1 antes da linha 2).</span><span class="sxs-lookup"><span data-stu-id="6dadd-3712">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="6dadd-3713">Colunas de tamanho fixo devem ser armazenadas nos deslocamentos especificados pela mensagem CPMSetBindingsIn mais recente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3713">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="6dadd-3714">Colunas de tamanho variável (por exemplo, cadeias de caracteres) devem ser armazenadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3714">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="6dadd-3715">A variável de dados em si (por exemplo, a cadeia de caracteres) é armazenada perto do final do buffer em ordem decrescente (por exemplo, a coleção de todos os dados da variável para a linha 1 está no final, linha 2 mais próxima, etc.).</span><span class="sxs-lookup"><span data-stu-id="6dadd-3715">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="6dadd-3716">A área de tamanho fixo (no início do buffer de linha) deve conter um CRowVariant para cada coluna, armazenado no deslocamento especificado na mensagem de CPMSetBindingsIn mais recente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3716">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="6dadd-3717">vType deve conter o tipo de dados (ex: VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="6dadd-3717">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="6dadd-3718">Se, conforme determinado pelas regras no início da seção, esta seção, os deslocamentos de 32 bits estão sendo usados, o campo de deslocamento em CRowVariant deve conter um valor de 32 bits que é o deslocamento dos dados da variável do início da mensagem CPMGetRowsOut, mais o valor de \_ ulClientBase especificado na mensagem de CPMGetRowsIn mais recente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3718">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="6dadd-3719">Se os deslocamentos de 64 bits estiverem sendo usados, o campo de deslocamento em CRowVariant deverá conter um valor de 64 bits que é o deslocamento do início da mensagem CPMGetRowsOut, adicionado a um valor de 64 bits composto por meio de \_ ulClientBase como baixo 32-bits e \_ ulReserved2 como o alto 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3719">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="6dadd-3720">Por exemplo, se a mensagem CPMSetBindingsIn especificou duas colunas-size (VT \_ i4) e Title (VT \_ LPWSTR)-e \_ ulClientBase de CPMGetRowsIn for 0x10000, duas linhas aparecerão da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3720">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="6dadd-3721">A seção marcada em cinza é a parte de comprimento fixo do buffer.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3721">The section marked in grey is the fixed-length part of the buffer.</span></span>

![exemplo de mensagem cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="6dadd-3723">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3723">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="6dadd-3724">A mensagem CPMRatioFinishedIn solicita a porcentagem de conclusão de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3724">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="6dadd-3725">O formato da mensagem CPMRatioFinishedIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3725">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3726">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3726">0</span></span>

<span data-ttu-id="6dadd-3727">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3727">1</span></span>

<span data-ttu-id="6dadd-3728">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3728">2</span></span>

<span data-ttu-id="6dadd-3729">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3729">3</span></span>

<span data-ttu-id="6dadd-3730">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3730">4</span></span>

<span data-ttu-id="6dadd-3731">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3731">5</span></span>

<span data-ttu-id="6dadd-3732">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3732">6</span></span>

<span data-ttu-id="6dadd-3733">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3733">7</span></span>

<span data-ttu-id="6dadd-3734">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3734">8</span></span>

<span data-ttu-id="6dadd-3735">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3735">9</span></span>

<span data-ttu-id="6dadd-3736">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3736">1</span></span><br/> <span data-ttu-id="6dadd-3737">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3737">0</span></span><br/>

<span data-ttu-id="6dadd-3738">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3738">1</span></span>

<span data-ttu-id="6dadd-3739">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3739">2</span></span>

<span data-ttu-id="6dadd-3740">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3740">3</span></span>

<span data-ttu-id="6dadd-3741">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3741">4</span></span>

<span data-ttu-id="6dadd-3742">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3742">5</span></span>

<span data-ttu-id="6dadd-3743">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3743">6</span></span>

<span data-ttu-id="6dadd-3744">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3744">7</span></span>

<span data-ttu-id="6dadd-3745">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3745">8</span></span>

<span data-ttu-id="6dadd-3746">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3746">9</span></span>

<span data-ttu-id="6dadd-3747">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3747">2</span></span><br/> <span data-ttu-id="6dadd-3748">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3748">0</span></span><br/>

<span data-ttu-id="6dadd-3749">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3749">1</span></span>

<span data-ttu-id="6dadd-3750">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3750">2</span></span>

<span data-ttu-id="6dadd-3751">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3751">3</span></span>

<span data-ttu-id="6dadd-3752">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3752">4</span></span>

<span data-ttu-id="6dadd-3753">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3753">5</span></span>

<span data-ttu-id="6dadd-3754">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3754">6</span></span>

<span data-ttu-id="6dadd-3755">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3755">7</span></span>

<span data-ttu-id="6dadd-3756">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3756">8</span></span>

<span data-ttu-id="6dadd-3757">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3757">9</span></span>

<span data-ttu-id="6dadd-3758">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3758">3</span></span><br/> <span data-ttu-id="6dadd-3759">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3759">0</span></span><br/>

<span data-ttu-id="6dadd-3760">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3760">1</span></span>

<span data-ttu-id="6dadd-3761">\_Hcursor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3761">\_hCursor</span></span>

<span data-ttu-id="6dadd-3762">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="6dadd-3762">\_fQuick</span></span>



 

<span data-ttu-id="6dadd-3763">**\_ hCursor:** o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual solicitar informações de conclusão.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3763">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="6dadd-3764">**\_ fQuick**: DEVE ser definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3764">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="6dadd-3765">Não usada e DEVE ser ignorada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3765">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="6dadd-3766">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-3766">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="6dadd-3767">A mensagem CPMRatioFinishedOut responde a uma mensagem CPMRatioFinishedIn com a taxa de conclusão de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3767">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="6dadd-3768">O formato da mensagem CPMRatioFinishedOut que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3768">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3769">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3769">0</span></span>

<span data-ttu-id="6dadd-3770">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3770">1</span></span>

<span data-ttu-id="6dadd-3771">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3771">2</span></span>

<span data-ttu-id="6dadd-3772">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3772">3</span></span>

<span data-ttu-id="6dadd-3773">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3773">4</span></span>

<span data-ttu-id="6dadd-3774">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3774">5</span></span>

<span data-ttu-id="6dadd-3775">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3775">6</span></span>

<span data-ttu-id="6dadd-3776">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3776">7</span></span>

<span data-ttu-id="6dadd-3777">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3777">8</span></span>

<span data-ttu-id="6dadd-3778">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3778">9</span></span>

<span data-ttu-id="6dadd-3779">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3779">1</span></span><br/> <span data-ttu-id="6dadd-3780">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3780">0</span></span><br/>

<span data-ttu-id="6dadd-3781">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3781">1</span></span>

<span data-ttu-id="6dadd-3782">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3782">2</span></span>

<span data-ttu-id="6dadd-3783">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3783">3</span></span>

<span data-ttu-id="6dadd-3784">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3784">4</span></span>

<span data-ttu-id="6dadd-3785">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3785">5</span></span>

<span data-ttu-id="6dadd-3786">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3786">6</span></span>

<span data-ttu-id="6dadd-3787">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3787">7</span></span>

<span data-ttu-id="6dadd-3788">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3788">8</span></span>

<span data-ttu-id="6dadd-3789">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3789">9</span></span>

<span data-ttu-id="6dadd-3790">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3790">2</span></span><br/> <span data-ttu-id="6dadd-3791">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3791">0</span></span><br/>

<span data-ttu-id="6dadd-3792">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3792">1</span></span>

<span data-ttu-id="6dadd-3793">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3793">2</span></span>

<span data-ttu-id="6dadd-3794">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3794">3</span></span>

<span data-ttu-id="6dadd-3795">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3795">4</span></span>

<span data-ttu-id="6dadd-3796">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3796">5</span></span>

<span data-ttu-id="6dadd-3797">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3797">6</span></span>

<span data-ttu-id="6dadd-3798">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3798">7</span></span>

<span data-ttu-id="6dadd-3799">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3799">8</span></span>

<span data-ttu-id="6dadd-3800">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3800">9</span></span>

<span data-ttu-id="6dadd-3801">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3801">3</span></span><br/> <span data-ttu-id="6dadd-3802">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3802">0</span></span><br/>

<span data-ttu-id="6dadd-3803">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3803">1</span></span>

<span data-ttu-id="6dadd-3804">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="6dadd-3804">\_ ulNumerator</span></span>

<span data-ttu-id="6dadd-3805">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="6dadd-3805">\_ulDenominator</span></span>

<span data-ttu-id="6dadd-3806">\_Corvos</span><span class="sxs-lookup"><span data-stu-id="6dadd-3806">\_cRows</span></span>

<span data-ttu-id="6dadd-3807">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="6dadd-3807">\_fNewRows</span></span>



 

<span data-ttu-id="6dadd-3808">**\_ ulNumerator:** um inteiro sem sinal de 32 bits que indica o numerador da taxa de conclusão em termos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3808">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="6dadd-3809">**\_ ulDenominator:** um inteiro sem sinal de 32 bits que indica o denominador da taxa de conclusão em termos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3809">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="6dadd-3810">DEVE ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3810">MUST be greater than zero.</span></span>

<span data-ttu-id="6dadd-3811">**\_ cRows:** um inteiro sem sinal de 32 bits que indica o número total de linhas para a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3811">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="6dadd-3812">**\_ fNewRows:** um valor booliana que indica se há novas linhas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3812">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="6dadd-3813">Um valor de 0x00000001 indica que novas linhas estão disponíveis no conjuntos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3813">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="6dadd-3814">Um valor de 0x00000000 indica que o conjuntos de linhas não contém nenhuma nova linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3814">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="6dadd-3815">Esse campo NÃO DEVE ser definido como nenhum outro valor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3815">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="6dadd-3816">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3816">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="6dadd-3817">A mensagem CPMFetchValueIn solicita um valor de propriedade muito grande para retornar em um conjuntos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3817">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="6dadd-3818">Conforme especificado na seção 3.2.4.2.5, essa mensagem é enviada repetidamente para recuperar todos os bytes da propriedade, atualizando cbSoFar para cada um, até que o campo fMoreExists da mensagem \_ \_ CPMFetchValueOut seja definido como **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="6dadd-3818">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="6dadd-3819">O formato da mensagem CPMFetchValueIn que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3819">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3820">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3820">0</span></span>

<span data-ttu-id="6dadd-3821">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3821">1</span></span>

<span data-ttu-id="6dadd-3822">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3822">2</span></span>

<span data-ttu-id="6dadd-3823">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3823">3</span></span>

<span data-ttu-id="6dadd-3824">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3824">4</span></span>

<span data-ttu-id="6dadd-3825">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3825">5</span></span>

<span data-ttu-id="6dadd-3826">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3826">6</span></span>

<span data-ttu-id="6dadd-3827">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3827">7</span></span>

<span data-ttu-id="6dadd-3828">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3828">8</span></span>

<span data-ttu-id="6dadd-3829">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3829">9</span></span>

<span data-ttu-id="6dadd-3830">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3830">1</span></span><br/> <span data-ttu-id="6dadd-3831">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3831">0</span></span><br/>

<span data-ttu-id="6dadd-3832">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3832">1</span></span>

<span data-ttu-id="6dadd-3833">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3833">2</span></span>

<span data-ttu-id="6dadd-3834">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3834">3</span></span>

<span data-ttu-id="6dadd-3835">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3835">4</span></span>

<span data-ttu-id="6dadd-3836">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3836">5</span></span>

<span data-ttu-id="6dadd-3837">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3837">6</span></span>

<span data-ttu-id="6dadd-3838">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3838">7</span></span>

<span data-ttu-id="6dadd-3839">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3839">8</span></span>

<span data-ttu-id="6dadd-3840">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3840">9</span></span>

<span data-ttu-id="6dadd-3841">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3841">2</span></span><br/> <span data-ttu-id="6dadd-3842">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3842">0</span></span><br/>

<span data-ttu-id="6dadd-3843">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3843">1</span></span>

<span data-ttu-id="6dadd-3844">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3844">2</span></span>

<span data-ttu-id="6dadd-3845">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3845">3</span></span>

<span data-ttu-id="6dadd-3846">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3846">4</span></span>

<span data-ttu-id="6dadd-3847">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3847">5</span></span>

<span data-ttu-id="6dadd-3848">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3848">6</span></span>

<span data-ttu-id="6dadd-3849">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3849">7</span></span>

<span data-ttu-id="6dadd-3850">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3850">8</span></span>

<span data-ttu-id="6dadd-3851">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3851">9</span></span>

<span data-ttu-id="6dadd-3852">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3852">3</span></span><br/> <span data-ttu-id="6dadd-3853">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3853">0</span></span><br/>

<span data-ttu-id="6dadd-3854">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3854">1</span></span>

<span data-ttu-id="6dadd-3855">\_Wid</span><span class="sxs-lookup"><span data-stu-id="6dadd-3855">\_wid</span></span>

<span data-ttu-id="6dadd-3856">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="6dadd-3856">\_cbSoFar</span></span>

<span data-ttu-id="6dadd-3857">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="6dadd-3857">\_cbPropSpec</span></span>

<span data-ttu-id="6dadd-3858">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="6dadd-3858">\_cbChunk</span></span>

<span data-ttu-id="6dadd-3859">PropSpec (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3859">PropSpec (variable)</span></span>

<span data-ttu-id="6dadd-3860">...</span><span class="sxs-lookup"><span data-stu-id="6dadd-3860">...</span></span>

<span data-ttu-id="6dadd-3861">\_preenchimento (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3861">\_padding (variable)</span></span>



 

<span data-ttu-id="6dadd-3862">**\_ wid:** um inteiro sem sinal de 32 bits que contém informações sobre a ID do documento que identifica o documento para o qual uma propriedade deve ser buscada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3862">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="6dadd-3863">**\_ cbSoFar:** um inteiro sem sinal de 32 bits que contém o número de bytes transferidos anteriormente para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3863">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="6dadd-3864">DEVE ser definido como 0x00000000 na primeira mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3864">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="6dadd-3865">**\_ cbPropSpec:** um inteiro sem sinal de 32 bits que contém o tamanho do campo PropSpec, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3865">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="6dadd-3866">**\_ cbChunk:** um inteiro sem sinal de 32 bits que contém o número máximo de bytes que o remetente pode aceitar em uma mensagem CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3866">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="6dadd-3867">*Comportamento do Windows: esse campo é definido como 0x00004000 para todas as versões do Windows.*</span><span class="sxs-lookup"><span data-stu-id="6dadd-3867">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="6dadd-3868">**PropSpec:** uma estrutura CFullPropSpec especificando a propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3868">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="6dadd-3869">**\_ preenchimento:** esse campo DEVE ter o comprimento necessário (de 0 a 3 bytes) para pad da mensagem para um múltiplo de 4 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3869">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="6dadd-3870">O valor dos bytes de preenchimento pode ser qualquer valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3870">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="6dadd-3871">Esse campo DEVE ser ignorado pelo receptor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3871">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="6dadd-3872">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-3872">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="6dadd-3873">A mensagem CPMFetchValueOut responde a uma mensagem CPMFetchValueIn com um valor de propriedade de uma consulta anterior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3873">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="6dadd-3874">Conforme especificado na seção 3.1.5.2.8, essa mensagem é enviada após cada mensagem CPMFetchValueIn até que todos os bytes da propriedade sejam transferidos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3874">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="6dadd-3875">O formato da mensagem CPMFetchValueOut que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3875">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3876">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3876">0</span></span>

<span data-ttu-id="6dadd-3877">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3877">1</span></span>

<span data-ttu-id="6dadd-3878">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3878">2</span></span>

<span data-ttu-id="6dadd-3879">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3879">3</span></span>

<span data-ttu-id="6dadd-3880">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3880">4</span></span>

<span data-ttu-id="6dadd-3881">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3881">5</span></span>

<span data-ttu-id="6dadd-3882">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3882">6</span></span>

<span data-ttu-id="6dadd-3883">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3883">7</span></span>

<span data-ttu-id="6dadd-3884">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3884">8</span></span>

<span data-ttu-id="6dadd-3885">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3885">9</span></span>

<span data-ttu-id="6dadd-3886">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3886">1</span></span><br/> <span data-ttu-id="6dadd-3887">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3887">0</span></span><br/>

<span data-ttu-id="6dadd-3888">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3888">1</span></span>

<span data-ttu-id="6dadd-3889">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3889">2</span></span>

<span data-ttu-id="6dadd-3890">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3890">3</span></span>

<span data-ttu-id="6dadd-3891">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3891">4</span></span>

<span data-ttu-id="6dadd-3892">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3892">5</span></span>

<span data-ttu-id="6dadd-3893">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3893">6</span></span>

<span data-ttu-id="6dadd-3894">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3894">7</span></span>

<span data-ttu-id="6dadd-3895">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3895">8</span></span>

<span data-ttu-id="6dadd-3896">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3896">9</span></span>

<span data-ttu-id="6dadd-3897">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3897">2</span></span><br/> <span data-ttu-id="6dadd-3898">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3898">0</span></span><br/>

<span data-ttu-id="6dadd-3899">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3899">1</span></span>

<span data-ttu-id="6dadd-3900">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3900">2</span></span>

<span data-ttu-id="6dadd-3901">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3901">3</span></span>

<span data-ttu-id="6dadd-3902">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3902">4</span></span>

<span data-ttu-id="6dadd-3903">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3903">5</span></span>

<span data-ttu-id="6dadd-3904">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3904">6</span></span>

<span data-ttu-id="6dadd-3905">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3905">7</span></span>

<span data-ttu-id="6dadd-3906">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3906">8</span></span>

<span data-ttu-id="6dadd-3907">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3907">9</span></span>

<span data-ttu-id="6dadd-3908">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3908">3</span></span><br/> <span data-ttu-id="6dadd-3909">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3909">0</span></span><br/>

<span data-ttu-id="6dadd-3910">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3910">1</span></span>

<span data-ttu-id="6dadd-3911">\_Cbvalue</span><span class="sxs-lookup"><span data-stu-id="6dadd-3911">\_cbValue</span></span>

<span data-ttu-id="6dadd-3912">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="6dadd-3912">\_fMoreExists</span></span>

<span data-ttu-id="6dadd-3913">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="6dadd-3913">\_fValueExists</span></span>

<span data-ttu-id="6dadd-3914">vType</span><span class="sxs-lookup"><span data-stu-id="6dadd-3914">vType</span></span>

<span data-ttu-id="6dadd-3915">vValue (variável)</span><span class="sxs-lookup"><span data-stu-id="6dadd-3915">vValue (variable)</span></span>



 

<span data-ttu-id="6dadd-3916">**\_ cbValue:** um inteiro sem sinal de 32 bits que contém o tamanho total, em bytes em vValue.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3916">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="6dadd-3917">**\_ fMoreExists:** um valor booliana que indica se há mensagens CPMFetchValueOut adicionais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3917">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="6dadd-3918">Se definido como 0x00000001, haverá mensagens CPMFetchValueOut adicionais.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3918">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="6dadd-3919">Se definido como 0x00000000, não haverá mensagens CPMFetchValueOut adicionais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3919">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="6dadd-3920">**\_ fValueExists:** um valor booliana que indica se há um valor para a propriedade .</span><span class="sxs-lookup"><span data-stu-id="6dadd-3920">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="6dadd-3921">Se definido como 0x00000001, existe um valor para a propriedade .</span><span class="sxs-lookup"><span data-stu-id="6dadd-3921">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="6dadd-3922">Se definido como 0x00000000, um valor para a propriedade não existirá.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3922">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="6dadd-3923">**vType:** um valor da enumeração VARENUM, consulte a Seção 2.2.1.1 para obter detalhes, descrevendo o tipo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3923">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="6dadd-3924">**vValue:** uma parte de uma matriz de byte que contém uma estrutura SERIALIZEDPROPERTYVALUE, conforme especificado na seção 2.2.1.32, em que o deslocamento do início da parte é o valor \_ de cbSoFar em CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3924">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="6dadd-3925">O comprimento da parte, indicado pelo campo cbValue, DEVE ser igual ao valor de \_ \_ cbChunk em CPMFetchValueIn se fMoreExists estiver definido como 0x00000001 e DEVE ser menor ou igual ao valor \_ de \_ cbChunk, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3925">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="6dadd-3926">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="6dadd-3926">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="6dadd-3927">A mensagem CPMGetNotify solicita que o cliente queira ser notificado sobre alterações no conjuntos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3927">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="6dadd-3928">A mensagem NÃO DEVE incluir um corpo; somente o header da mensagem, conforme especificado na Seção 2.2.2, deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3928">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="6dadd-3929">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-3929">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="6dadd-3930">A mensagem CPMSendNotifyOut notifica o cliente de uma alteração nos resultados de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3930">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="6dadd-3931">Essa mensagem só é enviada quando ocorre uma alteração.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3931">This message is only sent when a change occurs.</span></span> <span data-ttu-id="6dadd-3932">O formato da mensagem CPMSendNotifyOut que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3932">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3933">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3933">0</span></span>

<span data-ttu-id="6dadd-3934">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3934">1</span></span>

<span data-ttu-id="6dadd-3935">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3935">2</span></span>

<span data-ttu-id="6dadd-3936">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3936">3</span></span>

<span data-ttu-id="6dadd-3937">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3937">4</span></span>

<span data-ttu-id="6dadd-3938">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3938">5</span></span>

<span data-ttu-id="6dadd-3939">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3939">6</span></span>

<span data-ttu-id="6dadd-3940">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3940">7</span></span>

<span data-ttu-id="6dadd-3941">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3941">8</span></span>

<span data-ttu-id="6dadd-3942">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3942">9</span></span>

<span data-ttu-id="6dadd-3943">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3943">1</span></span><br/> <span data-ttu-id="6dadd-3944">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3944">0</span></span><br/>

<span data-ttu-id="6dadd-3945">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3945">1</span></span>

<span data-ttu-id="6dadd-3946">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3946">2</span></span>

<span data-ttu-id="6dadd-3947">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3947">3</span></span>

<span data-ttu-id="6dadd-3948">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3948">4</span></span>

<span data-ttu-id="6dadd-3949">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3949">5</span></span>

<span data-ttu-id="6dadd-3950">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3950">6</span></span>

<span data-ttu-id="6dadd-3951">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3951">7</span></span>

<span data-ttu-id="6dadd-3952">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3952">8</span></span>

<span data-ttu-id="6dadd-3953">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3953">9</span></span>

<span data-ttu-id="6dadd-3954">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3954">2</span></span><br/> <span data-ttu-id="6dadd-3955">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3955">0</span></span><br/>

<span data-ttu-id="6dadd-3956">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3956">1</span></span>

<span data-ttu-id="6dadd-3957">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3957">2</span></span>

<span data-ttu-id="6dadd-3958">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3958">3</span></span>

<span data-ttu-id="6dadd-3959">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3959">4</span></span>

<span data-ttu-id="6dadd-3960">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3960">5</span></span>

<span data-ttu-id="6dadd-3961">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3961">6</span></span>

<span data-ttu-id="6dadd-3962">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3962">7</span></span>

<span data-ttu-id="6dadd-3963">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3963">8</span></span>

<span data-ttu-id="6dadd-3964">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3964">9</span></span>

<span data-ttu-id="6dadd-3965">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3965">3</span></span><br/> <span data-ttu-id="6dadd-3966">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3966">0</span></span><br/>

<span data-ttu-id="6dadd-3967">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3967">1</span></span>

<span data-ttu-id="6dadd-3968">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="6dadd-3968">\_watchNotify</span></span>



 

<span data-ttu-id="6dadd-3969">**\_ watchNotify:** a alteração na consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3969">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="6dadd-3970">Ele DEVE ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3970">It MUST be one of the following values:</span></span>



| <span data-ttu-id="6dadd-3971">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-3971">Value</span></span>                                     | <span data-ttu-id="6dadd-3972">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-3972">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="6dadd-3973">DBWATCHNOTIFY \_ ROWSCHANGED 0X00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-3973">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="6dadd-3974">O número de linhas no conjuntos de linhas de consulta foi alterado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3974">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="6dadd-3975">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-3975">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="6dadd-3976">A consulta foi concluída.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3976">The query has completed.</span></span>                            |
| <span data-ttu-id="6dadd-3977">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-3977">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="6dadd-3978">A consulta foi executada de uma vez.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3978">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="6dadd-3979">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-3979">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="6dadd-3980">A mensagem CPMGetApproximatePositionIn solicita a posição aproximada de um indicador em um capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-3980">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="6dadd-3981">O formato da mensagem CPMGetApproximatePositionIn que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-3981">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-3982">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3982">0</span></span>

<span data-ttu-id="6dadd-3983">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3983">1</span></span>

<span data-ttu-id="6dadd-3984">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3984">2</span></span>

<span data-ttu-id="6dadd-3985">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3985">3</span></span>

<span data-ttu-id="6dadd-3986">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3986">4</span></span>

<span data-ttu-id="6dadd-3987">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3987">5</span></span>

<span data-ttu-id="6dadd-3988">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3988">6</span></span>

<span data-ttu-id="6dadd-3989">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-3989">7</span></span>

<span data-ttu-id="6dadd-3990">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-3990">8</span></span>

<span data-ttu-id="6dadd-3991">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-3991">9</span></span>

<span data-ttu-id="6dadd-3992">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3992">1</span></span><br/> <span data-ttu-id="6dadd-3993">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-3993">0</span></span><br/>

<span data-ttu-id="6dadd-3994">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-3994">1</span></span>

<span data-ttu-id="6dadd-3995">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-3995">2</span></span>

<span data-ttu-id="6dadd-3996">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-3996">3</span></span>

<span data-ttu-id="6dadd-3997">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-3997">4</span></span>

<span data-ttu-id="6dadd-3998">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-3998">5</span></span>

<span data-ttu-id="6dadd-3999">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-3999">6</span></span>

<span data-ttu-id="6dadd-4000">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4000">7</span></span>

<span data-ttu-id="6dadd-4001">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4001">8</span></span>

<span data-ttu-id="6dadd-4002">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4002">9</span></span>

<span data-ttu-id="6dadd-4003">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4003">2</span></span><br/> <span data-ttu-id="6dadd-4004">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4004">0</span></span><br/>

<span data-ttu-id="6dadd-4005">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4005">1</span></span>

<span data-ttu-id="6dadd-4006">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4006">2</span></span>

<span data-ttu-id="6dadd-4007">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4007">3</span></span>

<span data-ttu-id="6dadd-4008">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4008">4</span></span>

<span data-ttu-id="6dadd-4009">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4009">5</span></span>

<span data-ttu-id="6dadd-4010">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4010">6</span></span>

<span data-ttu-id="6dadd-4011">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4011">7</span></span>

<span data-ttu-id="6dadd-4012">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4012">8</span></span>

<span data-ttu-id="6dadd-4013">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4013">9</span></span>

<span data-ttu-id="6dadd-4014">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4014">3</span></span><br/> <span data-ttu-id="6dadd-4015">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4015">0</span></span><br/>

<span data-ttu-id="6dadd-4016">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4016">1</span></span>

<span data-ttu-id="6dadd-4017">\_Hcursor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4017">\_hCursor</span></span>

<span data-ttu-id="6dadd-4018">\_chapt</span><span class="sxs-lookup"><span data-stu-id="6dadd-4018">\_chapt</span></span>

<span data-ttu-id="6dadd-4019">\_Bmk</span><span class="sxs-lookup"><span data-stu-id="6dadd-4019">\_bmk</span></span>



 

<span data-ttu-id="6dadd-4020">**\_ hCursor:** um valor de 32 bits que representa o cursor de consulta obtido de CPMCreateQueryOut para o conjuntos de linhas que contém o indicador.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4020">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="6dadd-4021">**\_ chapt:** um valor de 32 bits que representa o handle para o capítulo que contém o indicador.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4021">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="6dadd-4022">**\_ bmk:** um valor de 32 bits que representa o indicador para o qual recuperar a posição aproximada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4022">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="6dadd-4023">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4023">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="6dadd-4024">A mensagem CPMGetApproximatePositionOut responde a uma mensagem CPMGetApproximatePositionIn que descreve a posição aproximada do indicador no capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4024">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="6dadd-4025">O formato da mensagem CPMGetApproximatePositionOut que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4025">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-4026">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4026">0</span></span>

<span data-ttu-id="6dadd-4027">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4027">1</span></span>

<span data-ttu-id="6dadd-4028">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4028">2</span></span>

<span data-ttu-id="6dadd-4029">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4029">3</span></span>

<span data-ttu-id="6dadd-4030">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4030">4</span></span>

<span data-ttu-id="6dadd-4031">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4031">5</span></span>

<span data-ttu-id="6dadd-4032">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4032">6</span></span>

<span data-ttu-id="6dadd-4033">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4033">7</span></span>

<span data-ttu-id="6dadd-4034">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4034">8</span></span>

<span data-ttu-id="6dadd-4035">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4035">9</span></span>

<span data-ttu-id="6dadd-4036">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4036">1</span></span><br/> <span data-ttu-id="6dadd-4037">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4037">0</span></span><br/>

<span data-ttu-id="6dadd-4038">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4038">1</span></span>

<span data-ttu-id="6dadd-4039">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4039">2</span></span>

<span data-ttu-id="6dadd-4040">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4040">3</span></span>

<span data-ttu-id="6dadd-4041">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4041">4</span></span>

<span data-ttu-id="6dadd-4042">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4042">5</span></span>

<span data-ttu-id="6dadd-4043">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4043">6</span></span>

<span data-ttu-id="6dadd-4044">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4044">7</span></span>

<span data-ttu-id="6dadd-4045">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4045">8</span></span>

<span data-ttu-id="6dadd-4046">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4046">9</span></span>

<span data-ttu-id="6dadd-4047">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4047">2</span></span><br/> <span data-ttu-id="6dadd-4048">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4048">0</span></span><br/>

<span data-ttu-id="6dadd-4049">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4049">1</span></span>

<span data-ttu-id="6dadd-4050">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4050">2</span></span>

<span data-ttu-id="6dadd-4051">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4051">3</span></span>

<span data-ttu-id="6dadd-4052">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4052">4</span></span>

<span data-ttu-id="6dadd-4053">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4053">5</span></span>

<span data-ttu-id="6dadd-4054">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4054">6</span></span>

<span data-ttu-id="6dadd-4055">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4055">7</span></span>

<span data-ttu-id="6dadd-4056">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4056">8</span></span>

<span data-ttu-id="6dadd-4057">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4057">9</span></span>

<span data-ttu-id="6dadd-4058">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4058">3</span></span><br/> <span data-ttu-id="6dadd-4059">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4059">0</span></span><br/>

<span data-ttu-id="6dadd-4060">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4060">1</span></span>

<span data-ttu-id="6dadd-4061">\_numerator</span><span class="sxs-lookup"><span data-stu-id="6dadd-4061">\_numerator</span></span>

<span data-ttu-id="6dadd-4062">\_denominator</span><span class="sxs-lookup"><span data-stu-id="6dadd-4062">\_denominator</span></span>



 

<span data-ttu-id="6dadd-4063">**\_ numerador**: um inteiro de 32 bits sem sinal contendo o número de linha do indicador no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4063">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="6dadd-4064">Se não houver linhas, esse campo deverá ser definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4064">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="6dadd-4065">**\_ denominador**: um inteiro sem sinal de 32 bits contendo o número de linhas no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4065">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="6dadd-4066">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4066">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="6dadd-4067">A mensagem CPMCompareBmkIn solicita uma comparação de dois indicadores em um capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4067">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="6dadd-4068">O formato da mensagem CPMCompareBmkIn que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4068">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-4069">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4069">0</span></span>

<span data-ttu-id="6dadd-4070">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4070">1</span></span>

<span data-ttu-id="6dadd-4071">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4071">2</span></span>

<span data-ttu-id="6dadd-4072">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4072">3</span></span>

<span data-ttu-id="6dadd-4073">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4073">4</span></span>

<span data-ttu-id="6dadd-4074">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4074">5</span></span>

<span data-ttu-id="6dadd-4075">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4075">6</span></span>

<span data-ttu-id="6dadd-4076">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4076">7</span></span>

<span data-ttu-id="6dadd-4077">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4077">8</span></span>

<span data-ttu-id="6dadd-4078">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4078">9</span></span>

<span data-ttu-id="6dadd-4079">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4079">1</span></span><br/> <span data-ttu-id="6dadd-4080">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4080">0</span></span><br/>

<span data-ttu-id="6dadd-4081">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4081">1</span></span>

<span data-ttu-id="6dadd-4082">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4082">2</span></span>

<span data-ttu-id="6dadd-4083">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4083">3</span></span>

<span data-ttu-id="6dadd-4084">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4084">4</span></span>

<span data-ttu-id="6dadd-4085">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4085">5</span></span>

<span data-ttu-id="6dadd-4086">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4086">6</span></span>

<span data-ttu-id="6dadd-4087">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4087">7</span></span>

<span data-ttu-id="6dadd-4088">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4088">8</span></span>

<span data-ttu-id="6dadd-4089">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4089">9</span></span>

<span data-ttu-id="6dadd-4090">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4090">2</span></span><br/> <span data-ttu-id="6dadd-4091">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4091">0</span></span><br/>

<span data-ttu-id="6dadd-4092">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4092">1</span></span>

<span data-ttu-id="6dadd-4093">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4093">2</span></span>

<span data-ttu-id="6dadd-4094">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4094">3</span></span>

<span data-ttu-id="6dadd-4095">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4095">4</span></span>

<span data-ttu-id="6dadd-4096">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4096">5</span></span>

<span data-ttu-id="6dadd-4097">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4097">6</span></span>

<span data-ttu-id="6dadd-4098">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4098">7</span></span>

<span data-ttu-id="6dadd-4099">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4099">8</span></span>

<span data-ttu-id="6dadd-4100">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4100">9</span></span>

<span data-ttu-id="6dadd-4101">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4101">3</span></span><br/> <span data-ttu-id="6dadd-4102">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4102">0</span></span><br/>

<span data-ttu-id="6dadd-4103">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4103">1</span></span>

<span data-ttu-id="6dadd-4104">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4104">\_hCursor</span></span>

<span data-ttu-id="6dadd-4105">\_chapt</span><span class="sxs-lookup"><span data-stu-id="6dadd-4105">\_chapt</span></span>

<span data-ttu-id="6dadd-4106">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="6dadd-4106">\_bmkFirst</span></span>

<span data-ttu-id="6dadd-4107">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="6dadd-4107">\_bmkSecond</span></span>



 

<span data-ttu-id="6dadd-4108">\_**hCursor**: um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut para o conjunto de linhas que contém os indicadores.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4108">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="6dadd-4109">\_**chapt**: um valor de 32 bits que representa o identificador do capítulo que contém os indicadores a serem comparados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4109">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="6dadd-4110">\_**bmkFirst**: um valor de 32 bits que representa o identificador para o primeiro indicador a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4110">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="6dadd-4111">\_**bmkSecond**: um valor de 32 bits que representa o identificador para o segundo indicador a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4111">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="6dadd-4112">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4112">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="6dadd-4113">A mensagem CPMCompareBmkOut responde a uma mensagem CPMCompareBmkIn com a comparação dos dois indicadores no capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4113">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="6dadd-4114">O formato da mensagem CPMCompareBmkOut que segue o cabeçalho é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4114">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-4115">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4115">0</span></span>

<span data-ttu-id="6dadd-4116">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4116">1</span></span>

<span data-ttu-id="6dadd-4117">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4117">2</span></span>

<span data-ttu-id="6dadd-4118">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4118">3</span></span>

<span data-ttu-id="6dadd-4119">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4119">4</span></span>

<span data-ttu-id="6dadd-4120">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4120">5</span></span>

<span data-ttu-id="6dadd-4121">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4121">6</span></span>

<span data-ttu-id="6dadd-4122">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4122">7</span></span>

<span data-ttu-id="6dadd-4123">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4123">8</span></span>

<span data-ttu-id="6dadd-4124">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4124">9</span></span>

<span data-ttu-id="6dadd-4125">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4125">1</span></span><br/> <span data-ttu-id="6dadd-4126">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4126">0</span></span><br/>

<span data-ttu-id="6dadd-4127">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4127">1</span></span>

<span data-ttu-id="6dadd-4128">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4128">2</span></span>

<span data-ttu-id="6dadd-4129">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4129">3</span></span>

<span data-ttu-id="6dadd-4130">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4130">4</span></span>

<span data-ttu-id="6dadd-4131">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4131">5</span></span>

<span data-ttu-id="6dadd-4132">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4132">6</span></span>

<span data-ttu-id="6dadd-4133">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4133">7</span></span>

<span data-ttu-id="6dadd-4134">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4134">8</span></span>

<span data-ttu-id="6dadd-4135">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4135">9</span></span>

<span data-ttu-id="6dadd-4136">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4136">2</span></span><br/> <span data-ttu-id="6dadd-4137">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4137">0</span></span><br/>

<span data-ttu-id="6dadd-4138">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4138">1</span></span>

<span data-ttu-id="6dadd-4139">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4139">2</span></span>

<span data-ttu-id="6dadd-4140">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4140">3</span></span>

<span data-ttu-id="6dadd-4141">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4141">4</span></span>

<span data-ttu-id="6dadd-4142">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4142">5</span></span>

<span data-ttu-id="6dadd-4143">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4143">6</span></span>

<span data-ttu-id="6dadd-4144">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4144">7</span></span>

<span data-ttu-id="6dadd-4145">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4145">8</span></span>

<span data-ttu-id="6dadd-4146">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4146">9</span></span>

<span data-ttu-id="6dadd-4147">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4147">3</span></span><br/> <span data-ttu-id="6dadd-4148">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4148">0</span></span><br/>

<span data-ttu-id="6dadd-4149">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4149">1</span></span>

<span data-ttu-id="6dadd-4150">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="6dadd-4150">\_dwComparison</span></span>



 

<span data-ttu-id="6dadd-4151">\_**dwComparison**: um dos valores a seguir, indicando as posições relativas dos dois indicadores no capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4151">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="6dadd-4152">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4152">Value</span></span>                               | <span data-ttu-id="6dadd-4153">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-4153">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6dadd-4154">DBCOMPARE \_ LT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-4154">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="6dadd-4155">O primeiro indicador é posicionado antes do segundo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4155">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="6dadd-4156">DbCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="6dadd-4156">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="6dadd-4157">O primeiro indicador tem a mesma posição que o segundo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4157">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="6dadd-4158">DBCOMPARE \_ GT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="6dadd-4158">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="6dadd-4159">O primeiro indicador é posicionado após o segundo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4159">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="6dadd-4160">DBCOMPARE \_ NE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="6dadd-4160">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="6dadd-4161">O primeiro indicador não tem a mesma posição que o segundo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4161">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="6dadd-4162">DBCOMPARE \_ NOTCOMPARABLE 0X00000004</span><span class="sxs-lookup"><span data-stu-id="6dadd-4162">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="6dadd-4163">O primeiro indicador não é comparável ao segundo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4163">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="6dadd-4164">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4164">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="6dadd-4165">A mensagem CPMRestartPositionIn move a posição de busca de um cursor para o início do capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4165">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="6dadd-4166">Conforme especificado na seção 3.1.5.2.12, o servidor responderá usando a mesma mensagem, com os resultados da solicitação contidos no campo de status do \_ header do CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4166">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="6dadd-4167">O formato da mensagem CPMRestartPositionIn que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4167">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-4168">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4168">0</span></span>

<span data-ttu-id="6dadd-4169">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4169">1</span></span>

<span data-ttu-id="6dadd-4170">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4170">2</span></span>

<span data-ttu-id="6dadd-4171">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4171">3</span></span>

<span data-ttu-id="6dadd-4172">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4172">4</span></span>

<span data-ttu-id="6dadd-4173">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4173">5</span></span>

<span data-ttu-id="6dadd-4174">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4174">6</span></span>

<span data-ttu-id="6dadd-4175">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4175">7</span></span>

<span data-ttu-id="6dadd-4176">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4176">8</span></span>

<span data-ttu-id="6dadd-4177">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4177">9</span></span>

<span data-ttu-id="6dadd-4178">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4178">1</span></span><br/> <span data-ttu-id="6dadd-4179">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4179">0</span></span><br/>

<span data-ttu-id="6dadd-4180">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4180">1</span></span>

<span data-ttu-id="6dadd-4181">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4181">2</span></span>

<span data-ttu-id="6dadd-4182">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4182">3</span></span>

<span data-ttu-id="6dadd-4183">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4183">4</span></span>

<span data-ttu-id="6dadd-4184">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4184">5</span></span>

<span data-ttu-id="6dadd-4185">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4185">6</span></span>

<span data-ttu-id="6dadd-4186">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4186">7</span></span>

<span data-ttu-id="6dadd-4187">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4187">8</span></span>

<span data-ttu-id="6dadd-4188">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4188">9</span></span>

<span data-ttu-id="6dadd-4189">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4189">2</span></span><br/> <span data-ttu-id="6dadd-4190">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4190">0</span></span><br/>

<span data-ttu-id="6dadd-4191">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4191">1</span></span>

<span data-ttu-id="6dadd-4192">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4192">2</span></span>

<span data-ttu-id="6dadd-4193">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4193">3</span></span>

<span data-ttu-id="6dadd-4194">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4194">4</span></span>

<span data-ttu-id="6dadd-4195">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4195">5</span></span>

<span data-ttu-id="6dadd-4196">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4196">6</span></span>

<span data-ttu-id="6dadd-4197">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4197">7</span></span>

<span data-ttu-id="6dadd-4198">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4198">8</span></span>

<span data-ttu-id="6dadd-4199">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4199">9</span></span>

<span data-ttu-id="6dadd-4200">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4200">3</span></span><br/> <span data-ttu-id="6dadd-4201">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4201">0</span></span><br/>

<span data-ttu-id="6dadd-4202">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4202">1</span></span>

<span data-ttu-id="6dadd-4203">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4203">\_hCursor (optional)</span></span>

<span data-ttu-id="6dadd-4204">\_chapt (opcional)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4204">\_chapt (optional)</span></span>



 

<span data-ttu-id="6dadd-4205">**\_ hCursor:** um valor de 32 bits que representa o identificador, obtido de uma mensagem CPMCreateQueryOut, que identifica a consulta para a qual reiniciar a posição.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4205">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="6dadd-4206">Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4206">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="6dadd-4207">**\_ chapt:** um valor de 32 bits que representa o alça de um capítulo do qual recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4207">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="6dadd-4208">Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4208">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="6dadd-4209">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4209">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="6dadd-4210">A mensagem CPMFreeCursorIn solicita a liberação de um cursor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4210">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="6dadd-4211">O formato da mensagem CPMFreeCursorIn que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4211">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="6dadd-4212">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4212">0</span></span>

<span data-ttu-id="6dadd-4213">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4213">1</span></span>

<span data-ttu-id="6dadd-4214">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4214">2</span></span>

<span data-ttu-id="6dadd-4215">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4215">3</span></span>

<span data-ttu-id="6dadd-4216">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4216">4</span></span>

<span data-ttu-id="6dadd-4217">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4217">5</span></span>

<span data-ttu-id="6dadd-4218">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4218">6</span></span>

<span data-ttu-id="6dadd-4219">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4219">7</span></span>

<span data-ttu-id="6dadd-4220">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4220">8</span></span>

<span data-ttu-id="6dadd-4221">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4221">9</span></span>

<span data-ttu-id="6dadd-4222">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4222">1</span></span><br/> <span data-ttu-id="6dadd-4223">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4223">0</span></span><br/>

<span data-ttu-id="6dadd-4224">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4224">1</span></span>

<span data-ttu-id="6dadd-4225">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4225">2</span></span>

<span data-ttu-id="6dadd-4226">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4226">3</span></span>

<span data-ttu-id="6dadd-4227">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4227">4</span></span>

<span data-ttu-id="6dadd-4228">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4228">5</span></span>

<span data-ttu-id="6dadd-4229">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4229">6</span></span>

<span data-ttu-id="6dadd-4230">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4230">7</span></span>

<span data-ttu-id="6dadd-4231">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4231">8</span></span>

<span data-ttu-id="6dadd-4232">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4232">9</span></span>

<span data-ttu-id="6dadd-4233">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4233">2</span></span><br/> <span data-ttu-id="6dadd-4234">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4234">0</span></span><br/>

<span data-ttu-id="6dadd-4235">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4235">1</span></span>

<span data-ttu-id="6dadd-4236">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4236">2</span></span>

<span data-ttu-id="6dadd-4237">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4237">3</span></span>

<span data-ttu-id="6dadd-4238">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4238">4</span></span>

<span data-ttu-id="6dadd-4239">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4239">5</span></span>

<span data-ttu-id="6dadd-4240">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4240">6</span></span>

<span data-ttu-id="6dadd-4241">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4241">7</span></span>

<span data-ttu-id="6dadd-4242">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4242">8</span></span>

<span data-ttu-id="6dadd-4243">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4243">9</span></span>

<span data-ttu-id="6dadd-4244">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4244">3</span></span><br/> <span data-ttu-id="6dadd-4245">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4245">0</span></span><br/>

<span data-ttu-id="6dadd-4246">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4246">1</span></span>

<span data-ttu-id="6dadd-4247">\_Hcursor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4247">\_hCursor</span></span>



 

<span data-ttu-id="6dadd-4248">**\_ hCursor:** um valor de 32 bits que representa o handle do cursor da mensagem CPMCreateQueryOut a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4248">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="6dadd-4249">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4249">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="6dadd-4250">A mensagem CPMFreeCursorOut responde a uma mensagem CPMFreeCursorIn com os resultados da liberação de um cursor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4250">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="6dadd-4251">O formato da mensagem CPMFreeCursorOut que segue o header é:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4251">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="6dadd-4252">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4252">0</span></span>

<span data-ttu-id="6dadd-4253">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4253">1</span></span>

<span data-ttu-id="6dadd-4254">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4254">2</span></span>

<span data-ttu-id="6dadd-4255">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4255">3</span></span>

<span data-ttu-id="6dadd-4256">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4256">4</span></span>

<span data-ttu-id="6dadd-4257">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4257">5</span></span>

<span data-ttu-id="6dadd-4258">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4258">6</span></span>

<span data-ttu-id="6dadd-4259">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4259">7</span></span>

<span data-ttu-id="6dadd-4260">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4260">8</span></span>

<span data-ttu-id="6dadd-4261">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4261">9</span></span>

<span data-ttu-id="6dadd-4262">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4262">1</span></span><br/> <span data-ttu-id="6dadd-4263">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4263">0</span></span><br/>

<span data-ttu-id="6dadd-4264">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4264">1</span></span>

<span data-ttu-id="6dadd-4265">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4265">2</span></span>

<span data-ttu-id="6dadd-4266">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4266">3</span></span>

<span data-ttu-id="6dadd-4267">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4267">4</span></span>

<span data-ttu-id="6dadd-4268">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4268">5</span></span>

<span data-ttu-id="6dadd-4269">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4269">6</span></span>

<span data-ttu-id="6dadd-4270">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4270">7</span></span>

<span data-ttu-id="6dadd-4271">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4271">8</span></span>

<span data-ttu-id="6dadd-4272">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4272">9</span></span>

<span data-ttu-id="6dadd-4273">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4273">2</span></span><br/> <span data-ttu-id="6dadd-4274">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4274">0</span></span><br/>

<span data-ttu-id="6dadd-4275">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4275">1</span></span>

<span data-ttu-id="6dadd-4276">2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4276">2</span></span>

<span data-ttu-id="6dadd-4277">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4277">3</span></span>

<span data-ttu-id="6dadd-4278">4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4278">4</span></span>

<span data-ttu-id="6dadd-4279">5</span><span class="sxs-lookup"><span data-stu-id="6dadd-4279">5</span></span>

<span data-ttu-id="6dadd-4280">6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4280">6</span></span>

<span data-ttu-id="6dadd-4281">7</span><span class="sxs-lookup"><span data-stu-id="6dadd-4281">7</span></span>

<span data-ttu-id="6dadd-4282">8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4282">8</span></span>

<span data-ttu-id="6dadd-4283">9</span><span class="sxs-lookup"><span data-stu-id="6dadd-4283">9</span></span>

<span data-ttu-id="6dadd-4284">3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4284">3</span></span><br/> <span data-ttu-id="6dadd-4285">0</span><span class="sxs-lookup"><span data-stu-id="6dadd-4285">0</span></span><br/>

<span data-ttu-id="6dadd-4286">1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4286">1</span></span>

<span data-ttu-id="6dadd-4287">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="6dadd-4287">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="6dadd-4288">**\_ cCursorsRemaining:** um inteiro sem sinal de 32 bits que indica o número de cursores ainda em uso para a consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4288">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="6dadd-4289">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="6dadd-4289">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="6dadd-4290">A mensagem CPMDisconnect encerra a conexão com o servidor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4290">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="6dadd-4291">A mensagem NÃO DEVE incluir um corpo; somente o header da mensagem, conforme especificado na Seção 2.2.2 deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4291">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="6dadd-4292">2.2.4 Erros</span><span class="sxs-lookup"><span data-stu-id="6dadd-4292">2.2.4 Errors</span></span>

<span data-ttu-id="6dadd-4293">Todas as mensagens do Protocolo do Serviço de Indexação de Conteúdo DEVEM retornar 0x00000000 êxito; caso contrário, eles retornarão um código de erro de 32 bits diferente de zero que pode ser um HRESULT ou um valor NTSTATUS (consulte a seção 1.8).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4293">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="6dadd-4294">Se um buffer for muito pequeno para se ajustar a um resultado, um código de status de STATUS \_ INSUFFICIENT RESOURCES (0xC0000009A) DEVERÁ ser retornado e a operação com falha deverá ser recuperada com um \_ buffer maior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4294">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="6dadd-4295">Todos os outros valores de erro DEVEM ser tratados da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4295">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="6dadd-4296">(Observe que, atualmente, os espaços de numeração HRESULT e NTSTATUS não se sobrepõem, exceto com valores de significado idêntico, mas mesmo se fossem conflitos no futuro, isso não causaria problemas de protocolo, desde que o valor para STATUS \_ RECURSOS \_ INSUFICIENTES permanecem exclusivos, pois todos os outros valores de erro são tratados da mesma forma.)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4296">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="6dadd-4297">3 Detalhes do protocolo</span><span class="sxs-lookup"><span data-stu-id="6dadd-4297">3 Protocol Details</span></span>

-   [<span data-ttu-id="6dadd-4298">3.1 Detalhes do servidor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4298">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="6dadd-4299">3.2 Detalhes do cliente</span><span class="sxs-lookup"><span data-stu-id="6dadd-4299">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="6dadd-4300">As solicitações de mensagem cisp para consultar remotamente os catálogos de serviço de indexação não exigem nenhuma sequência específica.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4300">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="6dadd-4301">No entanto, é aconselhável que a camada superior adera a uma sequência de mensagens significativa, quanto às mensagens recebidas fora dessa sequência ou com dados inválidos, o servidor responderá com um erro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4301">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="6dadd-4302">Algumas mensagens também dependem da camada superior, fornecendo dados válidos que foram recebidos em mensagens anteriormente na sequência.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4302">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="6dadd-4303">Uma sequência de mensagens típica para uma consulta simples de um cliente para um computador remoto é ilustrada no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4303">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![sequência de mensagens para consulta simples](images/protocoldetails.jpg)

<span data-ttu-id="6dadd-4305">As mensagens representadas no diagrama anterior representam um subconjunto de todas as mensagens CISP usadas para consultar um catálogo de serviços de indexação remota.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4305">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="6dadd-4306">3.1 Detalhes do servidor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4306">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="6dadd-4307">3.1.1 Modelo de dados abstratos</span><span class="sxs-lookup"><span data-stu-id="6dadd-4307">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="6dadd-4308">A seção a seguir especifica os dados e o estado mantidos pelo servidor CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4308">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="6dadd-4309">Os dados fornecidos aqui são para facilitar a explicação de como o protocolo se comporta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4309">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="6dadd-4310">Esta seção não determina que as implementações aderam a esse modelo, desde que seu comportamento externo seja consistente com o descrito neste documento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4310">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="6dadd-4311">Um serviço de indexação que implementa o CISP DEVE manter os seguintes elementos de dados abstratos:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4311">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="6dadd-4312">A lista de clientes conectados ao servidor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4312">The list of clients connected to the server</span></span>
-   <span data-ttu-id="6dadd-4313">Informações sobre cada cliente, que inclui:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4313">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="6dadd-4314">Versão do cliente (conforme indicado na mensagem CPMConnectIn especificada na seção 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4314">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="6dadd-4315">Catálogo associado ao cliente (por uma mensagem CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4315">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="6dadd-4316">Propriedades adicionais do cliente, conforme especificado na seção 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4316">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="6dadd-4317">Consulta de pesquisa do cliente</span><span class="sxs-lookup"><span data-stu-id="6dadd-4317">Client's search query</span></span>
    -   <span data-ttu-id="6dadd-4318">Lista de alças de cursor para a consulta e a posição no conjunto de resultados para cada alça.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4318">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="6dadd-4319">Conjunto atual de vinculações</span><span class="sxs-lookup"><span data-stu-id="6dadd-4319">Current set of bindings</span></span>
    -   <span data-ttu-id="6dadd-4320">Status atual da consulta que inclui (para cada cursor):</span><span class="sxs-lookup"><span data-stu-id="6dadd-4320">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="6dadd-4321">Número de linhas no resultado da consulta</span><span class="sxs-lookup"><span data-stu-id="6dadd-4321">Number of rows in query result</span></span>
        -   <span data-ttu-id="6dadd-4322">Numerador e denominador da conclusão da consulta</span><span class="sxs-lookup"><span data-stu-id="6dadd-4322">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="6dadd-4323">Último número de linhas, relatado pela mensagem CPMRatioFinishedOut mais recente para este cursor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4323">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="6dadd-4324">Se a consulta é monitorada pelo servidor quanto a alterações nos resultados da consulta e se ela é monitorada, o que mudou nos resultados da consulta desde que foi relatado pela última vez ao cliente pelo CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4324">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="6dadd-4325">Lista de alças de capítulos, atendidas por essa consulta a um cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4325">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="6dadd-4326">Lista de alças de indicador para cada cursor, atendida por essa consulta a um cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4326">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="6dadd-4327">O estado atual do serviço de indexação, que pode ser "não inicializado", "em execução" ou "desligando".</span><span class="sxs-lookup"><span data-stu-id="6dadd-4327">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="6dadd-4328">Observe que, na maioria das vezes, o servidor está no estado "em execução".</span><span class="sxs-lookup"><span data-stu-id="6dadd-4328">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="6dadd-4329">A seguir está o diagrama do computador de estado para o servidor:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4329">Following is the state machine diagram for the server:</span></span>

    ![diagrama do computador de estado do servidor de serviço de indexação](images/abstractdatamodel.jpg)

-   <span data-ttu-id="6dadd-4331">Informações por catálogo: número de documentos indexados, tamanho do índice, número de chaves exclusivas, etc (consulte a seção 2.2.3.1 para obter a lista completa), estado (que corresponde aos valores de dwNewState na seção 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4331">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="6dadd-4332">Para cada idioma com suporte, um banco de dados de variações de palavras, conforme discutido na seção 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4332">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="6dadd-4333">3.1.2 Temporizadores</span><span class="sxs-lookup"><span data-stu-id="6dadd-4333">3.1.2 Timers</span></span>

<span data-ttu-id="6dadd-4334">Nenhum temporizador de protocolo é necessário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4334">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="6dadd-4335">3.1.3 Inicialização</span><span class="sxs-lookup"><span data-stu-id="6dadd-4335">3.1.3 Initialization</span></span>

<span data-ttu-id="6dadd-4336">Na inicialização, o servidor deve definir seu estado como "não inicializado" e começar a escutar mensagens no pipe nomeado especificado na seção 1,9.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4336">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="6dadd-4337">Depois de fazer qualquer outra inicialização interna, ela deve fazer a transição para o estado "em execução".</span><span class="sxs-lookup"><span data-stu-id="6dadd-4337">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="6dadd-4338">3.1.4 Eventos disparados de camada superior</span><span class="sxs-lookup"><span data-stu-id="6dadd-4338">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="6dadd-4339">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4339">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="6dadd-4340">Processamento de mensagens 3.1.5 e regras de sequenciamento</span><span class="sxs-lookup"><span data-stu-id="6dadd-4340">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="6dadd-4341">Sempre que ocorrer um erro durante o processamento de uma mensagem enviada por um cliente, o servidor deverá relatar um erro de volta ao cliente da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4341">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="6dadd-4342">Parar o processamento da mensagem enviada pelo cliente</span><span class="sxs-lookup"><span data-stu-id="6dadd-4342">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="6dadd-4343">Responda com o cabeçalho da mensagem (somente) da mensagem enviada pelo cliente, mantendo o \_ campo msg intacto.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4343">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="6dadd-4344">Defina o \_ campo status para o valor do código de erro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4344">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="6dadd-4345">Quando uma mensagem chega, o servidor deve verificar o \_ valor do campo msg para ver se ele é um tipo conhecido (consulte a seção 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4345">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="6dadd-4346">Se o tipo não for conhecido, ele deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4346">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="6dadd-4347">O servidor deve validar o \_ valor do campo ulChecksum se o tipo de mensagem for um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4347">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="6dadd-4348">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4348">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="6dadd-4349">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4349">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="6dadd-4350">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4350">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="6dadd-4351">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4351">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="6dadd-4352">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4352">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="6dadd-4353">Para validar o \_ valor do campo ulChecksum, o servidor deve verificar o valor especificado pelo cliente no \_ campo iClientVersion da mensagem CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4353">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="6dadd-4354">Se o \_ campo iClientVersion não estiver definido como 0x00000008 e o \_ campo ulChecksum não estiver definido como 0x00000000, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4354">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="6dadd-4355">O servidor não deve validar o \_ campo ulChecksum para clientes defina o \_ campo iClientVersion com um valor menor que 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4355">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="6dadd-4356">Se o \_ valor do campo iClientVersionfield for 0x00000008 ou superior, o servidor deverá validar que o \_ campo ulChecksum foi calculado conforme especificado na seção 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4356">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="6dadd-4357">Se o \_ valor de ulChecksum for inválido, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0XC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4357">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="6dadd-4358">Em seguida, o servidor verifica em qual estado ele está.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4358">Next, the server checks which state is it in.</span></span> <span data-ttu-id="6dadd-4359">Se seu estado for "não inicializado", o servidor deverá relatar \_ um \_ erro CI E não \_ inicializado (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4359">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="6dadd-4360">Se o estado for "desligando", o servidor deverá relatar \_ um \_ erro de desligamento CI E Shutdown (0x80041812).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4360">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="6dadd-4361">Depois que um cabeçalho for determinado como válido e o servidor estar no estado "em execução", o processamento adicional específico à mensagem deverá ser feito conforme especificado nas subseções abaixo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4361">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="6dadd-4362">Gerenciamento de catálogo do serviço de indexação remota do 3.1.5.1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4362">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="6dadd-4363">3.1.5.1.1 recebendo uma solicitação CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4363">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="6dadd-4364">Quando o servidor recebe uma solicitação de mensagem CPMCIStateInOut do cliente, o servidor deve primeiro verificar se o cliente está em uma lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4364">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="6dadd-4365">Se o cliente não estiver na lista, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4365">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="6dadd-4366">Caso contrário, ele deve responder ao cliente com uma mensagem CPMCIStateInOut, preenchendo-o com informações sobre o catálogo associado do cliente, conforme especificado na seção 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4366">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="6dadd-4367">3.1.5.1.2 recebendo uma solicitação CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4367">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="6dadd-4368">Quando o servidor recebe uma solicitação de mensagem CPMSetCatStateIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4368">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4369">Verifique se o cliente tem acesso administrativo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4369">Check that client has administrative access.</span></span> <span data-ttu-id="6dadd-4370">Se o cliente não tiver acesso administrativo, o servidor deverá relatar um erro de STATUS de \_ acesso \_ negado (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4370">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="6dadd-4371">Se \_ dwNewState não for igual a CICAT \_ todos \_ abertos, altere o estado do catálogo especificado no campo CatName conforme especificado pelo \_ campo dwNewState.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4371">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="6dadd-4372">Consulte a seção 2.2.3.2 para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4372">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="6dadd-4373">Se o servidor não localizar um catálogo com o nome especificado no campo CatName, o servidor deverá retornar um \_ erro de parâmetro inválido \_ (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4373">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4374">Responda ao cliente com uma mensagem CPMSetCatStateOut, em que \_ DWOLDSTATE deve ser definido como o estado anterior do catálogo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4374">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="6dadd-4375">Se \_ dwNewState for igual a CICAT \_ todos \_ abertos, o servidor deverá verificar o status de todos os catálogos e, se todos eles forem iniciados, ele deverá definir \_ dwOldState como 0x00000001 e, caso contrário, definirá \_ dwOldState como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4375">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="6dadd-4376">3.1.5.1.3 recebendo uma solicitação CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4376">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="6dadd-4377">Quando o servidor recebe uma solicitação de mensagem CPMUpdateDocumentsIn, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4377">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4378">Verifique se o cliente está em uma lista de clientes conectados (que têm um catálogo associado).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4378">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="6dadd-4379">Se o cliente não estiver na lista, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4379">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4380">Verifique se o cliente tem acesso administrativo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4380">Check that client has administrative access.</span></span> <span data-ttu-id="6dadd-4381">Se o cliente não tiver acesso administrativo ao servidor, o servidor deverá relatar um erro de STATUS de \_ acesso \_ negado (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4381">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="6dadd-4382">Inicie o processo de indexação do caminho especificado pelo cliente, fazendo uma verificação completa ou incremental, dependendo do valor do \_ campo sinalizador na mensagem CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4382">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="6dadd-4383">Se o caminho não tiver sido indexado anteriormente, ele deverá ser adicionado à coleção de locais indexados e uma verificação completa realizada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4383">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="6dadd-4384">Se um valor ilegal do \_ campo flag for especificado, o servidor deverá agir como se o \_ sinalizador fosse definido como UPD \_ init e executar uma verificação completa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4384">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="6dadd-4385">Esta operação deve ser executada no catálogo associado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4385">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="6dadd-4386">Responda ao cliente com o cabeçalho da mensagem para o CPMUpdateDocumentsIn e defina o \_ campo status para os resultados da solicitação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4386">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="6dadd-4387">3.1.5.1.4 recebendo uma solicitação CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4387">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="6dadd-4388">Quando o servidor recebe uma solicitação de mensagem CPMForceMergeIn, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4388">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4389">Verifique se o cliente está em uma lista de clientes conectados (que têm um catálogo associado).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4389">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="6dadd-4390">Se o cliente não estiver na lista, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4390">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4391">Verifique se o cliente tem acesso administrativo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4391">Check that client has administrative access.</span></span> <span data-ttu-id="6dadd-4392">Se o cliente não tiver acesso administrativo, o servidor deverá relatar um erro de STATUS de \_ acesso \_ negado (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4392">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="6dadd-4393">Inicie qualquer processo de manutenção necessário para melhorar o desempenho de consulta em um catálogo, associado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4393">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="6dadd-4394">Responda ao cliente com um cabeçalho de mensagem para o CPMForceMergeIn e defina o \_ campo status para os resultados da solicitação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4394">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="6dadd-4395">Observe que o processo de manutenção é assíncrono e pode continuar depois que o cliente recebe a mensagem de resposta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4395">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="6dadd-4396">Esse processo não afeta diretamente o protocolo de nenhuma forma (além do tempo de resposta).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4396">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="6dadd-4397">Consulta do serviço de indexação remota do 3.1.5.2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4397">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="6dadd-4398">3.1.5.2.1 recebendo uma solicitação CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4398">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="6dadd-4399">Quando o servidor recebe uma solicitação CPMConnectIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4399">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4400">Verifique se o cliente está na lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4400">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="6dadd-4401">Se esse for o caso, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4401">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4402">Verifica se o catálogo especificado existe e não está no estado parado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4402">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="6dadd-4403">Se esse não for o caso, o servidor deverá ter um erro de CI \_ E \_ nenhum \_ catálogo (0x8004181D) de relatório.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4403">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="6dadd-4404">Adicione o cliente à lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4404">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="6dadd-4405">Associe o catálogo ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4405">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="6dadd-4406">Armazene as informações passadas na mensagem CPMConnectIn (como nome do catálogo, versão do cliente, etc.) no estado do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4406">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="6dadd-4407">Responda ao cliente com uma mensagem CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4407">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="6dadd-4408">3.1.5.2.2 recebendo uma solicitação CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4408">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="6dadd-4409">Quando o servidor recebe uma solicitação de mensagem CPMCreateQueryIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4409">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4410">Verifique se o cliente está na lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4410">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="6dadd-4411">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4411">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4412">Verifique se o cliente já tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4412">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="6dadd-4413">Se esse for o caso, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4413">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4414">Verifique se o catálogo associado ao cliente está no estado que permite que a consulta seja processada (CICAT \_ ReadOnly ou CICAT \_ gravável).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4414">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="6dadd-4415">Se esse não for o caso, o servidor deverá relatar um \_ erro de \_ 0x8004160C (consulta S sem \_ consulta).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4415">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="6dadd-4416">Analise o conjunto de restrições, as ordens de classificação e os agrupamentos especificados na consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4416">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="6dadd-4417">Se o servidor encontrar um erro, ele deverá relatar um erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4417">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="6dadd-4418">Se essa etapa falhar por qualquer outro motivo, o servidor deverá relatar o erro encontrado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4418">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="6dadd-4419">Para obter informações sobre erros de consulta de serviço de indexação, consulte \[ msdn-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="6dadd-4419">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="6dadd-4420">Salve a consulta de pesquisa no estado do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4420">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="6dadd-4421">Faça qualquer preparação necessária para atender linhas a um cliente e associar a consulta a identificadores de cursor apropriados (dependendo das informações passadas na mensagem CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4421">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="6dadd-4422">Adicione esses identificadores à lista de identificadores de cursor do cliente e inicialize as listas de identificadores e indicadores de capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4422">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="6dadd-4423">Inicializar a lista de identificadores de capítulo para cada cursor nesta consulta para DB \_ NULL \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="6dadd-4423">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="6dadd-4424">Inicializar a lista de identificadores de indicadores para cada cursor nesta consulta para um conjunto de DBBMK \_ First e DBBMK \_ Last.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4424">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="6dadd-4425">Marque a consulta como não monitorado para alterações.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4425">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="6dadd-4426">Inicialize o número de linhas para o número de linhas calculado no momento (que pode ser 0 se a consulta não começar a ser executada ou algum número se a consulta estiver em um processo de execução) e inicialize o numerador e o denominador da conclusão da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4426">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="6dadd-4427">Responda ao cliente com uma mensagem CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4427">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="6dadd-4428">3.1.5.2.3 recebendo uma solicitação CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4428">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="6dadd-4429">Quando o servidor recebe uma solicitação de mensagem CPMGetQueryStatusIn de um cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4429">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4430">Verifique se o cliente tem a consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4430">Check if the client has query associated with it.</span></span> <span data-ttu-id="6dadd-4431">Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4431">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4432">Verifique se o cursor handle está em uma lista de alças de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4432">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="6dadd-4433">Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4433">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4434">Prepare uma mensagem CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4434">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="6dadd-4435">O servidor DEVE recuperar o status atual da consulta e defini-lo no campo \_ QStatus (consulte 2.2.3.11 para obter valores possíveis).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4435">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="6dadd-4436">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4436">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="6dadd-4437">Responda ao cliente com a mensagem CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4437">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="6dadd-4438">3.1.5.2.4 Recebendo uma solicitação CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4438">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="6dadd-4439">Quando o servidor recebe uma solicitação de mensagem CPMGetQueryStatusExIn de um cliente, o servidor DEVE fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4439">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4440">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4440">Check if the client has a query associated with it.</span></span> <span data-ttu-id="6dadd-4441">Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4441">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4442">Verifique se o cursor passado está em uma lista de alças de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4442">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="6dadd-4443">Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4443">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4444">Prepare uma mensagem CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4444">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="6dadd-4445">O servidor DEVE recuperar o status atual da consulta e o progresso da consulta e definir QStatus (consulte 2.2.3.11 para obter valores possíveis), \_ dwRatioFinishedDenominator e \_ dwRatioFinishedNumerator, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4445">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="6dadd-4446">Em seguida, ele DEVE definir o número de linhas nos resultados da consulta \_ como cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4446">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="6dadd-4447">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4447">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="6dadd-4448">Recupere informações sobre o catálogo do cliente e preencha \_ cFilteredDocuments e \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4448">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="6dadd-4449">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4449">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="6dadd-4450">Recupere a posição do indicador indicada pelo handle no campo bmk e preencha o campo iRowBmk restante na mensagem \_ \_ CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4450">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="6dadd-4451">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4451">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="6dadd-4452">Responda ao cliente com a mensagem CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4452">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="6dadd-4453">3.1.5.2.5 Recebendo uma solicitação CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4453">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="6dadd-4454">Quando o servidor recebe uma solicitação de mensagem CPMRatioFinishedIn de um cliente, o servidor DEVE fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4454">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4455">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4455">Check if the client has query associated with it.</span></span> <span data-ttu-id="6dadd-4456">Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4456">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4457">Verifique se o cursor passado está na lista de alças de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4457">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="6dadd-4458">Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4458">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4459">Prepare uma mensagem CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4459">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="6dadd-4460">O servidor DEVE recuperar o status da consulta do cliente e preencher os campos \_ ulNumerator, \_ ulDenominator e \_ cRows.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4460">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="6dadd-4461">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4461">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="6dadd-4462">Se cRows for igual ao último número relatado de linhas para essa consulta, de definido \_ fNewRows como 0x00000000, caso contrário, de definido como \_ 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4462">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="6dadd-4463">Atualize o último número relatado de linhas para essa consulta para o valor \_ de cRows.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4463">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="6dadd-4464">Responda ao cliente com a mensagem CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4464">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="6dadd-4465">3.1.5.2.6 Recebendo uma solicitação CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4465">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="6dadd-4466">Quando o servidor recebe uma solicitação de mensagem CPMSetBindingsIn de um cliente, o servidor DEVE fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4466">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4467">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4467">Check if the client has a query associated with it.</span></span> <span data-ttu-id="6dadd-4468">Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4468">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4469">Verifique se o cursor passado está na lista de alças de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4469">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="6dadd-4470">Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4470">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4471">Verifique se as informações de associação são válidas (ou seja, a coluna pelo menos especifica o valor, o comprimento ou o status a ser retornado; nenhuma sobreposição nas vinculações para valor, tamanho ou status; e valor, tamanho e status se ajustam ao tamanho da linha especificado) e, se não relatar um erro de BD \_ \_ E BADBINDINFO (0x80040E08).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4471">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="6dadd-4472">Salve as informações de associação associadas às colunas especificadas no campo aColumns.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4472">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="6dadd-4473">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4473">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="6dadd-4474">Responda ao cliente com um header de mensagem (somente) com msg definido como \_ CPMSetBindingsIn e status definido como os resultados da \_ associação especificada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4474">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="6dadd-4475">3.1.5.2.7 Recebendo uma solicitação CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4475">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="6dadd-4476">Quando o servidor recebe uma solicitação de mensagem CPMGetRowsIn de um cliente, o servidor DEVE fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4476">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4477">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4477">Check if the client has query associated with it.</span></span> <span data-ttu-id="6dadd-4478">Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4478">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4479">Verifique se o cursor passado está na lista de alças de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4479">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="6dadd-4480">Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4480">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4481">Verifique se o cliente tem um conjunto atual de vinculações.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4481">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="6dadd-4482">Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4482">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4483">Prepare uma mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4483">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="6dadd-4484">O servidor DEVE posicionar o cursor nos resultados da consulta, conforme indicado pela descrição da busca.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4484">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="6dadd-4485">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4485">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="6dadd-4486">Busque quantas linhas cabem em um buffer, o tamanho do qual é indicado por cbReadBuffer, mas não mais do que indicado \_ por \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4486">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="6dadd-4487">Ao buscar linhas, o servidor DEVE comparar o tipo de valor da propriedade de cada coluna selecionada com o tipo especificado no conjunto atual de vinculações do cliente (seção 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4487">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="6dadd-4488">Se o tipo na associação não for VT VARIANT, o servidor DEVERÁ tentar converter o valor da propriedade da coluna \_ nesse tipo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4488">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="6dadd-4489">Caso contrário, se o sinalizador DBPROP USEEXTENDEDDBTYPES for definido no conjunto de propriedades \_ DBPROPSET QUERYEXT do cliente ou se o valor da propriedade da coluna não for um tipo VT VECTOR, o valor da propriedade DEVERÁ ser retornado em seu \_ \_ tipo normal.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4489">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="6dadd-4490">Se nenhum deles for o caso (ou seja, o servidor tiver um tipo VECTOR VT e o cliente não dá suporte a VECTOR VT), o servidor DEVERÁ tentar convertê-lo em um tipo VT ARRAY da seguinte \_ \_ \_ forma: VT \_ I8, VT \_ UI8, VT FILETIME e elementos de matriz \_ \_ CLSID VT não poderão ser convertidos e falharão; Os elementos da matriz VT LPSTR e VT LPWSTR DEVEM ser convertidos em VT BSTR; os elementos de matriz de todos os outros \_ \_ tipos DEVEM permanecer \_ inalterados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4490">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="6dadd-4491">Por fim, se as colunas de linha contêm alças de capítulo ou alças de indicador, o servidor DEVE atualizar as listas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4491">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="6dadd-4492">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4492">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="6dadd-4493">Armazene o número real de linhas buscadas em \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4493">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="6dadd-4494">Copie a descrição de busca e o campo de capítulo de CPMGetRowsIn para uma mensagem CPMGetRowsOut a ser enviada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4494">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="6dadd-4495">Armazene linhas buscadas no campo Linhas (consulte a observação sobre o byte de status abaixo e a seção 2.2.3.16 na estrutura do campo Linhas).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4495">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="6dadd-4496">Responda ao cliente com a mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4496">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="6dadd-4497">Observação no campo de byte de status:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4497">Note on status byte field:</span></span>

<span data-ttu-id="6dadd-4498">Se StatusUsed estiver definido como 0x01 na CTableColumn da mensagem CPMSetBindingIn para a coluna, o servidor DEVERÁ definir o byte de status (localizado em StatusOffset do início da linha) para essa coluna como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4498">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="6dadd-4499">Valor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4499">Value</span></span> | <span data-ttu-id="6dadd-4500">Significado</span><span class="sxs-lookup"><span data-stu-id="6dadd-4500">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="6dadd-4501">0x00</span><span class="sxs-lookup"><span data-stu-id="6dadd-4501">0x00</span></span>  | <span data-ttu-id="6dadd-4502">StatusOK</span><span class="sxs-lookup"><span data-stu-id="6dadd-4502">StatusOK</span></span>       |
| <span data-ttu-id="6dadd-4503">0x01</span><span class="sxs-lookup"><span data-stu-id="6dadd-4503">0x01</span></span>  | <span data-ttu-id="6dadd-4504">StatusDeferido</span><span class="sxs-lookup"><span data-stu-id="6dadd-4504">StatusDeferred</span></span> |
| <span data-ttu-id="6dadd-4505">0x02</span><span class="sxs-lookup"><span data-stu-id="6dadd-4505">0x02</span></span>  | <span data-ttu-id="6dadd-4506">StatusNull</span><span class="sxs-lookup"><span data-stu-id="6dadd-4506">StatusNull</span></span>     |



 

<span data-ttu-id="6dadd-4507">Se o valor da propriedade estiver ausente para essa linha, o servidor DEVERÁ definir o byte de status como StatusNull.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4507">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="6dadd-4508">Se o valor for muito grande para ser transferido na mensagem CPMGetRowsOut, o servidor DEVERÁ definir o byte de status como StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4508">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="6dadd-4509">Caso contrário, o servidor DEVERÁ definir o byte de status como StatusOK.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4509">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="6dadd-4510">3.1.5.2.8 Recebendo uma solicitação CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4510">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="6dadd-4511">Quando o servidor recebe uma solicitação de mensagem CPMFetchValueIn de um cliente, o servidor DEVE fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4511">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4512">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4512">Check if the client has query associated with it.</span></span> <span data-ttu-id="6dadd-4513">Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4513">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4514">Prepare uma mensagem CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4514">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="6dadd-4515">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4515">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="6dadd-4516">Localize o documento indicado pelo campo wid e verifique se a ID da propriedade deste documento (posteriormente conhecida como 'valor da propriedade') indicada pela estrutura PropSpec está disponível para \_ esse cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4516">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="6dadd-4517">Se esse valor não estiver disponível, o servidor DEVERÁ definir fValueExists como 0x00000000 e, de outra \_ forma, \_ definir fValueExists como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4517">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="6dadd-4518">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="6dadd-4519">Se \_ fValueExists for igual a 0x00000001 o servidor DEVERÁ fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4519">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="6dadd-4520">Serialize o valor da propriedade para uma estrutura SERIALIZEDPROPERTYVALUE e copie, começando no deslocamento \_ cbSoFar, no máximo bytes cbChunk (mas não após o final da propriedade serializada) para o campo \_ vValue.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4520">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="6dadd-4521">Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4521">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="6dadd-4522">De \_ definir cbValue como o número de bytes copiados na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4522">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="6dadd-4523">De definir vType como o tipo de propriedade do valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4523">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="6dadd-4524">Se o comprimento da propriedade serializada for maior que cbSoFar adicionado a cbValue, de definir \_ \_ fMoreExists como 0x00000001, caso contrário, de definido como \_ 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4524">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="6dadd-4525">Responder ao cliente com a mensagem CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4525">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="6dadd-4526">3.1.5.2.9 Recebendo uma solicitação CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="6dadd-4526">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="6dadd-4527">Quando o servidor recebe uma mensagem CPMGetNotify de um cliente, o servidor DEVE fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4527">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4528">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4528">Check if the client has query associated with it.</span></span> <span data-ttu-id="6dadd-4529">Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4529">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4530">Se não houver nenhuma alteração no conjunto de resultados da consulta desde a última mensagem CPMSendNotifyOut para esse cliente ou se a consulta não estiver monitorada no momento para alterações no conjunto de resultados, o servidor DEVERÁ responder com a mensagem CPMGetNotify e começar a monitorar a consulta em busca de alterações no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4530">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="6dadd-4531">Se, em um momento posterior, houver uma alteração no conjunto de resultados da consulta, o servidor deverá enviar exatamente uma mensagem CPMSendNotifyOut para o cliente e deve especificar a alteração no \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4531">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="6dadd-4532">Se houver alterações no conjunto de resultados da consulta desde a última mensagem CPMSendNotifyOut, o servidor deverá responder com CPMSendNotifyOut e deverá especificar a alteração no \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4532">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="6dadd-4533">Observe que, no caso de muitas alterações nos resultados da consulta, DBWATCHNOTIFY \_ rowschanged tem prioridade (ou seja, se a consulta foi feita, executada novamente e, em seguida, o número de linhas alteradas e a consulta foi feita novamente, o evento relatado seria DBWATCHNOTIFY \_ rowschanged).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4533">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="6dadd-4534">3.1.5.2.10 recebendo uma solicitação CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4534">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="6dadd-4535">Quando o servidor recebe uma solicitação de mensagem CPMGetApproximatePositionIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4535">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4536">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4536">Check if the client has a query associated with it.</span></span> <span data-ttu-id="6dadd-4537">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4537">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4538">Verifique se a alça do cursor, o identificador do capítulo e o identificador do indicador aprovado estão nas listas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4538">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="6dadd-4539">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4539">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4540">Localize uma linha que esteja associada ao identificador de indicador nos resultados da consulta e aproximar a posição da linha no conjunto de linhas, referenciada pelo identificador de capítulo, e determine o numerador e o denominador para a posição.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4540">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="6dadd-4541">Observe que, quando o identificador do capítulo é DB \_ NULL \_ HCHAPTER, o capítulo correspondente é o principal conjunto de linhas da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4541">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="6dadd-4542">Se essa etapa falhar por algum motivo, o servidor deverá relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4542">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="6dadd-4543">Responda ao cliente com uma mensagem CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4543">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="6dadd-4544">3.1.5.2.11 recebendo uma solicitação CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4544">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="6dadd-4545">Quando o servidor recebe uma solicitação de mensagem CPMCompareBmkIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4545">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4546">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4546">Check if the client has a query associated with it.</span></span> <span data-ttu-id="6dadd-4547">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4547">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4548">Verifique se a alça do cursor, o identificador do capítulo e os identificadores de indicador passados estão nas listas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4548">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="6dadd-4549">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4549">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4550">Prepare uma mensagem CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4550">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="6dadd-4551">Se as alças de indicador forem iguais, \_ DWCOMPARISON deverá ser definido como DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4551">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="6dadd-4552">Caso contrário, se um dos indicadores identificadores for DBBMK \_ First ou DBBMK \_ Last, \_ dwComparison deverá ser definido como DBCOMPARE \_ ne.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4552">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="6dadd-4553">Caso contrário, o servidor deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4553">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="6dadd-4554">Localizar linhas que são referenciadas por cada identificador de indicador nos resultados da consulta</span><span class="sxs-lookup"><span data-stu-id="6dadd-4554">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="6dadd-4555">Se qualquer uma das linhas não estiver no capítulo indicado pelo identificador de capítulo em CPMCompareBmkIn, \_ DWCOMPARISON deverá ser definido como DBCOMPARE não \_ comparável.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4555">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="6dadd-4556">Caso contrário, quando ambas as linhas estiverem no mesmo capítulo, o servidor deverá aproximar uma posição dessas linhas no conjunto de linhas referido pela alça deste capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4556">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="6dadd-4557">Em seguida, ele deve comparar valores de posição e definir \_ dwComparison como DBCOMPARE \_ lt se a posição da primeira linha for menor que a posição da segunda linha; caso contrário, \_ dwComparison deverá ser definido como DBCOMPARE \_ gt.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4557">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="6dadd-4558">Responda ao cliente com a mensagem CPMCompareBmkOut preenchida.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4558">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="6dadd-4559">3.1.5.2.12 recebendo uma solicitação CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4559">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="6dadd-4560">Quando o servidor recebe a solicitação de mensagem CPMRestartPositionIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4560">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4561">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4561">Check if the client has a query associated with it.</span></span> <span data-ttu-id="6dadd-4562">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4562">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4563">Verifique se o identificador do cursor e o identificador do capítulo aprovado estão nas listas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4563">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="6dadd-4564">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4564">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4565">Mova o cursor para o início do capítulo, identificado pelo identificador de capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4565">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="6dadd-4566">Observe que, quando o identificador do capítulo é DB \_ NULL \_ HCHAPTER, o capítulo correspondente é o principal conjunto de linhas da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4566">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="6dadd-4567">Se essa etapa falhar por algum motivo, o servidor deverá relatar um erro.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4567">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="6dadd-4568">Responda ao cliente com uma mensagem CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4568">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="6dadd-4569">3.1.5.2.13 recebendo uma solicitação CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4569">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="6dadd-4570">Quando o servidor recebe uma solicitação de mensagem CPMFreeCursorIn do cliente, o servidor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4570">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4571">Verifique se o cliente tem uma consulta associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4571">Check if the client has a query associated with it.</span></span> <span data-ttu-id="6dadd-4572">Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4572">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="6dadd-4573">Verifique se o identificador de cursor passado está na lista de identificadores de cursor do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4573">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="6dadd-4574">Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4574">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="6dadd-4575">Libere o cursor e os recursos associados (consulte a seção 3.1.1 para obter a lista completa) para esse identificador de cursor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4575">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="6dadd-4576">Remova o cursor da lista de cursores para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4576">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="6dadd-4577">Responda com uma mensagem CPMFreeCursorOut, definindo o \_ campo cCursorsRemaining com o número de cursores restantes.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4577">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="6dadd-4578">na lista deste cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4578">in this client's list.</span></span>
-   <span data-ttu-id="6dadd-4579">Se não houver mais cursores para esse cliente, o servidor deverá liberar a consulta e os recursos associados (consulte a seção 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4579">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="6dadd-4580">3.1.5.2.14 recebendo uma solicitação CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="6dadd-4580">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="6dadd-4581">Quando o servidor recebe uma solicitação de mensagem CPMDisconnect do cliente, o servidor deve remover o cliente da lista de clientes conectados e liberar todos os recursos associados ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4581">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="6dadd-4582">Eventos de timer 3.1.6</span><span class="sxs-lookup"><span data-stu-id="6dadd-4582">3.1.6 Timer Events</span></span>

<span data-ttu-id="6dadd-4583">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4583">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="6dadd-4584">3.1.7 outros eventos locais</span><span class="sxs-lookup"><span data-stu-id="6dadd-4584">3.1.7 Other Local Events</span></span>

<span data-ttu-id="6dadd-4585">Quando o servidor é interrompido, ele deve primeiro fazer a transição para o estado "desligando".</span><span class="sxs-lookup"><span data-stu-id="6dadd-4585">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="6dadd-4586">Em seguida, ele deve parar de escutar o pipe, executar outras tarefas de desligamento específicas da implementação e, em seguida, fazer a transição para o estado "Stopped".</span><span class="sxs-lookup"><span data-stu-id="6dadd-4586">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="6dadd-4587">3,2 detalhes do cliente</span><span class="sxs-lookup"><span data-stu-id="6dadd-4587">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="6dadd-4588">3.2.1 modelo de dados abstratos</span><span class="sxs-lookup"><span data-stu-id="6dadd-4588">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="6dadd-4589">A seção a seguir especifica os dados e o estado mantidos pelo cliente do protocolo do serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4589">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="6dadd-4590">Os dados fornecidos são para facilitar a explicação de como o protocolo se comporta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4590">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="6dadd-4591">Esta seção não exige que as implementações sigam esse modelo, desde que seu comportamento externo seja consistente com o descrito neste documento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4591">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="6dadd-4592">Um cliente tem o seguinte estado abstrato:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4592">A client has the following abstract state:</span></span>

-   <span data-ttu-id="6dadd-4593">**Última mensagem enviada**: uma cópia da última mensagem enviada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4593">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="6dadd-4594">**Valor da propriedade atual**: um valor parcial de uma propriedade "adiada", que está no processo de ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4594">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="6dadd-4595">**Bytes atuais recebidos**: o número de bytes recebidos para o valor da propriedade atual até o momento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4595">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="6dadd-4596">**Estado de conexão do pipe nomeado**: uma conexão com o servidor</span><span class="sxs-lookup"><span data-stu-id="6dadd-4596">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="6dadd-4597">temporizadores de 3.2.2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4597">3.2.2 Timers</span></span>

<span data-ttu-id="6dadd-4598">Nenhum temporizador de protocolo é necessário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4598">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="6dadd-4599">inicialização do 3.2.3</span><span class="sxs-lookup"><span data-stu-id="6dadd-4599">3.2.3 Initialization</span></span>

<span data-ttu-id="6dadd-4600">Nenhuma ação é executada até que uma solicitação de camada superior seja recebida.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4600">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="6dadd-4601">Eventos disparados Higher-Layer 3.2.4</span><span class="sxs-lookup"><span data-stu-id="6dadd-4601">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="6dadd-4602">Quando uma solicitação é recebida de uma camada superior, o cliente deve criar uma conexão de pipe nomeado para o servidor, usando os detalhes especificados na seção 2,1.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4602">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="6dadd-4603">Se não for possível fazer isso, a solicitação de camada superior deverá ter falhado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4603">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="6dadd-4604">Ou seja, no caso de uma falha ao se conectar, é responsabilidade do nível mais alto tentar novamente, se desejado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4604">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="6dadd-4605">Um cabeçalho deve ser semipendente com campos definidos conforme especificado na seção 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4605">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="6dadd-4606">Para mensagens que são especificadas como exigindo uma soma de verificação diferente de zero, o \_ valor de ULCHECKSUM deve ser calculado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4606">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="6dadd-4607">O conteúdo da mensagem após o \_ campo ulReserved2 no cabeçalho da mensagem deve ser interpretado como uma sequência de inteiros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4607">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="6dadd-4608">O cliente deve calcular a soma dos valores numéricos fornecidos por esses inteiros.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4608">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="6dadd-4609">Calcule o XOR bit a bit desse valor com 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4609">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="6dadd-4610">Subtraia o valor fornecido pela \_ mensagem do valor que resulta do XOR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4610">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="6dadd-4611">Gerenciamento de catálogo do serviço de indexação remota do 3.2.4.1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4611">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="6dadd-4612">Cada mensagem é disparada por uma solicitação da camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4612">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="6dadd-4613">Não há nenhuma sequência de mensagens imposta pelo cliente para solicitações de mensagens CISP para gerenciar catálogos remotamente, mas (com exceção de uma mensagem CPMSetCatStateIn) o servidor responderá com êxito somente se o cliente tiver se conectado anteriormente por meio de uma mensagem CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4613">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="6dadd-4614">3.2.4.1.1 enviando uma solicitação CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4614">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="6dadd-4615">Normalmente, a camada superior solicita que o cliente de protocolo envie uma mensagem CPMCiStateInOut quando requer informações sobre a indexação de serviços no servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4615">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="6dadd-4616">Quando solicitado a enviar esta mensagem, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4616">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4617">Envie uma mensagem CPMCiStateInOut conforme especificado na seção 2.2.3.1 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4617">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="6dadd-4618">Aguarde para receber a mensagem CPMCiStateInOut do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4618">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="6dadd-4619">Relate o valor do \_ campo status da resposta e, se tiver êxito, a estrutura informativa de volta à camada mais alta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4619">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="6dadd-4620">3.2.4.1.2 enviando uma solicitação CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4620">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="6dadd-4621">Normalmente, a camada superior solicita que o cliente de protocolo envie uma mensagem CPMSetCatStateIn quando requer informações sobre um catálogo ou todos os catálogos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4621">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="6dadd-4622">Para essa mensagem, a camada superior precisa fornecer ao cliente de protocolo um valor para \_ dwNewState e, se necessário, o nome do catálogo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4622">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="6dadd-4623">Quando solicitado a enviar esta mensagem, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4623">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4624">Envie uma mensagem CPMSetCatStateIn conforme especificado em 2.2.3.2 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4624">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="6dadd-4625">Aguarde para receber uma mensagem CPMSetCatStateOut do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4625">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="6dadd-4626">Relate o valor do \_ campo status da resposta e, se tiver sido bem-sucedida, o \_ dwOldState de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4626">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="6dadd-4627">3.2.4.1.3 enviando uma solicitação CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4627">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="6dadd-4628">A camada mais alta normalmente solicita o envio dessa mensagem quando precisa atualizar documentos no caminho existente ou adicionar um novo caminho de arquivo ao índice.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4628">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="6dadd-4629">Portanto, a camada mais alta é fornecer o caminho e o tipo de uma verificação, que é especificado como na seção 2.2.3.4, em que uma atualização incremental ou completa é destinada a caminhos existentes, e a nova inicialização é destinada a novos caminhos.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4629">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="6dadd-4630">Para atender à solicitação de camada superior, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4630">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4631">Envie uma mensagem CPMUpdateDocumentsIn conforme especificado na seção 2.2.3.4 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4631">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="6dadd-4632">Aguarde para receber a mensagem CPMUpdateDocumentsIn de volta do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4632">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="6dadd-4633">Relate o valor do \_ campo status da resposta de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4633">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="6dadd-4634">3.2.4.1.4 enviando uma solicitação CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4634">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="6dadd-4635">Normalmente, as solicitações de camada mais alta para enviar essa mensagem quando há necessidade de melhorar o desempenho da consulta ou fazem parte da manutenção agendada do serviço de indexação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4635">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="6dadd-4636">Para atender à camada mais alta, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4636">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4637">Envie a mensagem CPMForceMergeIn conforme especificado pela seção 2.2.3.5 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4637">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="6dadd-4638">Aguarde para receber uma mensagem CPMUpdateDocumentsIn de volta do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4638">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="6dadd-4639">Relate o valor do \_ campo status da resposta de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4639">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="6dadd-4640">Mensagens de consulta do catálogo de serviço de indexação remota do 3.2.4.2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4640">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="6dadd-4641">Com exceção de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, há uma relação um-para-um entre as mensagens CISP e as solicitações de camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4641">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="6dadd-4642">Para as duas exceções mencionadas acima, pode haver várias mensagens geradas pelo cliente para atender aos requisitos de tamanho ou para recuperar uma propriedade completa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4642">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="6dadd-4643">Normalmente, a camada superior controla todas as informações específicas de consulta (como identificadores de cursor abertos, valores válidos para identificadores de indicador e capítulo, valores de wid para valores de propriedade adiados, etc.) e também controla se o cliente está em um estado conectado, mas isso não é imposto de nenhuma forma pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4643">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="6dadd-4644">Para fins ilustrativos, a parte de cliente do diagrama na seção 3 ilustra essa sequência para uma consulta de serviço de indexação simples.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4644">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="6dadd-4645">3.2.4.2.1 enviando uma solicitação CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4645">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="6dadd-4646">Essa mensagem é normalmente a primeira solicitação da camada superior (como se o cliente não estiver conectado, o servidor falhará na maioria das mensagens com exceção de CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4646">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="6dadd-4647">O nível mais alto fornece ao cliente de protocolo as informações necessárias para se conectar.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4647">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="6dadd-4648">Para atender à camada mais alta, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4648">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4649">Preencha a mensagem, usando informações que o cliente de camada superior forneceu (consulte a seção 2.2.3.6) em \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 e aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4649">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="6dadd-4650">Defina \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet e cExtPropSet conforme especificado em 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4650">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="6dadd-4651">Defina a soma de verificação no \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4651">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="6dadd-4652">Envie a mensagem CPMConnectIn para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4652">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="6dadd-4653">Aguarde para receber uma mensagem CPMConnectOut de volta do servidor, descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4653">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="6dadd-4654">Relate o valor do \_ campo status da resposta e, se tiver sido bem-sucedida, o \_ serverVersion de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4654">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="6dadd-4655">Para fins informativos, espera-se que as camadas mais altas normalmente realizem as seguintes ações após a conexão bem-sucedida, mas elas não são impostas pelo cliente CISP:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4655">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="6dadd-4656">Usar mensagens de gerenciamento de catálogo de serviço de indexação remota para tarefas administrativas</span><span class="sxs-lookup"><span data-stu-id="6dadd-4656">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="6dadd-4657">Use uma solicitação CPMCreateQueryIn para criar uma consulta de pesquisa com a finalidade de recuperar os resultados do catálogo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4657">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="6dadd-4658">3.2.4.2.2 enviando uma solicitação CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4658">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="6dadd-4659">A camada superior normalmente fornecerá informações para a criação da consulta quando o cliente do protocolo estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4659">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="6dadd-4660">A camada superior fornece ao cliente um conjunto de restrições, conjunto de colunas, regras de ordem de classificação e conjunto de categorização (cada um deles pode ser omitido), propriedades de conjunto de linhas e estrutura do mapeador de ID de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4660">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="6dadd-4661">Quando essa solicitação é recebida de uma camada superior, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4661">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4662">Prepare um CPMCreateQueryOut da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4662">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="6dadd-4663">Se um conjunto de colunas estiver presente, defina CColumnsSetPreset como 0x01 e preencha o campo Columnsset.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4663">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="6dadd-4664">Se houver restrições, defina CRestrictionPresent como 0x01 e preencha o campo de restrição.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4664">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="6dadd-4665">Se um conjunto de classificação estiver presente, preencha o campo de classificação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4665">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="6dadd-4666">Se um conjunto de categorização estiver presente, defina CSortSetPresent como 0x01 e preencha o campo CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4666">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="6dadd-4667">Definir o restante dos campos conforme especificado em 2.2.3.8</span><span class="sxs-lookup"><span data-stu-id="6dadd-4667">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="6dadd-4668">Calcule \_ o campo ulCheckSum no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4668">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="6dadd-4669">Envie a mensagem CPMCreateQueryIn para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4669">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="6dadd-4670">Aguarde para receber a mensagem CPMCreateQueryOut (consulte os detalhes na seção 3.2.5.1.1), descartando silenciosamente todas as outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4670">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="6dadd-4671">Relate o valor do \_ campo status da resposta e, se tiver êxito, a matriz de identificadores de cursor e valores Boolianos informativos (conforme especificado em 2.2.3.9) de volta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4671">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="6dadd-4672">3.2.4.2.3 enviando uma solicitação CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4672">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="6dadd-4673">Normalmente, a camada superior definirá associações para cada coluna a ser retornada nas linhas quando ela já tiver um identificador de cursor válido (depois de receber CPMCreateQueryOut com êxito, consulte a seção 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4673">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="6dadd-4674">O valor mais alto é esperado para fornecer uma matriz de estruturas CTableColumn, conforme especificado na seção 2.2.4.31, para o campo aColumns e um identificador de cursor válido.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4674">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="6dadd-4675">Quando essa solicitação é recebida da camada superior, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4675">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4676">Calcule o número de estruturas CTableColumn na matriz aColumns e defina o campo cColumns com esse valor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4676">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="6dadd-4677">Calcule o tamanho total em bytes dos campos cColumns e aColumns e defina o \_ campo cbBindingDesc com esse valor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4677">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="6dadd-4678">Defina os campos especificados na mensagem CPMSetBindingsIn para os valores fornecidos pela camada de aplicativo superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4678">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="6dadd-4679">Defina o \_ campo ulChecksum para o valor calculado conforme especificado na seção 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4679">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="6dadd-4680">Envie a mensagem CPMSetBindignsIn concluída para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4680">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="6dadd-4681">Aguarde para receber uma mensagem CPMSetBindingsIn do servidor, descartando outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4681">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="6dadd-4682">Indique o status do \_ campo status da resposta para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4682">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="6dadd-4683">Para fins informativos, espera-se que as camadas mais altas normalmente solicitem que um cliente envie uma mensagem CPMGetRowsIn, mas isso não é imposto pelo protocolo de serviço de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4683">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="6dadd-4684">3.2.4.2.4 enviando uma solicitação CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4684">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="6dadd-4685">Quando a camada mais alta estiver prestes a receber informações de linhas, ele fornecerá ao cliente de protocolo com o cursor e o identificador do capítulo válidos e fornecerá a descrição de busca apropriada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4685">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="6dadd-4686">Normalmente, espera-se que uma camada mais alta faça isso quando tem um cursor e/ou identificador de capítulo válido, e as associações foram definidas com a mensagem CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4686">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="6dadd-4687">Para acessar o conjunto de linhas em um capítulo, a camada mais alta é usar o identificador de capítulo recebido do servidor em uma mensagem CPMGetRowsOut anterior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4687">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="6dadd-4688">Quando essa solicitação é recebida da camada superior, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4688">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4689">Determine qual valor inteiro sem sinal deve ser especificado para o \_ campo cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4689">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="6dadd-4690">Para determinar esse valor, o cliente deve obter o valor máximo do seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4690">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="6dadd-4691">1000 vezes o valor do campo c \_ RowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4691">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="6dadd-4692">Valor de \_ cbRowWidth, arredondado para o múltiplo de 512 bytes mais próximo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4692">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="6dadd-4693">Pegue os dois valores acima, até o limite de 16K.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4693">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="6dadd-4694">Nos casos em que uma única linha é maior que 16K, o servidor não pode retornar resultados para essa consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4694">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="6dadd-4695">Especifique uma base de cliente para dados de linha de tamanho variável no espaço de endereço de cliente no \_ campo ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4695">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="6dadd-4696">*Comportamento do Windows: para um cliente de 32 bits conversando com um servidor de 32 bits ou um cliente de 64 bits conversando com um servidor de 64 bits, esse valor é definido como um endereço de memória do buffer de recebimento no processo do aplicativo. Isso permite que os ponteiros, recebidos no campo de linhas de CPMGetRowsOut, sejam ponteiros de memória corretos em um processo de aplicativo cliente. Caso contrário, ele será definido como 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="6dadd-4696">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="6dadd-4697">Calcule o tamanho da descrição de busca e defina-a no \_ campo cbSeek.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4697">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="6dadd-4698">Defina o valor de cbReserved (que atuaria como um deslocamento para o início das linhas) para o valor de \_ cbSeek Plus 0x14.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4698">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="6dadd-4699">Envie uma mensagem CPMConnectIn conforme especificado em 2.2.3.15 para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4699">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="6dadd-4700">3.2.4.2.5 enviando uma solicitação CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4700">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="6dadd-4701">Se o cliente receber uma resposta CPMGetRowsOut do servidor com o campo status da coluna definido como StatusDeferred (0x01), isso significa que o valor da propriedade não foi incluído no campo linhas da mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4701">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="6dadd-4702">Nesse caso, a camada mais alta normalmente solicita que o cliente de protocolo recupere o valor por meio da mensagem CPMFetchValueIn e fornece o valor de PropSpec e \_ wid para uma propriedade adiada, que o cliente de protocolo deve usar na primeira mensagem CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4702">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="6dadd-4703">Se esta for a primeira mensagem CPMFetchValueIn que o cliente enviou para solicitar a propriedade especificada, o cliente deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4703">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4704">Defina todos os campos em uma mensagem conforme especificado na seção 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4704">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="6dadd-4705">Defina \_ cbSoFar como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4705">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="6dadd-4706">Defina os bytes atuais recebidos como 0.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4706">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="6dadd-4707">Envie a mensagem CPMFetchValueIn para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4707">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="6dadd-4708">3.2.4.2.6 enviando uma solicitação CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="6dadd-4708">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="6dadd-4709">Quando o nível mais alto não estiver mais usando a consulta de pesquisa, ele poderá liberar os recursos no servidor solicitando que o cliente envie uma mensagem CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4709">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="6dadd-4710">Quando essa solicitação é recebida, o cliente deve enviar uma mensagem CPMFreeCursorIn conforme especificado em 2.2.3.28 para o servidor, contendo o identificador especificado pela camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4710">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="6dadd-4711">3.2.4.2.7 enviando uma mensagem CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="6dadd-4711">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="6dadd-4712">Se a camada superior não tiver mais consultas para o serviço de indexação, para liberar mais recursos do servidor, o aplicativo poderá solicitar que o cliente envie uma mensagem CPMDisconnect ao servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4712">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="6dadd-4713">Quando essa consulta é recebida, o cliente deve simplesmente enviar a mensagem conforme solicitado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4713">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="6dadd-4714">Não há resposta a essa mensagem do servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4714">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="6dadd-4715">Processamento de mensagens 3.2.5 e regras de sequenciamento</span><span class="sxs-lookup"><span data-stu-id="6dadd-4715">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="6dadd-4716">Quando o cliente recebe uma resposta de mensagem do servidor, o cliente deve usar a última mensagem enviada para determinar se a mensagem recebida do servidor é a esperada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4716">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="6dadd-4717">Todas as mensagens com \_ o campo msg diferente da que está na última mensagem de envio devem ser ignoradas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4717">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="6dadd-4718">3.2.5.1 recebendo uma resposta CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4718">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="6dadd-4719">Quando o cliente recebe uma resposta de mensagem CPMCreateQueryOut do servidor, o cliente deve retornar o \_ status e (se o status for com êxito) os valores de ponteiro de volta para uma camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4719">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="6dadd-4720">Todas as ações adicionais são até a camada mais alta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4720">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="6dadd-4721">Como a camada mais alta reconhece a estrutura de consulta, ela sempre esperará o número correto de identificadores de cursor a serem retornados na mensagem CPMCreateOueryOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4721">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="6dadd-4722">As alças de cursor são retornadas na seguinte ordem: o primeiro identificador é para o conjunto de linhas sem capítulos, o segundo é para o primeiro conjunto de linhas com capítulo (que é o agrupamento de resultados com base na primeira categoria especificada no campo CategorizationSet da mensagem CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4722">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="6dadd-4723">Para fins informativos, espera-se que camadas mais altas possam realizar as seguintes ações, mas elas não são impostas pelo cliente CISP:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4723">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="6dadd-4724">Use CPMSetBindingsIn para definir associações para colunas individuais e executar ações subsequentes no caminho de consulta</span><span class="sxs-lookup"><span data-stu-id="6dadd-4724">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="6dadd-4725">Use CPMGetQueryStatusIn para verificar o progresso da execução de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4725">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="6dadd-4726">Use CPMRatioFinishedIn para solicitar o percentual de conclusão da consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4726">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="6dadd-4727">3.2.5.2 recebendo uma resposta CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4727">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="6dadd-4728">Quando o cliente recebe uma resposta de mensagem CPMGetRowsOut do servidor, o cliente deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4728">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4729">Verifique se o \_ campo status no cabeçalho indica êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4729">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="6dadd-4730">Se o \_ valor de status for \_ buffer de status \_ muito \_ pequeno (0xC0000023), o cliente deverá verificar o estado da última mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4730">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="6dadd-4731">Se ele não contém uma mensagem CPMGetRowsIn, a mensagem recebida DEVE ser ignorada silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4731">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="6dadd-4732">Caso contrário, o cliente DEVERÁ enviar ao servidor uma nova mensagem CPMGetRowsIn com todos os campos idênticos ao armazenado, exceto que cbReadBuffer DEVE ser aumentado em 512 (mas não maior que \_ 0x4000).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4732">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="6dadd-4733">Se o status for BUFFER DE STATUS MUITO PEQUENO (0xC0000023) e a Última Mensagem Enviada já tiver \_ \_ \_ \_ \_ cbReadBuffer igual 0x4000 cliente DEVERÁ relatar o erro até o nível superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4733">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="6dadd-4734">Se o valor de status for qualquer outro valor de erro, o cliente DEVERÁ indicar a \_ falha até a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4734">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="6dadd-4735">Se o valor de status indicar êxito, os resultados DEVERÃO ser indicados até a camada superior solicitando as informações e outras ações serão até \_ a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4735">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="6dadd-4736">Para fins informativos, espera-se que camadas mais altas normalmente faça as seguintes ações, mas elas não são impostas pelo cliente do Protocolo de Serviço de Indexação de Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4736">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="6dadd-4737">Se os valores em linhas representarem as IDs do documento, o capítulo ou o indicador manipulará a camada superior normalmente os armazenará para uso em operações subsequentes que envolvem IDs de documento válidas, alças de capítulo ou indicador.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4737">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="6dadd-4738">A camada superior normalmente armazenará ou exibirá ou usará os dados de valores de linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4738">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="6dadd-4739">Para os valores que foram marcados como camada superior adiada, buscará o valor usando mensagens CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4739">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="6dadd-4740">A descrição da busca também é retornada para a camada superior e pode ser reutilizada ou examinada pela camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4740">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="6dadd-4741">Para fins informativos, se a camada superior solicitada lidar com capítulos e indicadores que foram recebidos nas linhas, ele poderá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4741">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="6dadd-4742">Use CPMGetQueryStatusExIn para verificar o progresso da execução de uma consulta, bem como informações de status adicionais, como o número de documentos filtrados, os documentos restantes a serem filtrados, a taxa de documentos processados pela consulta, o número total de linhas na consulta e a posição do indicador no conjuntos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4742">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="6dadd-4743">Use CPMGetNotify para solicitar que o servidor notifique o cliente sobre alterações no conjuntos de linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4743">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="6dadd-4744">Use CPMGetApproximatePositionIn para solicitar a posição aproximada de um indicador em um capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4744">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="6dadd-4745">Use CPMCompareBmkIn para solicitar uma comparação de dois indicadores em um capítulo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4745">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="6dadd-4746">Use CPMRestartPositionIn para o servidor para alterar o local do cursor para o início do rowset.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4746">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="6dadd-4747">3.2.5.3 Recebendo uma resposta CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4747">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="6dadd-4748">Quando o cliente recebe uma resposta de mensagem CPMGetRowsOut do servidor, o cliente DEVE fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4748">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="6dadd-4749">Verifique se o \_ campo de status no header indica êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4749">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="6dadd-4750">Em caso de falha, notifique a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4750">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="6dadd-4751">Caso contrário, continue abaixo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4751">Otherwise, continue below.</span></span>
-   <span data-ttu-id="6dadd-4752">Verifique \_ fValueExist e, se definido como 0x00000000 notifique a camada superior de que o valor não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4752">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="6dadd-4753">Caso contrário, \_ aenda os bytes cbValue de vValue ao Valor da Propriedade Atual.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4753">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="6dadd-4754">Se fMoreExists estiver definido como 0x00000001 incrementar Bytes Atuais Recebidos por cbValue e enviar uma mensagem \_ \_ \_ CPMFetchValueIn para o servidor, definindo cbSoFar como o valor de Bytes Atuais Recebidos, cbPropSpec como zero e \_ \_ \_ \_ cbChunk para o tamanho do buffer desejado pela camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4754">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="6dadd-4755">Se fMoreExists for definido como 0x00000000, indique o valor da propriedade \_ de Valor da Propriedade Atual para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4755">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="6dadd-4756">3.2.5.4 Recebendo uma resposta CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="6dadd-4756">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="6dadd-4757">Quando o cliente recebe uma resposta de mensagem CPMFreeCursorOut bem-sucedida do servidor, o cliente DEVE retornar o valor \_ cCursorsRemaining para a camada superior.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4757">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="6dadd-4758">As informações a seguir são fornecidas apenas para fins informativos e não são impostas pelo cliente CISP.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4758">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="6dadd-4759">Espera-se que a camada superior controle os alças de cursor e não use aqueles que já foram liberados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4759">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="6dadd-4760">Depois que o número de cCursorsRemaining for igual a 0x00000000, a camada superior poderá usar a conexão para especificar outra consulta (usando uma mensagem \_ CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4760">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="6dadd-4761">3.2.6 Eventos de temporizador</span><span class="sxs-lookup"><span data-stu-id="6dadd-4761">3.2.6 Timer Events</span></span>

<span data-ttu-id="6dadd-4762">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4762">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="6dadd-4763">3.2.7 Outros eventos locais</span><span class="sxs-lookup"><span data-stu-id="6dadd-4763">3.2.7 Other Local Events</span></span>

<span data-ttu-id="6dadd-4764">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4764">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="6dadd-4765">4 Exemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="6dadd-4765">4 Protocol Examples</span></span>

-   [<span data-ttu-id="6dadd-4766">4.1 Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4766">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="6dadd-4767">4.2 Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4767">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="6dadd-4768">4.1 Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6dadd-4768">4.1 Example 1</span></span>

<span data-ttu-id="6dadd-4769">No exemplo a seguir, consideramos um cenário no qual o usuário JOHN no computador A deseja obter os tamanhos de arquivos que contêm a palavra "Microsoft" do conjunto de documentos armazenados no servidor X no catálogo SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4769">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="6dadd-4770">Vamos supor que o computador A está executando um sistema operacional Windows XP de 32 bits e o computador X está executando um sistema operacional Windows Server 2003 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4770">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="6dadd-4771">O usuário inicia um aplicativo de pesquisa e entra na consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4771">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="6dadd-4772">O aplicativo, por sua vez, passa a consulta de pesquisa para o cliente de protocolo.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4772">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="6dadd-4773">O cliente de protocolo estabelece uma conexão com o servidor de indexação X. O cliente de protocolo usa o \\ SKADS de CI de pipe \\ nomeado para se conectar ao servidor X por \_ SMB.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4773">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="6dadd-4774">Em seguida, o cliente de protocolo prepara uma mensagem CPMConnectIn com os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4774">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="6dadd-4775">O header da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4775">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4776">**\_ msg** é definido como 0x000000C8, indicando que esta é uma mensagem CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4776">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="6dadd-4777">**\_ status** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4777">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="6dadd-4778">**\_ ulChecksum** contém a verificação, calculada conforme especificado na Seção 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4778">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="6dadd-4779">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4779">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="6dadd-4780">O corpo da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4780">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4781">**\_ iClientVersion é** definido como 0x00000008, indicando que o servidor deve validar o campo de verificação.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4781">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="6dadd-4782">**\_ fClientIsRemote** é definido como 0x00000001, indicando que o servidor é um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4782">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="6dadd-4783">**\_ cbBlob1** é definido como o tamanho, em bytes, dos campos cPropSet, PropertySet1 e PropertySet2 combinados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4783">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="6dadd-4784">**\_ cbBlob2 é** definido como 0x00000004 (o que significa que nenhum conjunto de propriedades extra).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4784">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="6dadd-4785">**MachineName** está definido como A.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4785">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="6dadd-4786">**UserName** é definido como JOHN.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4786">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="6dadd-4787">**cPropSets** é definido como 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4787">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="6dadd-4788">**O campo PropertySet1** é do tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4788">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="6dadd-4789">A estrutura CDbPropSet que inclui o campo PropertySet1 é populada da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4789">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="6dadd-4790">O **campo GuidPropSet** é definido como A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4790">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="6dadd-4791">**O campo cProperties** é definido como 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4791">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="6dadd-4792">**o campo aProps** é uma matriz de estruturas CDbProp.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4792">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="6dadd-4793">Para o **elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4793">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="6dadd-4794">**PropId** é definido como 0x00000002 (NOME DO CATÁLOGO \_ DE CI \_ \_ DBPROP).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4794">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="6dadd-4795">**DBPROPOPTIONS é** definido como 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4795">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="6dadd-4796">**DBPROPSTATUS é** definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4796">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-4797">Para o **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4797">For the **ColId** element:</span></span>
                -   <span data-ttu-id="6dadd-4798">**eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4798">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="6dadd-4799">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4799">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="6dadd-4800">**ulID** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4800">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-4801">Para o **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4801">For the **vValue** element:</span></span>
                -   <span data-ttu-id="6dadd-4802">**vType** é definido como 0x001F (VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4802">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="6dadd-4803">**vValue** é definido como "SYSTEM", o nome do catálogo desejado.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4803">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="6dadd-4804">Para o **elemento aProps \[ 1: \]**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4804">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="6dadd-4805">**PropId** é definido como 0x00000007 (TIPO DE CONSULTA \_ CI \_ \_ DBPROP)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4805">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="6dadd-4806">**DBPROPOPTIONS é** definido como 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4806">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="6dadd-4807">**DBPROPSTATUS é** definido como0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4807">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-4808">Para o **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4808">For the **ColId** element:</span></span>
                -   <span data-ttu-id="6dadd-4809">**eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4809">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="6dadd-4810">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4810">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="6dadd-4811">**ulID** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4811">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-4812">Para o **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4812">For the **vValue** element:</span></span>
                -   <span data-ttu-id="6dadd-4813">**vType** é definido como 0x0003 (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4813">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="6dadd-4814">**vValue** é definido como 0x00000000 (CiNormal), o que significa que é uma consulta regular.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4814">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="6dadd-4815">Para o **elemento aProps \[ 2: \]**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4815">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="6dadd-4816">**PropId** é definido como 0x00000004 (SINALIZADORES DE ESCOPO \_ DE CI \_ \_ DBPROP).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4816">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="6dadd-4817">**DBPROPOPTIONS é** definido como 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4817">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="6dadd-4818">**DBPROPSTATUS é** definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4818">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-4819">Para o **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4819">For the **ColId** element:</span></span>
                -   <span data-ttu-id="6dadd-4820">**eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4820">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="6dadd-4821">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4821">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="6dadd-4822">**ulID** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4822">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-4823">Para o **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4823">For the **vValue** element:</span></span>
                -   <span data-ttu-id="6dadd-4824">**vType:** 0x1003 (VT \_ VECTOR \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4824">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="6dadd-4825">**vValue:** 0x00000001/0x00000001 (um elemento com valor 1), o que significa sub pastas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="6dadd-4825">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="6dadd-4826">Para o **elemento aProps \[ 3: \]**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4826">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="6dadd-4827">**PropId:** 0x00000003 (ESCOPOS DE \_ INCLUSÃO DE CI DO \_ \_ DBPROP)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4827">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="6dadd-4828">**DBPROPOPTIONS:** 0x0000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-4828">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="6dadd-4829">**DBPROPSTATUS**: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-4829">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="6dadd-4830">Para o **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4830">For the **ColId** element:</span></span>
                -   <span data-ttu-id="6dadd-4831">**eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4831">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="6dadd-4832">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4832">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="6dadd-4833">**ulID** é definido como 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-4833">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="6dadd-4834">Para o **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4834">For the **vValue** element:</span></span>
                -   <span data-ttu-id="6dadd-4835">**vType** é definido como 0x101F (VT \_ VECTOR \| VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4835">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="6dadd-4836">**vValue** é definido como 0x00000001 /0x00000002 /" (um elemento com uma cadeia de caracteres terminada em nulo de 2 caracteres), o que significa o \\ escopo raiz.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4836">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="6dadd-4837">O **campo PropertySet2** é do tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4837">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="6dadd-4838">A estrutura CDbPropSet que inclui o campo PropertySet1 é populada da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4838">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="6dadd-4839">**GuidPropSet** é definido como AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4839">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="6dadd-4840">**O campo cProperties** é definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4840">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="6dadd-4841">O **campo aProps** é uma matriz de estruturas CDbProp.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4841">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="6dadd-4842">Para o **elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4842">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="6dadd-4843">**PropId** é definido como 0x00000002 (DBPROP \_ MACHINE).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4843">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="6dadd-4844">**DBPROPOPTIONS é** definido como 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4844">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="6dadd-4845">**DBPROPSTATUS é** definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4845">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-4846">Para o **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4846">For the **ColId** element:</span></span>
                -   <span data-ttu-id="6dadd-4847">**eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID),</span><span class="sxs-lookup"><span data-stu-id="6dadd-4847">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="6dadd-4848">**GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4848">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="6dadd-4849">**ulID** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4849">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-4850">Para **o elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4850">For **vValue** element:</span></span>
                -   <span data-ttu-id="6dadd-4851">**vType:** 0x0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="6dadd-4851">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="6dadd-4852">**vValue:** 0x04 /"X" (4 bytes/cadeia de caracteres Unicode terminada em nulo), que significa "X" -name de um servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4852">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="6dadd-4853">**O campo cExtPropSet** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4853">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="6dadd-4854">**A matriz aPropertySets** não existe.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4854">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="6dadd-4855">Vários campos de preenchimento são preenchidos conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4855">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="6dadd-4856">A mensagem é enviada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4856">The message is sent to the server.</span></span>

4.  <span data-ttu-id="6dadd-4857">O servidor verifica se o **\_ ulChecksum** está correto, verifica se o usuário está autorizado a fazer essa solicitação e responde com uma mensagem CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4857">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="6dadd-4858">O header da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4858">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4859">**\_ msg** é definido como 0x000000C8, indicando que esta é uma mensagem CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4859">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="6dadd-4860">**\_ status** é definido como 0x0000000 indicando SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4860">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="6dadd-4861">**\_ ulChecksum** é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4861">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="6dadd-4862">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4862">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="6dadd-4863">O corpo da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4863">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4864">**\_ O campo serverVersion** é definido como 0x00000007 (Windows XP de 32 bits ou Windows Server 2003 de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4864">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="6dadd-4865">**\_ Os campos** reservados são preenchidos com dados arbitrários.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4865">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="6dadd-4866">O cliente prepara uma mensagem CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4866">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="6dadd-4867">O header da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4867">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4868">**\_ msg** é definido como 0x000000CA, indicando que esta é uma mensagem CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4868">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="6dadd-4869">**\_ status** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4869">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="6dadd-4870">**\_ ulChecksum contém** a verificação, calculada de acordo com 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4870">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="6dadd-4871">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4871">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="6dadd-4872">O corpo da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4872">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4873">**O** campo tamanho é definido como o tamanho do restante da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4873">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="6dadd-4874">**O campo CColumnSetPresent** está definido como 0x01.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4874">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="6dadd-4875">**O campo ColumnSet** é do tipo CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4875">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="6dadd-4876">A estrutura CColumnSet que inclui esse campo é definida da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4876">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="6dadd-4877">**\_ o** campo count é definido como 0x00000001 indicando que uma coluna é retornada.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4877">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="6dadd-4878">**A matriz** de índices 0x00000000 indicando a primeira entrada em \_ aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4878">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="6dadd-4879">**O campo CRestrictionPresent** é definido como 0x01 indicando que o **campo Restrição** está presente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4879">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="6dadd-4880">**O** campo de restrição é do tipo CRestriction e está definido como:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4880">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="6dadd-4881">**\_ ulType** é definido como 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4881">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="6dadd-4882">**\_ weight** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4882">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="6dadd-4883">O restante do campo contém uma estrutura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4883">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="6dadd-4884">**\_** A propriedade é definida como GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (para PRSPEC PROPID) /0x13 que representa o corpo \_ do documento.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4884">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="6dadd-4885">**\_ Cc** é definido como 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4885">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="6dadd-4886">**\_ pwcsphrase é** definido como a cadeia de caracteres "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="6dadd-4886">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="6dadd-4887">**\_ lcid é** definido como 0x409 (para inglês).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4887">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="6dadd-4888">**\_ ulGenerateMethod** é definido como 0x00000000 (combinação exata).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4888">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="6dadd-4889">**CSortPresent** é definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4889">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="6dadd-4890">**CCategorizationSetPresent** é definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4890">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="6dadd-4891">**RowSetProperties** é definido da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4891">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="6dadd-4892">**\_ uBooleanOptions** é definido como 0x00000001 (sequencial).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4892">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="6dadd-4893">**\_ ulMaxOpenRows** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4893">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="6dadd-4894">**\_ ulMemoryUsage** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4894">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="6dadd-4895">\_**cMaxResults** é definido como 0x00000100 (retornam no máximo 256 linhas).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4895">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="6dadd-4896">**\_ cCmdTimeOut** é definido como 0x00000000 (nunca o tempoout).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4896">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="6dadd-4897">**O PidMapper** está definido como:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4897">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="6dadd-4898">**\_ count** é definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4898">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="6dadd-4899">**\_ aPropSpec** é definido como GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0x00000001 (para PRSPEC PROPID) /0x0000000c que representa a propriedade \_ de tamanho de arquivo do Windows.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4899">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="6dadd-4900">O servidor o processa e responde com uma mensagem CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4900">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="6dadd-4901">O header da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4901">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4902">**\_ msg** é definido como 0x000000CA, indicando que esta é uma mensagem CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4902">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="6dadd-4903">**\_ status** é definido como SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4903">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="6dadd-4904">**\_ ulChecksum** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4904">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="6dadd-4905">**\_ ulReserved2** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4905">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="6dadd-4906">O corpo da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4906">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4907">**\_ fTrueSeqeuntial** é definido como 0x00000000, indicando que a consulta pode usar um índice.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4907">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="6dadd-4908">**\_ fWorkIdUnique** está definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4908">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="6dadd-4909">A **matriz aCursors** contém apenas um elemento, representando um alça de cursor para essa consulta.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4909">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="6dadd-4910">O valor depende do estado do servidor.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4910">The value depends on the state of the server.</span></span> <span data-ttu-id="6dadd-4911">Vamos supor que o valor retornado seja 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4911">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="6dadd-4912">O cliente emite uma mensagem de solicitação CPMSetBindingsIn para definir o formato de uma linha.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4912">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="6dadd-4913">O header da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4913">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4914">**\_ msg** é definido como 0x000000D0, indicando que esta é uma mensagem CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4914">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="6dadd-4915">**\_ status** é definido como SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4915">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="6dadd-4916">**\_ ulChecksum** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4916">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="6dadd-4917">**\_ ulReserved2** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4917">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="6dadd-4918">O corpo da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4918">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4919">**\_ hCursor** é definido como 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4919">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="6dadd-4920">**\_ cbRow** é definido como 0x10 (grande o suficiente para ajustar colunas).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4920">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="6dadd-4921">**\_ cbBindingDesc** é definido como o tamanho dos campos **\_ cColumns** e **\_ aColumns combinados.**</span><span class="sxs-lookup"><span data-stu-id="6dadd-4921">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="6dadd-4922">**\_ cColumns é** definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4922">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="6dadd-4923">**\_ a Matriz aColumns** é definida para conter uma estrutura CTableColumn que contém:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4923">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="6dadd-4924">**\_ PropSpec** é definido como GUID b725f130-47ef-101a-a5-f1-02608c9eebac/0x00000001 (para PRSPEC PROPID) /0x0000000c que representa a propriedade de tamanho de \_ arquivo do Windows.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4924">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="6dadd-4925">**\_ vType** é definido como 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4925">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="6dadd-4926">**\_ ValueUsed é** definido como 0x01 (coluna transferida em linha).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4926">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="6dadd-4927">**\_ ValueOffset** é definido como 0x0002 (no início da linha).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4927">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="6dadd-4928">**\_ ValueSize** é definido como 0x08 (tamanho de uma \_ VT UI8).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4928">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="6dadd-4929">**\_ StatusUsed** é definido como 0x01.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4929">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="6dadd-4930">**\_ StatusOffset** é definido como 0x0A.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4930">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="6dadd-4931">**\_ LengthUsed** é definido como 0x00.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4931">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="6dadd-4932">O servidor o processa e responde com uma mensagem CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4932">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="6dadd-4933">O header da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4933">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4934">**\_ msg** é definido como 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4934">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="6dadd-4935">**\_ status** é definido como SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4935">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="6dadd-4936">**\_ ulChecksum** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4936">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="6dadd-4937">**\_ ulReserved2** é definido como 0x00000000 (ou qualquer outro valor arbitrário).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4937">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="6dadd-4938">O cliente emite uma mensagem de solicitação CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4938">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="6dadd-4939">Vamos supor que o cliente está preparado para aceitar 100 linhas neste ponto e deseja-as em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4939">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="6dadd-4940">O header da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4940">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4941">**\_ msg** é definido como 0x000000CC, indicando que esta é uma mensagem CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4941">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="6dadd-4942">**\_ status** é definido como 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dadd-4942">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="6dadd-4943">**\_ ulChecksum contém** a verificação, calculada de acordo com a Seção 0.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4943">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="6dadd-4944">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4944">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="6dadd-4945">O corpo da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4945">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4946">**\_ hCursor** é definido como 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4946">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="6dadd-4947">**\_ cRowsToTransfer** é definido como 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4947">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="6dadd-4948">**\_ cRowWidth** é definido como 0x00000010 (de vinculações).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4948">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="6dadd-4949">**\_ cbSeek** é definido como 0x14 que é o tamanho dos campos eType, chapt e \_ CRowSeekNext combinados.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4949">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="6dadd-4950">**\_ cbReserved** é definido como 0x18 (0x14 mais \_ cbSeek).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4950">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="6dadd-4951">**\_ cbReadBuffer** é definido como 0x800 (0x64 0x10 arredondado para o próximo \* múltiplo de 0x200).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4951">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="6dadd-4952">**\_ ulClientBase** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4952">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="6dadd-4953">**\_ fBwdfetch** é definido como 0x00000000 indicando que as linhas devem ser buscadas em ordem de avanço.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4953">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="6dadd-4954">**EType** é definido como 0x0000001 indicando que o cliente deseja as próximas linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4954">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="6dadd-4955">**\_ chapt** é definido como 0 (não um resultado capítulo).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4955">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="6dadd-4956">**SeekDescription é** definido como CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4956">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="6dadd-4957">A estrutura CRowSeekNext contém os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4957">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="6dadd-4958">**CiTblChapt** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4958">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="6dadd-4959">**\_ hRegion** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4959">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="6dadd-4960">**\_ cSkip** é definido como 0, indicando que o cliente não deseja ignorar linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4960">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="6dadd-4961">O servidor o processa e responde com uma mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4961">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="6dadd-4962">Vamos supor que o servidor encontrou 100 documentos que contêm a palavra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="6dadd-4962">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="6dadd-4963">O header da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4963">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4964">**\_ msg** é definido como 0x000000CC, indicando que esta é uma mensagem CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4964">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="6dadd-4965">**\_ status** é definido como SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4965">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="6dadd-4966">**\_ ulChecksum** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4966">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="6dadd-4967">**\_ ulReserved2** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4967">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="6dadd-4968">O corpo da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4968">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4969">**\_ CRowsReturned** é definido como 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4969">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="6dadd-4970">**eType** é definido como 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4970">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="6dadd-4971">**\_ chapt** é definido como 0x00000000 (não um resultado capítulo).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4971">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="6dadd-4972">**SeekDescription** contém uma estrutura CRowSeekNext, populada da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4972">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="6dadd-4973">**CiTblChapt** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4973">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="6dadd-4974">**\_ hRegion** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4974">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="6dadd-4975">**\_ cSkip** é definido como 0, indicando que o cliente não deseja ignorar linhas.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4975">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="6dadd-4976">**As linhas** contêm o tamanho dos 100 documentos que contêm a palavra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="6dadd-4976">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="6dadd-4977">Como esses dados são de tamanho fixo, eles são simplesmente estruturados como uma lista de inteiros sem sinal de 100, 8 byte.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4977">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="6dadd-4978">O cliente envia uma mensagem CPMDisconnect para encerrar a conexão.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4978">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="6dadd-4979">O header da mensagem é populado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4979">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="6dadd-4980">**\_ msg** é definido como 0x000000C9, indicando que esta é uma mensagem CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4980">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="6dadd-4981">**\_ status** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4981">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="6dadd-4982">**\_ ulChecksum** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4982">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="6dadd-4983">O servidor processa a mensagem e remove todo o estado do cliente.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4983">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="6dadd-4984">4.2 Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6dadd-4984">4.2 Example 2</span></span>

<span data-ttu-id="6dadd-4985">No exemplo anterior, a consulta era bastante simples.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4985">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="6dadd-4986">Agora vamos considerar uma consulta um pouco mais complexa.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4986">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="6dadd-4987">Vamos supor que o usuário deseja recuperar o tamanho dos documentos que contêm as seguintes palavras: "Microsoft" e "Office".</span><span class="sxs-lookup"><span data-stu-id="6dadd-4987">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="6dadd-4988">Isso é especificado alterando o campo Restrição contido na mensagem CPMCreateQueryIn enviada na etapa 5 da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4988">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="6dadd-4989">O **campo Restrição** é do tipo CRestriction e está definido como:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4989">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="6dadd-4990">**\_ ulType** é definido como 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4990">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="6dadd-4991">**\_ weight** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4991">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="6dadd-4992">O restante do campo contém uma estrutura CNodeRestriction:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4992">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="6dadd-4993">**\_ cNode** é definido como 0x00000002, indicando que há dois nós na matriz paNode.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4993">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="6dadd-4994">O **\_ campo paNode** é uma matriz de duas estruturas CRestriction.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4994">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="6dadd-4995">**\_ paNode \[ 0 \]** contém:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4995">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="6dadd-4996">**\_ ulType** é definido como 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="6dadd-4996">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="6dadd-4997">**\_ weight** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4997">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-4998">O restante do campo contém uma estrutura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="6dadd-4998">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="6dadd-4999">**\_** A propriedade é definida como GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (para PRSPEC \_ PROPID) /0x13.</span><span class="sxs-lookup"><span data-stu-id="6dadd-4999">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="6dadd-5000">**\_ Cc** é definido como 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="6dadd-5000">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="6dadd-5001">**\_ pwcsphrase é** definido como a cadeia de caracteres "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="6dadd-5001">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="6dadd-5002">**\_ lcid é** definido como 0x409 (para inglês).</span><span class="sxs-lookup"><span data-stu-id="6dadd-5002">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="6dadd-5003">**\_ ulGenerateMethod** é definido como 0x00000000 (combinação exata).</span><span class="sxs-lookup"><span data-stu-id="6dadd-5003">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="6dadd-5004">**\_ paNode \[ 1 \]** contém:</span><span class="sxs-lookup"><span data-stu-id="6dadd-5004">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="6dadd-5005">**\_ ulType** é definido como 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="6dadd-5005">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="6dadd-5006">**\_ weight** é definido como 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="6dadd-5006">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="6dadd-5007">O restante do campo contém uma estrutura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="6dadd-5007">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="6dadd-5008">**\_** A propriedade é definida como GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (para PRSPEC \_ PROPID) /0x13.</span><span class="sxs-lookup"><span data-stu-id="6dadd-5008">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="6dadd-5009">**\_ Cc** é definido como 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="6dadd-5009">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="6dadd-5010">**\_ pwcsphrase é** definido como a cadeia de caracteres "Office".</span><span class="sxs-lookup"><span data-stu-id="6dadd-5010">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="6dadd-5011">**\_ lcid é** definido como 0x409 (para inglês).</span><span class="sxs-lookup"><span data-stu-id="6dadd-5011">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="6dadd-5012">**\_ ulGenerateMethod** é definido como 0x00000000 (combinação exata).</span><span class="sxs-lookup"><span data-stu-id="6dadd-5012">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="6dadd-5013">5 Segurança</span><span class="sxs-lookup"><span data-stu-id="6dadd-5013">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="6dadd-5014">5.1 Considerações de segurança para implementadores</span><span class="sxs-lookup"><span data-stu-id="6dadd-5014">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="6dadd-5015">As implementações de indexação que indexam o conteúdo seguro devem considerar o uso do contexto de usuário fornecido pelo SMB MS-SMB para cortar os resultados da pesquisa e retornar somente aqueles acessíveis ao \[ \] chamador.</span><span class="sxs-lookup"><span data-stu-id="6dadd-5015">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="6dadd-5016">5.2 Índice de parâmetros de segurança</span><span class="sxs-lookup"><span data-stu-id="6dadd-5016">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="6dadd-5017">Parâmetro de segurança</span><span class="sxs-lookup"><span data-stu-id="6dadd-5017">Security Parameter</span></span>  | <span data-ttu-id="6dadd-5018">Seção</span><span class="sxs-lookup"><span data-stu-id="6dadd-5018">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="6dadd-5019">Nível de representação</span><span class="sxs-lookup"><span data-stu-id="6dadd-5019">Impersonation level</span></span> | <span data-ttu-id="6dadd-5020">2.1</span><span class="sxs-lookup"><span data-stu-id="6dadd-5020">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="6dadd-5021">6 Índice de comportamento específico da versão</span><span class="sxs-lookup"><span data-stu-id="6dadd-5021">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="6dadd-5022">Comportamento específico da versão</span><span class="sxs-lookup"><span data-stu-id="6dadd-5022">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="6dadd-5023">Seção</span><span class="sxs-lookup"><span data-stu-id="6dadd-5023">Section</span></span>   | <span data-ttu-id="6dadd-5024">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6dadd-5024">Windows 2000</span></span> | <span data-ttu-id="6dadd-5025">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6dadd-5025">Windows XP</span></span> | <span data-ttu-id="6dadd-5026">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6dadd-5026">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="6dadd-5027">Esse protocolo é implementado no Windows 2000, Windows XP, Windows Server 2003 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6dadd-5027">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="6dadd-5028">1.3.2</span><span class="sxs-lookup"><span data-stu-id="6dadd-5028">1.3.2</span></span>     | <span data-ttu-id="6dadd-5029">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5029">X</span></span>            | <span data-ttu-id="6dadd-5030">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5030">X</span></span>          | <span data-ttu-id="6dadd-5031">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5031">X</span></span>                   |
| <span data-ttu-id="6dadd-5032">Normalmente, os aplicativos interagem com um wrapper de interface OLE DB</span><span class="sxs-lookup"><span data-stu-id="6dadd-5032">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="6dadd-5033">1.4</span><span class="sxs-lookup"><span data-stu-id="6dadd-5033">1.4</span></span>       | <span data-ttu-id="6dadd-5034">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5034">X</span></span>            | <span data-ttu-id="6dadd-5035">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5035">X</span></span>          | <span data-ttu-id="6dadd-5036">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5036">X</span></span>                   |
| <span data-ttu-id="6dadd-5037">Valores de NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="6dadd-5037">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="6dadd-5038">1.8</span><span class="sxs-lookup"><span data-stu-id="6dadd-5038">1.8</span></span>       | <span data-ttu-id="6dadd-5039">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5039">X</span></span>            | <span data-ttu-id="6dadd-5040">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5040">X</span></span>          | <span data-ttu-id="6dadd-5041">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5041">X</span></span>                   |
| <span data-ttu-id="6dadd-5042">O cliente define o \_ campo status em cada cabeçalho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dadd-5042">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="6dadd-5043">2.2.2</span><span class="sxs-lookup"><span data-stu-id="6dadd-5043">2.2.2</span></span>     | <span data-ttu-id="6dadd-5044">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5044">X</span></span>            | <span data-ttu-id="6dadd-5045">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5045">X</span></span>          | <span data-ttu-id="6dadd-5046">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5046">X</span></span>                   |
| <span data-ttu-id="6dadd-5047">o valor de cPendingScans geralmente é zero</span><span class="sxs-lookup"><span data-stu-id="6dadd-5047">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="6dadd-5048">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="6dadd-5048">2.2.3.1</span></span>   | <span data-ttu-id="6dadd-5049">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5049">X</span></span>            | <span data-ttu-id="6dadd-5050">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5050">X</span></span>          | <span data-ttu-id="6dadd-5051">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5051">X</span></span>                   |
| <span data-ttu-id="6dadd-5052">valor de iClientVersion</span><span class="sxs-lookup"><span data-stu-id="6dadd-5052">iClientVersion value</span></span>                                                                              | <span data-ttu-id="6dadd-5053">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="6dadd-5053">2.2.3.6</span></span>   | <span data-ttu-id="6dadd-5054">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5054">X</span></span>            | <span data-ttu-id="6dadd-5055">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5055">X</span></span>          | <span data-ttu-id="6dadd-5056">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5056">X</span></span>                   |
| <span data-ttu-id="6dadd-5057">\_valor de cbChunk</span><span class="sxs-lookup"><span data-stu-id="6dadd-5057">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="6dadd-5058">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="6dadd-5058">2.2.3.19</span></span>  | <span data-ttu-id="6dadd-5059">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5059">X</span></span>            | <span data-ttu-id="6dadd-5060">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5060">X</span></span>          | <span data-ttu-id="6dadd-5061">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5061">X</span></span>                   |
| <span data-ttu-id="6dadd-5062">endereços de memória de 32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="6dadd-5062">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="6dadd-5063">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="6dadd-5063">3.2.4.2.4</span></span> | <span data-ttu-id="6dadd-5064">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5064">X</span></span>            | <span data-ttu-id="6dadd-5065">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5065">X</span></span>          | <span data-ttu-id="6dadd-5066">X</span><span class="sxs-lookup"><span data-stu-id="6dadd-5066">X</span></span>                   |



 

 

 





