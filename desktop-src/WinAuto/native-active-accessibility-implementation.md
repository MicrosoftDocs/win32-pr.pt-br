---
title: Implementação de Acessibilidade Ativa nativo
description: Os elementos da interface do usuário que implementam a interface IAccessible são considerados para fornecer uma implementação nativa.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f6e6b6152c2f5e5c41a6a2b7cd3f84a3fce373
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105762426"
---
# <a name="native-active-accessibility-implementation"></a>Implementação de Acessibilidade Ativa nativo

Os elementos da interface do usuário que implementam a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) são considerados para fornecer uma *implementação nativa*. Embora o custo de desenvolvimento para implementar o **IAccessible** (ou qualquer outra interface de Component Object Model (com) possa ser alto, o benefício é o controle completo das informações expostas aos clientes.

Se seu aplicativo usar controles personalizados ou outros controles que não podem ser proxies por Oleacc.dll, será necessário fornecer uma implementação nativa.

 

 




