---
title: Formatos de arquivo de recurso
description: Esta seção descreve o formato do arquivo de recurso binário que o compilador de recursos cria com base no conteúdo do arquivo de definição de recurso.
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bfc85190993992b7bf87001f3d807b777ed2fe27b4d66cba0b7f7c948d8cfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869787"
---
# <a name="resource-file-formats"></a>Formatos de arquivo de recurso

Esta seção descreve o formato do arquivo de recurso binário que o compilador de recursos cria com base no conteúdo do arquivo de definição de recurso. Esse arquivo geralmente tem uma extensão .res. O linker reformata o arquivo .res em um arquivo de objeto de recurso e, em seguida, vincula-o ao arquivo executável de um aplicativo.

Um arquivo de recurso binário consiste em várias entradas de recurso concatenadas. Cada entrada consiste em um header de recurso e os dados para esse recurso. Um header de recurso é alinhado a **DWORD** no arquivo e consiste no seguinte:

-   Um **DWORD** que contém o tamanho do header de recurso
-   Um **DWORD** que contém o tamanho dos dados do recurso
-   O tipo de recurso
-   O nome do recurso
-   Informações adicionais do recurso

A [**estrutura RESOURCEHEADER**](resourceheader.md) descreve o formato desse header. Os dados do recurso seguem o header do recurso e são específicos para cada tipo de recurso. Alguns recursos também empregam uma estrutura de header de grupo específica de recursos para fornecer informações sobre um grupo de recursos.

## <a name="accelerator-table-resources"></a>Recursos de tabela do acelerador

Uma tabela de acelerador é uma entrada de recurso em um arquivo de recurso. Ele não tem um header de grupo. Uma [**estrutura ACCELTABLEENTRY**](acceltableentry.md) descreve cada entrada na tabela do acelerador. Várias tabelas de acelerador são permitidas.

## <a name="cursor-and-icon-resources"></a>Recursos de cursor e ícone

O sistema trata cada ícone e cursor como um único arquivo. No entanto, eles são armazenados em arquivos .res e em arquivos executáveis como um grupo de recursos de ícone ou um grupo de recursos de cursor. Os formatos de arquivo de ícone e recursos de cursor são semelhantes. No arquivo .res, um header do grupo de recursos segue todos os componentes individuais do ícone ou do grupo de cursores.

O formato de cada componente de ícone é semelhante ao formato do arquivo .ico. Cada imagem de ícone é armazenada em uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguida pelos bits DIB (bitmap independente do dispositivo) da máscara **XOR do** ícone. Os bits DIB monocromáticos da máscara **AND** do ícone seguem os bits DIB de cor.

O formato de cada componente de cursor é semelhante ao formato do arquivo .cur. Cada imagem de cursor é armazenada em uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguida pelos bits DIB monocromáticos da máscara **XOR** do cursor e, em seguida, pelos bits DIB monocromáticos da máscara **AND** do cursor. Observe que há uma diferença nos bitmaps dos dois recursos: ao contrário dos ícones, as máscaras XOR do cursor não têm bits DIB de cor. Embora os bitmaps das máscaras de cursor sejam monocromáticos e não tenham headers DIB ou tabelas de cores, os bits ainda estão no formato DIB em relação ao alinhamento e à direção. Outra diferença significativa entre cursores e ícones é que os cursores têm um ponto de acesso e os ícones não têm.

O header de grupo para recursos de ícone e cursor consiste em uma estrutura [**NEWHEADER**](newheader.md) mais uma ou [**mais estruturas RESDIR.**](resdir.md) Há uma estrutura **RESDIR** para cada ícone ou cursor. O header do grupo contém as informações que um aplicativo precisa para selecionar o ícone ou cursor correto a ser exibido. O título do grupo e os dados que se repetem para cada ícone ou cursor no grupo têm um comprimento fixo. Isso permite que o aplicativo acesse aleatoriamente as informações.

## <a name="dialog-box-resources"></a>Recursos da caixa de diálogo

Uma caixa de diálogo também é uma entrada de recurso no arquivo de recurso. Ele consiste em uma estrutura de header de caixa de diálogo [**DLGTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) mais uma [**estrutura DLGITEMTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) para cada controle na caixa de diálogo. As [**estruturas DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) e [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) descrevem o formato dos recursos estendidos da caixa de diálogo.

## <a name="font-resources"></a>Recursos de fonte

As fontes são armazenadas no arquivo de recurso como um grupo de recursos. Fontes individuais comem um grupo de fontes. Uma [instrução de definição](./font-statement.md) de recurso de Instrução FONT no . O arquivo RC define cada fonte. Cada fonte individual no recurso consiste no conteúdo completo do arquivo .fnt relacionado. Uma [**estrutura FONTGROUPHDR**](fontgrouphdr.md) segue todos os componentes de fonte individuais no arquivo .res.

Os recursos de fonte não são adicionados aos recursos de um aplicativo específico. Em vez disso, eles normalmente são adicionados a arquivos executáveis que têm uma extensão .fon. Esses arquivos geralmente são DLLs somente de recurso em vez de aplicativos.

## <a name="menu-resources"></a>Recursos de menu

Um *recurso de menu* consiste em uma estrutura [**MENUHEADER**](menuheader.md) seguida por uma ou mais estruturas [**NORMALMENUITEM**](normalmenuitem.md) ou [**POPUPMENUITEM,**](popupmenuitem.md) uma para cada item de menu no modelo de menu. As [**estruturas MENUEX \_ TEMPLATE \_ HEADER**](menuex-template-header.md) e [**MENUEX TEMPLATE \_ \_ ITEM**](menuex-template-item.md) descrevem o formato dos recursos de menu estendidos.

## <a name="message-table-resources"></a>Recursos da tabela de mensagens

Uma *tabela de* mensagens é um recurso que contém texto formatado para exibição como uma mensagem de erro ou em uma caixa de mensagem. A estrutura principal em um recurso de tabela de mensagens é a [**estrutura \_ MESSAGE RESOURCE \_ DATA.**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data)

## <a name="version-resources"></a>Recursos de versão

A estrutura principal em um recurso de versão é a [**estrutura VS \_ FIXEDFILEINFO.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Estruturas adicionais incluem a [**estrutura VarFileInfo**](varfileinfo.md) para armazenar dados de informações de idioma e [**StringFileInfo**](stringfileinfo.md) para informações de cadeia de caracteres definidas pelo usuário. Todas as cadeias de caracteres em um recurso de versão estão no formato Unicode. Cada bloco de informações é alinhado em um **limite DWORD.**

 

 