---
title: Estrutura VARIANT
description: A maioria das Microsoft Active Accessibility funções e os métodos e propriedades IAccessible levam uma estrutura VARIANT como um parâmetro. Essencialmente, a estrutura VARIANT é um contêiner para uma grande união que carrega muitos tipos de dados.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063d1e17d998f3cb7d70a0a271e55f02628e7864164e00becb5a708af371e12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563544"
---
# <a name="variant-structure"></a>Estrutura VARIANT

A maioria das funções Microsoft Active Accessibility e os métodos e propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) levam uma [**estrutura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) como um parâmetro. Essencialmente, a **estrutura VARIANT** é um contêiner para uma grande união que carrega muitos tipos de dados.

O valor no primeiro membro da estrutura, **vt**, descreve qual dos membros da união é válido. Embora a [**estrutura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) seja compatível com muitos tipos de dados diferentes, Microsoft Active Accessibility usa apenas os tipos a seguir.



| Valor de vt     | Nome do membro do valor correspondente |
|--------------|---------------------------------|
| VT \_ I4       | **lVal**                        |
| DISPATCH \_ da VT | **pdispVal**                    |
| VT \_ BSTR     | **bstrVal**                     |
| VT \_ VAZIO    | nenhum                            |



 

Quando você receber informações em uma [**estrutura VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) verifique o **membro vt** para descobrir qual membro contém dados válidos. Da mesma forma, quando você envia informações usando uma **estrutura VARIANT,** sempre de definido **vt** para refletir o membro da união que contém as informações.

Antes de usar a estrutura , inicialize-a chamando a [**função VARIANTInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM). Quando terminar com a estrutura, limpe-a antes que a memória que contém [**a VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) seja liberada chamando [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).

 

 