---
description: Para adicionar componentes à pasta Componentes de um aplicativo COM+, você pode usar o Assistente de Instalação de Componentes COM+ ou arrastar arquivos .dll que contêm os componentes do Windows Explorer e rebaixá-los no aplicativo.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Instalando novos componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af51bf28ce93e2d68dd1a07609c48c506911310781e8c5a0573017d43e022353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813586"
---
# <a name="installing-new-components"></a>Instalando novos componentes

Para adicionar componentes à pasta Componentes de um aplicativo COM+, você pode usar o Assistente de Instalação de Componentes COM+ ou arrastar os arquivos .dll que contêm os componentes do Windows Explorer e rebaixá-los no aplicativo. 

Se você usar o Assistente de Instalação de Componentes COM+, poderá instalar um novo componente, que registra o componente no computador, ou importar componentes que já foram registrados. Os componentes podem ser adicionados a aplicativos vazios ou aplicativos existentes.

**Para adicionar um componente a um aplicativo COM+**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador que hospeda o aplicativo COM+.

2.  Abra a **pasta Aplicativos COM+** para esse computador e selecione o aplicativo no qual você deseja instalar os componentes.

3.  Abra a pasta do aplicativo e selecione **Componentes**.

4.  No menu **Ação,** aponte para **Novo e** clique em **Componente**. Você também pode clicar com o botão direito do mouse na pasta **Componentes,** apontar para **Novo** e, em seguida, clicar em **Componente**.

5.  Na página De **boas-vindas** do Assistente de Instalação do  Aplicativo COM+, clique em Próximo e, em seguida, na caixa de diálogo Importar ou Instalar um Componente , clique em **Instalar novos componentes** .

6.  Na caixa **de diálogo Instalar novos** componentes, clique em **Adicionar** para procurar o componente que você deseja adicionar.

7.  Na caixa **de diálogo Selecionar arquivos a** serem instalados, digite o nome do arquivo do componente para instalar ou selecionar um nome de arquivo na lista exibida. Clique em **Abrir**.

    Depois de adicionar os arquivos, a **caixa** de diálogo Instalar novos componentes exibe os arquivos que você adicionou e seus componentes associados. Se você marcar a **caixa de** seleção Detalhes, verá mais informações sobre o conteúdo do arquivo e os componentes encontrados.

    > [!Note]  
    > Componentes COM não configurados devem ter uma biblioteca de tipos. Se o COM+ não conseguir encontrar a biblioteca de tipos do componente, o componente não aparecerá na lista. Você também pode remover um arquivo da lista Arquivos a **ser** instalado selecionando-o e clicando em **Remover**.

     

8.  Clique **em** Próximo e em **Concluir para** instalar o componente.

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

 

 



