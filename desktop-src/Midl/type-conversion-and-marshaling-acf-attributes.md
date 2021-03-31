---
title: Type-Conversion e empacotamento de atributos ACF
description: Use esses atributos para controlar como os dados são transmitidos pela rede.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- MIDL de ACF, atributos, conversão de tipos e marshaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916519"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a><span data-ttu-id="07c70-104">Type-Conversion e empacotamento de atributos ACF</span><span class="sxs-lookup"><span data-stu-id="07c70-104">Type-Conversion and Marshaling ACF Attributes</span></span>

<span data-ttu-id="07c70-105">Use esses atributos para controlar como os dados são transmitidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="07c70-105">Use these attributes to control how your data is transmitted over the network.</span></span>



| <span data-ttu-id="07c70-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="07c70-106">Attribute</span></span>                                        | <span data-ttu-id="07c70-107">Uso</span><span class="sxs-lookup"><span data-stu-id="07c70-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c70-108">[](encode.md)[ codificação de codificação](decode.md)</span><span class="sxs-lookup"><span data-stu-id="07c70-108">[**encode**](encode.md)[**decode**](decode.md)</span></span> | <span data-ttu-id="07c70-109">Instrui o MIDL a expor as rotinas de serialização de tipo ou de procedimento (escolha) que gera para os stubs.</span><span class="sxs-lookup"><span data-stu-id="07c70-109">Instructs MIDL to expose the type or procedure serialization (pickling) routines it generates for the stubs.</span></span> <span data-ttu-id="07c70-110">Seu aplicativo cliente pode chamar essas rotinas para realizar marshaling de dados por valor.</span><span class="sxs-lookup"><span data-stu-id="07c70-110">Your client application can call those routines to marshal data by value.</span></span>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="07c70-111">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="07c70-111">**represent\_as**</span></span>](represent-as.md)            | <span data-ttu-id="07c70-112">Especifica como um tipo de dados será representado na conexão, quando a natureza exata do tipo de dados de um cliente não for importante para o servidor (porque ele só precisa dos dados em si e não da estrutura real) ou o tipo de cliente real é desconhecido para MIDL no tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="07c70-112">Specifies how a data type will be represented on the wire, when the exact nature of a client's data type is unimportant to the server (because it only needs the data itself and not the actual structure), or the actual client type is unknown to MIDL at compile time.</span></span> <span data-ttu-id="07c70-113">Por exemplo, se o aplicativo cliente usar uma lista vinculada de números de ponto flutuante, você poderá especificar que a representação de transmissão dessa lista seja uma matriz do tipo [**float**](float.md).</span><span class="sxs-lookup"><span data-stu-id="07c70-113">For example, if your client application uses a linked list of floating-point numbers, you could specify that the wire-representation of that list be an array of type [**float**](float.md).</span></span> |
| [<span data-ttu-id="07c70-114">**Marshal do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="07c70-114">**user\_marshal**</span></span>](user-marshal.md)            | <span data-ttu-id="07c70-115">Controla como os dados são transmitidos pela rede implementando suas próprias rotinas de marshaling.</span><span class="sxs-lookup"><span data-stu-id="07c70-115">Controls how data is transmitted over the wire by implementing your own marshaling routines.</span></span> <span data-ttu-id="07c70-116">Esse atributo será útil se você tiver um tipo de dados desconhecido para MIDL ou se estiver passando informações entre plataformas big endian e little-endian.</span><span class="sxs-lookup"><span data-stu-id="07c70-116">This attribute is useful if you have a data type that is unknown to MIDL or if you are passing information between big-endian and little-endian platforms.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="07c70-117">Os atributos de marshaling de DCE [**em \_ linha**](in-line.md) e [**fora \_ de \_ linha**](out-of-line.md) não são implementados no Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="07c70-117">The DCE marshaling attributes [**in\_line**](in-line.md) and [**out\_of\_line**](out-of-line.md) are not implemented in Microsoft RPC.</span></span> <span data-ttu-id="07c70-118">O compilador MIDL realiza marshaling automaticamente de tipos de dados complexos fora de linha.</span><span class="sxs-lookup"><span data-stu-id="07c70-118">The MIDL compiler automatically marshals complex data types out-of-line.</span></span>

 

 




