---
description: O encobrimento é uma extensão da representação que permite um melhor controle sobre como o COM representa um cliente em um proxy. Como muitas formas de segurança de WMI, você define o encobrimento por meio das interfaces CoSetProxyBlanket e CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementando o encobrimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170613"
---
# <a name="implementing-cloaking"></a>Implementando o encobrimento

O encobrimento é uma extensão da representação que permite um melhor controle sobre como o COM representa um cliente em um proxy. Como muitas formas de segurança de WMI, você define o encobrimento por meio das interfaces [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

COM fornece as seguintes formas de encobrimento:

-   Estático

    COM estabelece a identidade do token pelo thread ou token de processo na primeira chamada para o proxy. Se você usar o encobrimento estático com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), defina a identidade do proxy para a vida útil do proxy.

-   Dinâmico

    COM restabelece a identidade do token do thread ou do token de processo em cada chamada para o proxy. Como o COM verifica a identidade em cada chamada, o encobrimento dinâmico permite um controle mais preciso sobre a identidade do cliente. No entanto, o encobrimento dinâmico é menos eficiente do que o encobrimento estático.

Quando você define o encobrimento em conjunto com o nível de delegação de representação, um servidor pode propagar a identidade de um cliente entre servidores, mesmo que os servidores sejam remotos. Se você não habilitar o encobrimento, o COM fará qualquer chamada de um servidor local para um servidor remoto sob o contexto do processo do servidor real.

O encobrimento permite que o WMI represente um cliente para acessar recursos de rede locais e remotos entre vários limites de computador. O WMI pode passar a identidade do cliente para servidores locais e remotos, como outras instâncias remotas do WMI. Em seguida, esses servidores remotos podem executar operações no contexto inicial do cliente.

O procedimento a seguir descreve como usar o encobrimento e a delegação em conjunto.

**Para usar o encobrimento e a delegação em conjunto**

1.  Defina o serviço de autenticação como Kerberos.

    O Kerberos é o único serviço de autenticação que dá suporte ao encobrimento e à delegação remotas. Isso significa que o encobrimento e a delegação só podem ser usados em servidores remotos.

2.  Marque a conta de logon do servidor como "confiável para delegação" nos serviços de Active Directory.
3.  Marque a conta de logon do cliente como "a conta é confidencial e não pode ser delegada" em serviços Active Directorys.

Por exemplo, uma chamada para o provedor de exibição, que pode retornar objetos de várias instâncias do WMI em vários computadores, pode se beneficiar da delegação e do encobrimento.

 

 
