---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-cadeia de caracteres do agente do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be481cf409468d9d182d37ae7636b167bc71d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828815"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8-cadeia de caracteres do agente do usuário

## <a name="affected-platforms"></a>Plataformas afetadas

 **Clientes** -Windows XP Windows \| Vista Windows \| 7  
**Servidores** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -média  
**Frequência** -alta  











## <a name="description"></a>Descrição

A cadeia de caracteres do agente do usuário é o identificador do Internet Explorer que fornece dados sobre sua versão e outros atributos para servidores Web. Muitos aplicativos Web dependem e se acumulam na cadeia de caracteres do agente do usuário do IE. Os que fazem isso e dependem de um número de versão anterior serão afetados. A cadeia de caracteres do agente do usuário agora inclui a cadeia de caracteres "Trident/4.0" para permitir a diferenciação entre a cadeia de caracteres do agente do usuário do Internet Explorer 7 e a cadeia de caracteres do agente do usuário do Internet Explorer 8 ao executar na exibição de compatibilidade do Internet Explorer 7. Consulte Noções básicas sobre cadeias de agente do usuário para obter detalhes.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

Há duas áreas afetadas:

-   As páginas da Web que verificam explicitamente a cadeia de caracteres do agente do usuário e não dão suporte à cadeia de caracteres do agente do usuário do Internet Explorer 8 podem não ser executadas corretamente. Na maioria dos casos, isso significa que as páginas serão bloquear os usuários do conteúdo que estão tentando acessar ou exibir conteúdo incorreto ou malformado.
-   Os aplicativos que hospedam o Trident (consulte hospedagem e reutilização) serão padronizados para o Internet Explorer 7 usando o componente opcional da Web, mas não terão acesso aos recursos do Internet Explorer 8.

## <a name="solution"></a>Solução

Verifique se seus aplicativos manipulam corretamente a nova versão ' MSIE 8,0 ' na cadeia de caracteres do agente do usuário. Você também pode optar pelo modo de exibição de compatibilidade do Internet Explorer 7 para esses aplicativos com base no Internet Explorer 7. Isso pode ser feito com marcas meta. Consulte a discussão em Noções básicas sobre cadeias de caracteres do agente do usuário para obter detalhes.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

-   Execute seus aplicativos e páginas da Web em um ambiente do Internet Explorer 8 no Windows Vista ou no Windows XP para garantir que eles se comportem da maneira desejada.
-   Como alternativa, você pode executar a ferramenta de teste de compatibilidade do Internet Explorer (IECTT) fornecida com o kit de ferramentas de compatibilidade de aplicativos (ACT) para localizar possíveis problemas devido a atualizações de recursos de segurança.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Noções básicas sobre cadeias de agente do usuário](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Cadeia de caracteres User-Agent do Internet Explorer 8](/archive/blogs/ie/)
-   [Cadeia de caracteres do agente do usuário e vetor de versão](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [Hospedagem e reutilização](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [Download do kit de ferramentas de compatibilidade de aplicativos](/windows-hardware/get-started/adk-install)
-   [Problemas conhecidos do recurso de segurança do Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
