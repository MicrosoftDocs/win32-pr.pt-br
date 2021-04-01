---
title: Estrutura de variante
description: A maioria das funções do Microsoft Acessibilidade Ativa e os métodos e as propriedades do IAccessible usam uma estrutura variante como parâmetro. Essencialmente, a estrutura variante é um contêiner para uma União grande que transporta muitos tipos de dados.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084658"
---
# <a name="variant-structure"></a>Estrutura de variante

A maioria das funções do Microsoft Acessibilidade Ativa e os métodos e as propriedades do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) usam uma estrutura [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) como parâmetro. Essencialmente, a estrutura **variante** é um contêiner para uma União grande que transporta muitos tipos de dados.

O valor no primeiro membro da estrutura, **VT**, descreve qual dos membros da União é válido. Embora a estrutura [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) ofereça suporte a muitos tipos de dados diferentes, o Microsoft Acessibilidade Ativa usa apenas os tipos a seguir.



| Valor de VT     | Nome do membro do valor correspondente |
|--------------|---------------------------------|
| \_I4 VT       | **lVal**                        |
| expedição de VT \_ | **pdispVal**                    |
| VT \_ BSTR     | **bstrVal**                     |
| VT \_ vazio    | none                            |



 

Ao receber informações em uma estrutura de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) , verifique o membro **VT** para descobrir qual membro contém dados válidos. Da mesma forma, quando você envia informações usando uma estrutura **Variant** , sempre defina **VT** para refletir o membro Union que contém as informações.

Antes de usar a estrutura, inicialize-a chamando a função COM ( [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model). Quando terminar com a estrutura, limpe-a antes que a memória que contém a [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) seja liberada chamando [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).

 

 