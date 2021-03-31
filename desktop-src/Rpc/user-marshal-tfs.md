---
title: Marshal do usuário
description: Marshaling do usuário na chamada de procedimento remoto (RPC).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822630"
---
# <a name="user-marshal"></a><span data-ttu-id="c21c5-103">Marshal do usuário</span><span class="sxs-lookup"><span data-stu-id="c21c5-103">User-marshal</span></span>

<span data-ttu-id="c21c5-104">O marshaling do usuário tem uma cadeia de caracteres de formato semelhante a transmitir \_ como:</span><span class="sxs-lookup"><span data-stu-id="c21c5-104">User marshal has a format string that is similar to transmit\_as:</span></span>

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

<span data-ttu-id="c21c5-105">Os sinalizadores<1> byte consiste no Nibble superior do sinalizador e no Nibble inferior do alinhamento.</span><span class="sxs-lookup"><span data-stu-id="c21c5-105">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="c21c5-106">Os dois bits superiores do demarcador Nibble são usados para descrever se o tipo de conexão é definido como um ponteiro exclusivo, um ponteiro de referência ou nenhum ponteiro (não pode ser um PTR).</span><span class="sxs-lookup"><span data-stu-id="c21c5-106">The upper 2 bits of the flag nibble are used to describe whether the wire type is defined as a unique pointer, reference pointer or no pointer (it cannot be a ptr).</span></span> <span data-ttu-id="c21c5-107">Os seguintes manifestos foram definidos para definir/obter os sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="c21c5-107">The following manifests have been defined to set/get the flags:</span></span>

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

<span data-ttu-id="c21c5-108">O Nibble de alinhamento da palavra de sinalizador mantém o alinhamento de fios do tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="c21c5-108">The alignment nibble of the flag word keeps the wire alignment of the transmitted type.</span></span>

<span data-ttu-id="c21c5-109">O índice quádruplo \_<2> é um índice da rotina de retorno de chamada quádruplo das funções de marshaling do usuário.</span><span class="sxs-lookup"><span data-stu-id="c21c5-109">The quadruple\_index<2> is an index of the callback routine quadruple of the user marshal functions.</span></span> <span data-ttu-id="c21c5-110">As posições de rotina são as seguintes: dimensionamento, empacotamento, desempacotamento e rotina de liberação.</span><span class="sxs-lookup"><span data-stu-id="c21c5-110">The routine positions are as follow: sizing, marshaling, unmarshaling, and freeing routine.</span></span>

<span data-ttu-id="c21c5-111">O tamanho da memória do tipo de usuário \_ \_ \_<2> fornece um tamanho para o tipo específico do usuário, incluindo tipos desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="c21c5-111">The user\_type\_memory\_size<2> provides a size for the user specific type, including unknown types.</span></span>

<span data-ttu-id="c21c5-112">O tamanho do buffer de tipo transmitido \_ \_ \_<2> é zero quando o tamanho é variável ou o tamanho fixo real.</span><span class="sxs-lookup"><span data-stu-id="c21c5-112">The transmitted\_type\_buffer\_size<2> is either zero when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="c21c5-113">Essa é uma otimização que permite ao MIDL ignorar retornos de chamada ao dimensionar o buffer e também ao liberar.</span><span class="sxs-lookup"><span data-stu-id="c21c5-113">This is an optimization that enables MIDL to skip callbacks when sizing the buffer, and also when freeing.</span></span>

## <a name="range"></a><span data-ttu-id="c21c5-114">Intervalo</span><span class="sxs-lookup"><span data-stu-id="c21c5-114">Range</span></span>

<span data-ttu-id="c21c5-115">A \[ verificação de intervalo \] fornece meios adicionais para validação de argumento na camada de NDR.</span><span class="sxs-lookup"><span data-stu-id="c21c5-115">The \[range\] checking provides additional means for argument validation at the NDR layer.</span></span> <span data-ttu-id="c21c5-116">O \[ \] descritor de intervalo tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="c21c5-116">The \[range\] descriptor has the following format:</span></span>

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

<span data-ttu-id="c21c5-117">Os sinalizadores assumem o Nibble superior e o tipo o Nibble inferior do segundo byte.</span><span class="sxs-lookup"><span data-stu-id="c21c5-117">The flags take the upper nibble and the type the lower nibble of the second byte.</span></span> <span data-ttu-id="c21c5-118">Os valores baixos e altos dependem do tipo da variável a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="c21c5-118">The low and high values depend on the type of the variable to be checked.</span></span>

<span data-ttu-id="c21c5-119">Os sinalizadores são destinados a um veículo de expansão; o compilador tem definido o Nibble para zero.</span><span class="sxs-lookup"><span data-stu-id="c21c5-119">The flags are meant as an expansion vehicle; the compiler has been setting the nibble to zero.</span></span>

 

 




