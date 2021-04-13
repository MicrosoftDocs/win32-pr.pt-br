---
title: Funções de servidor (recursos de acessibilidade do Windows)
description: Funções de servidor
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a747c073e84049fe578d19561b25d0b754dbb9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369176"
---
# <a name="server-functions-windows-accessibility-features"></a>Funções de servidor (recursos de acessibilidade do Windows)

Esta seção contém informações sobre as funções de servidor usadas com o Microsoft Acessibilidade Ativa.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccNotifyTouchInteraction**](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | Permite que um aplicativo de tecnologia assistencial (AT) notifique o sistema de que ele está interagindo com a interface do usuário por meio de uma API de automação do Windows (como a automação da interface de usuário da Microsoft) como resultado de um gesto de toque. Isso permite que a tecnologia assistencial notifique o aplicativo de destino e o sistema que o usuário está interagindo com o toque.<br/> |
| [**AccSetRunningUtilityState**](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | Define valores do sistema que indicam se um estado atual do aplicativo de tecnologia assistencial (AT) afeta a funcionalidade que normalmente é fornecida pelo sistema. <br/>                                                                                                                                                                                 |
| [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | Cria um objeto acessível com os métodos e as propriedades do tipo especificado do elemento de interface do usuário fornecido pelo sistema.<br/>                                                                                                                                                                                                                      |
| [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | Cria um objeto acessível que tem as propriedades e os métodos da classe especificada do elemento de interface do usuário fornecido pelo sistema.<br/>                                                                                                                                                                                                                 |
| [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | Retorna uma referência, semelhante a um identificador, ao objeto especificado. Os servidores retornam essa referência ao manipular o [**WM \_ GetObject**](wm-getobject.md).<br/>                                                                                                                                                                                              |
| [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | Recupera um ponteiro de interface solicitado para um objeto acessível com base em uma referência de objeto gerada anteriormente.<br/> Essa função foi projetada para uso interno do Microsoft Acessibilidade Ativa e é documentada apenas para fins informativos. Nem os clientes nem os servidores devem chamar essa função.<br/>                               |
| [**IsWinEventHookInstalled**](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | Determina se há um gancho WinEvent instalado que pode ser notificado de um evento especificado.<br/>                                                                                                                                                                                                                                                |
| [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | Sinaliza ao sistema que ocorreu um evento predefinido. Se qualquer aplicativo cliente tiver registrado uma função de gancho para o evento, o sistema chamará a função de gancho do cliente.<br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços de interface do usuário Acessibilidade Ativa](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 





