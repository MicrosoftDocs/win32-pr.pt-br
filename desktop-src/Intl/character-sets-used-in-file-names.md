---
description: O NTFS armazena nomes de arquivo em Unicode. Por outro lado, os sistemas de arquivos FAT12, FAT16 e FAT32 mais antigos usam o conjunto de caracteres OEM. Para obter mais informações, consulte Páginas de Código.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Conjuntos de caracteres usados em nomes de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828882"
---
# <a name="character-sets-used-in-file-names"></a><span data-ttu-id="29fb4-105">Conjuntos de caracteres usados em nomes de arquivo</span><span class="sxs-lookup"><span data-stu-id="29fb4-105">Character Sets Used in File Names</span></span>

<span data-ttu-id="29fb4-106">O NTFS armazena nomes de arquivo em Unicode.</span><span class="sxs-lookup"><span data-stu-id="29fb4-106">NTFS stores file names in Unicode.</span></span> <span data-ttu-id="29fb4-107">Por outro lado, os sistemas de arquivos FAT12, FAT16 e FAT32 mais antigos usam o conjunto de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="29fb4-107">In contrast, the older FAT12, FAT16, and FAT32 file systems use the OEM character set.</span></span> <span data-ttu-id="29fb4-108">Para obter mais informações, consulte [Páginas de Código](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="29fb4-108">For more information, see [Code Pages](code-pages.md).</span></span>

<span data-ttu-id="29fb4-109">Os aplicativos não-Unicode que criam arquivos FAT às vezes precisam usar as funções de conversão padrão da biblioteca de tempo de execução C para converter entre o conjunto de caracteres da página de código do Windows e o conjunto de caracteres da página de código OEM.</span><span class="sxs-lookup"><span data-stu-id="29fb4-109">Non-Unicode applications that create FAT files sometimes have to use the standard C runtime library conversion functions to translate between the Windows code page character set and the OEM code page character set.</span></span> <span data-ttu-id="29fb4-110">Com as implementações Unicode das funções do sistema de arquivos, não é necessário executar tais conversões.</span><span class="sxs-lookup"><span data-stu-id="29fb4-110">With Unicode implementations of the file system functions, it is not necessary to perform such translations.</span></span>

<span data-ttu-id="29fb4-111">Seu aplicativo pode usar tipos de cadeia de caracteres genéricos, conforme descrito em [tipos de dados do Windows para cadeias de](windows-data-types-for-strings.md)caracteres.</span><span class="sxs-lookup"><span data-stu-id="29fb4-111">Your application can use generic string types, as described in [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span> <span data-ttu-id="29fb4-112">O aplicativo também pode usar protótipos de função genéricos usando técnicas descritas em [convenções para protótipos de função](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="29fb4-112">The application can also use generic function prototypes using techniques described in [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span> <span data-ttu-id="29fb4-113">Para tipos de cadeia de caracteres genéricos ou protótipos de funções genéricas, seu aplicativo pode usar um único arquivo de origem para compilar uma versão Unicode ou não-Unicode.</span><span class="sxs-lookup"><span data-stu-id="29fb4-113">For either generic string types or generic function prototypes, your application can use a single source file to compile either a Unicode or a non-Unicode version.</span></span> <span data-ttu-id="29fb4-114">Para permitir isso, o aplicativo fornece macros para funções que não são invocadas durante a compilação para Unicode.</span><span class="sxs-lookup"><span data-stu-id="29fb4-114">To allow for this, the application provides macros for functions that are not invoked when compiling for Unicode.</span></span>

<span data-ttu-id="29fb4-115">Nos sistemas de arquivos NTFS e Fat, os caracteres de nome de arquivo especiais são: ' \\ ', '/', '. ', '? ' e ' \* '.</span><span class="sxs-lookup"><span data-stu-id="29fb4-115">In both NTFS and FAT file systems, the special file name characters are: '\\', '/', '.', '?', and '\*'.</span></span> <span data-ttu-id="29fb4-116">Em páginas de código OEM, esses caracteres especiais estão no intervalo ASCII de caracteres (0x00 a 0x7F).</span><span class="sxs-lookup"><span data-stu-id="29fb4-116">On OEM code pages, these special characters are in the ASCII range of characters (0x00 through 0x7F).</span></span> <span data-ttu-id="29fb4-117">Seus equivalentes Unicode são os mesmos valores em um formato de 2 bytes, 0x0000 por meio de 0x007F.</span><span class="sxs-lookup"><span data-stu-id="29fb4-117">Their Unicode equivalents are the same values in a 2-byte form, 0x0000 through 0x007F.</span></span>

> [!Caution]  
> <span data-ttu-id="29fb4-118">A página de código do Windows e os conjuntos de caracteres de página de código OEM usados em sistemas operacionais de idioma japonês contêm o símbolo de Iene (¥) em vez de uma barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="29fb4-118">Windows code page and OEM code page character sets used on Japanese-language operating systems contain the Yen symbol (¥) instead of a backslash (\\).</span></span> <span data-ttu-id="29fb4-119">Portanto, o símbolo de Iene é um caractere proibido para sistemas de arquivos NTFS e FAT.</span><span class="sxs-lookup"><span data-stu-id="29fb4-119">Thus, the Yen symbol is a prohibited character for NTFS and FAT file systems.</span></span> <span data-ttu-id="29fb4-120">Ao mapear o Unicode para uma página de código de idioma japonês, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e outras funções de conversão mapeiam ambas as barras invertidas (u + 005C) e o símbolo de iene Unicode normal (U + 00A5) para esse mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="29fb4-120">When mapping Unicode to a Japanese-language code page, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and other conversion functions map both backslash (U+005C) and the normal Unicode Yen symbol (U+00A5) to this same character.</span></span> <span data-ttu-id="29fb4-121">Por motivos de segurança, os aplicativos normalmente não devem permitir o caractere U + 00A5 em uma cadeia de caracteres Unicode que pode ser convertida para uso como um nome de arquivo FAT.</span><span class="sxs-lookup"><span data-stu-id="29fb4-121">For security reasons, your applications should not typically allow the character U+00A5 in a Unicode string that might be converted for use as a FAT file name.</span></span> <span data-ttu-id="29fb4-122">Para obter mais informações, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="29fb4-122">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="29fb4-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29fb4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29fb4-124">Unicode na API do Windows</span><span class="sxs-lookup"><span data-stu-id="29fb4-124">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> <dt>

[<span data-ttu-id="29fb4-125">Considerações sobre segurança: recursos internacionais</span><span class="sxs-lookup"><span data-stu-id="29fb4-125">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> </dl>

 

 



