---
title: Sistema de nomes de domínio
description: O DNS (sistema de nomes de domínio), um serviço localizador no Microsoft Windows, é um protocolo padrão do setor que localiza computadores em uma rede baseada em IP.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS, (consulte sistema de nome de domínio)
- Sistema de nomes de domínio
- Sistema de nomes de domínio, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104012066"
---
# <a name="domain-name-system"></a>Sistema de nomes de domínio

## <a name="purpose"></a>Finalidade

O DNS (sistema de nomes de domínio), um serviço localizador no Microsoft Windows, é um protocolo padrão do setor que localiza computadores em uma rede baseada em IP. Redes IP, como as redes Internet e Windows, dependem de endereços baseados em número para processar dados. No entanto, os usuários podem lembrar endereços de nomes com mais facilidade, portanto, é necessário converter nomes amigáveis (como `www.microsoft.com` ) em endereços que a rede possa reconhecer (como 207.46.131.137).

## <a name="where-applicable"></a>Quando aplicável

O Windows e o Active Directory usam o DNS. O DNS é o serviço localizador primário para a Internet e Active Directory e, portanto, o DNS é considerado um serviço base para Windows e Active Directory.

## <a name="developer-audience"></a>Público de desenvolvedores

O Windows fornece funções que permitem que os programadores de aplicativos usem o DNS, como consulta de DNS programática, comparação de registros e pesquisa de nomes.

Os componentes de DNS programáveis são projetados para uso por programadores de C/C++. É necessário ter familiaridade com a rede e o DNS. Os programadores devem estar familiarizados com o pacote de protocolo IP, bem como as operações de DNS e o protocolo DNS.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O DNS é usado em todas as redes IP que exigem um serviço de localizador compatível com a Internet. No entanto, a API DNS requer o Windows 2000 ou posterior.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                             | Descrição                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Documentos de padrões de DNS](dns-standards-documents.md)<br/> | Links para documentos de padrões de DNS públicos.<br/>                                  |
| [Sobre o DNS](about-dns.md)<br/>                             | Informações gerais sobre o DNS.<br/>                                            |
| [Referência de DNS](dns-reference.md)<br/>                     | Documentação de referência para DNS.<br/>                                          |
| [Provedor WMI de DNS](dns-wmi-provider.md)<br/>               | Informações gerais e documentação de referência para o provedor WMI de DNS.<br/> |
| [Glossário](glossary-gly.md)<br/>                           | Glossário de termos e definições de DNS.<br/>                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DHCP](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Auxiliar de protocolo de Internet](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

[Serviços de diretório](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)
</dt> </dl>

 

