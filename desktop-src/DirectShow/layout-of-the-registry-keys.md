---
description: Layout das chaves do Registro
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Layout das chaves do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4473027b2612d16b3c6daee4f8e708d90b993397b133db111aa55c58e9c4ceb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502286"
---
# <a name="layout-of-the-registry-keys"></a>Layout das chaves do Registro

DirectShow filtros são registrados em dois locais:

-   A DLL que contém o filtro é registrada como o servidor COM do filtro. Quando um aplicativo chama **CoCreateInstance** para criar o filtro, a biblioteca COM do Microsoft Windows usa essa entrada do Registro para localizar a DLL.
-   Informações adicionais sobre o filtro podem ser registradas em uma categoria de filtro. Essas informações permitem que o [Enumerador de Dispositivo do Sistema](system-device-enumerator.md) e o [Mapeador](filter-mapper.md) de Filtro localizem o filtro.

Os filtros não são necessários para registrar as informações de filtro adicionais. Desde que a DLL esteja registrada como o servidor COM, um aplicativo pode criar o filtro e adicioná-lo a um grafo de filtro. No entanto, se você quiser que seu filtro seja descoberto pelo Enumerador de Dispositivo do Sistema ou pelo Mapeador de Filtros, registre as informações adicionais.

A entrada do Registro para a DLL tem as seguintes chaves:


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



A entrada do Registro para as informações de filtro tem as seguintes chaves:


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



é o GUID de uma categoria de filtro. (Consulte [Categorias de Filtro](filter-categories.md).) As informações de filtro são empacotadas em um formato binário. A interface [**IFilterMapper2 descompacta**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) esses dados quando pesquisa um filtro no Registro.

Todos os GUIDs da categoria de filtro são listados no Registro sob a seguinte chave:


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



