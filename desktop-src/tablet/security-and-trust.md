---
description: o .NET Framework tem um modelo de segurança que trata aplicativos de forma diferente, dependendo de sua origem.
ms.assetid: 37fa870a-6f38-44ae-943e-27697f6b9fba
title: Segurança e confiança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99806fa3256dfd08d8f4a14c70620c767331fb3cb95b83a7ecd6940b04c155cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708196"
---
# <a name="security-and-trust"></a>Segurança e confiança

o .NET Framework tem um modelo de segurança que trata aplicativos de forma diferente, dependendo de sua origem. Os executáveis e assemblies que são do computador de um usuário geralmente são executados com confiança total; os mesmos executáveis e assemblies executados pela Internet geralmente são executados com confiança parcial. Isso é para impedir que códigos mal-intencionados leiam ou modifiquem informações às quais ele não deve ter acesso, como arquivos locais, itens na área de transferência e outros recursos. Se um executável chama um assembly que, por sua vez, chama outro assembly que requer um certo nível de confiança, o nível mais baixo de confiança de todos os componentes na cadeia é aplicado. No entanto, um administrador em um computador pode definir permissões específicas que substituem as permissões padrão.

Uma visão geral do modelo de segurança é fornecida em [controles seguros, Light-Weight Client-Side](/archive/msdn-magazine/2002/january/dhtml-and-net-host-secure-lightweight-client-side-controls-in-microsoft-internet-explorer)e você pode obter mais detalhes sobre o modelo de segurança na [segurança de acesso ao código na prática](/previous-versions/msp-n-p/ff648663(v=pandp.10)). Uma boa visão geral da segurança das bibliotecas (que é especialmente importante para objetos [**UserControl**](/uwp/api/Windows.UI.Xaml.Controls.UserControl?view=winrt-19041) em uma página da Web) pode ser encontrada em [usando bibliotecas de código parcialmente confiável](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconusinglibrariesfrompartiallytrustedcode.asp)e outras informações de segurança sobre controles gerenciados podem ser encontradas em [escrevendo controles gerenciados seguros](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconwritingsecuremanagedcontrols.asp%3fframe%3dtrue).

## <a name="permissions"></a>Permissões

A maioria dos objetos e membros gerenciados na API de tecnologias do Tablet PC tem dois requisitos:

-   A execução é sempre necessária.
-   FullTrust é necessário quando ocorre a ação de segurança [InheritanceDemand](/previous-versions/windows/) . Isso significa que a confiança total é necessária quando uma classe derivada herda uma classe ou substitui um método do SDK do Tablet PC.

A tabela a seguir lista as classes e os membros que exigem permissões adicionais. As permissões para uma determinada classe também se aplicam a todos os seus membros não listados nesta tabela.



| Classe ou método                                                                       | Permissões                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                                  | [UIPermissionClipboard. myclipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                                    | [UIPermissionClipboard.OwnClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                                  | [UIPermissionClipboard. myclipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Controles InkCollector**](inkcollector-class.md)                                            | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| InkCollector (IntPtr)                                                                  | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| InkCollector. Handle                                                                   | [UIPermissionWindow. @ Windows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (veja a observação abaixo)<br/> |
| InkEdit                                                                               | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [InkOverlay](/previous-versions/ms552322(v=vs.100))                                   | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| InkOverlay (IntPtr)                                                                    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e SecurityPermissionFlag. UnmanagedCode<br/>                                                                 |
| [InkOverlay. Handle](/previous-versions/ms833109(v=msdn.10))                      | [UIPermissionWindow. @ Windows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (veja a observação abaixo)<br/> |
| [InkPicture](/previous-versions/aa514604(v=msdn.10))                                   | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| [PenInputPanel](/previous-versions/aa514041(v=msdn.10))                             | Veja a observação abaixo.<br/>                                                                                                                                                                                     |
| [**InkRenderer**](inkrenderer-class.md)                                              | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [**Desenhar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw), [ **DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)        | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer. InkSpaceToPixel (IntPtr, ponto), processador. InkSpaceToPixel (IntPtr, ponto \[ \] )    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer. PixelToInkSpace (IntPtr, ponto), processador. PixelToInkSpace (IntPtr, ponto \[ \] )    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))                                      | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| DynamicRenderer (IntPtr)                                                               | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**RealTimeStylus**](realtimestylus-class.md)                                        | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| RealTimeStylus (IntPtr), RealTimeStylus (IntPtr, booliano), RealTimeStylus (IntPtr, Tablet) | [UIPermissionWindow. @ Windows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>                  |



 

> [!Note]  
> Geralmente, é preferível usar um controle em vez de um identificador (IntPtr) para construtores, pois os controles exigem menos permissões. Da mesma forma, é preferível usar um objeto Graphics em vez de um identificador para [Renderer. draw](/previous-versions/ms828488(v=msdn.10)), [Renderer. InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) e [Renderer. PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)).

 

> [!Note]  
> as propriedades [InkCollector. handle](/previous-versions/ms836504(v=msdn.10)) e [InkOverlay. Handle](/previous-versions/ms833109(v=msdn.10)) não exigem a permissão [SecurityPermissionFlag. unmanagedcode](/previous-versions/windows/) se o identificador for para um controle de Windows Forms, mas eles fazem para outras janelas.

 

> [!Note]  
> Para a [classe PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , os métodos e as propriedades a seguir exigem [SecurityPermissionFlag. alflags](/previous-versions/windows/): PenInputPanel (IntPtr), [AttachedEditWindow](/previous-versions/ms582240(v=vs.100)), [Busy](/previous-versions/ms571975(v=vs.100)), [CommitPendingInput](/previous-versions/ms569650(v=vs.100)), [CurrentPanel](/previous-versions/ms571976(v=vs.100)), [DefaultPanel](/previous-versions/ms571977(v=vs.100)), [EnableTsf](/previous-versions/ms569656(v=vs.100)), [factoname](/previous-versions/ms571978(v=vs.100)), [Height](/previous-versions/ms571979(v=vs.100)), [as](/previous-versions/ms571980(v=vs.100)), [InputFailed](/previous-versions/ms567738(v=vs.100)), [Left](/previous-versions/ms571981(v=vs.100)), [MoveTo](/previous-versions/ms569667(v=vs.100)), [panelchanged](/previous-versions/ms567741(v=vs.100)), [PanelMoving](/previous-versions/ms567748(v=vs.100)), [Atualizar](/previous-versions/ms569778(v=vs.100)), [Top](/previous-versions/ms571982(v=vs.100)), [VerticalOffset](/previous-versions/ms571983(v=vs.100)), [Visible](/previous-versions/ms571984(v=vs.100)), [VisibleChanged](/previous-versions/ms567754(v=vs.100))e [Width](/previous-versions/ms571985(v=vs.100)).

 

## <a name="other-considerations"></a>Outras considerações

Algumas outras considerações de segurança conhecidas são:

-   O Microsoft Internet Explorer 6 ou superior é necessário para que os controles da Web funcionem corretamente. Com o Internet Explorer 5,5, somente os controles gerenciados iniciais são carregados; Você não pode carregar controles adicionais dinamicamente em tempo de execução.
-   se você estiver usando Windows XP Service Pack 2 (SP2) e clr 1.0, ter controles da Web no Internet Explorer exigirá a adição do site como um site confiável, mesmo que eles estejam na zona da Intranet. No entanto, quando você fizer isso, eles não serão mais executados na zona do site confiável, embora sejam executados na zona da intranet. Esse problema é corrigido com o CLR 1.1.

 

 