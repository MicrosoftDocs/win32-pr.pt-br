---
description: A ação UnregisterProgIdInfo gerencia o cancelamento do registro de informações de ProgId do OLE com o sistema.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Ação UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6666e5648cba220dbb9bbc6e2d50c3959c1d73c98f97dcfd8c45cb3de8d94c82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786956"
---
# <a name="unregisterprogidinfo-action"></a>Ação UnregisterProgIdInfo

A ação UnregisterProgIdInfo gerencia o cancelamento do registro de informações de ProgId do OLE com o sistema.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação UnregisterProgIdInfo deve vir após a ação [InstallInitialize](installinitialize-action.md) , a ação [UnregisterClassInfo](unregisterclassinfo-action.md) , a ação [UnregisterExtensioninfo](unregisterextensioninfo-action.md) e antes da ação [RegisterProgIdInfo](registerprogidinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) deve vir antes de UnregisterProgIdInfo na sequência.

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensioninfo](unregisterextensioninfo-action.md)
-   UnregisterProgIdInfo
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por exemplo, UnregisterProgIdInfo deve vir antes de [UnregisterMIMEInfo](unregistermimeinfo-action.md) na tabela de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                |
|-------|-------------------------------------------|
| \[1\] | Identificador de programa do programa registrado. |



 

## <a name="remarks"></a>Comentários

A ação UnregisterProgIdInfo remove informações de ProgId do registro ([tabela ProgID](progid-table.md)) para os recursos que estão conectados às informações de extensão ([tabela de extensão](extension-table.md)) ou as informações de classe (tabela de[classe](class-table.md)) e estão selecionadas para serem desinstaladas no momento.

 

 



