---
description: Para cada aplicativo que usa um armazenamento de política de autorização, você deve criar um objeto IAzApplication e salvá-lo em um armazenamento de políticas.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Criando um objeto de aplicativo no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 02a5ada4a8a79244cc454d9efc88e69a5d9a205241119b5dda371699f0c86552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782542"
---
# <a name="creating-an-application-object-in-script"></a>Criando um objeto de aplicativo no script

Um armazenamento de política de autorização contém informações de política de autorização para um ou mais aplicativos. Para cada aplicativo que usa um armazenamento de política de autorização, você deve criar um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvá-lo em um armazenamento de políticas.

O exemplo a seguir mostra como criar um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que representa um aplicativo e como adicionar o objeto **IAzApplication** ao armazenamento de política de autorização usado pelo aplicativo. O exemplo supõe que haja um armazenamento de políticas XML existente chamado MyStore.xml no diretório raiz da unidade C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.CreateApplication("Expense")

'  Save changes to the store.
expenseApp.Submit
```



 

 



