---
title: Sobre o DNS
description: O DNS (Sistema de Nomes de Domínio) é um protocolo padrão do setor usado para localizar computadores em uma rede baseada em IP. Os usuários podem se lembrar de nomes de exibição, como www.microsoft.com endereços baseados em número, como 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Sobre DNS do sistema de nomes de domínio
- DNS do sistema de nomes de domínio, sobre
- DNS do sistema de nomes de domínio, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc286c18aa60a930a243c1500cf4707d0d42874fc9556fcb090df582334f077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084786"
---
# <a name="about-dns"></a>Sobre o DNS

O DNS (Sistema de Nomes de Domínio) é um protocolo padrão do setor usado para localizar computadores em uma rede baseada em IP. Os usuários podem se lembrar de nomes de exibição, como endereços baseados em número, como `www.microsoft.com` 207.46.131.137.

Redes IP, como a Internet e Windows rede, dependem de endereços baseados em número para transmitir dados pela rede; portanto, é necessário converter nomes de exibição (como ) em endereços numéricos que a rede possa reconhecer `www.microsoft.com` (como 207.46.131.137). DNS é o serviço de sua escolha Windows localizar esses recursos e traduzi-los em endereços IP.

O DNS é o serviço de localizador primário para o Active Directory e, portanto, o DNS pode ser considerado um serviço base para o Windows e o Active Directory. Windows fornece funções que permitem que os programadores de aplicativos usem funções DNS, como fazer consultas DNS programaticamente, comparar registros e procurar nomes.

Muitas funções DNS são, na verdade, tipos de função, pois há um nome base para a função, mas seu uso depende da codificação de caracteres. Por exemplo, a função [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) é listada na referência de função da API (Interface de Programação de Aplicativo DNS) como **DnsQuery,** mas seu uso em aplicativos depende se a codificação de caracteres é ANSI (designada acrescentando A ao nome do tipo de função), Unicode (designado acrescentando W ao nome do tipo de função) ou \_ \_ UTF-8 (designado acrescentando UTF ao nome do tipo de \_ função). Portanto, a chamada de função para **a função DnsQuery** seria, na verdade, uma das seguintes:

DnsQuery \_ A ( A para \_ codificação ANSI)

DnsQuery \_ W ( W para \_ codificação Unicode)

DnsQuery \_ UTF8 ( UTF8 para codificação \_ UTF-8)

Todas as funções que exigem essa convenção mostram claramente esse requisito dentro das primeiras frases de sua definição de função. Use o nome da função adequado; por exemplo, você não pode simplesmente chamar [**DnsQuery em**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) vez de DnsQuery \_ A.

 

 




