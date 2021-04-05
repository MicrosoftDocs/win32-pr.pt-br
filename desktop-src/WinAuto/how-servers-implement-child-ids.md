---
title: Como os servidores implementam IDs filho
description: Os desenvolvedores de servidor podem atribuir IDs filho a elementos simples e objetos acessíveis. No entanto, a abordagem recomendada é oferecer suporte à interface de Component Object Model padrão (COM) IEnumVARIANT em todos os objetos acessíveis que tenham filhos.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917476"
---
# <a name="how-servers-implement-child-ids"></a>Como os servidores implementam IDs filho

Os desenvolvedores de servidor podem atribuir IDs filho a elementos simples e objetos acessíveis. No entanto, a abordagem recomendada é oferecer suporte à interface de Component Object Model padrão (COM) [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em todos os objetos acessíveis que tenham filhos.

Se você implementar o [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), deverá:

-   Enumere todos os filhos, tanto elementos simples quanto objetos acessíveis. Forneça IDs filho para todos os elementos simples e forneça o [**IDispatch**](idispatch-interface.md) para cada objeto acessível.
-   Para objetos acessíveis, defina o membro **VT** da expedição de [**variante**](variant-structure.md) para VT \_ . O membro **pdispVal** deve conter um ponteiro para a interface [**IDispatch**](idispatch-interface.md) . Observe que a **variante** é alocada e liberada pelo cliente.
-   Para elementos simples, a ID filho é qualquer número inteiro positivo de 32 bits. Observe que os inteiros zero e negativos são reservados pelo Microsoft Acessibilidade Ativa. Defina o membro **VT** da estrutura [**variante**](variant-structure.md) como VT \_ i4 e o membro **lVal** como a ID filho.

Se você não oferecer suporte a [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), deverá atribuir IDs filho e numerar os filhos em cada objeto de forma sequencial, começando com um.

É recomendável que os clientes usem a função Microsoft Acessibilidade Ativa [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) em vez de chamar a interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) do servidor diretamente.

 

 