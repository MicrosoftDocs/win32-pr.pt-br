---
title: Opção/i
description: A opção/I especifica os diretórios a serem pesquisados em busca de arquivos IDL importados, arquivos de cabeçalho incluídos e arquivos ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I alternar MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fa167ea2ef95074d201ff460eb8eece79e43442a35985921c97455f086b46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992333"
---
# <a name="i-switch"></a>Opção/i

A opção **/i** especifica os diretórios a serem pesquisados em busca de arquivos IDL importados, arquivos de cabeçalho incluídos e arquivos ACF.

``` syntax
midl /I include_path
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*caminho de inclusão \_* 
</dt> <dd>

Especifica um ou mais diretórios que contêm arquivos de importação, inclusão e ACF. O espaço em branco entre a opção **/i** e o *\_ caminho de inclusão* é opcional. Separe vários diretórios com um caractere de ponto-e-vírgula (;).

</dd> </dl>

## <a name="remarks"></a>Comentários

Mais de um diretório pode aparecer com cada opção **/i** e mais de uma opção **/i** pode aparecer com cada invocação de compilador de MIDL. Os diretórios são pesquisados na ordem em que são especificados.

A configuração da opção **/i** também é passada pelo compilador MIDL para o pré-processador c do compilador c. Quando a [**opção \_ /cpp cmd**](-cpp-cmd.md) está presente e a opção de [**/cpp \_ opt**](-cpp-opt.md) não é, o compilador MIDL concatena a cadeia de caracteres especificada pela opção **\_ cmd/cpp** com as opções **/i**, [**/d**](-d.md)e [**/U**](-u.md) e usa essa cadeia de caracteres concatenada para invocar o pré-processador C para cada arquivo de origem IDL e ACF. A opção de compilador de MIDL **/i** não é passada para o pré-processador quando o parâmetro de compilador MIDL switch/ **/cpp \_ opt** é especificado. **\_**

em ambientes de sistema operacional da Microsoft (64 bits Windows, 32 bits Windows, Windows de 16 bits e MS-DOS), os diretórios são pesquisados na seguinte sequência:

1.  Diretório atual
2.  Diretórios especificados pela opção **/i** (na ordem em que seguem a opção)
3.  Diretórios especificados pela variável de ambiente INCLUDE

Quando os diretórios são especificados com a opção **/i** , a opção de [**\_ \_ Idir**](-no-def-idir.md) de chave de alteração instrui o compilador MIDL a ignorar o diretório atual, ignorar os diretórios especificados pela variável de ambiente include e Pesquisar apenas os diretórios especificados.

Quando nenhum diretório é especificado com a opção **/i** , a opção de [**\_ \_ Idir de//**](-no-def-idir.md) chave de alteração instrui o compilador MIDL a pesquisar somente o diretório atual.

## <a name="examples"></a>Exemplos

**MIDL/I c: \\ include; c: \\ include \\ h/i \\ include2 filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ aceitar**](-cpp-opt.md)
</dt> <dt>

[**/. de \_ \_ Idir def**](-no-def-idir.md)
</dt> </dl>

 

 




