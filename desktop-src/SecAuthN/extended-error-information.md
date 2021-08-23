---
description: Alguns pacotes de segurança dão suporte a mensagens de erro estendidas que permitem que os lados de um link de comunicação se comuniquem por qualquer motivo de falha.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Informações de erro estendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd93de1691a01802f65397abb1607612f5b7e61a311c9f801854a00c1ab4f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008214"
---
# <a name="extended-error-information"></a>Informações de erro estendidas

Alguns [*pacotes de segurança*](/windows/desktop/SecGloss/s-gly) dão suporte a mensagens de erro estendidas que permitem que os lados de um link de comunicação se comuniquem por qualquer motivo de falha. Por exemplo, o [*protocolo Kerberos*](/windows/desktop/SecGloss/k-gly) pode falhar devido a uma discrepância de tempo entre a hora da solicitação de um tíquete Kerberos e a hora do problema do tíquete. Com informações de informações de erro estendidas retornadas, um cliente pode ressincronizar seu relógio e gerar uma nova mensagem de conexão.

Um pacote de segurança que define \_ o \_ sinalizador de erro estendido do sinalizador SECPKG \_ no membro **FCapabilities** de uma estrutura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) indica que o pacote de segurança dá suporte a mensagens de erro estendidas.

Aplicativos cliente que exigem mensagens de erro estendidas especificam o sinalizador de erro estendido de solicitação de ISC \_ \_ \_ ao chamar a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Aplicativos de servidor que exigem mensagens de erro estendidas definem o \_ \_ sinalizador de erro estendido de ASC req \_ ao chamar [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).

 

 
