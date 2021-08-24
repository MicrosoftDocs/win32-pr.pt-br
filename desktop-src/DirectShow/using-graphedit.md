---
description: Usando GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Usando GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f12dd613339680ac22352f4538b7029d8c9cea213c55f66e1986a8d32d0a68ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072140"
---
# <a name="using-graphedit"></a>Usando GraphEdit

GraphEdit está disponível no SDK (Software Development Kit) do Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).

O nome do aplicativo GraphEdit é "graphedt.exe". Depois de instalar o SDK, "graphedt.exe" está localizado no seguinte diretório: Arquivos de Programas Microsoft \[ \] \\ SDKs \\ Windows versão Bin \\ \[ \] \\ \\ .

Antes de executar GraphEdit, use o utilitário regsvr32 para registrar as seguintes DLLs, que estão localizadas no mesmo diretório:

-   proppage.dll
-   evrprop.dll

Essas DLLs permitem que GraphEdit exibe páginas de propriedades para alguns dos filtros de DirectShow integrados.

## <a name="build-a-file-playback-graph"></a>Criar um arquivo de reprodução Graph

GraphEdit pode criar um grafo de filtro para reprodução de arquivo. Esse recurso é equivalente a chamar o [**método IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) em um aplicativo. No menu **Arquivo,** clique em **Renderizar Arquivo de Mídia**. GraphEdit exibe uma caixa **de diálogo Abrir** Arquivo. Selecione um arquivo multimídia e clique em **Abrir**. GraphEdit cria um grafo de filtro para reproduzir o arquivo selecionado.

Você também pode renderizar um arquivo de mídia localizado em uma URL. No menu **Arquivo,** clique em **Renderizar URL**. GraphEdit exibe uma caixa de diálogo na qual digitar a URL.

## <a name="build-a-filter-graph"></a>Criar um filtro Graph

GraphEdit pode criar um grafo de filtro personalizado usando qualquer um dos filtros registrados em seu sistema. No menu **Graph,** clique em **Inserir Filtros**. Uma caixa de diálogo é exibida com uma lista dos filtros em seu sistema, organizados por categoria de filtro. GraphEdit cria essa lista com base nas informações no Registro. A ilustração a seguir mostra a caixa de diálogo.

![quais filtros você deseja inserir?](images/gedit12.png)

Para adicionar um filtro ao grafo, selecione o  nome do filtro e clique no botão Inserir Filtros ou clique duas vezes no nome do filtro. Depois de adicionar os filtros, você pode conectar dois filtros arrastando o mouse do pino de saída de um filtro para o pino de entrada de outro filtro. Se os pinos aceitarem a conexão, GraphEdit desenhará uma seta conectando-os.

![conectando dois filtros](images/gedit-connect.png)

## <a name="run-the-graph"></a>Execute o Graph

Depois de ter criado um grafo de filtro no Graph Editar, você pode executar o grafo para ver se ele funciona conforme o esperado. O **menu Graph** menu contém os comandos de menu **Reproduzir,** **Pausar** e **Parar**. Esses comandos invocam para os [**métodos IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**Executar,**](/windows/desktop/api/Control/nf-control-imediacontrol-run) [**Pausar**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)e [**Parar**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectivamente. A barra de ferramentas graphEdit também tem botões para estes comandos:

![pausar, reproduzir e parar botões](images/gedit-toolbar.png)

> [!Note]  
> O comando GraphEdit **Stop** primeiro pausa o grafo e busca a hora zero (supondo que o grafo seja buscado). Para reprodução de arquivo, essa ação redefine a janela de vídeo para o primeiro quadro. Em seguida, GraphEdit [**chama IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).

 

Se o grafo for buscado, você poderá busca-lo arrastando a barra de controle deslizante que aparece abaixo da barra de ferramentas. Arrastar a barra de controle deslizante invoca o [**método IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

## <a name="view-property-pages"></a>Exibir páginas de propriedades

Alguns filtros dão suporte a páginas de propriedades personalizadas, que fornecem uma interface do usuário para definir propriedades no filtro. Para exibir a página de propriedades de um filtro em GraphEdit, clique com o botão direito do mouse no filtro e selecione **Propriedades** na janela pop-up. GraphEdit exibe uma página de propriedades que contém as folhas de propriedades definidas pelo filtro (se alguma). Além disso, GraphEdit inclui uma folha de propriedades para cada pino no filtro. As folhas de propriedades de pino são definidas por GraphEdit, não pelo filtro. Se o pino estiver conectado, a folha de propriedades do pino exibirá o tipo de mídia para a conexão. Caso contrário, ele lista os tipos de mídia preferenciais do pino.

> [!Note]  
> Para usar as páginas de propriedades do GraphEdit, você deve registrar proppage.dll. Essa DLL está disponível no SDK do Windows. A DLL também contém páginas de propriedades adicionais para alguns DirectShow filtros. Essas páginas de propriedades são fornecidas apenas para fins de depuração.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Simulando Graph com GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



