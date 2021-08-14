---
title: Funções de servidor (Windows recursos de acessibilidade)
description: Funções de servidor
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2eb449e81371a1c0c9e230610de97b8abdefb41429c5753059540e45f921d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828064"
---
# <a name="server-functions-windows-accessibility-features"></a>Funções de servidor (Windows recursos de acessibilidade)

Esta seção contém informações sobre as funções de servidor usadas com Microsoft Active Accessibility.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccNotifyTouchInteraction**](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | Permite que um aplicativo de AT (tecnologia adaptativa) notifique o sistema de que ele está interagindo com a interface do usuário por meio de uma API de Automação do Windows (como o Microsoft Automação da Interface do Usuário) como resultado de um gesto de toque do usuário. Isso permite que a tecnologia adaptativa notifique o aplicativo de destino e o sistema de que o usuário está interagindo com o toque.<br/> |
| [**AccSetRunningUtilityState**](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | Define valores do sistema que indicam se o estado atual de um aplicativo de AT (tecnologia adaptativa) afeta a funcionalidade que normalmente é fornecida pelo sistema. <br/>                                                                                                                                                                                 |
| [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | Cria um objeto acessível com os métodos e as propriedades do tipo especificado do elemento de interface do usuário fornecido pelo sistema.<br/>                                                                                                                                                                                                                      |
| [**Createstdaccessibleproxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | Cria um objeto acessível que tem as propriedades e os métodos da classe especificada do elemento de interface do usuário fornecido pelo sistema.<br/>                                                                                                                                                                                                                 |
| [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | Retorna uma referência, semelhante a um identificador, para o objeto especificado. Os servidores retornam essa referência ao lidar [**com WM \_ GETOBJECT.**](wm-getobject.md)<br/>                                                                                                                                                                                              |
| [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | Recupera um ponteiro de interface solicitado para um objeto acessível com base em uma referência de objeto gerada anteriormente.<br/> Essa função foi projetada para uso interno por Microsoft Active Accessibility e está documentada apenas para fins informacionais. Nem clientes nem servidores devem chamar essa função.<br/>                               |
| [**IsWinEventHookInstalled**](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | Determina se há um gancho WinEvent instalado que pode ser notificado de um evento especificado.<br/>                                                                                                                                                                                                                                                |
| [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | Sinaliza ao sistema que ocorreu um evento predefinido. Se algum aplicativo cliente tiver registrado uma função de gancho para o evento, o sistema chamará a função de gancho do cliente.<br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessibilidade Ativa Interface do Usuário serviços](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 





