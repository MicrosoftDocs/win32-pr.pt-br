---
description: Idêntico à coleção InprocServers, exceto que essa coleção também inclui servidores locais.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: Coleção LegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2ea542fa539ea1eb1cceae0f4cb8ba8dc2012085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756797"
---
# <a name="legacyservers-collection"></a>Coleção LegacyServers

Idêntico à coleção [**InprocServers**](inprocservers.md) , exceto que essa coleção também inclui servidores locais.

Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **LegacyServers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [ClassName](#classname)
-   [CLSID](#clsid)
-   [InprocServer32](#inprocserver32)
-   [LocalServer32](#localserver32)
-   [ProgID](#progid)

### <a name="classname"></a>ClassName



| Entrada | Valor |
|----------------|------------------------|
| Descrição    | O nome da classe. |
| Access         | ReadOnly               |
| Type           | String                 |
| Padrão        | N/D                    |
| Sistema mínimo | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um GUID para o componente. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Padrão        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrada | Valor |
|----------------|----------------------------------|
| Descrição    | O caminho do arquivo para o componente. |
| Access         | ReadOnly                         |
| Type           | String                           |
| Padrão        | N/D                              |
| Sistema mínimo | Windows XP                       |



 

### <a name="localserver32"></a>LocalServer32



| Entrada | Valor |
|----------------|---------------------------------------------------------------|
| Descrição    | Especifica o caminho completo para um aplicativo de servidor local de 32 bits. |
| Access         | ReadOnly                                                      |
| Type           | String                                                        |
| Padrão        | N/D                                                           |
| Sistema mínimo | Windows XP                                                    |



 

### <a name="progid"></a>ProgID



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um nome que identifica o componente. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                            |
| Type           | String                                                                                                                                                              |
| Padrão        | N/D                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
