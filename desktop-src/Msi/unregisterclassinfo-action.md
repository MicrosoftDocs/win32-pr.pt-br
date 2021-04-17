---
description: A ação UnregisterClassInfo gerencia a remoção de informações de classe COM do registro do sistema. Ele usa a tabela AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Ação UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748135"
---
# <a name="unregisterclassinfo-action"></a>Ação UnregisterClassInfo

A ação UnregisterClassInfo gerencia a remoção de informações de classe COM do registro do sistema. Ele usa a [tabela AppID](appid-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação UnregisterClassInfo deve vir após a ação [InstallInitialize](installinitialize-action.md) e antes da ação [RegisterClassInfo](registerclassinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) deve vir antes de UnregisterClassInfo na sequência.

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, elas deverão ocorrer na mesma sequência relativa, conforme mostrado na tabela a seguir:

-   UnregisterClassInfo
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por exemplo, [RegisterExtensionInfo](registerextensioninfo-action.md) deve vir antes de UnregisterClassInfo na tabela de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação      |
|-------|---------------------------------|
| \[1\] | GUID da classe COM não registrada. |



 

## <a name="remarks"></a>Comentários

O instalador define a propriedade [**OLEAdvtSupport**](oleadvtsupport.md) como true quando o sistema do usuário atual foi atualizado para funcionar com a instalação sob demanda por meio de com. Se o sistema não oferecer suporte à instalação sob demanda por meio de COM, o UnregisterClassInfo removerá todas as classes COM listadas na [tabela de classes](class-table.md) associada a recursos ou recursos desinstalados instalados como anunciados no registro do sistema. Caso contrário, essa ação remove apenas as classes COM associadas a recursos selecionados a serem desinstalados do registro do sistema.

 

 



