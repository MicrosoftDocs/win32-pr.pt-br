---
description: Exemplo introdutório usando o catálogo de administração do COM+
ms.assetid: e9ce25aa-4fb1-4357-9f4e-5bf649e29447
title: Exemplo introdutório usando o catálogo de administração do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db24f3985538b7189534c9fef3ef279ed240e3a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757583"
---
# <a name="introductory-example-using-the-com-administration-catalog"></a>Exemplo introdutório usando o catálogo de administração do COM+

Ao usar programaticamente o catálogo de administração do COM+, você normalmente executa as seguintes etapas gerais (não dadas em uma ordem estrita aqui):

-   Abra uma sessão com o catálogo COM+ no computador local. Opcionalmente, conecte-se ao catálogo COM+ em um computador remoto.
-   Executar ações como iniciar ou interromper serviços — ações que não pertencem a um aplicativo COM+ específico.
-   Execute ações como instalar ou exportar aplicativos COM+ ou instalar componentes em aplicativos — ações que pertencem à leitura ou gravação em arquivos.
-   Adicione novos itens a coleções, como criar um novo aplicativo COM+ adicionando um novo item à coleção "aplicativos".
-   Definir ou obter propriedades de um item em uma coleção.
-   Salve ou descarte as alterações pendentes no catálogo.
-   Manipule quaisquer erros que possam ocorrer.

Para mostrar a aparência dessas etapas quando você usa os objetos COMAdmin, um exemplo de Visual Basic da Microsoft é fornecido abaixo. Ele ilustra brevemente algumas das etapas típicas descritas acima, como localizar coleções, enumerar por meio de uma coleção para recuperar um item e definir propriedades nesse item.

No exemplo a seguir, você executará as seguintes ações:

1.  Crie um novo aplicativo COM+, "MyHomeZoo".
2.  Instale alguns componentes, Cat e Dog, no aplicativo. Ambos os componentes estão contidos em uma única DLL que já deve existir: MyZoo.dll.
3.  Configure a segurança baseada em função para o aplicativo definindo duas funções: ZooKeeper e AllergicToCats.
4.  Atribua o acesso à função ZooKeeper a todo o aplicativo.
5.  Atribua o acesso à função AllergicToCats somente ao componente Dog.
6.  Ative as propriedades de segurança para que a verificação de função seja imposta para o aplicativo.
7.  Exporte o aplicativo MyHomeZoo para um arquivo para que ele possa ser instalado em outros computadores.

Para usar este exemplo de Visual Basic, adicione uma referência à biblioteca de tipos de administrador do COM+.


