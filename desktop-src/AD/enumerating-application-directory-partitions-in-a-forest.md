---
title: Enumerando partições de diretório do aplicativo em uma floresta
description: Assim como as partições de domínio, cada partição de diretório de aplicativo é representada por um objeto crossRef no contêiner Partições da partição de configuração.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Enumerando partições de diretório do aplicativo em um AD de floresta
- AD de partições do diretório de aplicativos, enumerando em uma floresta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e8d48b2fc93ad7a879f76f2bbaa130186706ef957320612c866cb3b9f892c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191363"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Enumerando partições de diretório do aplicativo em uma floresta

Assim como as partições de domínio, cada partição de diretório de aplicativo é representada por um [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) no contêiner Partições da partição de configuração. Cada **objeto crossRef** armazena dados sobre sua partição correspondente.

Um [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) que representa uma partição de domínio é diferenciado de um objeto **crossRef** que representa uma partição de diretório do aplicativo pelo conteúdo do [**atributo systemFlags.**](/windows/desktop/ADSchema/a-systemflags) O **objeto crossRef** que representa uma partição de domínio terá os sinalizadores DE DOMÍNIO NC e ADS [**\_ SYSTEMFLAG \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) e **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_** definidos no atributo **systemFlags.** O **objeto crossRef** que representa uma partição de diretório de aplicativo terá o sinalizador **NC ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_** definido e o sinalizador DE DOMÍNIO **\_ \_ \_ NTDS \_ DO ADS SYSTEMFLAG CR** não será definido no atributo **systemFlags.**

Os [**objetos crossRef**](/windows/desktop/ADSchema/c-crossref) que representam as partições de Esquema e Configuração também terão o sinalizador [**NC \_ SYSTEMFLAG CR NTDS definido e o sinalizador DE DOMÍNIO \_ \_ \_ NTDS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) DO ADS **\_ SYSTEMFLAG \_ CR \_ \_** não será definido no atributo [**systemFlags.**](/windows/desktop/ADSchema/a-systemflags) Isso exige que esses dois **objetos crossRef** sejam diferenciados pelo conteúdo do [**atributo nCName.**](/windows/desktop/ADSchema/a-ncname) O **atributo nCName** para o objeto **crossRef** que representa o contêiner schema será idêntico ao atributo **schemaNamingContext** do objeto RootDSE. Da mesma forma, o atributo **nCName** para o objeto **crossRef** que representa o contêiner Configuration será idêntico ao atributo **configurationNamingContext** do objeto RootDSE.

**Para identificar todas as partições de diretório do aplicativo em uma floresta, execute as etapas a seguir**

1.  No contêiner Partições da partição de configuração, pesquise ou enumere todos os [**objetos crossRef.**](/windows/desktop/ADSchema/c-crossref)
2.  Se um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) não tiver o sinalizador [**NC ADS \_ SYSTEMFLAG \_ CR \_ \_ NTDS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) definido ou tiver o sinalizador DE DOMÍNIO **\_ SYSTEMFLAG \_ CR \_ NTDS \_** do ADS definido no valor do atributo [**systemFlags,**](/windows/desktop/ADSchema/a-systemflags) exclua o objeto do conjunto de resultados.
3.  Exclua a partição Schema do conjunto de resultados comparando o atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) com o atributo **schemaNamingContext** do objeto RootDSE.
4.  Exclua a partição Configuration do conjunto de resultados comparando o atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) com o atributo **configurationNamingContext** do objeto RootDSE.
5.  Os objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) restantes no conjunto de resultados representam partições de diretório do aplicativo.

 

 