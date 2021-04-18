---
description: A ação RegisterClassInfo gerencia o registro de informações de classe com com o sistema. Ele usa a tabela AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Ação RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759208"
---
# <a name="registerclassinfo-action"></a>Ação RegisterClassInfo

A ação RegisterClassInfo gerencia o registro de informações de classe com com o sistema. Ele usa a [tabela AppID](appid-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RegisterClassInfo deve vir após a ação [InstallFiles](installfiles-action.md) e a ação [UnregisterClassInfo](unregisterclassinfo-action.md) .

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por exemplo, RegisterClassInfo deve vir após [UnregisterMIMEInfo](unregistermimeinfo-action.md) na tabela de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                          |
|-------|-----------------------------------------------------|
| \[1\] | Identificador de classe de GUID do servidor COM registrado. |



 

## <a name="remarks"></a>Comentários

Se o sistema oferecer suporte à instalação sob demanda para servidores OLE, o RegisterClassInfo registrará todas as classes COM na [tabela de classes](class-table.md) associada a um recurso selecionado a ser instalado ou anunciado. Caso contrário, essa ação registra apenas as classes COM associadas a um recurso selecionado para instalação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedade OLEAdvtSupport**](oleadvtsupport.md)
</dt> </dl>

 

 



