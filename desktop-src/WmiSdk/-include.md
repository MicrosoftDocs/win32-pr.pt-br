---
description: Inclui o conteúdo de um arquivo MOF em outro arquivo MOF.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b7577639bd215fc051c2f1303e74fe946341a31c4b6708f881c3c9fabae2372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557769"
---
# <a name="include"></a>' #include '
/* Título: MyMof. mof                           *//*   title: MyMof2. mof */

O \# comando incluir pré-processador inclui o conteúdo de um arquivo MOF em outro arquivo MOF. O exemplo de código a seguir descreve a sintaxe para o \# comando include.

``` syntax
#include ("Moffile.mof")
```

No exemplo anterior, Moffile. mof é o nome do arquivo MOF a ser incluído.

O exemplo a seguir mostra dois arquivos MOF. Quando você compila o primeiro arquivo MOF, o compilador compila automaticamente o segundo arquivo MOF (Mymof2. MOF) no local em que você coloca a \# instrução include.

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

O seguinte arquivo MOF está incluído no exemplo anterior:

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 



