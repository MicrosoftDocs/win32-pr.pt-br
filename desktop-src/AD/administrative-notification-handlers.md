---
title: Manipuladores de notificação administrativa
description: O snap-in MMC do Microsoft Usuários e Computadores do Active Directory fornece um mecanismo para permitir que os componentes recebam notificações quando o usuário exclui, renomeia, move ou altera as propriedades de um objeto usando o snap-in.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- AD de manipuladores de notificação administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebe2e92edd9a2630963d7dda6d84e6c323743ef5d37687927502c62b32ec592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024656"
---
# <a name="administrative-notification-handlers"></a>Manipuladores de notificação administrativa

O snap-in MMC do Microsoft Usuários e Computadores do Active Directory fornece um mecanismo para permitir que os componentes recebam notificações quando o usuário exclui, renomeia, move ou altera as propriedades de um objeto usando o snap-in. O componente que recebe as notificações é conhecido como um "manipulador de notificação".

Isso é útil quando vários objetos são vinculados e devem existir dentro do mesmo contêiner. Se um dos objetos vinculados for movido, uma notificação será fornecida ao manipulador de notificação e o manipulador de notificação poderá mover os outros objetos vinculados para a mesma pasta.

Quando uma das operações é executada e um ou mais manipuladores de notificação são instalados, o snap-in Usuários e Computadores exibirá uma caixa de diálogo de confirmação que lista os manipuladores de notificação e uma caixa de seleção para cada manipulador. Se a caixa de seleção de um manipulador estiver marcada, o manipulador será notificado. Se a caixa de seleção não estiver marcada, o manipulador não será notificado.

## <a name="implementing-a-notification-handler"></a>Implementando um manipulador de notificação

Um manipulador de notificação é um objeto COM implementado como um servidor em processo. O manipulador de notificação deve implementar a interface [**IDsAdminNotifyHandler.**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler)

Quando ocorre um evento que causará uma notificação, o snap-in Usuários e Computadores enumera os manipuladores de notificação registrados e cria cada um deles usando o CLSID para o manipulador. Depois que o manipulador é criado, o snap-in chama o [**método IDsAdminNotifyHandler::Initialize.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) O **método Initialize** fornece o snap-in com os eventos que o manipulador deve receber.

Se o evento for um que deve ser enviado para o manipulador de notificação, o snap-in chamará o método [**IDsAdminNotifyHandler::Begin.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) O **método Begin** fornece ao manipulador o evento que está ocorrendo, dados sobre o objeto no qual o evento está ocorrendo e, dependendo do evento, dados sobre o que o objeto se tornará. O **método Begin** também fornece o snap-in com o texto que deve ser exibido para o manipulador na caixa de diálogo de confirmação.

Quando o [**método Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) para cada manipulador tiver sido chamado, o snap-in exibirá a caixa de diálogo de confirmação. A caixa de diálogo de confirmação solicita que o usuário selecione quais manipuladores receberão a notificação. Se o usuário pressionar o **botão Nenhum** push na caixa de diálogo de confirmação, nenhum dos manipuladores será notificado. Se o usuário pressionar o **botão Sim,** cada um dos manipuladores selecionados na caixa de diálogo de confirmação receberá a notificação. O snap-in envia a notificação para o manipulador chamando o [**método IDsAdminNotifyHandler::Notify.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify)

Depois que todos os manipuladores foram notificados, o snap-in chama o [**método IDsAdminNotifyHandler::End.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) O **método** End é sempre chamado, mesmo que o [**método Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) não seja chamado.

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>Registrando um manipulador de notificação no Windows Registro

Como todos os servidores COM, um manipulador de notificação deve ser registrado no Windows registro. O manipulador é registrado sob a seguinte chave:


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**<CLSID>** é a representação de cadeia de caracteres do CLSID conforme produzido pela [**função StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) Na **<CLSID>** chave, há uma chave **InProcServer32** que identifica o objeto como um servidor in-proc de 32 bits. Na chave **InProcServer32,** o local da DLL é especificado no valor padrão e o modelo de threading é especificado no **valor ThreadingModel.** Todos os manipuladores de notificação devem usar o **modelo de** threading Apartment.

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Registrando um manipulador de notificação com um servidor do Active Directory

Dentro Active Directory Domain Services, o registro do manipulador de notificação é específico para uma localidade. Se o manipulador de notificação se aplicar a todas as localidades, ele deverá ser registrado no objeto **displaySpecifier** em todos os subcontidores de localidade no contêiner DisplaySpecifiers. Se o manipulador de notificação estiver localizado para uma determinada localidade, ele será registrado no objeto **displaySpecifier** no subcontidor dessa localidade. Para obter mais informações sobre o contêiner e as localidades displaySpecifiers, consulte [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).

Manipuladores de notificação são registrados no atributo **dsUIAdminNotification** no contêiner **DS-UI-Default-Configurações.** Esse é um valor de cadeia de caracteres Unicode com valores múltiplos em que cada valor requer o seguinte formato:


```C++
<order number>,<CLSID>
```



O " &lt; número da ordem " é um número não assinado que representa a posição do manipulador na caixa de &gt; diálogo de confirmação. Quando a caixa de diálogo de confirmação é exibida, os valores são classificação usando uma comparação do " número de ordem" de &lt; cada &gt; valor. Se mais de um valor tiver o mesmo " número de ordem ", esses manipuladores serão exibidos na ordem em que são &lt; &gt; lidos do servidor do Active Directory. Um não existente, ou seja, um não usado por outros valores na propriedade , " número de ordem " deve &lt; &gt; ser usado, se possível. Não há nenhuma posição inicial prescrita e as lacunas podem aparecer na sequência " &lt; número da &gt; ordem ".

O " CLSID " é a representação de cadeia de &lt; &gt; caracteres do CLSID conforme produzido pela [**função StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)

 

 