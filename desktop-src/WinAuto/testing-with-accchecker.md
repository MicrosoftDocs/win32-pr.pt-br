---
title: Testando com AccChecker
description: Descreve o fluxo de trabalho de teste típico que incorpora AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- testando com AccChecker
- AccChecker, fluxo de trabalho de teste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addf725431a17a9b63376dfc3fc7ef8563a1737c9867b950f09eb123bf7daf18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795506"
---
# <a name="testing-with-accchecker"></a>Testando com AccChecker

O cenário a seguir descreve as etapas que você geralmente segue ao testar com AccChecker.

> [!Note]  
> Quando as rotinas de verificação AccChecker estão em execução, a interação do usuário com a máquina host pode interferir em algumas rotinas. Recomendamos que nenhuma interação adicional do usuário ocorra até que o AccChecker notifique o usuário de que todas as tarefas foram concluídas.

 

1.  Execute as verificações de AccChecker em um aplicativo ou controle de destino específico. Para obter mais informações, consulte a [guia verificações](the-accchecker-graphical-user-interface.md).
    > [!Note]  
    > AccChecker não explora todas as permutações de interface do usuário em um aplicativo. Elementos ocultos em controles como Windows, painéis, guias e menus devem ser expostos manualmente.

     

2.  Examine o log de erros do AccChecker e avalie ou faça a triagem dos resultados. Corrija problemas triviais e registre bugs graves conforme apropriado.
3.  Gerar um arquivo de supressão para bugs e erros que podem ser ignorados até o teste de regressão.
4.  Execute novamente as verificações de AccChecker com o arquivo de supressão e correções de bugs iniciais. Isso fornece um instantâneo dos problemas na implementação atual do Microsoft Acessibilidade Ativa e estabelece uma linha de base para testes de regressão.
5.  Integre as APIs do AccChecker e o arquivo de supressão em uma estrutura de teste automatizada para testes de regressão em log de bugs das verificações de AccChecker iniciais.
    > [!Note]  
    > À medida que os bugs são corrigidos, o arquivo de supressão deve ser modificado conforme necessário.

     

6.  Confirme se nenhuma regressão ou novos bugs de acessibilidade foram introduzidos no aplicativo ou no controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




