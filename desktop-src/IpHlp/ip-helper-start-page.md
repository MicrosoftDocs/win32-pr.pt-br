---
description: A API do auxiliar de protocolo de Internet (IP Helper) permite a recuperação e a modificação de definições de configuração de rede para o computador local.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827053"
---
# <a name="ip-helper"></a>Auxiliar de IP

## <a name="purpose"></a>Finalidade

A API do auxiliar de protocolo de Internet (IP Helper) permite a recuperação e a modificação de definições de configuração de rede para o computador local.

## <a name="where-applicable"></a>Quando aplicável

A API auxiliar de IP é aplicável em qualquer ambiente computacional no qual a manipulação programática da rede e da configuração de TCP/IP é útil. Os aplicativos típicos incluem protocolos de roteamento IP e agentes SNMP (Simple Network Management Protocol).

## <a name="developer-audience"></a>Público de desenvolvedores

A API auxiliar de IP foi projetada para ser usada por programadores C/C++. Os programadores também devem estar familiarizados com os conceitos de rede do Windows e de rede TCP/IP.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API auxiliar de IP pode ser usada em todas as plataformas Windows. Nem todos os sistemas operacionais dão suporte a todas as funções. Quando determinadas implementações ou recursos de restrições de plataforma do Windows Sockets 2 existem, eles são claramente indicados na documentação. Se uma função auxiliar de IP for chamada em uma plataforma que não oferece suporte à função, o erro \_ não \_ terá suporte será retornado. Para obter informações mais específicas sobre quais sistemas operacionais dão suporte a uma função específica, consulte as seções de requisitos na documentação do.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                              | Descrição                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [O que há de novo no auxiliar de IP](what-s-new-in-ip-helper.md)<br/>  | Informações sobre novos recursos para o auxiliar de IP.<br/>                                                                                                                                                             |
| [Sobre o auxiliar de IP](about-ip-helper.md)<br/>                  | Informações gerais sobre as considerações e os recursos de programação do auxiliar de IP disponíveis para os desenvolvedores.<br/>                                                                                               |
| [Usando o auxiliar de IP](using-ip-helper.md)<br/>                  | Procedimentos e técnicas de programação usados com o auxiliar de IP. Esta seção inclui técnicas básicas de programação de IP auxiliar, como [introdução com o auxiliar de IP](getting-started-with-ip-helper.md).<br/> |
| [Referência auxiliar de IP](ip-helper-function-reference.md)<br/> | Documentação de referência para as funções, estruturas e enumerações do IP Helper.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[Serviço de Roteamento e Acesso Remoto](../rras/routing-start-page.md)
</dt> </dl>

 

