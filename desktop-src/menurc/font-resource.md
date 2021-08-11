---
title: Recurso FONT
description: Define um arquivo que contém uma fonte.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Menus de recursos FONT e outros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf08abd68d5d99640435d355609d5647c71116f9fa29c137ba67a311d41f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235268"
---
# <a name="font-resource"></a>Recurso FONT

Define um arquivo que contém uma fonte.

``` syntax
nameID FONT filename
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Valor inteiro sem sinal de 16 bits exclusivo que identifica o recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Nome do arquivo que contém o recurso. O nome deve ser um nome de arquivo válido; ele deverá ser um caminho completo se o arquivo não estiver no diretório de trabalho atual. O caminho deve ser uma cadeia de caracteres entre aspas.

</dd> </dl>

Determinados atributos também têm suporte para compatibilidade com backward. Para obter mais informações, consulte [Common Resource Attributes](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir define um único recurso de fonte:

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




