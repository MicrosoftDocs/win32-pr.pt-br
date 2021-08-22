---
description: MSMQ (enfileiramento de mensagens da Microsoft)-remoção do serviço de suporte ao cliente do Windows 2000
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: MSMQ (enfileiramento de mensagens da Microsoft)-remoção do serviço de suporte ao cliente do Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bdcba684faa0a25994f66cc9cd205ba22b5ed949d8dcdd3e67497484f2784ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053044"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>MSMQ (enfileiramento de mensagens da Microsoft)-remoção do serviço de suporte ao cliente do Windows 2000

## <a name="affected-platforms"></a>Plataformas afetadas

**servidores** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -alta  
**Frequência** -baixa  

## <a name="description"></a>Descrição

o serviço de suporte ao cliente do Windows 2000 é um componente opcional do servidor de enfileiramento de mensagens que você pode instalar em um computador do controlador de domínio Windows 2003 ou Windows 2008. esse serviço permite que Windows clientes 2000 operem em um modo integrado ao domínio com qualquer servidor de enfileiramento de mensagens instalado em computadores Windows 2003/2008. os clientes MSMQ que operam no Windows XP para cima não precisam desse serviço.

### <a name="manifestation-of-impact"></a>Manifestação do impacto

essa alteração afeta Windows 2000 ao interoperar em um domínio Windows 7 em que todos os controladores de domínio são Windows Server 2008 R2. se um cliente atualizar para o domínio Windows 7, os aplicativos MSMQ existentes em qualquer Windows computadores 2000 no domínio não poderão operar em um modo integrado ao domínio, a menos que esses clientes atualizem para uma versão de Windows superior.

### <a name="mitigation"></a>Atenuação

os usuários que têm Windows computadores cliente 2000 em um domínio Windows 7 podem configurar um controlador de domínio Windows 2003/2008 no domínio e instalar o serviço de suporte ao cliente do MSMQ Windows 2000 nesse controlador de domínio.

### <a name="leveraging-feature-capabilities"></a>Aproveitando os recursos do recurso

os usuários que têm Windows computadores cliente 2000 executando o MSMQ devem ser atualizados para uma versão mais alta do Windows para aproveitar a implementação baseada em Active Directory do servidor MSMQ.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

os usuários que têm Windows computadores cliente 2000 executando o MSMQ em um domínio Windows 7 com um ou mais controladores de domínio de nível inferior devem verificar se seus aplicativos estão funcionando nesse domínio misto.

 

 



