---
description: As funções, tabelas e propriedades do instalador Windows Windows listadas nesta página não têm suporte do Windows Installer&\# 160;3.0 e versões anteriores.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Sem suporte no Windows 3.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b4211433762c68ed39af012d895d65aeee8fdc5a17f1e6142df76fcbe056c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926296"
---
# <a name="not-supported-in-windows-installer-30"></a>Sem suporte no Windows 3.0

As Windows, as tabelas e as propriedades listadas nesta página não são suportadas pelo Windows Installer 3.0 e versões anteriores. A ausência de um recurso dessa lista não garante que o recurso seja suportado. Consulte a documentação principal para determinar qual Windows do Instalador é necessária para um recurso específico. Para obter informações sobre Windows versões do Instalador do [Windows .](what-s-new-in-windows-installer.md)

Windows O Instalador 3.0 está disponível para Windows Server 2003, Windows XP ou Windows 2000. Para ver uma lista de todas as Windows instalador e redistribuíveis, consulte Versões lançadas [do Windows Installer](released-versions-of-windows-installer.md).

Os recursos a seguir não têm suporte no Windows Instalador 3.0 e versões anteriores.

[Funções do instalador](installer-functions.md)

-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Protótipo de função de retorno de chamada

-   [**REGISTRO DO MANIPULADOR \_ \_ INSTALLUI**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Tabelas de banco de dados](database-tables.md)

-   A coluna Valor da [Tabela MsiPatchMetadata](msipatchmetadata-table.md) aceita **OptimizedInstallMode** e **MinorUpdateTargetRTM**.

[Propriedades](properties.md)

-   [**Propriedade Msix64**](msix64.md)

[Windows Instalador em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md)

-   A [**propriedade Resumo do Modelo**](template-summary.md) aceita o valor x64.

[Avaliadores de consistência interna – ICEs](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
