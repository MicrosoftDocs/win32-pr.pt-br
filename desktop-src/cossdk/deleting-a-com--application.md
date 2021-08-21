---
description: À medida que os aplicativos existentes ficam desa datados ou não estão mais sendo usados, talvez seja necessário removê-los.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Excluindo um aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8332cd59ecde4115daa43ea97bc87d4354338e3ea94073317bfa293102deb78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047504"
---
# <a name="deleting-a-com-application"></a>Excluindo um aplicativo COM+

À medida que os aplicativos existentes ficam desa datados ou não estão mais sendo usados, talvez seja necessário removê-los.

**Para excluir um aplicativo COM+**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador para o qual você deseja excluir um aplicativo.

2.  Abra a **pasta Aplicativos COM+** do computador especificado para exibir todos os aplicativos.

3.  Selecione o aplicativo que você deseja remover.

4.  Se você selecionou um aplicativo de servidor, desligue o aplicativo. Você pode desligar um aplicativo selecionando-o na ferramenta administrativa serviços de componentes, clicando com o botão direito do mouse e clicando em **Desligar**. Se você selecionou um aplicativo de biblioteca, certifique-se de que todos os processos que usam esse aplicativo de biblioteca no momento sejam desligados.

5.  No menu **Ação,** clique em **Excluir**. Você também pode clicar com o botão direito do mouse no nome do aplicativo e, em seguida, clicar em **Excluir**. Você também pode excluir um aplicativo selecionando-o na  ferramenta administrativa Serviços de Componentes e pressionando a tecla Excluir ou pode selecionar o aplicativo, clicar com o botão direito do mouse e clicar em **Excluir**.

6.  Clique **em Sim** quando solicitado a confirmar sua ação.

Além disso, se um aplicativo de servidor ou proxy de aplicativo tiver sido instalado em um computador usando o instalador do Windows (conforme descrito em "Instalando aplicativos COM+" no Guia de Administração dos Serviços de Componentes), você poderá excluí-lo por meio do utilitário Adicionar/Remover Programas no Microsoft Windows Painel de Controle. Ou você pode excluir um aplicativo de servidor instalado ou proxy de aplicativo usando a sintaxe Windows linha de comando do instalador:

**msiexec -x nome** *do \_ aplicativo***.msi**

Esses métodos são especialmente úteis para excluir aplicativos COM+ em máquinas cliente que não estão executando a ferramenta administrativa dos Serviços de Componentes.

A exclusão do aplicativo também exclui todos os componentes contidos no aplicativo. Se esses componentes dependerem de recursos adicionais (conexões de banco de dados, arquivos de dados ou de texto, configuração de raiz virtual do IIS e assim por diante), esses recursos deverão ser removidos por meio de mecanismos diferentes da ferramenta administrativa dos Serviços de Componentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Copiando componentes](copying-components.md)
</dt> <dt>

[Criando um novo aplicativo COM+](creating-a-new-com--application.md)
</dt> <dt>

[Importando componentes](importing-components.md)
</dt> <dt>

[Instalando novos componentes](installing-new-components.md)
</dt> <dt>

[Movendo componentes](moving-components.md)
</dt> <dt>

[Removendo um componente de um aplicativo COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



