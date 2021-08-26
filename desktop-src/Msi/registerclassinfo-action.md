---
description: A ação RegisterClassInfo gerencia o registro de informações de classe COM com o sistema. Ele usa a tabela AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Ação RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a0983b77c517cb2084b21d6d1500ec9b2a54b45d403c43f65bcc29505e2afe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912886"
---
# <a name="registerclassinfo-action"></a>Ação RegisterClassInfo

A ação RegisterClassInfo gerencia o registro de informações de classe COM com o sistema. Ele usa a [tabela AppId](appid-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RegisterClassInfo deve vir após a [ação InstallFiles](installfiles-action.md) e [a ação UnregisterClassInfo.](unregisterclassinfo-action.md)

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrerem juntos em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa, conforme mostrado:

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



| Campo | Descrição dos dados de ação                          |
|-------|-----------------------------------------------------|
| \[1\] | Identificador de classe GUID do servidor COM registrado. |



 

## <a name="remarks"></a>Comentários

Se o sistema dá suporte à instalação sob demanda para servidores OLE, RegisterClassInfo registra todas as classes COM na tabela Classe associada a um recurso selecionado para ser instalado ou anunciado. [](class-table.md) Caso contrário, essa ação registrará apenas as classes COM associadas a um recurso selecionado para instalação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedade OLEAdvtSupport**](oleadvtsupport.md)
</dt> </dl>

 

 



