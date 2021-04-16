---
description: A ação RegisterProgIdInfo gerencia o registro de informações de ProgId de OLE com o sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Ação RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749987"
---
# <a name="registerprogidinfo-action"></a>Ação RegisterProgIdInfo

A ação RegisterProgIdInfo gerencia o registro de informações de ProgId de OLE com o sistema.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RegisterProgIdInfo deve vir após a ação [InstallFiles](installfiles-action.md) , a ação [UnregisterProgIdInfo](unregisterprogidinfo-action.md) , a ação [RegisterClassInfo](registerclassinfo-action.md) e a ação [RegisterExtensionInfo](registerextensioninfo-action.md) .

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   RegisterProgIdInfo
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por exemplo, RegisterProgIdInfo deve vir após [RegisterExtensionInfo](registerextensioninfo-action.md) na tabela de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                |
|-------|-------------------------------------------|
| \[1\] | Identificador de programa do programa registrado. |



 

## <a name="remarks"></a>Comentários

A ação RegisterProgIdInfo registra todas as informações de ProgId para servidores especificados na [tabela ProgID](progid-table.md) e para os quais o servidor de classe ou servidor de extensão correspondente foi selecionado para instalação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela de classes](class-table.md)
</dt> <dt>

[Tabela de extensão](extension-table.md)
</dt> </dl>

 

 



