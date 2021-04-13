---
title: Visão geral do tutorial ADSI com Visual Basic
description: Active Directory é um banco de dados de finalidade especial \ 8212; Não é uma substituição do registro.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104554062"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a><span data-ttu-id="5ca8e-103">Visão geral do tutorial: ADSI com Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5ca8e-103">Tutorial Overview: ADSI with Visual Basic</span></span>

> [!Note]  
> <span data-ttu-id="5ca8e-104">A documentação a seguir faz parte de uma descrição de cenário estendido para desenvolvedores de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-104">The following documentation is part of an extended scenario description for Visual Basic developers.</span></span> <span data-ttu-id="5ca8e-105">Se você estiver procurando uma visão geral do Active Directory, consulte os [documentos profissionais de ti no TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="5ca8e-105">If you are looking for a general overview of Active Directory, see the [IT Pro docs on Technet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span></span> <span data-ttu-id="5ca8e-106">Para obter uma visão mais detalhada do lado de desenvolvimento do Active Directory, consulte [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="5ca8e-106">For a more in-depth look at the development side of Active Directory, see [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span></span> <span data-ttu-id="5ca8e-107">Para obter uma introdução maior ao Active Directory interfaces de serviço, consulte o tópico pai deste tópico: [Active Directory interfaces de serviço](active-directory-service-interfaces-adsi.md), bem como o tópico irmão: [sobre Active Directory interfaces de serviço](about-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="5ca8e-107">For a larger introduction to Active Directory Service Interfaces, see this topic's parent topic: [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md), as well as the sibling topic: [About Active Directory Service Interfaces](about-adsi.md).</span></span>

 

<span data-ttu-id="5ca8e-108">Active Directory é um banco de dados de finalidade especial — não é uma substituição do registro.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-108">Active Directory is a special-purpose database — it is not a registry replacement.</span></span> <span data-ttu-id="5ca8e-109">O diretório foi projetado para lidar com um grande número de operações de leitura e pesquisa e um número significativamente menor de alterações e atualizações.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-109">The directory is designed to handle a large number of read and search operations and a significantly smaller number of changes and updates.</span></span> <span data-ttu-id="5ca8e-110">Active Directory dados são hierárquicos, replicados e extensíveis.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-110">Active Directory data is hierarchical, replicated, and extensible.</span></span> <span data-ttu-id="5ca8e-111">Como ele é replicado, você não deseja armazenar dados dinâmicos, como preços de estoque corporativos ou desempenho da CPU.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-111">Because it is replicated, you do not want to store dynamic data, such as corporate stock prices or CPU performance.</span></span> <span data-ttu-id="5ca8e-112">Se os dados forem específicos do computador, armazene os dados no registro.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-112">If your data is machine-specific, store the data in the registry.</span></span> <span data-ttu-id="5ca8e-113">Exemplos típicos de dados armazenados no diretório incluem dados de fila da impressora, dados de contato do usuário e dados de configuração de rede/computador.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-113">Typical examples of data stored in the directory include printer queue data, user contact data, and network/computer configuration data.</span></span> <span data-ttu-id="5ca8e-114">O banco de dados Active Directory consiste em objetos e atributos.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-114">The Active Directory database consists of objects and attributes.</span></span> <span data-ttu-id="5ca8e-115">Os objetos e as definições de atributo são armazenados no esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-115">Objects and attribute definitions are stored in the Active Directory schema.</span></span>

<span data-ttu-id="5ca8e-116">Você pode estar se perguntando quais objetos estão armazenados atualmente no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-116">You may be wondering what objects are currently stored in Active Directory.</span></span> <span data-ttu-id="5ca8e-117">Active Directory tem três partições.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-117">Active Directory has three partitions.</span></span> <span data-ttu-id="5ca8e-118">Eles também são conhecidos como contextos de nomenclatura: domínio, esquema e configuração.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-118">These are also known as naming contexts: domain, schema, and configuration.</span></span> <span data-ttu-id="5ca8e-119">A partição de domínio contém usuários, grupos, contatos, computadores, unidades organizacionais e muitos outros tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-119">The domain partition contains users, groups, contacts, computers, organizational units, and many other object types.</span></span> <span data-ttu-id="5ca8e-120">Como Active Directory é extensível, você também pode adicionar suas próprias classes e/ou atributos.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-120">Because Active Directory is extensible, you can also add your own classes and/or attributes.</span></span> <span data-ttu-id="5ca8e-121">A partição de esquema contém classes e definições de atributo.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-121">The schema partition contains classes and attribute definitions.</span></span> <span data-ttu-id="5ca8e-122">A partição de configuração inclui dados de configuração para serviços, partições e sites.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-122">The configuration partition includes configuration data for services, partitions, and sites.</span></span>

<span data-ttu-id="5ca8e-123">A captura de tela a seguir mostra a Active Directory partição de domínio.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-123">The following screen shot shows the Active Directory domain partition.</span></span>

![partição de domínio do Active Directory](images/adadsi1.png)

## <a name="related-topics"></a><span data-ttu-id="5ca8e-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ca8e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ca8e-126">Acessando Active Directory usando Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5ca8e-126">Accessing Active Directory Using Visual Basic</span></span>](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[<span data-ttu-id="5ca8e-127">Cenário: a Fabrikam Corporation</span><span class="sxs-lookup"><span data-stu-id="5ca8e-127">Scenario: The Fabrikam Corporation</span></span>](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[<span data-ttu-id="5ca8e-128">Tópicos avançados</span><span class="sxs-lookup"><span data-stu-id="5ca8e-128">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 