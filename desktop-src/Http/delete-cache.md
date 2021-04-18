---
title: delete cache
description: Libera o cache de URL inteiro ou exclui as entradas de acordo com a URL especificada.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- Excluir cache HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "105767652"
---
# <a name="delete-cache"></a>delete cache

Libera o cache de URL inteiro ou exclui as entradas de acordo com a URL especificada.

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[URL = \] * * * cadeia de caracteres*
</dt> <dd>

Obrigatórios. Especifica a URL totalmente qualificada.

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursivo = \] {Yes \| no}**
</dt> <dd>

Em caso afirmativo, remove todas as entradas na URL especificada.

</dd> </dl>

## <a name="examples"></a>Exemplos

**excluir URL do cache = https://www.contoso.com:80/myresource/ recursivo = Sim**

 

 




