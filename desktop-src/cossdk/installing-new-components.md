---
description: Para adicionar componentes à pasta componentes de um aplicativo COM+, você pode usar o assistente de instalação de componente COM+ ou arrastar arquivos. dll que contêm os componentes do Windows Explorer e soltá-los no aplicativo.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Instalando novos componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010228"
---
# <a name="installing-new-components"></a>Instalando novos componentes

Para adicionar componentes à pasta **componentes** de um aplicativo com+, você pode usar o assistente de instalação de componente com+ ou arrastar arquivos. dll que contêm os componentes do Windows Explorer e soltá-los no aplicativo.

Se você usar o assistente de instalação de componente COM+, poderá instalar um novo componente, que registra o componente no computador ou importar componentes que já foram registrados. Os componentes podem ser adicionados a aplicativos vazios ou a aplicativos existentes.

**Para adicionar um componente a um aplicativo COM+**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador que hospeda o aplicativo COM+.

2.  Abra a pasta **aplicativos com+** para esse computador e selecione o aplicativo no qual você deseja instalar os componentes.

3.  Abra a pasta do aplicativo e selecione **componentes**.

4.  No menu **ação** , aponte para **novo** e clique em **componente**. Você também pode clicar com o botão direito do mouse na pasta **componentes** , apontar para **novo** e clicar em **componente**.

5.  Na página de **boas-vindas** do assistente de instalação do aplicativo com+, clique em **Avançar** e, na caixa de diálogo **importar ou instalar um componente** , clique em **instalar novos componentes** .

6.  Na caixa de diálogo **instalar novos componentes** , clique em **Adicionar** para procurar o componente que você deseja adicionar.

7.  Na caixa de diálogo **selecionar arquivos para instalar** , digite o nome do arquivo do componente a ser instalado ou selecione um nome de arquivo na lista exibida. Clique em **Abrir**.

    Depois de adicionar os arquivos, a caixa de diálogo **instalar novos componentes** exibe os arquivos que você adicionou e seus componentes associados. Se você marcar a caixa de seleção **detalhes** , verá mais informações sobre o conteúdo do arquivo e os componentes que foram encontrados.

    > [!Note]  
    > Os componentes COM não configurados devem ter uma biblioteca de tipos. Se COM+ não conseguir localizar a biblioteca de tipos do componente, seu componente não aparecerá na lista. Você também pode remover um arquivo da lista **arquivos a serem instalados** selecionando-o e clicando em **remover**.

     

8.  Clique em **Avançar** e em **concluir** para instalar o componente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Copiando componentes](copying-components.md)
</dt> <dt>

[Criando um novo aplicativo COM+](creating-a-new-com--application.md)
</dt> <dt>

[Excluindo um aplicativo COM+](deleting-a-com--application.md)
</dt> <dt>

[Importando componentes](importing-components.md)
</dt> <dt>

[Movendo componentes](moving-components.md)
</dt> <dt>

[Removendo um componente de um aplicativo COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



