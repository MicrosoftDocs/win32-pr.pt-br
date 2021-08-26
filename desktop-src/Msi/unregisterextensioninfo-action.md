---
description: A ação UnregisterExtensionInfo gerencia a remoção de informações relacionadas à extensão do registro do sistema.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Ação UnregisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8dae707bc4dd517402d8a85fb64402637a815f8249d4677f18818c855ba4e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810226"
---
# <a name="unregisterextensioninfo-action"></a>Ação UnregisterExtensionInfo

A ação UnregisterExtensionInfo gerencia a remoção de informações relacionadas à extensão do registro do sistema.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação UnregisterExtensionInfo deve vir após a ação [InstallInitialize](installinitialize-action.md) e antes da ação [RegisterExtensionInfo](registerextensioninfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) deve vir antes de UnregisterExtensionInfo na sequência.

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   UnregisterExtensionInfo
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por exemplo, UnregisterExtensionInfo deve vir antes de [UnregisterProgIdInfo](unregisterprogidinfo-action.md) na tabela de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Extensão removida.         |



 

## <a name="remarks"></a>Comentários

Se o sistema não oferecer suporte à instalação sob demanda de servidores de extensão, o UnregisterExtensionInfo removerá todos os servidores de extensão na [tabela de extensão](extension-table.md) associada a um recurso desinstalado ou a um recurso instalado como anunciado no registro. Caso contrário, essa ação removerá os servidores de extensão associados a um recurso selecionado para ser removido do registro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedade ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



