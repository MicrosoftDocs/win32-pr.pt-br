---
description: Ao definir a propriedade Factoname como None, o reconhecedor de caracteres reconhece o manuscrito em uma base de caractere por caractere.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Reconhecimento de palavra versus caractere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f521b8abf1064ef87c5c79c3293e725c44190ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090291"
---
# <a name="word-vs-character-recognition"></a><span data-ttu-id="ac240-103">Reconhecimento de palavra versus caractere</span><span class="sxs-lookup"><span data-stu-id="ac240-103">Word vs. Character Recognition</span></span>

<span data-ttu-id="ac240-104">Ao definir a propriedade [factoname](/previous-versions/ms835848(v=msdn.10)) como **None**, o reconhecedor de caracteres reconhece o manuscrito em uma base de caractere por caractere.</span><span class="sxs-lookup"><span data-stu-id="ac240-104">By setting the [Factoid](/previous-versions/ms835848(v=msdn.10)) property to **None**, the character recognizer recognizes handwriting on a character-by-character basis.</span></span>

<span data-ttu-id="ac240-105">A propriedade [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) na automação) especifica o número de milissegundos de atraso entre o último [traço](/previous-versions/ms552692(v=vs.100)) e o fim da entrada de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="ac240-105">The [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) property specifies the number of milliseconds of delay between the last [Stroke](/previous-versions/ms552692(v=vs.100)) and the end of handwriting input.</span></span> <span data-ttu-id="ac240-106">Você pode aumentar esse valor para reconhecer o texto antes que palavras inteiras ou frases sejam gravadas.</span><span class="sxs-lookup"><span data-stu-id="ac240-106">You can increase this value to recognize text before entire words or sentences are written.</span></span> <span data-ttu-id="ac240-107">Você também pode forçar o reconhecimento de tinta imediatamente usando o método [Recognize](/previous-versions/ms836275(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ac240-107">You can also force the recognition of ink immediately by using the [Recognize](/previous-versions/ms836275(v=msdn.10)) method.</span></span>

 

 
