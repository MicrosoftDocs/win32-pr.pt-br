---
description: Os objetos da interface do usuário dão suporte a apenas um identificador por objeto. Os processos não podem herdar nem duplicar identificadores para objetos de usuário. Os processos em uma sessão não podem fazer referência a um identificador de usuário em outra sessão.
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: Objetos do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ed8afcf0f1d0e4c232cf503bc2c7ba86dca42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562010"
---
# <a name="user-objects"></a>Objetos do usuário

Os objetos da interface do usuário dão suporte a apenas um identificador por objeto. Os processos não podem herdar nem duplicar identificadores para objetos de usuário. Os processos em uma sessão não podem fazer referência a um identificador de usuário em outra sessão.

Há um limite teórico de 65.536 identificadores de usuário por sessão. No entanto, o número máximo de identificadores de usuário que podem ser abertos por sessão geralmente é menor, pois é afetado pela memória disponível. Também há um limite por processo padrão de identificadores de usuário. Para alterar esse limite, defina o seguinte valor de registro:

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **USERProcessHandleQuota**

Esse valor pode ser definido como um número entre 200 e 18.000.

## <a name="handles-to-user-objects"></a>Identificadores para objetos de usuário

Os identificadores para objetos de usuário são públicos a todos os processos. Ou seja, qualquer processo pode usar o identificador de objeto do usuário, desde que o processo tenha acesso de segurança ao objeto.

Na ilustração a seguir, um aplicativo cria um objeto Window. A função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) cria o objeto Window e retorna um identificador de objeto.

![aplicativo Criando um objeto de janela](images/cshob-01.png)

Depois que o objeto Window tiver sido criado, o aplicativo poderá usar o identificador de janela para exibir ou alterar a janela. O identificador permanece válido até que o objeto de janela seja destruído.

Na próxima ilustração, o aplicativo destrói o objeto Window. A função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) remove o objeto Window da memória, que invalida o identificador de janela.

![destruindo um objeto de janela](images/cshob-02.png)

## <a name="managing-user-objects"></a>Gerenciando objetos de usuário

A tabela a seguir lista os objetos de usuário, juntamente com as funções de criador e destruidor de cada objeto. As funções de criador criam o objeto e um identificador de objeto ou simplesmente retornam o identificador de objeto existente. As funções de destruidor removem o objeto da memória, o que invalida o identificador de objeto.



| Objeto de usuário       | Função Creator                                                                                                                                                                                                                                                              | Função de destruidor                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Tabela de acelerador | [**CreateAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**DestroyAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| Acento             | [**Não importa**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**DestroyCaret**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| Cursor            | [**CreateCursor**](/windows/win32/api/winuser/nf-winuser-createcursor), [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora), [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                                   | [**DestroyCursor**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| Conversa DDE  | [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect), [ **DdeConnectList**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**DdeDisconnect**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect), [ **DdeDisconnectList**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| Fixação              | [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| ícone              | [**CreateIconIndirect**](/windows/win32/api/winuser/nf-winuser-createiconindirect), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                           | [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| Menu              | [**CreateMenu**](/windows/win32/api/winuser/nf-winuser-createmenu), [**CreatePopupMenu**](/windows/win32/api/winuser/nf-winuser-createpopupmenu), [**LoadMenu**](/windows/win32/api/winuser/nf-winuser-loadmenua), [**LoadMenuIndirect**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta)                                                                                          | [**DestroyMenu**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| Janela            | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa), [**CreateDialogParam**](/windows/win32/api/winuser/nf-winuser-createdialogparama), [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama), [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) | [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| Posição da janela   | [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
