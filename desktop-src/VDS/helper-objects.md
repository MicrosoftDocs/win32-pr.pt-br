---
description: 'O VDS fornece dois objetos auxiliares: o objeto de enumeração e o objeto Async. Este tópico descreve cada um desses objetos e fornece links para exemplos de como os chamadores funcionam com cada um deles.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Objetos auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98464c31548309b50e21b2b8e3e20a867efe7ca647d7a9879efd0ef346e6a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999476"
---
# <a name="helper-objects"></a>Objetos auxiliares

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O VDS fornece dois objetos auxiliares: o objeto de enumeração e o objeto Async. Este tópico descreve cada um desses objetos e fornece links para exemplos de como os chamadores funcionam com cada um deles.

## <a name="enumeration-object"></a>Objeto de enumeração

Um objeto de enumeração é enumerado por meio de um conjunto de objetos VDS de um determinado tipo. Os objetos podem ser provedores, subsistemas, controladores, LUNs, plexes de LUN, unidades, pacotes de disco, discos, volumes ou plexes de volume. Os chamadores podem obter um ponteiro para um objeto específico selecionando o objeto desejado da enumeração que é retornada pelo método apropriado. Para obter um exemplo de código, consulte [trabalhando com objetos de enumeração](working-with-enumeration-objects.md).

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas. 

| Tipo                                              | Elemento                                  |
|---------------------------------------------------|------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| Enumerações associadas                           | Nenhum.                                    |
| Estruturas associadas                             | Nenhum.                                    |



 

## <a name="async-object"></a>Objeto Async

Um objeto assíncrono gerencia operações assíncronas. Os métodos que iniciam operações assíncronas retornam um ponteiro para uma interface [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) , que permite que o chamador cancele, aguarde e consulte o status da operação assíncrona.

As operações de longa execução do VDS tendem a ser implementadas de forma assíncrona. Os programas básicos e dinâmicos do provedor de software implementam métodos assíncronos de forma consistente para operações de volume, partição e disco. Os provedores de hardware também implementam métodos assíncronos de forma assíncrona. Independentemente de como o provedor implementa o método, a operação deve retornar um ponteiro para uma interface [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) para o chamador. Para obter um exemplo de código, consulte [gerenciando operações assíncronas](managing-asynchronous-operations.md).

As operações assíncronas incluem:

-   Criação de um LUN, volume ou partição.
-   Formatando um volume ou uma partição.
-   Adicionar ou remover um plex de LUN ou volume.
-   Quebrando um plex de volume.
-   Estendendo ou reduzindo um LUN ou volume.
-   Recuperando um LUN ou volume.
-   Limpando um disco.
-   Substituindo um disco.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas. 

| Tipo                                              | Elemento                        |
|---------------------------------------------------|--------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| Enumerações associadas                           | Nenhum.                          |
| Estruturas associadas                             | Nenhum.                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[Trabalhando com objetos de enumeração](working-with-enumeration-objects.md)
</dt> <dt>

[Gerenciando operações assíncronas](managing-asynchronous-operations.md)
</dt> </dl>

 

 
