---
title: Cadeias de caracteres de formato
description: Uma cadeia de caracteres de formato é um token interpretado que o mecanismo de NDR entende. Cadeias de caracteres de formato geralmente são conhecidas como MOPs; esta documentação usa o termo cadeia de caracteres de formato.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8c14fa649e71411c5706193e83fd9a09d30f8a0c57fec411d8c34fef675ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929863"
---
# <a name="format-strings"></a>Cadeias de caracteres de formato

Uma cadeia de caracteres de formato é um token interpretado que o mecanismo de NDR entende. Cadeias de caracteres de formato geralmente são conhecidas como MOPs; esta documentação usa o termo cadeia de caracteres de formato.

Para ser mais preciso, um caractere de formato é um token interpretável individual (atômico). Cada caractere de formato tem um byte de tamanho. Uma cadeia de caracteres de formato é uma sequência de caracteres de formato ou caracteres de formato e dados numéricos. O termo descritor também é usado para nomear sequências comuns; por exemplo, uma cadeia de caracteres de formato de parâmetro ou um descritor de parâmetro é uma cadeia de caracteres de formato usada para descrever um parâmetro de uma rotina.

Os caracteres de formato têm nomes simbólicos sugestivos, como FC \_ LONG ou FC \_ STRUCT. Todos os caracteres de cadeia de caracteres de formato usados por MIDL e o mecanismo NDR são definidos no arquivo Ndrtypes.h.

## <a name="format-string-tables"></a>Formatar tabelas de cadeia de caracteres

Duas tabelas de cadeia de caracteres de formato primário são usadas pelo mecanismo: a tabela de cadeia de caracteres de formato de procedimento, **\_ \_ MIDL \_ ProcFormatString**, que mantém os descritores de procedimento; e a tabela de cadeia de caracteres de formato de **\_ \_ tipo, \_ MIDL TypeFormatString**, que mantém os descritores de tipo de dados. O compilador gera ambos nos arquivos stub principais ( \* \_ c.c, \* \_ s.c, \* \_ p.c). A tabela de cadeia de caracteres de formato de procedimento é usada principalmente por vários interpretadores, mas também é usada para a conversão de buffer, independentemente do modo do compilador. A tabela de cadeia de caracteres de formato de tipo é usada ao chamar o mecanismo NDR principal para indicar tipos de dados específicos nos quais trabalhar.

## <a name="format-string-notation"></a>Notação de cadeia de caracteres de formato

A notação usada neste documento segue as diretrizes comuns de descrição de programação, com uma barra ( ) usada para denotar constructos alternativos e colchetes ( ) usados para indicar elementos \| \[ \] opcionais. Cadeias de caracteres de formato são frequentemente empilhadas para responsabilidade (responsabilidade). Ao longo deste documento, o FC denota um caractere de formato único. Os caracteres de formato são apresentados em todos os CAPS, usando seus nomes simbólicos reais. Outros campos arbitrários são representados por um nome e um tamanho.

Colchetes angulares ( <> ) são usados para denotar tamanhos dos descritores. As convenções mostradas na tabela a seguir são empregadas.



| Notation     | Significado                                                   |
|--------------|-----------------------------------------------------------|
| <*N*>  | O tamanho do descritor é n bytes.                        |
| <>     | O tamanho do descritor varia.                            |
| {<>}\* | O descritor é repetido qualquer número de vezes (0,1,2...). |



 

Os caracteres de formato a seguir têm um significado especial.



| Caractere | Significado                                   |
|-----------|-------------------------------------------|
| FC \_ END   | Indica o final de algumas cadeias de caracteres de formato. |
| FC \_ PAD   | Caractere de painel não interpretado.              |



 

 

 




