---
title: Habilitando a segurança COM usando DCOMCNFG
description: Dcomcnfg.exe fornece uma interface do usuário para modificar certas configurações no Registro.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813227"
---
# <a name="enabling-com-security-using-dcomcnfg"></a>Habilitando a segurança COM usando DCOMCNFG

Dcomcnfg.exe fornece uma interface do usuário para modificar certas configurações no Registro. Usando Dcomcnfg.exe, você pode habilitar a segurança em todo o computador ou em todo o processo. Você pode habilitar a segurança para um computador específico para que, quando um processo não fornecer suas próprias configurações de segurança, seja de forma programática ou por meio de valores de registro, os valores definidos por Dcomcnfg.exe serão usados. Ou você pode usar Dcomcnfg.exe para habilitar a segurança apenas para um aplicativo específico.

Ao habilitar a segurança, há duas tarefas principais a serem realizadas:

-   Defina um nível de autenticação que não seja nenhum.
-   Defina permissões, incluindo as permissões de inicialização e de acesso.

As etapas executadas para realizar essas tarefas dependem se você está habilitando a segurança para todo o computador ou apenas para um determinado aplicativo. Além disso, talvez você queira definir outros valores para o computador ou aplicativo.

> [!Note]  
> Você deve ser um administrador para executar Dcomcnfg.exe.

 

Os tópicos a seguir fornecem procedimentos passo a passo sobre como definir a segurança com Dcomcnfg.exe:

-   [Definindo System-Wide segurança usando DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)
-   [Configurando a segurança do processwide usando DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> <dt>

[Desativando a segurança](turning-off-security.md)
</dt> </dl>

 

 




