---
title: Interface do usuário de configuração do Client-Side
description: O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface do usuário de configuração para o protocolo.
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7296f6afd8fd84f287b6c2c7085e5ed92685f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293977"
---
# <a name="client-side-configuration-user-interface"></a>Interface do usuário de configuração do Client-Side

O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface do usuário de configuração para o protocolo. A interface do usuário de configuração pode ser implementada na mesma DLL como o protocolo de autenticação ou em uma DLL separada. Além disso, a DLL que implementa a interface do usuário de configuração pode dar suporte a mais de um protocolo de autenticação. O caminho para a DLL da interface do usuário de configuração é armazenado no \_ \_ valor do registro RAS EAP valueName \_ CONFIGUI, sob a chave do protocolo de autenticação. Para obter mais informações sobre como criar esse valor de registro, consulte [instalação EAP](eap-installation.md).

A DLL para a interface do usuário de configuração deve exportar pontos de entrada para as seguintes funções:

[**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Quando o usuário cria uma entrada de configuração para uma conexão específica, seja para um cliente RAS ou sem fio, o usuário é capaz de selecionar o protocolo de autenticação que o serviço deve usar com essa entrada. Se o protocolo de autenticação for configurável, o serviço chamará [**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) para invocar a interface do usuário de configuração. A interface do usuário de configuração armazena as informações de configuração retornadas por **RasEapInvokeConfigUI** na entrada de configuração.

As informações de configuração devem ser genéricas a todos os usuários no computador cliente. Informações específicas para um usuário específico ou usuários não devem ser armazenadas na entrada. O protocolo de autenticação deve obter informações específicas do usuário usando as [funções de identidade](obtaining-identity-information.md) ou a [interface do usuário interativa](interactive-user-interface.md). O protocolo de autenticação pode armazenar essas informações no registro passando-as para o serviço de autenticação no parâmetro *pEapOutput* de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

As informações de configuração também não devem ser específicas para a máquina atual; Ele deve ser portátil do computador para o computador.

Quando o serviço de autenticação chama a função [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) para o protocolo de autenticação, ele passa uma estrutura de [**\_ \_ entrada PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) que contém um ponteiro para as informações de configuração. Após a chamada para **RasEapBegin** ser concluída, o serviço de autenticação chama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar a memória ocupada pelas informações de configuração. Portanto, o protocolo de autenticação deve copiar as informações de configuração em um buffer de memória privada durante a chamada para **RasEapBegin**.

O fornecedor pode adicionar um valor na chave do registro para o protocolo de autenticação que especifica as informações de configuração padrão para o protocolo. O fornecedor também pode adicionar um valor que especifica se o usuário precisa inserir informações de configuração ao criar uma entrada de catálogo telefônico. Para obter mais informações, consulte [valores do registro do protocolo de autenticação](authentication-protocol-registry-values.md).

 

 