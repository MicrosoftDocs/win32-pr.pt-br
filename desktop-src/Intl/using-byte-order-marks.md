---
description: Sempre Prefixe um arquivo de texto sem formatação Unicode com uma marca de ordem de byte, que informa a um aplicativo que está recebendo o arquivo que o arquivo é ordenado por byte.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Usando marcas de ordem de byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747354"
---
# <a name="using-byte-order-marks"></a><span data-ttu-id="5e646-103">Usando marcas de ordem de byte</span><span class="sxs-lookup"><span data-stu-id="5e646-103">Using Byte Order Marks</span></span>

<span data-ttu-id="5e646-104">Sempre Prefixe um arquivo de texto sem formatação Unicode com uma marca de ordem de byte, que informa a um aplicativo que está recebendo o arquivo que o arquivo é ordenado por byte.</span><span class="sxs-lookup"><span data-stu-id="5e646-104">Always prefix a Unicode plain text file with a byte order mark, which informs an application receiving the file that the file is byte-ordered.</span></span> <span data-ttu-id="5e646-105">As marcas de ordem de byte disponíveis são listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e646-105">Available byte order marks are listed in the following table.</span></span> <span data-ttu-id="5e646-106">Como o texto sem formatação Unicode é uma sequência de valores de código de 16 bits, ele é sensível à ordenação de bytes usada quando o texto é gravado.</span><span class="sxs-lookup"><span data-stu-id="5e646-106">Because Unicode plain text is a sequence of 16-bit code values, it is sensitive to the byte ordering used when the text is written.</span></span>

> [!Note]  
> <span data-ttu-id="5e646-107">Uma marca de ordem de byte não é um caractere de controle que seleciona a ordem de bytes do texto.</span><span class="sxs-lookup"><span data-stu-id="5e646-107">A byte order mark is not a control character that selects the byte order of the text.</span></span>

 



| <span data-ttu-id="5e646-108">Marca de ordem de byte</span><span class="sxs-lookup"><span data-stu-id="5e646-108">Byte order mark</span></span> | <span data-ttu-id="5e646-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e646-109">Description</span></span>           |
|-----------------|-----------------------|
| <span data-ttu-id="5e646-110">EF BB BF</span><span class="sxs-lookup"><span data-stu-id="5e646-110">EF BB BF</span></span>        | <span data-ttu-id="5e646-111">UTF-8</span><span class="sxs-lookup"><span data-stu-id="5e646-111">UTF-8</span></span>                 |
| <span data-ttu-id="5e646-112">FF FE</span><span class="sxs-lookup"><span data-stu-id="5e646-112">FF FE</span></span>           | <span data-ttu-id="5e646-113">UTF-16, little endian</span><span class="sxs-lookup"><span data-stu-id="5e646-113">UTF-16, little endian</span></span> |
| <span data-ttu-id="5e646-114">FF DE FE</span><span class="sxs-lookup"><span data-stu-id="5e646-114">FE FF</span></span>           | <span data-ttu-id="5e646-115">UTF-16, big endian</span><span class="sxs-lookup"><span data-stu-id="5e646-115">UTF-16, big endian</span></span>    |
| <span data-ttu-id="5e646-116">FF FE 00 00</span><span class="sxs-lookup"><span data-stu-id="5e646-116">FF FE 00 00</span></span>     | <span data-ttu-id="5e646-117">UTF-32, little endian</span><span class="sxs-lookup"><span data-stu-id="5e646-117">UTF-32, little endian</span></span> |
| <span data-ttu-id="5e646-118">00 00 FE FF</span><span class="sxs-lookup"><span data-stu-id="5e646-118">00 00 FE FF</span></span>     | <span data-ttu-id="5e646-119">UTF-32, big-endian</span><span class="sxs-lookup"><span data-stu-id="5e646-119">UTF-32, big-endian</span></span>    |



 

> [!Note]  
> <span data-ttu-id="5e646-120">A Microsoft usa a ordem UTF-16, little endian byte.</span><span class="sxs-lookup"><span data-stu-id="5e646-120">Microsoft uses UTF-16, little endian byte order.</span></span>

 

<span data-ttu-id="5e646-121">O ideal é que todo o texto Unicode Siga apenas um conjunto de regras de ordenação de bytes.</span><span class="sxs-lookup"><span data-stu-id="5e646-121">Ideally, all Unicode text follows only one set of byte ordering rules.</span></span> <span data-ttu-id="5e646-122">No entanto, isso não é possível porque os microprocessadores diferem no posicionamento do byte menos significativo.</span><span class="sxs-lookup"><span data-stu-id="5e646-122">This is not possible, however, because microprocessors differ in the placement of the least significant byte.</span></span> <span data-ttu-id="5e646-123">Os processadores Intel e MIPS posicionam o byte menos significativo primeiro, enquanto os processadores Motorola (e todos os arquivos Unicode invertidos em bytes) o posicionam por último.</span><span class="sxs-lookup"><span data-stu-id="5e646-123">Intel and MIPS processors position the least significant byte first, whereas Motorola processors (and all byte-reversed Unicode files) position it last.</span></span> <span data-ttu-id="5e646-124">Com apenas um conjunto único de regras de ordenação de bytes, os usuários de um tipo de microprocessador são forçados a trocar a ordem de bytes sempre que um arquivo de texto sem formatação é lido ou gravado, mesmo que o arquivo nunca seja transferido para outro sistema operacional com base em um microprocessador diferente.</span><span class="sxs-lookup"><span data-stu-id="5e646-124">With only a single set of byte ordering rules, users of one type of microprocessor are forced to swap the byte order every time a plain text file is read from or written to, even if the file is never transferred to another operating system based on a different microprocessor.</span></span>

