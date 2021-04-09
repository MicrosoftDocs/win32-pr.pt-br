---
title: Enumerando partições de diretório de aplicativo em uma floresta
description: Assim como as partições de domínio, cada partição de diretório de aplicativo é representada por um objeto crossRef no contêiner de partições da partição de configuração.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Enumerando partições de diretório de aplicativo em um AD de floresta
- ANÚNCIO de partições de diretório de aplicativo, enumerando em uma floresta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d42bbe28ef37932394721d0c234ba3970ac263b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007319"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Enumerando partições de diretório de aplicativo em uma floresta

Assim como as partições de domínio, cada partição de diretório de aplicativo é representada por um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) no contêiner de partições da partição de configuração. Cada objeto **crossRef** armazena dados sobre sua partição correspondente.

Um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa uma partição de domínio é diferenciado de um objeto **crossRef** que representa uma partição de diretório de aplicativos pelo conteúdo do atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . O objeto **crossRef** que representa uma partição de domínio terá os sinalizadores de domínio [**ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) e **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_** definidos no atributo **systemFlags** . O objeto **crossRef** que representa uma partição de diretório de aplicativos terá o sinalizador de **anúncios \_ SYSTEMFLAG \_ CR \_ NTDS \_ NC** definido e o sinalizador de **domínio de NTDS do ADS \_ SYSTEMFLAG \_ CR \_ \_** não será definido no atributo **systemFlags** .

Os objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representam o esquema e as partições de configuração também terão o sinalizador do [**ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) , definido e o sinalizador de **domínio de NTDS do AD \_ SYSTEMFLAG \_ CR \_ \_** não será definido no atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . Isso exige que esses dois objetos **crossRef** sejam diferenciados pelo conteúdo do atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) . O atributo **NCName** para o objeto **crossRef** que representa o contêiner de esquema será idêntico ao atributo **schemaNamingContext** do objeto rootDSE. Da mesma forma, o atributo **NCName** para o objeto **crossRef** que representa o contêiner de configuração será idêntico ao atributo **configurationNamingContext** do objeto rootDSE.

**Para identificar todas as partições de diretório de aplicativo em uma floresta, execute as seguintes etapas**

1.  No contêiner partições da partição de configuração, pesquise ou Enumere todos os objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) .
2.  Se um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) não tiver o sinalizador [**ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) definido ou tiver o sinalizador **de \_ domínio ADS SYSTEMFLAG \_ CR \_ NTDS \_** definido no valor do atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , exclua o objeto do conjunto de resultados.
3.  Exclua a partição de esquema do conjunto de resultados comparando o atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) com o atributo **schemaNamingContext** do objeto rootDSE.
4.  Exclua a partição de configuração do conjunto de resultados comparando o atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) com o atributo **configurationNamingContext** do objeto rootDSE.
5.  Os objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) restantes no conjunto de resultados representam todas as partições de diretório de aplicativo.

 

 