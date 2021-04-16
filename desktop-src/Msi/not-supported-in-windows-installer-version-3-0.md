---
description: O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer&\# 160; 3.0 e versões anteriores.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Sem suporte no Windows Installer 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787074"
---
# <a name="not-supported-in-windows-installer-30"></a>Sem suporte no Windows Installer 3,0

O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer 3,0 e versões anteriores. A ausência de um recurso dessa lista não garante que o recurso tenha suporte. Consulte a documentação principal para determinar qual versão de Windows Installer é necessária para um recurso específico. Para obter informações sobre outras versões do Windows Installer, consulte [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 3,0 está disponível para o Windows Server 2003, Windows XP ou Windows 2000. Para obter uma lista de todas as versões e redistribuíveis do Windows Installer, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

Os recursos a seguir não têm suporte no Windows Installer 3,0 e versões anteriores.

[Funções do instalador](installer-functions.md)

-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Protótipo de função de retorno de chamada

-   [**\_registro do manipulador INSTALLUI \_**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Tabelas de banco de dados](database-tables.md)

-   A coluna Value da [tabela MsiPatchMetadata](msipatchmetadata-table.md) aceita **OptimizedInstallMode** e **MinorUpdateTargetRTM**.

[Propriedades](properties.md)

-   [**Propriedade Msix64**](msix64.md)

[Windows Installer em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md)

-   A [**Propriedade Summary do modelo**](template-summary.md) aceita o valor x64.

[Avaliadores de consistência internos-ICEs](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
