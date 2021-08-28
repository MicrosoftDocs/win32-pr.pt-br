---
description: LOCALIDADE \_ S1159 e Sam de localidade \_
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 e LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690132c0eb56dc75dd34eae217a6fa7598256852ef4e7039cc988754f7a589f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106336"
---
# <a name="locale_s1159-and-locale_sam"></a>LOCALIDADE \_ S1159 e Sam de localidade \_

Cadeia de caracteres do designador AM (primeiras 12 horas do dia). O número máximo de caracteres permitido para essa cadeia de caracteres, incluindo um caractere nulo de terminação, é diferente para diferentes versões do Windows.

**Windows XP:** Treze incluindo um caractere nulo de terminação para [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Quinze incluindo um caractere nulo de terminação para [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, Windows 2000:** Nove incluindo um caractere nulo de terminação.

**Windows Server 2003 e posterior:** Quinze incluindo um caractere nulo de terminação.

Windows 10 adicionou a localidade de valor **\_ SAM** como um sinônimo mais legível para a **localidade \_ S1159**.

 

 



