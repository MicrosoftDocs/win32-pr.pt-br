---
description: ChooseFont () caixa de diálogo comum do Win32
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: ChooseFont () caixa de diálogo comum do Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dd8eb6ec226f8dbf5220f5a90dac802cf149dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088604"
---
# <a name="choosefont-win32-common-dialog"></a>ChooseFont () caixa de diálogo comum do Win32

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -baixa  
**Frequência** -média  




## <a name="description"></a>Descrição

O Windows 7 inclui várias atualizações para a caixa de diálogo comum do Win32 ChooseFont (). Elas se enquadram em duas categorias:

-   Atualização Visual da caixa de diálogo
-   Suporte para novo recurso mostrar/ocultar fontes

A **atualização da caixa de diálogo** atualiza o modelo padrão para colocar a caixa de diálogo mais em linha com outros layouts de caixa de diálogo no Windows. Ele apresenta WYSIWYG às listas de exibição de fontes para ajudar os usuários a escolher as fontes. Ele também inclui um link para o CPL Fonts para fornecer acesso fácil para os usuários que desejam personalizar suas listas de fontes.

**Mostrar/ocultar fontes** é um novo recurso de plataforma do Windows 7 no qual as fontes não apropriadas para as configurações de idioma do usuário atual (métodos de entrada) não são apresentadas por padrão nas listas de seleção de fontes. Os usuários podem personalizar as fontes que desejam aparecer no CPL de fontes ou podem desabilitar esse recurso.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

**Atualização Visual do diálogo**

Apresentamos dois novos modelos no Windows 7 (um para aplicativos que carregam a versão 6 ou posterior de comctl32.dll e outro para aplicativos que carregam versões anteriores).

-   Por motivos de compatibilidade de aplicativos, esses novos modelos serão carregados somente para aplicativos que não conectam a fila de mensagens do ChooseFont. Os aplicativos que conectam a fila de mensagens continuarão a ver o layout de caixa de diálogo antigo.
-   Os aplicativos que fornecem seus próprios modelos continuarão a ser capazes de usá-los.

Os aplicativos que não obtiverem os novos modelos não verão nenhuma alteração de layout de caixa de diálogo do vista. No entanto, eles ainda devem obter a nova visualização de fonte WYSIWYG.

**Mostrar/ocultar fontes**

Para todas as versões do ChooseFont, a caixa de diálogo usará as configurações de fonte de mostrar/ocultar do usuário atual para determinar a lista de fontes a ser exibida. Isso resultará na exibição de menos listas de fontes na maioria das instâncias.

## <a name="end-user-mitigation"></a>Mitigação do usuário final

**Mostrar/ocultar fontes:** Para desabilitar a ocultação de fontes, os usuários devem ir para a página de configurações de fonte no CPL de fontes e desmarcar a seleção de '

Caixa de seleção "ocultar fontes com base nas configurações de idioma"

## <a name="developer-mitigation"></a>Mitigação do desenvolvedor

-   **Atualização Visual:** Os desenvolvedores de aplicativos que fornecem seus próprios modelos podem querer atualizá-lo para estar em linha com o novo modelo do Windows 7 apropriado. Os novos modelos estão disponíveis no arquivo de modelo Font. Dlg.

    **Observação:** O novo modelo publicado contém um controle SysLink adicional que fornece um atalho que permite aos usuários iniciarem as fontes CPL para exibir mais fontes. O controle de link requer a versão 6 da biblioteca de controle comum do Windows (comctl32.dll). Os desenvolvedores devem fornecer um manifesto ou diretiva que especifique o uso da versão 6 da DLL, se disponível. Em que um aplicativo usa uma versão anterior da biblioteca de controle comum, use o tipo de controle "botão de pressão".

-   **Mostrar/ocultar fontes:** Os desenvolvedores podem desabilitar esse recurso fornecendo um sinalizador adicional (CF \_ INACTIVEFONTS) no membro flags da estrutura CHOOSEFONT. Definir esse sinalizador faz com que todas as fontes instaladas sejam exibidas na lista de fontes.
-   **Mostrar/ocultar fontes:** Os aplicativos que fornecem conteúdo de ajuda do ChooseFont podem desejar adicionar conteúdo para explicar por que a lista de fontes é reduzida e direcionar os usuários para as fontes CPL para personalizar suas listas de fontes.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

Os desenvolvedores cujos aplicativos conectam a fila de mensagens do ChooseFont para personalizar a caixa de diálogo devem verificar se seus aplicativos retêm todas as funcionalidades existentes.

Os aplicativos que reduzem bastante a lista de fontes usando sinalizadores devem garantir que a lista de fontes apresentada permaneça aceitável.

 

 



