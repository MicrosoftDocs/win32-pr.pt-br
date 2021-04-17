---
description: Essa política do sistema por máquina desativa a criação de pontos de verificação por Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770193"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

Essa [política do sistema](system-policy.md) por máquina desativa a criação de pontos de verificação por Windows Installer.

Definido como 0 ou ausente, o instalador faz um ponto de verificação normal para instalação ou desinstalação. Definido como 1, o instalador não cria nenhum ponto de verificação.

Essa política afeta somente os pontos de verificação definidos por Windows Installer. Em computadores com Windows XP, os administradores podem optar por desabilitar o ponto de verificação no Windows Installer para melhorar o desempenho. A [**restauração do sistema**](../sr/system-restore-portal.md) também cria pontos de verificação adicionais. Para obter mais informações, consulte [pontos de restauração do sistema e o Windows Installer](system-restore-points-and-the-windows-installer.md) e [definindo um ponto de restauração de uma ação personalizada](setting-a-restore-point-from-a-custom-action.md).

## <a name="registry-key"></a>Chave do Registro

Defina o valor chamado LimitSystemRestoreCheckpointing na seguinte chave do registro.

**HKEY \_ local \_ Machine \\ software \\ Policies \\ Microsoft \\ Windows \\ Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 
