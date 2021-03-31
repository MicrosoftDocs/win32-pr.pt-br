---
title: Operações de StoClien
description: O exemplo StoClien demonstra como o cliente usa o armazenamento estruturado. A seguir, é resumido as operações de StoClien.
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- Operações de StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1068fcf1e377456211e08020f41279be9b5e3b0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641541"
---
# <a name="stoclien-operations"></a>Operações de StoClien

O exemplo [StoClien](structured-storage-client-sample--stoclien-.md) demonstra como o cliente usa o armazenamento estruturado. A seguir, é resumido as operações de StoClien.

A área de cliente da janela do aplicativo [StoClien](structured-storage-client-sample--stoclien-.md) é usada para exibição visual de desenho de forma livre criada com um mouse ou dispositivo tablet. Para desenhar com o mouse, pressione e mantenha o botão esquerdo do mouse ao mover o mouse. Soltar o botão esquerdo do mouse termina o desenho de uma linha.

Aqui está um resumo das operações do ponto de vista de Stoclien.exe como um cliente COM do servidor COM Stoserve.dll:

<dl> <dt>

<span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Arquivo/abrir
</dt> <dd>

Mostra a caixa de diálogo abrir para obter um nome e um caminho para que um arquivo de desenho de papel existente seja aberto. Um padrão. A extensão de nome de arquivo PAP para esses arquivos é assumida. Se forem feitas alterações no desenho existente quando esse item de menu for escolhido, uma caixa de diálogo separada será mostrada primeiro perguntando ao usuário se o desenho atual deve ser salvo em seu arquivo composto associado.

</dd> <dt>

<span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Arquivo/salvar
</dt> <dd>

Salva o desenho atual em seu arquivo composto associado.

</dd> <dt>

<span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Arquivo/salvar como
</dt> <dd>

Mostra a caixa de diálogo Salvar como para obter um nome e um caminho para um novo arquivo de desenho de papel a ser criado. O desenho atual se torna o conteúdo salvo do novo arquivo e o novo arquivo se torna o novo arquivo composto associado para o desenho.

</dd> <dt>

<span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Arquivo/sair
</dt> <dd>

Sai de [StoClien](structured-storage-client-sample--stoclien-.md).

</dd> <dt>

<span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Desenhar/desenhar em
</dt> <dd>

Ativa o desenho entre o cliente [StoClien](structured-storage-client-sample--stoclien-.md) e o objeto de copapel no servidor. Esse comando bloqueia o objeto de copapel para uso exclusivo por esse cliente e impede que outros clientes acessem a mesma instância de papel no servidor.

</dd> <dt>

<span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Desenhar/desenhar
</dt> <dd>

Desativa o desenho entre o cliente [StoClien](structured-storage-client-sample--stoclien-.md) e o objeto de copapel no servidor. Esse comando desbloqueia o copapel para uso exclusivo por esse cliente e permite que outros clientes acessem a mesma instância de papel no servidor.

</dd> <dt>

<span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Desenhar/redesenhar
</dt> <dd>

Redesenha no cliente os dados de desenho atuais mantidos no objeto de copapel no servidor.

</dd> <dt>

<span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Desenhar/apagar
</dt> <dd>

Apaga o conteúdo do desenho atual e limpa a imagem da janela. Seleção de menu: caneta/cor mostra a caixa de diálogo escolher cor para obter uma nova cor de caneta para desenhar.

</dd> <dt>

<span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Caneta/média
</dt> <dd>

Escolhe a largura média para o desenho. Uma marca de seleção nessa opção de menu indica que a média é a largura da caneta atual.

</dd> <dt>

<span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Caneta/grossa
</dt> <dd>

Escolhe a largura espessa para desenhar. Uma marca de seleção nessa opção de menu indica que a espessa é a largura atual da caneta.

</dd> <dt>

<span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Caneta/fina
</dt> <dd>

Escolhe a largura fina para desenhar. Uma marca de seleção nessa opção de menu indica que a fina é a largura atual da caneta.

</dd> <dt>

<span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Coletor/conexão
</dt> <dd>

Conecta a interface COPaperSink IPaperSink ao ponto de conexão do objeto copaper PaperSink. A repintura da imagem de desenho atual no [StoClien](structured-storage-client-sample--stoclien-.md) depende da conexão do coletor. Uma marca de seleção nessa opção de menu indica que a repintura está conectada.

</dd> <dt>

<span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Coletor/desconexão
</dt> <dd>

Desconecta a interface COPaperSink IPaperSink do objeto de copapel PaperSink ponto de conexão. A repintura da imagem de desenho atual no [StoClien](structured-storage-client-sample--stoclien-.md) depende da conexão do coletor. Uma marca de seleção nessa opção de menu indica que a repintura está desconectada.

</dd> <dt>

<span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Tutorial de ajuda/StoClien
</dt> <dd>

Abre o arquivo do tutorial STOCLIEN.HTM no navegador da Web.

</dd> <dt>

<span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Tutorial de ajuda/StoServe
</dt> <dd>

Abre o arquivo do tutorial STOSERVE.HTM no navegador da Web.

</dd> <dt>

<span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Arquivo de origem de ajuda/leitura
</dt> <dd>

Exibe a caixa de diálogo abrir para que você possa abrir um arquivo de origem desta lição ou de outra no bloco de notas do Windows.

</dd> <dt>

<span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Ajuda/sobre StoClien
</dt> <dd>

Exibe a caixa de diálogo sobre para este aplicativo.

</dd> </dl>

O exemplo [StoClien](structured-storage-client-sample--stoclien-.md) usa muitos dos serviços e classes de utilitário fornecidos pelo [APPUTIL](./using-visual-studio.md). Para obter mais informações sobre [APPUTIL](./using-visual-studio.md), consulte o código-fonte da biblioteca [APPUTIL](./using-visual-studio.md) no diretório [APPUTIL](./using-visual-studio.md) irmão e Apputil.MD no diretório principal do tutorial. Para obter mais informações sobre [APPUTIL](./using-visual-studio.md), consulte [como criar exemplos](how-to-build-samples.md).

 

 