---
description: 'Você pode usar o handle para um metadado aprimorado para realizar as seguintes tarefas:'
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: Operações de metadados aprimoradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5daf08ef5d8d48b81aea4daa5d2696ececec3fce44b1303c9ff7ccd692151a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250280"
---
# <a name="enhanced-metafile-operations"></a>Operações de metadados aprimoradas

Você pode usar o handle para um metadado aprimorado para realizar as seguintes tarefas:

-   Exibir a imagem armazenada em um metadado aprimorado.
-   Crie cópias de um metadado aprimorado.
-   Edite um metadado aprimorado.
-   Recupere a descrição opcional armazenada em um metadado aprimorado.
-   Recuperar uma cópia de um header de metadados aprimorado.
-   Recuperar uma versão binária de um metadado aprimorado.
-   Enumerar as cores na paleta opcional.

Essas tarefas são discutidas nas seções no restante deste tópico.

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>Exibir a imagem armazenada em um metadado aprimorado

Você pode exibir a imagem armazenada em um metadado aprimorado usando a [**função PlayEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) Passe a função um handle para o metarquivo aprimorado, sem se preocupar com o formato dos registros de metarquivo aprimorados. No entanto, às vezes é desejável enumerar os registros no metarquivo aprimorado para pesquisar uma função GDI específica e modificar os parâmetros da função de alguma maneira. Para fazer isso, você pode usar [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) e fornecer uma função de retorno de chamada, [**EnhMetaFileProc,**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)para processar os registros de metadados aprimorados. Para modificar os parâmetros de um registro de metarquivo aprimorado, você deve saber o formato dos parâmetros dentro do registro.

## <a name="create-copies-of-an-enhanced-metafile"></a>Criar cópias de um metadado aprimorado

Alguns aplicativos criam cópias temporárias de backup (ou duplicadas) de um arquivo antes de permitir que o usuário altere o original. Um aplicativo pode criar uma cópia de backup de um metadado aprimorado chamando a função [**CopyEnhMetaFile,**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) fornecendo um identificador que identifica o metadado aprimorado e fornecendo um ponteiro para o nome do novo arquivo.

Para criar um metarquivo de formato avançado baseado em memória, chame a [**função SetEnhMetaFileBits.**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)

## <a name="edit-an-enhanced-metafile"></a>Editar um metadado aprimorado

A maioria dos aplicativos cad (design auxiliado por computador), ilustração e desenho exigem um meio de editar uma imagem armazenada em um metadado aprimorado. Embora a edição de um metadado avançado seja uma tarefa complexa, você pode usar a função [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) em combinação com outras funções para fornecer essa funcionalidade em seu aplicativo. A **função EnumEnhMetaFile** e sua função de retorno de chamada associada, [**EnhMetaFileProc,**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)permitem que o aplicativo processe registros individuais em um metadado aprimorado.

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>Recuperar a descrição opcional armazenada em um metadado aprimorado

Alguns aplicativos exibem a descrição de texto de um metadado aprimorado com o nome de arquivo correspondente na **caixa de** diálogo Abrir. Você pode determinar se essa cadeia de caracteres existe em um metadado aprimorado recuperando o header de metadados com a [**função GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) e examinando um de seus membros. Se a cadeia de caracteres existir, o aplicativo a recuperará chamando a [**função GetEnhMetaFileDescription.**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>Recuperar uma versão binária de um metadado aprimorado

Você pode recuperar o conteúdo de um metadado chamando a [**função GetEnhMetaFileBits;**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) no entanto, antes de recuperar o conteúdo, você deve especificar o tamanho do arquivo. Para obter o tamanho, você pode usar a [**função GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) e examinar o membro apropriado.

## <a name="enumerate-the-colors-in-the-optional-palette"></a>Enumerar as cores na paleta opcional

Para obter cores consistentes quando uma imagem é exibida em vários dispositivos de saída, você pode chamar a função [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) e armazenar uma paleta lógica em um metadado aprimorado. Um aplicativo que exibe a imagem armazenada no metadado aprimorado recupera essa paleta e chama a [**função RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) antes de exibir a imagem. Para determinar se uma paleta é armazenada em um metadado aprimorado, recupere o header de metadados e examine o membro apropriado. Se houver uma paleta, você poderá chamar a [**função GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) para recuperar a paleta lógica.

 

 
