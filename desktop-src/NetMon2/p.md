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
# <a name="p-network-monitor"></a><span data-ttu-id="629a6-103">P (Monitor de Rede)</span><span class="sxs-lookup"><span data-stu-id="629a6-103">P (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="629a6-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**pacote**</span><span class="sxs-lookup"><span data-stu-id="629a6-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**packet**</span></span>
</dt> <dd>

<span data-ttu-id="629a6-105">Consulte [*quadro*](f.md).</span><span class="sxs-lookup"><span data-stu-id="629a6-105">See [*frame*](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="629a6-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**analisador**</span><span class="sxs-lookup"><span data-stu-id="629a6-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**parser**</span></span>
</dt> <dd>

<span data-ttu-id="629a6-107">Um componente que detecta um protocolo específico em uma captura atrasada.</span><span class="sxs-lookup"><span data-stu-id="629a6-107">A component that detects a specific protocol in a delayed capture.</span></span> <span data-ttu-id="629a6-108">Cada analisador pode detectar um protocolo.</span><span class="sxs-lookup"><span data-stu-id="629a6-108">Each parser can detect one protocol.</span></span> <span data-ttu-id="629a6-109">No entanto, uma DLL do analisador pode conter vários analisadores.</span><span class="sxs-lookup"><span data-stu-id="629a6-109">However, one parser DLL may contain multiple parsers.</span></span> <span data-ttu-id="629a6-110">Também chamado de analisador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="629a6-110">Also called a protocol parser.</span></span>

</dd> <dt>

<span data-ttu-id="629a6-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span><span class="sxs-lookup"><span data-stu-id="629a6-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span></span>
</dt> <dd>

<span data-ttu-id="629a6-112">Um arquivo de inicialização Monitor de Rede que contém uma lista de todos os analisadores instalados.</span><span class="sxs-lookup"><span data-stu-id="629a6-112">A Network Monitor initialization file that contains a list of all the installed parsers.</span></span> <span data-ttu-id="629a6-113">Para cada analisador, há uma cadeia de caracteres de comentário que descreve o analisador, o conjunto de acompanhamento do analisador e qualquer arquivo de ajuda associado ao analisador.</span><span class="sxs-lookup"><span data-stu-id="629a6-113">For each parser there is a comment string that describes the parser, the follow set of the parser, and any Help file associated with the parser.</span></span> <span data-ttu-id="629a6-114">O arquivo INI do analisador é atualizado quando Monitor de Rede chama **ParserAutoInstallInfo** ou quando a DLL do analisador chama **createentregatable**.</span><span class="sxs-lookup"><span data-stu-id="629a6-114">The parser INI file is updated when Network Monitor calls **ParserAutoInstallInfo**, or when the parser DLL calls **CreateHandoffTable**.</span></span>

</dd> <dt>

<span data-ttu-id="629a6-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**</span><span class="sxs-lookup"><span data-stu-id="629a6-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**</span></span>
</dt> <dd>

<span data-ttu-id="629a6-116">Uma ferramenta de software que permite exibir variáveis relacionadas ao desempenho da rede que identificam a atividade de um processo.</span><span class="sxs-lookup"><span data-stu-id="629a6-116">A software tool that allows you to view network performance-related variables that identify the activity of a process.</span></span>

</dd> <dt>

<span data-ttu-id="629a6-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**modo promíscuo**</span><span class="sxs-lookup"><span data-stu-id="629a6-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**promiscuous mode**</span></span>
</dt> <dd>

<span data-ttu-id="629a6-118">Um estado no qual uma placa de adaptador de rede copia todos os quadros que passam pela rede, independentemente do endereço de destino para um buffer local.</span><span class="sxs-lookup"><span data-stu-id="629a6-118">A state in which a network adapter card copies all the frames that pass over the network, regardless of the destination address to a local buffer.</span></span> <span data-ttu-id="629a6-119">Esse modo permite que Monitor de Rede Capture e exiba todo o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="629a6-119">This mode enables Network Monitor to capture and display all network traffic.</span></span>

</dd> <dt>

<span data-ttu-id="629a6-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="629a6-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="629a6-121">Um elemento de protocolo em um analisador que descreve um campo de dados dentro de um quadro que é enviado usando esse protocolo.</span><span class="sxs-lookup"><span data-stu-id="629a6-121">A protocol element in a parser that describes a data field within a frame that is sent by using that protocol.</span></span>

</dd> <dt>

<span data-ttu-id="629a6-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**banco de dados de propriedades**</span><span class="sxs-lookup"><span data-stu-id="629a6-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**property database**</span></span>
</dt> <dd>

<span data-ttu-id="629a6-123">Um banco de dados interno que define todas as propriedades às quais um protocolo específico dá suporte.</span><span class="sxs-lookup"><span data-stu-id="629a6-123">An internal database that defines all the properties that a specific protocol supports.</span></span> <span data-ttu-id="629a6-124">O banco de dados de propriedades contém uma estrutura **PROPERTYINFO** para cada propriedade que o analisador define.</span><span class="sxs-lookup"><span data-stu-id="629a6-124">The property database contains a **PROPERTYINFO** structure for each property that the parser defines.</span></span> <span data-ttu-id="629a6-125">Monitor de Rede usa as informações no banco de dados quando ele anexa uma definição de propriedade a uma instância da propriedade e, ao Formatar o dado de propriedade que é exibido no painel de detalhes da interface do usuário do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="629a6-125">Network Monitor uses the information in the database when it attaches a property definition to an instance of the property, and when it formats the property data that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="629a6-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**nível de protocolo**</span><span class="sxs-lookup"><span data-stu-id="629a6-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**protocol level**</span></span>
</dt> <dd>

<span data-ttu-id="629a6-127">Um agrupamento lógico de propriedades de protocolo.</span><span class="sxs-lookup"><span data-stu-id="629a6-127">A logical grouping of protocol properties.</span></span>

</dd> </dl>

 

 



