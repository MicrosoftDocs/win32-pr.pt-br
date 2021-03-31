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
# <a name="using-acf-attributes-in-an-idl-file"></a>Usando atributos de ACF em um arquivo IDL

Você pode usar a opção de compilador de MIDL de [**\_ configuração de aplicativo**](-app-config.md) para especificar atributos de identificador de associação no arquivo IDL em vez de em um arquivo ACF separado. Especificamente, você pode aplicar os [**atributos \_ identificador automático**](auto-handle.md), [**\_ identificador implícito**](implicit-handle.md)e [**\_ identificador explícito**](explicit-handle.md) ao cabeçalho de uma interface RPC em um arquivo IDL. Considere usar essa opção se o aplicativo RPC não exigir outros atributos de ACF e se você não exigir a compatibilidade uso-DCE estrita.

 

 




