---
title: Ícones (menus e outros recursos)
description: Esta seção aborda os ícones que são imagens de bitmap combinadas com uma máscara para criar áreas transparentes na imagem.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\icons.htm
keywords:
- recursos, ícones
- ícones, sobre
- RT_ICON recurso
- RT_GROUP_ICON recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c96e740c23bb61cfdaa6cfbcbf6d0ce7538586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369161"
---
# <a name="icons-menus-and-other-resources"></a>Ícones (menus e outros recursos)

Um *ícone* é uma imagem que consiste em uma imagem de bitmap combinada com uma máscara para criar áreas transparentes na imagem. O ícone de termo pode se referir a um dos seguintes:

-   Uma única imagem de ícone. Este é um recurso do tipo **RT \_ ícone**.
-   Um grupo de imagens, do qual o sistema ou um aplicativo pode escolher o ícone mais apropriado com base no tamanho e na profundidade da cor. Esse é um recurso do **ícone de \_ grupo \_** de tipo RT.

### <a name="in-this-section"></a>Nesta seção



| Nome                                 | Descrição                                                 |
|--------------------------------------|-------------------------------------------------------------|
| [Sobre ícones](about-icons.md)       | Discute ícones.<br/>                                 |
| [Usando ícones](using-icons.md)       | Discute como executar tarefas relacionadas a ícones.<br/> |
| [Referência de ícone](icon-reference.md) | Contém a referência de API.<br/>                      |



 

### <a name="icon-functions"></a>Funções de ícone



| Nome                                                               | Descrição                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon)                                       | Copia o ícone especificado de outro módulo para o módulo atual. <br/>                                                                                                                                      |
| [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon)                                   | Cria um ícone que tem o tamanho, as cores e os padrões de bits especificados. <br/>                                                                                                                                    |
| [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource)           | Cria um ícone ou cursor de bits de recurso que descreve o ícone.<br/>                                                                                                                                          |
| [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)       | Cria um ícone ou cursor de bits de recurso que descreve o ícone. <br/>                                                                                                                                         |
| [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)                   | Cria um ícone ou cursor a partir de uma estrutura [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . <br/>                                                                                                                                 |
| [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                 | Destrói um ícone e libera qualquer memória do ícone ocupado. <br/>                                                                                                                                                  |
| [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)                                       | Desenha um ícone ou cursor no contexto do dispositivo especificado.<br/>                                                                                                                                                 |
| [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex)                                   | Desenha um ícone ou cursor no contexto do dispositivo especificado, executando as operações de varredura especificadas e alongando ou compactando o ícone ou cursor conforme especificado. <br/>                                     |
| [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon)                             | Cria uma duplicata de um ícone especificado.<br/>                                                                                                                                                                   |
| [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona)             | Recupera um identificador para um ícone indexado encontrado em um arquivo ou um ícone encontrado em um arquivo executável associado. <br/>                                                                                                  |
| [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)                                 | Recupera um identificador para um ícone do arquivo executável especificado, DLL ou arquivo de ícone.<br/>                                                                                                                        |
| [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)                             | Cria uma matriz de identificadores para ícones grandes ou pequenos extraídos do arquivo executável especificado, DLL ou arquivo de ícone. <br/>                                                                                      |
| [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo)                                 | Recupera informações sobre o ícone ou cursor especificado. <br/>                                                                                                                                                 |
| [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa)                             | Recupera informações sobre o ícone ou cursor especificado. [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa) estende [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) usando a estrutura [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa) mais recente.<br/> |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                                       | Carrega o recurso de ícone especificado do arquivo executável (. exe) associado a uma instância do aplicativo.<br/>                                                                                                 |
| [**LookupIconIdFromDirectory**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectory)     | Pesquisa dados de ícone ou cursor para o ícone ou cursor que melhor se adapta ao dispositivo de vídeo atual.<br/>                                                                                                     |
| [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) | Pesquisa dados de ícone ou cursor para o ícone ou cursor que melhor se adapta ao dispositivo de vídeo atual. <br/>                                                                                                    |
| [**PrivateExtractIcons**](/windows/desktop/api/Winuser/nf-winuser-privateextracticonsa)                 | Cria uma matriz de identificadores para ícones que são extraídos de um arquivo especificado.<br/>                                                                                                                             |



 

### <a name="icon-structures"></a>Estruturas de ícone



| Nome                               | Descrição                                                                                                                                                                                                                                     |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo)       | Contém informações sobre um ícone ou um cursor. <br/>                                                                                                                                                                                     |
| [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa)   | Contém informações sobre um ícone ou um cursor. Estende [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo). Usado por [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa).<br/>                                                                                                |
| [**ICONMETRICS**](/windows/win32/api/winuser/ns-winuser-iconmetricsa) | Contém as métricas escalonáveis associadas a ícones. Essa estrutura é usada com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) quando a ação **SPI \_ GETICONMETRICS** ou **SPI \_ SETICONMETRICS** é especificada.<br/> |



 

 

