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
# <a name="stoclien-operations"></a><span data-ttu-id="30282-105">Operações de StoClien</span><span class="sxs-lookup"><span data-stu-id="30282-105">StoClien Operations</span></span>

<span data-ttu-id="30282-106">O exemplo [StoClien](structured-storage-client-sample--stoclien-.md) demonstra como o cliente usa o armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="30282-106">The [StoClien](structured-storage-client-sample--stoclien-.md) sample demonstrates how the client uses structured storage.</span></span> <span data-ttu-id="30282-107">A seguir, é resumido as operações de StoClien.</span><span class="sxs-lookup"><span data-stu-id="30282-107">The following summarizes the StoClien operations.</span></span>

<span data-ttu-id="30282-108">A área de cliente da janela do aplicativo [StoClien](structured-storage-client-sample--stoclien-.md) é usada para exibição visual de desenho de forma livre criada com um mouse ou dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="30282-108">The [StoClien](structured-storage-client-sample--stoclien-.md) application window client area is used for visual display of freeform drawing created with a mouse or tablet device.</span></span> <span data-ttu-id="30282-109">Para desenhar com o mouse, pressione e mantenha o botão esquerdo do mouse ao mover o mouse.</span><span class="sxs-lookup"><span data-stu-id="30282-109">To draw with the mouse, press and hold the left mouse button while moving the mouse.</span></span> <span data-ttu-id="30282-110">Soltar o botão esquerdo do mouse termina o desenho de uma linha.</span><span class="sxs-lookup"><span data-stu-id="30282-110">Releasing the left mouse button ends the drawing of a line.</span></span>

<span data-ttu-id="30282-111">Aqui está um resumo das operações do ponto de vista de Stoclien.exe como um cliente COM do servidor COM Stoserve.dll:</span><span class="sxs-lookup"><span data-stu-id="30282-111">Here is a summary of operations from the standpoint of Stoclien.exe as a COM client of the Stoserve.dll COM server:</span></span>

<dl> <dt>

<span data-ttu-id="30282-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Arquivo/abrir</span><span class="sxs-lookup"><span data-stu-id="30282-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>File/Open</span></span>
</dt> <dd>

<span data-ttu-id="30282-113">Mostra a caixa de diálogo abrir para obter um nome e um caminho para que um arquivo de desenho de papel existente seja aberto.</span><span class="sxs-lookup"><span data-stu-id="30282-113">Shows the Open dialog box to obtain a name and path for an existing paper drawing file to open.</span></span> <span data-ttu-id="30282-114">Um padrão. A extensão de nome de arquivo PAP para esses arquivos é assumida.</span><span class="sxs-lookup"><span data-stu-id="30282-114">A default .PAP file name extension for these files is assumed.</span></span> <span data-ttu-id="30282-115">Se forem feitas alterações no desenho existente quando esse item de menu for escolhido, uma caixa de diálogo separada será mostrada primeiro perguntando ao usuário se o desenho atual deve ser salvo em seu arquivo composto associado.</span><span class="sxs-lookup"><span data-stu-id="30282-115">If changes were made to the existing drawing when this menu item is chosen, a separate dialog will first be shown asking the user if the current drawing should be saved into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="30282-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Arquivo/salvar</span><span class="sxs-lookup"><span data-stu-id="30282-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>File/Save</span></span>
</dt> <dd>

<span data-ttu-id="30282-117">Salva o desenho atual em seu arquivo composto associado.</span><span class="sxs-lookup"><span data-stu-id="30282-117">Saves the current drawing into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="30282-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Arquivo/salvar como</span><span class="sxs-lookup"><span data-stu-id="30282-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>File/Save As</span></span>
</dt> <dd>

<span data-ttu-id="30282-119">Mostra a caixa de diálogo Salvar como para obter um nome e um caminho para um novo arquivo de desenho de papel a ser criado.</span><span class="sxs-lookup"><span data-stu-id="30282-119">Shows the Save As dialog box to obtain a name and path for a new paper drawing file to create.</span></span> <span data-ttu-id="30282-120">O desenho atual se torna o conteúdo salvo do novo arquivo e o novo arquivo se torna o novo arquivo composto associado para o desenho.</span><span class="sxs-lookup"><span data-stu-id="30282-120">The current drawing becomes the saved content of the new file, and the new file becomes the new associated compound file for the drawing.</span></span>

</dd> <dt>

<span data-ttu-id="30282-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Arquivo/sair</span><span class="sxs-lookup"><span data-stu-id="30282-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/Exit</span></span>
</dt> <dd>

