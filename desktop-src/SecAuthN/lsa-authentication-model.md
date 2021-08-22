---
description: Explica o modelo de autenticação LSA.
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: Modelo de autenticação LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762595332252c22141aebdc7f3ecbe168e49a83795830a0cb03e49eb5da73ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140939"
---
# <a name="lsa-authentication-model"></a>Modelo de autenticação LSA

O [*modelo de autenticação*](../secgloss/l-gly.md) da LSA (Autoridade de Segurança Local) tem os seguintes recursos:

-   A autenticação LSA dá suporte a pacotes [de autenticação personalizados](authentication-packages.md). Isso permite que os clientes finais e ISVs (fornecedores independentes de software) personalizem ou substituam rotinas de autenticação para atender aos requisitos além daqueles fornecidos pelos pacotes de autenticação padrão da Microsoft. Embora os pacotes de autenticação fornecidos pela Microsoft exigem um nome de usuário e dados de logon de senha, um pacote de autenticação personalizado pode assumir outras formas de dados de logon, como informações de cartão do ATM e um PIN (número de identificação pessoal). Um pacote de autenticação personalizado também pode ser usado para implementar um novo protocolo [*de segurança*](../secgloss/s-gly.md).
-   O LSA dá suporte a pacotes de segurança personalizados, que funcionam como provedores de suporte de segurança para aplicativos distribuídos e como pacotes de autenticação para aplicativos que exigem serviços de autenticação. A funcionalidade de autenticação é acessada usando a mesma interface que um pacote de autenticação autônomo, enquanto a funcionalidade do provedor de suporte de segurança é acessada usando o SSPI (Security [Support Provider Interface).](sspi.md) O conjunto de funções de suporte LSA disponíveis para pacotes de segurança personalizados permite que eles fornecem recursos avançados de segurança, como criação de tokens e gerenciamento [*de credenciais complementares.*](../secgloss/s-gly.md)
-   O LSA dá suporte ao gerenciamento de credenciais heterogêneas para interface com produtos que não são da Microsoft, como redes e bancos de dados. Como esses produtos geralmente têm suas próprias credenciais de segurança, a LSA fornece funções que os pacotes de autenticação podem usar para associar credenciais que não são da Microsoft a Windows processos. Os pacotes de autenticação personalizados podem fornecer serviços para consultar essas credenciais quando necessário, como quando um redirecionador de rede tenta estabelecer uma conexão com um sistema remoto.
-   Cada classe de dispositivo de logon instalado em um sistema pode ter seu próprio processo de logon. As classes de dispositivo normalmente incluem dispositivos como leitores de cartão inteligente; no entanto, para fins de [*autenticação LSA,*](../secgloss/l-gly.md) as redes conectadas também são tratadas como dispositivos. Por padrão, o Windows sistema operacional fornece o processo de logon que dá suporte a logons de nome de usuário e senha usando um teclado. Os desenvolvedores podem adicionar suporte para outros dispositivos, como [*leitores de cartão*](../secgloss/s-gly.md) [*inteligente*](../secgloss/r-gly.md). Para obter mais informações sobre cartões inteligentes, consulte [Autenticação de cartão inteligente](smart-card-authentication.md). Para obter mais informações sobre o suporte ao dispositivo de logon, [consulte Winlogon e LTD.](winlogon-and-gina.md)

 

 
