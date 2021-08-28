---
title: Manipuladores de notificação administrativa
description: O snap-in MMC usuários e computadores do Microsoft Active Directory fornece um mecanismo para permitir que os componentes recebam notificações quando o usuário exclui, renomeia, move ou altera as propriedades de um objeto usando o snap-in.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- AD de manipuladores de notificação administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d89627cdb15cc7ea15f4b56e3a6ec90eafbe6a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879886"
---
# <a name="administrative-notification-handlers"></a>Manipuladores de notificação administrativa

O snap-in MMC usuários e computadores do Microsoft Active Directory fornece um mecanismo para permitir que os componentes recebam notificações quando o usuário exclui, renomeia, move ou altera as propriedades de um objeto usando o snap-in. O componente que recebe as notificações é conhecido como "manipulador de notificação".

Isso é útil quando vários objetos são vinculados e devem existir dentro do mesmo contêiner. Se um dos objetos vinculados for movido, uma notificação será fornecida ao manipulador de notificação e o manipulador de notificação poderá mover os outros objetos vinculados para a mesma pasta.

Quando uma das operações for executada e um ou mais manipuladores de notificação estiverem instalados, o snap-in usuários e computadores exibirá uma caixa de diálogo de confirmação que lista os manipuladores de notificação e uma caixa de seleção para cada manipulador. Se a caixa de seleção de um manipulador for selecionada, o manipulador será notificado. Se a caixa de seleção não estiver marcada, o manipulador não será notificado.

## <a name="implementing-a-notification-handler"></a>Implementando um manipulador de notificação

Um manipulador de notificação é um objeto COM implementado como um servidor em processo. O manipulador de notificação deve implementar a interface [**IDsAdminNotifyHandler**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler) .

Quando ocorrer um evento que causará uma notificação, o snap-in usuários e computadores enumerará os manipuladores de notificação registrados e criará cada um usando o CLSID para o manipulador. Depois que o manipulador é criado, o snap-in chama o método [**IDsAdminNotifyHandler:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) . O método **Initialize** fornece o snap-in com os eventos que o manipulador deve receber.

Se o evento for um que deve ser enviado para o manipulador de notificação, o snap-in chamará o método [**IDsAdminNotifyHandler:: Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) . O método **begin** fornece o manipulador com o evento que ocorre, dados sobre o objeto em que o evento está ocorrendo e, dependendo do evento, dados sobre o que o objeto se tornará. O método **begin** também fornece o snap-in com o texto que deve ser exibido para o manipulador na caixa de diálogo de confirmação.

Quando o método [**begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) de cada manipulador for chamado, o snap-in exibirá a caixa de diálogo de confirmação. A caixa de diálogo de confirmação solicita que o usuário Selecione quais manipuladores receberão a notificação. Se o usuário pressionar o botão **sem** push na caixa de diálogo de confirmação, nenhum dos manipuladores será notificado. Se o usuário pressionar o botão de ação **Sim** , cada um dos manipuladores selecionados na caixa de diálogo de confirmação receberá a notificação. O snap-in envia a notificação para o manipulador chamando o método [**IDsAdminNotifyHandler:: Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) .

Depois que todos os manipuladores tiverem sido notificados, o snap-in chamará o método [**IDsAdminNotifyHandler:: End**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) . O método **end** é sempre chamado, mesmo que o método [**Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) não seja chamado.

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>registrando um manipulador de notificação no registro de Windows

como todos os servidores COM, um manipulador de notificação deve ser registrado no registro de Windows. O manipulador é registrado sob a seguinte chave:


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**&lt; CLSID &gt;** é a representação de cadeia de caracteres do CLSID, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . Sob a chave **&lt; &gt; CLSID** , há uma chave **InprocServer32** que identifica o objeto como um servidor no processo de 32 bits. Na chave **InprocServer32** , o local da dll é especificado no valor padrão e o modelo de threading é especificado no valor de **ThreadingModel** . Todos os manipuladores de notificação devem usar o modelo de Threading **Apartment** .

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Registrando um manipulador de notificação com um servidor Active Directory

No Active Directory Domain Services, o registro do manipulador de notificação é específico para uma localidade. Se o manipulador de notificação se aplica a todas as localidades, ele deve ser registrado no objeto **displaySpecifier** em todos os subcontêineres de localidade no contêiner DisplaySpecifiers. Se o manipulador de notificação for localizado para uma determinada localidade, ele será registrado no objeto **displaySpecifier** no subcontêiner dessa localidade. Para obter mais informações sobre o contêiner DisplaySpecifiers e as localidades, consulte [Exibir especificadores](display-specifiers.md) e [contêiner DisplaySpecifiers](displayspecifiers-container.md).

os manipuladores de notificação são registrados no atributo **dsUIAdminNotification** no contêiner **DS-UI-Default-Configurações** . Esse valor de cadeia de caracteres Unicode com vários valores, em que cada valor requer o seguinte formato:


```C++
<order number>,<CLSID>
```



O " &lt; número do pedido &gt; " é um número sem sinal que representa a posição do manipulador na caixa de diálogo de confirmação. Quando a caixa de diálogo de confirmação é exibida, os valores são classificados usando uma comparação do " &lt; número de ordem" de cada valor &gt; . Se mais de um valor tiver o mesmo " &lt; número do pedido &gt; ", esses manipuladores serão exibidos na ordem em que são lidos do servidor de Active Directory. Um não existente, ou seja, um não usado por outros valores na propriedade " &lt; número do pedido &gt; " deve ser usado, se possível. Não há uma posição de início prescrita e as lacunas podem aparecer na &lt; sequência "número do pedido &gt; ".

O " &lt; CLSID &gt; " é a representação de cadeia de caracteres do CLSID, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

 

 
