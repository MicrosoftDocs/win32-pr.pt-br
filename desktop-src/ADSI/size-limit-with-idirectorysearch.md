---
title: Limite de tamanho com IDirectorySearch
description: O cliente pode se concentrar em um pequeno número de objetos retornados do servidor e ignorar o restante do conjunto de resultados.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Limite de tamanho com ADSI IDirectorySearch
- ADSI, Search, IDirectorySearch, outras opções de pesquisa, limite de tamanho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6ee4e23cb3014ea92e8510da88767a433b76c0fe73ccbe74bac6ba0bfc1c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178741"
---
# <a name="size-limit-with-idirectorysearch"></a>Limite de tamanho com IDirectorySearch

Para reduzir o requisito de memória ou para outras finalidades, o cliente pode se concentrar em um pequeno número de objetos retornados do servidor e ignorar o restante do conjunto de resultados que não são de interesse. Para fazer isso, o cliente especifica o limite de tamanho da pesquisa e outros critérios de pesquisa apropriados. Por exemplo, se o diretório armazenar as pontuações de teste de um distrito escolar, você poderá consultar os dez principais alunos com as pontuações de teste mais altas especificando um limite de tamanho de dez (10) e uma ordem de classificação decrescente.

O padrão para o limite de tamanho não é nenhum limite. Para definir um limite de tamanho, de definir uma opção de pesquisa **ADS \_ SEARCHPREF \_ SIZE \_ LIMIT** com um valor **INTEIRO \_ ADSTYPE** que contém o tamanho máximo na matriz [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o [**método IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

O exemplo de código a seguir mostra como definir o limite de tamanho. Um valor limite de tamanho de zero não indica nenhum limite de tamanho.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Para o Active Directory, o limite de tamanho especifica o número máximo de objetos a serem retornados pela pesquisa. Além disso, para o Active Directory, o número máximo de objetos retornados por uma pesquisa é de 1000 objetos.

 

 




