---
title: Sobrecarregando IPropertyNotifySink
description: Sobrecarregando IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364331"
---
# <a name="overloading-ipropertynotifysink"></a><span data-ttu-id="692ed-103">Sobrecarregando IPropertyNotifySink</span><span class="sxs-lookup"><span data-stu-id="692ed-103">Overloading IPropertyNotifySink</span></span>

<span data-ttu-id="692ed-104">Muitos contêineres de controle ActiveX implementam uma janela de navegação de propriedade sem controle de modelo.</span><span class="sxs-lookup"><span data-stu-id="692ed-104">Many ActiveX control containers implement a modeless property browsing window.</span></span> <span data-ttu-id="692ed-105">Se as propriedades de um controle forem alteradas por meio das páginas de propriedades do controle, as propriedades do controle poderão ficar fora de sincronia com a exibição do contêiner dessas propriedades (o controle é sempre certo, é claro).</span><span class="sxs-lookup"><span data-stu-id="692ed-105">If a control's properties are altered through the control's property pages, then the control's properties can get out of sync with the container's view of those properties (the control is always right, of course).</span></span> <span data-ttu-id="692ed-106">Para garantir que ele sempre tenha os valores atuais para as propriedades de um controle, um contêiner de controle ActiveX pode sobrecarregar a interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (Associação de dados) e também usá-la para ser notificado de que uma propriedade de controle foi alterada.</span><span class="sxs-lookup"><span data-stu-id="692ed-106">To ensure that it always has the current values for a control's properties, an ActiveX control container can overload the [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) interface (data binding) and also use it to be notified that a control property has changed.</span></span> <span data-ttu-id="692ed-107">Essa técnica é opcional e não é necessária para contêineres de controle ActiveX ou controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="692ed-107">This technique is optional and is not required of ActiveX control containers or ActiveX controls.</span></span>

<span data-ttu-id="692ed-108">Observe que um controle deve usar [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) somente para vinculação de dados; é livre usar [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) para uma ou ambas as finalidades.</span><span class="sxs-lookup"><span data-stu-id="692ed-108">Note that a control should use [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) only for data binding; it is free to use [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) for either or both purposes.</span></span>

 

 




