---
description: Saiba como usar a ferramenta Standard User Analyzer (SUA) e o Assistente de SUA para testar seus aplicativos e detectar possíveis problemas de compatibilidade.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Ferramenta SUA (Standard User Analyzer) (SUA) e Assistente do SUA (Assistente do Standard User Analyzer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fa9329f2f42dd8fc3b948388ef44948deca052a919ca50704cbccedc83fca84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994666"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>Ferramenta SUA (Standard User Analyzer) (SUA) e Assistente do SUA (Assistente do Standard User Analyzer)

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes:** Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  

## <a name="description"></a>Descrição

O aplicativo de compatibilidade Toolkit inclui a ferramenta Standard User Analyzer (SUA) e o Assistente de Standard User Analyzer (Assistente sua). Essas ferramentas permitem que você teste seus aplicativos e monitore chamadas à API para detectar possíveis problemas de compatibilidade devido ao recurso UAC (Controle de Conta de Usuário) no sistema operacional Windows 7.

O UAC, anteriormente conhecido como CONTA de Usuário Limitado (LUA), requer que todos os usuários (incluindo membros do grupo Administrador) executem como Usuários Padrão usando a caixa de diálogo de prompt de segurança até que o aplicativo seja deliberadamente elevado. No entanto, os aplicativos que exigem acesso e privilégios para locais que não estão disponíveis para um Usuário Padrão não podem ser executados corretamente com a função usuário padrão.

## <a name="usage"></a>Uso

As seções a seguir fornecem informações detalhadas sobre como usar as ferramentas do Assistente sua e SUA.

**Ferramenta SUA**

A ferramenta SUA permite que você analise um aplicativo, revise um relatório detalhado sobre os problemas relacionados ao UAC e aplique as mitigações de aplicativo sugeridas e selecionadas, conforme mostrado no fluxograma a seguir.

![Diagrama que mostra o fluxo da ferramenta SU A.](images/act-suaflowchart-appcookbook.gif)

*Ferramenta SUA e Virtualização*

Somente a ferramenta SUA permite que você ative e desligue o recurso de virtualização. Ao desligar o recurso de virtualização, o aplicativo testado se comportará mais como quando estiver funcionando no sistema operacional Windows XP.

*Ferramenta SUA e privilégios elevados*

Somente a ferramenta SUA permite que você ative e desligue o **recurso Iniciar Elevado.** O recurso Iniciar Elevado permite que o aplicativo selecionado seja executado como administrador ou como um usuário padrão. Dependendo da seleção, você localizará diferentes tipos de problemas relacionados ao UAC. Se você  desempurar a caixa de seleção Iniciar Com Privilégios Elevados, seu aplicativo será executado com privilégios de Administrador completos, o que permite que o SEU preveia os problemas que podem ocorrer para um Usuário Padrão. Se você marcar a caixa de seleção Iniciar Com Elevação, verá erros resultantes da execução e geração de erros do aplicativo.

**Assistente de SUA**

O Assistente sua permite que você siga um processo guiado passo a passo pelo qual você pode analisar um aplicativo e, em seguida, aplicar as mitigações de aplicativo sugeridas e selecionadas, conforme mostrado no fluxograma a seguir. Ao contrário da ferramenta SUA, o assistente não habilita uma revisão dos problemas detalhados relacionados ao UAC.

![Diagrama que mostra o fluxo do Assistente de UU da S.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Download de compatibilidade Toolkit aplicativo](/windows-hardware/get-started/adk-install)
-   [Noções básicas sobre as Standard User Analyzer ferramentas](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [Standard User Analyzer referência técnica](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [Testando e atenuando problemas usando as Ferramentas de Desenvolvimento](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [Compatibilidade de aplicativos e controle de conta de usuário](/previous-versions/windows/)

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.

 

 

 
