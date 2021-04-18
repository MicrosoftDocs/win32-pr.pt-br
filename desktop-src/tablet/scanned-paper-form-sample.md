---
description: Neste exemplo de C \# , um formulário de papel foi examinado como um arquivo PNG (Portable Network Graphics) e especificado como a imagem de plano de fundo em tempo de execução para um controle InkPicture. O exemplo usa uma caixa de mensagem para exibir resultados de reconhecimento de manuscrito.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Exemplo de formulário de papel digitalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780686"
---
# <a name="scanned-paper-form-sample"></a>Exemplo de formulário de papel digitalizado

Neste exemplo de C \# , um formulário de papel foi examinado como um arquivo PNG (Portable Network Graphics) e especificado como a imagem de plano de fundo em tempo de execução para um controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) . O exemplo usa uma caixa de mensagem para exibir resultados de reconhecimento de manuscrito.

O exemplo inclui um arquivo linguagem XML (XML), Formdata.xml. O arquivo XML contém o nome do arquivo PNG. Ele também contém `FieldInfo` elementos que definem regiões retangulares no formulário em que um usuário pode inserir tinta. As informações no `FieldInfo` elemento são mostradas no exemplo a seguir:


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



Os elementos esquerdo, superior, direito e inferior são definições de coordenadas de pixel para cada campo.

O exemplo inicializa um novo [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) com os dados contidos no Formdata.xml:


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



A imagem do formulário especificada em Formdata.xml é carregada como o plano de fundo do controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) :


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



A coleta de tinta é então habilitada para o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) :


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a>Manipuladores de eventos de menu

O aplicativo inclui manipuladores de eventos de clique para todos os menus exibidos ao longo da parte superior do formulário.

### <a name="recognize-menu-item"></a>Reconhecer item de menu

O manipulador de eventos de clique do menu reconhecer desabilita a coleta de tinta para o controle e verifica se há um reconhecedor de manuscrito. Se nenhum reconhecedor estiver instalado, uma caixa de diálogo será exibida. Um usuário deve clicar na opção de menu tinta ou caneta para reabilitar o controle para entrada à tinta.

Se um reconhecedor estiver instalado, a `Recognize` função recuperará os dados XML que especificam coordenadas de pixel para cada campo de formulário. As coordenadas são convertidas em coordenadas de espaço à tinta e um retângulo é definido para cada campo de formulário. Depois que os retângulos são definidos, a função localiza os traços que interseccionam e ficam dentro de cada retângulo. Por fim, ele executa o reconhecimento na tinta e exibe os resultados em uma caixa de mensagem.

### <a name="ink-menu-item"></a>Item de menu de tinta

O manipulador de eventos de clique do menu de tinta habilita o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) .

### <a name="pen-menu-item"></a>Item de menu da caneta

O manipulador de eventos de clique no menu de caneta executa as seguintes tarefas:

-   Desabilita a coleta de tinta para o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) (que é necessário antes de alterar a propriedade [EditingMode](/previous-versions/ms582189(v=vs.100)) ).
-   Define a propriedade [EditingMode](/previous-versions/ms582189(v=vs.100)) para coletar tinta.
-   Habilita novamente a coleta de tinta para o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) e alterna os menus de caneta, seleção e borracha para indicar o modo ativo.

### <a name="edit-menu-item"></a>Editar item de menu

O menu Editar manipulador de eventos de clique é semelhante ao manipulador de eventos de menu de caneta. Ele executa as seguintes tarefas:

-   Desabilita a coleta de tinta.
-   Define a propriedade [EditingMode](/previous-versions/ms582189(v=vs.100)) a ser **selecionada**, o que permite que o usuário execute a seleção de tinta.
-   Habilita novamente a coleta de tinta e alterna os menus de caneta, de edição e de borracha para indicar o modo ativo.

### <a name="eraser-menu-item"></a>Item de menu de borracha

O menu de borracha clique no [manipulador de eventos](/previous-versions/ms582189(v=vs.100)) define o controle [inkpicturemode](/previous-versions/aa514604(v=msdn.10)) para **excluir**, que permite que um usuário apague a tinta. Ele também alterna os itens de menu caneta, editar e borracha.

### <a name="clear-menu-item"></a>Limpar item de menu

O manipulador de eventos de clique de menu Limpar exclui a coleção de [traços](/previous-versions/ms552701(v=vs.100)) atuais para o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) , apagando, assim, toda a tinta no formulário.

## <a name="closing-the-form"></a>Fechando o formulário

No código gerado pelo Windows Form Designer, o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) é adicionado à lista de componentes do formulário quando o formulário é inicializado. Quando o formulário é fechado, o controle InkPicture é Descartado, bem como os outros componentes do formulário, pelo método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle InkEdit](inkedit-control.md)
</dt> <dt>

[Controle InkPicture](inkpicture-control.md)
</dt> </dl>

 

 
