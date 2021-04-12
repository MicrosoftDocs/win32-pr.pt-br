---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Estrutura de esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617f747b950676f2359645684c9e672fb5c87ee3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172530"
---
# <a name="print-schema-framework"></a><span data-ttu-id="1f480-104">Estrutura de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="1f480-104">Print Schema Framework</span></span>

<span data-ttu-id="1f480-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="1f480-105">This topic is not current.</span></span> <span data-ttu-id="1f480-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1f480-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1f480-107">Esta seção fornece informações mais detalhadas sobre o significado e o uso dos tipos de elemento de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="1f480-107">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="1f480-108">O foco principal da versão inicial da estrutura de esquema de impressão é representar as configurações e os recursos dos atributos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f480-108">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="1f480-109">Em um alto nível, essa estrutura oferece dois estilos diferentes de descrição de um atributo de dispositivo: como um constructo de recurso/opção ou como uma construção de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1f480-109">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="1f480-110">Se um atributo de dispositivo tiver um pequeno número de valores ou Estados disponíveis, o atributo deverá ser caracterizado como um recurso com os valores permitidos ou Estados chamados de elementos de opção.</span><span class="sxs-lookup"><span data-stu-id="1f480-110">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="1f480-111">Por outro lado, se um atributo de dispositivo tiver um grande número de valores ou Estados disponíveis e o conjunto de todos os valores possíveis for facilmente definido sem recorrer à enumeração explícita, o atributo do dispositivo deverá ser caracterizado como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1f480-111">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="1f480-112">(Um parâmetro é definido por meio de um elemento ParameterDef e uma instância de parâmetro é inicializada por meio de um elemento ParameterInit.) Os elementos de propriedade são usados em constructos de recurso/opção e de parâmetro para fornecer um nível mais preciso de diferenciação.</span><span class="sxs-lookup"><span data-stu-id="1f480-112">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f480-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f480-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f480-114">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="1f480-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



