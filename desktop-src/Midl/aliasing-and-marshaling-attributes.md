---
title: Atributos de alias e empacotamento
description: Os aplicativos distribuídos quase sempre passam dados entre os programas cliente e servidor quando chamam procedimentos de interface.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- MIDL de IDL, atributos MIDL, alias e marshaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006099"
---
# <a name="aliasing-and-marshaling-attributes"></a><span data-ttu-id="f684e-104">Atributos de alias e empacotamento</span><span class="sxs-lookup"><span data-stu-id="f684e-104">Aliasing and Marshaling Attributes</span></span>

<span data-ttu-id="f684e-105">Os aplicativos distribuídos quase sempre passam dados entre os programas cliente e servidor quando chamam procedimentos de interface.</span><span class="sxs-lookup"><span data-stu-id="f684e-105">Distributed applications almost always pass data between client and server programs when they call interface procedures.</span></span> <span data-ttu-id="f684e-106">Os desenvolvedores usam MIDL para descrever os dados que os programas de cliente e servidor passam de forma padrão.</span><span class="sxs-lookup"><span data-stu-id="f684e-106">Developers use MIDL to describe the data that client and server programs pass in a standard way.</span></span> <span data-ttu-id="f684e-107">O compilador MIDL cria o stub do aplicativo, ou o proxy, programas para o cliente e o servidor que convertem os dados em um formato padronizado que pode ser enviado por uma rede.</span><span class="sxs-lookup"><span data-stu-id="f684e-107">The MIDL compiler creates application stub, or proxy, programs for the client and the server that convert the data into a standardized form that can be sent over a network.</span></span> <span data-ttu-id="f684e-108">Esse formato, o formato NDR (representação de dados de rede), geralmente é chamado de formato de conexão dos dados.</span><span class="sxs-lookup"><span data-stu-id="f684e-108">This format, the Network Data Representation (NDR) format, is often called the wire format of the data.</span></span> <span data-ttu-id="f684e-109">Os stubs devem converter dados de seu formato nativo no espaço de memória do programa para o NDR.</span><span class="sxs-lookup"><span data-stu-id="f684e-109">The stubs must convert data from its native format in the program's memory space to NDR.</span></span> <span data-ttu-id="f684e-110">Essa conversão é chamada de marshaling dos dados.</span><span class="sxs-lookup"><span data-stu-id="f684e-110">This conversion is termed marshaling the data.</span></span> <span data-ttu-id="f684e-111">Quando um cliente ou programa de servidor recebe dados, ele deve converter os dados do NDR para o formato nativo para esse programa.</span><span class="sxs-lookup"><span data-stu-id="f684e-111">When a client or server program receives data, it must convert the data from NDR to the native format for that program.</span></span> <span data-ttu-id="f684e-112">Isso é chamado de desempacotamento dos dados.</span><span class="sxs-lookup"><span data-stu-id="f684e-112">This is called unmarshaling the data.</span></span>

<span data-ttu-id="f684e-113">Use atributos de alias e de marshaling para controlar como os dados são empacotados em formato NDR e transmitidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="f684e-113">Use aliasing and marshaling attributes to control how your data is packaged into NDR format and transmitted over the network.</span></span>



| <span data-ttu-id="f684e-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="f684e-114">Attribute</span></span>                             | <span data-ttu-id="f684e-115">Uso</span><span class="sxs-lookup"><span data-stu-id="f684e-115">Usage</span></span>                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f684e-116">**chamar \_ como**</span><span class="sxs-lookup"><span data-stu-id="f684e-116">**call\_as**</span></span>](call-as.md)           | <span data-ttu-id="f684e-117">Mapeia uma função não Remotable para uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="f684e-117">Maps a nonremotable function to a remote procedure call.</span></span>                                                                      |
| [<span data-ttu-id="f684e-118">**IID \_ é**</span><span class="sxs-lookup"><span data-stu-id="f684e-118">**iid\_is**</span></span>](iid-is.md)             | <span data-ttu-id="f684e-119">Fornece o identificador de interface da interface COM que é o objeto do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="f684e-119">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                     |
| [<span data-ttu-id="f684e-120">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="f684e-120">**transmit\_as**</span></span>](transmit-as.md)   | <span data-ttu-id="f684e-121">Converte um tipo de dados em um tipo mais simples para transmissão em uma rede.</span><span class="sxs-lookup"><span data-stu-id="f684e-121">Converts a data type to a simpler type for transmission over a network.</span></span>                                                       |
| [<span data-ttu-id="f684e-122">**\_marshaling de transmissão**</span><span class="sxs-lookup"><span data-stu-id="f684e-122">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="f684e-123">Semelhante a [**transmitir \_ como**](transmit-as.md) , mas você implementa as rotinas para dimensionar, realizar marshaling, desempacotar e liberar os dados.</span><span class="sxs-lookup"><span data-stu-id="f684e-123">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f684e-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f684e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f684e-125">Conversão de tipo e empacotamento de atributos ACF</span><span class="sxs-lookup"><span data-stu-id="f684e-125">Type Conversion and Marshaling ACF Attributes</span></span>](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




