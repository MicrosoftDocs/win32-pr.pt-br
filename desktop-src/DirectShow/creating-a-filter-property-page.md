---
description: Criando uma página de propriedades de filtro
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Criando uma página de propriedades de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105751099"
---
# <a name="creating-a-filter-property-page"></a><span data-ttu-id="88e3d-103">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="88e3d-103">Creating a Filter Property Page</span></span>

<span data-ttu-id="88e3d-104">Esta seção descreve como criar uma página de propriedades para um filtro do DirectShow personalizado, usando a classe [**CBasePropertyPage**](cbasepropertypage.md) .</span><span class="sxs-lookup"><span data-stu-id="88e3d-104">This section describes how to create a property page for a custom DirectShow filter, using the [**CBasePropertyPage**](cbasepropertypage.md) class.</span></span> <span data-ttu-id="88e3d-105">O código de exemplo nesta seção mostra todas as etapas necessárias para criar uma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="88e3d-105">The example code in this section shows all the steps needed to create a property page.</span></span> <span data-ttu-id="88e3d-106">O exemplo mostra uma página de propriedades para um filtro de efeito de vídeo hipotético que dá suporte a uma propriedade de saturação.</span><span class="sxs-lookup"><span data-stu-id="88e3d-106">The example shows a property page for a hypothetical video effect filter that supports a saturation property.</span></span> <span data-ttu-id="88e3d-107">A página de propriedades tem um controle deslizante, que o usuário pode mover para ajustar o nível de saturação do filtro.</span><span class="sxs-lookup"><span data-stu-id="88e3d-107">The property page has a slider, which the user can move to adjust the filter's saturation level.</span></span>

<span data-ttu-id="88e3d-108">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="88e3d-108">This section contains the following topics:</span></span>

-   [<span data-ttu-id="88e3d-109">Etapa 1. Definir um mecanismo para definir a propriedade</span><span class="sxs-lookup"><span data-stu-id="88e3d-109">Step 1. Define a Mechanism for Setting the Property</span></span>](step-1--define-a-mechanism-for-setting-the-property.md)
-   [<span data-ttu-id="88e3d-110">Etapa 2. Implementar ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="88e3d-110">Step 2. Implement ISpecifyPropertyPages</span></span>](step-2--implement-ispecifypropertypages.md)
-   [<span data-ttu-id="88e3d-111">Etapa 3. Suporte a QueryInterface</span><span class="sxs-lookup"><span data-stu-id="88e3d-111">Step 3. Support QueryInterface</span></span>](step-3--support-queryinterface.md)
-   [<span data-ttu-id="88e3d-112">Etapa 4. Criar a página de propriedades</span><span class="sxs-lookup"><span data-stu-id="88e3d-112">Step 4. Create the Property Page</span></span>](step-4--create-the-property-page.md)
-   [<span data-ttu-id="88e3d-113">Etapa 5. Armazenar um ponteiro para o filtro</span><span class="sxs-lookup"><span data-stu-id="88e3d-113">Step 5. Store a Pointer to the Filter</span></span>](step-5--store-a-pointer-to-the-filter.md)
-   [<span data-ttu-id="88e3d-114">Etapa 6. Inicializar a caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="88e3d-114">Step 6. Initialize the Dialog</span></span>](step-6--initialize-the-dialog.md)
-   [<span data-ttu-id="88e3d-115">Etapa 7. Processar mensagens de janela</span><span class="sxs-lookup"><span data-stu-id="88e3d-115">Step 7. Handle Window Messages</span></span>](step-7--handle-window-messages.md)
-   [<span data-ttu-id="88e3d-116">Etapa 8. Aplicar alterações de propriedade</span><span class="sxs-lookup"><span data-stu-id="88e3d-116">Step 8. Apply Property Changes</span></span>](step-8--apply-property-changes.md)
-   [<span data-ttu-id="88e3d-117">Etapa 9. Desconectar a página de propriedades</span><span class="sxs-lookup"><span data-stu-id="88e3d-117">Step 9. Disconnect the Property Page</span></span>](step-9--disconnect-the-property-page.md)
-   [<span data-ttu-id="88e3d-118">Etapa 10. Suporte ao registro COM</span><span class="sxs-lookup"><span data-stu-id="88e3d-118">Step 10. Support COM Registration</span></span>](step-10--support-com-registration.md)

## <a name="related-topics"></a><span data-ttu-id="88e3d-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88e3d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88e3d-120">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="88e3d-120">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



