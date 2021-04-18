---
description: O compilador formato MOF (MOF) dá suporte a dois estilos de comentário usando dois estilos diferentes de delimitadores de comentário.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Criando um comentário
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788759"
---
# <a name="creating-a-comment"></a>Criando um comentário

O compilador formato MOF (MOF) dá suporte a dois estilos de comentário usando dois estilos diferentes de delimitadores de comentário.

A tabela a seguir lista os delimitadores que são usados para comentários e o efeito que os delimitadores têm no código.



| Delimitador   | Marcas                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | Início de um comentário que termina no final da linha.                                    |
| /\* e \*/ | Início e fim de um comentário que pode abranger várias linhas ou apenas uma parte de uma linha. |



 

Como nas linguagens de programação C e C++, você deve usar o delimitador//somente com comentários de linha única, mas usar os delimitadores/ \* e \* /com comentários de linha única ou de várias linhas.

O exemplo de código a seguir descreve os dois estilos de delimitador.

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



