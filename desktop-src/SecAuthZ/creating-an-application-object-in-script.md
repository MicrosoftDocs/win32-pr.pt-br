---
description: Para cada aplicativo que usa um repositório de política de autorização, você deve criar um objeto IAzApplication e, em seguida, salvá-lo em um repositório de políticas.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Criando um objeto de aplicativo no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a4852ef0c06d721f9409c000989895f6767eb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647648"
---
# <a name="creating-an-application-object-in-script"></a>Criando um objeto de aplicativo no script

Um repositório de diretivas de autorização contém informações de política de autorização para um ou mais aplicativos. Para cada aplicativo que usa um repositório de política de autorização, você deve criar um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvá-lo em um repositório de políticas.

O exemplo a seguir mostra como criar um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que representa um aplicativo e como adicionar o objeto **IAzApplication** ao armazenamento de política de autorização que o aplicativo usa. O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C.


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



 

 