```VB
Function SetupMyZoo() As Boolean  ' Return False if any errors occur.

    '  Initialize error handling for this function.
    SetupMyZoo = False 
    On Error GoTo My_Error_Handler

    '  Open a session with the catalog.
    '  Instantiate a COMAdminCatalog object. 
    Dim objCatalog As COMAdminCatalog
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")

    '  Create a new COM+ application.
    '  First get the "Applications" collection from the catalog.
    Dim objApplicationsColl As COMAdminCatalogCollection
    Set objApplicationsColl = objCatalog.GetCollection("Applications")

    '  Add a new item to this collection. 
    Dim objZooApp As COMAdminCatalogObject
    Set objZooApp = objApplicationsColl.Add

    '  The "Applications" collection determines the available properties.
    '  Set the "Name" property of the new application item. 
    objZooApp.Value("Name") = "MyHomeZoo"

    '  Set the "Description" property of the new application item. 
    objZooApp.Value("Description") = "My pets at home"

    '  Save changes made to the "Applications" collection. 
    objApplicationsColl.SaveChanges

    '  Install components into the application.
    '  Use the InstallComponent method on COMAdminCatalog. 
    '  In this case, the last two parameters are passed as empty strings.
    objCatalog.InstallComponent "MyHomeZoo","MyZoo.DLL","","" 

    '  Define the roles ZooKeeper and AllergicToCats 
    '  by adding them to the "Roles" collection related to MyHomeZoo. 
    '  First get the "Roles" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Roles", 
    '  and the Key property value of objZooApp.   
    '  The Key property uniquely identifies the object, serving
    '  here to distinguish the "Roles" collection related 
    '  to MyHomeZoo from that of any other application. 
    Dim objRolesColl As COMAdminCatalogCollection
    Set objRolesColl = objApplicationsColl.GetCollection("Roles", objZooApp.Key)

    '  Add new items to this "Roles" collection. 
    Dim objZooKeeperRole As COMAdminCatalogObject
    Dim objAllergicToCatsRole As COMAdminCatalogObject
    Set objZooKeeperRole = objRolesColl.Add
    Set objAllergicToCatsRole = objRolesColl.Add

    '  Set the "Name" for the new items.
    objZooKeeperRole.Value("Name") = "ZooKeeper" 
    objAllergicToCatsRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to any items in this "Roles" collection. 
    objRolesColl.SaveChanges

    '  Assign the AllergicToCats role to the Dog component to 
    '  restrict its scope of access. (The ZooKeeper role, if assigned
    '  only at the application level, can access the whole application.)
    '  First get the "Components" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Components", and
    '  the Key property value of objZooApp. 
    Dim objZooComponentsColl As COMAdminCatalogCollection
    Set objZooComponentsColl = objApplicationsColl.GetCollection("Components", objZooApp.Key) 

    '  Find the Dog component item in this "Components" collection.
    '  First Populate the collection to read in data for all its items. 
    objZooComponentsColl.Populate

    '  Enumerate through the "Components" collection 
    '  until the Dog component item is located. 
    Dim objDog As COMAdminCatalogObject 
    For Each objDog in objZooComponentsColl
        If objDog.Name = "Dog" Then 
            Exit For
        End If
    Next 
    '  Set the role checking property at the component level for Dog.
        objDog.Value("ComponentAccessChecksEnabled") = True 

    '  Save these changes.
        objZooComponentsColl.SaveChanges
    '  Get the "RolesForComponent" collection related to the 
    '  Dog component, using the Key property of objDog. 
    Dim objRolesForDogColl As COMAdminCatalogCollection 
    Set objRolesForDogColl = objZooComponentsColl.GetCollection("RolesForComponent", objDog.Key) 

    '  Add a new item to this "RolesForComponent" collection. 
    Dim objCatSneezerRole As COMAdminCatalogObject
    Set objCatSneezerRole = objRolesForDogColl.Add

    '  Set the "Name" of the new item to be "AllergicToCats". 
    objCatSneezerRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to this "RolesForComponent" collection. 
    objRolesForDogColl.SaveChanges

    '  Now set properties to enforce role-based security. 
    '  First set role-based security at the application level.
    objZooApp.Value("ApplicationAccessChecksEnabled") = True 
    objZooApp.Value("AccessChecksLevel") = COMAdminAccessChecksApplicationComponentLevel 

    '  Save these changes.
    objApplicationsColl.SaveChanges

    '  Finally, export the new configured MyHomeZoo application to an 
    '  MSI file, used to install the application on other machines.
    '  Use the ExportApplication method on COMAdminCatalogObject.
    objCatalog.ExportApplication "MyHomeZoo", "c:\Program Files\COM applications\MyHomeZoo.MSI", 4

    '  Exit the function gracefully.
    SetupMyZoo = True

My_Error_Handler:
    If Not SetupMyZoo Then
        MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) & ")" & vbNewLine & Err.Description
    End If
    objCatSneezerRole = Nothing
    objRolesForDogColl = Nothing
    objDog = Nothing
    objZooComponentsColl = Nothing
    objAllergicToCatsRole = Nothing
    objZooKeeperRole = Nothing
    objRolesColl = Nothing
    objZooApp = Nothing
    objApplicationsColl = Nothing
    objCatalog = Nothing
Exit Function
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operações de administração COM+ em transações](com--administration-operations-within-transactions.md)
</dt> <dt>

[Manipulando erros de administração COM+](handling-com--administration-errors.md)
</dt> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Definindo propriedades e salvando alterações no catálogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



