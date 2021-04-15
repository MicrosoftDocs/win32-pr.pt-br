---
description: Usando GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Usando GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506017"
---
# <a name="using-graphedit"></a>Usando GraphEdit

O GraphEdit está disponível no Microsoft Windows Software Development Kit (SDK) ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).

O nome do aplicativo GraphEdit é "graphedt.exe". Depois de instalar o SDK, "graphedt.exe" está localizado no seguinte diretório: \[ arquivos de programas \] \\ Microsoft SDKs \\ Windows \\ \[ versão \] \\ bin \\ .

Antes de executar o GraphEdit, use o utilitário regsvr32 para registrar as seguintes DLLs, que estão localizadas no mesmo diretório:

-   proppage.dll
-   evrprop.dll

Essas DLLs permitem que o GraphEdit exiba páginas de propriedades para alguns dos filtros internos do DirectShow.

## <a name="build-a-file-playback-graph"></a>Criar um grafo de reprodução de arquivo

GraphEdit pode criar um grafo de filtro para reprodução de arquivos. Esse recurso é equivalente a chamar o método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) em um aplicativo. No menu **arquivo** , clique em **renderizar arquivo de mídia**. GraphEdit exibe uma caixa de diálogo **Abrir arquivo** . Selecione um arquivo multimídia e clique em **abrir**. O GraphEdit cria um grafo de filtro para reproduzir o arquivo que você selecionou.

Você também pode renderizar um arquivo de mídia localizado em uma URL. No menu **arquivo** , clique em **renderizar URL**. GraphEdit exibe uma caixa de diálogo na qual digitar a URL.

## <a name="build-a-filter-graph"></a>Criar um gráfico de filtro

O GraphEdit pode criar um grafo de filtro personalizado, usando qualquer um dos filtros registrados no seu sistema. No menu **gráfico** , clique em **Inserir filtros**. Uma caixa de diálogo é exibida com uma lista dos filtros em seu sistema, organizadas por categoria de filtro. GraphEdit compila essa lista a partir de informações no registro. A ilustração a seguir mostra a caixa de diálogo.

![quais filtros você deseja inserir?](images/gedit12.png)

Para adicionar um filtro ao grafo, selecione o nome do filtro, clique no botão **Inserir filtros** ou clique duas vezes no nome do filtro. Depois de adicionar os filtros, você pode conectar dois filtros arrastando o mouse do pino de saída de um filtro para o PIN de entrada de outro filtro. Se os Pins aceitarem a conexão, o GraphEdit desenhará uma seta conectando-as.

![Conectando dois filtros](images/gedit-connect.png)

## <a name="run-the-graph"></a>Executar o grafo

Depois de criar um grafo de filtro na edição de grafo, você pode executar o grafo para ver se ele funciona conforme o esperado. O menu **gráfico** contém os comandos de menu **reproduzir**, **Pausar** e **parar**. Esses comandos são invocados para os métodos [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**executados**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pausar**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)e [**parar**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectivamente. A barra de ferramentas GraphEdit também tem botões para esses comandos:

![botões pausar, reproduzir e parar](images/gedit-toolbar.png)

> [!Note]  
> O comando GraphEdit **Stop** primeiro pausa o grafo e procura o tempo zero (supondo que o grafo seja pesquisável). Para a reprodução de arquivo, essa ação redefine a janela de vídeo para o primeiro quadro. Em seguida, GraphEdit chama [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).

 

Se o grafo for pesquisável, você poderá Seek-lo arrastando a barra deslizante que aparece abaixo da barra de ferramentas. Arrastar a barra deslizante invoca o método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

## <a name="view-property-pages"></a>Exibir páginas de propriedades

Alguns filtros oferecem suporte a páginas de propriedades personalizadas, que fornecem uma interface do usuário para definir propriedades no filtro. Para exibir a página de propriedades de um filtro no GraphEdit, clique com o botão direito do mouse no filtro e selecione **Propriedades** na janela pop-up. GraphEdit exibe uma página de propriedades que contém as folhas de propriedades definidas pelo filtro (se houver). Além disso, o GraphEdit inclui uma folha de propriedades para cada Pin no filtro. As folhas de propriedades do PIN são definidas por GraphEdit, não pelo filtro. Se o PIN estiver conectado, a folha de propriedades do PIN exibirá o tipo de mídia para a conexão. Caso contrário, ele listará os tipos de mídia preferenciais do PIN.

> [!Note]  
> Para usar as páginas de propriedades internas do GraphEdit, você deve registrar proppage.dll. Essa DLL está disponível no SDK do Windows. A DLL também contém páginas de propriedades adicionais para alguns filtros do DirectShow. Essas páginas de propriedades são fornecidas apenas para fins de depuração.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Simulando a criação de gráficos com o GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



