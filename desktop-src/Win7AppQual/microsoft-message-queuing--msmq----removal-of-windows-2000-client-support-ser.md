---
description: MSMQ (enfileiramento de mensagens da Microsoft)-remoção do serviço de suporte ao cliente do Windows 2000
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: MSMQ (enfileiramento de mensagens da Microsoft)-remoção do serviço de suporte ao cliente do Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be68d40271153567bdaf6b04d73218aaf3d3977
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088144"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>MSMQ (enfileiramento de mensagens da Microsoft)-remoção do serviço de suporte ao cliente do Windows 2000

## <a name="affected-platforms"></a>Plataformas afetadas

**Servidores** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -alta  
**Frequência** -baixa  

## <a name="description"></a>Descrição

O serviço de suporte ao cliente do Windows 2000 é um componente opcional do servidor de enfileiramento de mensagens que você pode instalar em um computador do controlador de domínio Windows 2003 ou Windows 2008. Esse serviço permite que os clientes do Windows 2000 operem em um modo integrado ao domínio com qualquer servidor de enfileiramento de mensagens instalado em computadores Windows 2003/2008. Os clientes MSMQ que operam no Windows XP para cima não precisam desse serviço.

### <a name="manifestation-of-impact"></a>Manifestação do impacto

Essa alteração afeta o Windows 2000 ao interoperar em um domínio do Windows 7 em que todos os controladores de domínio são Windows Server 2008 R2. Se um cliente atualizar para o domínio do Windows 7, os aplicativos MSMQ existentes em qualquer computador com Windows 2000 no domínio não poderão operar em um modo integrado ao domínio, a menos que esses clientes atualizem para uma versão superior do Windows.

### <a name="mitigation"></a>Atenuação

Os usuários que têm computadores cliente com Windows 2000 em um domínio do Windows 7 podem configurar um controlador de domínio do Windows 2003/2008 no domínio e instalar o serviço de suporte ao cliente MSMQ Windows 2000 nesse controlador de domínio.

### <a name="leveraging-feature-capabilities"></a>Aproveitando os recursos do recurso

Os usuários que têm computadores cliente com Windows 2000 executando o MSMQ devem atualizar para uma versão superior do Windows para aproveitar a implementação baseada em Active Directory do servidor MSMQ.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

Os usuários que têm computadores cliente com Windows 2000 executando o MSMQ em um domínio do Windows 7 com um ou mais controladores de domínio de nível inferior devem verificar se seus aplicativos estão funcionais nesse domínio misto.

 

 



