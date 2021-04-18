---
description: Navegando na hierarquia da coleção COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navegando na hierarquia da coleção COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766936"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Navegando na hierarquia da coleção COM+

Algumas coleções que você pode recuperar facilmente usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) no objeto [**COMAdminCatalog**](comadmincatalog.md) . Esse método recupera uma coleção de "nível superior"; ou seja, uma coleção, como [**aplicativos**](applications.md), que tem seu próprio e que é exclusiva e não logicamente incorporadas em outra coleção.

No entanto, muitas coleções são logicamente incorporadasdas em outra coleção porque contêm elementos que fazem parte de uma estrutura maior. Por exemplo, a coleção de [**componentes**](components.md) é incorporadas, ou relacionada, à coleção de [**aplicativos**](applications.md) porque ela contém os componentes instalados em um aplicativo com+ específico, que por sua vez corresponde a um item na coleção de **aplicativos** . Coleções relacionadas como esta não são exclusivas; Há uma coleção de **componentes** para cada aplicativo distinto.

Portanto, as coleções são organizadas em uma estrutura hierárquica que corresponde naturalmente às relações lógicas entre os itens que elas contêm. Um diagrama da hierarquia de coleção pode ser encontrado em [coleções de administração do com+](com--administration-collections.md). Para muitos dos elementos que você deseja configurar usando os objetos COMAdmin, você precisa navegar por alguma parte da hierarquia de coleção para recuperar o item apropriado.

O que isso significa na prática é que, se você quiser obter um item em uma coleção relacionada, será necessário percorrer todas as coleções de subsuming de nível superior necessárias primeiro. E para recuperar uma coleção relacionada, você precisa recuperar o item específico na coleção pai à qual a coleção filho está relacionada. Por exemplo, se você quiser configurar um item correspondente a um componente em um aplicativo COM+ específico, você deve executar as seguintes etapas:

1.  Obter a coleção de [**aplicativos**](applications.md) e preenchê-la.
2.  Enumere o conteúdo da coleção de [**aplicativos**](applications.md) até chegar ao item correspondente ao aplicativo com+ correto.
3.  Obtenha e preencha a coleção de [**componentes**](components.md) para esse aplicativo com+ específico.
4.  Enumere o conteúdo da coleção de [**componentes**](components.md) até chegar ao item correspondente ao componente correto.

O exemplo de Visual Basic a seguir da Microsoft mostra como executar as etapas anteriores:


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



Dois métodos **GetCollection** distintos são usados no exemplo anterior. O primeiro é exposto por [**COMAdminCatalog**](comadmincatalog.md) e é usado para obter uma coleção de nível superior — neste caso, "Applications". O segundo é exposto por [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e é usado para obter uma coleção relacionada à coleção atual; Você indica precisamente qual coleção deseja passando o nome "Components" e o valor da propriedade de chave do objeto pai. O valor da propriedade de chave é geralmente um nome ou um GUID que identifica exclusivamente o objeto; Esse valor é identificado na documentação de cada coleção.

No caso mais geral, você precisa obter coleções relacionadas iterativamente na hierarquia de coleção até recuperar a coleção desejada. As etapas que você seguiria seguem o mesmo modelo geral, repetidamente. Para obter uma lista completa de coleções, consulte [coleções de administração do com+](com--administration-collections.md).

Em alguns casos, talvez você queira usar um método de atalho na segunda vez que seguir um caminho por meio da hierarquia de coleção. Você pode usar esse método somente depois que você já armazenou em cache todos os valores de chave intermediários. Para obter detalhes, consulte [**ICOMAdminCatalog:: GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Populando coleções COM+](populating-com--collections.md)
</dt> <dt>

[Consultando coleções relacionadas disponíveis](querying-for-available-related-collections.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



