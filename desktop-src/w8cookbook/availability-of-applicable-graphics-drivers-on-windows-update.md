---
title: Disponibilidade de drivers gráficos aplicáveis no Windows Update
description: A disponibilidade desses drivers em Windows Update (WU) determinará se um usuário recebe automaticamente uma atualização do Windows 7, Windows 8 ou Windows 8.1 para o Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784964"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a><span data-ttu-id="86dac-103">Disponibilidade de drivers gráficos aplicáveis no Windows Update</span><span class="sxs-lookup"><span data-stu-id="86dac-103">Availability of applicable graphics drivers on Windows Update</span></span>

<span data-ttu-id="86dac-104">A disponibilidade desses drivers em Windows Update (WU) determinará se um usuário recebe automaticamente uma atualização do Windows 7, Windows 8 ou Windows 8.1 para o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="86dac-104">The availability of these drivers on Windows Update (WU) will determine whether a user is automatically offered an upgrade from Windows 7, Windows 8 or Windows 8.1 to Windows 10.</span></span> <span data-ttu-id="86dac-105">Se as verificações de hardware mostrarem que não havia driver de gráficos disponível em Windows Update para o adaptador gráfico no PC, os usuários não receberam o sistema operacional Windows 10 atualizado.</span><span class="sxs-lookup"><span data-stu-id="86dac-105">If hardware scans showed that there was no graphics driver available on Windows Update for the graphics adapter in the PC, users were not offered the updated Windows 10 OS.</span></span> <span data-ttu-id="86dac-106">No entanto, os usuários ainda podem obter o Windows 10 por meio de outras fontes e executar manualmente a atualização.</span><span class="sxs-lookup"><span data-stu-id="86dac-106">However, users can still obtain Windows 10 through other sources and manually perform the upgrade.</span></span>

<span data-ttu-id="86dac-107">Alguns usuários não tinham certeza de por que eles não ofereciam a atualização quando outras pessoas eram, embora o supervisor de atualização tenha explicado que não havia nenhum driver de gráfico disponível para seu hardware.</span><span class="sxs-lookup"><span data-stu-id="86dac-107">Some users were unsure of why they were not offered the upgrade when other people were, even though the Upgrade Advisor explained that there was no graphics driver available for their hardware.</span></span>

<span data-ttu-id="86dac-108">Além disso, alguns usuários forçaram uma atualização e, em seguida, descobriram que sua funcionalidade gráfica e desempenho sofreu devido à falta de um driver de hardware.</span><span class="sxs-lookup"><span data-stu-id="86dac-108">Additionally, some users forced an upgrade and then found that their graphics functionality and performance suffered due to the lack of a hardware driver.</span></span>

## <a name="mitigations"></a><span data-ttu-id="86dac-109">Atenuações</span><span class="sxs-lookup"><span data-stu-id="86dac-109">Mitigations</span></span>

<span data-ttu-id="86dac-110">Para atenuar isso, os usuários podem instalar manualmente um driver mais antigo, ou seja, do Windows 7, Windows 8 ou Windows 8.1, acessando o site da Web do IHV ou OEM e baixando um driver explicitamente.</span><span class="sxs-lookup"><span data-stu-id="86dac-110">To mitigate this, users can manually install an older driver, i.e. from Windows 7, Windows 8 or Windows 8.1, by going to the IHV or OEM web site and downloading a driver explicitly.</span></span> <span data-ttu-id="86dac-111">Isso deve ser feito após a atualização e não há garantia de que funcione.</span><span class="sxs-lookup"><span data-stu-id="86dac-111">This must be done after the upgrade and is not guaranteed to work.</span></span> <span data-ttu-id="86dac-112">Não há solução com suporte se um driver gráfico adequado não estiver disponível no WU.</span><span class="sxs-lookup"><span data-stu-id="86dac-112">There is no supported solution if a suitable graphics driver is not available on WU.</span></span> <span data-ttu-id="86dac-113">O usuário deve decidir se:</span><span class="sxs-lookup"><span data-stu-id="86dac-113">The user must decide whether to:</span></span>

-   <span data-ttu-id="86dac-114">Permanecer no sistema operacional anterior;</span><span class="sxs-lookup"><span data-stu-id="86dac-114">Remain on the previous OS;</span></span>
-   <span data-ttu-id="86dac-115">Aceite as limitações do driver de software, o adaptador de vídeo básico da Microsoft (MSBDA); or</span><span class="sxs-lookup"><span data-stu-id="86dac-115">Accept the limitations of the software driver, Microsoft Basic Display Adapter (MSBDA); or</span></span>
-   <span data-ttu-id="86dac-116">Compre uma nova placa gráfica que tenha um driver do Windows 10 com suporte.</span><span class="sxs-lookup"><span data-stu-id="86dac-116">Buy a new graphics card that has a supported Windows 10 driver.</span></span>

## <a name="solutions"></a><span data-ttu-id="86dac-117">Soluções</span><span class="sxs-lookup"><span data-stu-id="86dac-117">Solutions</span></span>

<span data-ttu-id="86dac-118">É fundamental que os IHVs e os OEMs Carreguem seus drivers gráficos do Windows 10 no WU para qualquer hardware que pretendam oferecer suporte.</span><span class="sxs-lookup"><span data-stu-id="86dac-118">It’s critical that IHVs and OEMs upload their Windows 10 graphics drivers to WU for any hardware that they intend to support.</span></span>

<span data-ttu-id="86dac-119">Observe que o hardware que atingiu o fim da vida útil (EOL) pode não ter drivers no WU.</span><span class="sxs-lookup"><span data-stu-id="86dac-119">Note that hardware that has reached End-Of-Live (EOL) might not have drivers on WU.</span></span> <span data-ttu-id="86dac-120">Não há nenhuma solução nesse caso – o usuário deve escolher uma das opções em atenuações acima.</span><span class="sxs-lookup"><span data-stu-id="86dac-120">There is no solution in this case – the user must choose one of the options under Mitigations above.</span></span>

 

 




