---
title: Sobre o DNS
description: O DNS (sistema de nomes de domínio) é um protocolo padrão do setor usado para localizar computadores em uma rede baseada em IP. Os usuários podem lembrar nomes de exibição, como www.microsoft.com mais fáceis do que endereços baseados em número, como 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Sobre DNS do sistema de nome de domínio
- DNS do sistema de nome de domínio, sobre
- DNS do sistema de nomes de domínio, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104172894"
---
# <a name="about-dns"></a>Sobre o DNS

O DNS (sistema de nomes de domínio) é um protocolo padrão do setor usado para localizar computadores em uma rede baseada em IP. Os usuários podem lembrar nomes de exibição, como `www.microsoft.com` mais fáceis do que endereços baseados em número, como 207.46.131.137.

Redes IP, como redes Internet e Windows, dependem de endereços baseados em número para transmitir dados em toda a rede; Portanto, é necessário converter nomes de exibição (como `www.microsoft.com` ) em endereços numéricos que a rede possa reconhecer (como 207.46.131.137). O DNS é o serviço de escolha no Windows para localizar esses recursos e convertê-los em endereços IP.

O DNS é o serviço localizador primário para Active Directory e, portanto, o DNS pode ser considerado um serviço base para Windows e Active Directory. O Windows fornece funções que permitem que os programadores de aplicativos usem funções DNS, como fazer consultas de DNS programaticamente, comparar registros e pesquisar nomes.

Muitas funções DNS são realmente tipos de função, pois há um nome de base para a função, mas seu uso depende da codificação de caracteres. Por exemplo, a função [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) está listada na referência de função da API (interface de programação de aplicativo) do DNS como **DnsQuery**, mas seu uso em aplicativos depende de a codificação de caracteres ser ANSI (designada ao acrescentar \_ um ao nome do tipo de função), Unicode (designado por acrescentar \_ W ao nome do tipo de função) ou UTF-8 (designado acrescentando \_ UTF ao nome do tipo de função). Portanto, a chamada de função para a função **DnsQuery** seria, na verdade, um dos seguintes:

DnsQuery \_ a ( \_ a para codificação ANSI)

DnsQuery \_ w ( \_ w para codificação Unicode)

DnsQuery \_ UTF8 ( \_ UTF8 para codificação UTF-8)

Todas as funções que exigem essa Convenção declaram claramente esse requisito nas primeiras frases de sua definição de função. Usar o nome de função apropriado; por exemplo, você não pode simplesmente chamar [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) em vez de DnsQuery \_ A.

 

 




