---
title: Modificar o padrão de redirecionamento de dispositivo
description: Como Área de Trabalho Remota gateways tentam impor políticas de redirecionamento de dispositivo seguras antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota, talvez seja necessário desabilitar esse padrão em alguns casos.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b74515f6bf79b42c129ec7c113729b9871d4e4bfb0101f845f91dcac0d49237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138160"
---
# <a name="modify-device-redirection-default"></a>Modificar o padrão de redirecionamento de dispositivo

Como Área de Trabalho Remota gateways tentam impor políticas de redirecionamento de dispositivo seguras antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota, talvez seja necessário desabilitar esse padrão em alguns casos.

No Windows Server 2008 R2 e posterior, os servidores do Gateway do Área de Trabalho Remota tentarão impor políticas de redirecionamento de dispositivo seguras antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota segurança. No entanto, esse recurso não é suportado por alguns servidores. Por exemplo, isso não tem suporte para conexões com sessões de console do Hyper-V e pode ser necessário desabilitar o padrão para dar suporte à autenticação federada. Nesses casos, esse recurso pode ser desabilitado criando a seguinte chave do Registro para permitir que as conexões sejam feitas.

**HKEY \_ LOCAL MACHINE Software Microsoft Terminal Server Gateway \_ \\ \\ \\ \\ preRDPDisableRegKey**

Quando essa chave existir, o gateway Área de Trabalho Remota não imporá o redirecionamento de dispositivo.

 

 




