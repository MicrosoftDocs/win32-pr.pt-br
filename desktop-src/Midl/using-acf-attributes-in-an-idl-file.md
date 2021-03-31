---
title: Usando atributos de ACF em um arquivo IDL
description: Você pode usar a \_ opção de compilador/app config MIDL para especificar atributos de identificador de associação no arquivo IDL em vez de em um arquivo ACF separado.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- MIDL de ACF, atributos, usando ACF em IDL
- MIDL de IDL, usando ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712dde95201bc2c729ac126b35e04919fd196cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635673"
---
# <a name="using-acf-attributes-in-an-idl-file"></a><span data-ttu-id="b115d-105">Usando atributos de ACF em um arquivo IDL</span><span class="sxs-lookup"><span data-stu-id="b115d-105">Using ACF Attributes in an IDL File</span></span>

<span data-ttu-id="b115d-106">Você pode usar a opção de compilador de MIDL de [**\_ configuração de aplicativo**](-app-config.md) para especificar atributos de identificador de associação no arquivo IDL em vez de em um arquivo ACF separado.</span><span class="sxs-lookup"><span data-stu-id="b115d-106">You can use the /[**app\_config**](-app-config.md) MIDL compiler option to specify binding handle attributes in the IDL file rather than in a separate ACF file.</span></span> <span data-ttu-id="b115d-107">Especificamente, você pode aplicar os [**atributos \_ identificador automático**](auto-handle.md), [**\_ identificador implícito**](implicit-handle.md)e [**\_ identificador explícito**](explicit-handle.md) ao cabeçalho de uma interface RPC em um arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="b115d-107">Specifically, you can apply the [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), and [**explicit\_handle**](explicit-handle.md) attributes to the header of an RPC interface in an IDL file.</span></span> <span data-ttu-id="b115d-108">Considere usar essa opção se o aplicativo RPC não exigir outros atributos de ACF e se você não exigir a compatibilidade uso-DCE estrita.</span><span class="sxs-lookup"><span data-stu-id="b115d-108">Consider using this option if your RPC application does not require other ACF attributes, and if you do not require strict OSF-DCE compatibility.</span></span>

 

 




