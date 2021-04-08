---
description: Os aplicativos distribuídos (cliente/servidor) usam pacotes de segurança para obter conexões autenticadas e mensagens do Exchange.
ms.assetid: 8f28177f-335a-4fa2-bf66-2ec1698bebec
title: Inicialização do modo de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473b06daf2e1c3612b02583d203ce4cd9afebabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922313"
---
# <a name="user-mode-initialization"></a>Inicialização do modo de usuário

Os aplicativos distribuídos (cliente/servidor) usam [*pacotes de segurança*](../secgloss/s-gly.md) para obter conexões autenticadas e mensagens do Exchange. O aplicativo chama funções de SSPI (interface do provedor de suporte de segurança) que são mapeadas para [funções implementadas pelo SSP/APS](authentication-functions.md)e [funções implementadas pelo SSP/APS do modo de usuário](authentication-functions.md). Esse mapeamento é executado pela DLL do provedor de segurança (Secur32.dll ou Security.dll), que pode ser carregada nos processos do cliente e do servidor dinamicamente. A DLL também pode ser vinculada estaticamente usando Secur32. lib. A DLL e a LIB são fornecidas com o SDK (Software Development Kit) do Microsoft Windows.

Carregar o pacote de segurança no processo do cliente ou do servidor é tratado pelo sistema, se a DLL do SSP/AP que contém o pacote de segurança estiver corretamente registrada.

O servidor inicia o processo de obtenção de uma conexão segura com um cliente monitorando uma porta, aguardando um cliente enviar uma mensagem. O cliente inicia o processo de obtenção de uma conexão segura com o servidor chamando a função SSPI [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta). Essa função é mapeada para a função [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) do pacote de segurança personalizado. **SpInitLsaModeContext** retorna um token para o cliente, que o encaminha para o servidor.

Após receber o token do cliente, o servidor chama a função SSPI [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), que é expedida para a função [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) do pacote de segurança. Se a função **SpAcceptLsaModeContext** for bem-sucedida e nenhum processamento for necessário para estabelecer o contexto de segurança, a função deverá retornar o status \_ Success ao chamador. Se o processamento adicional for necessário, a função deverá retornar s \_ I \_ continue \_ necessário e retorna um token para o servidor. O servidor encaminha o token para o cliente, que chama [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) novamente.

Esse ciclo de chamada pode ser repetido sempre que necessário até que uma conexão autenticada seja estabelecida ou falhe. Durante esse processo, se a função [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) ou [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) for bem-sucedida e nenhum processamento for necessário para estabelecer o [*contexto de segurança*](../secgloss/s-gly.md), a função deverá retornar o status \_ Success ao chamador. Se o processamento adicional for necessário, a função deverá retornar \_ s \_ \_ e continuar necessário e retornar um token para o chamador, que é responsável por encaminhá-lo.

O protocolo implementado pelo pacote de segurança determina o número de vezes que esse ciclo é repetido. Por exemplo, em pacotes de segurança que dão suporte à autenticação mútua de três trechos, a sequência de chamada é a seguinte:

1.  O cliente obtém um token chamando [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)e o envia para o servidor. O servidor chama [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) pela primeira vez e Obtém um token de resposta que ele envia para o cliente.
2.  O cliente usa o token recebido do servidor em uma segunda chamada para [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)e retorna um token final. O cliente envia esse token para o servidor.
3.  O servidor recebe o token gerado no segmento 2 que ele usa na chamada final para [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).

Quando as funções [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) e [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) são bem-sucedidas e nenhum processamento é necessário para estabelecer o contexto de segurança, as funções devem retornar o status \_ êxito ao chamador. Além disso, se o pacote de segurança personalizado oferecer suporte às [funções implementadas pelo SSP/APS do modo de usuário](authentication-functions.md), **SpAcceptLsaModeContext** e **SpInitLsaModeContext** deverão retornar **true** por meio do parâmetro *MappedContext* . O valor de *MappedContext* não é passado de volta para o aplicativo; Ele é interceptado pela LSA.

Quando *MappedContext* é **true**, a LSA chama a função [**SpUsermodeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) da dll do SSP/AP. Essa função fornece tabelas de ponteiros para as funções de modo de usuário implementadas por cada pacote de segurança. A função [**SpInstanceInit**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn) de cada pacote é chamada, usando as tabelas de função retornadas por **SpUsermodeInitialize**. **SpInstanceInit** recebe uma tabela de ponteiros para [funções LSA chamadas por SSP/APS do modo de usuário](authentication-functions.md).

 

 
