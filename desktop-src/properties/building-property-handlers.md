---
description: No Windows Vista e posterior, os metadados se tornaram centrais como um método de organizar itens, como arquivos, email ou contatos.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementando manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170505"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="73433-103">Implementando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="73433-103">Implementing Property Handlers</span></span>

<span data-ttu-id="73433-104">No Windows Vista e posterior, os metadados se tornaram centrais como um método de organizar itens, como arquivos, email ou contatos.</span><span class="sxs-lookup"><span data-stu-id="73433-104">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="73433-105">Para habilitar um sistema em que os itens podem ser pesquisados com base em seus metadados e onde os usuários podem ler ou gravar esses metadados, o Windows Vista introduziu um novo sistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="73433-105">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="73433-106">Os metadados nesse sistema são representados por um conjunto extensível de propriedades.</span><span class="sxs-lookup"><span data-stu-id="73433-106">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="73433-107">Neste conjunto de tópicos, descrevemos como você pode criar um manipulador que lê e grava Propriedades de e para um fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="73433-107">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="73433-108">Esses manipuladores são chamados de manipuladores de propriedade e cada um é associado a um determinado tipo de arquivo, identificado pela extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="73433-108">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="73433-109">Os tópicos a seguir abordam os requisitos e as estratégias envolvidas na definição de suas propriedades e manipuladores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="73433-109">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="73433-110">Noções básicas sobre manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="73433-110">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="73433-111">Usando nomes de tipos</span><span class="sxs-lookup"><span data-stu-id="73433-111">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="73433-112">Usando listas de propriedades</span><span class="sxs-lookup"><span data-stu-id="73433-112">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="73433-113">Inicializando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="73433-113">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="73433-114">Registrando e distribuindo manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="73433-114">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="73433-115">Práticas recomendadas e perguntas frequentes do manipulador de propriedades</span><span class="sxs-lookup"><span data-stu-id="73433-115">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="73433-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73433-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73433-117">Criando propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="73433-117">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="73433-118">Esquema de descrição da propriedade</span><span class="sxs-lookup"><span data-stu-id="73433-118">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
