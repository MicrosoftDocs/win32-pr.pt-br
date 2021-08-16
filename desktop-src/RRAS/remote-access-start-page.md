---
title: Acesso remoto
description: Use o serviço de acesso remoto (RAS) para criar aplicativos cliente.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS do serviço de acesso remoto
- RAS RAS
- RAS do serviço de acesso remoto, página inicial
- RAS do RAS, consulte acesso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e300061c328751f288634faf2f36ab0391ba41d7079e4f42c842d31b3e29397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788281"
---
# <a name="remote-access"></a>Acesso remoto

## <a name="purpose"></a>Finalidade

Use o serviço de acesso remoto (RAS) para criar aplicativos cliente. Esses aplicativos exibem caixas de diálogo comuns de RAS, gerenciam dispositivos e conexões de acesso remoto e manipulam entradas de catálogo telefônico. O RAS também fornece a próxima geração de funcionalidade de servidor para o RAS (serviço de acesso remoto) para Windows. A funcionalidade de servidor RRAS segue e se baseia no serviço de acesso remoto (RAS).

## <a name="where-applicable"></a>Quando aplicável

O serviço de acesso remoto é aplicável em qualquer ambiente computacional que usa um link WAN (rede de longa distância) ou uma VPN (rede virtual privada). O RAS torna possível conectar um computador cliente remoto a um servidor de rede por meio de um link WAN ou VPN. O computador remoto, em seguida, funciona na LAN do servidor como se o computador remoto estivesse conectado diretamente à LAN. A API RAS permite que os programadores acessem os recursos do RAS de forma programática.

## <a name="developer-audience"></a>Público de desenvolvedores

A API de RAS foi projetada para uso por programadores C/C++. os programadores do Microsoft Visual Basic também podem encontrar a API útil. Os programadores devem estar familiarizados com os conceitos de rede.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Algumas das funções na API RAS têm suporte apenas em servidores de rede e outras funções têm suporte apenas em clientes de rede. Para obter informações mais específicas sobre quais sistemas operacionais dão suporte a uma função específica, consulte as seções de requisitos na documentação do.

a [funcionalidade avançada de RAS](function-comparison-windows-2000-versus-rras-redistributable.md) do RRAS está disponível para o Windows NT Server 4,0 instalando o [RRAS redistribuível](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp). toda a funcionalidade do RRAS é incorporada ao servidor Windows 2000, Windows server 2003 e Windows server 2008. os aplicativos RRAS não podem ser executados no Windows NT estação de trabalho 4,0 ou em sistemas operacionais cliente, como Windows 95. Para obter informações mais específicas sobre quais sistemas operacionais dão suporte a uma função específica, consulte as seções de requisitos na documentação do.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Serviço de acesso remoto](about-remote-access-service.md)<br/>                               | O RAS (serviço de acesso remoto) fornece recursos de acesso remoto a aplicativos cliente em computadores que executam o Windows.<br/>                                                                                          |
| [Administração do serviço de acesso remoto](about-remote-access-service-administration.md)<br/> | A administração do serviço de acesso remoto fornece um conjunto de funções para administrar permissões e portas de usuário em servidores RAS. Usando essas funções, você pode desenvolver um aplicativo de administração de servidor RAS.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Roteiros](routing-start-page.md)
</dt> <dt>

[Protocolos de roteamento](routing-protocols-start-page.md)
</dt> </dl>

 

 





