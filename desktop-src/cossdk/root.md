---
description: Contém as coleções de nível superior no catálogo.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Coleção raiz
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: ad896c69ab6fad75179c9bb30668143aa2ea741e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813486"
---
# <a name="root-collection"></a>Coleção raiz

Contém as coleções de nível superior no catálogo. Ele não contém nenhum objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) nem oferece suporte a nenhuma propriedade.

A coleção **raiz** não oferece suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

Não é possível navegar até a coleção **raiz** de qualquer coleção.

## <a name="members"></a>Membros

A coleção **raiz** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

A seguir estão as coleções de nível superior no catálogo:

-   [**ApplicationCluster**](applicationcluster.md)
-   [**ApplicationInstances**](applicationinstances.md)
-   [**Aplicativos**](applications.md)
-   [**Computerlist**](computerlist.md)
-   [**DCOMProtocols**](dcomprotocols.md)
-   [**EventClassesForIID**](eventclassesforiid.md)
-   [**FilesForImport**](filesforimport.md)
-   [**InprocServers**](inprocservers.md)
-   [**LegacyServers**](legacyservers.md)
-   [**LocalComputer**](localcomputer.md)
-   [**Partições**](partitions.md)
-   [**PartitionUsers**](partitionusers.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientSubscriptions**](transientsubscriptions.md)
-   [**WOWInprocServers**](wowinprocservers.md)
-   [**WOWLegacyServers**](wowlegacyservers.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
