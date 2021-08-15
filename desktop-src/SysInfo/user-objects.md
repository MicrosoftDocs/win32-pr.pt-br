---
description: Os objetos de interface do usuário suportam apenas um identificador por objeto. Os processos não podem herdar ou duplicar os alças para objetos de usuário. Os processos em uma sessão não podem referenciar um usuário em outra sessão.
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: Objetos do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c3cdb5c0927a5773bad818064442f654159fefba2b2dfa4d0cb4c08d17ff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884313"
---
# <a name="user-objects"></a>Objetos do usuário

Os objetos de interface do usuário suportam apenas um identificador por objeto. Os processos não podem herdar ou duplicar os alças para objetos de usuário. Os processos em uma sessão não podem referenciar um usuário em outra sessão.

Há um limite teórico de 65.536 alças de usuário por sessão. No entanto, o número máximo de alças de usuário que podem ser abertas por sessão geralmente é menor, pois é afetado pela memória disponível. Também há um limite padrão por processo de alças de usuário. Para alterar esse limite, de definido o seguinte valor do Registro:

**HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **USERProcessHandleQuota**

Esse valor pode ser definido como um número entre 200 e 18.000.

## <a name="handles-to-user-objects"></a>Alças para objetos de usuário

Os alças para objetos de usuário são públicos para todos os processos. Ou seja, qualquer processo pode usar o identificador de objeto do usuário, desde que o processo tenha acesso de segurança ao objeto.

Na ilustração a seguir, um aplicativo cria um objeto de janela. A [**função CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) cria o objeto de janela e retorna um identificador de objeto.

![aplicativo que cria um objeto de janela](images/cshob-01.png)

Depois que o objeto de janela tiver sido criado, o aplicativo poderá usar o identificador de janela para exibir ou alterar a janela. O identificador permanece válido até que o objeto de janela seja destruído.

Na próxima ilustração, o aplicativo destrói o objeto de janela. A [**função DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) remove o objeto de janela da memória, o que invalida o identificador de janela.

![destruir um objeto de janela](images/cshob-02.png)

## <a name="managing-user-objects"></a>Gerenciando objetos de usuário

A tabela a seguir lista os objetos de usuário, juntamente com as funções criador e de autor de cada objeto. As funções criadoras criam o objeto e um identificador de objeto ou simplesmente retornam o identificador de objeto existente. As funções de remoção removem o objeto da memória, o que invalida o identificador de objeto.



| Objeto de usuário       | Função criador                                                                                                                                                                                                                                                              | Função Det.                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Tabela do acelerador | [**CreateAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**DestroyAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| Cursor             | [**Createcaret**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**DestroyCaret**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| Cursor            | [**CreateCursor,**](/windows/win32/api/winuser/nf-winuser-createcursor) [**LoadCursor,**](/windows/win32/api/winuser/nf-winuser-loadcursora) [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                                   | [**DestroyCursor**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| Conversa de DDE  | [**DdeConnect,**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) [ **DdeConnectList**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**DdeDisconnect**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect), [ **DdeDisconnectList**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| Gancho              | [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| ícone              | [**CreateIconIndirect,**](/windows/win32/api/winuser/nf-winuser-createiconindirect) [**LoadIcon,**](/windows/win32/api/winuser/nf-winuser-loadicona) [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                           | [**Destroyicon**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| Menu              | [**CreateMenu,**](/windows/win32/api/winuser/nf-winuser-createmenu) [**CreatePopupMenu,**](/windows/win32/api/winuser/nf-winuser-createpopupmenu) [**LoadMenu,**](/windows/win32/api/winuser/nf-winuser-loadmenua) [**LoadMenuIndirect**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta)                                                                                          | [**Destroymenu**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| Janela            | [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) [**CreateDialogParam,**](/windows/win32/api/winuser/nf-winuser-createdialogparama) [**CreateDialogIndirectParam,**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama) [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) | [**Destroywindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| Posição da janela   | [**Begindeferwindowpos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**Enddeferwindowpos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
