---
title: Endereços IP e nomes de computador
description: Não é seguro pressupor que o nome do computador ou o endereço IP atribuído ao computador está associados um único usuário, pois vários usuários podem ser conectados simultaneamente a um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294413"
---
# <a name="ip-addresses-and-computer-names"></a>Endereços IP e nomes de computador

Vários usuários podem ser conectados simultaneamente a um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Consequentemente, não é seguro supor que o nome do computador ou o endereço IP atribuído ao computador estejam associados a um único usuário. Isso é diferente de um ambiente Windows de usuário único, no qual apenas um usuário está conectado por vez.

Os aplicativos que usam o nome do computador ou endereço IP para licenciamento ou como um meio de identificar uma iteração do aplicativo na rede não funcionarão corretamente em um ambiente Serviços de Área de Trabalho Remota, pois o nome do computador ou o endereço IP do servidor pode ser associado a muitos usuários.

Em um ambiente de Serviços de Área de Trabalho Remota, cada terminal de cliente ou emulador de terminal tem um endereço IP e um nome de computador separados. Para recuperar o endereço IP e o nome do computador de um cliente, chame a função [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) . Outras funções que recuperam esses endereços de rede e nomes de computador recuperam o nome e o endereço do servidor de Host da Sessão RD. Por exemplo, a função [**GetComputerNameEx devia**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) retorna o nome do computador do servidor.

 

 