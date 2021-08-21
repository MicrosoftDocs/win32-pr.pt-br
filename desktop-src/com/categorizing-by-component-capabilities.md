---
title: Categorizando por funcionalidades de componente
description: As categorias de componente podem ser usadas para exibir um subconjunto de todos os componentes instalados.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251e8197c00a39c8d9666dee7122be7445402fc84ce7b3508987bcf79f27df15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048744"
---
# <a name="categorizing-by-component-capabilities"></a>Categorizando por funcionalidades de componente

As categorias de componente podem ser usadas para exibir um subconjunto de todos os componentes instalados. Cada categoria de componente é identificada por um GUID, conhecido como CATID (ID da Categoria). Cada CATID tem uma lista de nomes marcados por localidade e leitura humana associados a ele. Uma listagem dos CATIDs e dos nomes que podem ser lidos por humanos é armazenada em um local conhecido no Registro.

Por exemplo, todos os componentes que implementam a funcionalidade para a incorporação de documentos OLE podem ser classificados dentro de uma categoria de componente. No passado, esses objetos teriam sido identificados pela chave "Inserível" no Registro. Para usar categorias de componente, as seguintes informações seriam adicionadas ao Registro:

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

Cada classe que implementa a funcionalidade correspondente a uma categoria de componente lista a ID da categoria para essa categoria dentro da chave CLSID no Registro. Como um único componente pode dar suporte a uma ampla variedade de funcionalidades, os componentes podem pertencer a várias categorias de componentes. Por exemplo, um controle OLE específico pode dar suporte a todas as funcionalidades necessárias para participar como a incorporação de documentos OLE, a associação de dados do Microsoft Visual Basic e a funcionalidade da Internet. Esse controle teria as seguintes informações armazenadas em sua chave CLSID no Registro:

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

Com essas informações, um contêiner pode enumerar os controles instalados em um sistema e exibir somente os controles que suportam a funcionalidade exigida pelo contêiner. O uso de categorias de componentes fornece uma maneira de categorizar componentes pela funcionalidade implementada do componente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associando ícones a uma categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizando por funcionalidades de contêiner](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classes e associações padrão](default-classes-and-associations.md)
</dt> <dt>

[Definindo categorias de componentes](defining-component-categories.md)
</dt> <dt>

[O Gerenciador de Categorias de Componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




