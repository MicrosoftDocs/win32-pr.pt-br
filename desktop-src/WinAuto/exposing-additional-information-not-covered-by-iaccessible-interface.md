---
title: Expondo informações adicionais não cobertas pela interface IAccessible
description: Dependendo de seus produtos, os desenvolvedores de servidores talvez precisem expor informações ou funcionalidades além do suporte ao Microsoft Acessibilidade Ativa.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294357"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a>Expondo informações adicionais não cobertas pela interface IAccessible

Dependendo de seus produtos, os desenvolvedores de servidores talvez precisem expor informações ou funcionalidades além do suporte ao Microsoft Acessibilidade Ativa. Se esse for o caso, trabalhe com fornecedores de tecnologia assistencial (clientes) para garantir que eles adicionem suporte para os recursos.

Não tente estender a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . As interfaces não podem ser alteradas depois de serem publicadas. Para expor informações adicionais, use uma interface personalizada e exporte-a usando uma das seguintes técnicas:

-   [Usando OBJID \_ NATIVEOM para expor uma interface de modelo de objeto nativo para uma janela](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [Usando o QueryService para expor uma interface de modelo de objeto nativo para um objeto IAccessible](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

Observe que o objetivo da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) é ter uma interface bem definida que é usada por servidores e clientes. Antes de expor interfaces personalizadas, não se esqueça de expor o máximo possível de informações por meio do **IAccessible**.

Você não pode usar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para expor interfaces personalizadas. Use **IServiceProvider:: QueryService** conforme descrito nos procedimentos a seguir.

 

 