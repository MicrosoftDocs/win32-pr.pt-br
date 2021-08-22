---
title: Desabilitando recursos de Serviços de Área de Trabalho Remota
description: Para aumentar a segurança, você pode optar por desabilitar Serviços de Área de Trabalho Remota recursos.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e994999293a23468da78724fdcec8b09f3be4a5f814b4e805923f1bff469267d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401346"
---
# <a name="disabling-remote-desktop-services-features"></a>Desabilitando recursos de Serviços de Área de Trabalho Remota

para aumentar a segurança, você pode optar por desabilitar Serviços de Área de Trabalho Remota recursos como redirecionamento de área de transferência e redirecionamento de impressora para clientes que se conectam a servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) usando o controle Área de Trabalho Remota ActiveX.

**Para desabilitar Serviços de Área de Trabalho Remota recursos**

1.  Edite o registro do computador cliente e adicione as seguintes chaves:

    -   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**
    -   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**
    -   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**

2.  Defina o valor de ambas as chaves para **reg \_ DWORD** 1.

 

 




