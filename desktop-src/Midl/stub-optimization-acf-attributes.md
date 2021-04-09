---
title: Atributos de ACF de otimização de stub
description: Esses atributos permitem otimizar o tamanho e a velocidade do seu código stub.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- MIDL de ACF, atributos, otimização de stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822501"
---
# <a name="stub-optimization-acf-attributes"></a><span data-ttu-id="ee348-104">Atributos de ACF de otimização de stub</span><span class="sxs-lookup"><span data-stu-id="ee348-104">Stub Optimization ACF Attributes</span></span>

<span data-ttu-id="ee348-105">Esses atributos permitem otimizar o tamanho e a velocidade do seu código stub.</span><span class="sxs-lookup"><span data-stu-id="ee348-105">These attributes enable you to optimize the size and speed of your stub code.</span></span>



| <span data-ttu-id="ee348-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="ee348-106">Attribute</span></span>                                    | <span data-ttu-id="ee348-107">Uso</span><span class="sxs-lookup"><span data-stu-id="ee348-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee348-108">[**código**](code.md)[**Nocode**](nocode.md)</span><span class="sxs-lookup"><span data-stu-id="ee348-108">[**code**](code.md)[**nocode**](nocode.md)</span></span> | <span data-ttu-id="ee348-109">Use os atributos [**Code**](code.md) e [**Nocode**](nocode.md) juntos para evitar a geração de código stub para funções não utilizadas.</span><span class="sxs-lookup"><span data-stu-id="ee348-109">Use the [**code**](code.md) and [**nocode**](nocode.md) attributes together to avoid generating stub code for unused functions.</span></span> <span data-ttu-id="ee348-110">Aplique o atributo **Nocode** ao cabeçalho da interface e aplique o atributo **Code** a esses procedimentos que o aplicativo cliente irá implementar.</span><span class="sxs-lookup"><span data-stu-id="ee348-110">Apply the **nocode** attribute to the interface header, and apply the **code** attribute to those procedures that the client application will implement.</span></span> <span data-ttu-id="ee348-111">O código stub do cliente será gerado somente para os procedimentos selecionados.</span><span class="sxs-lookup"><span data-stu-id="ee348-111">Client stub code will be generated only for the selected procedures.</span></span>                                                                |
| [<span data-ttu-id="ee348-112">**formato**</span><span class="sxs-lookup"><span data-stu-id="ee348-112">**optimize**</span></span>](optimize.md)                 | <span data-ttu-id="ee348-113">Permite ajustar o nível de otimização que o compilador MIDL executa ao gerar código stub, especificando que os dados serão empacotados pelo método misto ou interpretado.</span><span class="sxs-lookup"><span data-stu-id="ee348-113">Lets you fine-tune the level of optimization that the MIDL compiler performs when generating stub code, by specifying that data is to be marshaled by either the mixed-mode or interpreted method.</span></span> <span data-ttu-id="ee348-114">Você pode aplicar o atributo [**Optimize**](optimize.md) a uma interface ou a funções selecionadas dentro da interface.</span><span class="sxs-lookup"><span data-stu-id="ee348-114">You can apply the [**optimize**](optimize.md) attribute to an interface or to selected functions within the interface.</span></span> <span data-ttu-id="ee348-115">Em ambos os casos, seu uso substituirá as otimizações de linha de comando e quaisquer padrões preexistentes.</span><span class="sxs-lookup"><span data-stu-id="ee348-115">In either case, its use will override the command-line optimizations and any pre-existing defaults.</span></span> |



 

 

 




