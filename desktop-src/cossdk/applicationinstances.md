---
description: Recupera informações sobre aplicativos em execução.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Coleção ApplicationInstances
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 957fe3fa556a3e41e2484116ff2c9242fd63efa1469a4a6040f31aa04a3627e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129378"
---
# <a name="applicationinstances-collection"></a>Coleção ApplicationInstances

Recupera informações sobre aplicativos em execução.

Essa coleção dá suporte [**aos métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membros

A **coleção ApplicationInstances** herda da interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Aplicativos**](applications.md)
-   [**Raiz**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte no [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Aplicativo](#applicationinstances-collection)
-   [HasRecycled](#hasrecycled)
-   [InstanceID](#instanceid)
-   [Ispaused](#ispaused)
-   [Partitionid](#partitionid)
-   [ProcessID](#processid)

### <a name="application"></a>Aplicativo



| Entrada | Valor |
|----------------|-------------------------------------|
| Descrição    | A ID do aplicativo em execução. |
| Access         | ReadOnly                            |
| Type           | String                              |
| Padrão        | N/D                                 |
| Sistema mínimo | Windows XP                          |



 

### <a name="hasrecycled"></a>HasRecycled



| Entrada | Valor |
|----------------|---------------------------------------------------------------|
| Descrição    | Indica se a instância do aplicativo foi reciclada. |
| Access         | ReadOnly                                                      |
| Tipo           | Bool                                                          |
| Padrão        | Falso                                                         |
| Sistema mínimo | Windows XP                                                    |



 

### <a name="instanceid"></a>InstanceID



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O identificador global exclusivo para a instância do aplicativo. Essa propriedade é retornada quando [**o método de**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) propriedade Key ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto dessa coleção. |
| Access         | ReadOnly                                                                                                                                                                                                                            |
| Type           | String                                                                                                                                                                                                                              |
| Padrão        | N/D                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>Ispaused



| Entrada | Valor |
|----------------|-----------------------------------------------------------------|
| Descrição    | Indica se a instância do aplicativo está em pausa no momento. |
| Access         | ReadOnly                                                        |
| Tipo           | Bool                                                            |
| Padrão        | Falso                                                           |
| Sistema mínimo | Windows XP                                                      |



 

### <a name="partitionid"></a>Partitionid



| Entrada | Valor |
|----------------|-------------------------------------------------|
| Descrição    | A ID de partição que o aplicativo está usando. |
| Access         | ReadOnly                                        |
| Type           | String                                          |
| Padrão        | N/D                                             |
| Sistema mínimo | Windows XP                                      |



 

### <a name="processid"></a>ProcessID



| Entrada | Valor |
|----------------|---------------------------------------------|
| Descrição    | A ID do processo da instância do aplicativo. |
| Access         | ReadOnly                                    |
| Type           | String                                      |
| Padrão        | N/D                                         |
| Sistema mínimo | Windows XP                                  |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
