---
description: A API do Auxiliar de Protocolo IP permite a recuperação e a modificação das definições de configuração de rede para o computador local.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6262543d1644fbe62858f2c90064f42d2c1348b2f3c56033813f453d33470ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146769"
---
# <a name="ip-helper"></a>Auxiliar de IP

## <a name="purpose"></a>Finalidade

A API do Auxiliar de Protocolo IP permite a recuperação e a modificação das definições de configuração de rede para o computador local.

## <a name="where-applicable"></a>Quando aplicável

A API auxiliar de IP é aplicável em qualquer ambiente de computação em que a manipulação programática de rede e a configuração de TCP/IP é útil. Os aplicativos típicos incluem protocolos de roteamento de IP e agentes SNMP (Simple Network Management Protocol).

## <a name="developer-audience"></a>Público de desenvolvedores

A API auxiliar de IP foi projetada para uso por programadores C/C++. Os programadores também devem estar familiarizados com Windows rede e conceitos de rede TCP/IP.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API auxiliar de IP pode ser usada em todas as Windows plataformas. Nem todos os sistemas operacionais são suportados por todas as funções. Quando determinadas implementações ou funcionalidades Windows de plataforma soquetes 2 existem, elas são claramente notadas na documentação. Se uma função auxiliar de IP for chamada em uma plataforma que não dá suporte à função, ERROR \_ NOT \_ SUPPORTED será retornado. Para obter informações mais específicas sobre quais sistemas operacionais suportam uma função específica, consulte as seções Requisitos na documentação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                              | Descrição                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novidades no Auxiliar de IP](what-s-new-in-ip-helper.md)<br/>  | Informações sobre novos recursos para o Auxiliar de IP.<br/>                                                                                                                                                             |
| [Sobre o Auxiliar de IP](about-ip-helper.md)<br/>                  | Informações gerais sobre as considerações e funcionalidades de programação do Auxiliar de IP disponíveis para desenvolvedores.<br/>                                                                                               |
| [Usando o Auxiliar de IP](using-ip-helper.md)<br/>                  | Procedimentos e técnicas de programação usados com o Auxiliar de IP. Esta seção inclui técnicas básicas de programação do Auxiliar de IP, como [Ponto de Partida Com o Auxiliar de IP.](getting-started-with-ip-helper.md)<br/> |
| [Referência auxiliar de IP](ip-helper-function-reference.md)<br/> | Documentação de referência para funções, estruturas e enumerações do Auxiliar de IP.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Soquetes 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[Serviço de Roteamento e Acesso Remoto](../rras/routing-start-page.md)
</dt> </dl>

 

