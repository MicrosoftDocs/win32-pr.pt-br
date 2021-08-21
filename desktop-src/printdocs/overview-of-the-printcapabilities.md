---
description: As PrintCapabilities descrevem as configurações ou os Estados disponíveis em um dispositivo, que geralmente podem ser colocados em várias configurações diferentes.
ms.assetid: 094472fc-28ca-4d7a-a8be-cc4623d02ff2
title: Visão geral dos PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2cf4ffb6dca92693abbfe1fd3c7ac7b906c13abf41c02b71efeb1e6607a21a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868441"
---
# <a name="overview-of-the-printcapabilities"></a>Visão geral dos PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

As PrintCapabilities descrevem as configurações ou os Estados disponíveis em um dispositivo. Um dispositivo descrito por PrintCapabilities geralmente pode ser colocado em várias configurações diferentes. No caso de um dispositivo de impressão, os atributos de impressão típicos incluem impressão duplex, resolução e tamanho da mídia. Se o dispositivo der suporte a esses atributos, eles serão parte da configuração desse dispositivo. O usuário seleciona uma configuração específica atribuindo um valor específico a cada um dos atributos disponíveis; por exemplo, duplex: OneSided, resolução: 600 dpi e MediaSize: legal.

Os PrintCapabilities são criados na estrutura de esquema de impressão, que define os elementos que podem ser usados nos PrintCapabilities. As palavras-chave do esquema de impressão definem as hierarquias de elemento usadas com frequência, ou palavras-chave, com a finalidade de promover a portabilidade das informações e a intenção entre clientes individuais. No entanto, as palavras-chave do esquema de impressão também permitem extensões privadas para que as PrintCapabilities possam ser adaptadas para atender a necessidades específicas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



