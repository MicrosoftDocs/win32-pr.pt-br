---
description: Explica o modelo de autenticação LSA.
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: Modelo de autenticação LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f5a44a20284a7285eb7fcffe1d1f8f6bf1f286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750200"
---
# <a name="lsa-authentication-model"></a>Modelo de autenticação LSA

O modelo de autenticação da [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) tem os seguintes recursos:

-   A autenticação LSA dá suporte a [pacotes de autenticação](authentication-packages.md)personalizados. Isso permite que os clientes finais e ISVs (fornecedores de software independentes) personalizem ou substituam rotinas de autenticação para atender aos requisitos além daqueles fornecidos pelos pacotes de autenticação padrão da Microsoft. Embora os pacotes de autenticação fornecidos pela Microsoft exijam um nome de usuário e dados de logon de senha, um pacote de autenticação personalizado pode usar outras formas de dados de logon, como informações de placa ATM e um PIN (número de identificação pessoal). Um pacote de autenticação personalizado também pode ser usado para implementar um novo [*protocolo de segurança*](../secgloss/s-gly.md).
-   O LSA dá suporte a pacotes de segurança personalizados, que funcionam como provedores de suporte de segurança para aplicativos distribuídos e como pacotes de autenticação para aplicativos que exigem serviços de autenticação. A funcionalidade de autenticação é acessada usando a mesma interface que um pacote de autenticação autônomo, enquanto a funcionalidade do provedor de suporte de segurança é acessada usando a [interface de provedor de suporte de segurança](sspi.md) (SSPI). O conjunto de funções de suporte LSA disponíveis para pacotes de segurança personalizados permite que eles forneçam recursos de segurança avançados, como a criação de tokens e o gerenciamento de [*credenciais complementares*](../secgloss/s-gly.md) .
-   O LSA oferece suporte ao gerenciamento de credenciais heterogêneas para a interface com produtos que não são da Microsoft, como redes e bancos de dados. Como esses produtos geralmente têm suas próprias credenciais de segurança, a LSA fornece funções que os pacotes de autenticação podem usar para associar credenciais não Microsoft a processos do Windows. Os pacotes de autenticação personalizados podem fornecer serviços para consultar essas credenciais quando necessário, como quando um redirecionador de rede tenta estabelecer uma conexão com um sistema remoto.
-   Cada classe de dispositivo de logon instalada em um sistema pode ter seu próprio processo de logon. As classes de dispositivo normalmente incluem dispositivos como leitores de cartão inteligente; no entanto, para fins de autenticação [*LSA*](../secgloss/l-gly.md) , as redes conectadas também são tratadas como dispositivos. Por padrão, o sistema operacional Windows fornece o processo de logon que dá suporte a logons de nome de usuário e senha usando um teclado. Os desenvolvedores podem adicionar suporte para outros dispositivos, como [*leitores*](../secgloss/r-gly.md)de [*cartão inteligente*](../secgloss/s-gly.md) . Para obter mais informações sobre cartões inteligentes, consulte [autenticação de cartão inteligente](smart-card-authentication.md). Para obter mais informações sobre o suporte a dispositivos de logon, consulte [Winlogon e Gina](winlogon-and-gina.md).

 

 
