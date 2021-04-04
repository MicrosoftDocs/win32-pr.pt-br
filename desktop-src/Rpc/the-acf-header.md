---
title: O cabeçalho ACF
description: O cabeçalho ACF contém atributos específicos da plataforma que se aplicam à interface como um todo. Os atributos aplicados a tipos individuais e funções no corpo de ACF substituem os atributos no cabeçalho ACF. Nenhum atributo é necessário no cabeçalho ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007827"
---
# <a name="the-acf-header"></a>O cabeçalho ACF

O cabeçalho ACF contém atributos específicos da plataforma que se aplicam à interface como um todo. Os atributos aplicados a tipos individuais e funções no corpo de ACF substituem os atributos no cabeçalho ACF. Nenhum atributo é necessário no cabeçalho ACF.

O cabeçalho ACF pode incluir um dos seguintes atributos: **\[** [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) **\]** ou [**\_ identificador explícito**](/windows/desktop/Midl/explicit-handle) **\]** . Se o **\[ \_ identificador \] automático** ou o **\[ \_ \] identificador implícito** for usado, ele especificará o tipo de identificador de associação que será usado para associação quando uma função remota não tiver um parâmetro de identificador de ligação explícito. Quando o ACF não está presente ou não especifica um identificador de associação automático, implícito ou explícito, MIDL usa o **\[ \_ identificador \] auto** para associação implícita.

O **\[** [**código**](/windows/desktop/Midl/code) **\]** ou o **\[** [**Nocode**](/windows/desktop/Midl/nocode) **\]** podem aparecer no cabeçalho da interface, mas o que você escolher pode aparecer apenas uma vez. Quando nenhum atributo estiver presente, o compilador usará o **\[ código \]** como padrão.

Para obter mais informações, consulte [atributos de ACF](/windows/desktop/Midl/acf-attributes).

 

 