---
title: comutador/ACF
description: A opção/ACF permite que o usuário forneça um nome de arquivo ACF explícito. A opção também permite o uso de nomes de interface diferentes nos arquivos IDL e ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- MIDL do comutador/ACF
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916797"
---
# <a name="acf-switch"></a>comutador/ACF

A opção **/ACF** permite que o usuário forneça um nome de arquivo ACF explícito. A opção também permite o uso de nomes de interface diferentes nos arquivos IDL e ACF.

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*\_nome de arquivo ACF* 
</dt> <dd>

Especifica o nome do ACF. O espaço em branco pode ou não estar presente entre o comutador **/ACF** e o nome do arquivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Por padrão, o compilador MIDL constrói o nome do ACF substituindo a extensão de nome de arquivo IDL (normalmente. idl) por. ACF. Quando a opção **/ACF** está presente, o ACF pega seu nome do nome de arquivo especificado. A opção **/ACF** se aplica somente ao arquivo IDL especificado na linha de comando do compilador MIDL. Ele não se aplica a arquivos importados.

Quando a opção **/ACF** é usada, o nome da interface no ACF não precisa corresponder ao nome da interface MIDL. Esse recurso permite que as interfaces compartilhem uma especificação ACF.

Quando um caminho absoluto para um ACF não é especificado, o compilador MIDL pesquisa no diretório atual, nos diretórios fornecidos pela opção [**/i**](-i.md) e nos diretórios no caminho de inclusão.

Se o ACF não for encontrado, o compilador MIDL pressupõe que não há um ACF para essa interface. Para obter mais informações sobre a sequência de diretórios, consulte as entradas de referência para as opções [**/i**](-i.md) e [**/. \_ \_ Idir def**](-no-def-idir.md) . Para obter mais informações relacionadas ao **/ACF**, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Exemplos

**MIDL/ACF bar. ACF filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/I**](-i.md)
</dt> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/. de \_ \_ Idir def**](-no-def-idir.md)
</dt> </dl>

 

 




