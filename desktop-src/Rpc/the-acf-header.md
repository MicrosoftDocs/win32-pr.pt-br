---
title: O header do ACF
description: O header ACF contém atributos específicos da plataforma que se aplicam à interface como um todo. Atributos aplicados a tipos e funções individuais no corpo do ACF substituem os atributos no header do ACF. Nenhum atributos é necessário no header do ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdfeced843337143fd441d816e3b575be2e7ebc7d93000094f8dcd3737a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924606"
---
# <a name="the-acf-header"></a>O header do ACF

O header ACF contém atributos específicos da plataforma que se aplicam à interface como um todo. Atributos aplicados a tipos e funções individuais no corpo do ACF substituem os atributos no header do ACF. Nenhum atributos é necessário no header do ACF.

O header ACF pode incluir um dos seguintes atributos: **\[** [**auto \_ handle**](/windows/desktop/Midl/auto-handle) **\]** , implicit **\[** [**\_ handle**](/windows/desktop/Midl/implicit-handle) **\]** ou explicit [**\_ handle**](/windows/desktop/Midl/explicit-handle) **\]** . Se **\[ o \_ \] identificador** **\[ \_ \] automático** ou o identificador implícito for usado, ele especificará o tipo de identificador de associação que será usado para associação quando uma função remota não tiver um parâmetro de identificador de associação explícito. Quando o ACF não está presente ou não especifica um alça de associação automática, implícita ou explícita, o MIDL **\[ \_ \]** usa o controle automático para associação implícita.

O **\[** [**código**](/windows/desktop/Midl/code) **\]** ou **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** pode aparecer no header da interface, mas o que você escolher pode aparecer apenas uma vez. Quando nenhum atributo está presente, o compilador usa **\[ o código \]** como padrão.

Para obter mais informações, consulte [Atributos do ACF.](/windows/desktop/Midl/acf-attributes)

 

 