---
description: Saiba como criar um manipulador de propriedades que lê e grava propriedades de e para um fluxo de arquivos. Cada manipulador está associado a um determinado tipo de arquivo.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementando manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf37ae37e43ce14cf69bec44e7f210b32373d38e
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989261"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="da2d3-104">Implementando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="da2d3-104">Implementing Property Handlers</span></span>

<span data-ttu-id="da2d3-105">No Windows Vista e posterior, os metadados se tornaram centrais como um método de organização de itens, como arquivos, email ou contatos.</span><span class="sxs-lookup"><span data-stu-id="da2d3-105">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="da2d3-106">Para habilitar um sistema em que os itens podem ser pesquisados com base em seus metadados e em que os usuários podem ler ou gravar esses metadados, o Windows Vista introduziu um novo sistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="da2d3-106">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="da2d3-107">Os metadados nesse sistema são representados por um conjunto extensível de propriedades.</span><span class="sxs-lookup"><span data-stu-id="da2d3-107">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="da2d3-108">Neste conjunto de tópicos, descrevemos como você pode criar um manipulador que lê e grava propriedades de e para um fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="da2d3-108">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="da2d3-109">Esses manipuladores são chamados de manipuladores de propriedade e cada um deles é associado a determinados tipos de arquivo, identificados pela extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="da2d3-109">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="da2d3-110">Os tópicos a seguir discutem os requisitos e estratégias envolvidos na definição de suas propriedades e manipuladores de propriedades.</span><span class="sxs-lookup"><span data-stu-id="da2d3-110">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="da2d3-111">Noções básicas sobre manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="da2d3-111">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="da2d3-112">Usando nomes de tipo</span><span class="sxs-lookup"><span data-stu-id="da2d3-112">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="da2d3-113">Usando listas de propriedades</span><span class="sxs-lookup"><span data-stu-id="da2d3-113">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="da2d3-114">Inicializando manipuladores de propriedades</span><span class="sxs-lookup"><span data-stu-id="da2d3-114">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="da2d3-115">Registrando e distribuindo manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="da2d3-115">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="da2d3-116">Práticas recomendadas e perguntas frequentes do manipulador de propriedades</span><span class="sxs-lookup"><span data-stu-id="da2d3-116">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="da2d3-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da2d3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da2d3-118">Criando propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="da2d3-118">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="da2d3-119">Esquema de descrição da propriedade</span><span class="sxs-lookup"><span data-stu-id="da2d3-119">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
