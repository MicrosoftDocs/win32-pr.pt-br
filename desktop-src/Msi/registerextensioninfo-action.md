---
description: A ação RegisterExtensionInfo gerencia o registro de informações relacionadas à extensão com o sistema.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Ação RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0541fc512c2300b0cb37f4a23305a3d312a4e60208890507fb7c6112e00c94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519376"
---
# <a name="registerextensioninfo-action"></a>Ação RegisterExtensionInfo

A ação RegisterExtensionInfo gerencia o registro de informações relacionadas à extensão com o sistema.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RegisterExtensionInfo deve vir após a ação [InstallFiles](installfiles-action.md) e a ação [UnregisterExtensionInfo](unregisterextensioninfo-action.md) .

O sequenciamento das ações no grupo a seguir é restrito. Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   RegisterExtensionInfo
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por exemplo, RegisterExtensionInfo deve vir após [UnregisterMIMEInfo](unregistermimeinfo-action.md) na tabela de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Extensão registrada.      |



 

## <a name="remarks"></a>Comentários

Se o sistema oferecer suporte à instalação sob demanda para servidores de extensão, o RegisterExtensionInfo registrará todos os servidores de extensão na [tabela de extensão](extension-table.md) associada aos recursos definidos para instalação ou anúncio. Caso contrário, essa ação registra somente os servidores de extensão associados aos recursos definidos como instalação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedade ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



