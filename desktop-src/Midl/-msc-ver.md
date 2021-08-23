---
title: opção/msc_ver
description: A \_ opção/MSC ver é usada para permitir que MIDL gere código que inclui otimizações para versões diferentes de compiladores do Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver MIDL do comutador
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f010224e5339ef89e05d1d96630dbedc0cb453eb8dafb4dd5e9c6edb3c24cc00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811366"
---
# <a name="msc_ver-switch"></a>\_opção/MSC ver

A opção **/MSC \_ Ver** é usada para permitir que MIDL gere código que inclui otimizações para versões diferentes de compiladores do Microsoft C/C++.

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*número de versão \_* 
</dt> <dd>

especifica um número de versão de inteiro do compilador de Microsoft Visual C++ que será usado para compilar os stubs de cliente e de servidor do aplicativo distribuído. O número de versão padrão é 1100, que corresponde a Visual C++ versão 5,0. O número de versão 1200 corresponde a Visual C++ versão 6,0 e assim por diante.

</dd> </dl>

## <a name="remarks"></a>Comentários

Em particular, os valores de versão de 1100 ou superior fazem com que o compilador MIDL gere código utilizando a diretiva **\_ \_ declspec (UUID ())** . Ele também ativa macros que usam as diretivas **\_ \_ declspec (selectany)** e **\_ \_ declspec (novtable)** .

 

 




