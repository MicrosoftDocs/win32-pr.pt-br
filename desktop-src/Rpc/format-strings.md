---
title: Cadeias de caracteres de formato
description: Uma cadeia de caracteres de formato é um token interpretado que o mecanismo de NDR compreende. Cadeias de caracteres de formato costumam ser chamadas de MOPs; Esta documentação usa a cadeia de caracteres de formato de termo em todo o.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636211"
---
# <a name="format-strings"></a>Cadeias de caracteres de formato

Uma cadeia de caracteres de formato é um token interpretado que o mecanismo de NDR compreende. Cadeias de caracteres de formato costumam ser chamadas de MOPs; Esta documentação usa a cadeia de caracteres de formato de termo em todo o.

Para ser mais preciso, um caractere de formato é um token interpretável individual (atômico). Cada caractere de formato tem um byte de tamanho. Uma cadeia de caracteres de formato é uma sequência de caracteres de formato ou caracteres de formato e dados numéricos. O descritor de termo também é usado para nomear sequências comuns; por exemplo, uma cadeia de caracteres de formato de parâmetro ou um descritor de parâmetro é uma cadeia de caracteres de formato usada para descrever um parâmetro de uma rotina.

Os caracteres de formato têm nomes simbólicos sugeridos como FC \_ longo ou FC \_ struct. Todos os caracteres de cadeia de formato usados pelo MIDL e pelo mecanismo de NDR são definidos no arquivo Ndrtypes. h.

## <a name="format-string-tables"></a>Formatar tabelas de cadeia de caracteres

Duas tabelas de cadeia de caracteres de formato primário são usadas pelo mecanismo: a tabela de cadeia de caracteres de formato de procedimento, **\_ \_ MIDL \_ ProcFormatString**, que mantém os descritores de procedimento; e a tabela de cadeia de caracteres de formato de tipo, **\_ \_ MIDL \_ TypeFormatString**, que mantém os descritores de tipo de dados. O compilador gera ambos os arquivos stub principais ( \* \_ c. c, \* \_ s. c, \* \_ p. c). A tabela de cadeia de caracteres de formato de procedimento é usada principalmente por vários interpretadores, mas também é usada para a conversão de buffer, independentemente do modo de compilador. A tabela de cadeia de caracteres de formato de tipo é usada ao chamar o mecanismo de NDR principal para indicar os tipos de dados específicos nos quais trabalhar.

## <a name="format-string-notation"></a>Formatar notação de cadeia de caracteres

A notação usada neste documento segue as diretrizes de descrição de programação comuns, com uma barra ( \| ) usada para denotar construções alternativas e colchetes ( \[ \] ) usados para indicar elementos opcionais. As cadeias de caracteres de formato são frequentemente empilhadas para facilitar a leitura (responsabilidade). Em todo este documento, o FC denota um único caractere de formato. Os caracteres de formato são apresentados em todos os limites, usando seus nomes simbólicos reais. Outros campos arbitrários são representados por um nome e um tamanho.

Os colchetes angulares ( <> ) são usados para denotar os tamanhos dos descritores. As convenções mostradas na tabela a seguir são empregadas.



| Notation     | Significado                                                   |
|--------------|-----------------------------------------------------------|
| <*p*>  | O tamanho do descritor é n bytes.                        |
| <>     | O tamanho do descritor varia.                            |
| {<>}\* | O descritor é repetido qualquer número de vezes (0, 1, 2...). |



 

Os caracteres de formato a seguir têm um significado especial.



| Caractere | Significado                                   |
|-----------|-------------------------------------------|
| extremidade de FC \_   | Indica o fim de algumas cadeias de caracteres de formato. |
| Pad do FC \_   | Caractere de preenchimento não interpretado.              |



 

 

 




