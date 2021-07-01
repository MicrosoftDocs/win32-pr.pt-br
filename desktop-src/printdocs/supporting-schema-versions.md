---
description: Saiba como dar suporte a diferentes versões da estrutura de esquema de impressão. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Suporte a versões de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eac627d3dd711bc952d881efd393720af128e7f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120591"
---
# <a name="supporting-schema-versions"></a><span data-ttu-id="dc37a-105">Suporte a versões de esquema</span><span class="sxs-lookup"><span data-stu-id="dc37a-105">Supporting Schema Versions</span></span>

<span data-ttu-id="dc37a-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="dc37a-106">This topic is not current.</span></span> <span data-ttu-id="dc37a-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dc37a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dc37a-108">A estrutura do esquema de impressão está sujeita a alterações no futuro conforme surgem as novas necessidades.</span><span class="sxs-lookup"><span data-stu-id="dc37a-108">The Print Schema Framework is subject to change in the future as new needs arise.</span></span> <span data-ttu-id="dc37a-109">Essas alterações devem ser muito frequentes, pois a alteração mais comum é a introdução de novos nomes de instância.</span><span class="sxs-lookup"><span data-stu-id="dc37a-109">Such changes are expected to be very infrequent, because the most common change is the introduction of new instance names.</span></span> <span data-ttu-id="dc37a-110">Essa alteração não afeta a estrutura da estrutura e deve ser transparente para clientes e provedores.</span><span class="sxs-lookup"><span data-stu-id="dc37a-110">This change does not affect the structure of the Framework, and should be transparent to clients and providers.</span></span> <span data-ttu-id="dc37a-111">Quaisquer alterações na estrutura e na organização da estrutura de esquema de impressão serão identificadas por incrementos para seu número de versão.</span><span class="sxs-lookup"><span data-stu-id="dc37a-111">Any changes to the structure and organization of the Print Schema Framework will be identified by increments to its version number.</span></span> <span data-ttu-id="dc37a-112">As inclusões nas palavras-chave do esquema de impressão não serão identificadas.</span><span class="sxs-lookup"><span data-stu-id="dc37a-112">Additions to the Print Schema Keywords will not be identified.</span></span> <span data-ttu-id="dc37a-113">Os provedores PrintTicket devem ser capazes de dar suporte à versão atual da estrutura de esquema de impressão, bem como a qualquer versão anterior.</span><span class="sxs-lookup"><span data-stu-id="dc37a-113">PrintTicket providers must be capable of supporting the current Print Schema Framework version, as well as any prior version.</span></span> <span data-ttu-id="dc37a-114">A versão da estrutura de esquema de impressão é identificada usando o atributo XML: versão que aparece no elemento raiz do PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="dc37a-114">The Print Schema Framework version is identified using the XML Attribute: Version that appears at the root element of the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc37a-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc37a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc37a-116">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="dc37a-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



