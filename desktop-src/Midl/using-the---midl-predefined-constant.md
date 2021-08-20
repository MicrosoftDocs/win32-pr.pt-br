---
title: Usando o __midl constante predefinida
description: Quando o compilador MIDL processa os arquivos IDL e ACF de entrada, \_ \_ MIDL é definido por padrão e é usado para compilação condicional para atingir a consistência em todo o Build.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL do compilador MIDL, usando a _midl constante predefinida
- _midl MIDL de constante predefinida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fbc111ad07839d891f7bdffaf7ecaae83fbf277a0fc2c93fc483f526f9dda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382817"
---
# <a name="using-the-__midl-predefined-constant"></a>Usando a \_ \_ constante predefinida MIDL

Quando o compilador MIDL processa os arquivos IDL e ACF de entrada, \_ \_ MIDL é definido por padrão e é usado para compilação condicional para atingir a consistência em todo o Build. Isso reduz o uso de instruções de definição nos arquivos de cabeçalho, como o **\_ passo de MIDL**, e os substitui por um sinalizador consistente. O valor da \_ \_ constante MIDL indica a versão do compilador *Major. Minor* de acordo com a fórmula *Major* \* 100 + *Minor*; por exemplo, MIDL ver. 6.0. x tem o \_ \_ MIDL definido como 600.

Se você escolher, poderá substituir esse padrão especificando o seguinte na linha de comando: **/u \_ \_ MIDL**. Para obter mais informações, consulte [**/u**](-u.md).

 

 




