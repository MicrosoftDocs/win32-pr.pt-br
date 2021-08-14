---
title: Opção /acf
description: A opção /acf permite que o usuário fornece um nome de arquivo ACF explícito. A opção também permite o uso de nomes de interface diferentes nos arquivos IDL e ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /acf switch MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37248ac346350f618eebc5ca81af144ecee91ce2acf40c39b9e980b574df4764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386123"
---
# <a name="acf-switch"></a>Opção /acf

A **opção /acf** permite que o usuário fornece um nome de arquivo ACF explícito. A opção também permite o uso de nomes de interface diferentes nos arquivos IDL e ACF.

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*acf \_ filename* 
</dt> <dd>

Especifica o nome do ACF. O espaço em branco pode ou não estar presente entre a opção **/acf** e o nome do arquivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Por padrão, o compilador MIDL constrói o nome do ACF substituindo a extensão de nome de arquivo IDL (geralmente .idl) por .acf. Quando a **opção /acf** está presente, o ACF recebe seu nome do nome de arquivo especificado. A **opção /acf** se aplica somente ao arquivo IDL especificado na linha de comando do compilador MIDL. Ele não se aplica a arquivos importados.

Quando a **opção /acf** é usada, o nome da interface no ACF não precisa corresponder ao nome da interface MIDL. Esse recurso permite que as interfaces compartilhem uma especificação do ACF.

Quando um caminho absoluto para um ACF não é especificado, o compilador MIDL pesquisa no diretório atual, diretórios fornecidos pela opção [**/I**](-i.md) e diretórios no caminho INCLUDE.

Se o ACF não for encontrado, o compilador MIDL assumirá que não há ACF para essa interface. Para obter mais informações sobre a sequência de diretórios, consulte as entradas de referência para as opções [**/I**](-i.md) e [**/no \_ def \_ idir.**](-no-def-idir.md) Para obter mais informações relacionadas **ao arquivo /acf**, consulte [Arquivo de IDL (Definição de Interface).](interface-definition-idl-file.md)

## <a name="examples"></a>Exemplos

**midl /acf bar.acf filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/i**](-i.md)
</dt> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




