---
description: 'Você pode usar o identificador para um metarquivo avançado para realizar as seguintes tarefas:'
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: Operações de metarquivo aprimoradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ba9e2ac2f14c4436c039a66cc3211b471c0461
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091186"
---
# <a name="enhanced-metafile-operations"></a>Operações de metarquivo aprimoradas

Você pode usar o identificador para um metarquivo avançado para realizar as seguintes tarefas:

-   Exiba a imagem armazenada em um metarquivo avançado.
-   Crie cópias de um metarquivo avançado.
-   Edite um metarquivo avançado.
-   Recupere a descrição opcional armazenada em um metarquivo avançado.
-   Recupere uma cópia de um cabeçalho Enhanced-Metafile.
-   Recuperar uma versão binária de um metarquivo avançado.
-   Enumere as cores na paleta opcional.

Essas tarefas são discutidas nas seções no restante deste tópico.

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>Exibir a imagem armazenada em um metarquivo avançado

Você pode exibir a imagem armazenada em um metarquivo avançado usando a função [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) . Passe a função um identificador para o metarquivo avançado, sem se preocupar com o formato dos registros de metarquivo aprimorados. No entanto, às vezes é desejável enumerar os registros no metarquivo avançado para pesquisar uma função GDI específica e modificar os parâmetros da função de alguma maneira. Para fazer isso, você pode usar [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) e fornecer uma função de retorno de chamada, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), para processar os registros de metarquivo avançados. Para modificar os parâmetros de um registro de metarquivo avançado, você deve saber o formato dos parâmetros no registro.

## <a name="create-copies-of-an-enhanced-metafile"></a>Criar cópias de um metarquivo avançado

Alguns aplicativos criam cópias de backup temporário (ou duplicadas) de um arquivo antes de permitir que o usuário altere o original. Um aplicativo pode criar uma cópia de backup de um metarquivo avançado chamando a função [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) , fornecendo um identificador que identifica o metarquivo avançado e fornecendo um ponteiro para o nome do novo arquivo.

Para criar um metarquivo de formato avançado baseado em memória, chame a função [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits) .

## <a name="edit-an-enhanced-metafile"></a>Editar um metarquivo avançado

A maioria dos aplicativos de desenho, ilustração e desenvolvimento auxiliado por computador (CAD) exigem um meio de editar uma imagem armazenada em um metarquivo avançado. Embora a edição de um metarquivo avançado seja uma tarefa complexa, você pode usar a função [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) em combinação com outras funções para fornecer esse recurso em seu aplicativo. A função **EnumEnhMetaFile** e sua função de retorno de chamada associada, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), permitem que o aplicativo processe registros individuais em um metarquivo avançado.

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>Recuperar a descrição opcional armazenada em um metarquivo avançado

Alguns aplicativos exibem a descrição de texto de um metarquivo avançado com o nome de arquivo correspondente na caixa de diálogo **abrir** . Você pode determinar se essa cadeia de caracteres existe em um metarquivo avançado recuperando o cabeçalho do metarquivo com a função [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) e examinando um de seus membros. Se a cadeia de caracteres existir, o aplicativo a recuperará chamando a função [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona) .

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>Recuperar uma versão binária de um metarquivo avançado

Você pode recuperar o conteúdo de um metarquivo chamando a função [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) ; no entanto, antes de recuperar o conteúdo, você deve especificar o tamanho do arquivo. Para obter o tamanho, você pode usar a função [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) e examinar o membro apropriado.

## <a name="enumerate-the-colors-in-the-optional-palette"></a>Enumerar as cores na paleta opcional

Para obter cores consistentes quando uma imagem é exibida em vários dispositivos de saída, você pode chamar a função [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) e armazenar uma paleta lógica em um metarquivo avançado. Um aplicativo que exibe a imagem armazenada no metarquivo avançado recupera essa paleta e chama a função [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) antes de exibir a imagem. Para determinar se uma paleta é armazenada em um metarquivo avançado, recupere o cabeçalho do metarquivo e examine o membro apropriado. Se houver uma paleta, você poderá chamar a função [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) para recuperar a paleta lógica.

 

 
