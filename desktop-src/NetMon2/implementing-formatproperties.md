---
description: Monitor de Rede chama a função Formatproperties para formatar os dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementando Formatproperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090253"
---
# <a name="implementing-formatproperties"></a><span data-ttu-id="bdf03-103">Implementando Formatproperties</span><span class="sxs-lookup"><span data-stu-id="bdf03-103">Implementing FormatProperties</span></span>

<span data-ttu-id="bdf03-104">Monitor de Rede chama a função [**formatproperties**](formatproperties.md) para formatar os dados que são exibidos no painel de detalhes da interface do usuário do monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="bdf03-104">Network Monitor calls the [**FormatProperties**](formatproperties.md) function to format the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="bdf03-105">Normalmente, **formatproperties** é chamado para formatar a linha de Resumo de um protocolo e, em seguida, Formatar todas as instâncias de Propriedade do protocolo dentro de um quadro.</span><span class="sxs-lookup"><span data-stu-id="bdf03-105">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="bdf03-106">No entanto, Monitor de Rede não identifica o número de vezes que **formatproperties** é chamado para um analisador específico.</span><span class="sxs-lookup"><span data-stu-id="bdf03-106">However, Network Monitor does not identify the number of times that **FormatProperties** is called for a specific parser.</span></span>

<span data-ttu-id="bdf03-107">Ao chamar [**formatproperties**](formatproperties.md), o monitor de rede fornece uma estrutura [**PROPERTYINST**](propertyinst.md) para cada propriedade exibida.</span><span class="sxs-lookup"><span data-stu-id="bdf03-107">When calling [**FormatProperties**](formatproperties.md), Network Monitor provides a [**PROPERTYINST**](propertyinst.md) structure for each property that it displays.</span></span> <span data-ttu-id="bdf03-108">A estrutura **PROPERTYINST** fornece informações sobre os dados a serem exibidos, incluindo um ponteiro para a estrutura [**PROPERTYINFO**](propertyinfo.md) que especifica a função a ser usada para formatar a propriedade de dados exibida.</span><span class="sxs-lookup"><span data-stu-id="bdf03-108">The **PROPERTYINST** structure provides information about the data to be displayed, including a pointer to the [**PROPERTYINFO**](propertyinfo.md) structure that specifies the function to use to format the displayed data property.</span></span>

> [!Note]  
> <span data-ttu-id="bdf03-109">Uma estrutura [**PROPERTYINFO**](propertyinfo.md) é especificada ao adicionar uma propriedade ao [*banco de dados de propriedade*](p.md) do analisador.</span><span class="sxs-lookup"><span data-stu-id="bdf03-109">A [**PROPERTYINFO**](propertyinfo.md) structure is specified when adding a property to the [*property database*](p.md) of the parser.</span></span>

 

<span data-ttu-id="bdf03-110">Monitor de Rede identifica a função de formato a ser chamada para cada instância de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bdf03-110">Network Monitor identifies the format function to call for each property instance.</span></span> <span data-ttu-id="bdf03-111">O membro **InstanceData** da estrutura [**PROPERTYINFO**](propertyinfo.md) pode especificar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bdf03-111">The **InstanceData** member of the [**PROPERTYINFO**](propertyinfo.md) structure can specify the following:</span></span>

-   <span data-ttu-id="bdf03-112">A função [**FormatPropertyInstance**](formatpropertyinstance.md) para usar o [*formatador genérico*](g.md) que o monitor de rede fornece.</span><span class="sxs-lookup"><span data-stu-id="bdf03-112">The [**FormatPropertyInstance**](formatpropertyinstance.md) function to use the [*generic formatter*](g.md) that Network Monitor provides.</span></span>

    <span data-ttu-id="bdf03-113">– ou –</span><span class="sxs-lookup"><span data-stu-id="bdf03-113">– or –</span></span>

-   <span data-ttu-id="bdf03-114">O nome de uma função de formato personalizado que o analisador fornece.</span><span class="sxs-lookup"><span data-stu-id="bdf03-114">The name of a custom format function that the parser provides.</span></span>

<span data-ttu-id="bdf03-115">As funções de formato [**FormatPropertyInstance**](formatpropertyinstance.md) e personalizado retornam os dados formatados que são exibidos no painel de detalhes da interface do usuário do monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="bdf03-115">The [**FormatPropertyInstance**](formatpropertyinstance.md) and the custom format functions return the formatted data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="bdf03-116">A ilustração a seguir mostra como Monitor de Rede identifica a função a ser chamada para cada instância de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bdf03-116">The following illustration shows how Network Monitor identifies the function to call for each property instance.</span></span>

![como o monitor de rede identifica a função a ser chamada](images/formatprop1.png)

<span data-ttu-id="bdf03-118">O procedimento a seguir identifica as etapas necessárias para implementar [**formatproperties**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="bdf03-118">The following procedure identifies the steps necessary to implement [**FormatProperties**](formatproperties.md).</span></span>

<span data-ttu-id="bdf03-119">**Para implementar Formatproperties**</span><span class="sxs-lookup"><span data-stu-id="bdf03-119">**To implement FormatProperties**</span></span>

-   <span data-ttu-id="bdf03-120">Usando uma estrutura de loop, chame a função Format para cada estrutura [**PROPERTYINST**](propertyinst.md) que é passada para o analisador no parâmetro *LpPropInst* da função [**formatproperties**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="bdf03-120">Using a loop structure, call the format function for each [**PROPERTYINST**](propertyinst.md) structure that is passed to the parser in the *lpPropInst* parameter of the [**FormatProperties**](formatproperties.md) function.</span></span>

<span data-ttu-id="bdf03-121">A seguir está uma implementação básica de [**formatproperties**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="bdf03-121">The following is a basic implementation of [**FormatProperties**](formatproperties.md).</span></span>

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



