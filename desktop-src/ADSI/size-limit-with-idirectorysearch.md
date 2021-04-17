---
title: Limite de tamanho com IDirectorySearch
description: O cliente pode se concentrar em um pequeno número de objetos retornados do servidor e ignorar o restante do conjunto de resultados.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Limite de tamanho com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, limite de tamanho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748293"
---
# <a name="size-limit-with-idirectorysearch"></a>Limite de tamanho com IDirectorySearch

Para reduzir o requisito de memória ou para outras finalidades, o cliente pode se concentrar em um pequeno número de objetos retornados do servidor e ignorar o restante do conjunto de resultados que não são de interesse. Para fazer isso, o cliente especifica o limite de tamanho de pesquisa e outros critérios de pesquisa apropriados. Por exemplo, se o diretório armazena as pontuações de teste de um distrito escolar, você pode consultar os dez principais alunos com as pontuações de teste mais altas especificando um limite de tamanho de dez (10) e uma ordem de classificação decrescente.

O limite de tamanho padrão é sem limite. Para definir um limite de tamanho, defina uma opção de pesquisa de **\_ limite de \_ tamanho \_ do ADS SEARCHPREF** com um valor **\_ inteiro de ADSTYPE** que contenha o tamanho máximo na matriz de [**informações de \_ SEARCHPREF \_ de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

O exemplo de código a seguir mostra como definir o limite de tamanho. Um valor de limite de tamanho igual A zero indica que não há limite de tamanho.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Por Active Directory, o limite de tamanho especifica o número máximo de objetos a serem retornados pela pesquisa. Além disso, para Active Directory, o número máximo de objetos retornados por uma pesquisa é de 1000 objetos.

 

 




