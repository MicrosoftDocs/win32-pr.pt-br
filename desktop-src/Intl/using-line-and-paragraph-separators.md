---
description: Seus aplicativos devem usar o caractere separador de linha (0x2028) e o caractere separador de parágrafo (0x2029) para dividir o texto sem formatação. Uma nova linha é iniciada após cada separador de linha. Um novo parágrafo é iniciado após cada separador de parágrafo.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Usando separadores de linha e parágrafo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172178"
---
# <a name="using-line-and-paragraph-separators"></a><span data-ttu-id="69a1e-105">Usando separadores de linha e parágrafo</span><span class="sxs-lookup"><span data-stu-id="69a1e-105">Using Line and Paragraph Separators</span></span>

<span data-ttu-id="69a1e-106">Seus aplicativos devem usar o caractere separador de linha (0x2028) e o caractere separador de parágrafo (0x2029) para dividir o texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="69a1e-106">Your applications should use the line separator character (0x2028) and the paragraph separator character (0x2029) to divide plain text.</span></span> <span data-ttu-id="69a1e-107">Uma nova linha é iniciada após cada separador de linha.</span><span class="sxs-lookup"><span data-stu-id="69a1e-107">A new line is begun after each line separator.</span></span> <span data-ttu-id="69a1e-108">Um novo parágrafo é iniciado após cada separador de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="69a1e-108">A new paragraph is begun after each paragraph separator.</span></span>

<span data-ttu-id="69a1e-109">Não é necessário iniciar a primeira linha ou parágrafo em um arquivo com esses caracteres, ou para terminar a última linha ou parágrafo com eles.</span><span class="sxs-lookup"><span data-stu-id="69a1e-109">It is not necessary to start the first line or paragraph in a file with these characters, or to end the last line or paragraph with them.</span></span> <span data-ttu-id="69a1e-110">Isso indica que há uma linha ou parágrafo vazio nesse local.</span><span class="sxs-lookup"><span data-stu-id="69a1e-110">Doing so indicates that there is an empty line or paragraph in that location.</span></span>

<span data-ttu-id="69a1e-111">O aplicativo pode usar o separador de linha para indicar um fim de linha incondicional.</span><span class="sxs-lookup"><span data-stu-id="69a1e-111">The application can use the line separator to indicate an unconditional end of line.</span></span> <span data-ttu-id="69a1e-112">No entanto, separadores de linha não correspondem ao retorno de carro separado e caracteres de avanço de linha nem a uma combinação desses caracteres.</span><span class="sxs-lookup"><span data-stu-id="69a1e-112">However, line separators do not correspond to the separate carriage return and linefeed characters, or to a combination of these characters.</span></span> <span data-ttu-id="69a1e-113">Os separadores de linha devem ser processados separadamente de caracteres de avanço de linha e de retorno do carro.</span><span class="sxs-lookup"><span data-stu-id="69a1e-113">Line separators must be processed separately from carriage return and linefeed characters.</span></span>

<span data-ttu-id="69a1e-114">O aplicativo pode inserir um separador de parágrafo entre parágrafos de texto.</span><span class="sxs-lookup"><span data-stu-id="69a1e-114">The application can insert a paragraph separator between paragraphs of text.</span></span> <span data-ttu-id="69a1e-115">O uso desse separador permite a criação de arquivos de texto sem formatação que podem ser formatados com larguras de linha diferentes em sistemas operacionais diversos.</span><span class="sxs-lookup"><span data-stu-id="69a1e-115">Use of this separator allows creation of plain text files that can be formatted with different line widths on different operating systems.</span></span> <span data-ttu-id="69a1e-116">O sistema de destino pode ignorar todos os separadores de linha e interromper parágrafos apenas nos separadores de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="69a1e-116">The target system can ignore any line separators and break paragraphs only at the paragraph separators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69a1e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69a1e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69a1e-118">Usando caracteres especiais em Unicode</span><span class="sxs-lookup"><span data-stu-id="69a1e-118">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



