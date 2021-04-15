---
title: atributo importlib
description: A diretiva \ importlib \ torna os tipos que já foram compilados em outra biblioteca de tipos disponíveis para a biblioteca de tipos que está sendo criada.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- importlib do atributo MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453977"
---
# <a name="importlib-attribute"></a>atributo importlib

A diretiva **\[ importlib \]** torna os tipos que já foram compilados em outra biblioteca de tipos disponíveis para a biblioteca de tipos que está sendo criada.

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

*biblioteca-atributos* 
</dt> <dd>

Zero ou mais atributos que serão aplicados à biblioteca.

</dd> <dt>

*nome da biblioteca* 
</dt> <dd>

O identificador que os componentes de software usarão para denotar essa [**biblioteca**](library.md).

</dd> <dt>

*arquivo a ser importado* 
</dt> <dd>

O nome e o local do arquivo importado em tempo de compilação de MIDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todas as diretivas **\[ importlib \]** devem preceder as outras descrições de tipo na biblioteca. Observe que a biblioteca importada, bem como a biblioteca gerada, deve ser distribuída com o aplicativo para que esteja disponível em tempo de execução.

Na maioria dos casos, você deve usar a diretiva de **\[** [**importação**](import.md) MIDL **\]** para fazer referência a definições de outro. Arquivo IDL em seu. Arquivo IDL. Esse método fornece a biblioteca de tipos com todas as informações do arquivo original, enquanto **\[ importlib \]** só traz o conteúdo da biblioteca de tipos.

> [!Note]  
> A diretiva **\[ importlib \]** torna qualquer tipo definido na biblioteca importada acessível de dentro da biblioteca que está sendo compilada. Para evitar ambigüidade quando houver referências duplicadas, recomendamos qualificar cada referência desse tipo com o nome de biblioteca apropriado, da seguinte maneira:

 

``` syntax
library_name.type
```

Na ausência de tal qualificação, o MIDL resolve a ambiguidade de referência duplicada da seguinte maneira:

-   Em vigor com a versão 3,1, MIDL usa a primeira referência encontrada.
-   A versão 3,0 do MIDL, a primeira versão do MIDL que poderia gerar bibliotecas de tipos, usa a última referência encontrada.

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

[**biblioteca**](library.md)
</dt> <dt>

[**importe**](import.md)
</dt> <dt>

[Importar arquivos de cabeçalho do sistema](importing-system-header-files.md)
</dt> <dt>

[Importando arquivos e bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 