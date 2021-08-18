---
title: Modificando o recurso de caixa de diálogo de eco
description: Modificando o recurso de caixa de diálogo de eco
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Windows Media Player plug-ins, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do DSP de eco, páginas de propriedades
- Exemplo de plug-in do DSP de eco, recurso de caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37dc88fe2c1b85dfc08727a00e744f1c5c16a2f25a4c5d429b2ab13898b0fcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996136"
---
# <a name="modifying-the-echo-dialog-resource"></a>Modificando o recurso de caixa de diálogo de eco

Você precisa alterar o recurso de caixa de diálogo que é a interface do usuário para o objeto de página de propriedade. Primeiro, você pode alterar a caixa de edição e o rótulo existentes para ser útil para a propriedade de tempo de atraso e, em seguida, adicionar uma segunda caixa de edição e um rótulo para a propriedade de combinação de umidade.

Para editar o recurso de caixa de diálogo Visual C++:

1.  Clique na **guia ResourceView** no Project Workspace.
2.  Expanda a árvore de recursos abrindo a pasta de nível superior.
3.  Abra a **pasta Caixa de** diálogo.
4.  Clique duas vezes no nome do recurso da caixa de diálogo, IDD \_ ECHOPROPPAGE. O editor de recursos aparece no painel direito.

## <a name="changing-the-existing-resources"></a>Alterando os recursos existentes

Para alterar os recursos da página de propriedades existentes para a propriedade de tempo de atraso:

1.  Primeiro, altere o texto no controle de texto estático existente. Clique com o botão direito do mouse no controle e escolha **Propriedades**. No campo **Legenda,** digite a nova legenda:
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  Feche a caixa de diálogo Propriedades de Texto .
3.  Agora, altere o nome do controle de caixa de edição. Para fazer isso, clique com o botão direito do mouse no controle e escolha **Propriedades**. No campo **ID,** digite um novo nome para o controle:
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  Feche a caixa de diálogo Editar Propriedades.
5.  Salve o recurso.
6.  Responda **Sim** se for solicitado a recarregar o arquivo resource.h.
7.  Clique na **guia FileView** no Project Workspace. Abra resource.h
8.  Localize o definido para o recurso de caixa de edição de fator de \# escala (IDC \_ SCALEFACTOR) e exclua-o. Ele deve ter o mesmo número de ID que \_ DELAYTIME do IDC.

## <a name="adding-the-new-resources"></a>Adicionando os novos recursos

Para adicionar os novos recursos da página de propriedades para a propriedade de combinação de umidade:

1.  Clique na **guia ResourceView** no Project Workspace para selecioná-lo.
2.  Clique duas vezes no nome da caixa de diálogo da página de propriedades, IDD \_ ECHOPROPPAGE. O editor de recursos aparece no painel direito.
3.  Use a caixa de ferramentas para adicionar um controle de texto estático e uma caixa de edição à página de propriedades.
4.  Clique com o botão direito do mouse no controle de texto estático e escolha **Propriedades**.
5.  Digite um novo nome para o controle de texto estático no **campo ID:**
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  Digite uma legenda para o rótulo:
    ```C++
    Effect level (%):
    
    ```

    

7.  Feche a caixa de diálogo Propriedades de Texto .
8.  Clique com o botão direito do mouse na caixa de edição e escolha **Propriedades**.
9.  Digite um novo nome para a caixa de edição no **campo ID:**
    ```C++
    IDC_WETMIX
    
    ```

    

10. Feche a caixa de diálogo Editar Propriedades.

Ao salvar o projeto, talvez seja solicitado que você recarregue resource.h. Clique **em Sim** se isso acontecer. O editor de recursos da caixa de diálogo deve adicionar os nomes de recursos e números de ID a resource.h para os itens que você adicionou. Se, por algum motivo, isso não acontecer, você deverá abrir resource.h e digitar novas entradas para o rótulo e o controle de caixa de edição e atribuir a cada um número de ID exclusivo.

## <a name="modifying-and-adding-the-string-resources"></a>Modificando e adicionando os recursos de cadeia de caracteres

O código de exemplo do assistente de plug-in especifica um recurso de cadeia de caracteres chamado IDS SCALERANGEERROR que contém uma mensagem a ser exibida quando a entrada do usuário \_ está fora do intervalo. Você pode modificar esse recurso para atender às suas necessidades para o valor de tempo de atraso seguindo estas etapas em Visual C++:

1.  Clique na **guia ResourceView.**
2.  Abra a pasta **Tabela de Cadeia de** Caracteres.
3.  Clique duas vezes no ícone **Tabela de Cadeia** de Caracteres para abrir o editor de recursos.
4.  Clique duas vezes no nome do recurso que você deseja editar, nesse caso, IDS \_ SCALERANGEERROR. A caixa de diálogo Propriedades da Cadeia de Caracteres é exibida.
5.  Altere o nome no campo **ID** para IDS \_ DELAYRANGEERROR.
6.  Altere o texto no **campo Legenda:**
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  Feche a caixa de diálogo Propriedades da Cadeia de Caracteres .

Em seguida, adicione um novo recurso de cadeia de caracteres para a mensagem de erro de propriedade de combinação de umidade.

1.  Clique duas vezes na linha vazia na parte inferior do editor de recursos.
2.  Altere o nome no campo **ID** para IDS \_ MIXRANGEERROR.
3.  Adicione o seguinte texto ao campo **Legenda:**
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  Feche a caixa de diálogo Propriedades da Cadeia de Caracteres .

Há dois outros valores que você deseja alterar na Tabela de Cadeia de Caracteres. IDS FRIENDLYNAME é o nome que aparece na Windows Media Player do usuário \_ para identificar o plug-in. A DESCRIÇÃO do IDS \_ permite que você conte ao usuário sobre seu plug-in. Ambas as cadeias de caracteres são passadas como parâmetros para a função **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin,** que é chamada no método DllRegisterServer em Echodll.cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modificando a página de propriedades de exemplo de eco**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




