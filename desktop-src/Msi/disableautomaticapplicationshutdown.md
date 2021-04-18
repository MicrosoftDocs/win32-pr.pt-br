---
description: Se essa política do sistema por máquina for definida como 1 (uma), Windows Installer não interagirá com o Gerenciador de reinicialização, mas usará a caixa de diálogo FilesInUse. se essa política do sistema por máquina for definida como 2 (dois), Windows Installer usará a caixa de diálogo FilesInUse.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780515"
---
# <a name="disableautomaticapplicationshutdown"></a>DisableAutomaticApplicationShutdown

Se essa política do sistema por máquina for definida como 1 (uma), Windows Installer não irá interagir com o [Gerenciador de reinicialização](/windows/desktop/RstMgr/restart-manager-portal), mas usará a [caixa de diálogo FilesInUse](filesinuse-dialog.md).

Se essa política do sistema por máquina for definida como 2 (dois), Windows Installer usará a [caixa de diálogo FilesInUse](filesinuse-dialog.md). Essa configuração desabilita as tentativas do Gerenciador de [reinicialização](/windows/desktop/RstMgr/restart-manager-portal) para atenuar as reinicializações ao instalar um pacote de Windows Installer que não foi criado para usar o Gerenciador de reinicialização. O instalador ainda usa o Gerenciador de reinicialização para detectar arquivos em uso pelos aplicativos.

A política DisableAutomaticApplicationShutdown está disponível a partir do Windows Installer versão 4,0 no Windows Vista.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
