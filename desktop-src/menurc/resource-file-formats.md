---
title: Formatos de arquivo de recurso
description: Esta seção descreve o formato do arquivo de recurso binário que o compilador de recurso cria com base no conteúdo do arquivo de definição de recurso.
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90c789cd1684c1f5ca31af0e2d60a31052ca03f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823756"
---
# <a name="resource-file-formats"></a>Formatos de arquivo de recurso

Esta seção descreve o formato do arquivo de recurso binário que o compilador de recurso cria com base no conteúdo do arquivo de definição de recurso. Esse arquivo geralmente tem uma extensão. res. O vinculador reformata o arquivo. res em um arquivo de objeto de recurso e o vincula ao arquivo executável de um aplicativo.

Um arquivo de recurso binário consiste em um número de entradas de recurso concatenadas. Cada entrada consiste em um cabeçalho de recurso e os dados para esse recurso. Um cabeçalho de recurso é alinhado em **DWORD** no arquivo e consiste no seguinte:

-   Um **DWORD** que contém o tamanho do cabeçalho do recurso
-   Um **DWORD** que contém o tamanho dos dados do recurso
-   O tipo de recurso
-   O nome do recurso
-   Informações adicionais sobre recursos

A estrutura [**RESOURCEHEADER**](resourceheader.md) descreve o formato desse cabeçalho. Os dados do recurso seguem o cabeçalho do recurso e são específicos de cada tipo de recurso. Alguns recursos também empregam uma estrutura de cabeçalho de grupo específica do recurso para fornecer informações sobre um grupo de recursos.

## <a name="accelerator-table-resources"></a>Recursos de tabela de acelerador

Uma tabela de acelerador é uma entrada de recurso em um arquivo de recurso. Ele não tem um cabeçalho de grupo. Uma estrutura [**ACCELTABLEENTRY**](acceltableentry.md) descreve cada entrada na tabela do acelerador. Várias tabelas de acelerador são permitidas.

## <a name="cursor-and-icon-resources"></a>Recursos de cursor e ícone

O sistema trata cada ícone e cursor como um único arquivo. No entanto, eles são armazenados em arquivos. res e em arquivos executáveis como um grupo de recursos de ícone ou um grupo de recursos de cursor. Os formatos de arquivo dos recursos de ícone e cursor são semelhantes. No arquivo. res, um cabeçalho do grupo de recursos segue todos os componentes individuais de ícone ou grupo de cursores.

O formato de cada componente de ícone é parecido com o formato do arquivo. ico. Cada imagem de ícone é armazenada em uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguida pelos bits DIB (bitmap independente de cor) da máscara **XOR** do ícone. Os bits DIB monocromáticos do ícone **e** da máscara seguem os bits de cor DIB.

O formato de cada componente de cursor se assemelha ao formato do arquivo. cur. Cada imagem de cursor é armazenada em uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguida pelos bits DIB monocromáticos da máscara **XOR** do cursor e, em seguida, pelos bits DIB monocromáticos do cursor **e** da máscara. Observe que há uma diferença nos bitmaps dos dois recursos: ao contrário dos ícones, as máscaras XOR do cursor não têm bits DIB de cor. Embora os bitmaps das máscaras de cursor sejam monocromáticos e não tenham cabeçalhos DIB ou tabelas de cores, os bits ainda estão no formato DIB em relação ao alinhamento e à direção. Outra diferença significativa entre cursores e ícones é que os cursores têm um ponto de interativação e os ícones não.

O cabeçalho de grupo para os recursos de ícone e cursor consiste em uma estrutura [**NEWHEADER**](newheader.md) , além de uma ou mais estruturas [**RESDIR**](resdir.md) . Há uma estrutura **RESDIR** para cada ícone ou cursor. O cabeçalho do grupo contém as informações de que um aplicativo precisa para selecionar o ícone ou o cursor correto a ser exibido. O cabeçalho do grupo e os dados que se repetem para cada ícone ou cursor no grupo têm um comprimento fixo. Isso permite que o aplicativo acesse as informações aleatoriamente.

## <a name="dialog-box-resources"></a>Recursos da caixa de diálogo

Uma caixa de diálogo também é uma entrada de recurso no arquivo de recurso. Ele consiste em uma estrutura de cabeçalho da caixa de diálogo [**DLGTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) mais uma estrutura [**DLGITEMTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) para cada controle na caixa de diálogo. As estruturas [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) e [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) descrevem o formato dos recursos estendidos da caixa de diálogo.

## <a name="font-resources"></a>Recursos de fonte

As fontes são armazenadas no arquivo de recursos como um grupo de recursos. Fontes individuais compõem um grupo de fontes. Uma instrução de definição de recurso de [instrução de fonte](./font-statement.md) no. O arquivo RC define cada fonte. Cada fonte individual no recurso consiste no conteúdo completo do arquivo. fnt relacionado. Uma estrutura [**FONTGROUPHDR**](fontgrouphdr.md) segue todos os componentes de fonte individuais no arquivo. res.

Os recursos de fonte não são adicionados aos recursos de um aplicativo específico. Em vez disso, eles são normalmente adicionados a arquivos executáveis que têm uma extensão. Fon. Esses arquivos normalmente são DLLs somente de recursos em vez de aplicativos.

## <a name="menu-resources"></a>Recursos de menu

Um *recurso de menu* consiste em uma estrutura [**MENUHEADER**](menuheader.md) seguida por uma ou mais estruturas [**NORMALMENUITEM**](normalmenuitem.md) ou [**POPUPMENUITEM**](popupmenuitem.md) , uma para cada item de menu no modelo de menu. O [**\_ \_ cabeçalho do modelo MENUEX**](menuex-template-header.md) e as estruturas de [**\_ \_ item de modelo MENUEX**](menuex-template-item.md) descrevem o formato dos recursos de menu estendidos.

## <a name="message-table-resources"></a>Recursos de tabela de mensagens

Uma *tabela de mensagens* é um recurso que contém texto formatado para exibição como uma mensagem de erro ou em uma caixa de mensagem. A estrutura principal em um recurso de tabela de mensagens é a estrutura de [**\_ \_ dados do recurso de mensagem**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data) .

## <a name="version-resources"></a>Recursos de versão

A estrutura principal em um recurso de versão é a estrutura do [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Estruturas adicionais incluem a estrutura [**VarFileInfo**](varfileinfo.md) para armazenar dados de informações de idioma e [**StringFileInfo**](stringfileinfo.md) para informações de cadeias de caracteres definidas pelo usuário. Todas as cadeias de caracteres em um recurso de versão estão no formato Unicode. Cada bloco de informações é alinhado em um limite **DWORD** .

 

 