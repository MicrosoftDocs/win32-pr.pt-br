---
description: Gerenciamento de esquema de energia
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Gerenciamento de esquema de energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757083"
---
# <a name="power-scheme-management"></a><span data-ttu-id="c7466-103">Gerenciamento de esquema de energia</span><span class="sxs-lookup"><span data-stu-id="c7466-103">Power Scheme Management</span></span>

<span data-ttu-id="c7466-104">Cada esquema de energia é identificado exclusivamente por um **GUID**.</span><span class="sxs-lookup"><span data-stu-id="c7466-104">Each power scheme is uniquely identified by a **GUID**.</span></span> <span data-ttu-id="c7466-105">Para enumerar todos os esquemas de energia disponíveis, use a função [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) .</span><span class="sxs-lookup"><span data-stu-id="c7466-105">To enumerate all available power schemes, use the [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) function.</span></span> <span data-ttu-id="c7466-106">**PowerEnumerate** também pode ser usado para recuperar todas as configurações de energia de um esquema especificado.</span><span class="sxs-lookup"><span data-stu-id="c7466-106">**PowerEnumerate** can also be used to retrieve all of the power settings for a specified scheme.</span></span>

<span data-ttu-id="c7466-107">O esquema de energia que está atualmente em uso no sistema é chamado de plano ou esquema de energia ativo.</span><span class="sxs-lookup"><span data-stu-id="c7466-107">The power scheme that is currently in use on the system is called the active power scheme or plan.</span></span> <span data-ttu-id="c7466-108">Para recuperar o **GUID** do plano ativo, chame a função [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="c7466-108">To retrieve the **GUID** of the active plan, call the [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) function.</span></span> <span data-ttu-id="c7466-109">Para alterar o plano de energia ativo, chame a função [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="c7466-109">To change the active power plan, call the [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) function.</span></span>

<span data-ttu-id="c7466-110">Para criar um esquema de energia, você precisa primeiro duplicar um esquema existente usando a função [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) , especificando o **GUID** do esquema no qual você deseja basear seu novo esquema.</span><span class="sxs-lookup"><span data-stu-id="c7466-110">To create a power scheme, you need to first duplicate an existing scheme by using the [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) function, specifying the **GUID** of the scheme you wish to base your new scheme upon.</span></span> <span data-ttu-id="c7466-111">Você deve copiar um dos esquemas internos e modificar as configurações de energia para suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="c7466-111">You should copy one of the built-in schemes and modify the power settings to your needs.</span></span> <span data-ttu-id="c7466-112">Observe que a criação de um plano de energia não atualiza automaticamente o plano de energia ativo.</span><span class="sxs-lookup"><span data-stu-id="c7466-112">Note that creating a power plan does not automatically update the active power plan.</span></span> <span data-ttu-id="c7466-113">Você deve sempre chamar [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) para atualizar o plano de energia ativo.</span><span class="sxs-lookup"><span data-stu-id="c7466-113">You must always call [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) to update the active power plan.</span></span> <span data-ttu-id="c7466-114">Os planos de energia existentes podem ser modificados e aplicados da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="c7466-114">Existing power plans can be modified and then applied in the same manner.</span></span>

<span data-ttu-id="c7466-115">Para remover um plano de energia, chame a função [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) .</span><span class="sxs-lookup"><span data-stu-id="c7466-115">To remove a power plan, call the [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) function.</span></span>

> [!Note]  
> <span data-ttu-id="c7466-116">Para recuperar informações adicionais sobre o estado de energia do sistema, chame a função [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) .</span><span class="sxs-lookup"><span data-stu-id="c7466-116">To retrieve additional information about the system power state, call the [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c7466-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7466-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7466-118">Esquemas de energia</span><span class="sxs-lookup"><span data-stu-id="c7466-118">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 



