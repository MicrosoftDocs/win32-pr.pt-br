---
description: LOCALE \_ INVARIANT
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: Locale_invariant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c3a4bddaaa51ca72be9d48f273ac0cbd1727e18e5c821e8ce86acaf0f90ec4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106576"
---
# <a name="locale_invariant"></a>LOCALE \_ INVARIANT

**Windows XP:** A localidade usada para funções no nível do sistema operacional que exigem resultados consistentes e independentes de localidade. Por exemplo, a localidade invariável é usada quando um aplicativo compara cadeias de caracteres usando a [**função CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e espera um resultado consistente, independentemente da localidade do usuário. As configurações da localidade invariável são semelhantes às do inglês (Estados Unidos), mas não devem ser usadas para exibir dados formatados. Normalmente, um aplicativo não usa LOCALE INVARIANT porque espera que os resultados de uma ação dependam das regras que regem \_ cada localidade individual. O valor de LOCALE \_ INVARIANT É 0x007f.

 

 
