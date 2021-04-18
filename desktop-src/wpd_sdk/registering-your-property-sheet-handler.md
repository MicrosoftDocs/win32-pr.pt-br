---
description: Registrando seu manipulador de folha de propriedades
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: Registrando seu manipulador de folha de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a59a03ebd13f5a541674012da7b07045e0a510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808300"
---
# <a name="registering-your-property-sheet-handler"></a>Registrando seu manipulador de folha de propriedades

Para que o manipulador de folha de propriedades seja reconhecido pelo namespace WPD, você deve registrá-lo corretamente no registro do Windows. As entradas de registro para um manipulador de folhas de propriedades WPD são semelhantes às do Shell, mas são registradas como tipos de arquivo especiais. Os manipuladores de folha de propriedades WPD são registrados de acordo com o tipo de conteúdo que representam. Veja abaixo uma árvore de registro de exemplo para um manipulador de menu de contexto WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



O exemplo acima registra um manipulador personalizado com o namespace WPD. Quando um usuário clica com o botão direito do mouse em um arquivo de imagem em um dispositivo por meio do shell do Windows e seleciona **Propriedades**, ele invoca esse manipulador de folha de propriedades. O namespace WPD usa o \_ tipo de conteúdo WPD \_ para determinar quais manipuladores de folha de propriedades carregar. Se o tipo de conteúdo não fornecer uma classificação útil, o namespace carregará os manipuladores de folha de propriedades na chave **do registro WPDPropSheet. Generic** . A tabela a seguir lista todas as classes de arquivo disponíveis para um manipulador de menu de contexto e quais tipos de conteúdo e extensões de arquivo elas representam.



| Chave do Registro                   | Tipo de conteúdo WPD                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPDContextMenu. Device**      | O registro sob essa chave habilita o manipulador de menu de contexto no nível do dispositivo. (Clique com o botão direito do mouse em um dispositivo).                   |
| **WPDContextMenu. Storage**     | O registro sob essa chave habilita o manipulador de menu de contexto no nível de armazenamento. (Clique com o botão direito do mouse em um armazenamento).                 |
| **WPDContextMenu. pasta**      | \_pasta de \_ tipo de conteúdo WPD \_                                                                                                     |
| **WPDContextMenu. Image**       | \_imagem de \_ tipo de conteúdo WPD \_                                                                                                      |
| **WPDContextMenu. Audio**       | \_áudio de \_ tipo de conteúdo WPD \_                                                                                                      |
| **WPDContextMenu. Video**       | \_vídeo de \_ tipo de conteúdo WPD \_                                                                                                      |
| **WPDContextMenu. playlist**    | \_playlist de \_ tipo de conteúdo WPD \_                                                                                                   |
| **WPDContextMenu.Document**    | \_documento de \_ tipo de conteúdo WPD \_                                                                                                   |
| **WPDContextMenu. Contact**     | \_contato de \_ tipo de conteúdo WPD \_                                                                                                    |
| **WPDContextMenu.Email**       | \_email de \_ tipo de conteúdo WPD \_                                                                                                      |
| **WPDContextMenu. compromisso** | \_compromisso de \_ tipo de conteúdo WPD \_                                                                                                |
| **WPDContextMenu. Task**        | \_tarefa de \_ tipo de conteúdo WPD \_                                                                                                       |
| **WPDContextMenu. Memo**        | \_memorando de \_ tipo de conteúdo WPD \_                                                                                                       |
| **WPDContextMenu.ImageAlbum**  | \_álbum de \_ imagem de tipo de conteúdo WPD \_ \_                                                                                               |
| **WPDContextMenu.AudioAlbum**  | \_álbum de \_ áudio do tipo de conteúdo WPD \_ \_                                                                                               |
| **WPDContextMenu.VideoAlbum**  | \_álbum de \_ vídeo do tipo de conteúdo WPD \_ \_                                                                                               |
| **WPDContextMenu.MixedAlbum**  | tipo de conteúdo WPD- \_ \_ \_ álbum de \_ conteúdo misto \_                                                                                      |
| **WPDContextMenu. Generic**     | \_tipo de conteúdo WPD \_ \_ não especificado<br/> \_ \_ arquivo genérico de tipo de conteúdo WPD \_ \_<br/> \_programa de \_ tipo de conteúdo WPD \_<br/> |



 

 

 




