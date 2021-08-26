---
title: Recurso MESSAGETABLE
description: Define a ID e o arquivo do recurso de tabela de mensagens de um aplicativo. As tabelas de mensagens são recursos de cadeia de caracteres especiais usados no log de eventos e com a função FormatMessage. O arquivo contém uma tabela de mensagens binárias gerada pelo compilador de mensagem, MC.EXE.
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- Menus de recurso MESSAGETABLE e outros recursos
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378860e10ab6da929147e13a8120ee169204276e3c609b20176c22df9de15dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886716"
---
# <a name="messagetable-resource"></a>Recurso MESSAGETABLE

Define a ID e o arquivo do recurso de tabela de mensagens de um aplicativo. As tabelas de mensagens são recursos de cadeia de caracteres especiais usados no log de eventos e com a [**função FormatMessage.**](/windows/desktop/api/winbase/nf-winbase-formatmessage) O arquivo contém uma tabela de mensagens binárias gerada pelo compilador de mensagem, MC.EXE.

O compilador de mensagem também gera um arquivo de script de recurso que contém as instruções **MESSAGETABLE** de que você precisa para incluir os recursos da tabela de mensagens no arquivo de recurso compilado. Use a [**\# diretiva include**](-include.md) para incluir esse script de recurso em seu script de recurso principal.

``` syntax
nameID MESSAGETABLE filename
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Nome do arquivo que contém o recurso. O nome deve ser um nome de arquivo válido; ele deverá ser um caminho completo se o arquivo não estiver no diretório de trabalho atual.

</dd> </dl>

Determinados atributos também têm suporte para compatibilidade com backward. Para obter mais informações, consulte [Common Resource Attributes](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir define um **recurso MESSAGETABLE:**

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> </dl>

 

 