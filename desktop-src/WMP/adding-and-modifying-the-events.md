---
title: Adicionando e modificando os eventos
description: Adicionando e modificando os eventos
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- plug-ins Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 464d20b600a5535e3cf2c02be01fa19c10a590e143c7a96375580719b70c274c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865336"
---
# <a name="adding-and-modifying-the-events"></a>Adicionando e modificando os eventos

Você precisa fornecer manipuladores de eventos para os \_ eventos de alteração en que ocorrem quando o usuário altera o texto nas caixas de edição da página de propriedades. Esses manipuladores de eventos têm uma implementação simples que apenas habilita a **aplicação** na caixa de diálogo página de propriedades.

## <a name="modifying-the-scale-factor-event-handler"></a>Modificando o manipulador de eventos do fator de escala

Você precisa alterar o nome do manipulador de eventos existente que o assistente de plug-in forneceu para a caixa de edição do fator de escala. Você deve alterar o nome de OnChangeScale para OnChangeDelay em três locais:

1.  Em EchoPropPage. h, altere o nome na seção macro do mapa de mensagens. Substitua a linha que mapeia o evento de alteração do fator de escala para o método OnChangeScale com o seguinte código:
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  Em EchoPropPage. h, altere o nome na linha que protótipos da função OnChangeScale:
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  Em EchoPropPage. cpp, altere o nome no cabeçalho da função:
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a>Adicionando o manipulador de eventos de mixagem úmida

Você pode adicionar facilmente o manipulador de eventos para o \_ evento de alteração en que é anexado ao \_ controle da caixa de edição WETMIX do IDC. No editor de recursos da caixa de diálogo:

1.  Clique com o botão direito do mouse na \_ caixa de edição IDC WETMIX e escolha **eventos**. a caixa de diálogo novo Windows mensagens e manipuladores de eventos é exibida.
2.  Na caixa **classe ou objeto a ser manipulada** , clique no nome do recurso da caixa de edição, IDC \_ WETMIX.
3.  na caixa **novo Windows mensagens/eventos** , clique em EN \_ alterar para selecioná-lo.
4.  Clique em **Adicionar manipulador**. A caixa de diálogo Adicionar função de membro é exibida.
5.  Na caixa **nome da função de membro** , digite o nome OnChangeWetmix.
6.  Clique em **OK** para fechar a caixa de diálogo Adicionar função de membro.
7.  Clique em **OK** para retornar para o editor de recursos da caixa de diálogo.

Visual C++ adiciona automaticamente o código para o mapa de mensagens e para a função de manipulador de eventos para EchoPropPage. h. O código que ele insere fornece um comentário TODO, no qual você pode adicionar a implementação no cabeçalho da função. esse é um estilo um pouco diferente do que o código de exemplo do assistente de Plug-in de Windows Media Player usa, mas é aceitável.

Se você deseja escrever sua implementação no arquivo de cabeçalho ou movê-lo para EchoPropPage. cpp, você precisa. Em ambos os casos, a implementação precisa apenas de uma única linha de código adicional para habilitar a **aplicação** na caixa de diálogo da página de propriedades. Insira esta linha de código antes da linha que retorna da função:


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modificando a página de propriedades de exemplo de eco**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




