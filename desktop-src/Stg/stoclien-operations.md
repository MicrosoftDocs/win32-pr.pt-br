---
title: Operações StoCl ltda
description: O exemplo de StoCl ltda demonstra como o cliente usa o armazenamento estruturado. O exemplo a seguir resume as operações StoCl ltda.
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- Operações StoCl ltda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57b030065f73cbaede16fed8395dac58aa1d55085f0b5fd928fedf52b7cd80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960266"
---
# <a name="stoclien-operations"></a>Operações StoCl ltda

O [exemplo de StoCl ltda](structured-storage-client-sample--stoclien-.md) demonstra como o cliente usa o armazenamento estruturado. O exemplo a seguir resume as operações StoCl ltda.

A área de cliente da janela do aplicativo [StoClhin](structured-storage-client-sample--stoclien-.md) é usada para exibição visual do desenho de forma livre criado com um dispositivo de mouse ou tablet. Para desenhar com o mouse, pressione e segure o botão esquerdo do mouse ao mover o mouse. Liberar o botão esquerdo do mouse encerra o desenho de uma linha.

Aqui está um resumo das operações do ponto de vista do Stoclien.exe como um cliente COM do servidor Stoserve.dll COM:

<dl> <dt>

<span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Arquivo/Abrir
</dt> <dd>

Mostra a caixa de diálogo Abrir para obter um nome e um caminho para um arquivo de desenho de papel existente a ser aberto. Um padrão. A extensão de nome de arquivo PAP para esses arquivos é assumida. Se foram feitas alterações no desenho existente quando esse item de menu for escolhido, uma caixa de diálogo separada será mostrada primeiro perguntando ao usuário se o desenho atual deve ser salvo em seu arquivo composto associado.

</dd> <dt>

<span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Arquivo/Salvar
</dt> <dd>

Salva o desenho atual em seu arquivo composto associado.

</dd> <dt>

<span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Arquivo/Salvar como
</dt> <dd>

Mostra a caixa de diálogo Salvar como para obter um nome e um caminho para um novo arquivo de desenho de papel a ser criado. O desenho atual se torna o conteúdo salvo do novo arquivo e o novo arquivo se torna o novo arquivo composto associado para o desenho.

</dd> <dt>

<span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Arquivo/Saída
</dt> <dd>

Sai [de StoCl ltda.](structured-storage-client-sample--stoclien-.md)

</dd> <dt>

<span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Desenhar/desenhar em
</dt> <dd>

Liga o desenho entre o [cliente StoClhin](structured-storage-client-sample--stoclien-.md) e o objeto COPaper no servidor. Esse comando bloqueia o objeto COPaper para uso exclusivo por esse cliente e impede que outros clientes acessem a mesma instância do COPaper no servidor.

</dd> <dt>

<span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Desenhar/desenhar
</dt> <dd>

Desliga o desenho entre o [cliente StoClhin](structured-storage-client-sample--stoclien-.md) e o objeto COPaper no servidor. Esse comando desbloqueia o COPaper para uso exclusivo por esse cliente e permite que outros clientes acessem a mesma instância do COPaper no servidor.

</dd> <dt>

<span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Desenhar/redesenhar
</dt> <dd>

Redesenha no cliente os dados de desenho atuais mantidos no objeto COPaper no servidor.

</dd> <dt>

<span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Desenhar/apagar
</dt> <dd>

Apaga o conteúdo de desenho atual e limpa a imagem da janela. Seleção de Menu: Caneta/Cor Mostra a caixa de diálogo Escolher Cor para obter uma nova cor da caneta para desenho.

</dd> <dt>

<span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Caneta/Média
</dt> <dd>

Escolhe a largura média para desenho. Uma marca de seleção nessa opção de menu indica que a média é a largura da caneta atual.

</dd> <dt>

<span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Caneta/Espesso
</dt> <dd>

Escolhe a largura espesso para desenho. Uma marca de seleção nessa opção de menu indica que espesso é a largura da caneta atual.

</dd> <dt>

<span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Caneta/Fina
</dt> <dd>

Escolhe a largura fina para desenho. Uma marca de seleção nessa opção de menu indica que a fina é a largura da caneta atual.

</dd> <dt>

<span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/Conexão
</dt> <dd>

Conecta a interface IPaperSink COPaperSink ao ponto de conexão PaperSink do objeto COPaper. A repinção da imagem de desenho atual [em StoCl ltda](structured-storage-client-sample--stoclien-.md) depende da conexão do sink. Uma marca de seleção nessa opção de menu indica que a reainting está conectada.

</dd> <dt>

<span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/Disconnect
</dt> <dd>

Desconecta a interface IPaperSink COPaperSink do ponto de conexão PaperSink do objeto COPaper. A repinção da imagem de desenho atual [em StoCl ltda](structured-storage-client-sample--stoclien-.md) depende da conexão do sink. Uma marca de seleção nessa opção de menu indica que a repinção está desconectada.

</dd> <dt>

<span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Tutorial de Ajuda/StoCl tutorial
</dt> <dd>

Abre o STOCLIEN.HTM tutorial no navegador da Web.

</dd> <dt>

<span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Tutorial de Ajuda/StoServe
</dt> <dd>

Abre o STOSERVE.HTM tutorial no navegador da Web.

</dd> <dt>

<span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Arquivo de origem de ajuda/leitura
</dt> <dd>

Exibe a caixa de diálogo Abrir para que você possa abrir um arquivo de origem desta lição ou outro na Windows Bloco de notas.

</dd> <dt>

<span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Ajuda/Sobre o StoCl euclid
</dt> <dd>

Exibe a caixa de diálogo Sobre para este aplicativo.

</dd> </dl>

O [exemplo de StoCl ltda](structured-storage-client-sample--stoclien-.md) usa muitas das classes e serviços do utilitário fornecidos pelo [APPUTIL.](./using-visual-studio.md) Para obter mais informações sobre [APPUTIL](./using-visual-studio.md), consulte o código-fonte da biblioteca [APPUTIL](./using-visual-studio.md) no diretório [APPUTIL](./using-visual-studio.md) irmão e Apputil.md no diretório principal do tutorial. Para obter mais informações sobre [APPUTIL,](./using-visual-studio.md) [consulte How to Build Samples](how-to-build-samples.md).

 

 