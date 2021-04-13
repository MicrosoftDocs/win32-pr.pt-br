---
description: Normalmente, um MSP (provedor de serviços de mídia) implementa a criação de terminal.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Gravando um terminal conectável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501908"
---
# <a name="writing-a-pluggable-terminal"></a>Gravando um terminal conectável

Normalmente, um MSP (provedor de serviços de mídia) implementa a criação de terminal. A partir do Windows 2000 SP1, a TAPI 3 inclui terminais conectáveis para permitir que um aplicativo implemente a criação de terminal. Consulte a visão geral sobre como [implementar terminais conectáveis](implementing-pluggable-terminals.md) para obter informações adicionais sobre como usar esses terminais.

Você não deve usar os terminais conectáveis rotineiramente porque os recursos completos de um terminal só estarão disponíveis quando um MSP estiver totalmente ciente dele. Além disso, você não deve tentar implementar terminais conectáveis, a menos que já esteja familiarizado com a gravação de provedores de serviços de mídia. As técnicas e os possíveis problemas envolvidos são bastante semelhantes.

A provisão para um caso especial de terminal conectável existe atualmente para a situação de um servidor de conferência que precisa adicionar clientes não Windows 2000 SP1 ou não multicast H. 323 a conferências de multicast/IP multipartes de antivírus 3.

 

 



