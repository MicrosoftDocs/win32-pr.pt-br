---
description: Layout das chaves do registro
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Layout das chaves do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758430"
---
# <a name="layout-of-the-registry-keys"></a>Layout das chaves do registro

Os filtros do DirectShow são registrados em dois locais:

-   A DLL que contém o filtro é registrada como o servidor COM do filtro. Quando um aplicativo chama **CoCreateInstance** para criar o filtro, a biblioteca com do Microsoft Windows usa essa entrada de registro para localizar a dll.
-   Informações adicionais sobre o filtro podem ser registradas em uma categoria de filtro. Essas informações permitem que o [enumerador de dispositivo do sistema](system-device-enumerator.md) e o [mapeador de filtro](filter-mapper.md) localizem o filtro.

Os filtros não são necessários para registrar as informações de filtro adicionais. Desde que a DLL seja registrada como o servidor COM, um aplicativo pode criar o filtro e adicioná-lo a um grafo de filtro. No entanto, se você quiser que o filtro seja detectável pelo enumerador de dispositivo do sistema ou pelo mapeador de filtro, deverá registrar as informações adicionais.

A entrada do registro para a DLL tem as seguintes chaves:


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



A entrada de registro para as informações de filtro tem as seguintes chaves:


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



é o GUID de uma categoria de filtro. (Consulte [Filtrar categorias](filter-categories.md).) As informações do filtro são incluídas em um formato binário. A interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) desempacota esses dados quando procura um filtro no registro.

Todos os GUIDs de categoria de filtro estão listados no registro na seguinte chave:


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



