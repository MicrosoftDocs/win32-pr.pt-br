---
title: Usando Serviços de Área de Trabalho Remota canais virtuais
description: Para implementar um canal virtual, você fornece os módulos de servidor e cliente do aplicativo de um canal virtual.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f538259134d539104e55706578778931a1180a1901a9891eec7f62f1f40144b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423736"
---
# <a name="using-remote-desktop-services-virtual-channels"></a>Usando Serviços de Área de Trabalho Remota canais virtuais

Para implementar um canal virtual, você fornece os módulos de servidor e cliente do aplicativo de um canal virtual. O módulo do servidor pode ser um aplicativo de modo de usuário ou um driver de modo kernel. O módulo cliente deve ser uma DLL.

Para ver descrições desses módulos, consulte os tópicos a seguir.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Aplicativo de Servidor de Canal Virtual](virtual-channel-server-application.md)
</dt> <dd>

O módulo de servidor de um aplicativo que usa canais virtuais deve ser um aplicativo de modo de usuário em execução em uma sessão de cliente no servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Observe que você deve fornecer um método para iniciar o aplicativo de servidor.

</dd> <dt>

[DLL do cliente de canal virtual](virtual-channel-client-dll.md)
</dt> <dd>

O cliente de um aplicativo de canais virtuais é uma DLL carregada durante a Serviços de Área de Trabalho Remota inicialização no computador cliente. A DLL deve ser registrada no computador cliente.

</dd> <dt>

[Registro de cliente de canal virtual](virtual-channel-client-registration.md)
</dt> <dd>

Você deve armazenar o nome da DLL do cliente no Registro.

</dd> <dt>

[Canais virtuais persistentes de controle remoto](remote-control-persistent-virtual-channels.md)
</dt> <dd>

Um canal virtual persistente de controle remoto não é fechado quando um controle remoto se conecta ou se desconecta para a sessão conectada ao cliente. Os dados continuarão a ser transmitidos e recebidos por meio desse canal.

</dd> <dt>

[Canais Virtuais Dinâmicos](dynamic-virtual-channels.md)
</dt> <dd>

AS APIs de canal virtual dinâmico (DVC) estendem as APIs de canal virtual existentes para Serviços de Área de Trabalho Remota, conhecidas como APIs de canal virtual estático (SVC).

</dd> </dl>

Se você habilitar o aplicativo de um canal virtual em sua implantação do Serviços de Área de Trabalho Remota, também poderá disponibilizar o aplicativo para computadores cliente que acessam o servidor Host da Sessão RD por meio do controle Área de Trabalho Remota ActiveX. Para obter mais informações, [consulte Usando o controle Área de Trabalho Remota ActiveX com canais virtuais](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




