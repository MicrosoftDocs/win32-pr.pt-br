---
description: A ação RegisterMIMEInfo registra informações de registro relacionadas a MIME com o sistema.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Ação RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662144"
---
# <a name="registermimeinfo-action"></a>Ação RegisterMIMEInfo

A ação RegisterMIMEInfo registra informações de registro relacionadas a MIME com o sistema.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RegisterMIMEInfo deve vir após a ação [InstallFiles](installfiles-action.md) , a ação [UnregisterMIMEInfo](unregistermimeinfo-action.md) , a ação [RegisterClassInfo](registerclassinfo-action.md) e a ação [RegisterExtensionInfo](registerextensioninfo-action.md) .

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   RegisterMIMEInfo

Por exemplo, RegisterMIMEInfo deve vir após [UnregisterMIMEInfo](unregistermimeinfo-action.md) na tabela de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                   |
|-------|----------------------------------------------|
| \[1\] | Identificador do tipo de conteúdo MIME registrado.  |
| \[2\] | Extensão associada ao tipo de conteúdo MIME. |



 

## <a name="remarks"></a>Comentários

A ação RegisterMIMEInfo registra todas as informações de MIME para servidores da [tabela MIME](mime-table.md) para as quais o servidor de classe ou servidor de extensão correspondente foi selecionado para instalação.

 

 



