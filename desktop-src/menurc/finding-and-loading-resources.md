---
title: Localizando e carregando recursos
description: Este tópico discute como carregar um recurso na memória.
ms.assetid: 9e56cfdd-b365-4433-a507-a30220b4a92d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca9590927cad28772a6b4a5b761d74c9ebf101a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453992"
---
# <a name="finding-and-loading-resources"></a>Localizando e carregando recursos

Antes de usar um recurso, um aplicativo deve carregá-lo na memória. As funções [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) e [**FindResourceEx**](/windows/desktop/api/Winbase/nf-winbase-findresourceexa) localizam um recurso em um módulo e retornam um identificador para os dados de recursos binários. **FindResource** localiza um recurso por tipo e nome. **FindResourceEx** localiza o recurso por tipo, nome e idioma. As informações sobre **FindResource** neste tópico também se aplicam a **FindResourceEx**.

A função [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) usa o identificador de recurso retornado por [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) para carregar o recurso na memória. Depois que um aplicativo carregar um recurso usando **LoadResource**, o sistema descarregará a memória associada somente quando todas as referências a seu módulo forem liberadas por meio de [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Os aplicativos que precisam acessar repetidamente os mesmos ou muitos recursos dentro de um módulo específico podem incorrer em penalidades de desempenho devido ao mapeamento de memória que ocorre em chamadas [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e **FreeLibrary** repetidas. Os aplicativos devem armazenar um único identificador de módulo até que os recursos não sejam mais necessários e, em seguida, chamar **FreeLibrary**. Depois que um módulo é descarregado da memória, os identificadores de recursos se tornam inválidos.

Um aplicativo pode usar [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) e [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) para localizar e carregar qualquer tipo de recurso, mas essas funções devem ser usadas apenas em uma destas situações:

-   Quando o aplicativo não pode acessar o recurso usando uma função específica de recurso existente.
-   Quando o aplicativo deve acessar o recurso como dados binários para chamadas de função subsequentes.

Sempre que possível, um aplicativo deve usar uma das seguintes funções específicas do recurso para localizar e carregar recursos em uma chamada:



| Função                                     | Ação                                   | Para remover o recurso                                                                                               |
|----------------------------------------------|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)      | Carrega e formata uma entrada de tabela de mensagens. | Nenhuma ação necessária.                                                                                                |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) | Carrega uma tabela de acelerador.              | [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)                                                       |
| [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)             | Carrega um recurso de bitmap.                 | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                             |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)             | Carrega um recurso de cursor.                 | [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)                                                                           |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                 | Carrega um recurso de ícone.                  | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                                                               |
| [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)               | Carrega um ícone, cursor ou bitmap.        | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon), [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor), [**ExcluirObjeto**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                 | Carrega um recurso de menu.                   | [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                                                                               |
| [**Cadeia de caracteres LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)             | Carrega uma entrada de tabela de cadeia de caracteres.              | Nenhuma ação necessária.                                                                                                |



 

Observe as funções de liberação na tabela acima. Antes de encerrar, um aplicativo deve liberar a memória ocupada por tabelas de acelerador, bitmaps, cursores, ícones e menus usando as funções apropriadas.

A memória associada aos recursos carregados por meio de [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) e [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) será liberada depois que o módulo for descarregado por uma chamada para [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Todos os recursos que permanecerem descarregados na terminação do aplicativo serão liberados automaticamente pelo sistema.

 

 