---
description: O WoW64 agora é um recurso opcional para o Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Status do WoW64 no Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084044"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>O WoW64 agora é um recurso opcional para o Server Core

## <a name="affected-platforms"></a>Plataformas afetadas

**Servidores** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

A opção de instalação Server Core para o Windows Server 2008 R2 permite que você desinstale o WoW64. O WoW64 agora é um recurso opcional que você pode desinstalar se não for necessário executar o código de 32 bits.

Além disso, as funções Active Directory e serviços AD LDS exigem o WoW64 para serem executadas no Windows Server 2008 R2.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

Se você desinstalar o WoW64, os administradores que executam o código de 32 bits no Server Core receberão uma mensagem de erro informando que o aplicativo não pode ser executado. Se os administradores tentarem executar Active Directory e serviços AD LDS, eles receberão uma mensagem de erro.

## <a name="mitigation"></a>Atenuação

Instale o WoW64.

## <a name="solution"></a>Solução

A solução preferida é fornecer uma versão de 64 bits do código para permitir que ele seja executado no Server Core sem precisar do WoW64.

No mínimo, forneça a documentação do usuário indicando que, para executar o código de 32 bits, eles devem instalar o WoW64.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

Verifique se todo o código usado é de 64 bits.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Detalhes da implementação do WOW64](../winprog64/wow64-implementation-details.md)
-   [Depurando WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
