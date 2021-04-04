---
title: Desabilitando recursos de Serviços de Área de Trabalho Remota
description: Para aumentar a segurança, você pode optar por desabilitar Serviços de Área de Trabalho Remota recursos.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/01/2020
ms.locfileid: "103917866"
---
# <a name="disabling-remote-desktop-services-features"></a>Desabilitando recursos de Serviços de Área de Trabalho Remota

Para aumentar a segurança, você pode optar por desabilitar Serviços de Área de Trabalho Remota recursos como redirecionamento de área de transferência e redirecionamento de impressora para clientes que se conectam a servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) usando o controle ActiveX Área de Trabalho Remota.

**Para desabilitar Serviços de Área de Trabalho Remota recursos**

1.  Edite o registro do computador cliente e adicione as seguintes chaves:

    -   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**
    -   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**
    -   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**

2.  Defina o valor de ambas as chaves para **reg \_ DWORD** 1.

 

 




