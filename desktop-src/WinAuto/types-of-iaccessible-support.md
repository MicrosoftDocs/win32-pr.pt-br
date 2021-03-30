---
title: Tipos de suporte do IAccessible
description: Tipos de suporte do IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635964"
---
# <a name="types-of-iaccessible-support"></a>Tipos de suporte do IAccessible

Os Microsoft Acessibilidade Ativa Servers têm dois tipos de suporte a [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : nativo e com proxy. Os elementos da interface do usuário usados em um aplicativo determinam qual tipo de suporte é apropriado. Muitos servidores que estão sendo gravados hoje aproveitam totalmente os proxies do **IAccessible** e só implementam o **IAccessible** para esses controles que não são proxies por Oleacc.dll, como controles sem janela ou controles com um nome de classe de janela personalizado.

## <a name="in-this-section"></a>Nesta seção

-   [Implementação de Acessibilidade Ativa nativo](native-active-accessibility-implementation.md)
-   [Proxies do IAccessible](iaccessible-proxies.md)

 

 




