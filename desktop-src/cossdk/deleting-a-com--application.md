---
description: À medida que os aplicativos existentes forem desatualizados ou não estiverem mais sendo usados, talvez seja necessário removê-los.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Excluindo um aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370456"
---
# <a name="deleting-a-com-application"></a>Excluindo um aplicativo COM+

À medida que os aplicativos existentes forem desatualizados ou não estiverem mais sendo usados, talvez seja necessário removê-los.

**Para excluir um aplicativo COM+**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador para o qual você deseja excluir um aplicativo.

2.  Abra a pasta **aplicativos com+** do computador especificado para exibir todos os aplicativos.

3.  Selecione o aplicativo que você deseja remover.

4.  Se você selecionou um aplicativo de servidor, desligue o aplicativo. Você pode desligar um aplicativo selecionando-o na ferramenta administrativa serviços de componentes, clicando com o botão direito do mouse e, em seguida, clicando em **desligar**. Se você selecionou um aplicativo de biblioteca, verifique se todos os processos que estão usando este aplicativo de biblioteca atualmente estão desligados.

5.  No menu **ação** , clique em **excluir**. Você também pode clicar com o botão direito do mouse no nome do aplicativo e clicar em **excluir**. Você também pode excluir um aplicativo selecionando-o na ferramenta administrativa serviços de componentes e pressionando a tecla **delete** , ou pode selecionar o aplicativo, clicar com o botão direito do mouse e, em seguida, clicar em **excluir**.

6.  Clique em **Sim** quando for solicitado a confirmar sua ação.

Além disso, se um aplicativo de servidor ou proxy de aplicativo tiver sido instalado em um computador usando Windows Installer (conforme descrito em "Instalando aplicativos COM+" no guia de administração de serviços de componentes), você poderá excluí-lo por meio do utilitário adicionar/remover programas no painel de controle do Microsoft Windows. Ou você pode excluir um aplicativo de servidor instalado ou proxy de aplicativo usando a sintaxe de linha de comando Windows Installer:

**msiexec-x** *nome do aplicativo \_ * * *. msi**

Esses métodos são especialmente úteis para excluir aplicativos COM+ em computadores cliente que não executam a ferramenta administrativa serviços de componentes.

Excluir o aplicativo também exclui todos os componentes contidos no aplicativo. Se esses componentes dependerem de recursos adicionais (conexões de banco de dados, arquivos de data ou de texto, configuração de raiz virtual do IIS e assim por diante), esses recursos deverão ser removidos por meio de mecanismos diferentes da ferramenta administrativa serviços de componentes.

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

 

 



