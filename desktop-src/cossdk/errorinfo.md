---
description: Recupera informações de erro estendidas referentes a métodos que lidam com vários objetos, como Populate e SaveChanges no objeto COMAdminCatalogCollection, e métodos para instalar, importar ou exportar aplicativos ou componentes no objeto COMAdminCatalog.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: Coleção ErrorInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457096"
---
# <a name="errorinfo-collection"></a>Coleção ErrorInfo

Recupera informações de erro estendidas referentes a métodos que lidam com vários objetos, como [**populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , e métodos para instalar, importar ou exportar aplicativos ou componentes no objeto [**COMAdminCatalog**](comadmincatalog.md) .

Use o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) em um [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para acessar a coleção **errorInfo** associada à coleção original que tem um erro.

Você deve chamar [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) em **errorInfo** imediatamente após ocorrer um erro; caso contrário, as informações de erro serão perdidas.

Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **errorInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção de cada coleção, exceto **errorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**root**](root.md)e [**WOWInprocServers**](wowinprocservers.md).

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [ErrorCode](#errorcode)
-   [MajorRef](#majorref)
-   [MinorRef](#minorref)
-   [Nome](#name)

### <a name="errorcode"></a>ErrorCode



| Entrada | Valor |
|----------------|----------------------------------------|
| Descrição    | O código de erro para o objeto ou arquivo. |
| Access         | ReadOnly                               |
| Type           | String                                 |
| Padrão        | Nenhum                                   |
| Sistema mínimo | Windows 2000                           |



 

### <a name="majorref"></a>MajorRef



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O valor da propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) do objeto que tem um erro. Por exemplo, se uma chamada [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para uma coleção falhar em um objeto específico na coleção, o valor da propriedade de **chave** desse objeto será relatado como o valor de MajorRef. Use essa propriedade para examinar o item que não pôde ser atualizado ou para localizar o componente ou DLL que não é instalado. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Padrão        | Nenhum                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Uma especificação precisa do item que tem um erro, como um nome de propriedade. Se ocorrerem vários erros ou em contextos nos quais isso não se aplica, MinorRef será <Invalid> . |
| Access         | ReadOnly                                                                                                                                                                          |
| Type           | String                                                                                                                                                                            |
| Padrão        | Nenhum                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do objeto ou arquivo que tem um erro. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                                                                                 |
| Type           | String                                                                                                                                                                                                                   |
| Padrão        | Nenhum                                                                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
