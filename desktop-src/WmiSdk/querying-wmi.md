---
description: Uma das principais ferramentas do Instrumentação de Gerenciamento do Windows (WMI) é a capacidade de consultar o repositório WMI quanto a informações de classe e instância.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Consultando o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813545"
---
# <a name="querying-wmi"></a><span data-ttu-id="a6cae-103">Consultando o WMI</span><span class="sxs-lookup"><span data-stu-id="a6cae-103">Querying WMI</span></span>

<span data-ttu-id="a6cae-104">Uma das principais ferramentas do Instrumentação de Gerenciamento do Windows (WMI) é a capacidade de consultar o repositório WMI quanto a informações de classe e instância.</span><span class="sxs-lookup"><span data-stu-id="a6cae-104">One of the main tools of Windows Management Instrumentation (WMI) is the ability to query the WMI repository for class and instance information.</span></span> <span data-ttu-id="a6cae-105">Por exemplo, você pode solicitar que o WMI retorne todos os objetos que representam eventos de desligamento do seu sistema de desktop.</span><span class="sxs-lookup"><span data-stu-id="a6cae-105">For example, you can request that WMI return all the objects representing shut-down events from your desktop system.</span></span> <span data-ttu-id="a6cae-106">Você também pode recuperar dados de classe, instância ou esquema.</span><span class="sxs-lookup"><span data-stu-id="a6cae-106">You can also retrieve class, instance, or schema data.</span></span> <span data-ttu-id="a6cae-107">A tabela a seguir lista os diferentes tipos de consultas que você pode fazer.</span><span class="sxs-lookup"><span data-stu-id="a6cae-107">The following table lists the different types of queries you can make.</span></span>



| <span data-ttu-id="a6cae-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="a6cae-108">Topic</span></span>                                                                | <span data-ttu-id="a6cae-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6cae-109">Description</span></span>                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6cae-110">Invocando uma consulta síncrona</span><span class="sxs-lookup"><span data-stu-id="a6cae-110">Invoking a Synchronous Query</span></span>](invoking-a-synchronous-query.md)     | <span data-ttu-id="a6cae-111">Descreve como manter um link com o WMI em todo o processo de consulta.</span><span class="sxs-lookup"><span data-stu-id="a6cae-111">Describes how to maintain a link with WMI throughout the query process.</span></span> <span data-ttu-id="a6cae-112">As consultas síncronas são válidas para consultas pequenas ou consultas a um sistema local.</span><span class="sxs-lookup"><span data-stu-id="a6cae-112">Synchronous queries are good for small queries or queries to a local system.</span></span><br/>                                  |
| [<span data-ttu-id="a6cae-113">Invocando uma consulta assíncrona</span><span class="sxs-lookup"><span data-stu-id="a6cae-113">Invoking an Asynchronous Query</span></span>](invoking-an-asynchronous-query.md) | <span data-ttu-id="a6cae-114">Descreve como configurar um processo separado para receber consultas.</span><span class="sxs-lookup"><span data-stu-id="a6cae-114">Describes how to set up a separate process to receive queries.</span></span> <span data-ttu-id="a6cae-115">As consultas assíncronas são mais complexas e fornecem um nível mais baixo de segurança, mas geralmente melhoram o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="a6cae-115">Asynchronous queries are more complex and provide a lower level of security, but generally improve system performance.</span></span><br/> |



 

<span data-ttu-id="a6cae-116">Além de consultar o repositório WMI, você também pode usar o [*linguagem WQL (WQL)*](gloss-w.md) para rotear eventos de notificação para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6cae-116">In addition to querying the WMI repository, you can also use the [*WMI Query Language (WQL)*](gloss-w.md) to route notification events to your application.</span></span> <span data-ttu-id="a6cae-117">Para obter mais informações, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="a6cae-117">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

> [!Note]
>
> <span data-ttu-id="a6cae-118">Para consultar o WMI corretamente, você deve ter uma boa compreensão do WQL.</span><span class="sxs-lookup"><span data-stu-id="a6cae-118">To properly query WMI, you must have a good understanding of WQL.</span></span> <span data-ttu-id="a6cae-119">Uma consulta incorreta, muito complexa ou inadequada pode fazer com que o processador de consultas retorne um erro ou resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="a6cae-119">A query that is incorrect, too complex, or inappropriate can cause the query processor to return an error or unexpected results.</span></span> <span data-ttu-id="a6cae-120">Para obter um guia abrangente da WQL, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="a6cae-120">For a comprehensive guide to WQL, see [Querying with WQL](querying-with-wql.md).</span></span>
>
> <span data-ttu-id="a6cae-121">Há limites para o número de palavras-chave **and** e **or** que podem ser usadas em consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="a6cae-121">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="a6cae-122">Grandes números de palavras-chave WQL usadas em uma consulta complexa podem fazer com que o WMI retorne o código de erro de **\_ \_ \_ violação E de cota de WBEM** como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6cae-122">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="a6cae-123">O limite de palavras-chave WQL depende da complexidade da consulta.</span><span class="sxs-lookup"><span data-stu-id="a6cae-123">The limit of WQL keywords depends on how complex the query is.</span></span>
>
> <span data-ttu-id="a6cae-124">Ao consultar valores de propriedade com um tipo de dados **UInt64** ou **sint64** em uma linguagem de script como o VBScript, o WMI retorna valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a6cae-124">When querying for property values with a **uint64** or **sint64** data type in a scripting language like VBScript, WMI returns string values.</span></span> <span data-ttu-id="a6cae-125">Resultados inesperados podem ocorrer ao comparar esses valores, pois a comparação de cadeias de caracteres retorna resultados diferentes de comparação de números.</span><span class="sxs-lookup"><span data-stu-id="a6cae-125">Unexpected results can occur when comparing these values, because comparing strings returns different results than comparing numbers.</span></span> <span data-ttu-id="a6cae-126">Por exemplo, "10000000000" é menor que "9" ao comparar cadeias de caracteres e 9 é menor que 10000000000 ao comparar números.</span><span class="sxs-lookup"><span data-stu-id="a6cae-126">For example, "10000000000" is less than "9" when comparing strings, and 9 is less than 10000000000 when comparing numbers.</span></span> <span data-ttu-id="a6cae-127">Para evitar confusão, você deve usar o método [CDbl](/previous-versions//ftekwwt0(v=vs.85)) no VBScript quando as propriedades do tipo **UInt64** ou **SINT64** são recuperadas do WMI.</span><span class="sxs-lookup"><span data-stu-id="a6cae-127">To avoid confusion you should use the [CDbl](/previous-versions//ftekwwt0(v=vs.85)) method in VBScript when properties of type **uint64** or **sint64** are retrieved from WMI.</span></span>

 

> [!Note]  

 

<span data-ttu-id="a6cae-128">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="a6cae-128">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

