---
title: Recurso MESSAGEtable
description: Define a ID e o arquivo do recurso de tabela de mensagens de um aplicativo. As tabelas de mensagens são recursos de cadeia de caracteres especiais usados no log de eventos e com a função FormatMessage. O arquivo contém uma tabela de mensagens binárias gerada pelo compilador de mensagem, MC.EXE.
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- Menus de recursos do MESSAGEtable e outros recursos
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36281f7f6415465a6741f461574bca29c681cbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640662"
---
# <a name="messagetable-resource"></a>Recurso MESSAGEtable

Define a ID e o arquivo do recurso de tabela de mensagens de um aplicativo. As tabelas de mensagens são recursos de cadeia de caracteres especiais usados no log de eventos e com a função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) . O arquivo contém uma tabela de mensagens binárias gerada pelo compilador de mensagem, MC.EXE.

O compilador de mensagens também gera um arquivo de script de recurso que contém as instruções de **mensagens** que você precisa para incluir os recursos de tabela de mensagens no arquivo de recurso compilado. Use a diretiva [**\# include**](-include.md) para incluir esse script de recurso em seu script de recurso principal.

``` syntax
nameID MESSAGETABLE filename
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Nome do arquivo que contém o recurso. O nome deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual.

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir define um recurso **messagetable** :

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 