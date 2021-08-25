---
description: A ação RegisterProgIdInfo gerencia o registro de informações do OLE ProgId com o sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Ação RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cebf5ddb3bf8b9c98ebea0364b685016d343afa283b937400360f31bbcebd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912826"
---
# <a name="registerprogidinfo-action"></a>Ação RegisterProgIdInfo

A ação RegisterProgIdInfo gerencia o registro de informações do OLE ProgId com o sistema.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RegisterProgIdInfo deve vir após a ação [InstallFiles,](installfiles-action.md) a ação [UnregisterProgIdInfo,](unregisterprogidinfo-action.md) a ação [RegisterClassInfo](registerclassinfo-action.md) e a [ação RegisterExtensionInfo.](registerextensioninfo-action.md)

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrerem juntos em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa, conforme mostrado:

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



| Campo | Descrição dos dados de ação                |
|-------|-------------------------------------------|
| \[1\] | Identificador do programa registrado. |



 

## <a name="remarks"></a>Comentários

A ação RegisterProgIdInfo registra todas as informações de ProgId para servidores especificados na tabela [ProgId](progid-table.md) e para os quais o servidor de classe ou servidor de extensão correspondente foi selecionado para ser instalado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela de classes](class-table.md)
</dt> <dt>

[Tabela de extensão](extension-table.md)
</dt> </dl>

 

 



