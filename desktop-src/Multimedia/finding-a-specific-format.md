---
title: Localizando um formato específico
description: Localizando um formato específico
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- Gerenciador de compactação de áudio (ACM), localizando formatos
- ACM (Gerenciador de compactação de áudio), localizando formatos
- Exemplos do ACM, localização de formatos
- Localizando formatos
- função acmFormatEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c148c075df09cb702caf6b1d192fe8ce41b48ad0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916539"
---
# <a name="finding-a-specific-format"></a>Localizando um formato específico

Um aplicativo pode ter apenas uma especificação parcial para um formato quando precisa da especificação completa. Por exemplo, a especificação pode estipular um formato de um mono de 4 bits, uma ADPCM, mas não a média de bytes por segundo. O aplicativo pode obter o formato completo sem intervenção do usuário usando a função [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) e especificando sinalizadores no parâmetro *fdwEnum* .

 

 




