---
description: As PrintCapabilities descrevem as configurações ou os Estados disponíveis em um dispositivo, que geralmente podem ser colocados em várias configurações diferentes.
ms.assetid: 094472fc-28ca-4d7a-a8be-cc4623d02ff2
title: Visão geral dos PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8f61d1ee4125a9a1ac5f9ddb07cf226cd7094e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408519"
---
# <a name="overview-of-the-printcapabilities"></a><span data-ttu-id="a78ad-103">Visão geral dos PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="a78ad-103">Overview of the PrintCapabilities</span></span>

<span data-ttu-id="a78ad-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a78ad-104">This topic is not current.</span></span> <span data-ttu-id="a78ad-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a78ad-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a78ad-106">As PrintCapabilities descrevem as configurações ou os Estados disponíveis em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a78ad-106">The PrintCapabilities describe the configurations or states available on a device.</span></span> <span data-ttu-id="a78ad-107">Um dispositivo descrito por PrintCapabilities geralmente pode ser colocado em várias configurações diferentes.</span><span class="sxs-lookup"><span data-stu-id="a78ad-107">A device that is described by PrintCapabilities can often be placed in a number of different configurations.</span></span> <span data-ttu-id="a78ad-108">No caso de um dispositivo de impressão, os atributos de impressão típicos incluem impressão duplex, resolução e tamanho da mídia.</span><span class="sxs-lookup"><span data-stu-id="a78ad-108">In the case of a printing device, typical printing attributes include duplex printing, resolution, and media size.</span></span> <span data-ttu-id="a78ad-109">Se o dispositivo der suporte a esses atributos, eles serão parte da configuração desse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a78ad-109">If the device supports these attributes, they are part of the configuration for that device.</span></span> <span data-ttu-id="a78ad-110">O usuário seleciona uma configuração específica atribuindo um valor específico a cada um dos atributos disponíveis; por exemplo, duplex: OneSided, resolução: 600 dpi e MediaSize: legal.</span><span class="sxs-lookup"><span data-stu-id="a78ad-110">The user selects a particular configuration by assigning a specific value to each of the available attributes; for example, Duplex: OneSided, Resolution: 600 dpi, and MediaSize: Legal.</span></span>

<span data-ttu-id="a78ad-111">Os PrintCapabilities são criados na estrutura de esquema de impressão, que define os elementos que podem ser usados nos PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a78ad-111">The PrintCapabilities are built on the Print Schema Framework, which defines the elements that can be used in the PrintCapabilities.</span></span> <span data-ttu-id="a78ad-112">As palavras-chave do esquema de impressão definem as hierarquias de elemento usadas com frequência, ou palavras-chave, com a finalidade de promover a portabilidade das informações e a intenção entre clientes individuais.</span><span class="sxs-lookup"><span data-stu-id="a78ad-112">The Print Schema Keywords define commonly-used element hierarchies, or keywords, for the purpose of promoting portability of the information and intent between individual clients.</span></span> <span data-ttu-id="a78ad-113">No entanto, as palavras-chave do esquema de impressão também permitem extensões privadas para que as PrintCapabilities possam ser adaptadas para atender a necessidades específicas.</span><span class="sxs-lookup"><span data-stu-id="a78ad-113">However, the Print Schema Keywords also allow private extensions so that PrintCapabilities can be tailored to meet specific needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a78ad-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a78ad-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a78ad-115">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a78ad-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



