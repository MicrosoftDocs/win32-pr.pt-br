---
title: Exibir. scriptfile
description: O atributo scriptfile especifica os nomes de arquivo que acompanham arquivos JScript.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- Exibir. scriptfile Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751923"
---
# <a name="viewscriptfile"></a>Exibir. scriptfile

O atributo **scriptfile** especifica os nomes de arquivo que acompanham arquivos JScript.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** somente gravação sem valor padrão. Os nomes de arquivo de vários arquivos JScript são delimitados por ponto-e-vírgula. Os espaços e pontos e vírgulas iniciais e seguintes não devem estar presentes.

## <a name="remarks"></a>Comentários

O código nos arquivos especificados pode ser usado por qualquer manipulador de eventos na exibição. O código usado por manipuladores de eventos em várias exibições pode ser colocado em um arquivo com o mesmo nome do arquivo de definição de capa, mas com uma extensão. js em vez de uma extensão. WMS. Esse arquivo é carregado automaticamente e não precisa ser especificado no arquivo de definição de capa.

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

 

 





