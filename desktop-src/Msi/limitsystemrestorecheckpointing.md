---
description: essa política do sistema por máquina desativa a criação de pontos de verificação por Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbea03dcab5db690f6fc06725dbb38a376310e967b9e92a9fcb0c59daab0180
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763506"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

essa [política do sistema](system-policy.md) por máquina desativa a criação de pontos de verificação por Windows Installer.

Definido como 0 ou ausente, o instalador faz um ponto de verificação normal para instalação ou desinstalação. Definido como 1, o instalador não cria nenhum ponto de verificação.

essa política afeta somente os pontos de verificação definidos por Windows Installer. em computadores Windows XP, os administradores podem optar por desabilitar o ponto de verificação de dentro de Windows Installer para melhorar o desempenho. A [**restauração do sistema**](../sr/system-restore-portal.md) também cria pontos de verificação adicionais. para obter mais informações, consulte [pontos de restauração do sistema e o Windows Installer](system-restore-points-and-the-windows-installer.md) e [definindo um ponto de restauração de uma ação personalizada](setting-a-restore-point-from-a-custom-action.md).

## <a name="registry-key"></a>Chave do Registro

Defina o valor chamado LimitSystemRestoreCheckpointing na seguinte chave do registro.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ policies \\ Microsoft \\ Windows \\ Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 
