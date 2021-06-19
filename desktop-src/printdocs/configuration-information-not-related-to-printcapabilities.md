---
description: Além de PrintCapabilities, o PrintTicket permite que informações adicionais sejam adicionadas por clientes na forma de elementos Property.
ms.assetid: 00f1d2c4-3c71-4b64-b689-83b4399aa61d
title: Informações de configuração não relacionadas a PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e4ac332d6e9b106ab9d68c29d03366761c01d5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409649"
---
# <a name="configuration-information-not-related-to-printcapabilities"></a><span data-ttu-id="4f92e-103">Informações de configuração não relacionadas a PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="4f92e-103">Configuration Information Not Related to PrintCapabilities</span></span>

<span data-ttu-id="4f92e-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="4f92e-104">This topic is not current.</span></span> <span data-ttu-id="4f92e-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4f92e-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4f92e-106">Além de fornecer seleções para os atributos de dispositivo definidos em PrintCapabilities, o PrintTicket permite que informações adicionais sejam adicionadas por clientes na forma de elementos Property.</span><span class="sxs-lookup"><span data-stu-id="4f92e-106">In addition to providing selections for the device attributes defined in the PrintCapabilities, the PrintTicket allows additional information to be added by clients in the form of Property elements.</span></span> <span data-ttu-id="4f92e-107">O Esquema de Impressão define várias instâncias de Propriedade padrão e o provedor de interface também é livre para introduzir instâncias de Propriedade privada.</span><span class="sxs-lookup"><span data-stu-id="4f92e-107">The Print Schema defines a number of standard Property instances, and the interface provider is free to introduce private Property instances as well.</span></span> <span data-ttu-id="4f92e-108">Por exemplo, se os membros de uma organização enviarem a maioria de seus trabalhos de impressão para um recurso de lote central, eles poderão especificar para cada trabalho uma instância de Propriedade privada que contém um endereço de retorno.</span><span class="sxs-lookup"><span data-stu-id="4f92e-108">For example, if members of an organization send most of their print jobs to a central batch facility, they can specify for each job a private Property instance that contains a return address.</span></span> <span data-ttu-id="4f92e-109">Essa propriedade pode facilitar a entrega do trabalho concluído pode ser entregue ao originador.</span><span class="sxs-lookup"><span data-stu-id="4f92e-109">This Property can make it easier to deliver the completed job can be delivered to the originator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f92e-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f92e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f92e-111">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="4f92e-111">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



