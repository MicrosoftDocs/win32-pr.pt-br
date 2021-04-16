---
title: Aplicação da camada de aplicativo (EPA)
description: A EPA é um conjunto de camadas de modo de kernel da WFP (plataforma de filtragem do Windows) que são usadas para filtragem com monitoração de estado.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365966"
---
# <a name="application-layer-enforcement-ale"></a>Aplicação da camada de aplicativo (EPA)

A EPA é um conjunto de camadas de modo de kernel da WFP (plataforma de filtragem do Windows) que são usadas para filtragem com monitoração de estado.

A filtragem com monitoração de estado controla o estado das conexões de rede e permite apenas os pacotes que correspondem a um estado de conexão conhecido. Por exemplo, a filtragem com monitoração de estado para uma conexão TCP iniciada por trás de um firewall pode permitir apenas pacotes de entrada que correspondam aos pacotes de saída anteriores enviados pela parte protegida.

Filtros nas camadas de ALE autorizam a criação de conexão de entrada e saída, atribuições de porta, operações de soquete como [**escuta ()**](/windows/desktop/api/winsock2/nf-winsock2-listen), criação de soquete bruto e modo promíscuo recebendo.

O tráfego nas camadas ALE é classificado por conexão ou operação por soquete. Em camadas não ALE, os filtros só podem classificar o tráfego em uma base por pacote.

As camadas de ALE são as únicas camadas de WFP em que o tráfego de rede pode ser filtrado com base na identidade do aplicativo — usando um nome de arquivo normalizado — e com base na identidade do usuário — usando um descritor de segurança. (Consulte FLT \_ Informações de nome de arquivo \_ \_ na documentação do Windows Driver Kit (WDK), para obter mais informações sobre nomes de arquivo normalizados.)

Além disso, quando o IPsec é usado para proteger a conexão, a filtragem em camadas ALE também pode ser executada na identidade do computador remoto e na identidade do usuário remoto. As identidades do computador remoto e do usuário são obtidas das credenciais usadas na criação de uma sessão IPsec.

Por esse motivo, as políticas que impõem quem (por exemplo, "administrador") e/ou qual aplicativo (por exemplo, "Internet Explorer") têm permissão para executar as operações de rede mencionadas acima são criadas nas camadas da ALE.

A EPA fornece imposição para políticas como "permitir que o Windows Messenger todo o acesso à rede ao bloquear todos os outros aplicativos". Nesse exemplo, quando o aplicativo "Messenger" se conecta pela rede, a EPA intercepta o evento, determina que ele foi iniciado pelo Messenger e consulta o mecanismo de filtro de WFP para determinar se o soquete deve ter permissão para continuar.

> [!Note]  
> Devido à natureza dos soquetes de IP duplo, as classificações na camada ALE de IPv4 podem não ocorrer. Isso é por design, porque para todas as intenções e finalidades, o soquete é um soquete IPv6. Para ver o tráfego v4 para esse soquete, crie filtros na camada V6 usando o endereço mapeado para IPv6.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Camadas ALE](ale-layers.md)
</dt> <dt>

[Filtragem de estado de ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfego de difusão/multicast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalização de fluxo ALE](ale-flow-customization.md)
</dt> </dl>

 

 