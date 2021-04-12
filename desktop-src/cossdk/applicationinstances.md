---
description: Recupera informações sobre a execução de aplicativos.
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
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456985"
---
# <a name="applicationinstances-collection"></a>Coleção ApplicationInstances

Recupera informações sobre a execução de aplicativos.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **ApplicationInstances** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Aplicativos**](applications.md)
-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Aplicativo](#applicationinstances-collection)
-   [HasRecycled](#hasrecycled)
-   [InstanceID](#instanceid)
-   [IsPaused](#ispaused)
-   [PartitionID](#partitionid)
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
| Descrição    | O identificador global exclusivo para a instância do aplicativo. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                                                                                            |
| Type           | String                                                                                                                                                                                                                              |
| Padrão        | N/D                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>IsPaused



| Entrada | Valor |
|----------------|-----------------------------------------------------------------|
| Descrição    | Indica se a instância do aplicativo está pausada no momento. |
| Access         | ReadOnly                                                        |
| Tipo           | Bool                                                            |
| Padrão        | Falso                                                           |
| Sistema mínimo | Windows XP                                                      |



 

### <a name="partitionid"></a>PartitionID



| Entrada | Valor |
|----------------|-------------------------------------------------|
| Descrição    | A ID da partição que o aplicativo está usando. |
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

 

 
