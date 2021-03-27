---
description: Quando um usuário clica com o botão direito do mouse em um objeto do Shell, o menu de atalho que é exibido normalmente inclui um item de propriedades.
title: Manipuladores de folha de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 40ccb8d1cee0fffb993aef417b979816597cf707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828905"
---
# <a name="property-sheet-handlers"></a>Manipuladores de folha de propriedades

Quando um usuário clica com o botão direito do mouse em um objeto do Shell, o menu de atalho que é exibido normalmente inclui um item de **Propriedades** . A seleção desse item inicia uma folha de propriedades que permite ao usuário exibir e, em alguns casos, modificar as propriedades do objeto. Você pode personalizar essa folha de propriedades implementando e registrando um *manipulador de folha de propriedades*.

Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](handlers.md). Este documento se concentra nesses aspectos da implementação que são específicos de manipuladores de folha de propriedades.

-   [Como funcionam os manipuladores de folha de propriedades](#how-property-sheet-handlers-work)
-   [Registrando e implementando um manipulador de folha de propriedades para uma unidade montada](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [Tópicos relacionados](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>Como funcionam os manipuladores de folha de propriedades

A ilustração a seguir mostra a folha de propriedades Propriedades de um arquivo de texto do Windows XP.

![folha de propriedades](images/propsheethandler1.jpg)

Esta ilustração mostra a folha de propriedades de propriedades padrão que é exibida para qualquer arquivo. Para muitas dessas folhas de propriedades, você pode adicionar uma ou mais páginas à folha de propriedades implementando e registrando um manipulador de folhas de propriedades.

Manipuladores de folha de propriedades geralmente são registrados para um [tipo de arquivo](fa-file-types.md). Cada manipulador pode adicionar uma página personalizada à folha de propriedades de propriedades para a classe. Essas páginas normalmente dão aos usuários acesso a propriedades que são específicas para o tipo de arquivo específico. Um tipo de arquivo que consiste em documentos de texto pode, por exemplo, exibir uma página que liste o título e o autor e um resumo do documento. Um caso especial desse tipo de manipulador de folhas de propriedades é usado para adicionar uma página à folha de propriedades de propriedades de uma unidade montada.

O outro uso para manipuladores de folha de propriedades é substituir páginas nas folhas de propriedades exibidas por aplicativos do painel de controle. Um fabricante de mouse, por exemplo, pode usar um manipulador de folha de propriedades para substituir a página **botões** da folha de propriedades **Propriedades do mouse** do painel de controle por uma página que é personalizada para as características do seu mouse.

Como todos os manipuladores de extensão do Shell, os manipuladores de folha de propriedades são objetos COM (Component Object Model) em processo implementados como DLLs. Eles devem exportar duas interfaces além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext).

A interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) é usada pelo shell para inicializar o manipulador. Quando o Shell chama [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), ele passa um objeto de dados com o nome do objeto e o ponteiro para uma PIDL (lista de identificadores de item) da pasta que contém o arquivo. O parâmetro *hRegKey* não é usado com manipuladores de folha de propriedades. O método **IShellExtInit:: Initialize** deve extrair o nome do arquivo do objeto de dados e armazenar o nome e o PIDL da pasta para uso posterior. Para obter mais detalhes, consulte a seção *implementando IShellExtInit* de [criando manipuladores de extensão de shell](handlers.md).

O restante da operação ocorre por meio da interface [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) do manipulador. Se a folha de propriedades estiver associada a um tipo de arquivo, o Shell chamará [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) para permitir que o manipulador adicione uma página à folha de propriedades. Se a folha de propriedades estiver associada a um aplicativo do painel de controle, o Shell chamará [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) para permitir que o manipulador substitua uma página.

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>Registrando e implementando um manipulador de folha de propriedades para uma unidade montada

Cada unidade montada tem uma folha de propriedades que pode ser exibida pelo usuário. A ilustração a seguir mostra uma folha de propriedades de propriedades para uma unidade de CD-ROM.

![folha de propriedades Propriedades de CD-ROM](images/propsheethandler2.jpg)

Há uma ampla variedade de dispositivos que podem ser montados como unidades. Como a folha de propriedades padrão, projetada para unidades de disco, pode não ser suficiente para alguns dispositivos, um manipulador de folhas de propriedades pode ser implementado para adicionar uma página específica ao dispositivo montado. A implementação básica desse tipo de manipulador de folhas de propriedades é idêntica à discutida em [como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md), com duas exceções.

-   O objeto de dados passado para o método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) do manipulador pode conter o caminho da unidade no formato [CFSTR \_ MOUNTEDVOLUME](clipboard.md) em vez do formato [CF \_ HDROP](clipboard.md) . O \_ formato CF HDROP é usado quando o dispositivo é montado em uma letra de unidade. O \_ formato CFSTR MOUNTEDVOLUME é usado com sistemas de arquivos NTFS quando o dispositivo remoto é montado em uma pasta em vez de uma letra de unidade.
-   O GUID do manipulador é registrado na chave do **HKEY \_ classes \_ raiz** \\  \\ **shellex** \\ **PropertySheetHandlers** Key.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[Como registrar e implementar um manipulador de folha de propriedades para um aplicativo do painel de controle](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
