---
title: Gerando UUIDs de interface
description: Gerando UUIDs (identificadores exclusivos universal) de interface e usando Uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635803"
---
# <a name="generating-interface-uuids"></a>Gerando UUIDs de interface

Esta seção apresenta informações sobre identificadores exclusivos universais (UUIDs) e o utilitário Uuidgen nos seguintes tópicos:

-   [O que é um UUID?](#what-is-a-uuid)
-   [Usando Uuidgen](#using-uuidgen)

## <a name="what-is-a-uuid"></a>O que é um UUID?

Todas as interfaces devem ser identificadas exclusivamente em uma rede para que os clientes possam encontrá-las. Em redes pequenas, o nome da interface sozinha pode ser suficiente para identificá-la. No entanto, isso geralmente não é viável em redes grandes. Portanto, os desenvolvedores normalmente atribuem um identificador exclusivo universal (UUID, intercambiável com o termo GUID ou identificador global exclusivo) para cada interface. Um UUID é uma cadeia de caracteres que contém um conjunto de dígitos hexadecimais. Cada interface tem um UUID diferente. Para obter detalhes, consulte [UUID de cadeia de caracteres](string-uuid.md).

A representação textual de um UUID é uma cadeia de caracteres que consiste em 8 dígitos hexadecimais seguidos por um hífen, seguido por três grupos separados por hífen de 4 dígitos hexadecimais, seguidos por um hífen, seguido por 12 dígitos hexadecimais. O exemplo a seguir é uma cadeia de caracteres UUID válida:

ba209999-0c6c-11d2-97cf-00c04f8eea45

Os UUIDs vazios são referidos como UUIDs Nil em vez de UUIDs **nulos** . O termo nil indica qualquer coisa que seja zero, em branco, vazio ou não inicializado. Uma cadeia de caracteres vazia, um registro de banco de dados vazio ou um UUID não inicializado são exemplos de valores nulos.

> [!Note]  
> O valor **NULL** é o valor especificado zero. Ele é frequentemente usado em programação C e C++ em conjunto com ponteiros. Nil é um termo mais geral do que **NULL**. Os UUIDs de interface de objeto não inicializados sempre devem ser chamados de UUIDs **nulos** em vez de UUIDs NULL.

 

## <a name="using-uuidgen"></a>Usando Uuidgen

A Microsoft fornece um programa utilitário chamado Uuidgen para gerar os UUIDs. O utilitário Uuidgen gera o UUID no formato de arquivo IDL ou no formato C-Language.

Ao executar o utilitário Uuidgen na linha de comando, você pode usar as seguintes opções de comando.



| Comutador Uuidgen           | Description                                                                |
|--------------------------|----------------------------------------------------------------------------|
| **/I**                   | Gera UUID para um modelo de interface IDL.                                 |
| **/s**                   | Gera UUID como uma estrutura C inicializada.                                |
| **/o** < *nome do arquivo*> | Redireciona a saída para um arquivo; especificado imediatamente após a opção **/o** . |
| **/n** < *número* de>   | Especifica o número de UUIDs a serem gerados.                                 |
| **/v**                   | Exibe informações de versão sobre Uuidgen.                                |
| **/h** ou **?**          | Exibe o resumo da opção de comando.                                           |



 

Normalmente, você usará o utilitário Uuidgen, conforme mostrado no exemplo a seguir.

**Uuidgen-i-oMyApp. idl**

Esse comando gera um UUID e o armazena em um arquivo MIDL que você pode usar como modelo. Quando o comando anterior é executado, o conteúdo de MyApp. idl é semelhante ao seguinte:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

A próxima etapa seria substituir o nome do espaço reservado, INTERFACENAME, pelo nome real da sua interface.

 

 




