---
description: A edição avançada 3,0 dá suporte ao IME HexToUnicode, que permite que um usuário converta entre caracteres hexadecimais e Unicode usando teclas de acesso em uma de duas maneiras.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506281"
---
# <a name="hextounicode-ime"></a><span data-ttu-id="c4e66-103">HexToUnicode IME</span><span class="sxs-lookup"><span data-stu-id="c4e66-103">HexToUnicode IME</span></span>

<span data-ttu-id="c4e66-104">A edição avançada 3,0 dá suporte ao IME HexToUnicode, que permite que um usuário converta entre caracteres hexadecimais e Unicode usando teclas de acesso em uma de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="c4e66-104">Rich Edit 3.0 supports the HexToUnicode IME, which allows a user to convert between hexadecimal and Unicode characters by using hot keys in one of two ways.</span></span>

<span data-ttu-id="c4e66-105">Usando o primeiro método de conversão, o usuário digita o código de caractere em hexadecimal e, em seguida, insere ALT + X.</span><span class="sxs-lookup"><span data-stu-id="c4e66-105">Using the first conversion method, the user types the character code in hexadecimal and then enters ALT+X.</span></span> <span data-ttu-id="c4e66-106">O IME substitui os dígitos hexadecimais que antecedem o ponto de inserção com o caractere Unicode.</span><span class="sxs-lookup"><span data-stu-id="c4e66-106">The IME replaces the hexadecimal digits preceding the insertion point with the Unicode character.</span></span> <span data-ttu-id="c4e66-107">Se a fonte atual não oferecer suporte ao código de caractere, será escolhida uma fonte apropriada que ofereça suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="c4e66-107">If the current font does not support the character code, an appropriate font is chosen that does support it.</span></span> <span data-ttu-id="c4e66-108">Para converter de Unicode em hexadecimal, o usuário insere SHIFT + ALT + X.</span><span class="sxs-lookup"><span data-stu-id="c4e66-108">To convert from Unicode to hexadecimal, the user enters SHIFT+ALT+X.</span></span> <span data-ttu-id="c4e66-109">Essa entrada substitui o caractere Unicode que precede o ponto de inserção com os dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="c4e66-109">This entry replaces the Unicode character that precedes the insertion point with the hexadecimal digits.</span></span> <span data-ttu-id="c4e66-110">Em particular, esse método permite que o usuário determine o caractere indicado por um indicador de "glifo ausente".</span><span class="sxs-lookup"><span data-stu-id="c4e66-110">In particular, this method allows the user to determine the character that is indicated by a "missing glyph" indicator.</span></span> <span data-ttu-id="c4e66-111">Se o código de caractere hexadecimal seguir imediatamente alguns caracteres hexadecimais (não caracteres) legítimos, o usuário selecionará os dígitos específicos a serem convertidos antes de digitar ALT + X.</span><span class="sxs-lookup"><span data-stu-id="c4e66-111">If the hexadecimal character code immediately follows some legitimate (noncharacter) hexadecimal characters, the user selects the specific digits to convert before typing ALT+X.</span></span> <span data-ttu-id="c4e66-112">Um problema com esse primeiro método é que ALT + X às vezes é usado como uma combinação de teclas para o comando exit (ou seja, eXit).</span><span class="sxs-lookup"><span data-stu-id="c4e66-112">A problem with this first method is that ALT+X is sometimes used as a key combination for the exit command (that is, eXit).</span></span> <span data-ttu-id="c4e66-113">Por exemplo, em Microsoft Office, esse comando só aparece como uma opção do menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="c4e66-113">For example, in Microsoft Office, this command only appears as an option of the **File** menu.</span></span>

<span data-ttu-id="c4e66-114">O segundo método de conversão entre caracteres hexadecimais e Unicode envolve o teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="c4e66-114">The second method of converting between hexadecimal and Unicode characters involves the number pad.</span></span> <span data-ttu-id="c4e66-115">Usando esse método, o usuário digita ALT + números de teclado numérico (com valores maiores que 255) para inserir caracteres Unicode usando valores decimais.</span><span class="sxs-lookup"><span data-stu-id="c4e66-115">Using this method, the user types ALT+NumPad numbers (with values greater than 255) to enter Unicode characters using decimal values.</span></span> <span data-ttu-id="c4e66-116">Esse método não é tão útil quanto o primeiro porque o usuário não pode ver quais dígitos hexadecimais foram digitados.</span><span class="sxs-lookup"><span data-stu-id="c4e66-116">This method is not as useful as the first because the user cannot see what hexadecimal digits have been typed.</span></span> <span data-ttu-id="c4e66-117">Além disso, o usuário não pode corrigir os dígitos hexadecimais, exceto inserindo novamente todos os dígitos.</span><span class="sxs-lookup"><span data-stu-id="c4e66-117">Also, the user cannot correct the hexadecimal digits except by re-entering all the digits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4e66-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4e66-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4e66-119">Sobre o Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="c4e66-119">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 



