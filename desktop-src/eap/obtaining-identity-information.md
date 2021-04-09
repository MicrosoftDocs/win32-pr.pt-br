---
title: Obtendo informações de identidade
description: O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface de função que obtém informações de identificação inicial para o usuário que solicita autenticação.
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9519da9d66937fd25245fe78f12ef34c3c0ad8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007389"
---
# <a name="obtaining-identity-information"></a>Obtendo informações de identidade

O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface de função que obtém informações de identificação inicial para o usuário que solicita autenticação.

O fornecedor deve implementar as funções a seguir.

-   [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Essas funções podem ser implementadas na mesma DLL que o protocolo de autenticação ou em uma DLL separada. Além disso, a DLL que implementa as funções de identidade pode dar suporte a mais de um protocolo de autenticação. O caminho para a DLL para essas funções é armazenado no valor de registro de [ \_ \_ \_ identidadename EAP do RAS](authentication-protocol-registry-values.md) , sob a chave para o protocolo de autenticação. Para obter mais informações sobre como criar esse valor de registro, consulte [instalação EAP](eap-installation.md).

A função [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) normalmente exibe uma interface do usuário para obter informações de identidade para o usuário. No entanto, se o parâmetro *dwFlags* contiver o \_ \_ sinalizador não interativo de sinalizador EAP do RAS \_ \_ , **RasEapGetIdentity** não deverá exibir uma interface do usuário.

Se [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) exibir uma interface do usuário, a interface do usuário deverá oferecer suporte a mensagens de [**\_ comando do WM**](../menurc/wm-command.md) , em que o valor de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) é igual a IDCANCEL.

O serviço de autenticação chama [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) se o valor [RAS \_ EAP \_ valueName \_ Invoke \_ NAMEDLG](authentication-protocol-registry-values.md) que está no registro para esse EAP é definido como zero. Se RAS \_ EAP \_ valueName \_ Invoke \_ NAMEDLG não estiver presente, ou estiver presente e estiver definido como um, o serviço de autenticação exibirá a caixa de diálogo padrão de nome de usuário do sistema.

Além do RAS \_ EAP \_ valueName \_ Invoke \_ NAMEDLG, o fornecedor do EAP pode criar um valor relacionado, [RAS \_ EAP \_ valueName \_ invocar \_ PWDDLG](authentication-protocol-registry-values.md), no registro. Se esse valor estiver presente e for definido como zero, o serviço não exibirá a caixa de diálogo padrão de senha do sistema. Esse valor é útil ao implementar um método biométrico, como uma verificação de impressão digital, para autenticar o usuário. Se os valores de RAS \_ EAP \_ valueName \_ Invoke \_ NAMEDLG e RAS \_ EAP \_ valueName \_ Invoke \_ PWDDLG forem zero, uma interface do usuário de identidade poderá ser usada para obter as informações de identidade e biométrica. No entanto, se somente RAS \_ EAP \_ valueName \_ Invoke \_ PWDDLG for zero, o serviço de autenticação não chamará [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). Nesse caso, você pode usar a [interface do usuário interativa](interactive-user-interface.md) para obter informações biométricas.

Para obter mais informações sobre esses valores de registro, consulte [valores de registro do protocolo de autenticação](authentication-protocol-registry-values.md).

As informações obtidas pelo [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) são passadas para o protocolo de autenticação durante a chamada para [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). As informações são apontadas pelos membros **pszIdentity** e **pUserData** da estrutura de [**\_ \_ entrada do EAP do PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . Para salvar essas informações no registro no computador cliente, o protocolo de autenticação deve retornar as informações no parâmetro *pEapOutput* de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Após a chamada para [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), o serviço de autenticação chama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar a memória ocupada por esses dados. Portanto, o protocolo de autenticação deve copiar as informações em um buffer de memória privada durante a chamada para **RasEapBegin**.

 

 