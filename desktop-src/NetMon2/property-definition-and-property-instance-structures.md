---
description: Monitor de Rede fornece uma estrutura PROPERTYINFO para definir as propriedades de um protocolo, e uma estrutura PROPERTYINST e PROPERTYINSTEX para definir uma instância de uma propriedade.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Definição de propriedade e estruturas de instância de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662059"
---
# <a name="property-definition-and-property-instance-structures"></a><span data-ttu-id="49fae-103">Definição de propriedade e estruturas de instância de propriedade</span><span class="sxs-lookup"><span data-stu-id="49fae-103">Property Definition and Property Instance Structures</span></span>

<span data-ttu-id="49fae-104">Monitor de Rede fornece uma estrutura [**PROPERTYINFO**](propertyinfo.md) para definir as propriedades de um protocolo, e uma estrutura [**PROPERTYINST**](propertyinst.md)e [**PROPERTYINSTEX**](propertyinstex.md) para definir uma instância de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="49fae-104">Network Monitor provides a [**PROPERTYINFO**](propertyinfo.md) structure to define the properties of a protocol, and a [**PROPERTYINST**](propertyinst.md), and [**PROPERTYINSTEX**](propertyinstex.md) structure to define an instance of a property.</span></span>

![estruturas do monitor de rede](images/property1.png)

<span data-ttu-id="49fae-106">O analisador aloca e preenche a estrutura [**PROPERTYINFO**](propertyinfo.md) para todas as propriedades às quais um protocolo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="49fae-106">The parser allocates and fills-in the [**PROPERTYINFO**](propertyinfo.md) structure for all the properties that a protocol supports.</span></span> <span data-ttu-id="49fae-107">O analisador passa a estrutura para Monitor de Rede onde a estrutura é adicionada ao banco de [*dados de propriedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="49fae-107">The parser passes the structure to Network Monitor where the structure is added to the protocol [*property database*](p.md).</span></span> <span data-ttu-id="49fae-108">As informações na estrutura **PROPERTYINFO** são usadas ao analisar uma instância de uma propriedade e ao formatar os dados exibidos na interface do usuário do monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="49fae-108">The information in the **PROPERTYINFO** structure is used when parsing an instance of a property, and when formatting the data that is displayed in the Network Monitor UI.</span></span>

<span data-ttu-id="49fae-109">Monitor de Rede aloca as estruturas [**PROPERTYINST**](propertyinst.md) e [**PROPERTYINSTEX**](propertyinstex.md) quando o analisador anexa uma definição de propriedade a uma instância de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="49fae-109">Network Monitor allocates the [**PROPERTYINST**](propertyinst.md) and [**PROPERTYINSTEX**](propertyinstex.md) structures when the parser attaches a property definition to an instance of a property.</span></span>

<span data-ttu-id="49fae-110">O procedimento a seguir identifica as etapas necessárias para anexar uma definição de propriedade.</span><span class="sxs-lookup"><span data-stu-id="49fae-110">The following procedure identifies the steps necessary to attach a property definition.</span></span>

<span data-ttu-id="49fae-111">**Para anexar uma definição de propriedade**</span><span class="sxs-lookup"><span data-stu-id="49fae-111">**To attach a property definition**</span></span>

1.  <span data-ttu-id="49fae-112">Identifique cada propriedade que existe em uma instância do protocolo.</span><span class="sxs-lookup"><span data-stu-id="49fae-112">Identify each property that exists in an instance of the protocol.</span></span> <span data-ttu-id="49fae-113">Ao anexar uma definição, Monitor de Rede passa os dados capturados para o analisador.</span><span class="sxs-lookup"><span data-stu-id="49fae-113">When attaching a definition, Network Monitor passes the captured data to the parser.</span></span> <span data-ttu-id="49fae-114">Os dados são passados em uma base de instância de protocolo.</span><span class="sxs-lookup"><span data-stu-id="49fae-114">The data is passed on a protocol instance basis.</span></span>
2.  <span data-ttu-id="49fae-115">Determine o local da propriedade na instância de protocolo.</span><span class="sxs-lookup"><span data-stu-id="49fae-115">Determine the location of the property in the protocol instance.</span></span>
3.  <span data-ttu-id="49fae-116">Anexe uma definição de propriedade ao local da propriedade.</span><span class="sxs-lookup"><span data-stu-id="49fae-116">Attach a property definition to the property location.</span></span>

<span data-ttu-id="49fae-117">Monitor de Rede implementa uma estrutura [**PROPERTYINST**](propertyinst.md) quando o analisador usa os dados de propriedade como eles existem na captura.</span><span class="sxs-lookup"><span data-stu-id="49fae-117">Network Monitor implements a [**PROPERTYINST**](propertyinst.md) structure when the parser uses the property data as it exists in the capture.</span></span> <span data-ttu-id="49fae-118">Monitor de Rede implementa uma estrutura [**PROPERTYINSTEX**](propertyinstex.md) quando o analisador deve modificar os dados de propriedade na captura.</span><span class="sxs-lookup"><span data-stu-id="49fae-118">Network Monitor implements a [**PROPERTYINSTEX**](propertyinstex.md) structure when the parser must modify the property data in the capture.</span></span>

 

 



