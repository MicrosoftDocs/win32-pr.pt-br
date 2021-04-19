---
description: Os clientes de NLA podem gravar informações de configuração de rede em todo o sistema, permitindo que consultas futuras retornem as informações de configuração especificadas, independentemente de a rede estar ativa.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrando uma instância de serviço com NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783766"
---
# <a name="registering-a-service-instance-with-nla"></a>Registrando uma instância de serviço com NLA

Os clientes de NLA podem gravar informações de configuração de rede em todo o sistema, permitindo que consultas futuras retornem as informações de configuração especificadas, independentemente de a rede estar ativa. Essa funcionalidade permite que os clientes de NLA afetem uma experiência de usuário consistente de informações de rede em vários aplicativos.

## <a name="parameters"></a>Parâmetros

Para registrar uma instância de serviço com o provedor de serviços de reconhecimento de local de rede, use a função [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) . Para registrar corretamente uma instância de serviço, determinados parâmetros da função **WSASetService** devem ser definidos com as informações apropriadas, conforme explicado nesta seção. Para referência rápida, a função **WSASetService** tem a seguinte sintaxe:

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

Para o parâmetro *lpqsRegInfo* , forneça uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) de um resultado de consulta NLA SP ou tenha construído a adesão aos requisitos de uma consulta NLA SP, conforme especificado em [consultando NLA](querying-nla-2.md).

As operações com suporte para o parâmetro *essOperation* são as seguintes:

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>registro de RNRSERVICE \_
</dt> <dd>

A rede definida na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecida no *lpqsRegInfo* torna-se persistente para o usuário ativo, armazenando a instância de rede no hive do registro para o usuário atual, o que permite a representação.

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ excluir
</dt> <dd>

Se a rede definida na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecida em *lpqsRegInfo* for persistente, ela será removida.

</dd> </dl>

A operação especificada no parâmetro *essOperation* pode ser modificada pelas seguintes opções, que podem ser especificadas com binary ou Logic:

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_nome amigável de NLA \_
</dt> <dd>

Quando usado com o \_ registro RNRSERVICE, o campo *lpszComment* da rede definida em *lpqsRegInfo* é verificado quanto à validade e armazenado de forma persistente. Quando usado com RNRSERVICE \_ Delete e a rede definida tem um nome amigável, o nome amigável é removido, mas a entrada de rede permanece intacta.

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>\_rede NLA AllUsers \_
</dt> <dd>

Quando usado com o \_ registro RNRSERVICE, a entrada é armazenada de forma persistente em hKey \_ local \_ Machine, disponibilizando-a durante consultas a todos os usuários no computador local. Quando usado com RNRSERVICE \_ delete, a rede especificada é removida da \_ máquina local hKey \_ . Um erro será retornado se a rede especificada não estiver presente. Para excluir uma rede do hive do registro do usuário atual, esse sinalizador não deve ser especificado. Esse sinalizador só é válido no contexto de segurança de um administrador do sistema local.

</dd> </dl>

O NLA dá suporte aos seguintes códigos de erro para chamadas de função [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) :

| Erro             | Significado                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | Uma chamada bem-sucedida para a função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar o NLA não foi executada.                                                                  |
| WSAEACCESS        | \_ \_ A rede de NLA AllUsers foi especificada em *dwControlFlags* , embora não esteja no contexto de segurança de um administrador de sistema local.                                                |
| WSAEALREADY       | A rede especificada já está armazenada de forma persistente na maneira solicitada e nenhum sinalizador foi especificado em *dwControlFlags* para indicar uma atualização para a entrada existente. |
| WSAEAFNOSUPPORT   | Uma família de protocolos foi especificada para a qual não há suporte. Somente as famílias de protocolo IP têm suporte no NLA.                                                             |
| WSAEPFNOSUPPORT   | Um protocolo foi especificado para o qual não há suporte. Somente o protocolo IP tem suporte em NLA.                                                                              |



 

 

 



