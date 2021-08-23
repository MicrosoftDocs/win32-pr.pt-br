---
title: Ferramentas de acessibilidade – AccChecker (verificador de acessibilidade da interface do usuário)
description: Descreve o AccChecker (verificador de acessibilidade da interface do usuário), uma ferramenta para testar a automação da interface do usuário do aplicativo ou a implementação do Microsoft Acessibilidade Ativa (MSAA).
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI Accessibility Checker
- AccChecker
- Implementação da automação da interface do usuário, teste
- Implementação de UIA, teste
- Implementação do Microsoft Acessibilidade Ativa, testes
- Implementação de MSAA, teste
- testando a automação da interface do usuário
- testando UIA
- testando o Microsoft Acessibilidade Ativa
- testando a MSAA
- Ferramentas de teste de UIA
- Ferramentas de teste de automação da interface do usuário
- Ferramentas de teste de MSAA
- Ferramentas de teste do Microsoft Acessibilidade Ativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 452ff74140b50f1f6ea6d5357187e42ecff2d83cc85076d11ff22e191da7f3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052404"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a>Ferramentas de acessibilidade – AccChecker (verificador de acessibilidade da interface do usuário)

**AccChecker** (verificador de acessibilidade da interface do usuário) verifica se os principais requisitos de acessibilidade da interface do usuário são atendidos no design e na implementação da UIA (automação da interface do usuário) ou Microsoft acessibilidade ativa (MSAA), independentemente da estrutura subjacente da interface do usuário. O **AccChecker** também inclui um conjunto de verificações de acessibilidade da Web.

O **AccChecker** fornece os seguintes níveis de funcionalidade:

- um aplicativo de GUI Windows que dá suporte a testes manuais, registro de mensagens e geração de supressão.
- Uma API para uso em estruturas de teste automatizadas.
- Um aplicativo de console que dá suporte a automaçãos de teste não gerenciadas para cenários em que a API gerenciada **AccChecker** não pode ser usada.

Todos os níveis de funcionalidade do **AccChecker** fornecem rotinas para verificar o acesso programático ao Microsoft acessibilidade ativa, geração de eventos programático, layout de controle e navegação por teclado. O **AccChecker** também fornece um serviço básico de transcrição de leitor de tela.

o **AccChecker** é instalado com o SDK (Software Development Kit) do Windows. Ele está localizado na \\ pasta bin \\ < *version* > \\ <  > \\ AccChecker do caminho de instalação do SDK.

> [!NOTE]
> **AccChecker** é uma ferramenta herdada. é recomendável usar [Insights de acessibilidade](https://accessibilityinsights.io/) em vez disso.

## <a name="requirements"></a>Requisitos

requer o .NET Framework 2,0 ou posterior.

O **AccChecker** pode ser usado para examinar dados de acessibilidade em sistemas que não têm a automação da interface do usuário da Microsoft, mas só pode examinar as propriedades do Microsoft acessibilidade ativa. Para examinar a automação da interface do usuário, a automação da interface do usuário deve estar presente no sistema. Para obter mais informações, consulte a seção "requisitos" da [automação da interface do usuário](entry-uiauto-win32.md).

O **AccChecker** é instalado como parte do conjunto geral de ferramentas no SDK do Windows, ele não é distribuído como um download de exe separado. o SDK do Windows inclui todas as ferramentas relacionadas à acessibilidade documentadas nesta seção. [obtenha o SDK do Windows.](https://developer.microsoft.com/) (Há também um arquivo de download do SDK vinculado dessa página, se você precisar de uma versão anterior.)

## <a name="related-topics"></a>Tópicos relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Inspecionar](inspect-objects.md)
- [Ferramentas de teste](testing-tools.md)
- [Verificação da Automação da Interface do Usuário](ui-automation-verify.md)
