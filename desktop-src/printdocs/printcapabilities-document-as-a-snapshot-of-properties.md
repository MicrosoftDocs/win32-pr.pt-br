---
title: Documento como um instantâneo das propriedades
description: Examine o documento PrintCapabilities como um instantâneo das propriedades. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118641"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="564af-105">Documento de PrintCapabilities como um instantâneo das propriedades</span><span class="sxs-lookup"><span data-stu-id="564af-105">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="564af-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="564af-106">This topic is not current.</span></span> <span data-ttu-id="564af-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="564af-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="564af-108">O dispositivo descrito pelos PrintCapabilities pode ter propriedades que dependem do Estado ou da configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="564af-108">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="564af-109">Embora os PrintCapabilities representem o espaço completo de configuração de um dispositivo, o provedor de PrintCapabilities produz uma instância dependente de configuração dos recursos de PrintCapabilities chamados de documentos de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="564af-109">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="564af-110">Este documento de PrintCapabilities dependente de configuração evita sobrecarregar o esquema de PrintCapabilities com a complexidade de representar dados de valores.</span><span class="sxs-lookup"><span data-stu-id="564af-110">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="564af-111">Mais importante, para aliviar um consumidor do documento PrintCapabilities da carga de extrair o valor apropriado de uma representação de dados com valores múltiplos, todas as instâncias de propriedade e ScoredProperty em um documento de PrintCapabilities devem ser de valor único.</span><span class="sxs-lookup"><span data-stu-id="564af-111">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="564af-112">Em outras palavras, cada instância de propriedade e ScoredProperty em um documento de PrintCapabilities deve ter um valor fixo, em relação à configuração de entrada.</span><span class="sxs-lookup"><span data-stu-id="564af-112">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="564af-113">Cada documento de PrintCapabilities pode ser considerado um instantâneo das propriedades do dispositivo quando o dispositivo está em um estado específico.</span><span class="sxs-lookup"><span data-stu-id="564af-113">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="564af-114">Consequentemente, antes que um documento de PrintCapabilities possa ser construído, a configuração a ser usada deve ser fornecida.</span><span class="sxs-lookup"><span data-stu-id="564af-114">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="564af-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="564af-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="564af-116">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="564af-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



