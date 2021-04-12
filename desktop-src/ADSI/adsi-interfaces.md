---
title: Interfaces ADSI
description: Este tópico descreve as categorias usadas para interfaces ADSI.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI de interfaces ADSI
- ADSI da ADSI, referência, interfaces
- ADSI de interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2930292defa99301fb74f37c933a9af24b73f1fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363663"
---
# <a name="adsi-interfaces"></a><span data-ttu-id="4f799-106">Interfaces ADSI</span><span class="sxs-lookup"><span data-stu-id="4f799-106">ADSI Interfaces</span></span>

<span data-ttu-id="4f799-107">A ADSI (Active Directory Service Interfaces) dá suporte a um conjunto avançado de interfaces que podem ser classificadas de acordo com as seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="4f799-107">Active Directory Service Interfaces (ADSI) supports a rich set of interfaces that can be classified according to the following categories:</span></span>

-   <span data-ttu-id="4f799-108">[Núcleo](core-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-108">[Core](core-interfaces.md).</span></span> <span data-ttu-id="4f799-109">Essas interfaces fornecem as funções básicas de gerenciamento de objeto dos objetos ADSI.</span><span class="sxs-lookup"><span data-stu-id="4f799-109">These interfaces provide the basic object management functions of ADSI objects.</span></span> <span data-ttu-id="4f799-110">As funções principais incluem o fornecimento de um ponto de entrada em um repositório de diretório, o carregamento de propriedades no cache de propriedades e a confirmação de alterações no diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="4f799-110">The core functions include providing an entry point into a directory store, loading properties into the property cache, and committing changes to the underlying directory.</span></span>
-   <span data-ttu-id="4f799-111">[Esquema](schema-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-111">[Schema](schema-interfaces.md).</span></span> <span data-ttu-id="4f799-112">Essas interfaces fornecem métodos para gerenciar e estender o esquema de diretório.</span><span class="sxs-lookup"><span data-stu-id="4f799-112">These interfaces provide methods for managing and extending the directory schema.</span></span>
-   <span data-ttu-id="4f799-113">[Cache de propriedades](property-cache-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-113">[Property Cache](property-cache-interfaces.md).</span></span> <span data-ttu-id="4f799-114">Essas interfaces definem métodos para manipular propriedades no cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4f799-114">These interfaces define methods for manipulating properties in the property cache.</span></span>
-   <span data-ttu-id="4f799-115">[Objeto persistente](persistent-object-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-115">[Persistent Object](persistent-object-interfaces.md).</span></span> <span data-ttu-id="4f799-116">Essas interfaces manipulam dados persistentes no namespace do serviço de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="4f799-116">These interfaces manipulate persistent data in the namespace of the underlying directory service.</span></span> <span data-ttu-id="4f799-117">Os objetos ADSI implementam esses tipos de interfaces para fornecer acesso aos seus dados persistentes, incluindo contas de usuário, compartilhamentos de arquivos, hierarquias organizacionais e listagens de trabalhos em uma fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="4f799-117">ADSI objects implement these types of interfaces to provide access to their persistent data, including user accounts, file shares, organizational hierarchies, and job listings in a print queue.</span></span>
-   <span data-ttu-id="4f799-118">[Objeto dinâmico](dynamic-object-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-118">[Dynamic Object](dynamic-object-interfaces.md).</span></span> <span data-ttu-id="4f799-119">Essas interfaces funcionam com dados dinâmicos em um serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="4f799-119">These interfaces work with dynamic data in a directory service.</span></span> <span data-ttu-id="4f799-120">Os objetos de diretório não representados no serviço de diretório subjacente implementam essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="4f799-120">Directory objects not represented in the underlying directory service implement such interfaces.</span></span> <span data-ttu-id="4f799-121">Exemplos de dados dinâmicos incluem comandos emitidos por uma rede.</span><span class="sxs-lookup"><span data-stu-id="4f799-121">Examples of dynamic data include commands issued over a network.</span></span>
-   <span data-ttu-id="4f799-122">[Segurança](security-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-122">[Security](security-interfaces.md).</span></span> <span data-ttu-id="4f799-123">Essas interfaces permitem que um cliente ADSI estabeleça suas credenciais para um servidor e use recursos de segurança aos quais o serviço de diretório dá suporte, como a lista de controle de acesso ou descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="4f799-123">These interfaces enable an ADSI client to establish its credentials to a server and use security features that the directory service supports, such as the access control list or security descriptors.</span></span>
-   <span data-ttu-id="4f799-124">[Não automação](non-automation-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-124">[Non-Automation](non-automation-interfaces.md).</span></span> <span data-ttu-id="4f799-125">Essas interfaces permitem que clientes que não são de automação (por exemplo, aplicativos C/C++) tenham acesso de baixa sobrecarga a objetos de diretório, fornecendo acesso de vtable a métodos para gerenciar e Pesquisar objetos de serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="4f799-125">These interfaces allow non-Automation clients (for example, C/C++ applications) low-overhead access to directory objects by providing Vtable access to methods for managing and searching directory service objects.</span></span>
-   <span data-ttu-id="4f799-126">[Extensão](extension-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-126">[Extension](extension-interfaces.md).</span></span> <span data-ttu-id="4f799-127">Essas interfaces permitem que os clientes ADSI estendam os recursos das classes ADSI existentes para oferecer soluções personalizadas aos serviços de diretório.</span><span class="sxs-lookup"><span data-stu-id="4f799-127">These interfaces allow ADSI clients to extend the features of existing ADSI classes to offer customized solutions to directory services.</span></span>
-   <span data-ttu-id="4f799-128">[Utilitário](utility-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-128">[Utility](utility-interfaces.md).</span></span> <span data-ttu-id="4f799-129">Essas interfaces fornecem funções auxiliares avançadas para o gerenciamento de objetos ADSI.</span><span class="sxs-lookup"><span data-stu-id="4f799-129">These interfaces provide advanced helper functions for managing ADSI objects.</span></span>
-   <span data-ttu-id="4f799-130">[Tipo de dados](data-type-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4f799-130">[Data Type](data-type-interfaces.md).</span></span> <span data-ttu-id="4f799-131">Essas interfaces fornecem métodos para acessar tipos de dados ADSI.</span><span class="sxs-lookup"><span data-stu-id="4f799-131">These interfaces provide methods to access ADSI data types.</span></span>

 

 




