---
title: Imposição de camada de aplicativo (ALE)
description: ALE é um conjunto de camadas de modo kernel Windows WFP (Plataforma de Filtragem de Dados) que são usadas para filtragem com estado.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d74db5fdc231569f65c3b25cb630b306111aa5d6a7e3eb7faad743a5f74db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069466"
---
# <a name="application-layer-enforcement-ale"></a>Imposição de camada de aplicativo (ALE)

ALE é um conjunto de camadas de modo kernel Windows WFP (Plataforma de Filtragem de Dados) que são usadas para filtragem com estado.

A filtragem com estado acompanha o estado das conexões de rede e permite apenas pacotes que corresponderem a um estado de conexão conhecido. Por exemplo, a filtragem com estado para uma conexão TCP iniciada por trás de um firewall pode permitir somente pacotes de entrada que corresponderem aos pacotes de saída anteriores enviados pela parte protegida.

Filtros nas camadas ALE autorizam a criação de conexão de entrada e saída, atribuições de porta, operações de soquete como [**listen(),**](/windows/desktop/api/winsock2/nf-winsock2-listen)criação de soquete bruto e recebimento de modo promiscuo.

O tráfego nas camadas ALE é classificado por conexão ou operação por soquete. Em camadas não ALE, os filtros só podem classificar o tráfego por pacote.

As camadas ALE são as únicas camadas WFP em que o tráfego de rede pode ser filtrado com base na identidade do aplicativo, usando um nome de arquivo normalizado e com base na identidade do usuário, usando um descritor de segurança. (Consulte FLT \_ INFORMAÇÕES DE NOME DE ARQUIVO Windows documentação do \_ WDK (Driver Kit), para obter mais informações \_ sobre nomes de arquivo normalizados.)

Além disso, quando o IPsec é usado para proteger a conexão, a filtragem em camadas ALE também pode ser executada na identidade do computador remoto e na identidade do usuário remoto. As identidades de usuário e computador remoto são obtidas das credenciais usadas na criação de uma sessão IPsec.

Por esse motivo, as políticas que impõem quem (por exemplo, "administrador") e/ou qual aplicativo (por exemplo, "Internet Explorer") têm permissão para executar as operações de rede mencionadas acima são autoradas nas camadas ALE.

A ALE fornece imposição para políticas como "permitir Windows Messenger todo o acesso à rede enquanto bloqueia todos os outros aplicativos". Nesse exemplo, quando o aplicativo "Messenger" se conecta pela rede, a ALE intercepta o evento, determina que ele foi iniciado pelo Messenger e consulta o mecanismo de filtro WFP para determinar se o soquete deve ter permissão para continuar.

> [!Note]  
> Devido à natureza dos verdadeiros soquetes ip duplos, as classificações na camada ALE IPv4 podem não ocorrer. Isso é por design, porque para todas as intenções e finalidades, o soquete é um soquete IPv6. Para ver o tráfego V4 para esse soquete, crie filtros na camada V6 usando o endereço mapeado para IPv6.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Camadas ALE](ale-layers.md)
</dt> <dt>

[Filtragem com estado ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfego multicast/difusão ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalização de Flow ALE](ale-flow-customization.md)
</dt> </dl>

 

 