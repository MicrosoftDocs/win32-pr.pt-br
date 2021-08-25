---
title: Implementação de Acessibilidade Ativa nativo
description: Os elementos da interface do usuário que implementam a interface IAccessible são considerados para fornecer uma implementação nativa.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4414fa1cd40b66b0971d7c74f484b90c62f86db64722abaabc0e8eea60b14fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859926"
---
# <a name="native-active-accessibility-implementation"></a>Implementação de Acessibilidade Ativa nativo

Os elementos da interface do usuário que implementam a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) são considerados para fornecer uma *implementação nativa*. Embora o custo de desenvolvimento para implementar o **IAccessible** (ou qualquer outra interface de Component Object Model (com) possa ser alto, o benefício é o controle completo das informações expostas aos clientes.

Se seu aplicativo usar controles personalizados ou outros controles que não podem ser proxies por Oleacc.dll, será necessário fornecer uma implementação nativa.

 

 




