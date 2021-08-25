---
title: atributo importlib
description: A diretiva \ importlib\ disponibiliza os tipos que já foram compilados em outra biblioteca de tipos para a biblioteca de tipos que está sendo criada.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- atributo importlib MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d5c4b19800f92e3080d3fb435ddd20d62e4b6fe76986869a0f4da86deabcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895066"
---
# <a name="importlib-attribute"></a>atributo importlib

A **\[ diretiva \] importlib** disponibiliza tipos que já foram compilados em outra biblioteca de tipos para a biblioteca de tipos que está sendo criada.

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*library-attributes* 
</dt> <dd>

Zero ou mais atributos que serão aplicados à biblioteca.

</dd> <dt>

*nome da biblioteca* 
</dt> <dd>

O identificador que os componentes de software usarão para denotar essa [**biblioteca**](library.md).

</dd> <dt>

*arquivo a ser importado* 
</dt> <dd>

O nome e o local do arquivo importado no tempo de compilação MIDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todas **\[ as \] diretivas importlib** devem preceder as outras descrições de tipo na biblioteca. Observe que a biblioteca importada, bem como a biblioteca gerada, deve ser distribuída com o aplicativo para que ela seja disponibilizada em tempo de executar.

Na maioria dos casos, você deve usar a diretiva de importação MIDL **\[** [](import.md) **\]** para referenciar definições de outro . Arquivo IDL em seu . Arquivo IDL. Esse método fornece à biblioteca de tipos todas as informações do arquivo original, enquanto **\[ importlib \]** apenas traz o conteúdo da biblioteca de tipos.

> [!Note]  
> A **\[ diretiva \] importlib** torna qualquer tipo definido na biblioteca importada acessível de dentro da biblioteca que está sendo compilada. Para evitar ambiguidade quando há referências duplicadas, recomendamos qualificar cada referência com o nome apropriado da biblioteca, da seguinte maneira:

 

``` syntax
library_name.type
```

Na ausência dessa qualificação, o MIDL resolve a ambiguidade de referência duplicada da seguinte forma:

-   Em vigor com a versão 3.1, o MIDL usa a primeira referência que encontra.
-   A versão 3.0 do MIDL, a primeira versão do MIDL que pode gerar bibliotecas de tipos, usa a última referência encontrada.

## <a name="examples"></a>Exemplos

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[**Importação**](import.md)
</dt> <dt>

[Importar arquivos de cabeçalho do sistema](importing-system-header-files.md)
</dt> <dt>

[Importando arquivos e bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 