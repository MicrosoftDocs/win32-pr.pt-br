---
description: Esses artigos fornecem informações mais detalhadas sobre o significado e o uso dos tipos de elemento de esquema de impressão.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Estrutura de esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570701df700954ad85fb724b9528b7e7912f3174
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407159"
---
# <a name="print-schema-framework"></a><span data-ttu-id="ead26-103">Estrutura de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ead26-103">Print Schema Framework</span></span>

<span data-ttu-id="ead26-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="ead26-104">This topic is not current.</span></span> <span data-ttu-id="ead26-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ead26-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ead26-106">Esta seção fornece informações mais detalhadas sobre o significado e o uso dos tipos de elemento de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="ead26-106">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="ead26-107">O foco principal da versão inicial da estrutura de esquema de impressão é representar as configurações e os recursos dos atributos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ead26-107">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="ead26-108">Em um alto nível, essa estrutura oferece dois estilos diferentes de descrição de um atributo de dispositivo: como um constructo de recurso/opção ou como uma construção de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ead26-108">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="ead26-109">Se um atributo de dispositivo tiver um pequeno número de valores ou Estados disponíveis, o atributo deverá ser caracterizado como um recurso com os valores permitidos ou Estados chamados de elementos de opção.</span><span class="sxs-lookup"><span data-stu-id="ead26-109">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="ead26-110">Por outro lado, se um atributo de dispositivo tiver um grande número de valores ou Estados disponíveis e o conjunto de todos os valores possíveis for facilmente definido sem recorrer à enumeração explícita, o atributo do dispositivo deverá ser caracterizado como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ead26-110">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="ead26-111">(Um parâmetro é definido por meio de um elemento ParameterDef e uma instância de parâmetro é inicializada por meio de um elemento ParameterInit.) Os elementos de propriedade são usados em constructos de recurso/opção e de parâmetro para fornecer um nível mais preciso de diferenciação.</span><span class="sxs-lookup"><span data-stu-id="ead26-111">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ead26-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ead26-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ead26-113">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ead26-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



