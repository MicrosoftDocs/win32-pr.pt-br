---
description: Restauração do Sistema monitora e registra automaticamente as principais alterações do sistema no computador do usuário. Para obter mais informações, consulte Restauração do Sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Restauração do Sistema pontos e o instalador Windows aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b8de832208f2bee301a1a159da058ba0f97cf2ecbd74892cb809e1186fbb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624085"
---
# <a name="system-restore-points-and-the-windows-installer"></a>Restauração do Sistema pontos e o instalador Windows aplicativo

Restauração do Sistema monitora e registra automaticamente as principais alterações do sistema no computador do usuário. Para obter mais informações, [consulte Restauração do Sistema](../sr/system-restore-portal.md).

Os pontos de restauração do sistema são criados pelo sistema e também são criados Windows Instalador quando o software é instalado ou removido.

No Windows XP, o instalador pode criar pontos de verificação durante a primeira instalação de um aplicativo e durante sua remoção. O instalador só cria pontos de verificação nesses casos quando a alteração é executado com pelo menos uma [*interface do usuário básica.*](b-gly.md) As instalações que têm [o nível de interface do](user-interface-levels.md) usuário definido como Nenhum geralmente são iniciadas pelo sistema ou por um aplicativo que deve lidar com a criação de um ponto de verificação. Para obter mais informações, [consulte Restauração do Sistema](../sr/system-restore-portal.md).

Em empresas com muitos aplicativos pequenos, os administradores podem optar por desabilitar o ponto de verificação de dentro do instalador para melhorar o desempenho. Para obter mais informações, [consulte LimitSystemRestoreCheckpointing ou](limitsystemrestorecheckpointing.md) [Configurando um ponto de restauração de uma ação personalizada](setting-a-restore-point-from-a-custom-action.md).

A partir do Windows 5.0, a propriedade [**MSIFASTINSTALL**](msifastinstall.md) pode ser definida para impedir que uma instalação gere um ponto de restauração do sistema.

 

 