<span data-ttu-id="5e646-125">O local preferencial para especificar a ordem de byte está em um cabeçalho de arquivo, mas os arquivos de texto não têm cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="5e646-125">The preferred place to specify byte order is in a file header, but text files do not have headers.</span></span> <span data-ttu-id="5e646-126">Portanto, o Unicode definiu um caractere (U + FEFF) e um não caractere (U + FFFE) como marcas de ordem de byte.</span><span class="sxs-lookup"><span data-stu-id="5e646-126">Therefore, Unicode has defined a character (U+FEFF) and a noncharacter (U+FFFE) as byte order marks.</span></span> <span data-ttu-id="5e646-127">Elas são imagens de byte espelhadas uma da outra.</span><span class="sxs-lookup"><span data-stu-id="5e646-127">They are mirror byte images of each other.</span></span>

<span data-ttu-id="5e646-128">Como a sequência U + FEFF é extremamente rara no início de um arquivo de texto não-Unicode regular, ele pode servir como um marcador ou assinatura implícita para identificar o arquivo como um arquivo Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e646-128">Since the sequence U+FEFF is exceedingly rare at the beginning of a regular non-Unicode text file, it can serve as an implicit marker or signature to identify the file as a Unicode file.</span></span> <span data-ttu-id="5e646-129">Os aplicativos que lêem arquivos de texto Unicode e não Unicode devem usar a presença dessa sequência como um indicador de que o arquivo provavelmente é um arquivo Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e646-129">Applications that read both Unicode and non-Unicode text files should use the presence of this sequence as an indicator that the file is most likely a Unicode file.</span></span> <span data-ttu-id="5e646-130">Compare essa técnica com o uso do marcador EOF do MS-DOS para encerrar arquivos de texto.</span><span class="sxs-lookup"><span data-stu-id="5e646-130">Compare this technique to using the MS-DOS EOF marker to terminate text files.</span></span>

<span data-ttu-id="5e646-131">Quando um aplicativo encontra U + FEFF no início de um arquivo de texto, ele normalmente processa o arquivo como um arquivo Unicode, embora possa executar verificações de heurística adicionais para verificação.</span><span class="sxs-lookup"><span data-stu-id="5e646-131">When an application finds U+FEFF at the beginning of a text file, it typically processes the file as a Unicode file, although it can perform further heuristic checks for verification.</span></span> <span data-ttu-id="5e646-132">Essa verificação pode ser tão simples quanto o teste para descobrir se a variação nos bytes de ordem inferior é muito maior do que a variação nos bytes de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="5e646-132">Such a check can be as simple as testing to find out if the variation in the low-order bytes is much higher than the variation in the high-order bytes.</span></span> <span data-ttu-id="5e646-133">Por exemplo, se o texto ASCII for convertido em texto Unicode, cada segundo byte será 0.</span><span class="sxs-lookup"><span data-stu-id="5e646-133">For example, if ASCII text is converted to Unicode text, every second byte is 0.</span></span> <span data-ttu-id="5e646-134">Além disso, a verificação dos caracteres de alimentação e de retorno de carro (U + 000A e U + 000D) e de tamanho de arquivo par ou ímpar pode fornecer um indicador forte da natureza do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e646-134">Also, checking both for the linefeed and carriage return characters (U+000A and U+000D) and for even or odd file size can provide a strong indicator of the nature of the file.</span></span>

<span data-ttu-id="5e646-135">Quando um aplicativo encontra U + FFFE no início de um arquivo de texto, ele o interpreta para significar que o arquivo é um arquivo Unicode invertido em bytes.</span><span class="sxs-lookup"><span data-stu-id="5e646-135">When an application finds U+FFFE at the beginning of a text file, it interprets it to mean that the file is a byte-reversed Unicode file.</span></span> <span data-ttu-id="5e646-136">O aplicativo pode trocar a ordem dos bytes ou alertar o usuário de que ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="5e646-136">The application can either swap the order of the bytes or alert the user that an error has occurred.</span></span>

<span data-ttu-id="5e646-137">Como o caractere de marca de ordem de byte Unicode não é encontrado em nenhuma página de código, ele desaparece se os dados são convertidos em ANSI.</span><span class="sxs-lookup"><span data-stu-id="5e646-137">Since the Unicode byte order mark character is not found in any code page, it disappears if data is converted to ANSI.</span></span> <span data-ttu-id="5e646-138">Ao contrário de outros caracteres Unicode, ele não é substituído por um caractere padrão quando é convertido.</span><span class="sxs-lookup"><span data-stu-id="5e646-138">Unlike other Unicode characters, it is not replaced by a default character when it is converted.</span></span> <span data-ttu-id="5e646-139">Se uma marca de ordem de byte for encontrada no meio de um arquivo, ela não será interpretada como um caractere Unicode e não terá nenhum efeito na saída de texto.</span><span class="sxs-lookup"><span data-stu-id="5e646-139">If a byte order mark is found in the middle of a file, it is not interpreted as a Unicode character and has no effect on text output.</span></span>

> [!Note]  
> <span data-ttu-id="5e646-140">O valor Unicode U + FFFF é inválido em arquivos de texto sem formatação e não pode ser passado entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5e646-140">The Unicode value U+FFFF is illegal in plain text files and cannot be passed between applications.</span></span> <span data-ttu-id="5e646-141">Ele é reservado para o uso particular de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e646-141">It is reserved for the private use of an application.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5e646-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e646-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e646-143">Usando caracteres especiais em Unicode</span><span class="sxs-lookup"><span data-stu-id="5e646-143">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