<span data-ttu-id="30282-122">Sai de [StoClien](structured-storage-client-sample--stoclien-.md).</span><span class="sxs-lookup"><span data-stu-id="30282-122">Exits [StoClien](structured-storage-client-sample--stoclien-.md).</span></span>

</dd> <dt>

<span data-ttu-id="30282-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Desenhar/desenhar em</span><span class="sxs-lookup"><span data-stu-id="30282-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Draw/Drawing On</span></span>
</dt> <dd>

<span data-ttu-id="30282-124">Ativa o desenho entre o cliente [StoClien](structured-storage-client-sample--stoclien-.md) e o objeto de copapel no servidor.</span><span class="sxs-lookup"><span data-stu-id="30282-124">Turns on drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="30282-125">Esse comando bloqueia o objeto de copapel para uso exclusivo por esse cliente e impede que outros clientes acessem a mesma instância de papel no servidor.</span><span class="sxs-lookup"><span data-stu-id="30282-125">This command locks the COPaper object for exclusive use by this client and prevents other clients from accessing the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="30282-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Desenhar/desenhar</span><span class="sxs-lookup"><span data-stu-id="30282-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Draw/Drawing Off</span></span>
</dt> <dd>

<span data-ttu-id="30282-127">Desativa o desenho entre o cliente [StoClien](structured-storage-client-sample--stoclien-.md) e o objeto de copapel no servidor.</span><span class="sxs-lookup"><span data-stu-id="30282-127">Turns off drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="30282-128">Esse comando desbloqueia o copapel para uso exclusivo por esse cliente e permite que outros clientes acessem a mesma instância de papel no servidor.</span><span class="sxs-lookup"><span data-stu-id="30282-128">This command unlocks the COPaper for exclusive use by this client and allows other clients to access the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="30282-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Desenhar/redesenhar</span><span class="sxs-lookup"><span data-stu-id="30282-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Draw/Redraw</span></span>
</dt> <dd>

<span data-ttu-id="30282-130">Redesenha no cliente os dados de desenho atuais mantidos no objeto de copapel no servidor.</span><span class="sxs-lookup"><span data-stu-id="30282-130">Redraws in the client the current drawing data held in the COPaper object in the server.</span></span>

</dd> <dt>

<span data-ttu-id="30282-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Desenhar/apagar</span><span class="sxs-lookup"><span data-stu-id="30282-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Draw/Erase</span></span>
</dt> <dd>

<span data-ttu-id="30282-132">Apaga o conteúdo do desenho atual e limpa a imagem da janela.</span><span class="sxs-lookup"><span data-stu-id="30282-132">Erases the current drawing content and clears the window image.</span></span> <span data-ttu-id="30282-133">Seleção de menu: caneta/cor mostra a caixa de diálogo escolher cor para obter uma nova cor de caneta para desenhar.</span><span class="sxs-lookup"><span data-stu-id="30282-133">Menu Selection: Pen/Color Shows the Choose Color dialog box to obtain a new pen color for drawing.</span></span>

</dd> <dt>

<span data-ttu-id="30282-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Caneta/média</span><span class="sxs-lookup"><span data-stu-id="30282-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Pen/Medium</span></span>
</dt> <dd>

<span data-ttu-id="30282-135">Escolhe a largura média para o desenho.</span><span class="sxs-lookup"><span data-stu-id="30282-135">Chooses the medium width for drawing.</span></span> <span data-ttu-id="30282-136">Uma marca de seleção nessa opção de menu indica que a média é a largura da caneta atual.</span><span class="sxs-lookup"><span data-stu-id="30282-136">A check mark on this menu choice indicates that medium is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="30282-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Caneta/grossa</span><span class="sxs-lookup"><span data-stu-id="30282-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Pen/Thick</span></span>
</dt> <dd>

<span data-ttu-id="30282-138">Escolhe a largura espessa para desenhar.</span><span class="sxs-lookup"><span data-stu-id="30282-138">Chooses the thick width for drawing.</span></span> <span data-ttu-id="30282-139">Uma marca de seleção nessa opção de menu indica que a espessa é a largura atual da caneta.</span><span class="sxs-lookup"><span data-stu-id="30282-139">A check mark on this menu choice indicates that thick is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="30282-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Caneta/fina</span><span class="sxs-lookup"><span data-stu-id="30282-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Pen/Thin</span></span>
</dt> <dd>

