---
title: Usando o __midl constante predefinida
description: Quando o compilador MIDL processa os arquivos IDL e ACF de entrada, \_ \_ MIDL é definido por padrão e é usado para compilação condicional para atingir a consistência em todo o Build.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL do compilador MIDL, usando a _midl constante predefinida
- _midl MIDL de constante predefinida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005595"
---
# <a name="using-the-__midl-predefined-constant"></a>Usando a \_ \_ constante predefinida MIDL

Quando o compilador MIDL processa os arquivos IDL e ACF de entrada, \_ \_ MIDL é definido por padrão e é usado para compilação condicional para atingir a consistência em todo o Build. Isso reduz o uso de instruções de definição nos arquivos de cabeçalho, como o **\_ passo de MIDL**, e os substitui por um sinalizador consistente. O valor da \_ \_ constante MIDL indica a versão do compilador *Major. Minor* de acordo com a fórmula *Major* \* 100 + *Minor*; por exemplo, MIDL ver. 6.0. x tem o \_ \_ MIDL definido como 600.

Se você escolher, poderá substituir esse padrão especificando o seguinte na linha de comando: **/u \_ \_ MIDL**. Para obter mais informações, consulte [**/u**](-u.md).

 

 




