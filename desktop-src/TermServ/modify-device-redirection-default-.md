---
title: Modificar o padrão de redirecionamento de dispositivo
description: Como Área de Trabalho Remota servidores de gateway tentam impor políticas de redirecionamento de dispositivo seguro antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota, talvez seja necessário desabilitar esse padrão em alguns casos.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822706"
---
# <a name="modify-device-redirection-default"></a>Modificar o padrão de redirecionamento de dispositivo

Como Área de Trabalho Remota servidores de gateway tentam impor políticas de redirecionamento de dispositivo seguro antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota, talvez seja necessário desabilitar esse padrão em alguns casos.

No Windows Server 2008 R2 e posterior, Área de Trabalho Remota servidores de gateway, por padrão, tentam impor políticas de redirecionamento de dispositivo seguro antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota. No entanto, esse recurso não tem suporte em alguns servidores. Por exemplo, isso não tem suporte para conexões com sessões de console do Hyper-V e pode ser necessário desabilitar o padrão para dar suporte à autenticação federada. Nesses casos, esse recurso pode ser desabilitado com a criação da seguinte chave do registro para permitir que as conexões passem.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server gateway \\ preRDPDisableRegKey**

Quando essa chave existir, o gateway de Área de Trabalho Remota não impedirá o redirecionamento de dispositivo.

 

 




