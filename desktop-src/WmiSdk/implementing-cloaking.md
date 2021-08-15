---
description: A redução é uma extensão para representação que permite um melhor controle sobre como o COM representa um cliente em um proxy. Assim como muitas formas de segurança WMI, você pode definir a desinformação por meio das interfaces CoSetProxyBlanket e CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementando a desaplicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d32333250bc37d8ccbfdb17421fed635f0da77e6394229220b2b36a1ce57f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318891"
---
# <a name="implementing-cloaking"></a>Implementando a desaplicação

A redução é uma extensão para representação que permite um melhor controle sobre como o COM representa um cliente em um proxy. Assim como muitas formas de segurança WMI, você pode definir a desinformação por meio das interfaces [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) e [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

O COM fornece as seguintes formas de proteção:

-   Estático

    COM estabelece a identidade do token pelo thread ou token de processo na primeira chamada para o proxy. Se você usar a responsabilidade estática com [**CoSetProxyBlanket,**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)definirá a identidade do proxy durante a vida útil do proxy.

-   Dinâmico

    O COM restabelece a identidade do token do thread ou do token de processo em cada chamada para o proxy. Como o COM verifica a identidade em cada chamada, a responsabilidade dinâmica permite um controle mais fino sobre a identidade do cliente. No entanto, a desastagem dinâmica é menos eficiente do que a desastagem estática.

Quando você definir a redução em conjunto com o nível de delegação de representação, um servidor poderá propagar a identidade de um cliente entre servidores, mesmo que os servidores sejam remotos. Se você não habilitar a desajuste, o COM fará qualquer chamada de um servidor local para um servidor remoto no contexto do processo de servidor real.

A união permite que o WMI represente um cliente para acessar recursos de rede locais e remotos em vários limites de computador. O WMI pode passar a identidade do cliente para servidores locais e remotos, como outras instâncias remotas do WMI. Esses servidores remotos podem executar operações no contexto inicial do cliente.

O procedimento a seguir descreve como usar a delegação e a reação juntos.

**Para usar a delegação e a reação juntos**

1.  De definir o serviço de autenticação como Kerberos.

    O Kerberos é o único serviço de autenticação que dá suporte à delegação e à reação remota. Isso significa que a delegação e a reação só podem ser usadas em servidores remotos.

2.  Marque a conta de logon do servidor como "Confiável para Delegação" nos serviços do Active Directory.
3.  Marque a conta de logon do cliente como "A conta é sensível e não pode ser delegada" nos serviços do Active Directory.

Por exemplo, uma chamada para o Provedor de Exibição, que pode retornar objetos de várias instâncias do WMI em vários computadores, pode se beneficiar da delegação e da delegação.

 

 
