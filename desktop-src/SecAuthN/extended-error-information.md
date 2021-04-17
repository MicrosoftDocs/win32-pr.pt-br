---
description: Alguns pacotes de segurança dão suporte a mensagens de erro estendidas que permitem que os lados de um link de comunicação se comuniquem por qualquer motivo de falha.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Informações de erro estendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748874"
---
# <a name="extended-error-information"></a>Informações de erro estendidas

Alguns [*pacotes de segurança*](/windows/desktop/SecGloss/s-gly) dão suporte a mensagens de erro estendidas que permitem que os lados de um link de comunicação se comuniquem por qualquer motivo de falha. Por exemplo, o [*protocolo Kerberos*](/windows/desktop/SecGloss/k-gly) pode falhar devido a uma discrepância de tempo entre a hora da solicitação de um tíquete Kerberos e a hora do problema do tíquete. Com informações de informações de erro estendidas retornadas, um cliente pode ressincronizar seu relógio e gerar uma nova mensagem de conexão.

Um pacote de segurança que define \_ o \_ sinalizador de erro estendido do sinalizador SECPKG \_ no membro **FCapabilities** de uma estrutura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) indica que o pacote de segurança dá suporte a mensagens de erro estendidas.

Aplicativos cliente que exigem mensagens de erro estendidas especificam o sinalizador de erro estendido de solicitação de ISC \_ \_ \_ ao chamar a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Aplicativos de servidor que exigem mensagens de erro estendidas definem o \_ \_ sinalizador de erro estendido de ASC req \_ ao chamar [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).

 

 