<span data-ttu-id="30282-141">Escolhe a largura fina para desenhar.</span><span class="sxs-lookup"><span data-stu-id="30282-141">Chooses the thin width for drawing.</span></span> <span data-ttu-id="30282-142">Uma marca de seleção nessa opção de menu indica que a fina é a largura atual da caneta.</span><span class="sxs-lookup"><span data-stu-id="30282-142">A check mark on this menu choice indicates that thin is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="30282-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Coletor/conexão</span><span class="sxs-lookup"><span data-stu-id="30282-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/Connect</span></span>
</dt> <dd>

<span data-ttu-id="30282-144">Conecta a interface COPaperSink IPaperSink ao ponto de conexão do objeto copaper PaperSink.</span><span class="sxs-lookup"><span data-stu-id="30282-144">Connects the COPaperSink IPaperSink interface to the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="30282-145">A repintura da imagem de desenho atual no [StoClien](structured-storage-client-sample--stoclien-.md) depende da conexão do coletor.</span><span class="sxs-lookup"><span data-stu-id="30282-145">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="30282-146">Uma marca de seleção nessa opção de menu indica que a repintura está conectada.</span><span class="sxs-lookup"><span data-stu-id="30282-146">A check mark on this menu choice indicates that repainting is connected.</span></span>

</dd> <dt>

<span data-ttu-id="30282-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Coletor/desconexão</span><span class="sxs-lookup"><span data-stu-id="30282-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/Disconnect</span></span>
</dt> <dd>

<span data-ttu-id="30282-148">Desconecta a interface COPaperSink IPaperSink do objeto de copapel PaperSink ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="30282-148">Disconnects the COPaperSink IPaperSink interface from the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="30282-149">A repintura da imagem de desenho atual no [StoClien](structured-storage-client-sample--stoclien-.md) depende da conexão do coletor.</span><span class="sxs-lookup"><span data-stu-id="30282-149">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="30282-150">Uma marca de seleção nessa opção de menu indica que a repintura está desconectada.</span><span class="sxs-lookup"><span data-stu-id="30282-150">A check mark on this menu choice indicates that repainting is disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="30282-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Tutorial de ajuda/StoClien</span><span class="sxs-lookup"><span data-stu-id="30282-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Help/StoClien Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="30282-152">Abre o arquivo do tutorial STOCLIEN.HTM no navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="30282-152">Opens the STOCLIEN.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="30282-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Tutorial de ajuda/StoServe</span><span class="sxs-lookup"><span data-stu-id="30282-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Help/StoServe Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="30282-154">Abre o arquivo do tutorial STOSERVE.HTM no navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="30282-154">Opens the STOSERVE.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="30282-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Arquivo de origem de ajuda/leitura</span><span class="sxs-lookup"><span data-stu-id="30282-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Help/Read Source File</span></span>
</dt> <dd>

<span data-ttu-id="30282-156">Exibe a caixa de diálogo abrir para que você possa abrir um arquivo de origem desta lição ou de outra no bloco de notas do Windows.</span><span class="sxs-lookup"><span data-stu-id="30282-156">Displays the Open dialog box so you can open a source file from this lesson or another one in the Windows Notepad.</span></span>

</dd> <dt>

<span data-ttu-id="30282-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Ajuda/sobre StoClien</span><span class="sxs-lookup"><span data-stu-id="30282-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Help/About StoClien</span></span>
</dt> <dd>

<span data-ttu-id="30282-158">Exibe a caixa de diálogo sobre para este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30282-158">Displays the About dialog box for this application.</span></span>

</dd> </dl>

<span data-ttu-id="30282-159">O exemplo [StoClien](structured-storage-client-sample--stoclien-.md) usa muitos dos serviços e classes de utilitário fornecidos pelo [APPUTIL](./using-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="30282-159">The [StoClien](structured-storage-client-sample--stoclien-.md) sample uses many of the utility classes and services provided by [APPUTIL](./using-visual-studio.md).</span></span> <span data-ttu-id="30282-160">Para obter mais informações sobre [APPUTIL](./using-visual-studio.md), consulte o código-fonte da biblioteca [APPUTIL](./using-visual-studio.md) no diretório [APPUTIL](./using-visual-studio.md) irmão e Apputil.MD no diretório principal do tutorial.</span><span class="sxs-lookup"><span data-stu-id="30282-160">For more information about [APPUTIL](./using-visual-studio.md), see the [APPUTIL](./using-visual-studio.md) library source code in the sibling [APPUTIL](./using-visual-studio.md) directory and Apputil.md in the main tutorial directory.</span></span> <span data-ttu-id="30282-161">Para obter mais informações sobre [APPUTIL](./using-visual-studio.md), consulte [como criar exemplos](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="30282-161">For more information about [APPUTIL](./using-visual-studio.md), see [How to Build Samples](how-to-build-samples.md).</span></span>

 

 