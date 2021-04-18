---
title: Recurso de CURSOR
description: Define um bitmap que define a forma do cursor na tela de exibição ou um cursor animado.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Menus de recursos de CURSOR e outros recursos
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758708"
---
# <a name="cursor-resource"></a>Recurso de CURSOR

Define um bitmap que define a forma do cursor na tela de exibição ou um cursor animado.

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um inteiro de 16 bits sem sinal identificando o recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Nome do arquivo que contém o recurso. O nome deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual. O caminho deve ser uma cadeia de caracteres entre aspas.

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="remarks"></a>Comentários

Os recursos de ícone e cursor podem conter mais de uma imagem.

## <a name="examples"></a>Exemplos

O exemplo a seguir define dois recursos de cursor; um por nome (cursor1) e o outro por número (2):

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando cursores](./using-cursors.md)
</dt> </dl>

 

 