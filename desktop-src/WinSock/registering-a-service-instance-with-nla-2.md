---
description: Os clientes NLA podem registrar informações de configuração de rede em todo o sistema, permitindo que consultas futuras retornem as informações de configuração especificadas, independentemente de a rede estar ativa.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrando uma instância de serviço com NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a623f28d30d02cd3a1266e173dbe28270f377a55c3f59f8ff095cf3d023a80eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641676"
---
# <a name="registering-a-service-instance-with-nla"></a>Registrando uma instância de serviço com NLA

Os clientes NLA podem registrar informações de configuração de rede em todo o sistema, permitindo que consultas futuras retornem as informações de configuração especificadas, independentemente de a rede estar ativa. Essa funcionalidade permite que os clientes NLA afetem uma experiência consistente do usuário de informações de rede em vários aplicativos.

## <a name="parameters"></a>Parâmetros

Para registrar uma instância de serviço com o provedor de serviços de Reconhecimento de Localização de Rede, use a [**função WSASetService.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) Para registrar corretamente uma instância de serviço, determinados parâmetros da **função WSASetService** devem ser definidos com as informações apropriadas, conforme explicado nesta seção. Para referência rápida, a **função WSASetService** tem a seguinte sintaxe:

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

Para o parâmetro *lpqsRegInfo,* forneça uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) de um resultado de consulta NLA SP ou construído aderindo aos requisitos de uma consulta NLA SP, conforme especificado em [Consultando NLA](querying-nla-2.md).

As operações com suporte para *o parâmetro essOperation* são as seguintes:

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE \_ REGISTER
</dt> <dd>

A rede definida na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecida em *lpqsRegInfo* se tornou persistente para o usuário ativo ao armazenar a instância de rede no hive do Registro para o usuário atual, o que permite a representação.

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ DELETE
</dt> <dd>

Se a rede definida na [**estrutura WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecida em *lpqsRegInfo* for persistente, ela será removida.

</dd> </dl>

A operação especificada no parâmetro *essOperation* pode ser modificada pelas seguintes opções, que podem ser especificadas com lógica OR binária:

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NOME AMIGÁVEL DE NLA \_ \_
</dt> <dd>

Quando usado com RNRSERVICE REGISTER, o campo \_ *lpszComment* da rede definida em *lpqsRegInfo* é verificado quanto à validade e armazenado persistentemente. Quando usado com RNRSERVICE DELETE e a rede definida tiver um nome amigável, o nome amigável será removido, mas a entrada de \_ rede será deixada intacta.

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA \_ ALLUSERS \_ NETWORK
</dt> <dd>

Quando usada com RNRSERVICE REGISTER, a entrada é armazenada persistentemente em HKEY LOCAL MACHINE, disponibilizando-a durante consultas a todos os usuários \_ \_ no computador \_ local. Quando usado com RNRSERVICE \_ DELETE, a rede especificada é removida do HKEY \_ LOCAL \_ MACHINE. Um erro será retornado se a rede especificada não estiver presente. Para excluir uma rede do hive do Registro do usuário atual, esse sinalizador não deve ser especificado. Esse sinalizador só é válido no contexto de segurança de um administrador do sistema local.

</dd> </dl>

O NLA dá suporte aos seguintes códigos de erro para chamadas de função [**WSASetService:**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

| Erro             | Significado                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | Uma chamada bem-sucedida para [**a função WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar o NLA não foi executada.                                                                  |
| WSAEACCESS        | NLA \_ ALLUSERS \_ NETWORK foi especificado em *dwControlFlags* enquanto não estava no contexto de segurança de um administrador do sistema local.                                                |
| WSAEALREADY       | A rede especificada já está armazenada persistentemente da maneira solicitada e nenhum sinalizador foi especificado em *dwControlFlags* para indicar uma atualização para a entrada existente. |
| WSAEAFNOSUPPORT   | Foi especificada uma família de protocolos para a qual não há suporte. Somente as famílias de protocolo IP têm suporte no NLA.                                                             |
| WSAEPFNOSUPPORT   | Foi especificado um protocolo para o qual não há suporte. Somente o protocolo IP tem suporte no NLA.                                                                              |



 

 

 



