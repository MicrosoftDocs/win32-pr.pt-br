---
description: A ação UnregisterMIMEInfo cancela o registro das informações do registro relacionadas a MIME do sistema. A ação cancela o registro de informações de MIME para servidores da tabela MIME para a qual o recurso correspondente está selecionado no momento para ser desinstalado.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Ação UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e03ea1c50aa543615edc0ed875bd83b3338cdb261d09e01232e0fe76f7aa51ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810136"
---
# <a name="unregistermimeinfo-action"></a>Ação UnregisterMIMEInfo

A ação UnregisterMIMEInfo cancela o registro das informações do registro relacionadas a MIME do sistema. A ação cancela o registro de informações de MIME para servidores da [tabela MIME](mime-table.md) para a qual o recurso correspondente está selecionado no momento para ser desinstalado.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação UnregisterMIMEInfo deve vir após a ação [InstallInitialize](installinitialize-action.md) , a ação [UnregisterClassInfo](unregisterclassinfo-action.md) , a ação [UnregisterExtensionInfo](unregisterextensioninfo-action.md) e antes da ação [RegisterMIMEInfo](registermimeinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) deve vir antes de UnregisterMIMEInfo na sequência.

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   UnregisterMIMEInfo
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por exemplo, UnregisterMIMEInfo deve vir antes de [RegisterExtensionInfo](registerextensioninfo-action.md) na tabela de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador do tipo de conteúdo MIME não registrado. |
| \[2\] | Extensão associada ao tipo de conteúdo MIME.  |



 

 

 



