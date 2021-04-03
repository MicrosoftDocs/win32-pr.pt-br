---
description: A ação UnregisterComPlus remove aplicativos COM+ do registro.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Ação UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922899"
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

[Instalando um aplicativo COM+ com o Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



