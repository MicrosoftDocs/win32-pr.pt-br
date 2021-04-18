---
description: O Uniscribe usa vários mecanismos de shaping que contêm o conhecimento de layout para scripts específicos.
ms.assetid: 3cdd18f3-51d3-4d1c-be31-f5709074cbe7
title: Usando mecanismos de shaping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a106e993aba515af38edd2b809ef60454a186cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749600"
---
# <a name="using-shaping-engines"></a><span data-ttu-id="883e8-103">Usando mecanismos de shaping</span><span class="sxs-lookup"><span data-stu-id="883e8-103">Using Shaping Engines</span></span>

<span data-ttu-id="883e8-104">O Uniscribe usa vários mecanismos de shaping que contêm o conhecimento de layout para scripts específicos.</span><span class="sxs-lookup"><span data-stu-id="883e8-104">Uniscribe uses multiple shaping engines that contain the layout knowledge for particular scripts.</span></span> <span data-ttu-id="883e8-105">Ele também aproveita o mecanismo de modelagem de layout OpenType para manipular recursos de script específicos de fontes, como geração de glifos, medição de extensão e suporte à quebra de palavras.</span><span class="sxs-lookup"><span data-stu-id="883e8-105">It also takes advantage of the OpenType layout shaping engine for handling font-specific script features, such as glyph generation, extent measurement, and word-breaking support.</span></span> <span data-ttu-id="883e8-106">O Uniscribe gerencia a reordenação de caracteres bidirecionais usando o algoritmo bidirecional Unicode e entende formatos de fonte de layout não-OpenType para formatação árabe, Hebraico e tailandês.</span><span class="sxs-lookup"><span data-stu-id="883e8-106">Uniscribe manages bidirectional character reordering using the Unicode bidirectional algorithm, and understands non-OpenType layout font formats for Arabic, Hebrew, and Thai shaping.</span></span>

<span data-ttu-id="883e8-107">Como os intervalos de ponto de código exatos atribuídos a cada mecanismo de shaping podem variar, os números de script não são publicados, com exceção do SCRIPT \_ indefinido.</span><span class="sxs-lookup"><span data-stu-id="883e8-107">Since the exact code point ranges assigned to each shaping engine might vary, script numbers are not published, with the exception of SCRIPT\_UNDEFINED.</span></span> <span data-ttu-id="883e8-108">No entanto, seu aplicativo pode testar os atributos de scripts chamando a função [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) , que acessa a tabela global de propriedades de script.</span><span class="sxs-lookup"><span data-stu-id="883e8-108">However, your application can test the attributes of scripts by calling the [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) function, which accesses the global script properties table.</span></span> <span data-ttu-id="883e8-109">O aplicativo pode usar as propriedades de script global para ajudar a combinar suas próprias regras de layout com as divisões do mecanismo de shaping necessárias.</span><span class="sxs-lookup"><span data-stu-id="883e8-109">The application can use the global script properties to help combine its own layout rules with the required shaping engine divisions.</span></span>

<span data-ttu-id="883e8-110">O aplicativo acessa um mecanismo de shaping com uma chamada para a função [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) .</span><span class="sxs-lookup"><span data-stu-id="883e8-110">The application accesses a shaping engine with a call to the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) function.</span></span> <span data-ttu-id="883e8-111">Todos os mecanismos de modelagem de script complexos, os mecanismos de modelagem de dígitos e os mecanismos de formatação ASCII validam a fonte indicada no identificador de contexto do dispositivo antes do Shaping.</span><span class="sxs-lookup"><span data-stu-id="883e8-111">All the complex script shaping engines, the digit shaping engines, and the ASCII shaping engines validate the font indicated in the device context handle before shaping.</span></span> <span data-ttu-id="883e8-112">Scripts complexos devem ser moldados usando o script retornado pela função [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) para que você possa ser legível.</span><span class="sxs-lookup"><span data-stu-id="883e8-112">Complex scripts must be shaped using the script returned by the [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) function in order to be legible.</span></span> <span data-ttu-id="883e8-113">Outras execuções permanecerão legíveis se moldado com SCRIPT \_ especificado no membro **eScript** da estrutura [**de \_ análise de script**](/windows/win32/api/usp10/ns-usp10-script_analysis) , embora elas possam perder qualidade tipográfica.</span><span class="sxs-lookup"><span data-stu-id="883e8-113">Other runs remain legible if shaped with SCRIPT\_UNDEFINED specified in the **eScript** member of the [**SCRIPT\_ANALYSIS**](/windows/win32/api/usp10/ns-usp10-script_analysis) structure, although they might lose typographic quality.</span></span>

<span data-ttu-id="883e8-114">[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) retornará 0 se for bem-sucedido ou \_ \_ o script USP E não estará \_ \_ na \_ fonte se a fonte fornecida pelo aplicativo não contiver marcas de formatação ou glifos suficientes.</span><span class="sxs-lookup"><span data-stu-id="883e8-114">[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) returns 0 if successful, or USP\_E\_SCRIPT\_NOT\_IN\_FONT if the font supplied by the application does not contain sufficient glyphs or shaping tables.</span></span> <span data-ttu-id="883e8-115">Se o aplicativo especificar o SCRIPT \_ indefinido e alguns caracteres não forem suportados pela fonte, a função ainda terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="883e8-115">If the application specifies SCRIPT\_UNDEFINED and some characters are not supported by the font, the function still succeeds.</span></span> <span data-ttu-id="883e8-116">Nesse caso, o aplicativo deve verificar o buffer de saída de glifo para a presença de glifos ausentes.</span><span class="sxs-lookup"><span data-stu-id="883e8-116">In this case, the application should scan the glyph output buffer for the presence of missing glyphs.</span></span> <span data-ttu-id="883e8-117">Para obter estratégias para lidar com glifos ausentes, consulte [usando o fallback de fonte](using-font-fallback.md).</span><span class="sxs-lookup"><span data-stu-id="883e8-117">For strategies to deal with missing glyphs, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="883e8-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="883e8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="883e8-119">Usando o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="883e8-119">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



