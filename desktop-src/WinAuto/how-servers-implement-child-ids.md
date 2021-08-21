---
title: Como os servidores implementam IDs filho
description: Os desenvolvedores de servidores podem atribuir IDs filho a elementos simples e objetos acessíveis. No entanto, a abordagem recomendada é dar suporte à interface padrão Component Object Model (COM) IEnumVARIANT em cada objeto acessível que tenha filhos.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb59dc263880ef73a4c1d52e15baa9d669d4cf712668b7bdabab549700ffd01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828643"
---
# <a name="how-servers-implement-child-ids"></a>Como os servidores implementam IDs filho

Os desenvolvedores de servidores podem atribuir IDs filho a elementos simples e objetos acessíveis. No entanto, a abordagem recomendada é dar suporte à interface padrão Component Object Model (COM) [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em cada objeto acessível que tenha filhos.

Se você implementar [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), deverá:

-   Enumerar todos os filhos, elementos simples e objetos acessíveis. Forneça IDs filho para todos os elementos simples e forneça [**o IDispatch para**](idispatch-interface.md) cada objeto acessível.
-   Para objetos acessíveis, de **definido o membro vt** da [**VARIANT**](variant-structure.md) como VT \_ DISPATCH. O **membro pdispVal** deve conter um ponteiro para a interface [**IDispatch.**](idispatch-interface.md) Observe que **VARIANT** é alocado e liberado pelo cliente.
-   Para elementos simples, a ID filho é qualquer inteiro positivo de 32 bits. Observe que zero e inteiros negativos são reservados por Microsoft Active Accessibility. De definir [**o membro**](variant-structure.md) da estrutura VARIANT **vt** como VT \_ I4 e o membro **lVal** como a ID filho.

Se você não tiver suporte para [IEnumVARIANT,](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)deverá atribuir IDs filho e numerar os filhos em cada objeto sequencialmente começando com um.

É recomendável que os clientes usem a função Microsoft Active Accessibility [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) em vez de chamar a interface [IEnumVARIANT do](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) servidor diretamente.

 

 