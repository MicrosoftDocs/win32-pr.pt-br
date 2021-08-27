---
description: Recupera informações de erro estendidas sobre métodos que lidam com vários objetos, como Populate e SaveChanges no objeto COMAdminCatalogCollection e métodos para instalar, importar ou exportar aplicativos ou componentes no objeto COMAdminCatalog.
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
ms.openlocfilehash: 9953bc1119d7e203936ca7e78048a4083a996ec2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881049"
---
# <a name="errorinfo-collection"></a>Coleção ErrorInfo

Recupera informações de erro estendidas sobre métodos que lidam com vários objetos, como [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e métodos para instalar, importar ou exportar aplicativos ou componentes no objeto [**COMAdminCatalog.**](comadmincatalog.md)

Use o [**método GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) em [**um COMAdminCatalogCollection**](comadmincatalogcollection.md) para acessar a coleção **ErrorInfo** associada à coleção original que tem um erro.

Você deve chamar [**GetCollection em**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) **ErrorInfo** imediatamente após ocorrer um erro; caso contrário, as informações de erro são perdidas.

Essa coleção não dá suporte aos [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membros

A **coleção ErrorInfo** herda da interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção de cada coleção, exceto **para ErrorInfo,** [**InprocServers,**](inprocservers.md) [**PropertyInfo,**](propertyinfo.md) [**RelatedCollectionInfo,**](relatedcollectioninfo.md) [**Root**](root.md)e [**WOWInprocServers.**](wowinprocservers.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte no [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [ErrorCode](#errorcode)
-   [Majorref](#majorref)
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



 

### <a name="majorref"></a>Majorref



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O [**valor**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) da propriedade Key para o objeto que tem um erro. Por exemplo, se uma chamada [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para uma coleção falhar em um objeto específico na coleção, o valor da propriedade **Key** desse objeto será relatado como o valor MajorRef. Use essa propriedade para ver o item que falha ao atualizar ou para encontrar o componente ou DLL que falha ao instalar. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Padrão        | Nenhum                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Uma especificação precisa do item que tem um erro, como um nome de propriedade. Se ocorrerem vários erros ou em contextos nos quais isso não se aplica, MinorRef será &lt; &gt; Inválido. |
| Access         | ReadOnly                                                                                                                                                                          |
| Type           | String                                                                                                                                                                            |
| Padrão        | Nenhum                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do objeto ou arquivo que tem um erro. Essa propriedade é retornada quando [**o método de**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) propriedade Key ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                                                                                 |
| Type           | String                                                                                                                                                                                                                   |
| Padrão        | Nenhum                                                                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
