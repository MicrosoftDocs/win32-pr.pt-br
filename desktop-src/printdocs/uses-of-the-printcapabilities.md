---
description: Saiba mais sobre os usos de PrintCapabilities. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usos de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119421"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="56532-105">Usos de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="56532-105">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="56532-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="56532-106">This topic is not current.</span></span> <span data-ttu-id="56532-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="56532-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56532-108">As PrintCapabilities destinam-se a representar atributos de dispositivo configuráveis como constructos de recurso/opção ou constructos de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="56532-108">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="56532-109">Essas informações definem o espaço de configuração do dispositivo e podem ser usadas por um cliente de interface do usuário para construir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="56532-109">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="56532-110">As Palavras-chave de esquema de impressão definem um conjunto de instâncias de recurso padrão, instâncias option para as instâncias de Recurso padrão e instâncias ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="56532-110">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="56532-111">Os constructos de recurso/opção ou parâmetro em PrintCapabilities destinam-se a manter instâncias property ou ScoredProperty que descrevem um dispositivo e que têm suporte pelo subsistema spooler.</span><span class="sxs-lookup"><span data-stu-id="56532-111">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="56532-112">Essas instâncias Property e ScoredProperty são de interesse geral para os clientes do dispositivo e contêm as informações fornecidas pelas funções Win32 DevCaps.</span><span class="sxs-lookup"><span data-stu-id="56532-112">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="56532-113">As Palavras-chave de esquema de impressão definem um conjunto de instâncias Padrão de Propriedade e ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="56532-113">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="56532-114">É necessário enfatizar que o documento PrintCapabilities destina-se a representar apenas dados com valor único: dados que não dependem de uma configuração específica do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56532-114">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="56532-115">O documento PrintCapabilities fornece apenas um instantâneo de dados dependentes de configuração.</span><span class="sxs-lookup"><span data-stu-id="56532-115">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56532-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="56532-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56532-117">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="56532-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



