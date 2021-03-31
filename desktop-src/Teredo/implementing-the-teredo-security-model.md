---
title: Implementando o modelo de segurança Teredo
description: O modelo de segurança Teredo é baseado na tecnologia WFP (Windows Filtering Platform) interna do Windows Vista. Como resultado, é recomendável que firewalls de terceiros usem o WFP para impor o modelo de segurança Teredo.
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a39668f8e1c86e0cd5b12056df5eb9a5fd9cd3ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641537"
---
# <a name="implementing-the-teredo-security-model"></a>Implementando o modelo de segurança Teredo

O modelo de segurança Teredo é baseado na tecnologia WFP ( [Windows Filtering Platform](/windows/desktop/FWP/windows-filtering-platform-start-page) ) interna do Windows Vista. Como resultado, é recomendável que firewalls de terceiros usem o WFP para impor o modelo de segurança [Teredo](about-teredo.md) .

A implementação geral do [modelo de segurança Teredo](the-teredo-security-model.md) requer o seguinte:

-   Um firewall de host com capacidade para IPv6 deve ser registrado na WSC (central de segurança do Windows) no computador. Na ausência de um firewall baseado em host, ou da WSC em si, a interface teredo não estará disponível para uso. Esse é o único requisito para receber tráfego solicitado da Internet pela interface teredo.
-   Qualquer aplicativo que recebe tráfego não solicitado da Internet pela interface teredo deve se registrar com um firewall compatível com IPv6, como o [Firewall do Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page), antes de receber o tráfego não solicitado.

Um endereço Teredo se tornará inativo se o tráfego não tiver sido enviado ou recebido pela interface teredo por uma hora e se os aplicativos que atendem aos critérios de segurança necessários para o tráfego não solicitado não estiverem em execução ou não tiverem soquetes de escuta abertos.

Após a reinicialização de um computador, ou se o endereço Teredo perder suas qualificações, o Windows Vista qualificará automaticamente o endereço e o tornará disponível para uso assim que um aplicativo for associado a soquetes compatíveis com IPv6. É importante observar que a opção "travessia da borda" do firewall do Windows definida por um aplicativo para permitir o tráfego não solicitado via Teredo é persistente entre reinicializações.

## <a name="firewall-requirements-for-teredo"></a>Requisitos de firewall para Teredo

Os fornecedores de firewall podem incorporar facilmente o suporte a Teredo em seus produtos e proteger seus usuários usando os recursos da plataforma de filtragem do Windows. Isso pode ser feito registrando o firewall compatível com IPv6 com a central de segurança do Windows, adicionando as regras apropriadas à subcamada do WFP Teredo e usando APIs internas no Windows para enumerar aplicativos que podem ouvir o tráfego não solicitado pelo Teredo. Em situações em que um aplicativo não precisa escutar o tráfego solicitado por Teredo, os firewalls não exigem regras adicionais adicionadas à WFP. No entanto, um registro de firewall compatível com IPv6 com a central de segurança do Windows ainda é um requisito para disponibilizar o endereço Teredo para uso.

Para dar suporte a esse cenário, o firewall deve ser compatível com IPv6 e registrado na central de segurança do Windows. Além disso, o firewall não deve alterar o estado de execução ou de inicialização do serviço da central de segurança do Windows (wscsvc), pois o Teredo depende das informações de estado fornecidas por meio das APIs da WSC.

A API utilizada para registrar um firewall com a WSC pode ser obtida entrando em contato com a Microsoft em wscisv@microsoft.com . Um contrato de confidencialidade (NDA) é necessário para a divulgação dessa API devido a questões de segurança.

A documentação a seguir detalha os filtros e as exceções utilizados para garantir a compatibilidade ideal com o Teredo:

-   [Implementando filtros de firewall para Teredo](implementing-firewall-filters-for-teredo.md)
-   [Exceções de firewall necessárias para Teredo](required-firewall-exceptions-for-teredo.md)
-   [Exceções necessárias da plataforma de filtragem do Windows para Teredo](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>Requisitos de firewall para outras tecnologias de transição IPv6

Para dar suporte a outras tecnologias de transição IPv6 (como 6to4 e ISATAP), o produto de firewall de host deve ser capaz de processar o tráfego IPv6. O protocolo IP 41 indica quando um cabeçalho IPv6 segue um cabeçalho IPv4. Quando um firewall de host encontra o protocolo 41, ele deve reconhecer que o pacote é um pacote encapsulado IPv6 e, como resultado, deve processar o pacote adequadamente e tomar as decisões de aceitação/negação com base nas regras de IPv6 em sua política.

 

 