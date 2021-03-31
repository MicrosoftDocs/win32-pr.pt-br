---
title: Configuração dos limites de TTL
description: Um cliente pode solicitar um valor TTL para uma entrada que varia entre 1 e 31557600 (ou seja, de 1 segundo a 1 ano).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configuração de limites de TTL do AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634800"
---
# <a name="configuration-of-ttl-limits"></a><span data-ttu-id="0d653-104">Configuração dos limites de TTL</span><span class="sxs-lookup"><span data-stu-id="0d653-104">Configuration of TTL Limits</span></span>

<span data-ttu-id="0d653-105">Um cliente pode solicitar um valor TTL para uma entrada que varia entre 1 e 31557600 (ou seja, de 1 segundo a 1 ano).</span><span class="sxs-lookup"><span data-stu-id="0d653-105">A client can request a TTL value for an entry ranging between 1 and 31557600 (that is, from 1 second to 1 year).</span></span> <span data-ttu-id="0d653-106">Esse intervalo de valores de atributo será imposto pelos valores de atributo **RangeLower** e **rangeUpper** na definição **attributeSchema** para o atributo **entryTTL** .</span><span class="sxs-lookup"><span data-stu-id="0d653-106">This attribute value range will be enforced by the **rangeLower** and **rangeUpper** attribute values in the **attributeSchema** definition for the **entryTTL** attribute.</span></span> <span data-ttu-id="0d653-107">De acordo com a RFC 2589, os servidores de diretório não precisam aceitar esse valor e podem retornar um valor de TTL diferente para o cliente.</span><span class="sxs-lookup"><span data-stu-id="0d653-107">As per RFC 2589, directory servers are not required to accept this value and might return a different TTL value to the client.</span></span> <span data-ttu-id="0d653-108">Os clientes devem ser capazes de usar esse valor determinado pelo servidor como seu período de atualização do cliente (CRP), que controlará com que frequência o cliente precisará executar a operação de atualização na entrada dinâmica.</span><span class="sxs-lookup"><span data-stu-id="0d653-108">Clients must be able to use this server-dictated value as their client refresh period (CRP) which will govern how often the client will need to perform the refresh operation on the dynamic entry.</span></span>

<span data-ttu-id="0d653-109">Active Directory Domain Services fornecer aos administradores a capacidade de configurar os valores de TTL mínimos e padrão para uma floresta.</span><span class="sxs-lookup"><span data-stu-id="0d653-109">Active Directory Domain Services provide administrators with the ability to configure the default and minimum TTL values for a forest.</span></span> <span data-ttu-id="0d653-110">O valor de TTL padrão é o que será atribuído a uma entrada dinâmica recém-criada se uma TTL não for especificada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="0d653-110">The default TTL value is what will be assigned to a newly created dynamic entry if a TTL is not explicitly specified.</span></span> <span data-ttu-id="0d653-111">O TTL mínimo substituirá qualquer valor de TTL especificado pelo cliente que seja menor do que o mínimo configurado.</span><span class="sxs-lookup"><span data-stu-id="0d653-111">The minimum TTL will override any client specified TTL value that is lower than the configured minimum.</span></span> <span data-ttu-id="0d653-112">Nenhum valor de TTL máximo configurável precisa ser fornecido porque um máximo será imposto pelo valor do atributo **rangeUpper** no objeto **attributeSchema** .</span><span class="sxs-lookup"><span data-stu-id="0d653-112">No configurable maximum TTL value needs to be provided because a maximum will be imposed by the **rangeUpper** attribute value in the **attributeSchema** object.</span></span> <span data-ttu-id="0d653-113">Permitir que os administradores configurem esses valores permitirá que eles definam valores TTL que impedirão um tráfego de atualização baixa ou, no outro extremo, fornecem um diretório altamente atualizado.</span><span class="sxs-lookup"><span data-stu-id="0d653-113">Allowing administrators to configure these values will enable them to set TTL values which will enforce a low refresh traffic or, at the other extreme, provide a highly up-to-date directory.</span></span>

<span data-ttu-id="0d653-114">Os valores padrão para os dois parâmetros de TTL configuráveis serão os seguintes:</span><span class="sxs-lookup"><span data-stu-id="0d653-114">The default values for the two configurable TTL parameters will be as follows:</span></span>

-   <span data-ttu-id="0d653-115">Valor TTL padrão = 86400 segundos (1 dia)</span><span class="sxs-lookup"><span data-stu-id="0d653-115">Default TTL value = 86400 seconds (1 day)</span></span>
-   <span data-ttu-id="0d653-116">Valor TTL mínimo = 900 segundos (15 minutos)</span><span class="sxs-lookup"><span data-stu-id="0d653-116">Minimum TTL value = 900 seconds (15 minutes)</span></span>

<span data-ttu-id="0d653-117">Os parâmetros de TTL configuráveis serão armazenados como entradas de AVA (declaração de valor de atributo) no formato "<valor-nome>=</span><span class="sxs-lookup"><span data-stu-id="0d653-117">The configurable TTL parameters will be stored as AVA (attribute value assertion) entries of the form "<value-name>=</span></span><value><span data-ttu-id="0d653-118">"no atributo **MS-DS-Other-Settings** do objeto NTDS-Service fornecido pelo seguinte DN na partição de configuração:</span><span class="sxs-lookup"><span data-stu-id="0d653-118">" in the attribute **ms-DS-Other-Settings** of the NTDS-Service object given by the following DN in the Configuration partition:</span></span>


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



<span data-ttu-id="0d653-119">A sintaxe AVA exata, para os dois parâmetros TTL configuráveis, é a seguinte, em que NNNN é expresso em segundos:</span><span class="sxs-lookup"><span data-stu-id="0d653-119">The exact AVA syntax, for the two configurable TTL parameters, is as follows where NNNN is expressed in seconds:</span></span>


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



<span data-ttu-id="0d653-120">Esses valores podem ser definidos por um administrador por meio do utilitário de linha de comando Ntdsutil.</span><span class="sxs-lookup"><span data-stu-id="0d653-120">These values can be set by an administrator through the command-line utility ntdsutil.</span></span>

 

 




