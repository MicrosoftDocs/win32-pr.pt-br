---
title: Usando o método SetSearchPreference
description: Chamar o método IDirectorySearch SetSearchPreference altera a maneira como os resultados da pesquisa são obtidos e apresentados por meio da interface IDirectorySearch.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- SetSearchPreference ADSI, usando o método SetSearchPreference
- ADSI ADSI, código de exemplo C/C++, usando o método SetSearchPreference
- consulta ADSI, usando SetSearchPreference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c357fd331ae8589bffdd3ff7a834a7bc9e0430
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004848"
---
# <a name="using-the-setsearchpreference-method"></a>Usando o método SetSearchPreference

Chamar o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) altera a maneira como os resultados da pesquisa são obtidos e apresentados por meio da interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

A documentação do SDK define [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) da seguinte maneira:


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



Várias preferências podem ser definidas passando uma matriz como o primeiro parâmetro e o tamanho da matriz como o segundo parâmetro.


```C++
ADS_SEARCHPREF_INFO arSearchPrefs[2];
 
arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_PAGESIZE; 
arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
arSearchPrefs[0].vValue.Integer = 100;
 
arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
arSearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER; 
arSearchPrefs[1].vValue.Integer = ADS_SCOPE_SUBTREE; 
 
hr = pDSearch->SetSearchPreference(&arSearchPrefs, 2);
```



Este exemplo define o tamanho da página como 100 linhas e o escopo para o \_ tipo de subárvore de escopo ADS \_ . A configuração tamanho da página faz com que o servidor retorne imediatamente os dados para o cliente, depois de 100 linhas terem sido calculadas. A \_ \_ configuração subárvore do escopo ADS faz com que a pesquisa abranja todas as ramificações na árvore abaixo do ponto em que a pesquisa está sendo executada.

 

 




