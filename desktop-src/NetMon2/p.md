---
description: Glossário de Monitor de Rede termos que começam com a letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a95ed739acb6f4a59cf8c7a7edb760547f6469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010593"
---
# <a name="p-network-monitor"></a>P (Monitor de Rede)

<dl> <dt>

<span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**pacote**
</dt> <dd>

Consulte [*quadro*](f.md).

</dd> <dt>

<span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**analisador**
</dt> <dd>

Um componente que detecta um protocolo específico em uma captura atrasada. Cada analisador pode detectar um protocolo. No entanto, uma DLL do analisador pode conter vários analisadores. Também chamado de analisador de protocolo.

</dd> <dt>

<span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**
</dt> <dd>

Um arquivo de inicialização Monitor de Rede que contém uma lista de todos os analisadores instalados. Para cada analisador, há uma cadeia de caracteres de comentário que descreve o analisador, o conjunto de acompanhamento do analisador e qualquer arquivo de ajuda associado ao analisador. O arquivo INI do analisador é atualizado quando Monitor de Rede chama **ParserAutoInstallInfo** ou quando a DLL do analisador chama **createentregatable**.

</dd> <dt>

<span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**
</dt> <dd>

Uma ferramenta de software que permite exibir variáveis relacionadas ao desempenho da rede que identificam a atividade de um processo.

</dd> <dt>

<span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**modo promíscuo**
</dt> <dd>

Um estado no qual uma placa de adaptador de rede copia todos os quadros que passam pela rede, independentemente do endereço de destino para um buffer local. Esse modo permite que Monitor de Rede Capture e exiba todo o tráfego de rede.

</dd> <dt>

<span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**Propriedade**
</dt> <dd>

Um elemento de protocolo em um analisador que descreve um campo de dados dentro de um quadro que é enviado usando esse protocolo.

</dd> <dt>

<span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**banco de dados de propriedades**
</dt> <dd>

Um banco de dados interno que define todas as propriedades às quais um protocolo específico dá suporte. O banco de dados de propriedades contém uma estrutura **PROPERTYINFO** para cada propriedade que o analisador define. Monitor de Rede usa as informações no banco de dados quando ele anexa uma definição de propriedade a uma instância da propriedade e, ao Formatar o dado de propriedade que é exibido no painel de detalhes da interface do usuário do Monitor de Rede.

</dd> <dt>

<span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**nível de protocolo**
</dt> <dd>

Um agrupamento lógico de propriedades de protocolo.

</dd> </dl>

 

 



