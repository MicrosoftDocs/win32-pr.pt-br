---
title: Implementando o modelo de segurança Teredo
description: o modelo de segurança Teredo é baseado na tecnologia WFP (Windows filtering Platform) incorporada ao Windows Vista. Como resultado, é recomendável que firewalls de terceiros usem o WFP para impor o modelo de segurança Teredo.
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cad78b7c1512e0f1c632ecd27d0bb9580ac3796d6d36001a1cd19fb72c7b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001744"
---
# <a name="implementing-the-teredo-security-model"></a>Implementando o modelo de segurança Teredo

o modelo de segurança Teredo é baseado na tecnologia WFP ( [Windows filtering Platform](/windows/desktop/FWP/windows-filtering-platform-start-page) ) incorporada ao Windows Vista. Como resultado, é recomendável que firewalls de terceiros usem o WFP para impor o modelo de segurança [Teredo](about-teredo.md) .

A implementação geral do [modelo de segurança Teredo](the-teredo-security-model.md) requer o seguinte:

-   um firewall de host com capacidade para IPv6 deve ser registrado com o Segurança do Windows Center (WSC) no computador. Na ausência de um firewall baseado em host, ou da WSC em si, a interface teredo não estará disponível para uso. Esse é o único requisito para receber tráfego solicitado da Internet pela interface teredo.
-   qualquer aplicativo que recebe tráfego não solicitado da Internet pela interface Teredo deve se registrar em um firewall compatível com IPv6, como [Windows firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page), antes de receber o tráfego não solicitado.

Um endereço Teredo se tornará inativo se o tráfego não tiver sido enviado ou recebido pela interface teredo por uma hora e se os aplicativos que atendem aos critérios de segurança necessários para o tráfego não solicitado não estiverem em execução ou não tiverem soquetes de escuta abertos.

após a reinicialização de um computador, ou se o endereço Teredo perder suas qualificações, o Windows Vista qualificará automaticamente o endereço e o tornará disponível para uso assim que um aplicativo for associado a soquetes compatíveis com IPv6. é importante observar que a opção "passagem de borda" do Firewall Windows definida por um aplicativo para permitir tráfego não solicitado via Teredo é persistente entre reinicializações.

## <a name="firewall-requirements-for-teredo"></a>Requisitos de firewall para Teredo

os fornecedores de Firewall podem incorporar facilmente o suporte a Teredo em seus produtos e proteger seus usuários usando os recursos da plataforma de filtragem de Windows. isso pode ser feito registrando o firewall com capacidade para IPv6 com o centro de Segurança do Windows, adicionando regras apropriadas à subcamada do WFP Teredo e usando APIs internas no Windows para enumerar aplicativos que podem ouvir o tráfego não solicitado pelo Teredo. Em situações em que um aplicativo não precisa escutar o tráfego solicitado por Teredo, os firewalls não exigem regras adicionais adicionadas à WFP. no entanto, um registro de firewall com capacidade de IPv6 com o Segurança do Windows Center ainda é um requisito para disponibilizar o endereço Teredo para uso.

para dar suporte a esse cenário, o firewall deve ser compatível com IPv6 e registrado com o centro de Segurança do Windows. além disso, o firewall não deve alterar o estado de execução ou inicialização do serviço do Segurança do Windows Center (wscsvc), pois o Teredo depende das informações de estado fornecidas por meio das APIs da WSC.

A API utilizada para registrar um firewall com a WSC pode ser obtida entrando em contato com a Microsoft em wscisv@microsoft.com . Um contrato de confidencialidade (NDA) é necessário para a divulgação dessa API devido a questões de segurança.

A documentação a seguir detalha os filtros e as exceções utilizados para garantir a compatibilidade ideal com o Teredo:

-   [Implementando filtros de firewall para Teredo](implementing-firewall-filters-for-teredo.md)
-   [Exceções de firewall necessárias para Teredo](required-firewall-exceptions-for-teredo.md)
-   [Windows necessárias exceções da plataforma de filtragem para Teredo](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>Requisitos de firewall para outras tecnologias de transição IPv6

para dar suporte a outras tecnologias de transição IPv6 (como 6to4 e ISATAP), o produto de firewall de host deve ser capaz de processar o tráfego IPv6. O protocolo IP 41 indica quando um cabeçalho IPv6 segue um cabeçalho IPv4. Quando um firewall de host encontra o protocolo 41, ele deve reconhecer que o pacote é um pacote encapsulado IPv6 e, como resultado, deve processar o pacote adequadamente e tomar as decisões de aceitação/negação com base nas regras de IPv6 em sua política.

 

 