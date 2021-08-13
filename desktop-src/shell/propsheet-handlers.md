---
description: Quando um usuário clica com o botão direito do mouse em um objeto Shell, o menu de atalho exibido normalmente inclui um item Propriedades.
title: Manipuladores de folha de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 27327db4718430ba646d9566227116e304d4d5f5770d0119987b32e0cd2adce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719538"
---
# <a name="property-sheet-handlers"></a>Manipuladores de folha de propriedades

Quando um usuário clica com o botão direito do mouse em um objeto Shell, o menu de atalho exibido normalmente inclui um item **Propriedades.** A seleção desse item inicia uma folha de propriedades que permite que o usuário veja e, em alguns casos, modifique as propriedades do objeto. Você pode personalizar essa folha de propriedades implementando e registrando um manipulador *de folha de propriedades*.

Os procedimentos gerais para implementar e registrar um manipulador de extensão do Shell são discutidos em Criando manipuladores de [extensão do Shell.](handlers.md) Este documento se concentra nos aspectos da implementação que são específicos para manipuladores de folha de propriedades.

-   [Como os manipuladores de folha de propriedades funcionam](#how-property-sheet-handlers-work)
-   [Registrando e implementando um manipulador de folha de propriedades para uma unidade montada](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [Tópicos relacionados](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>Como os manipuladores de folha de propriedades funcionam

A ilustração a seguir mostra a folha de propriedades Propriedades de um Windows de texto XP.

![folha de propriedades](images/propsheethandler1.jpg)

Esta ilustração mostra a folha de propriedades Propriedades padrão que é exibida para qualquer arquivo. Para muitas dessas folhas de propriedades, você pode adicionar uma ou mais páginas à folha de propriedades implementando e registrando um manipulador de folha de propriedades.

Manipuladores de folha de propriedades são mais comumente registrados para um [tipo de arquivo](fa-file-types.md). Cada manipulador pode adicionar uma página personalizada à folha de propriedades Propriedades da classe . Normalmente, essas páginas dão aos usuários acesso a propriedades específicas ao tipo de arquivo específico. Um tipo de arquivo que consiste em documentos de texto pode, por exemplo, exibir uma página que listou o título e o autor e um resumo do documento. Um caso especial desse tipo de manipulador de folha de propriedades é usado para adicionar uma página à folha de propriedades Propriedades de uma unidade montada.

O outro uso para manipuladores de folha de propriedades é substituir páginas nas folhas de propriedades exibidas por Painel de Controle aplicativos. Um fabricante do mouse, por exemplo, pode usar um manipulador de folha de propriedades para substituir a página Botões na folha de propriedades Propriedades do **Mouse** do Painel de Controle por uma página personalizada para as **características** do mouse.

Como todos os manipuladores de extensão do Shell, os manipuladores de folha de propriedades são objetos COM (Component Object Model em processo) implementados como DLLs. Eles devem exportar duas interfaces além de [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)

A interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) é usada pelo Shell para inicializar o manipulador. Quando o Shell chama [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), ele passa um objeto de dados com o nome do objeto e o ponteiro para uma PIDL (lista de identificadores de item) da pasta que contém o arquivo. O *parâmetro hRegKey* não é usado com manipuladores de folha de propriedades. O **método IShellExtInit::Initialize** deve extrair o nome do arquivo do objeto de dados e armazenar o nome e o PIDL da pasta para uso posterior. Para obter mais detalhes, consulte *a seção Implementando IShellExtInit* em Criando manipuladores de [extensão de shell.](handlers.md)

O restante da operação ocorre por meio da interface [**IShellPropSheetExt do**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) manipulador. Se a folha de propriedades estiver associada a um tipo de arquivo, o Shell [**chamará IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) para permitir que o manipulador adicione uma página à folha de propriedades. Se a folha de propriedades estiver associada a um aplicativo Painel de Controle, o Shell chamará [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) para permitir que o manipulador substitua uma página.

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>Registrando e implementando um manipulador de folha de propriedades para uma unidade montada

Cada unidade montada tem uma folha Propriedades que pode ser exibida pelo usuário. A ilustração a seguir mostra uma folha de propriedades Propriedades para uma unidade CD-ROM.

![folha de propriedades de cd-rom](images/propsheethandler2.jpg)

Há uma ampla variedade de dispositivos que podem ser montados como unidades. Como a folha de propriedades padrão, projetada para unidades de disco, pode não ser suficiente para alguns dispositivos, um manipulador de folha de propriedades pode ser implementado para adicionar uma página específica ao dispositivo montado. A implementação básica desse tipo de manipulador de folha de propriedades é idêntica à discutida em How [to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md), com duas exceções.

-   O objeto de dados passado para o método [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) do manipulador pode conter o caminho da unidade no formato [CFSTR \_ MOUNTEDVOLUME](clipboard.md) em vez do [formato CF \_ HDROP.](clipboard.md) O formato \_ CF HDROP é usado quando o dispositivo é montado em uma letra da unidade. O formato CFSTR MOUNTEDVOLUME é usado com sistemas de arquivos NTFS quando o dispositivo remoto é montado em uma pasta em vez de em uma \_ letra da unidade.
-   O GUID do manipulador é registrado na chave **HKEY \_ CLASSES \_ ROOT** \\ **Drive** \\ **shellex** \\ **PropertySheetHandlers.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[Como registrar e implementar um manipulador de folha de propriedades para um Painel de Controle aplicativo](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
