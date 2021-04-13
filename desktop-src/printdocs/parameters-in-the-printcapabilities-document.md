---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parâmetros no documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298015"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="25ab2-104">Parâmetros no documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="25ab2-104">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="25ab2-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="25ab2-105">This topic is not current.</span></span> <span data-ttu-id="25ab2-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="25ab2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="25ab2-107">Como discutido em [elementos de referência de parâmetro](parameter-reference-elements.md), elementos ParameterInit podem ser referenciados de dentro de instâncias de opção, mas a construção de parâmetro também tem um uso que é independente desse tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="25ab2-107">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="25ab2-108">Um exemplo de um atributo de configuração de dispositivo que é adequado para a representação de parâmetro é CopyCount.</span><span class="sxs-lookup"><span data-stu-id="25ab2-108">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="25ab2-109">Os valores permitidos para esse atributo de configuração de dispositivo podem ser facilmente e concisamente definidos sem listar cada um deles explicitamente.</span><span class="sxs-lookup"><span data-stu-id="25ab2-109">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="25ab2-110">Embora seja possível, embora entediante, listar cada valor de CopyCount em sua própria opção, alguns atributos de configuração de dispositivo simplesmente não podem ser representados usando uma construção de recurso/opção.</span><span class="sxs-lookup"><span data-stu-id="25ab2-110">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="25ab2-111">Como exemplo, considere um dispositivo que aceita uma cadeia de caracteres de texto que é usada para produzir uma marca d' água virtual em cada página de saída.</span><span class="sxs-lookup"><span data-stu-id="25ab2-111">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="25ab2-112">O conjunto de todas as cadeias de caracteres de texto possíveis não pode ser facilmente enumerado explicitamente, mas a cadeia de caracteres de texto pode ser facilmente descrita usando um elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="25ab2-112">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="25ab2-113">O documento de palavras-chave do esquema de impressão define uma série de construções de parâmetro usadas com frequência, mas os provedores de PrintCapabilities são livres para definir as próprias próprias.</span><span class="sxs-lookup"><span data-stu-id="25ab2-113">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="25ab2-114">No entanto, essas construções de parâmetro definidas de forma privada não são portáveis para outros dispositivos, devido ao fato de que um documento de PrintCapabilities fornecido por outra parte não define tal constructo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="25ab2-114">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="25ab2-115">Independentemente da definição de esquema ou definida de modo privado, a instância ParameterDef deve estar presente no documento PrintCapabilities antes que o parâmetro seja reconhecido e usado pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="25ab2-115">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="25ab2-116">Esses parâmetros são chamados de *parâmetros designados*.</span><span class="sxs-lookup"><span data-stu-id="25ab2-116">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25ab2-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25ab2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25ab2-118">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="25ab2-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



