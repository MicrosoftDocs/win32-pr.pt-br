---
description: Entenda os parâmetros no documento PrintCapabilities. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parâmetros no documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6b2ba61f1985fdcd02f40e8e08100725968a8e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118621"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="e6d7a-105">Parâmetros no documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="e6d7a-105">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="e6d7a-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-106">This topic is not current.</span></span> <span data-ttu-id="e6d7a-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e6d7a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e6d7a-108">Conforme discutido em Elementos de Referência de Parâmetro [,](parameter-reference-elements.md)os elementos ParameterInit podem ser referenciados de dentro de instâncias option, mas o constructo de parâmetro também tem um uso que é independente desse tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-108">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="e6d7a-109">Um exemplo de um atributo de configuração de dispositivo que é adequado para a representação de parâmetro é CopyCount.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-109">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="e6d7a-110">Os valores permitidos para esse atributo de configuração de dispositivo podem ser definidos de forma fácil e concisa sem listar cada um deles explicitamente.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-110">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="e6d7a-111">Embora seja possível, embora entediante, listar cada valor copyCount em sua própria Opção, alguns atributos de configuração de dispositivo simplesmente não podem ser representados usando um constructo Recurso/Opção.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-111">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="e6d7a-112">Por exemplo, considere um dispositivo que aceita uma cadeia de caracteres de texto que é usada para produzir uma marca-d'água virtual em cada página de saída.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-112">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="e6d7a-113">O conjunto de todas as cadeias de caracteres de texto possíveis não pode ser enumerado explicitamente com facilidade, mas a cadeia de caracteres de texto pode ser facilmente descrita usando um elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-113">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="e6d7a-114">O documento Palavras-chave de esquema de impressão define uma série de constructos de parâmetros comumente usados, mas os provedores PrintCapabilities são livres para definir outros próprios.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-114">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="e6d7a-115">No entanto, esses constructos de parâmetro definidos de forma privada não são portáteis para outros dispositivos, devido ao fato de que um documento PrintCapabilities fornecido por outra parte não define esse constructo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-115">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="e6d7a-116">Se definido pelo esquema ou definido de forma privada, a instância parameterDef deve estar presente no documento PrintCapabilities antes que o parâmetro seja reconhecido e usado pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="e6d7a-116">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="e6d7a-117">Esses parâmetros são chamados de *parâmetros designados.*</span><span class="sxs-lookup"><span data-stu-id="e6d7a-117">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6d7a-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6d7a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6d7a-119">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="e6d7a-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



