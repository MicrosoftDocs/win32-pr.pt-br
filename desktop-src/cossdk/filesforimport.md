---
description: Recupera informações para aplicativos que são importados.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Coleção FilesForImport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089368"
---
# <a name="filesforimport-collection"></a>Coleção FilesForImport

Recupera informações para aplicativos que são importados.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **FilesForImport** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [ApplicationFileName](#applicationfilename)
-   [ApplicationName](#applicationname)
-   [Descrição](#partitiondescription)
-   [FileName](#applicationfilename)
-   [HasUsers](#hasusers)
-   [IsProxy](#isproxy)
-   [IsService](#isservice)
-   [PartitionDescription](#partitiondescription)
-   [PartitionID](#partitionid)
-   [PartitionName](#partitionname)

### <a name="applicationfilename"></a>ApplicationFileName



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------|
| Descrição    | O nome do arquivo MSI que contém o aplicativo que pode ser importado. |
| Access         | ReadOnly                                                                     |
| Type           | String                                                                       |
| Padrão        | N/D                                                                          |
| Sistema mínimo | Windows XP                                                                   |



 

### <a name="applicationname"></a>ApplicationName



| Entrada | Valor |
|----------------|------------------------------|
| Descrição    | O nome do aplicativo. |
| Access         | ReadOnly                     |
| Type           | String                       |
| Padrão        | ""                           |
| Sistema mínimo | Windows XP                   |



 

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|-----------------------------------|
| Descrição    | Uma descrição do aplicativo. |
| Access         | ReadOnly                          |
| Type           | String                            |
| Padrão        | ""                                |
| Sistema mínimo | Windows XP                        |



 

### <a name="filename"></a>FileName



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do arquivo DLL ou EXE que contém o aplicativo. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                |
| Padrão        | ""                                                                                                                                                                                                                                    |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a>HasUsers



| Entrada | Valor |
|----------------|--------------------------------------------------|
| Descrição    | Indica se o aplicativo tem algum usuário. |
| Access         | ReadOnly                                         |
| Tipo           | Bool                                             |
| Padrão        | Falso                                            |
| Sistema mínimo | Windows XP                                       |



 

### <a name="isproxy"></a>IsProxy



| Entrada | Valor |
|----------------|-----------------------------------------------|
| Descrição    | Indica se o aplicativo é um proxy. |
| Access         | ReadOnly                                      |
| Tipo           | Bool                                          |
| Padrão        | Falso                                         |
| Sistema mínimo | Windows XP                                    |



 

### <a name="isservice"></a>IsService



| Entrada | Valor |
|----------------|-------------------------------------------------|
| Descrição    | Indica se o aplicativo é um serviço. |
| Access         | ReadOnly                                        |
| Tipo           | Bool                                            |
| Padrão        | Falso                                           |
| Sistema mínimo | Windows XP                                      |



 

### <a name="partitiondescription"></a>PartitionDescription



| Entrada | Valor |
|----------------|-----------------------------------------------|
| Descrição    | Uma descrição da partição do aplicativo. |
| Access         | ReadOnly                                      |
| Type           | String                                        |
| Padrão        | ""                                            |
| Sistema mínimo | Windows Server 2003                           |



 

### <a name="partitionid"></a>PartitionID



| Entrada | Valor |
|----------------|------------------------------------------|
| Descrição    | O GUID da partição do aplicativo. |
| Access         | ReadOnly                                 |
| Type           | String                                   |
| Padrão        | ""                                       |
| Sistema mínimo | Windows Server 2003                      |



 

### <a name="partitionname"></a>PartitionName



| Entrada | Valor |
|----------------|------------------------------------------|
| Descrição    | O nome da partição do aplicativo. |
| Access         | ReadOnly                                 |
| Type           | String                                   |
| Padrão        | ""                                       |
| Sistema mínimo | Windows Server 2003                      |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
