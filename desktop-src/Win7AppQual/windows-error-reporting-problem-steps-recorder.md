---
description: Gravador de etapas de Relatório de Erros do Windows problema
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Gravador de etapas de Relatório de Erros do Windows problema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abb8adf545152e34c2b2100022068291e3571f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084154"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Gravador de etapas de Relatório de Erros do Windows problema

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  


## <a name="description"></a>Descrição

Antes do Windows 7, Relatório de Erros do Windows (WER) coletou relatórios de erros que indicaram problemas de necessidade de reparo. Esses relatórios de erros contêm informações úteis que descrevem a natureza geral de um problema, mas não informações suficientes para determinar sua causa raiz. Para isso, os desenvolvedores precisam de uma ferramenta para reproduzir o cenário de falha/travamento para depuração.

Um novo aplicativo, o gravador de passos para problemas (PSR.exe), está sendo enviado em todas as compilações do Windows 7. Esse recurso habilita a coleta das ações executadas por um usuário ao encontrar uma falha para que os testadores e os desenvolvedores possam reproduzir a situação de análise e depuração.

## <a name="usage"></a>Uso

Atualmente, um desenvolvedor de serviço Relatório de Erros do Windows deve solicitar a habilitação de PSR para um aplicativo; As organizações de suporte da Microsoft também usam essa ferramenta durante a solução de problemas com os usuários finais. Os planos estão em vigor para tornar o PSR disponível no winqual (Windows Quality Online Services) após o lançamento do Windows 7.

**Observação:** Com o PSR habilitado para um aplicativo, o aplicativo pode ver alguma degradação do desempenho.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Relatório de Erros do Windows entrada de blog](/archive/blogs/wer/)
-   [Winqual (Windows Quality Online Services)](https://winqual.microsoft.com)

 

 
