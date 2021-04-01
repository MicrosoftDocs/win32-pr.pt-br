---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usos dos PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dda5b21d1472ec8d4162c8d7229ff47264fb55
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930245"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="385e4-104">Usos dos PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="385e4-104">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="385e4-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="385e4-105">This topic is not current.</span></span> <span data-ttu-id="385e4-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="385e4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="385e4-107">As PrintCapabilities são destinadas a representar atributos de dispositivo configuráveis como construções de recurso/opção ou construções de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="385e4-107">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="385e4-108">Essas informações definem o espaço de configuração do dispositivo e podem ser usadas por um cliente de interface do usuário (IU) para construir uma IU.</span><span class="sxs-lookup"><span data-stu-id="385e4-108">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="385e4-109">As palavras-chave do esquema de impressão definem um conjunto de instâncias de recursos padrão, instâncias de opção para as instâncias de recurso padrão e instâncias de ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="385e4-109">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="385e4-110">As construções de recurso/opção ou parâmetro nos recursos de PrintCapabilities destinam-se a manter as instâncias de propriedade ou ScoredProperty que descrevem um dispositivo e que têm suporte no subsistema do spooler.</span><span class="sxs-lookup"><span data-stu-id="385e4-110">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="385e4-111">Essas instâncias de propriedade e ScoredProperty são de interesse geral para clientes do dispositivo e contêm as informações fornecidas pelas funções do DevCaps do Win32.</span><span class="sxs-lookup"><span data-stu-id="385e4-111">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="385e4-112">As palavras-chave do esquema de impressão definem um conjunto de propriedades padrão e instâncias de ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="385e4-112">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="385e4-113">Deve-se enfatizar que o documento de PrintCapabilities tem como objetivo representar apenas dados de valor único: dados que não dependem de uma configuração específica do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="385e4-113">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="385e4-114">O documento PrintCapabilities fornece apenas um instantâneo dos dados dependentes de configuração.</span><span class="sxs-lookup"><span data-stu-id="385e4-114">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="385e4-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="385e4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="385e4-116">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="385e4-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



