---
description: Necessidades de desempenho de usuários e administradores com aplicativos Windows Sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Necessidades de desempenho: usuários e administradores'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010482"
---
# <a name="performance-needs-users-and-administrators"></a>Necessidades de desempenho: usuários e administradores

Os usuários julgam o desempenho do aplicativo de acordo com sua experiência:

-   O aplicativo é rápido para responder?
-   Um ícone de ampulheta é exibido enquanto as operações em segundo plano são executadas?
-   O aplicativo é iniciado e fechado rapidamente?
-   Os erros são manipulados de forma compreensível?

Para resumir, os usuários querem que os aplicativos sejam rápidos e previsíveis.

Por outro lado, os administradores costumam avaliar o desempenho de um aplicativo em quão eficientemente ele usa os recursos de rede. Os administradores podem perguntar:

-   O aplicativo tem baixa sobrecarga e um uso de rede eficiente?
-   O número mínimo de conexões é usado, portanto, meu servidor pode atender o máximo possível de usuários de uma vez?
-   Estou constantemente ligando para o helpdesk?

Em suma, os administradores querem que os aplicativos sejam dimensionados.

## <a name="best-practices-for-performance-needs"></a>Práticas recomendadas para necessidades de desempenho

Ao desenvolver um aplicativo do Windows Sockets, esses requisitos de desempenho são convertidos em regras úteis.

-   Fazer com que os aplicativos de rede sejam inicializados rapidamente.

    A interface do usuário não deve esperar por respostas de rede. Algumas tarefas podem ser executadas antes que a rede esteja disponível ou sem a rede. Se a rede não estiver respondendo, o usuário poderá precisar da interface do usuário para operações simples, como fechar o aplicativo.

-   Não aguarde a rede ser desligada.

    Aplicativos cliente-servidor gravados corretamente tratam desconexões anuladas normalmente. Não inicie uma operação potencialmente demorada, como sincronizar arquivos ou pastas com um servidor, que não pode ser interrompido no desligamento. As redes não são responsivas consistentemente, portanto, até mesmo as pequenas operações poderiam provar tempo demorado. Forneça comentários positivos para os usuários, incluindo indicações de progresso e tempos de conclusão estimados.

-   Garanta uma interface do usuário responsiva.

    A capacidade de resposta do aplicativo ajuda a eliminar chamadas de helpdesk desnecessárias. Uma boa diretriz para resposta interativa é de 500 milissegundos. Os usuários percebem pausas por mais de 500 milissegundos como um retardo no desempenho. Os aplicativos devem ser responsivos o suficiente para fornecer ao usuário confiança sobre o aplicativo.

-   Analisar erros de rede.

    Nem todos os erros de rede são críticos. Por exemplo, um aplicativo que recebeu ou postou todos os seus dados pode, provavelmente, ignorar erros ao fechar a conexão. Não presuma que a rede ou o usuário esteja disponível; Trate erros sem intervenção do usuário ou ignore-os se os erros forem não críticos.

-   Um aplicativo deve definir seus próprios tempos limite razoáveis.

    Por exemplo, uma solicitação do Windows Sockets Connect () pode bloquear em algumas condições para até 21 segundos. Os aplicativos podem precisar introduzir seus próprios tempos limite conforme apropriado para seus usuários.

-   Minimizar a sobrecarga de protocolo.

    Conservar a largura de banda da rede está parcialmente prestes a minimizar a sobrecarga de protocolo incorrida pelo seu aplicativo. Ele também está prestes a eliminar o tráfego de rede desnecessário. Protocolos com uma sobrecarga de cabeçalho inferior podem ser usados para transferir dados de aplicativos. Por exemplo, ao enviar quantidades menores de dados não críticos ou repetíveis, use UDP em oposição ao TCP para reduzir a sobrecarga associada ao estabelecimento e à manutenção da conexão. Se os mesmos dados precisarem ser enviados a vários destinatários, considere multicast. Lembre-se de que os aplicativos UDP não são controlados por fluxo — o envio por push além da largura de banda disponível pode causar uma falha catastrófica na rede. O utilitário netstat pode ser usado com as opções **-** e e **-s** para exibir estatísticas de vários protocolos.

-   Conservar recursos do sistema.

    Os recursos do sistema podem ser consumidos rapidamente se o retentor adequado não for usado. Por exemplo, soquetes e conexões TCP consomem recursos. Não use várias conexões TCP por cliente, em que uma atenderá à finalidade do aplicativo.

Para aplicativos transacionais, boa experiência do usuário e baixa utilização da rede não são metas conflitantes. A rede é um afunilamento. Aplicativos com uso intensivo de rede passam mais tempo aguardando, e aplicativos de rede bem escritos são projetados para minimizar o tempo de espera desnecessário, tanto para a interface do usuário quanto para as transmissões de rede.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de alto desempenho do Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensões de desempenho](performance-dimensions-2.md)
</dt> </dl>

 

 



