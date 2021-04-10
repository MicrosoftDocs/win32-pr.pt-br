---
title: Servidor de Políticas de Rede
description: O NPS (servidor de diretivas de rede) é a implementação da Microsoft de um servidor RADIUS e proxy de autenticação remota.
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294162"
---
# <a name="network-policy-server"></a>Servidor de Políticas de Rede

## <a name="purpose"></a>Finalidade

O NPS (servidor de diretivas de rede) é a implementação da Microsoft de um servidor RADIUS e proxy de autenticação remota. É o sucessor do IAS (serviço de autenticação da Internet).

Como um servidor RADIUS, o NPS executa autenticação, autorização e contabilidade para conexões sem fio, de comutador de autenticação e de VPN (rede virtual privada) e dial-up de acesso remoto.

O NPS também é um servidor avaliador de integridade para NAP (proteção de acesso à rede). O NPS executa a autenticação e a autorização de tentativas de conexão de rede e, com base nas políticas de integridade do sistema configuradas, avalia a conformidade da integridade do computador e determina como limitar o acesso à rede ou a comunicação de um computador não compatível. Este é um novo recurso específico somente ao NPS; O IAS não oferece suporte a ele. Consulte [serviço de autenticação da Internet e servidor de políticas de rede](internet-authentication-service-vs-network-policy-server.md) para obter uma lista completa dos recursos novos para o NPS.

O NPS inclui dois conjuntos de API: API de extensões do NPS e API de SDO (objetos de dados do servidor). Tanto a API de extensões NPS quanto a API de SDO também são compatíveis com o precurso do NPS, o serviço de autenticação da Internet.

A API de extensões do NPS pode ser usada para estender os métodos de autenticação, autorização e contabilidade oferecidos pelo NPS e anteriormente pelo IAS.

A API de objetos de dados do servidor pode ser usada para manipular a configuração da diretiva de rede em um computador que executa o NPS ou o IAS.

> [!Note]  
> As políticas de rede no NPS são equivalentes às políticas de acesso remoto no IAS.

 

## <a name="developer-audience"></a>Público de desenvolvedores

A API de extensões do NPS foi projetada para uso por programadores que usam o software de desenvolvimento C/C++. Os programadores devem estar familiarizados com os conceitos de rede e o protocolo RADIUS. O RADIUS está documentado em [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

A API de objetos de dados do servidor foi projetada para uso por programadores usando o software de desenvolvimento C/C++ ou Visual Basic. Os programadores devem estar familiarizados com o RAS ( [serviço de acesso remoto](/windows/desktop/RRAS/remote-access-request-for-comments) ) e o protocolo RADIUS.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API de extensões do NPS tem suporte no Windows Server 2008 com a instalação do serviço de Internet comercial da Microsoft (MCIS).

A API de objetos de dados do servidor tem suporte no Windows Server 2008.

O NPS está disponível no Windows Server 2008 com a instalação do serviço de Internet comercial da Microsoft (MCIS).

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Visão geral](about-network-policy-server.md)
</dt> <dd>

Informações gerais sobre RADIUS, IAS e NPS.

</dd> <dt>

[API de extensões do servidor de políticas de rede](ias-extensions.md)
</dt> <dd>

API para implementar DLLs de extensão usadas para autenticação, autorização e contabilidade.

</dd> <dt>

[API de objetos de dados do servidor](server-data-objects.md)
</dt> <dd>

API para gerenciar a configuração de política de rede.

</dd> <dt>

[Programação do SQL](sql-programmability.md)
</dt> <dd>

Exemplos de procedimentos armazenados usados para gerenciar o registro em log do NPS (IAS).

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TechNet: servidor de políticas de rede](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[TechNet: serviço de autenticação da Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[Proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 