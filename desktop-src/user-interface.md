---
description: Esta seção fornece diretrizes para integrar e estender os recursos voltados para o usuário da área de trabalho do Windows.
ms.assetid: 1ffeeb4f-b337-45b9-885f-307b81670557
title: Ambiente de desktop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a86d8b979647ef9dfbedf1858c50bdd7db1b2a6b6ca02f9c6095fc43ee0104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966067"
---
# <a name="desktop-environment"></a>Ambiente de desktop

Esta seção fornece diretrizes para integrar e estender os recursos voltados para o usuário da área de trabalho do Windows. Você pode aprender a garantir que seus aplicativos e formatos de arquivo apareçam e se comportem corretamente no início, na barra de tarefas, na área de trabalho e no explorador de arquivos. Você também pode garantir que seus formatos de arquivo e armazenamentos de dados sejam indexáveis e pesquisáveis.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Shell](./shell/shell-entry.md)<br/>                                      | a interface do usuário do Windows desktop fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional. Os mais numerosos e familiares desses objetos são as pastas e os arquivos que residem nas unidades de disco do computador. Também há uma série de objetos virtuais que permitem ao usuário executar tarefas como enviar arquivos para impressoras remotas ou acessar a lixeira. O Shell organiza esses objetos em um namespace hierárquico e fornece aos usuários e aplicativos uma maneira consistente e eficiente de acessar e gerenciar objetos.<br/> |
| [Windows Sistema de propriedades](./properties/windows-properties-system.md)<br/>         | o sistema de propriedades Windows é um sistema de leitura/gravação extensível de definições de dados que fornece uma maneira uniforme de expressar metadados sobre itens de Shell. o sistema de propriedades Windows permite que você armazene e recupere metadados para itens de Shell. Um item de Shell é qualquer conteúdo único, como um arquivo, uma pasta, um email ou um contato. Uma propriedade é uma parte individual dos metadados associados a um item de Shell.<br/>                                                                                                                                                                             |
| [Windows Search](./search/windows-search.md)<br/>                                 | Windows A pesquisa é uma plataforma de pesquisa de desktop que tem recursos de pesquisa instantânea para os tipos de dados e de arquivo mais comuns, como email, contatos, compromissos de calendário, documentos, fotos, multimídia e outros formatos que podem ser estendidos por desenvolvedores de terceiros. Esses recursos permitem que os usuários encontrem, gerenciem e organizem a quantidade cada vez maior de dados comuns em ambientes corporativos e domésticos.<br/>                                                                                                                                                                                    |
| [Estações e desktops da janela](./winstation/window-stations-and-desktops.md)<br/> | Windows fornece três categorias principais de objetos: interface do usuário, interface gráfica do dispositivo (GDI) e kernel. Objetos de kernel são protegíveis, enquanto objetos de usuário e objetos GDI não são. Portanto, para fornecer segurança adicional, os objetos da interface do usuário são gerenciados usando estações de janela e áreas de trabalho, que são objetos protegíveis.<br/>                                                                                                                                                                                                                                              |
| [Ajuda do Windows](/windows/win32/api/winuser/nf-winuser-winhelpa)<br/>                                        | Descreve as tecnologias de ajuda disponíveis no Windows.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [Consoles](/windows/console/character-mode-applications)<br/>                        | Os consoles gerenciam entrada e saída (e/s) para aplicativos de modo de caractere (aplicativos que não fornecem sua própria interface gráfica do usuário).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Desenvolvimento da interface do usuário do aplicativo](./windows-application-ui-development.md)
</dt> </dl>

 

 
