---
description: Glossário de Monitor de Rede termos que começam com a letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de258a4394ae13ca71a62d90fd9ee9218862ab7845c7300fcfe509a3a286f34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555466"
---
# <a name="p-network-monitor"></a>P (Monitor de Rede)

<dl> <dt>

<span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**Pacote**
</dt> <dd>

Consulte [*quadro*](f.md).

</dd> <dt>

<span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**Analisador**
</dt> <dd>

Um componente que detecta um protocolo específico em uma captura atrasada. Cada analisador pode detectar um protocolo. No entanto, uma DLL do analisador pode conter vários analisadores. Também chamado de analisador de protocolo.

</dd> <dt>

<span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**
</dt> <dd>

Um Monitor de Rede de inicialização que contém uma lista de todos os analisadores instalados. Para cada analisador, há uma cadeia de caracteres de comentário que descreve o analisador, o conjunto a seguir do analisador e qualquer arquivo de Ajuda associado ao analisador. O arquivo INI do analisador é atualizado quando Monitor de Rede **chama ParserAutoInstallInfo** ou quando a DLL do analisador chama **CreateHandoffTable.**

</dd> <dt>

<span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**
</dt> <dd>

Uma ferramenta de software que permite exibir variáveis relacionadas ao desempenho de rede que identificam a atividade de um processo.

</dd> <dt>

<span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**modo promiscuo**
</dt> <dd>

Um estado no qual uma placa de adaptador de rede copia todos os quadros que passam pela rede, independentemente do endereço de destino para um buffer local. Esse modo permite que Monitor de Rede capturar e exibir todo o tráfego de rede.

</dd> <dt>

<span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**Propriedade**
</dt> <dd>

Um elemento de protocolo em um analisador que descreve um campo de dados dentro de um quadro enviado usando esse protocolo.

</dd> <dt>

<span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**banco de dados de propriedade**
</dt> <dd>

Um banco de dados interno que define todas as propriedades às quais um protocolo específico dá suporte. O banco de dados de propriedades **contém uma estrutura PROPERTYINFO** para cada propriedade que o analisador define. Monitor de Rede usa as informações no banco de dados quando anexa uma definição de propriedade a uma instância da propriedade e quando formatar os dados de propriedade exibidos no painel de detalhes da interface do usuário Monitor de Rede.

</dd> <dt>

<span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**nível de protocolo**
</dt> <dd>

Um grupo lógico de propriedades de protocolo.

</dd> </dl>

 

 



