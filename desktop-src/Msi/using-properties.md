---
description: As seções a seguir descrevem como usar as propriedades internas do instalador e as propriedades adicionais definidas pelo autor do pacote.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Usando propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090476"
---
# <a name="using-properties"></a><span data-ttu-id="986df-103">Usando propriedades</span><span class="sxs-lookup"><span data-stu-id="986df-103">Using Properties</span></span>

<span data-ttu-id="986df-104">As seções a seguir descrevem como usar as propriedades internas do instalador e as propriedades adicionais definidas pelo autor do pacote.</span><span class="sxs-lookup"><span data-stu-id="986df-104">The following sections describe using the built-in installer properties and additional properties defined by the package author.</span></span> <span data-ttu-id="986df-105">As propriedades podem ser propriedades [públicas](public-properties.md) ou [privadas](private-properties.md).</span><span class="sxs-lookup"><span data-stu-id="986df-105">Properties can be either [public properties](public-properties.md) or [private properties](private-properties.md).</span></span> <span data-ttu-id="986df-106">Cada propriedade que precisa ser definida na inicialização do instalador deve ter seu nome e o valor inicial listados na tabela de [Propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="986df-106">Every property that needs to be defined upon initialization of the installer must have its name and initial value listed in the [Property table](property-table.md).</span></span> <span data-ttu-id="986df-107">Propriedades com um valor nulo não estão listadas na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="986df-107">Properties having a Null value are not listed in the Property table.</span></span> <span data-ttu-id="986df-108">Você pode obter ou definir propriedades de programas e ações personalizadas e definir propriedades públicas na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="986df-108">You can get or set properties from programs and custom actions and set public properties from the command line.</span></span> <span data-ttu-id="986df-109">O processo de instalação pode ser modificado usando propriedades em instruções condicionais.</span><span class="sxs-lookup"><span data-stu-id="986df-109">The installation process can be modified by using properties in conditional statements.</span></span>

[<span data-ttu-id="986df-110">Restrições em nomes de propriedade</span><span class="sxs-lookup"><span data-stu-id="986df-110">Restrictions on Property Names</span></span>](restrictions-on-property-names.md)

[<span data-ttu-id="986df-111">Inicialização de valores de propriedade</span><span class="sxs-lookup"><span data-stu-id="986df-111">Initialization of Property Values</span></span>](initialization-of-property-values.md)

[<span data-ttu-id="986df-112">Obtendo e definindo propriedades</span><span class="sxs-lookup"><span data-stu-id="986df-112">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)

[<span data-ttu-id="986df-113">Usando propriedades em instruções condicionais</span><span class="sxs-lookup"><span data-stu-id="986df-113">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)

[<span data-ttu-id="986df-114">Usando uma propriedade de diretório em um caminho</span><span class="sxs-lookup"><span data-stu-id="986df-114">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)

> [!Note]  
> <span data-ttu-id="986df-115">Não use Propriedades para senhas ou outras informações que devam permanecer seguras.</span><span class="sxs-lookup"><span data-stu-id="986df-115">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="986df-116">O instalador pode gravar o valor de uma propriedade criada na tabela de propriedades ou criado em tempo de execução em um log ou no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="986df-116">The installer may write the value of a property authored into the Property table or created at runtime into a log or the system registry.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="986df-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="986df-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="986df-118">Sobre propriedades</span><span class="sxs-lookup"><span data-stu-id="986df-118">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="986df-119">Referência de propriedade</span><span class="sxs-lookup"><span data-stu-id="986df-119">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



