---
title: Client-Side configuração Interface do Usuário
description: O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface do usuário de configuração para o protocolo.
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c8b067ba65312edea412ba532620e029912088e9cc61885626f8a13f5a2834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117796"
---
# <a name="client-side-configuration-user-interface"></a>Client-Side configuração Interface do Usuário

O fornecedor que implementa o protocolo de autenticação também pode fornecer uma interface do usuário de configuração para o protocolo. A interface do usuário de configuração pode ser implementada na mesma DLL que o protocolo de autenticação ou em uma DLL separada. Além disso, a DLL que implementa a interface do usuário de configuração pode dar suporte a mais de um protocolo de autenticação. O caminho para a DLL para a interface do usuário de configuração é armazenado no valor do registro RAS \_ EAP VALUENAME CONFIGUI, na chave \_ do protocolo de \_ autenticação. Para obter mais informações sobre como criar esse valor do Registro, consulte [Instalação do EAP](eap-installation.md).

A DLL para a interface do usuário de configuração deve exportar pontos de entrada para as seguintes funções:

[**Raseapinvokeconfigui**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**Raseapfreememory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Quando o usuário cria uma entrada de configuração para uma conexão específica, seja para um cliente RAS ou sem fio, o usuário pode selecionar o protocolo de autenticação que o serviço deve usar com essa entrada. Se o protocolo de autenticação for configurável, o serviço [**chamará RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) para invocar a interface do usuário de configuração. A interface do usuário de configuração armazena as informações de configuração retornadas por **RasEapInvokeConfigUI** na entrada de configuração.

As informações de configuração devem ser genéricas para todos os usuários no computador cliente. Informações específicas para um usuário específico ou usuários não devem ser armazenadas na entrada. O protocolo de autenticação deve obter informações específicas do usuário usando as funções [de identidade](obtaining-identity-information.md) ou a interface do [usuário interativa](interactive-user-interface.md). O protocolo de autenticação pode armazenar essas informações no Registro passando-as para o serviço de autenticação no parâmetro *pEapOutput* de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

As informações de configuração também não devem ser específicas para o computador atual; ele deve ser portátil de computador para computador.

Quando o serviço de autenticação chama a [**função RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) para o protocolo de autenticação, ele passa uma estrutura [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) que contém um ponteiro para as informações de configuração. Após a conclusão da chamada **para RasEapBegin,** o serviço de autenticação chama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar a memória ocupada pelas informações de configuração. Portanto, o protocolo de autenticação deve copiar as informações de configuração para um buffer de memória privada durante a chamada para **RasEapBegin.**

O fornecedor pode adicionar um valor sob a chave do Registro para o protocolo de autenticação que especifica informações de configuração padrão para o protocolo. O fornecedor também pode adicionar um valor que especifica se o usuário precisa inserir informações de configuração ao criar uma entrada de phone-book. Para obter mais informações, consulte [Valores do Registro do Protocolo de Autenticação](authentication-protocol-registry-values.md).

 

 