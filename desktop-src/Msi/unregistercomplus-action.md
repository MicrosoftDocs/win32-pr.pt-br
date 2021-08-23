---
description: A ação UnregisterComPlus remove aplicativos COM+ do registro.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Ação UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc3ed5e8e4afd853294e7f5832662e9aaf1eb122d3573e7c384115c86d994588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499846"
---
# <a name="unregistercomplus-action"></a>Ação UnregisterComPlus

A ação UnregisterComPlus remove aplicativos COM+ do registro.

## <a name="sequence-restrictions"></a>Restrições de sequência

A [ação RegisterComPlus](registercomplus-action.md) deve seguir a [ação InstallFiles](installfiles-action.md) e a ação UnregisterComPlus.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Identificador de aplicativo do aplicativo COM+ que está sendo removido. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ação RegisterComPlus](registercomplus-action.md)
</dt> <dt>

[Tabela ComPlus](complus-table.md)
</dt> <dt>

[instalando um aplicativo COM+ com o Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



