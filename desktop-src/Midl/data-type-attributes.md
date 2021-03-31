---
title: Atributos de tipo de dados
description: Você pode aplicar esses atributos a tipos de dados em uma instrução typedef para definir ainda mais o uso ou o efeito do tipo de dados.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- MIDL, atributos, tipo de dados IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637191"
---
# <a name="data-type-attributes"></a><span data-ttu-id="4fd8f-104">Atributos de tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4fd8f-104">Data Type Attributes</span></span>

<span data-ttu-id="4fd8f-105">Você pode aplicar esses atributos a tipos de dados em uma instrução [**typedef**](typedef.md) para definir ainda mais o uso ou o efeito do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-105">You can apply these attributes to data types in a [**typedef**](typedef.md) statement to further define the usage or effect of the data type.</span></span>



| <span data-ttu-id="4fd8f-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="4fd8f-106">Attribute</span></span>                                 | <span data-ttu-id="4fd8f-107">Uso</span><span class="sxs-lookup"><span data-stu-id="4fd8f-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4fd8f-108">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="4fd8f-108">**context\_handle**</span></span>](context-handle.md) | <span data-ttu-id="4fd8f-109">Identifica um identificador de associação que mantém informações de estado (contexto) em um servidor específico entre chamadas de procedimento remotos de um cliente específico.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-109">Identifies a binding handle that maintains state (context) information on a particular server between remote procedure calls from a particular client.</span></span> <span data-ttu-id="4fd8f-110">Não é válido para funções de interface de [**objeto**](object.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd8f-110">Not valid for [**object**](object.md) interface functions.</span></span>                                                                                                         |
| [<span data-ttu-id="4fd8f-111">**processamento**</span><span class="sxs-lookup"><span data-stu-id="4fd8f-111">**handle**</span></span>](handle.md)                  | <span data-ttu-id="4fd8f-112">Especifica um tipo de identificador personalizado específico para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-112">Specifies a custom handle type specific to the application.</span></span>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="4fd8f-113">**\_União MS**</span><span class="sxs-lookup"><span data-stu-id="4fd8f-113">**ms\_union**</span></span>](-ms-union.md)            | <span data-ttu-id="4fd8f-114">Controla o alinhamento de NDR de uniões não encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-114">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="4fd8f-115">Use em [**typedef**](typedef.md)s para compatibilidade com versões anteriores com interfaces criadas com MIDL 1,0 ou 2,0.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-115">Use on [**typedef**](typedef.md)s for backward compatibility with interfaces built with MIDL 1.0 or 2.0.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="4fd8f-116">**pipe**</span><span class="sxs-lookup"><span data-stu-id="4fd8f-116">**pipe**</span></span>](pipe.md)                      | <span data-ttu-id="4fd8f-117">Permite a transmissão de um fluxo aberto de dados digitados através de uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-117">Allows transmission of an open-ended stream of typed data across a remote procedure call.</span></span> <span data-ttu-id="4fd8f-118">Um parâmetro [**no**](in.md) pipe permite que o servidor receba o fluxo de dados do cliente durante uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-118">An [**in**](in.md) pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="4fd8f-119">Um parâmetro [**out**](-out.md) pipe permite que o servidor envie por push o fluxo de dados de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-119">An [**out**](-out.md) pipe parameter allows the server to push the data stream back to the client.</span></span> |
| [<span data-ttu-id="4fd8f-120">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="4fd8f-120">**transmit\_as**</span></span>](transmit-as.md)       | <span data-ttu-id="4fd8f-121">Especifica como um tipo de dados será transmitido em uma rede, usado para marshaling personalizado.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-121">Specifies how a data type will be transmitted over a network, used for custom marshaling.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="4fd8f-122">**\_Enumeração v1**</span><span class="sxs-lookup"><span data-stu-id="4fd8f-122">**v1\_enum**</span></span>](v1-enum.md)               | <span data-ttu-id="4fd8f-123">Direciona que o tipo enumerado especificado seja transmitido como uma entidade de 32 bits, em vez do padrão de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-123">Directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>                                                                                                                                                                                                              |
| [<span data-ttu-id="4fd8f-124">**\_marshaling de transmissão**</span><span class="sxs-lookup"><span data-stu-id="4fd8f-124">**wire\_marshal**</span></span>](wire-marshal.md)     | <span data-ttu-id="4fd8f-125">Semelhante a [**transmitir \_ como**](transmit-as.md) , mas você implementa as rotinas para dimensionar, realizar marshaling, desempacotar e liberar os dados.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-125">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span>                                                                                                                                                                                              |



 

 

 




