---
title: Trabalhando com listas de associação de variáveis
description: Uma associação de variável é o emparelhamento de um nome de instância de objeto SNMP com um valor associado. Uma lista de associação de variáveis é uma série de entradas de associação de variáveis. No WinSNMP, uma PDU (unidade de dados de protocolo) inclui uma lista de associações de variáveis.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Trabalhando com listas de associação de variáveis SNMP
- Associação de variáveis lista SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103640187"
---
# <a name="working-with-variable-binding-lists"></a><span data-ttu-id="f6fb9-107">Trabalhando com listas de associação de variáveis</span><span class="sxs-lookup"><span data-stu-id="f6fb9-107">Working with Variable Binding Lists</span></span>

<span data-ttu-id="f6fb9-108">Uma *Associação de variável* é o emparelhamento de um nome de instância de objeto SNMP com um valor associado.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-108">A *variable binding* is the pairing of an SNMP object instance name with an associated value.</span></span> <span data-ttu-id="f6fb9-109">Uma *lista de associação de variáveis* é uma série de entradas de associação de variáveis.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-109">A *variable binding list* is a series of variable binding entries.</span></span> <span data-ttu-id="f6fb9-110">No WinSNMP, uma PDU (unidade de dados de protocolo) inclui uma lista de associações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-110">In WinSNMP, a protocol data unit (PDU) includes a variable binding list.</span></span>

<span data-ttu-id="f6fb9-111">Os detalhes da estrutura da lista de associação de variáveis são restritos à implementação do Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-111">The details of the variable binding list structure are restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="f6fb9-112">Um aplicativo WinSNMP pode acessar uma lista de associação de variáveis com um identificador do tipo **HSNMP \_ VBL**.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-112">A WinSNMP application can access a variable binding list with a handle of type **HSNMP\_VBL**.</span></span> <span data-ttu-id="f6fb9-113">Para obter mais informações, consulte [objetos de identificador de recursos](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f6fb9-113">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="f6fb9-114">O aplicativo WinSNMP pode construir e manipular listas de associação de variáveis e incluí-las em PDUs.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-114">The WinSNMP application can construct and manipulate variable binding lists, and include them in PDUs.</span></span> <span data-ttu-id="f6fb9-115">Para executar essas operações, o aplicativo usa as [funções de associação de variável](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-115">To perform these operations, the application uses the WinSNMP [variable binding functions](winsnmp-functions.md).</span></span> <span data-ttu-id="f6fb9-116">Para obter mais informações sobre como trabalhar com as listas de associação de variáveis e WinSNMP, consulte os tópicos listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-116">For more information about working with WinSNMP and variable binding lists, see the topics listed in the following table.</span></span>



| <span data-ttu-id="f6fb9-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="f6fb9-117">Topic</span></span>                                                                    | <span data-ttu-id="f6fb9-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6fb9-118">Description</span></span>                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="f6fb9-119">Criando uma lista de associações de variáveis</span><span class="sxs-lookup"><span data-stu-id="f6fb9-119">Creating a Variable Binding List</span></span>](creating-a-variable-binding-list.md) | <span data-ttu-id="f6fb9-120">Descreve como criar uma lista de associações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-120">Describes how to create a variable binding list.</span></span> |
| [<span data-ttu-id="f6fb9-121">Gerenciando uma lista de associação de variáveis</span><span class="sxs-lookup"><span data-stu-id="f6fb9-121">Managing a Variable Binding List</span></span>](managing-a-variable-binding-list.md) | <span data-ttu-id="f6fb9-122">Descreve como gerenciar uma lista de associações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-122">Describes how to manage a variable binding list.</span></span> |



 

<span data-ttu-id="f6fb9-123">Para obter mais informações sobre associações de variáveis e listas de associação de variáveis, consulte [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "operações de protocolo para a versão 2 do protocolo de gerenciamento de rede simples (SNMPv2)" e as [funções de associação de variável](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="f6fb9-123">For more information about variable bindings and variable binding lists, see [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Protocol Operations for Version 2 of the Simple Network Management Protocol (SNMPv2)," and the WinSNMP [Variable Binding Functions](winsnmp-functions.md).</span></span>

 

 




