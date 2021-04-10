---
title: Modificando o recurso de diálogo de eco
description: Modificando o recurso de diálogo de eco
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, recurso de caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292491"
---
# <a name="modifying-the-echo-dialog-resource"></a>Modificando o recurso de diálogo de eco

Você precisa alterar o recurso de caixa de diálogo que é a interface do usuário para o objeto da página de propriedades. Você pode primeiro alterar a caixa de edição e o rótulo existentes para que sejam úteis para a propriedade de tempo de atraso e, em seguida, adicionar uma segunda caixa de edição e rótulo para a propriedade de combinação úmida.

Para editar o recurso de caixa de diálogo no Visual C++:

1.  Clique na guia **ResourceView** no espaço de trabalho do projeto.
2.  Expanda a árvore de recursos abrindo a pasta de nível superior.
3.  Abra a pasta **caixa de diálogo** .
4.  Clique duas vezes no nome do recurso de caixa de diálogo, IDD \_ ECHOPROPPAGE. O editor de recursos é exibido no painel direito.

## <a name="changing-the-existing-resources"></a>Alterando os recursos existentes

Para alterar os recursos da página de propriedades existente para a propriedade tempo de atraso:

1.  Primeiro, altere o texto no controle de texto estático existente. Clique com o botão direito do mouse no controle e escolha **Propriedades**. No campo **legenda** , digite a nova legenda:
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  Feche a caixa de diálogo Propriedades de texto.
3.  Agora, altere o nome do controle caixa de edição. Para fazer isso, clique com o botão direito do mouse no controle e escolha **Propriedades**. No campo **ID** , digite um novo nome para o controle:
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  Feche a caixa de diálogo Editar propriedades.
5.  Salve o recurso.
6.  Responda **Sim** se for solicitado a recarregar o arquivo Resource. h.
7.  Clique na guia **fileview** no espaço de trabalho do projeto. Abrir Resource. h
8.  Localize o \# recurso definir para a caixa de edição fator de escala (IDC \_ SCALEFACTOR) e exclua-o. Ele deve ter o mesmo número de ID que o IDC \_ DelayTime.

## <a name="adding-the-new-resources"></a>Adicionando os novos recursos

Para adicionar os novos recursos da página de propriedades para a propriedade de combinação úmida:

1.  Clique na guia **ResourceView** no espaço de trabalho do projeto para selecioná-la.
2.  Clique duas vezes no nome da caixa de diálogo página de propriedades, IDD \_ ECHOPROPPAGE. O editor de recursos é exibido no painel direito.
3.  Use o Toolbox para adicionar um controle de texto estático e uma caixa de edição à página de propriedades.
4.  Clique com o botão direito do mouse no controle de texto estático e escolha **Propriedades**.
5.  Digite um novo nome para o controle de texto estático no campo **ID** :
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  Digite uma legenda para o rótulo:
    ```C++
    Effect level (%):
    
    ```

    

7.  Feche a caixa de diálogo Propriedades de texto.
8.  Clique com o botão direito do mouse na caixa de edição e escolha **Propriedades**.
9.  Digite um novo nome para a caixa de edição no campo **ID** :
    ```C++
    IDC_WETMIX
    
    ```

    

10. Feche a caixa de diálogo Editar propriedades.

Ao salvar o projeto, você pode ser solicitado a recarregar o Resource. h. Clique em **Sim** se isso acontecer. A caixa de diálogo Editor de recursos deve adicionar os nomes de recursos e os números de ID a Resource. h para os itens adicionados. Se, por algum motivo, isso não acontecer, você deverá abrir Resource. h e digitar novas entradas para o controle rótulo e caixa de edição e atribuir cada um número de ID exclusivo.

## <a name="modifying-and-adding-the-string-resources"></a>Modificando e adicionando os recursos de cadeia de caracteres

O código de exemplo do assistente de plug-in especifica um recurso de cadeia de caracteres chamado IDS \_ SCALERANGEERROR que contém uma mensagem a ser exibida quando a entrada do usuário está fora do intervalo. Você pode modificar esse recurso para se adequar às suas necessidades pelo valor do tempo de atraso seguindo estas etapas no Visual C++:

1.  Clique na guia **ResourceView** .
2.  Abra a pasta da **tabela de cadeia de caracteres** .
3.  Clique duas vezes no ícone de **tabela de cadeia de caracteres** para abrir o editor de recursos.
4.  Clique duas vezes no nome do recurso que você deseja editar, nesse caso, IDS \_ SCALERANGEERROR. A caixa de diálogo Propriedades da cadeia de caracteres é exibida.
5.  Altere o nome no campo **ID** para IDs \_ DELAYRANGEERROR.
6.  Altere o texto no campo **legenda** :
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  Feche a caixa de diálogo Propriedades da cadeia de caracteres.

Em seguida, adicione um novo recurso de cadeia de caracteres para a mensagem de erro de propriedade de mistura úmida.

1.  Clique duas vezes na linha vazia na parte inferior do editor de recursos.
2.  Altere o nome no campo **ID** para IDs \_ MIXRANGEERROR.
3.  Adicione o seguinte texto ao campo de **legenda** :
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  Feche a caixa de diálogo Propriedades da cadeia de caracteres.

Há dois outros valores que você deve alterar na tabela de cadeias de caracteres. IDS \_ FriendlyName é o nome que aparece na interface do usuário do Windows Media Player para identificar o plug-in. \_Descrição de IDs permite que você informe o usuário sobre seu plug-in. Essas duas cadeias de caracteres são passadas como parâmetros para a função **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** , que é chamada no método DllRegisterServer em Echodll. cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modificando a página de propriedades de exemplo de eco**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




