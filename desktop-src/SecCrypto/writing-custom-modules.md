---
description: Você pode escrever módulos de política na linguagem de programação C, C++ ou Visual Basic.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Gravando módulos personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921846"
---
# <a name="writing-custom-modules"></a><span data-ttu-id="f0733-103">Gravando módulos personalizados</span><span class="sxs-lookup"><span data-stu-id="f0733-103">Writing Custom Modules</span></span>

<span data-ttu-id="f0733-104">Você pode escrever módulos de política na linguagem de programação C, C++ ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f0733-104">You can write policy modules in the C, C++, or Visual Basic programming language.</span></span> <span data-ttu-id="f0733-105">O compilador da Microsoft necessário está disponível no Visual C++ versão 5,0 ou posterior ou no Visual Basic versão 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f0733-105">The required Microsoft compiler is available in Visual C++ version 5.0 or later or in Visual Basic version 5.0 or later.</span></span> <span data-ttu-id="f0733-106">Uma AC ( [*autoridade de certificação*](../secgloss/c-gly.md) ) corporativa deve usar apenas o módulo de política corporativa fornecido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f0733-106">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

<span data-ttu-id="f0733-107">Você deve implementar o [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) ao gravar um módulo de política personalizada.</span><span class="sxs-lookup"><span data-stu-id="f0733-107">You must implement [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) when writing a custom policy module.</span></span> <span data-ttu-id="f0733-108">Além disso, você deve implementar o [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) ao gravar um módulo de política personalizada.</span><span class="sxs-lookup"><span data-stu-id="f0733-108">Additionally, you must implement [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) when writing a custom policy module.</span></span>

<span data-ttu-id="f0733-109">Os módulos de política podem chamar métodos de [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) para auxiliar no processamento de uma [*solicitação de certificado*](../secgloss/c-gly.md); **ICertServerPolicy** permite que as propriedades e extensões de certificado sejam definidas e recuperadas.</span><span class="sxs-lookup"><span data-stu-id="f0733-109">Policy modules can call methods from [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) to assist in the processing of a [*certificate request*](../secgloss/c-gly.md); **ICertServerPolicy** allows properties and certificate extensions to be set and retrieved.</span></span>

<span data-ttu-id="f0733-110">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0733-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="f0733-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="f0733-111">Topic</span></span>                                                                      | <span data-ttu-id="f0733-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0733-112">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="f0733-113">Definindo propriedades de certificado</span><span class="sxs-lookup"><span data-stu-id="f0733-113">Setting Certificate Properties</span></span>](setting-certificate-properties.md)       | <span data-ttu-id="f0733-114">Definindo as propriedades de um certificado</span><span class="sxs-lookup"><span data-stu-id="f0733-114">Setting the properties of a certificate</span></span> |
| [<span data-ttu-id="f0733-115">Gravando módulos de saída personalizados</span><span class="sxs-lookup"><span data-stu-id="f0733-115">Writing Custom Exit Modules</span></span>](writing-custom-exit-modules.md)             | <span data-ttu-id="f0733-116">Gravando módulos de saída personalizados</span><span class="sxs-lookup"><span data-stu-id="f0733-116">Writing custom exit modules</span></span>             |
| [<span data-ttu-id="f0733-117">Gravando manipuladores de extensão personalizados</span><span class="sxs-lookup"><span data-stu-id="f0733-117">Writing Custom Extension Handlers</span></span>](writing-custom-extension-handlers.md) | <span data-ttu-id="f0733-118">Gravando manipuladores de extensão personalizados</span><span class="sxs-lookup"><span data-stu-id="f0733-118">Writing custom extension handlers</span></span>       |



 

 

 
