---
title: Obtendo informações de identidade
description: O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface de função que obtém informações de identificação iniciais para o usuário que está solicitando autenticação.
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46245b22a5538fc347ba735620270b7bbc1071574852305adc6b3881202ae317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605816"
---
# <a name="obtaining-identity-information"></a>Obtendo informações de identidade

O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface de função que obtém informações de identificação iniciais para o usuário que está solicitando autenticação.

O fornecedor deve implementar as funções a seguir.

-   [**Raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**Raseapfreememory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Essas funções podem ser implementadas na mesma DLL que o protocolo de autenticação ou em uma DLL separada. Além disso, a DLL que implementa as funções de identidade pode dar suporte a mais de um protocolo de autenticação. O caminho para a DLL para essas funções é armazenado no valor do registro DE IDENTIDADE VALUENAME DE [RAS \_ \_ \_ EAP,](authentication-protocol-registry-values.md) na chave do protocolo de autenticação. Para obter mais informações sobre como criar esse valor do Registro, consulte [Instalação do EAP](eap-installation.md).

A [**função RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) normalmente exibe uma interface do usuário para obter informações de identidade para o usuário. No entanto, se *o parâmetro dwFlags* contiver o sinalizador RAS \_ EAP FLAG NON \_ \_ \_ INTERACTIVE, **RasEapGetIdentity** não deverá exibir uma interface do usuário.

Se [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) exibir uma interface do usuário, a interface do usuário deverá dar suporte a mensagens [**WM \_ COMMAND**](../menurc/wm-command.md) em que o valor de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) é igual a IDCANCEL.

O serviço de autenticação [**chamará RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) se o [valor DE VALUENAME DE RAS \_ EAP INVOKE \_ \_ \_ NAMEDLG](authentication-protocol-registry-values.md) que está no Registro para essa EAP estiver definido como zero. Se RAS \_ EAP \_ VALUENAME \_ INVOKE NAMEDLG não estiver presente ou estiver presente e estiver definido como um, o serviço de autenticação exibirá a caixa de diálogo nome de usuário do sistema \_ padrão.

Além de RAS EAP VALUENAME INVOKE NAMEDLG, o fornecedor de EAP pode criar um valor \_ \_ \_ \_ relacionado, [RAS \_ EAP \_ VALUENAME \_ INVOKE \_ PWDDLG,](authentication-protocol-registry-values.md)no Registro. Se esse valor estiver presente e estiver definido como zero, o serviço não exibirá a caixa de diálogo de senha do sistema padrão. Esse valor é útil ao implementar um método biométrico, como uma verificação de impressão digital, para autenticar o usuário. Se os valores DE INVOKE \_ \_ NAMEDLG e RAS \_ \_ \_ EAP \_ VALUENAME INVOKE \_ \_ PWDDLG de RAS EAP são zero, uma interface do usuário de identidade pode ser usada para obter as informações biométricas e de identidade. No entanto, se apenas RAS EAP VALUENAME INVOKE PWDDLG for zero, o serviço de autenticação não chamará \_ \_ \_ \_ [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). Nesse caso, você pode usar a [interface interativa do usuário](interactive-user-interface.md) para obter as informações biométricas.

Para obter mais informações sobre esses valores do Registro, consulte Valores do Registro do Protocolo [de Autenticação](authentication-protocol-registry-values.md).

As informações obtidas por [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) são passadas para o protocolo de autenticação durante a chamada para [**RasEapBegin.**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) As informações são apontadas pelos membros **pszIdentity** e **pUserData** da estrutura [**PPP \_ EAP \_ INPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Para salvar essas informações no Registro no computador cliente, o protocolo de autenticação deve retornar as informações no parâmetro *pEapOutput* de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Após a chamada para [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), o serviço de autenticação chama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar a memória ocupada por esses dados. Portanto, o protocolo de autenticação deve copiar as informações para um buffer de memória privada durante a chamada para **RasEapBegin.**

 

 