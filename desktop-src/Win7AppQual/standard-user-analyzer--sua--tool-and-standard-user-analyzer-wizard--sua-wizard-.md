---
description: Saiba como usar a ferramenta de Standard User Analyzer (SUA) e o assistente de SUA para testar seus aplicativos e detectar possíveis problemas de compatibilidade.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Ferramenta SUA (Standard User Analyzer) (SUA) e Assistente do SUA (Assistente do Standard User Analyzer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc0e729c37ff1650f0dab7f3dd1c05ffb4b5f370
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104011898"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>Ferramenta SUA (Standard User Analyzer) (SUA) e Assistente do SUA (Assistente do Standard User Analyzer)

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes:** Windows XP Windows \| Vista Windows \| 7  
**Servidores:** Windows Server 2003 \| Windows server 2008 \| windows Server 2008 R2  

## <a name="description"></a>Descrição

O kit de ferramentas de compatibilidade de aplicativos inclui a ferramenta de Standard User Analyzer (SUA) e o assistente de Standard User Analyzer (Assistente de SUA). Essas ferramentas permitem que você teste seus aplicativos e monitore as chamadas à API para detectar possíveis problemas de compatibilidade devido ao recurso UAC (controle de conta de usuário) no sistema operacional Windows 7.

O UAC, anteriormente conhecido como LUA (conta de usuário limitada), requer que todos os usuários (incluindo membros do grupo de administradores) sejam executados como usuários padrão usando a caixa de diálogo de aviso de segurança até que o aplicativo seja deliberadamente elevado. No entanto, os aplicativos que exigem acesso e privilégios para locais que não estão disponíveis para um usuário padrão não podem ser executados corretamente com a função de usuário padrão.

## <a name="usage"></a>Uso

As seções a seguir fornecem informações detalhadas sobre como usar as ferramentas do seu e do assistente de SUA.

**Ferramenta SUA**

A ferramenta SUA permite analisar um aplicativo, examinar um relatório detalhado sobre os problemas relacionados ao UAC e, em seguida, aplicar as atenuações de aplicativo sugeridas e selecionadas, conforme mostrado no fluxograma a seguir.

![Diagrama que mostra o fluxo do S U uma ferramenta.](images/act-suaflowchart-appcookbook.gif)

*Ferramenta e virtualização da SUA*

Somente a ferramenta SUA permite ativar e desativar o recurso de virtualização. Ao desativar o recurso de virtualização, o aplicativo testado se comportará mais como quando estiver funcionando no sistema operacional Windows XP.

*Ferramenta SUA e privilégios elevados*

Somente a ferramenta SUA permite ativar e desativar o recurso de **inicialização elevada** . O recurso de inicialização elevada permite que o aplicativo selecionado seja executado como administrador ou como usuário padrão. Dependendo da sua seleção, você encontrará diferentes tipos de problemas relacionados ao UAC. Se você desmarcar a caixa de seleção Iniciar com privilégios **elevados** , seu aplicativo será executado com privilégios totais de administrador, o que permite ao seu prever os problemas que podem ocorrer para um usuário padrão. Se você marcar a caixa de seleção Iniciar com privilégios elevados, você verá erros que resultam do aplicativo realmente executando e gerando erros.

**Assistente de SUA**

O assistente do SUA permite que você siga um processo guiado e passo a passo pelo qual você pode analisar um aplicativo e, em seguida, aplicar as atenuações sugeridas e selecionadas do aplicativo, conforme mostrado no fluxograma a seguir. Diferentemente da ferramenta do SUA, o assistente não permite uma revisão dos problemas detalhados relacionados ao UAC.

![Diagrama que mostra o fluxo do S U de um assistente.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Download do kit de ferramentas de compatibilidade de aplicativos](/windows-hardware/get-started/adk-install)
-   [Noções básicas sobre as ferramentas de Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [Referência técnica do Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [Testando e mitigando problemas usando as ferramentas de desenvolvimento](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [Compatibilidade de aplicativos e controle de conta de usuário](/previous-versions/windows/)

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.

 

 

 
