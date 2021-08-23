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
ms.openlocfilehash: ecc291a6dff0c6b2befec6afd001a32735a54e95fd65a464378adb690a95019c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691526"
---
# <a name="finding-a-specific-format"></a>Localizando um formato específico

Um aplicativo pode ter apenas uma especificação parcial para um formato quando precisa da especificação completa. Por exemplo, a especificação pode estipular um formato de um mono de 4 bits, uma ADPCM, mas não a média de bytes por segundo. O aplicativo pode obter o formato completo sem intervenção do usuário usando a função [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) e especificando sinalizadores no parâmetro *fdwEnum* .

 

 




