---
title: Usando atributos de ACF em um arquivo IDL
description: Você pode usar a \_ opção de compilador/app config MIDL para especificar atributos de identificador de associação no arquivo IDL em vez de em um arquivo ACF separado.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- MIDL de ACF, atributos, usando ACF em IDL
- MIDL de IDL, usando ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda925a3b3242072f297c8828427ae4f7a488d1f3b002e05ace6bec45a46d2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105516"
---
# <a name="using-acf-attributes-in-an-idl-file"></a>Usando atributos de ACF em um arquivo IDL

Você pode usar a opção de compilador de MIDL de [**\_ configuração de aplicativo**](-app-config.md) para especificar atributos de identificador de associação no arquivo IDL em vez de em um arquivo ACF separado. Especificamente, você pode aplicar os [**atributos \_ identificador automático**](auto-handle.md), [**\_ identificador implícito**](implicit-handle.md)e [**\_ identificador explícito**](explicit-handle.md) ao cabeçalho de uma interface RPC em um arquivo IDL. Considere usar essa opção se o aplicativo RPC não exigir outros atributos de ACF e se você não exigir a compatibilidade uso-DCE estrita.

 

 




