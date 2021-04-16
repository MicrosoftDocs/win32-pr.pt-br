---
title: Interface do usuário interativa
description: O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface do usuário interativa para o protocolo.
ms.assetid: 4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761799969f4e439a65534ab551f09b3788e95ba7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105764981"
---
# <a name="interactive-user-interface"></a>Interface do usuário interativa

O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface do usuário interativa para o protocolo. A interface de usuário interativa permite que o protocolo de autenticação Obtenha informações adicionais do usuário, conforme necessário, durante o curso da sessão de autenticação.

A interface do usuário interativa pode ser implementada na mesma DLL que o protocolo de autenticação ou em uma DLL separada. Além disso, a DLL que implementa a interface do usuário interativa pode dar suporte a mais de um protocolo de autenticação. O caminho para a DLL para a interface do usuário interativa é armazenado no valor do registro [RAS \_ EAP \_ valueName \_ INTERACTIVEUI](authentication-protocol-registry-values.md) , sob a chave para o protocolo de autenticação. Para obter mais informações sobre como criar esse valor de registro, consulte [instalação EAP](eap-installation.md).

A DLL para a interface do usuário interativa deve exportar pontos de entrada para as seguintes funções:<dl>

[**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)  
[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)  
</dl>

A interface do usuário interativa deve dar suporte a mensagens de [**\_ comando do WM**](../menurc/wm-command.md) em que [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) é igual a IDCANCEL.

Para exibir a interface do usuário interativa, o protocolo de autenticação deve definir o membro **fInvokeInteractiveUI** da estrutura de [**saída do \_ EAP \_ do PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) como **true**. O protocolo de autenticação pode opcionalmente definir os membros **pUIContextData** e **dwSizeOfUIContextData** como **true** também. O serviço de autenticação usa os valores desses membros para passar dados de contexto para a interface do usuário interativa. O protocolo de autenticação retorna a estrutura de **\_ \_ saída de EAP do PPP** como um parâmetro na função [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) .

O serviço de autenticação invoca a interface do usuário interativa chamando [**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui). Em seguida, o serviço passa o protocolo de autenticação um ponteiro para os dados retornados pela interface do usuário interativa na chamada subsequente para [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). O ponteiro é passado como um membro de uma estrutura de [**\_ \_ entrada PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . Depois que **RasEapMakeMessage** retorna, o serviço chama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar a memória ocupada pelas informações. Portanto, o protocolo de autenticação deve copiar as informações em um buffer de memória privada durante a chamada para **RasEapMakeMessage**.

 

 