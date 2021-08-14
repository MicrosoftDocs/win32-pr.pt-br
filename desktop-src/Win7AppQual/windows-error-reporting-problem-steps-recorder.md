---
description: Relatório de Erros do Windows Gravador de etapas do problema
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Relatório de Erros do Windows Gravador de etapas do problema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba90b76b3d486dc0708e0803609539fda6d6141d0a6f3ab100ba0ce198846fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328078"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Relatório de Erros do Windows Gravador de etapas do problema

## <a name="affected-platforms"></a>Plataformas afetadas

**clientes** – Windows 7  
**servidores** – Windows Server 2008 R2  


## <a name="description"></a>Descrição

antes do Windows 7, Relatório de Erros do Windows (WER) coletou relatórios de erros que indicaram problemas de necessidade de reparo. Esses relatórios de erros contêm informações úteis que descrevem a natureza geral de um problema, mas não informações suficientes para determinar sua causa raiz. Para isso, os desenvolvedores precisam de uma ferramenta para reproduzir o cenário de falha/travamento para depuração.

um novo aplicativo, o gravador de etapas de problema (PSR.exe), está sendo enviado em todas as compilações do Windows 7. Esse recurso habilita a coleta das ações executadas por um usuário ao encontrar uma falha para que os testadores e os desenvolvedores possam reproduzir a situação de análise e depuração.

## <a name="usage"></a>Uso

atualmente, um desenvolvedor de serviço Relatório de Erros do Windows deve solicitar a habilitação de PSR para um aplicativo; As organizações de suporte da Microsoft também usam essa ferramenta durante a solução de problemas com os usuários finais. os planos estão em vigor para tornar o PSR disponível em Winqual (Windows Quality Online Services) após o lançamento do Windows 7.

**Observação:** Com o PSR habilitado para um aplicativo, o aplicativo pode ver alguma degradação do desempenho.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Relatório de Erros do Windows entrada de blog](/archive/blogs/wer/)
-   [Windows Winqual (Quality Online Services)](https://winqual.microsoft.com)

 

 
