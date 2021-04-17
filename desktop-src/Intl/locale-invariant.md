---
description: LOCALIDADE \_ invariável
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752269"
---
# <a name="locale_invariant"></a>LOCALIDADE \_ invariável

**Windows XP:** A localidade usada para funções de nível de sistema operacional que exigem resultados consistentes e independentes de localidade. Por exemplo, a localidade invariável é usada quando um aplicativo compara Cadeias de caracteres usando a função [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e espera um resultado consistente independentemente da localidade do usuário. As configurações da localidade invariável são semelhantes às do inglês (Estados Unidos), mas não devem ser usadas para exibir dados formatados. Normalmente, um aplicativo não usa a localidade \_ invariável porque espera que os resultados de uma ação dependam das regras que regem cada localidade individual. O valor de localidade \_ invariável é 0x007F.

 

 
