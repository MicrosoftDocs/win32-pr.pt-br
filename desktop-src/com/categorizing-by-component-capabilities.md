---
title: Categorizando por recursos de componente
description: As categorias de componentes podem ser usadas para exibir um subconjunto de todos os componentes instalados.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771274"
---
# <a name="categorizing-by-component-capabilities"></a>Categorizando por recursos de componente

As categorias de componentes podem ser usadas para exibir um subconjunto de todos os componentes instalados. Cada categoria de componente é identificada por um GUID, chamado de CATID (ID de categoria). Cada CATID tem uma lista de nomes com marca de localidade e legíveis para pessoas associadas a ele. Uma lista das CATIDs e dos nomes legíveis é armazenada em um local conhecido no registro.

Por exemplo, todos os componentes que implementam a funcionalidade para inserção de documentos OLE podem ser classificados dentro de uma categoria de componente. No passado, esses objetos teriam sido identificados pela chave "Insertable" no registro. Para usar categorias de componente em vez disso, as seguintes informações seriam adicionadas ao registro:

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

Cada classe que implementa a funcionalidade correspondente a uma categoria de componente lista a ID de categoria para essa categoria dentro da chave de CLSID no registro. Como um único componente pode dar suporte a uma ampla gama de funcionalidades, os componentes podem pertencer a várias categorias de componentes. Por exemplo, um controle OLE específico pode dar suporte a toda a funcionalidade necessária para participar como incorporação de documentos OLE, vinculação de dados do Microsoft Visual Basic e funcionalidade de Internet. Tal controle teria as seguintes informações armazenadas em sua chave CLSID no registro:

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

Com essas informações, um contêiner pode enumerar os controles instalados em um sistema e exibir somente os controles que dão suporte à funcionalidade exigida pelo contêiner. O uso de categorias de componentes fornece uma maneira de categorizar componentes pela funcionalidade implementada do componente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associando ícones a uma categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizando por recursos de contêiner](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classes e associações padrão](default-classes-and-associations.md)
</dt> <dt>

[Definindo categorias de componentes](defining-component-categories.md)
</dt> <dt>

[O Gerenciador de categorias de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




