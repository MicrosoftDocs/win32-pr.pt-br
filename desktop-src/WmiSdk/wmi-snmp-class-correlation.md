---
description: A correlação afeta o conjunto de classes retornadas do SMIR.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Correlação de classes SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165319"
---
# <a name="wmi-snmp-class-correlation"></a><span data-ttu-id="9a3a7-103">Correlação de classes SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="9a3a7-103">WMI SNMP Class Correlation</span></span>

<span data-ttu-id="9a3a7-104">A correlação afeta o conjunto de classes retornadas do SMIR.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-104">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="9a3a7-105">As classes correlacionadas são aquelas em que um determinado dispositivo SNMP é conhecido por dar suporte no momento em que a enumeração ocorre.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-105">Correlated classes are those that a given SNMP device is known to support at the time enumeration occurs.</span></span> <span data-ttu-id="9a3a7-106">A enumeração não correlacionada retorna todas as classes presentes no SMIR, independentemente de o dispositivo dar suporte a elas.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-106">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="9a3a7-107">A correlação é um recurso do provedor SNMP WMI e pode ser desativada ou ativada (padrão).</span><span class="sxs-lookup"><span data-stu-id="9a3a7-107">Correlation is a feature of the WMI SNMP provider and can be turned off or on (default).</span></span>

> [!Note]  
> <span data-ttu-id="9a3a7-108">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9a3a7-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="9a3a7-109">A correlação pode impedi-lo de ver todas as classes que são realmente suportadas por um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-109">Correlation might prevent you from seeing all of the classes that are actually supported by a device.</span></span> <span data-ttu-id="9a3a7-110">Se você souber que uma classe específica tem suporte, mas ela não aparece no SMIR, isso pode ser devido a vários motivos, um dos quais é a correlação.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-110">If you know that a particular class is supported but it does not appear in the SMIR, this could be due to several reasons, one of which is correlation.</span></span> <span data-ttu-id="9a3a7-111">Considere a possibilidade de desativar a correlação antes de gravar no dispositivo em questão.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-111">Consider turning correlation off before writing to the device in question.</span></span> <span data-ttu-id="9a3a7-112">No entanto, a desativação da correlação resulta na probabilidade de que muitas classes sem suporte do dispositivo apareçam no SMIR.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-112">However, turning correlation off results in the likelihood that many classes not supported by the device will appear in the SMIR.</span></span> <span data-ttu-id="9a3a7-113">Além disso, há um custo de desempenho no uso da correlação porque o dispositivo é consultado para ver quais classes ele suporta.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-113">Also, there is a performance cost in using correlation because the device is queried to see what classes it supports.</span></span> <span data-ttu-id="9a3a7-114">Quando a correlação é ativada, o provedor SNMP causa uma enumeração de classes com suporte a dispositivos semelhantes ao resultado da execução de uma ferramenta de *passagem MIB* .</span><span class="sxs-lookup"><span data-stu-id="9a3a7-114">When correlation is turned on, the SNMP provider causes an enumeration of device-supported classes similar to the result of running a *mib walk* tool.</span></span>

<span data-ttu-id="9a3a7-115">Por exemplo, um Gerenciador de rede quer saber várias partes importantes de dados sobre todos os hubs gerenciados em uma rede específica.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-115">For example, a network manager wants to know several key pieces of data about all the managed hubs in a particular network.</span></span> <span data-ttu-id="9a3a7-116">Já existe um banco de dados dos dispositivos atuais e seus MIBs com suporte. portanto, não há necessidade de contar com a função de correlação do dispositivo para fornecer os elementos de dados com suporte.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-116">A database of the current devices and their supported MIBs already exists, so there is no need to rely on the correlation function of the device to provide the supported data elements.</span></span> <span data-ttu-id="9a3a7-117">Nesse caso, a correlação pode ser desativada.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-117">In this case, correlation could be turned off.</span></span>

<span data-ttu-id="9a3a7-118">O exemplo a seguir mostra como desativar a correlação.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-118">The following example shows how to turn off correlation.</span></span>


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



<span data-ttu-id="9a3a7-119">Por outro lado, outro gerenciador de rede pode querer monitorar todas as unidades de disco de máquina UNIX na rede, mas não está familiarizado com os dados da MIB nesses computadores.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-119">On the other hand, another network manager may want to monitor all the UNIX machine disk drives on the network but is unfamiliar with the MIB data on those machines.</span></span> <span data-ttu-id="9a3a7-120">Nesse caso, a correlação seria ativada.</span><span class="sxs-lookup"><span data-stu-id="9a3a7-120">In that case, correlation would be turned on.</span></span>

 

 



