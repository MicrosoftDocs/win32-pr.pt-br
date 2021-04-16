---
description: A restauração do sistema monitora e registra automaticamente as principais alterações do sistema no computador de um usuário. Para obter mais informações, consulte restauração do sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Pontos de restauração do sistema e o Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782323"
---
# <a name="system-restore-points-and-the-windows-installer"></a>Pontos de restauração do sistema e o Windows Installer

A restauração do sistema monitora e registra automaticamente as principais alterações do sistema no computador de um usuário. Para obter mais informações, consulte [restauração do sistema](../sr/system-restore-portal.md).

Os pontos de restauração do sistema são criados pelo sistema e também são criados por Windows Installer quando o software é instalado ou removido.

No Windows XP, o instalador pode criar pontos de verificação durante a primeira instalação de um aplicativo e durante sua remoção. O instalador cria somente pontos de verificação nesses casos quando a alteração é executada com pelo menos uma [*interface do usuário básica*](b-gly.md). As instalações que têm o [nível de interface do usuário](user-interface-levels.md) definido como nenhum geralmente são iniciadas pelo sistema ou por um aplicativo que deve lidar com a criação de um ponto de verificação. Para obter mais informações, consulte [restauração do sistema](../sr/system-restore-portal.md).

Em corporações com muitos aplicativos pequenos, os administradores podem optar por desabilitar o ponto de verificação de dentro do instalador para melhorar o desempenho. Para obter mais informações, consulte [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) ou [definindo um ponto de restauração de uma ação personalizada](setting-a-restore-point-from-a-custom-action.md).

A partir do Windows Installer 5,0, a propriedade [**MSIFASTINSTALL**](msifastinstall.md) pode ser definida para impedir que uma instalação gere um ponto de restauração do sistema.

 

 
