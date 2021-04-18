---
description: Você pode usar a ferramenta administrativa serviços de componentes para importar para componentes específicos de aplicativos que já foram registrados em seu computador como componentes COM no registro do Windows.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importando componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456953"
---
# <a name="importing-components"></a>Importando componentes

Você pode usar a ferramenta administrativa serviços de componentes para importar para componentes específicos de aplicativos que já foram registrados em seu computador como componentes COM no registro do Windows. A importação de um componente não instala as informações de interface ou método necessárias para definir propriedades de interface ou para configurar o acesso ao componente de um cliente remoto. Portanto, se possível, você deve instalar o em vez de importar componentes não configurados.

> [!Note]  
> Ao importar um componente para um aplicativo COM+, o COM+ não preenche as informações de interface e de método do componente. Durante a exportação de um proxy de aplicativo, o COM+ não fornecerá informações de marshaling (bibliotecas de tipo ou proxy/stubs) para algumas ou todas as interfaces. A exportação de proxies de aplicativo que contêm componentes importados falhará ou fará com que um aviso seja emitido.

 

**Para importar um componente para um aplicativo COM+**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador que hospeda o aplicativo COM+.

2.  Abra a pasta **aplicativos com+** para esse computador e selecione o aplicativo no qual você deseja instalar o componente.

3.  Abra a pasta do aplicativo e selecione **componentes**.

4.  No menu **ação** , aponte para **novo** e clique em **componente**. Você também pode clicar com o botão direito do mouse na pasta **componentes** , apontar para **novo** e clicar em **componente**.

5.  Na página de **boas-vindas** do assistente de instalação do aplicativo com+, clique em **Avançar** e, na caixa de diálogo **importar ou instalar um componente** , clique em **importar componente (s) que já está registrado**.

6.  Na caixa de diálogo **escolher componentes a serem importados** , marque a caixa de seleção **detalhes** para ver informações completas sobre os componentes que já estão registrados. Selecione os componentes que você deseja importar da lista exibida e clique em **Avançar**.

7.  Clique em **Concluir**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Copiando componentes](copying-components.md)
</dt> <dt>

[Criando um novo aplicativo COM+](creating-a-new-com--application.md)
</dt> <dt>

[Excluindo um aplicativo COM+](deleting-a-com--application.md)
</dt> <dt>

[Instalando novos componentes](installing-new-components.md)
</dt> <dt>

[Movendo componentes](moving-components.md)
</dt> <dt>

[Removendo um componente de um aplicativo COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



