---
title: O identificador do objeto OBJID_QUERYCLASSNAMEIDX
description: O Microsoft Acessibilidade Ativa usa o \_ identificador de objeto OBJID QUERYCLASSNAMEIDX com a mensagem do WM \_ GetObject para determinar a classe à qual pertence um controle padrão do Windows ou o controle comum.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764378"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a><span data-ttu-id="a1aab-103">O \_ identificador de objeto OBJID QUERYCLASSNAMEIDX</span><span class="sxs-lookup"><span data-stu-id="a1aab-103">The OBJID\_QUERYCLASSNAMEIDX Object Identifier</span></span>

<span data-ttu-id="a1aab-104">O Microsoft Acessibilidade Ativa usa o identificador de objeto [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) com a mensagem do [**WM \_ GetObject**](wm-getobject.md) para determinar a classe à qual pertence um controle padrão do Windows ou o controle comum.</span><span class="sxs-lookup"><span data-stu-id="a1aab-104">Microsoft Active Accessibility uses the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier with the [**WM\_GETOBJECT**](wm-getobject.md) message to determine the class to which a standard Windows control or common control belongs.</span></span> <span data-ttu-id="a1aab-105">Um controle responde a essa mensagem retornando um valor que o Microsoft Acessibilidade Ativa mapeia para o nome de classe do controle.</span><span class="sxs-lookup"><span data-stu-id="a1aab-105">A control responds to this message by returning a value that Microsoft Active Accessibility maps to the class name of the control.</span></span> <span data-ttu-id="a1aab-106">O Microsoft Acessibilidade Ativa usa essas informações para fornecer suporte de acessibilidade para controles padrão do Windows e controles comuns.</span><span class="sxs-lookup"><span data-stu-id="a1aab-106">Microsoft Active Accessibility uses this information to provide accessibility support for standard Windows controls and common controls.</span></span>

<span data-ttu-id="a1aab-107">Em geral, somente os controles padrão do Windows e os controles comuns respondem ao identificador de objeto [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="a1aab-107">Generally, only the standard Windows controls and the common controls respond to the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="a1aab-108">No entanto, um controle personalizado também pode responder se ele inclui toda a mesma funcionalidade de um controle padrão do Windows ou controle comum.</span><span class="sxs-lookup"><span data-stu-id="a1aab-108">However, a custom control can also respond if it includes all of the same functionality as an existing standard Windows control or common control.</span></span> <span data-ttu-id="a1aab-109">Isso permite que o controle personalizado tenha suporte de um dos objetos de proxy padrão fornecidos pelo Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="a1aab-109">This enables the custom control to be supported by one of the standard proxy objects provided by Microsoft Active Accessibility.</span></span>

<span data-ttu-id="a1aab-110">Para obter mais informações, consulte o [Apêndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span><span class="sxs-lookup"><span data-stu-id="a1aab-110">For more information, see [Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span></span>

 

 




