---
description: Considerando que, em muitos casos, você poderá depurar apenas uma parte da funcionalidade de seus componentes no ambiente do Microsoft Visual Basic, haverá situações em que você precisará depurar os componentes criados com Visual Basic depois que eles tiverem sido compilados. Como o ambiente de Visual Basic não permite isso, você deve usar o ambiente de Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Depurando componentes de Visual Basic compilados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089175"
---
# <a name="debugging-compiled-visual-basic-components"></a>Depurando componentes de Visual Basic compilados

Considerando que, em muitos casos, você poderá depurar apenas uma parte da funcionalidade do componente dentro do ambiente do Microsoft Visual Basic, haverá situações em que você precisará depurar os componentes criados com Visual Basic depois que eles tiverem sido compilados. Como o ambiente de Visual Basic não permite isso, você deve usar o ambiente de Microsoft Visual C++.

**Para depurar um componente de Visual Basic no ambiente de Visual C++**

1.  No Visual Basic 6,0, abra o projeto Visual Basic que você deseja depurar.

2.  No menu **arquivo** , clique em **fazer YourProject.dll**.

3.  Na caixa de diálogo **criar projeto** , clique em **Opções**.

4.  Na caixa de diálogo **Propriedades do projeto** , na guia **Compilar** , clique em **Compilar para código nativo** e **sem otimização** e marque a caixa de seleção **criar informações de depuração simbólicas** .

5.  Clique em **OK** e em **OK** novamente para compilar o projeto.

6.  Mova a DLL compilada para o local onde os aplicativos COM+ são instalados normalmente.

    > [!Note]  
    > Se você não mover a DLL, poderá receber uma mensagem de erro informando que não foi possível localizar informações de depuração simbólicas da DLL. Se você tiver problemas para fazer com que o depurador pare nos pontos de interrupção em seu componente, confirme se a DLL está no diretório de pacotes padrão, exclua o componente de seu pacote e adicione o componente novamente.

     

7.  Iniciar Visual C++.

8.  No menu **arquivo** , clique em **abrir espaço de trabalho**.

9.  Na caixa de diálogo **abrir espaço de trabalho** , defina **arquivos do tipo** como **todos os arquivos ( \* . \* )**, selecione o componente compilado e clique em **abrir**.

10. No menu **arquivo** , clique em **abrir** (não **abra espaço de trabalho**) e abra o módulo Visual Basic (. bas), formulário (. frm) ou classe (. CLS) que você deseja depurar.

11. No menu **projeto** , clique em **configurações**.

12. Na caixa de diálogo **configurações do projeto** , na guia **depurar** , selecione **geral** na caixa **categoria** .

13. Na caixa **executável para sessão de depuração** , insira o caminho totalmente qualificado para Dllhost.exe, seguido por um argumento ESPECIFICANDO a ID do processo do aplicativo com+ que contém o componente. Você encontrará a ID do processo na guia **geral** da caixa de diálogo **Propriedades** do aplicativo com+. Veja a seguir um exemplo: C: \\ WinNT \\ System32 \\Dllhost.exe/ProcessId: { <processID> }.

14. Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte à depuração de Visual Basic COM+ em contraste com o MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Depuração no IDE Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



