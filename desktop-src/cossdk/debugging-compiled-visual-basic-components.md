---
description: Considerando que, em muitos casos, você poderá depurar apenas uma parte da funcionalidade de seus componentes no ambiente do Microsoft Visual Basic, haverá situações em que você precisará depurar componentes compilados com Visual Basic depois que eles foram compilados. Como o Visual Basic ambiente não habilita isso, você deve usar o ambiente Microsoft Visual C++ ambiente.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Depurando componentes Visual Basic compilados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eac784808602d3554e4610e70a8d8a22ef2ca1594062599ec6acd43db68b98a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128778"
---
# <a name="debugging-compiled-visual-basic-components"></a>Depurando componentes Visual Basic compilados

Considerando que, em muitos casos, você poderá depurar apenas uma parte da funcionalidade do componente no ambiente do Microsoft Visual Basic, haverá situações em que você precisará depurar componentes compilados com Visual Basic depois que eles foram compilados. Como o Visual Basic ambiente não habilita isso, você deve usar o ambiente Microsoft Visual C++ ambiente.

**Para depurar um Visual Basic no ambiente de Visual C++**

1.  No Visual Basic 6.0, abra o Visual Basic projeto que você deseja depurar.

2.  No menu **Arquivo,** clique em **Fazer YourProject.dll**.

3.  Na caixa **de diálogo Project,** clique em **Opções**.

4.  Na caixa de **Project propriedades,**  na guia Compilar, clique em  **Compilar** em Código Nativo e Sem Otimização e marque a caixa de seleção Criar Informações **de Depuração** Simbólicas .

5.  Clique **em OK** e em **OK** novamente para compilar seu projeto.

6.  Mova a DLL compilada para o local em que os aplicativos COM+ normalmente estão instalados.

    > [!Note]  
    > Se você não mover a DLL, poderá receber uma mensagem de erro informando que não foi possível localizar informações de depuração simbólicas para a DLL. Se você tiver problemas para fazer com que o depurador pare em pontos de interrupção em seu componente, confirme se a DLL está no diretório de pacotes padrão, exclua o componente de seu pacote e adicione o componente.

     

7.  Inicie Visual C++.

8.  No menu **Arquivo,** clique em **Abrir Workspace**.

9.  Na caixa **de diálogo Abrir Workspace,** de definido Arquivos do **Tipo** como Todos os **arquivos( . \* \* )**, selecione o componente compilado e clique em **Abrir**.

10. No **menu** Arquivo, clique em Abrir **(não** Abrir **Workspace)** e abra o módulo Visual Basic (.bas), o formulário (.frm) ou a classe (.cls) que você deseja depurar.

11. No menu **Project,** clique **em Configurações**.

12. Na caixa **Project Configurações** de diálogo, na guia **Depurar,** selecione **Geral** na **caixa Categoria.**

13. Na caixa **Executável** para sessão de depuração, insira o caminho totalmente qualificado para Dllhost.exe, seguido por um argumento que especifica a ID do processo do aplicativo COM+ que contém o componente. Você encontrará a ID do processo na **guia** Geral  da caixa de diálogo Propriedades do aplicativo COM+. Veja a seguir um exemplo: C: \\ Winnt \\ System32 \\Dllhost.exe /ProcessID:{ <processID> }.

14. Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte à depuração de Visual Basic COM+ contrastado com o MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Depuração no Visual Basic IDE](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



