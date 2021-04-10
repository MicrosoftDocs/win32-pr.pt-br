---
description: O compilador MOF aceita um valor de ponto flutuante especificado para uma propriedade de ponto não flutuante. O valor é arredondado para cima ou para baixo e armazenado como um número de ponto não-flutuante. Essa situação pode causar alguns resultados inesperados.
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: Compilando código MOF com valores de Floating-Point
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170617"
---
# <a name="compiling-mof-code-with-floating-point-values"></a>Compilando código MOF com valores de Floating-Point

O compilador MOF aceita um valor de ponto flutuante especificado para uma propriedade de ponto não flutuante. O valor é arredondado para cima ou para baixo e armazenado como um número de ponto não-flutuante. Essa situação pode causar alguns resultados inesperados.

O exemplo de código MOF a seguir define uma classe chamada **ABC** em um namespace chamado "Test". Esse código MOF compila sem erros, mas você não pode consultar o valor de ponto flutuante definido para a propriedade **exampleUint16** na instância que esse código cria.

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

Se você emitir a consulta a seguir, obterá um código de erro que indica uma consulta inválida.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



No entanto, a consulta a seguir localiza a instância indicada.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Compilando arquivos MOF](compiling-mof-files.md)
</dt> <dt>

[**Mofcomp**](mofcomp.md)
</dt> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 



