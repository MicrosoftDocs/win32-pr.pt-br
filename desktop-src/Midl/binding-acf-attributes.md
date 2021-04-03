---
title: Atributos de ACF de associação
description: Especifique como o cliente se conecta ao servidor para chamadas de procedimento remoto com os atributos listados na tabela a seguir.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- MIDL de ACF, atributos, associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005916"
---
# <a name="binding-acf-attributes"></a><span data-ttu-id="57e79-104">Atributos de ACF de associação</span><span class="sxs-lookup"><span data-stu-id="57e79-104">Binding ACF Attributes</span></span>

<span data-ttu-id="57e79-105">Especifique como o cliente se conecta ao servidor para chamadas de procedimento remoto com os atributos listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="57e79-105">Specify how the client connects to the server for remote procedure calls with the attributes listed in the following table.</span></span>



| <span data-ttu-id="57e79-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="57e79-106">Attribute</span></span>                                                          | <span data-ttu-id="57e79-107">Uso</span><span class="sxs-lookup"><span data-stu-id="57e79-107">Usage</span></span>                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57e79-108">**Async**</span><span class="sxs-lookup"><span data-stu-id="57e79-108">**async**</span></span>](async.md)                                             | <span data-ttu-id="57e79-109">Define um identificador que permite que o chamador faça uma chamada assíncrona e retorne imediatamente sem esperar pelos resultados e, em seguida, sincronize novamente com a função chamada para receber dados após a conclusão da chamada.</span><span class="sxs-lookup"><span data-stu-id="57e79-109">Defines a handle that allows the caller to make an asynchronous call and return immediately without waiting for results, and then resynchronize with the called function to receive data after the call completes.</span></span> |
| [<span data-ttu-id="57e79-110">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="57e79-110">**auto\_handle**</span></span>](auto-handle.md)                                | <span data-ttu-id="57e79-111">Informa ao MIDL para permitir que o código de stub controle a associação automaticamente.</span><span class="sxs-lookup"><span data-stu-id="57e79-111">Tells MIDL to let the stub code control the binding automatically.</span></span> <span data-ttu-id="57e79-112">Esse será o padrão se você não especificar nenhum identificador de ligação.</span><span class="sxs-lookup"><span data-stu-id="57e79-112">This is the default if you don't specify any binding handle.</span></span>                                                                                    |
| [<span data-ttu-id="57e79-113">**identificador de contexto \_ \_ noserializeize**</span><span class="sxs-lookup"><span data-stu-id="57e79-113">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md) | <span data-ttu-id="57e79-114">Garante que um identificador de contexto nunca será serializado, independentemente do comportamento padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57e79-114">Guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>                                                                                                       |
| [<span data-ttu-id="57e79-115">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="57e79-115">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)     | <span data-ttu-id="57e79-116">Garante que um identificador de contexto sempre será serializado, independentemente do comportamento padrão do aplicativo</span><span class="sxs-lookup"><span data-stu-id="57e79-116">Guarantees that a context handle will always be serialized, regardless of the application's default behavior</span></span>                                                                                                       |
| [<span data-ttu-id="57e79-117">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="57e79-117">**explicit\_handle**</span></span>](explicit-handle.md)                        | <span data-ttu-id="57e79-118">Permite que o aplicativo cliente controle a associação com um parâmetro explícito em cada procedimento.</span><span class="sxs-lookup"><span data-stu-id="57e79-118">Lets the client application control the binding with an explicit parameter in each procedure.</span></span>                                                                                                                      |
| [<span data-ttu-id="57e79-119">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="57e79-119">**implicit\_handle**</span></span>](implicit-handle.md)                        | <span data-ttu-id="57e79-120">Especifica um identificador para procedimentos que não têm um parâmetro identificador explícito.</span><span class="sxs-lookup"><span data-stu-id="57e79-120">Specifies a handle for procedures that do not have an explicit handle parameter.</span></span> <span data-ttu-id="57e79-121">O aplicativo cliente ainda controla a associação.</span><span class="sxs-lookup"><span data-stu-id="57e79-121">The client application still controls the binding.</span></span>                                                                                |
| [<span data-ttu-id="57e79-122">**\_identificador de contexto estrito \_**</span><span class="sxs-lookup"><span data-stu-id="57e79-122">**strict\_context\_handle**</span></span>](strict-context-handle.md)           | <span data-ttu-id="57e79-123">Garante que os métodos na interface aceitem apenas identificadores de contexto que foram criados por um método dessa interface.</span><span class="sxs-lookup"><span data-stu-id="57e79-123">Guarantees that the methods in the interface will only accept context handles that were created by a method of that interface.</span></span>                                                                                     |



 

 

 




