---
description: Windows Installer pode configurar a instalação do software usando os valores das variáveis definidas em um pacote de instalação ou pelo usuário.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Sobre propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169222"
---
# <a name="about-properties"></a><span data-ttu-id="842c8-103">Sobre propriedades</span><span class="sxs-lookup"><span data-stu-id="842c8-103">About Properties</span></span>

<span data-ttu-id="842c8-104">Windows Installer pode configurar a instalação do software usando os valores das variáveis definidas em um pacote de instalação ou pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="842c8-104">Windows Installer can configure software installation by using the values of variables defined in an installation package or by the user.</span></span>

<span data-ttu-id="842c8-105">Windows Installer usa três categorias de variáveis globais durante uma instalação:</span><span class="sxs-lookup"><span data-stu-id="842c8-105">Windows Installer uses three categories of global variables during an installation:</span></span>

-   <span data-ttu-id="842c8-106">Propriedades particulares: o instalador usa propriedades privadas internamente e seus valores devem ser criados no banco de dados de instalação ou definidos para valores determinados pelo ambiente operacional.</span><span class="sxs-lookup"><span data-stu-id="842c8-106">Private properties: The installer uses private properties internally and their values must be authored into the installation database or set to values determined by the operating environment.</span></span>
-   <span data-ttu-id="842c8-107">Propriedades públicas: as propriedades públicas podem ser criadas no banco de dados e alteradas por um usuário ou administrador do sistema na linha de comando, aplicando uma transformação ou interagindo com uma interface do usuário criada.</span><span class="sxs-lookup"><span data-stu-id="842c8-107">Public properties: Public properties can be authored into the database and changed by a user or system administrator on the command line, by applying a transform, or by interacting with an authored user interface.</span></span>
-   <span data-ttu-id="842c8-108">Propriedades públicas restritas: para fins de segurança, o autor de um pacote de instalação pode restringir as propriedades públicas que um usuário pode alterar.</span><span class="sxs-lookup"><span data-stu-id="842c8-108">Restricted public properties: For security purposes, the author of an installation package can restrict the public properties a user can change.</span></span>

<span data-ttu-id="842c8-109">Nem todas as propriedades precisam ser definidas em todos os pacotes, há um pequeno conjunto de propriedades necessárias que devem ser definidas em todos os pacotes.</span><span class="sxs-lookup"><span data-stu-id="842c8-109">Not all properties need to be defined in every package, there is a small set of required properties that must be defined in every package.</span></span> <span data-ttu-id="842c8-110">O instalador define os valores das propriedades em uma determinada ordem de precedência.</span><span class="sxs-lookup"><span data-stu-id="842c8-110">The installer sets the values of properties in a particular order of precedence.</span></span>

[<span data-ttu-id="842c8-111">Propriedades particulares</span><span class="sxs-lookup"><span data-stu-id="842c8-111">Private Properties</span></span>](private-properties.md)

[<span data-ttu-id="842c8-112">Propriedades públicas</span><span class="sxs-lookup"><span data-stu-id="842c8-112">Public Properties</span></span>](public-properties.md)

[<span data-ttu-id="842c8-113">Propriedades públicas restritas</span><span class="sxs-lookup"><span data-stu-id="842c8-113">Restricted Public Properties</span></span>](restricted-public-properties.md)

[<span data-ttu-id="842c8-114">Propriedades obrigatórias</span><span class="sxs-lookup"><span data-stu-id="842c8-114">Required Properties</span></span>](required-properties.md)

[<span data-ttu-id="842c8-115">Ordem de precedência de propriedade</span><span class="sxs-lookup"><span data-stu-id="842c8-115">Order of Property Precedence</span></span>](order-of-property-precedence.md)

## <a name="related-topics"></a><span data-ttu-id="842c8-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="842c8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="842c8-117">Usando propriedades</span><span class="sxs-lookup"><span data-stu-id="842c8-117">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="842c8-118">Referência de propriedade</span><span class="sxs-lookup"><span data-stu-id="842c8-118">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



