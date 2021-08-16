---
description: Ao definir a propriedade Factoid como None, o reconhecedor de caracteres reconhece o manuscrito em uma base de caractere por caractere.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Reconhecimento de palavras versus caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e704943afb2b411441752056aace0889e87483fc4992d59c39ea6a135ef76b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966595"
---
# <a name="word-vs-character-recognition"></a>Reconhecimento de palavras versus caracteres

Ao definir a [propriedade Factoid](/previous-versions/ms835848(v=msdn.10)) como **Nenhum**, o reconhecedor de caracteres reconhece o manuscrito em uma base de caractere por caractere.

A [propriedade RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) na Automação) especifica o número de milissegundos de atraso entre o último [Traço](/previous-versions/ms552692(v=vs.100)) e o fim da entrada de manuscrito. Você pode aumentar esse valor para reconhecer texto antes que palavras inteiras ou frases sejam escritas. Você também pode forçar o reconhecimento de tinta imediatamente usando o [método Recognize.](/previous-versions/ms836275(v=msdn.10))

 

 
