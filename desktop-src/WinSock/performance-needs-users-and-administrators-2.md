---
description: Necessidades de desempenho de usuários e administradores com Windows soquetes (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Necessidades de desempenho: usuários e administradores'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c74f4ec6f0a545a98a890f0bc8ff954fe43a3f79fc04fd2c2d92e68ea9f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097666"
---
# <a name="performance-needs-users-and-administrators"></a>Necessidades de desempenho: usuários e administradores

Os usuários avaliam o desempenho do aplicativo por sua experiência:

-   O aplicativo é rápido para responder?
-   Um ícone de ampulheta é exibido enquanto as operações em segundo plano são executadas?
-   O aplicativo é lançado e fechado rapidamente?
-   Os erros são tratados de maneira compreensível?

Para resumir, os usuários querem que os aplicativos sejam rápidos e previsíveis.

Por outro lado, os administradores geralmente avaliam o desempenho de um aplicativo sobre a eficiência com que ele usa recursos de rede. Os administradores podem perguntar:

-   O aplicativo tem baixa sobrecarga e uso eficiente de rede?
-   O número mínimo de conexões é usado, portanto, meu servidor pode ser atendido o máximo de usuários ao mesmo tempo?
-   Estou chamando constantemente o helpdesk?

Em resumo, os administradores querem que os aplicativos dimensionem.

## <a name="best-practices-for-performance-needs"></a>Práticas recomendadas para necessidades de desempenho

Ao desenvolver um aplicativo Windows Sockets, esses requisitos de desempenho se traduzem em regras úteis.

-   Fazer com que os aplicativos de rede inicializem rapidamente.

    A interface do usuário não deve ter que aguardar respostas de rede. Algumas tarefas podem ser executadas antes que a rede seja disponibilizada ou sem a rede. Se a rede não estiver respondendo, o usuário poderá precisar da interface do usuário para operações simples, como fechar o aplicativo.

-   Não aguarde o desligamento da rede.

    Aplicativos cliente-servidor escritos corretamente lidam com desconectações anulativas normalmente. Não inicie uma operação potencialmente longa, como sincronizar arquivos ou pastas com um servidor, que não pode ser interrompida no desligamento. As redes não são consistentemente responsivas, portanto, até mesmo operações pequenas podem ser demoradas. Forneça comentários positivos para os usuários, incluindo indicações de progresso e tempos de conclusão estimados.

-   Verifique se há uma interface do usuário responsiva.

    A capacidade de resposta do aplicativo ajuda a eliminar chamadas de ajuda desnecessárias. Uma boa diretriz para resposta interativa é de 500 milissegundos. Os usuários agem como um atraso no desempenho em pausas de mais de 500 milissegundos. Os aplicativos devem ser responsivos o suficiente para fornecer ao usuário confiança sobre o aplicativo.

-   Examinar erros de rede.

    Nem todos os erros de rede são críticos. Por exemplo, um aplicativo que recebeu ou postou todos os seus dados provavelmente pode ignorar erros ao fechar a conexão. Não suponha que a rede ou o usuário está disponível; tratar erros sem intervenção do usuário ou ignorá-los se os erros não sãocríticos.

-   Um aplicativo deve definir seus próprios tempos de tempo razoáveis.

    Por exemplo, uma solicitação Windows Sockets connect() pode ser bloqueado em algumas condições por até 21 segundos. Os aplicativos talvez precisem apresentar seus próprios tempos de tempo, conforme apropriado para seus usuários.

-   Minimizar a sobrecarga do protocolo.

    A conservação da largura de banda de rede é parcialmente sobre minimizar a sobrecarga de protocolo incorrida pelo seu aplicativo. Também se trata de eliminar o tráfego de rede desnecessário. Protocolos com uma sobrecarga de header inferior podem ser usados para transferir dados do aplicativo. Por exemplo, ao enviar quantidades menores de dados não acríticos ou reprontáveis, use UDP em vez de TCP para reduzir a sobrecarga associada ao estabelecimento e à manutenção da conexão. Se os mesmos dados devem ser enviados a vários destinatários, considere multicast. Esteja ciente de que os aplicativos UDP não são controlados por fluxo– o esmaeamento além da largura de banda disponível pode causar falha catastrófica na rede. O utilitário Netstat pode ser usado com suas **opções -e** **e -s** para exibir estatísticas para vários protocolos.

-   Conservar recursos do sistema.

    Os recursos do sistema poderão ser consumidos rapidamente se a devida união não for usada. Por exemplo, soquetes e conexões TCP consomem recursos. Não use várias conexões TCP por cliente em que uma atenderá à finalidade do aplicativo.

Para aplicativos transacionais, uma boa experiência do usuário e baixa utilização de rede não são metas conflitantes. A rede é um gargalo. Os aplicativos com uso intensivo de rede gastam mais tempo aguardando e os aplicativos de rede bem escritos são projetados para minimizar o tempo de espera desnecessário, tanto para a interface do usuário quanto para transmissões de rede.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de soquetes Windows de alto desempenho](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensões de desempenho](performance-dimensions-2.md)
</dt> </dl>

 

 



