---
description: Se você optar por converter seus pacotes MTS em aplicativos COM+ manualmente ou deixar que o processo de instalação do Microsoft Windows faça isso automaticamente, você deve estar ciente dos resultados da conversão, bem como dos problemas.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Resultados e problemas de conversão de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370508"
---
# <a name="com-conversion-results-and-issues"></a><span data-ttu-id="ddd4a-103">Resultados e problemas de conversão de COM+</span><span class="sxs-lookup"><span data-stu-id="ddd4a-103">COM+ Conversion Results and Issues</span></span>

<span data-ttu-id="ddd4a-104">Se você optar por converter seus pacotes MTS em aplicativos COM+ manualmente ou deixar que o processo de instalação do Microsoft Windows faça isso automaticamente, você deve estar ciente dos resultados da conversão, bem como dos problemas.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-104">Whether you choose to convert your MTS packages to COM+ applications manually or let the Microsoft Windows setup process do it for you automatically, you should be aware of the results of conversion as well as the issues.</span></span>

## <a name="what-is-converted"></a><span data-ttu-id="ddd4a-105">O que é convertido</span><span class="sxs-lookup"><span data-stu-id="ddd4a-105">What Is Converted</span></span>

<span data-ttu-id="ddd4a-106">Durante a conversão, o utilitário MTSTOCOM converte funções, atribuições de função, interfaces, métodos, usuários, a lista de computadores e a maioria das configurações do computador.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-106">During conversion, the MTSTOCOM utility converts roles, role assignments, interfaces, methods, users, the computer list, and most computer settings.</span></span> <span data-ttu-id="ddd4a-107">O utilitário MTSTOCOM também converte a identidade e a senha de um pacote MTS.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-107">The MTSTOCOM utility also converts the identity and password for an MTS package.</span></span>

<span data-ttu-id="ddd4a-108">Os novos atributos COM+ que não estavam disponíveis no MTS são automaticamente definidos com os padrões a seguir para todos os componentes do MTS convertidos.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-108">The new COM+ attributes that were not available in MTS are automatically set to the following defaults for all converted MTS components.</span></span> <span data-ttu-id="ddd4a-109">Esses padrões podem ser alterados usando a ferramenta administrativa serviços de componentes ou as interfaces administrativas COM+.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-109">These defaults can be changed using either the Component Services administrative tool or the COM+ administrative interfaces.</span></span>

-   <span data-ttu-id="ddd4a-110">Ativação JIT habilitada.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-110">JIT activation enabled.</span></span>
-   <span data-ttu-id="ddd4a-111">Pool de objetos desabilitado.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-111">Object pooling disabled.</span></span>
-   <span data-ttu-id="ddd4a-112">Sincronização igual à configuração de transação.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-112">Synchronization same as Transaction setting.</span></span>

## <a name="conversion-issues"></a><span data-ttu-id="ddd4a-113">Problemas de conversão</span><span class="sxs-lookup"><span data-stu-id="ddd4a-113">Conversion Issues</span></span>

<span data-ttu-id="ddd4a-114">O COM+ é instalado automaticamente quando você instala o Windows.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-114">COM+ is automatically installed when you install Windows.</span></span> <span data-ttu-id="ddd4a-115">Não é possível desinstalar o COM+.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-115">It is not possible to uninstall COM+.</span></span> <span data-ttu-id="ddd4a-116">Os problemas relacionados a atualizações das instalações MTS e COM+ existentes incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ddd4a-116">Issues related to upgrades of existing MTS and COM+ installations include the following:</span></span>

-   <span data-ttu-id="ddd4a-117">Se você estiver usando o MTS 1,0 no momento, o MTS será atualizado automaticamente para COM+.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-117">If you are currently using MTS 1.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="ddd4a-118">No entanto, os pacotes definidos pelo usuário serão perdidos e você deverá recriá-los.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-118">However, user-defined packages will be lost and you must re-create them.</span></span>
-   <span data-ttu-id="ddd4a-119">Se você estiver usando o MTS 2,0 no momento, o MTS será atualizado automaticamente para COM+.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-119">If you are currently using MTS 2.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="ddd4a-120">Todos os pacotes definidos pelo usuário serão atualizados para aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-120">All user-defined packages will be upgraded to COM+ applications.</span></span> <span data-ttu-id="ddd4a-121">Todos os componentes devem funcionar como faziam no MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-121">All components should work as they did under MTS 2.0.</span></span>
-   <span data-ttu-id="ddd4a-122">Se você estiver usando o MTS 1,0 e o MTS 2,0 e tiver instalado a opção SDK, os arquivos do SDK serão removidos.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-122">If you are using MTS 1.0 and MTS 2.0 and have installed the SDK option, the SDK files will be removed.</span></span> <span data-ttu-id="ddd4a-123">Você pode instalar o SDK COM+ mais recente por meio do SDK do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-123">You can install the latest COM+ SDK through the Microsoft Windows SDK.</span></span>
-   <span data-ttu-id="ddd4a-124">Você não pode gerenciar um computador MTS remoto a partir de um computador COM+.</span><span class="sxs-lookup"><span data-stu-id="ddd4a-124">You cannot manage a remote MTS computer from a COM+ computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddd4a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddd4a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddd4a-126">Conversão automática do MTS</span><span class="sxs-lookup"><span data-stu-id="ddd4a-126">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="ddd4a-127">Conversão manual do MTS</span><span class="sxs-lookup"><span data-stu-id="ddd4a-127">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="ddd4a-128">Biblioteca de administração MTS</span><span class="sxs-lookup"><span data-stu-id="ddd4a-128">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



