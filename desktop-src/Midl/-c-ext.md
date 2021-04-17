---
title: opção/c_ext
description: Essa opção é obsoleta a partir da versão 3,0 do compilador MIDL. No entanto, usar a \_ opção c ext não gerará um erro do compilador, portanto, você não precisa remover referências a/MS \_ ext ou/c \_ ext de um makefile existente.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext MIDL do comutador
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105782795"
---
# <a name="c_ext-switch"></a>\_opção/c ext

Essa opção é obsoleta a partir da versão 3,0 do compilador MIDL. No entanto, usar a opção **c \_ ext** não gerará um erro do compilador, portanto, você não precisa remover referências a [**/MS \_ ext**](-ms-ext.md) ou **/c \_ ext** de um makefile existente.

``` syntax
midl /c_ext
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Os recursos a seguir agora estão disponíveis por padrão:

-   Muitos arquivos de cabeçalho existentes definem tipos com qualificadores, como **far** e **stdcall**, que não fazem parte da IDL de DCE. Esses compiladores (e o compilador MIDL no modo de compatibilidade do DCE) geram erros quando tentam processar esses qualificadores. O compilador MIDL permite que você compile arquivos IDL que contenham esses qualificadores. Os qualificadores de tipo não afetam a maneira como os dados são transmitidos na rede.
-   Você pode omitir atributos direcionais como [**\[ in \]**](in.md) ou [**\[ out \]**](out-idl.md).

As seguintes extensões C-Language têm suporte no modo padrão:

-   Campos de bits em estruturas e uniões
-   Comentários que começam com dois caracteres de barra (//)
-   Declarações externas
-   Procedimentos com reticências na lista de parâmetros (...)
-   Em plataformas de 32 bits, [**int**](int.md) é um tipo de base de 32 bits nativo; em plataformas de 16 bits, **int** é reconhecido, mas não é um tipo remoto
-   Tipo [**void \***](void.md) que não é usado em operações remotas
-   Qualificadores de tipo — incluindo o formulário com o prefixo de conformidade com ANSI — contêm dois caracteres de sublinhado: **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **Export**, **\_ \_ Export**, **muito** **\_ \_ longe,** **LOADDS**, **\_ \_ LOADDS**, **Near**, **\_ \_ Near**, **Pascal**, **\_ \_ Pascal**, **stdcall**, **\_ \_ stdcall**, **volátil** e **\_ \_ volátil**.

Para obter mais informações sobre qualificadores de declaração, consulte a documentação do Microsoft C/C++.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**configuração do/App \_**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




