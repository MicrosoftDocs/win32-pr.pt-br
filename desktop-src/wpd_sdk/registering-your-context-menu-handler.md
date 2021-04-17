---
description: Registrando seu manipulador de menu de contexto
ms.assetid: 0023004b-b6b3-486a-8b8c-8e63c5731206
title: Registrando seu manipulador de menu de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafd2798683b4bc291653bca34996f143fc36842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752585"
---
# <a name="registering-your-context-menu-handler"></a>Registrando seu manipulador de menu de contexto

Para que o manipulador de menu de contexto seja reconhecido pelo namespace WPD, você deve registrá-lo corretamente no registro do Windows. As entradas de registro para um manipulador de menu de contexto WPD são semelhantes às do Shell, mas são registradas como tipos de arquivo especiais. Os manipuladores de menu de contexto WPD são registrados de acordo com o tipo de conteúdo que representam. Veja abaixo uma árvore de registro de exemplo para um manipulador de menu de contexto WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDContextMenu.Image
      \-- shellex
           \-- ContextMenuHandlers
                \-- ShImageViewer (Default)  REG_SZ {E847DA7C-1D6A-45F6-B725-CB260C236066}

```



O exemplo acima registra o Visualizador de imagens do shell com o namespace WPD. Quando um usuário clica com o botão direito do mouse ou clica duas vezes no conteúdo de um dispositivo por meio do shell do Windows Vista, ele invoca esse manipulador de menu de contexto. O namespace WPD usa \_ \_ o tipo de conteúdo WPD para determinar quais manipuladores de menu de contexto carregar. Se o \_ tipo de conteúdo WPD \_ for igual ao \_ tipo de conteúdo WPD \_ \_ , não especificado, tipo de conteúdo WPD, \_ \_ \_ \_ arquivo genérico ou \_ \_ \_ programa de tipo de conteúdo WPD, o namespace WPD tentará encontrar a melhor correspondência com base na extensão do arquivo selecionado. Se nem a extensão de arquivo nem o tipo de conteúdo fornecerem uma classificação útil, o namespace WPD carregará os manipuladores de menu de contexto na chave do registro **WPDContextMenu. Generic** . A tabela a seguir lista todas as classes de arquivo disponíveis para um manipulador de menu de contexto e quais tipos de conteúdo e extensões de arquivo eles representam:



| Chave do Registro                           | Tipo de conteúdo WPD                                                                                               | Extensão do arquivo                                                                                           |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **WPDContextMenu. Device**              | O registro sob essa chave habilita o manipulador de menu de contexto no nível do dispositivo. (Clique com o botão direito do mouse em um dispositivo).   | (N/D)                                                                                                    |
| **WPDContextMenu. Storage**             | O registro sob essa chave habilita o manipulador de menu de contexto no nível de armazenamento. (Clique com o botão direito do mouse em um armazenamento). | (N/D)                                                                                                    |
| **WPDContextMenu. pasta**              | \_pasta de \_ tipo de conteúdo WPD \_                                                                                     | (N/D)                                                                                                    |
| **WPDContextMenu. Image**               | \_imagem de \_ tipo de conteúdo WPD \_                                                                                      | .bmp <br/> .gif <br/> .png <br/> .jpg <br/> .jpe <br/> .jpeg <br/>   |
| **WPDContextMenu. Audio**               | \_áudio de \_ tipo de conteúdo WPD \_                                                                                      | .aiff <br/> .mp3 <br/> .wav <br/> .wma <br/>                                     |
| **WPDContextMenu. Video**               | \_vídeo de \_ tipo de conteúdo WPD \_                                                                                      | .asf<br/> .avi <br/> . DVR-MS <br/> .mpeg <br/> .mpg <br/> .wmv <br/> |
| **WPDContextMenu. playlist**<br/> | \_playlist de \_ tipo de conteúdo WPD \_                                                                                   | . wpl <br/> .m3u <br/> .mpl <br/> .asx <br/> . pls <br/>                     |
| **WPDContextMenu.Document**            | \_documento de \_ tipo de conteúdo WPD \_                                                                                   | .doc <br/> .txt <br/> .rtf <br/> .xls <br/> .ppt <br/>                     |
| **WPDContextMenu. Contact**<br/>  | \_contato de \_ tipo de conteúdo WPD \_                                                                                    | Nenhum                                                                                                     |
| **WPDContextMenu.Email**               | \_email de \_ tipo de conteúdo WPD \_                                                                                      | Nenhum                                                                                                     |
| **WPDContextMenu. compromisso**         | \_compromisso de \_ tipo de conteúdo WPD \_                                                                                | Nenhum                                                                                                     |
| **WPDContextMenu. Task**                | \_tarefa de \_ tipo de conteúdo WPD \_                                                                                       | Nenhum                                                                                                     |
| **WPDContextMenu. Memo**                | \_memorando de \_ tipo de conteúdo WPD \_                                                                                       | Nenhum                                                                                                     |
| **WPDContextMenu.ImageAlbum**          | \_álbum de \_ imagem de tipo de conteúdo WPD \_ \_                                                                               | Nenhum                                                                                                     |
| **WPDContextMenu.AudioAlbum**          | \_álbum de \_ áudio do tipo de conteúdo WPD \_ \_                                                                               | Nenhum                                                                                                     |
| **WPDContextMenu.VideoAlbum**          | \_álbum de \_ vídeo do tipo de conteúdo WPD \_ \_                                                                               | Nenhum                                                                                                     |
| **WPDContextMenu.MixedAlbum**          | tipo de conteúdo WPD- \_ \_ \_ álbum de \_ conteúdo misto \_                                                                      | Nenhum                                                                                                     |
| **WPDContextMenu. Generic**             | \_tipo de conteúdo WPD \_ \_ não especificado                                                                                | Todas as outras extensões de arquivo                                                                                |



 

 

 




