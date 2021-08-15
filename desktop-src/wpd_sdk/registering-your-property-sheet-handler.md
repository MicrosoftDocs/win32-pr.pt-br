---
description: Registrando o manipulador de folha de propriedades
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: Registrando o manipulador de folha de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f1642c03a068a24b37cd5647bcdef63222ed2dbe5d78832daeea31e8abd67d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083530"
---
# <a name="registering-your-property-sheet-handler"></a>Registrando o manipulador de folha de propriedades

Para que o manipulador de folha de propriedades seja reconhecido pelo namespace WPD, você deve registrá-lo corretamente no Windows registro. As entradas de registro para um manipulador de folha de propriedades WPD são semelhantes às do shell, mas são registradas como tipos de arquivo especiais. Manipuladores de folha de propriedades WPD são registrados de acordo com o tipo de conteúdo que eles representam. Veja abaixo uma árvore de registro de exemplo para um manipulador de menu de contexto WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



O exemplo acima registra um manipulador personalizado com o namespace WPD. Quando um usuário clica com o botão direito do mouse em um arquivo de imagem em um dispositivo por meio do shell Windows e seleciona **Propriedades**, ele invoca esse manipulador de folha de propriedades. O namespace WPD usa o TIPO DE CONTEÚDO WPD \_ \_ para determinar quais manipuladores de folha de propriedades carregar. Se o tipo de conteúdo não fornecer uma classificação útil, o namespace carregará os manipuladores de folha de propriedades na chave do Registro **WPDPropSheet.Generic.** A tabela a seguir lista todas as classes de arquivo disponíveis para um manipulador de menu de contexto e quais tipos de conteúdo e extensões de arquivo elas representam.



| Chave do Registro                   | Tipo de conteúdo WPD                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPDContextMenu.Device**      | O registro nessa chave habilita o manipulador de menu de contexto no nível do dispositivo. (Clique com o botão direito do mouse em um dispositivo.)                   |
| **WPDContextMenu. Armazenamento**     | Registrar-se nessa chave habilita o manipulador de menu de contexto no nível de armazenamento. (Clique com o botão direito do mouse em um armazenamento.)                 |
| **WPDContextMenu.Folder**      | PASTA DE TIPO \_ \_ DE CONTEÚDO \_ WPD                                                                                                     |
| **WPDContextMenu.Image**       | IMAGEM DO TIPO \_ DE \_ CONTEÚDO \_ WPD                                                                                                      |
| **WPDContextMenu.Audio**       | ÁUDIO DO TIPO \_ \_ DE CONTEÚDO WPD \_                                                                                                      |
| **WPDContextMenu.Video**       | VÍDEO DO TIPO \_ \_ DE CONTEÚDO WPD \_                                                                                                      |
| **WPDContextMenu.Playlist**    | PLAYLIST DO TIPO DE CONTEÚDO WPD \_ \_ \_                                                                                                   |
| **WPDContextMenu.Document**    | DOCUMENTO DE TIPO \_ DE \_ CONTEÚDO \_ WPD                                                                                                   |
| **WPDContextMenu.Contact**     | CONTATO DO TIPO \_ DE \_ CONTEÚDO \_ WPD                                                                                                    |
| **WPDContextMenu.Email**       | EMAIL DO TIPO DE CONTEÚDO WPD \_ \_ \_                                                                                                      |
| **WPDContextMenu.Appointment** | COMPROMISSO DO TIPO DE CONTEÚDO WPD \_ \_ \_                                                                                                |
| **WPDContextMenu.Task**        | TAREFA TIPO \_ DE \_ CONTEÚDO \_ WPD                                                                                                       |
| **WPDContextMenu.Memo**        | MEMO DE \_ TIPO \_ DE CONTEÚDO \_ WPD                                                                                                       |
| **WPDContextMenu.ImageAlbum**  | WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM                                                                                               |
| **WPDContextMenu.AudioAlbum**  | ÁLBUM DE ÁUDIO DO \_ \_ TIPO DE \_ CONTEÚDO \_ WPD                                                                                               |
| **WPDContextMenu.VideoAlbum**  | ÁLBUM DE VÍDEO \_ DO \_ TIPO DE CONTEÚDO \_ WPD \_                                                                                               |
| **WPDContextMenu.MixedAlbum**  | WPD \_ CONTENT \_ TYPE \_ MIXED \_ CONTENT \_ ALBUM                                                                                      |
| **WPDContextMenu.Generic**     | TIPO DE CONTEÚDO WPD \_ \_ NÃO \_ ESPECIFICADO<br/> ARQUIVO GENÉRICO \_ DO TIPO \_ DE \_ CONTEÚDO \_ WPD<br/> PROGRAMA DE TIPO \_ DE \_ CONTEÚDO \_ WPD<br/> |



 

 

 




