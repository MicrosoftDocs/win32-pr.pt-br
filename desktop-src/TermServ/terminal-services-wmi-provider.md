---
title: Provedor WMI de Serviços de Área de Trabalho Remota
description: O provedor WMI de Serviços de Área de Trabalho Remota fornece acesso programático às informações e configurações que são expostas pelo snap-in do MMC (console de gerenciamento Microsoft) Serviços de Área de Trabalho Remota de configuração/conexões.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, provedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec4ed84dee9b2521c392b8b39ee1297121a85e1c4f8ad41f7d96d0d73042a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869596"
---
# <a name="remote-desktop-services-wmi-provider"></a>Provedor WMI de Serviços de Área de Trabalho Remota

O provedor WMI de Serviços de Área de Trabalho Remota fornece acesso programático às informações e configurações que são expostas pelo snap-in do MMC (console de gerenciamento Microsoft) Serviços de Área de Trabalho Remota de configuração/conexões.

a DLL do provedor é carregada pelo processo de gerenciamento de Windows (Winmgmt.exe) quando um cliente faz uma solicitação ao servidor. A administração é possível usando os métodos de provedor. O provedor é registrado como uma instância e um provedor de métodos.

O provedor WMI Serviços de Área de Trabalho Remota foi implementado como um provedor dinâmico derivado da classe base [**de \_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) , herdando todas as suas propriedades e métodos e uma biblioteca de vínculo dinâmico em processo.

Para obter mais informações, consulte a [referência do provedor WMI serviços de área de trabalho remota](terminal-services-wmi-provider-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços de Área de Trabalho Remota referência do provedor WMI](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 