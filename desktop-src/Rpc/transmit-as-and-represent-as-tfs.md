---
title: Transmit_as e Represent_as
description: Transmitir \_ como e representar \_ como compartilhar o mesmo layout, exceto para o token principal; o token lê a \_ transmissão FC \_ como ou FC \_ representa \_ como, mas o código subjacente é comum.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917345"
---
# <a name="transmit_as-and-represent_as"></a><span data-ttu-id="cbc3f-103">Transmitir \_ como e representar \_ como</span><span class="sxs-lookup"><span data-stu-id="cbc3f-103">Transmit\_as and Represent\_as</span></span>

<span data-ttu-id="cbc3f-104">Transmitir \_ como e representar \_ como compartilhar o mesmo layout, exceto para o token principal; o token lê a \_ transmissão FC \_ como ou FC \_ representa \_ como, mas o código subjacente é comum.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-104">Transmit\_as and represent\_as share the same layout except for the leading token; the token reads FC\_TRANSMIT\_AS or FC\_REPRESENT\_AS, but the underlying code is common.</span></span>

<span data-ttu-id="cbc3f-105">A descrição tem o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="cbc3f-105">The description has the following layout:</span></span>

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

<span data-ttu-id="cbc3f-106">Os sinalizadores<1> byte consiste no Nibble superior do sinalizador e no Nibble inferior do alinhamento.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-106">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="cbc3f-107">O Nibble de alinhamento mantém o alinhamento de fios do tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-107">The alignment nibble keeps the wire alignment of the transmitted type.</span></span> <span data-ttu-id="cbc3f-108">Isso é necessário quando o dimensionamento do buffer e o uso do tamanho do tipo transmitido do código de formato.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-108">This is needed when buffer sizing and using the transmitted type size from the format code.</span></span>

<span data-ttu-id="cbc3f-109">O Nibble do sinalizador pode ter os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="cbc3f-109">The flag nibble can have the following flags:</span></span>

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

<span data-ttu-id="cbc3f-110">O \_ tipo apresentado \_ é \_ um sinalizador de matriz marca um argumento de transmissão de nível superior como (ou representa como), sendo uma matriz de algo e valor de aprovado por.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-110">The PRESENTED\_TYPE\_IS\_ARRAY flag marks a top-level transmit as (or represent as) argument being an array of something and passed-by value.</span></span> <span data-ttu-id="cbc3f-111">O intérprete [**– Oi**](/windows/desktop/Midl/-oi) usa esse sinalizador para percorrer esse argumento (que é, na verdade, um ponteiro na pilha, não na matriz).</span><span class="sxs-lookup"><span data-stu-id="cbc3f-111">The [**–Oi**](/windows/desktop/Midl/-oi) interpreter uses this flag to step over such an argument (which is actually a pointer on stack, not the array).</span></span> <span data-ttu-id="cbc3f-112">Os outros dois sinalizadores também são usados apenas em interpretadores anteriores para passar corretamente por um tipo apresentado na pilha.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-112">The other two flags are also used only in previous interpreters to step correctly over a presented type on the stack.</span></span>

<span data-ttu-id="cbc3f-113">O \_ índice quintuple<2> é um índice da rotina de retorno de chamada quintuple (isso é, na verdade, um quádruplo) de funções.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-113">The quintuple\_index<2> is an index of the callback routine quintuple (this is actually a quadruple) of functions.</span></span> <span data-ttu-id="cbc3f-114">A tabela é comum para transmitir como e representar como e há um mapeamento óbvio para a posição das rotinas, como o mesmo serviço de pontos de entrada é transmitido como e representa como códigos.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-114">The table is common to both transmit as and represent as and there is an obvious mapping for the position of the routines, as the same entry points service transmit as and represent as codes.</span></span> <span data-ttu-id="cbc3f-115">O mapeamento é de \_ local => para \_ transmissão, para \_ local => de \_ transmissão, \_ Inst gratuito => \_ transmissão gratuita, \_ local livre => Free \_ Inst.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-115">The mapping is from\_local => to\_xmit, to\_local => from\_xmit, free\_inst => free\_xmit, free\_local => free\_inst.</span></span>

<span data-ttu-id="cbc3f-116">O \_ tamanho da memória de tipo apresentado \_ \_<2> sempre fornece um tamanho para o tipo apresentado/local, incluindo os tipos de representações desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-116">The presented\_type\_memory\_size<2> always provides a size for the presented/local type, including unknown represent as types.</span></span>

<span data-ttu-id="cbc3f-117">O tamanho do buffer de tipo transmitido \_ \_ \_<2> é zero, quando o tamanho é variável ou o tamanho fixo real.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-117">The transmitted\_type\_buffer\_size<2> is either zero, when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="cbc3f-118">Essa é uma otimização que permite ignorar alguns retornos de chamada ao dimensionar o buffer.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-118">This is an optimization that enables skipping some callbacks when sizing the buffer.</span></span>

<span data-ttu-id="cbc3f-119">O deslocamento do tipo transmitido \_ \_<2> é o deslocamento de tipo relativo usual para a cadeia de caracteres de formato do tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-119">The transmitted\_type\_offset<2> is the usual relative type offset to the transmitted type format string.</span></span>

 

 