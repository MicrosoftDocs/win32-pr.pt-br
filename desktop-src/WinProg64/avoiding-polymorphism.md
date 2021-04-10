---
title: Evitando o polimorfismo
description: Os novos tipos de dados incluem dois tipos polimórficos, INT \_ PTR e Long \_ PTR.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- Programação do Windows de polimorfismo de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292714"
---
# <a name="avoiding-polymorphism"></a><span data-ttu-id="d770e-104">Evitando o polimorfismo</span><span class="sxs-lookup"><span data-stu-id="d770e-104">Avoiding Polymorphism</span></span>

<span data-ttu-id="d770e-105">Os novos tipos de dados incluem dois tipos polimórficos, **int \_ PTR** e **Long \_ PTR**.</span><span class="sxs-lookup"><span data-stu-id="d770e-105">The new data types include two polymorphic types, **INT\_PTR** and **LONG\_PTR**.</span></span> <span data-ttu-id="d770e-106">No Windows de 32 bits, o **int \_ PTR** mapeia para **int** e o **\_ PTR longo** mapeia para **Long**.</span><span class="sxs-lookup"><span data-stu-id="d770e-106">On 32-bit Windows, the **INT\_PTR** maps to **int** and the **LONG\_PTR** maps to **long**.</span></span> <span data-ttu-id="d770e-107">No Windows de 64 bits, os dois tipos são mapeados para o tipo intrínseco **\_ \_ Int64** .</span><span class="sxs-lookup"><span data-stu-id="d770e-107">On 64-bit Windows, both types map to the **\_\_int64** intrinsic type.</span></span> <span data-ttu-id="d770e-108">O compilador MIDL dá suporte a esses tipos para chamadas de procedimento remoto, mas há uma limitação inerente que você deve ter em mente ao usá-los em um ambiente distribuído.</span><span class="sxs-lookup"><span data-stu-id="d770e-108">The MIDL compiler supports these types for remote procedure calls, but there is an inherent limitation that you must keep in mind when using them in a distributed environment.</span></span> <span data-ttu-id="d770e-109">Lembre-se de comentar seu código de acordo.</span><span class="sxs-lookup"><span data-stu-id="d770e-109">Be sure to comment your code accordingly.</span></span>

<span data-ttu-id="d770e-110">Independentemente do tamanho da plataforma, o tamanho da conexão desses tipos polimórficos é sempre de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d770e-110">Regardless of the platform size, the wire size of these polymorphic types is always 32 bits.</span></span> <span data-ttu-id="d770e-111">Ao desempacotar no Windows de 64 bits, o logon da biblioteca de tempo de execução estende os valores assinados e atribui zero aos bytes de ordem superior para um valor não assinado.</span><span class="sxs-lookup"><span data-stu-id="d770e-111">When unmarshaling on 64-bit Windows, the run-time library sign extends signed values and assigns zero to the high-order bytes for an unsigned value.</span></span> <span data-ttu-id="d770e-112">Ao colocar um valor de 64 bits na transmissão, o tempo de execução trunca os bytes de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="d770e-112">When putting a 64-bit value on the wire, the run time truncates the high-order bytes.</span></span> <span data-ttu-id="d770e-113">Portanto, somente os valores de 32 bits de ordem inferior são utilizáveis.</span><span class="sxs-lookup"><span data-stu-id="d770e-113">Thus, only the low-order 32-bit values are usable.</span></span>

<span data-ttu-id="d770e-114">Use os tipos polimórficos somente quando necessário para portabilidade.</span><span class="sxs-lookup"><span data-stu-id="d770e-114">Use the polymorphic types only when necessary for porting.</span></span> <span data-ttu-id="d770e-115">Para novas interfaces, use os tipos inteiros intrínsecos de MIDL **\_ \_ Int32** e **\_ \_ Int64** ou use um tipo de ponteiro ou identificador de contexto, o que for mais apropriado para o tipo de dados que está sendo transferido.</span><span class="sxs-lookup"><span data-stu-id="d770e-115">For new interfaces, use the MIDL intrinsic integer types **\_\_int32** and **\_\_int64**, or use a pointer type or context handle, whichever is most appropriate for the kind of data being transferred.</span></span>

<span data-ttu-id="d770e-116">O compilador de 64 bits dá suporte a um novo **\_ \_ int3264** intrínseco de polimórfico.</span><span class="sxs-lookup"><span data-stu-id="d770e-116">The 64-bit compiler supports a new polymorphic intrinsic **\_\_int3264**.</span></span> <span data-ttu-id="d770e-117">Novamente, esse tipo foi desenvolvido para dar suporte a esforços de portabilidade, neste caso, para dar suporte aos tipos de **\_ PTR de uint** de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="d770e-117">Again, this type was developed to support porting efforts, in this case to support the **UINT\_PTR** types transparently.</span></span> <span data-ttu-id="d770e-118">(Outro intrínseco, **\_ \_ long3264**, dará suporte ao tipo de **\_ PTR de ULong** .) Não use **\_ \_ int3264** diretamente; use o tipo **de \_ PTR** , quando precisar de um tipo polimórfico para portar motivos.</span><span class="sxs-lookup"><span data-stu-id="d770e-118">(Another intrinsic, **\_\_long3264**, will support the **ULONG\_PTR** type.) Do not use **\_\_int3264** directly; use the **INT\_PTR** type when you need a polymorphic type for porting reasons.</span></span>

 

 




