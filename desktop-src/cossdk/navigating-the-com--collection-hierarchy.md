---
description: Navegando na hierarquia de coleção COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navegando na hierarquia de coleção COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef6f23cd9f584b6cbe496fe7122abfa9978cd25cb28d81a5c89782b718138be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070446"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Navegando na hierarquia de coleção COM+

Algumas coleções que você pode recuperar facilmente usando o [**método GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) [**no objeto COMAdminCatalog.**](comadmincatalog.md) Esse método recupera uma coleção de "nível superior"; ou seja, uma coleção como [**Aplicativos**](applications.md), que se mantém por conta própria e que é exclusiva e não é logicamente subsumada em outra coleção.

No entanto, muitas coleções são logicamente subumadas em outra coleção porque contêm elementos que fazem parte de alguma estrutura maior. Por exemplo, [](components.md) a coleção Components é subumada ou relacionada à coleção [**De**](applications.md) aplicativos porque contém os componentes instalados em um aplicativo COM+ específico, que corresponde a um item na coleção **Aplicativos.** Coleções relacionadas como essa não são exclusivas; há uma coleção **Componentes** para cada aplicativo distinto.

Portanto, as coleções são organizadas em uma estrutura hierárquica que corresponde naturalmente às relações lógicas entre os itens que elas contêm. Um diagrama da hierarquia de coleção pode ser encontrado em [Coleções de Administração COM+.](com--administration-collections.md) Para muitos dos elementos que você deseja configurar usando os objetos COMAdmin, você precisa navegar por alguma parte da hierarquia de coleção para recuperar o item apropriado.

Isso significa que, na prática, se você quiser obter um item em uma coleção relacionada, precisará passar por todas as coleções de nível mais alto necessárias, subsumando primeiro. E para recuperar uma coleção relacionada, você precisa recuperar o item específico na coleção pai à qual a coleção filho está relacionada. Por exemplo, se você quiser configurar um item correspondente a um componente em um aplicativo COM+ específico, execute as seguintes etapas:

1.  Obter a [**coleção Aplicativos**](applications.md) e populá-la.
2.  Enumerar pelo conteúdo da coleção [**Aplicativos**](applications.md) até chegar ao item correspondente ao aplicativo COM+ correto.
3.  Obter e popular a coleção [**Componentes**](components.md) para esse aplicativo COM+ específico.
4.  Enumerar pelo conteúdo da coleção [**Componentes**](components.md) até chegar ao item correspondente ao componente correto.

O exemplo de Visual Basic Microsoft a seguir mostra como executar as etapas anteriores:


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



Dois métodos **GetCollection** distintos são usados no exemplo anterior. O primeiro é exposto por [**COMAdminCatalog**](comadmincatalog.md) e é usado para obter uma coleção de nível superior– nesse caso, "Aplicativos". O segundo é exposto por [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e é usado para obter uma coleção relacionada à coleção atual; você indica precisamente qual coleção você deseja passando o nome "Componentes" e o valor da propriedade Key do objeto pai. O valor da propriedade Key geralmente é um nome ou um GUID que identifica exclusivamente o objeto; esse valor é identificado na documentação de cada coleção.

No caso mais geral, você precisa obter coleções relacionadas iterativamente na hierarquia de coleção até recuperar a coleção que deseja. As etapas que você seguiria seguem o mesmo modelo geral, repetitivo. Para ver uma lista completa de coleções, consulte [Coleções de Administração COM+.](com--administration-collections.md)

Em alguns casos, talvez você queira usar um método de atalho na segunda vez que seguir um caminho pela hierarquia da coleção. Você pode usar esse método somente depois de já ter armazenado em cache todos os valores de Chave intermediárias. Para obter detalhes, [**consulte ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Populando coleções COM+](populating-com--collections.md)
</dt> <dt>

[Consultando coleções relacionadas disponíveis](querying-for-available-related-collections.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



