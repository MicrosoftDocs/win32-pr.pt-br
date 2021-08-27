---
description: Caixa de diálogo Comum ChooseFont() Win32
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Caixa de diálogo Comum ChooseFont() Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95edc873d6984b5db312d3a86fc926f72817a5170672ad315d07e209d98c4398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098526"
---
# <a name="choosefont-win32-common-dialog"></a>Caixa de diálogo Comum ChooseFont() Win32

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Gravidade –** Baixa  
**Frequência** – Média  




## <a name="description"></a>Descrição

Windows 7 inclui várias atualizações para a caixa de diálogo comum ChooseFont() Win32. Elas se enquadram em duas categorias:

-   Atualização visual da caixa de diálogo
-   Suporte para o novo recurso mostrar/ocultar fontes

A **atualização da caixa** de diálogo atualiza o modelo padrão para colocar a caixa de diálogo mais alinhada com outros layouts de caixa de diálogo Windows. Ele apresenta o WYSIWYG às listas de exibição de fonte para ajudar os usuários a escolher fontes. Ele também inclui um link para a CPL de Fontes para fornecer acesso fácil aos usuários que desejam personalizar suas listas de fontes.

**Mostrar/ocultar fontes** é um novo recurso de plataforma do Windows 7 pelo qual as fontes não apropriadas para as configurações de idioma do usuário atual (métodos de entrada) não são apresentadas por padrão nas listas de seleção de fonte. Os usuários podem personalizar as fontes que desejam aparecer na CPL de Fontes ou podem desabilitar esse recurso.

## <a name="manifestation-of-impact"></a>Manifestação de impacto

**Atualização visual da caixa de diálogo**

Introduzimos dois novos modelos no Windows 7 (um para aplicativos que carregam a versão 6 ou posterior do comctl32.dll e outro para aplicativos que carregam versões anteriores).

-   Por motivos de compatibilidade do aplicativo, esses novos modelos só serão carregados para aplicativos que não conectarem a fila de mensagens ChooseFont. Os aplicativos que conectarem a fila de mensagens continuarão a ver o layout da caixa de diálogo antigo.
-   Os aplicativos que fornecem seus próprios modelos continuarão a ser capazes de usá-los.

Os aplicativos que não receberem os novos modelos não verão nenhuma alteração de layout de caixa de diálogo do Vista. No entanto, eles ainda devem obter a nova versão prévia da fonte DEMSIWYG.

**Mostrar/ocultar fontes**

Para todas as versões do ChooseFont, a caixa de diálogo usará as configurações de fonte show/hide do usuário atual para determinar a lista de fontes a ser exibida. Isso resultará na exibição de menos listas de fontes na maioria das instâncias.

## <a name="end-user-mitigation"></a>Mitigação do usuário final

**Mostrar/Ocultar Fontes:** Para desabilitar a ocultação de fonte, os usuários devem ir para a página Configurações fonte na CPL fontes e desmarcar o '

Caixa de seleção "Ocultar fontes com base em configurações de idioma"

## <a name="developer-mitigation"></a>Mitigação do desenvolvedor

-   **Atualização visual:** Os desenvolvedores de aplicativos que fornecem seus próprios modelos podem querer atualizar isso para que eles sejam alinhados com o novo modelo Windows 7 apropriado. Os novos modelos estão disponíveis no arquivo de modelo Font.dlg.

    **Observação:** O novo modelo publicado contém um controle SysLink adicional que fornece um atalho que permite aos usuários iniciar a CPL de Fontes para exibir mais fontes. O controle de link requer a versão 6 Windows biblioteca de controle comum (comctl32.dll). Os desenvolvedores devem fornecer um manifesto ou diretiva que especifique o uso da versão 6 da DLL, se disponível. Em que um aplicativo usa uma versão anterior da biblioteca de controle comum, use o tipo de controle "PUSHBUTTON".

-   **Mostrar/Ocultar Fontes:** Os desenvolvedores podem desabilitar esse recurso fornecendo um sinalizador adicional (CF INACTIVEFONTS) no membro de sinalizadores da \_ estrutura CHOOSEFONT. Definir esse sinalizador faz com que todas as fontes instaladas são exibidas na lista de fontes.
-   **Mostrar/Ocultar Fontes:** Os aplicativos que fornecem conteúdo da ajuda ChooseFont podem querer adicionar conteúdo para explicar por que a lista de fontes é reduzida e direcionar os usuários à CPL de Fontes para personalizar suas listas de fontes.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Teste de compatibilidade, desempenho, confiabilidade e usabilidade

Os desenvolvedores cujos aplicativos conectarem a fila de mensagens ChooseFont para personalizar a caixa de diálogo devem verificar se seus aplicativos mantêm todas as funcionalidades existentes.

Os aplicativos que cortam intensamente a lista de fontes usando sinalizadores devem garantir que a lista de fontes apresentada permaneça aceitável.

 

 



