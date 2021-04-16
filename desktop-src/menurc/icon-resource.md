---
title: Recurso de ícone
description: Define um bitmap que define a forma do ícone a ser usado para um determinado aplicativo ou um ícone animado.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- ÍCONE de menus de recursos e outros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499026"
---
# <a name="icon-resource"></a>Recurso de ícone

Define um bitmap que define a forma do ícone a ser usado para um determinado aplicativo ou um ícone animado.

``` syntax
nameID ICON filename
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Nome do arquivo que contém o recurso. O nome deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual. O caminho deve ser uma cadeia de caracteres entre aspas.

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="remarks"></a>Comentários

Os recursos de ícone e cursor podem conter mais de uma imagem.

## <a name="examples"></a>Exemplos

O exemplo a seguir define dois recursos de ícone:

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando ícones](./using-icons.md)
</dt> </dl>

 

 