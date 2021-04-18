---
title: Associação de dados
description: Associação de dados
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105786228"
---
# <a name="databinding"></a><span data-ttu-id="7ea06-103">Associação de dados</span><span class="sxs-lookup"><span data-stu-id="7ea06-103">Databinding</span></span>

<span data-ttu-id="7ea06-104">Um novo atributo DataBinding foi adicionado para permitir que as propriedades se diferenciem entre as alterações de comunicação somente quando o foco deixa o controle ou durante todas as notificações de alteração de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7ea06-104">A new databinding attribute has been added to allow properties distinguish between communicating changes only when focus leaves the control or during all property change notifications.</span></span>

<span data-ttu-id="7ea06-105">O novo atributo, conhecido como ImmediateBind, permite que os controles diferenciem dois tipos diferentes de propriedades vinculáveis.</span><span class="sxs-lookup"><span data-stu-id="7ea06-105">The new attribute, known as ImmediateBind, enables controls to differentiate two different types of bindable properties.</span></span> <span data-ttu-id="7ea06-106">Um tipo de propriedade vinculável precisa notificar todas as alterações no banco de dados, por exemplo, com um controle caixa de seleção em que cada alteração precisa ser enviada para o banco de dados subjacente, embora o controle não tenha perdido o foco.</span><span class="sxs-lookup"><span data-stu-id="7ea06-106">One type of bindable property needs to notify every change to the database, for example with a check box control where every change needs to be sent through to the underlying database even though the control has not lost the focus.</span></span> <span data-ttu-id="7ea06-107">No entanto, os controles como uma ListBox só querem ter a alteração de uma propriedade notificada para o banco de dados quando o controle perde o foco, pois o usuário pode ter alterado a seleção realçada com as teclas de direção antes de localizar a configuração desejada, para que a notificação de alteração seja enviada ao banco de dados sempre que o usuário atingir a tecla de seta seria inaceitável.</span><span class="sxs-lookup"><span data-stu-id="7ea06-107">However controls such as a listbox only wish to have the change of a property notified to the database when the control loses focus, as the user may have changed the highlighted selection with the arrow keys before finding the desired setting, to have the change notification sent to the database every time that the user hit the arrow key would be give unacceptable performance.</span></span> <span data-ttu-id="7ea06-108">A nova propriedade de ligação imediata permite que as propriedades vinculáveis individuais em um formulário tenham esse comportamento especificado, quando esse bit for definido, todas as alterações serão notificadas.</span><span class="sxs-lookup"><span data-stu-id="7ea06-108">The new immediate bind property allows individual bindable properties on a form to have this behavior specified, when this bit is set all changes will be notified.</span></span>

<span data-ttu-id="7ea06-109">O novo bit ImmediateBind é mapeado para o novo VARFLAG \_ FIMMEDIATEBIND (0x80) e os bits FUNCFLAG FIMMEDIATEBIND \_ (0x80) nas enumerações VARFLAGS e FUNCFLAGS para a interface [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) , permitindo que os atributos de propriedades sejam inspecionados.</span><span class="sxs-lookup"><span data-stu-id="7ea06-109">The new ImmediateBind bit maps through to the new VARFLAG\_FIMMEDIATEBIND (0x80) and the FUNCFLAG\_FIMMEDIATEBIND (0x80) bits in the VARFLAGS and FUNCFLAGS enumerations for the [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interface allowing for the properties attributes to be inspected.</span></span>

 

 