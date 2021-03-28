---
description: A área de notificação é uma parte da barra de tarefas que fornece uma fonte temporária para notificações e status.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Notificações e a área de notificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296477"
---
# <a name="notifications-and-the-notification-area"></a>Notificações e a área de notificação

A área de notificação é uma parte da barra de tarefas que fornece uma fonte temporária para notificações e status. Ele também pode ser usado para exibir ícones de recursos do sistema e do programa que não têm nenhuma presença na área de trabalho, como nível da bateria, controle de volume e status da rede. A área de notificação é conhecida historicamente como a área de status ou a bandeja do sistema.

Este tópico contém as seguintes seções:

-   [Diretrizes de notificação e área de notificação](#notification-and-notification-area-guidelines)
-   [Criando e exibindo uma notificação](#notifications-and-the-notification-area)
    -   [Adicionar um ícone de notificação](#add-a-notification-icon)
    -   [Definir a versão do NOTIFYICONDATA](#define-the-notifyicondata-version)
    -   [Definir a aparência e o conteúdo da notificação](#define-the-notification-look-and-contents)
    -   [Verificar o status do usuário](#check-the-user-status)
    -   [Exibir a notificação](#display-the-notification)
    -   [Removendo um ícone](#removing-an-icon)
-   [Exemplo de SDK](#sdk-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a>Diretrizes de notificação e área de notificação

Consulte as seções da [área](../uxguide/winenv-notification.md) [notificações](../uxguide/mess-notif.md) e notificação das diretrizes de interação da experiência do usuário do Windows para obter as práticas recomendadas no uso de notificações e da área de notificação. O objetivo é fornecer um benefício ao usuário por meio do uso apropriado de notificações, sem ser irritante ou distração.

A área de notificação não é para informações críticas que devem ser acionadas imediatamente. Ele também não se destina a acesso rápido de programa ou comando. A partir do Windows 7, grande parte dessa funcionalidade é melhor realizada por meio do botão da barra de tarefas de um aplicativo.

O Windows 7 permite que um usuário omita todas as notificações de um aplicativo se elas escolherem, portanto, o design e o uso de notificações elaborados causará a inclinação do usuário para permitir que seu aplicativo continue a exibi-los. As notificações são uma interrupção; Certifique-se de que valem a pena.

O Windows 7 apresenta o conceito de "tempo de silêncio". O tempo de silêncio é definido como a primeira hora depois que um novo usuário faz logon em sua conta pela primeira vez ou pela primeira vez após uma atualização do sistema operacional ou uma instalação limpa. Esse tempo é reservado para permitir que o usuário Explore e se familiarize com o novo ambiente sem a distração de notificações. Durante esse tempo, a maioria das notificações não deve ser enviada ou exibida. As exceções incluem comentários que o usuário esperaria ver em resposta a uma ação do usuário, como quando ele se conecta a um dispositivo USB ou imprime um documento. As especificidades de API de em relação ao tempo de silêncio são discutidas posteriormente neste tópico.

## <a name="creating-and-displaying-a-notification"></a>Criando e exibindo uma notificação

As seções restantes neste tópico descrevem o procedimento básico a ser seguido para exibir uma notificação do seu aplicativo para o usuário.

1.  [Adicionar um ícone de notificação](#add-a-notification-icon)
2.  [Definir a versão do NOTIFYICONDATA](#define-the-notifyicondata-version)
3.  [Definir a aparência e o conteúdo da notificação](#define-the-notification-look-and-contents)
4.  [Verificar o status do usuário](#check-the-user-status)
5.  [Exibir a notificação](#display-the-notification)
6.  [Removendo um ícone](#removing-an-icon)

### <a name="add-a-notification-icon"></a>Adicionar um ícone de notificação

Para exibir uma notificação, você deve ter um ícone na área de notificação. Em determinados casos, como o Microsoft Communicator ou o nível da bateria, esse ícone já estará presente. Em muitos outros casos, no entanto, você adicionará um ícone à área de notificação somente contanto que seja necessário para mostrar a notificação. Em ambos os casos, isso é feito usando a função [**\_ NotifyIcon do Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) . **Shell \_ do NotifyIcon** permite adicionar, modificar ou excluir um ícone na área de notificação.

![área de notificação contendo três ícones](images/taskbar/notificationareaicons.png)

Quando um ícone é adicionado à área de notificação no Windows 7, ele é adicionado à seção de estouro da área de notificação por padrão. Essa área contém ícones de área de notificação que estão ativos, mas que não estão visíveis na área de notificação. Somente o usuário pode promover um ícone do estouro para a área de notificação, embora em determinadas circunstâncias o sistema possa promover temporariamente um ícone para a área de notificação como uma breve visualização (em um minuto).

> [!Note]  
> O usuário deve ter a dizer final sobre quais ícones eles desejam ver na área de notificação. Antes de instalar um ícone não transitório na área de notificação, o usuário deve receber uma solicitação de permissão. Eles também devem receber a opção (normalmente, embora seu menu de atalho) Remova o ícone da área de notificação.

 

A estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada na chamada para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contém informações que especificam o ícone da área de notificação e a própria notificação. Estes são os itens específicos para o ícone da área de notificação em si, que podem ser definidos por meio de **NOTIFYICONDATA**.

-   O recurso do qual o ícone é tirado.
-   Um identificador exclusivo para o ícone.
-   O estilo da dica de ferramenta do ícone.
-   O estado do ícone (oculto, compartilhado ou ambos) na área de notificação.
-   O identificador de uma janela de aplicativo associada ao ícone.
-   Um identificador de mensagem de retorno de chamada que permite que o ícone comunique eventos que ocorrem dentro do retângulo delimitador do ícone e a notificação de balão com a janela do aplicativo associada. O retângulo delimitador do ícone pode ser recuperado por meio do [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).

Cada ícone na área de notificação pode ser identificado de duas maneiras:

-   O GUID com o qual o ícone é declarado no registro. Esse é o método preferencial no Windows 7 e posterior.
-   O identificador de uma janela associada ao ícone da área de notificação, além de um identificador de ícone definido pelo aplicativo. Esse método é usado no Windows Vista e versões anteriores.

Os ícones na área de notificação podem ter uma dica de ferramenta. A dica de ferramenta pode ser uma dica de ferramenta padrão (preferencial) ou uma interface do usuário de pop-up, desenhada por aplicativo. Embora uma dica de ferramenta não seja necessária, é recomendável.

Os ícones da área de notificação devem ter reconhecimento de DPI alta. Um aplicativo deve fornecer um ícone de 16x16 pixels e um ícone de 32x32 em seu arquivo de recurso e, em seguida, usar [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) para garantir que o ícone correto seja carregado e dimensionado adequadamente.

O aplicativo responsável pelo ícone da área de notificação deve lidar com um clique do mouse para esse ícone. Quando um usuário clica com o botão direito do mouse no ícone, ele deve abrir um menu de atalho normal. No entanto, o resultado de um único clique com o botão esquerdo do mouse irá variar com a função do ícone. Ele deve exibir o que o usuário esperaria ver no formulário mais adequado para esse conteúdo — uma janela pop-up, uma caixa de diálogo ou a própria janela do programa. Por exemplo, ele pode mostrar o texto de status de um ícone de status ou um controle deslizante para o controle de volume.

O posicionamento de uma janela pop-up ou caixa de diálogo que resulta do clique deve ser colocado próximo à coordenada do clique na área de notificação. Use o [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) para determinar sua localização.

O ícone pode ser adicionado à área de notificação sem exibir uma notificação definindo somente os membros específicos do ícone de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (discutidos acima) e chamando o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , conforme mostrado aqui:


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



Você também pode adicionar o ícone à área de notificação e exibir uma notificação em uma chamada para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Para fazer isso, continue com as instruções neste tópico.

### <a name="define-the-notifyicondata-version"></a>Definir a versão do NOTIFYICONDATA

À medida que o Windows progrediu, a estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) expandiu-se para incluir mais membros para definir mais funcionalidade. As constantes são usadas para declarar qual versão do **NOTIFYICONDATA** usar com o ícone da área de notificação para permitir a compatibilidade com versões anteriores. A menos que haja um motivo convincente para fazer o contrário, é altamente recomendável que você use a \_ versão do NOTIFYICON versão \_ 4, introduzida no Windows Vista. Essa versão fornece a funcionalidade completa disponível, incluindo a capacidade preferida de identificar o ícone da área de notificação, embora um GUID registrado, um mecanismo de retorno de chamada superior e melhor acessibilidade.

Defina a versão por meio das seguintes chamadas:


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



Observe que essa chamada para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) não exibe uma notificação.

### <a name="define-the-notification-look-and-contents"></a>Definir a aparência e o conteúdo da notificação

Uma notificação é um tipo especial de controle de dica de ferramenta de balão. Ele contém um título, corpo de texto e um ícone. Como uma janela, ele tem um botão **fechar** no canto superior direito. Ele também contém um botão **Opções** que abre o item ícones da área de notificação no painel de controle, que permite ao usuário mostrar ou ocultar o ícone ou mostrar apenas as notificações sem um ícone.

![captura de tela do balão de notificação indicando que a energia da bateria está baixa](images/taskbar/notificationballoon.png)

A estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada na chamada para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contém informações que especificam o ícone da área de notificação e o próprio balão de notificação. Estes são os itens específicos para a notificação que podem ser definidos por meio de **NOTIFYICONDATA**.

-   Um ícone a ser exibido no balão de notificação, que é especificado pelo tipo de notificação. O tamanho do ícone pode ser especificado, bem como ícones personalizados.
-   Um título de notificação. Este título deve ter no máximo 48 caracteres de comprimento em inglês (para acomodar a localização). O título é a primeira linha da notificação e é definido de acordo com o uso do tamanho da fonte, da cor e do peso.
-   Texto a ser usado no corpo da notificação. Esse texto deve ter no máximo 200 caracteres em inglês (para acomodar a localização).
-   Se a notificação deve ser descartada se não puder ser exibida imediatamente.
-   Um tempo limite para a notificação. Essa configuração é ignorada no Windows Vista e em sistemas posteriores em favor de uma configuração de tempo limite de acessibilidade em todo o sistema.
-   Se a notificação deve respeitar o tempo de silêncio, defina por meio do sinalizador [**NIIF \_ respeitar o \_ \_ tempo de silêncio**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) .

> [!Note]  
> As interfaces [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) e [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) são wrappers Component Object Model (com) para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). No entanto, neste momento, eles não fornecem a funcionalidade totalmente NOTIFYICON da \_ versão \_ 4 disponível por meio do **shell \_ NotifyIcon** diretamente, incluindo o uso de um GUID para identificar o ícone da área de notificação.

 

### <a name="check-the-user-status"></a>Verificar o status do usuário

O sistema usa a função [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) é usada para verificar se o usuário está em tempo de silêncio, fora do computador ou em um estado ininterrupto, como o modo de apresentação. Se o sistema exibe sua notificação depende desse Estado.

> [!Note]  
> Se seu aplicativo estiver usando um método de notificação personalizado que não usa [**o \_ shell NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)ou [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), ele deverá sempre chamar explicitamente [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) para determinar se ele deve exibir a interface do usuário de notificação nesse momento.

 

As notificações enviadas quando o usuário está ausente são enfileiradas para exibição, mas como não é possível saber quando o usuário retornará ou se a notificação ainda será válida nesse momento, você poderá considerar reenviar a notificação mais tarde.

As notificações enviadas durante o tempo de silêncio são descartadas não mostradas. As diretrizes de design solicitam que todas as notificações sejam ignoradas. Eles não devem exigir ação imediata do usuário. Portanto, nenhuma notificação é tão importante que ela deve substituir o tempo de silêncio.

### <a name="display-the-notification"></a>Exibir a notificação

Depois de ter definido a versão [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e definido a notificação em uma estrutura **NOTIFYICONDATA** , chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para exibir o ícone.

-   Se o ícone da área de notificação não estiver presente, chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para adicionar o ícone. Faça isso para ícones transitórios e não transitórios.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   Se o ícone da área de notificação já estiver presente, chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para modificar o ícone.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

O código a seguir mostra um exemplo de como definir dados de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e enviá-los por meio do [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Observe que este exemplo identifica o ícone de notificação por meio de um GUID (preferencial no Windows 7).


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a>Removendo um ícone

Para remover um ícone — por exemplo, quando você adicionou apenas o ícone temporariamente para transmitir uma notificação — chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), conforme mostrado aqui. Somente uma estrutura de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) mínima que identifica o ícone é necessária nesta chamada.


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> Quando um aplicativo é desinstalado, seu ícone da área de notificação ainda pode aparecer para o usuário como uma opção na página ícones da área de notificação no painel de controle por até sete dias. No entanto, qualquer alteração feita ali não terá nenhum efeito.

 

## <a name="sdk-sample"></a>Exemplo de SDK

Consulte o exemplo de exemplo [NotificationIcon](samples-notificationicon.md) no SDK (Software Development Kit) do Windows para obter um exemplo completo do uso [**de \_ NotifyIcon do Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**NotifyIcon do Shell \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[**NotifyIconGetRect do Shell \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[A barra de tarefas](taskbar.md)
</dt> <dt>

[Extensões da barra de tarefas](taskbar-extensions.md)
</dt> </dl>

 

 
