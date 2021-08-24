---
title: Exibir. scriptfile
description: o atributo scriptfile especifica os nomes de arquivo que acompanham JScript arquivos.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- Windows Media Player VIEW. scriptfile
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f22b0fb5f0815c8977a363c033d26c0d68f725e0cdcd546bc2f2c1a7b723c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615326"
---
# <a name="viewscriptfile"></a>Exibir. scriptfile

o atributo **scriptfile** especifica os nomes de arquivo que acompanham JScript arquivos.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** somente gravação sem valor padrão. os nomes de arquivo de vários arquivos de JScript são delimitados por ponto-e-vírgula. Os espaços e pontos e vírgulas iniciais e seguintes não devem estar presentes.

## <a name="remarks"></a>Comentários

O código nos arquivos especificados pode ser usado por qualquer manipulador de eventos na exibição. O código usado por manipuladores de eventos em várias exibições pode ser colocado em um arquivo com o mesmo nome do arquivo de definição de capa, mas com uma extensão de .js em vez de uma extensão. WMS. Esse arquivo é carregado automaticamente e não precisa ser especificado no arquivo de definição de capa.

## <a name="examples"></a>Exemplos


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 





