---
title: Requisitos de pré-processador do C para MIDL
description: Esta página se aplica somente a desenvolvedores que têm motivos específicos para substituir o pré-processador do Microsoft C/C++ como o pré-processador usado pelo MIDL ou para os desenvolvedores que devem especificar comutadores de pré-processador personalizados.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL do compilador MIDL, pré-processador, requisitos
- C-pré-processador MIDL, requisitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ed109c9febe4ead697e2c773f4e45d9af78abdf20bed99400a011ef12294b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807690"
---
# <a name="c-preprocessor-requirements-for-midl"></a>Requisitos de pré-processador do C para MIDL

Esta página se aplica somente a desenvolvedores que têm motivos específicos para substituir o pré-processador do Microsoft C/C++ como o pré-processador usado pelo MIDL ou para os desenvolvedores que devem especificar comutadores de pré-processador personalizados. O MIDL alterna [**/cpp \_ cmd**](-cpp-cmd.md), [**/cpp \_ opt**](-cpp-opt.md)e [**// \_ ///////////////////////**](-no-cpp-nocpp.md) Normalmente, não há motivo para substituir o pré-processador do Microsoft C/C++, nem para especificar comutadores de pré-processador personalizados.

O compilador MIDL usa um pré-processador C durante o processamento inicial do arquivo IDL. O ambiente de compilação usado durante a compilação dos arquivos IDL é associado a um pré-processador C/C++ padrão. Se um pré-processador diferente for usado, o compilador MIDL switch [**/cpp \_ cmd**](-cpp-cmd.md) permitirá uma substituição do nome padrão C/C++-preprocessador:

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*nome do pré-processador \_*
</dt> <dd>

Especifica o nome do pré-processador a ser usado pelo MIDL. Pode ser especificado com um caminho para o binário. A extensão de .exe é opcional.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Especifica o nome do arquivo IDL.

</dd> </dl>

-   O compilador MIDL espera que qualquer pré-processador Observe as seguintes convenções:
-   O arquivo de entrada é especificado como o último argumento na linha de comando.
-   O pré-processador deve redirecionar a saída para o dispositivo de saída padrão, stdout.
-   No fluxo de saída do pré-processador, as diretivas de **\# linha** estão presentes para habilitar melhores mensagens de diagnóstico.
-   As diretivas de linha são as únicas diretivas de pré-processador no fluxo de saída.

O MIDL pressupõe que o pré-processador gerado removeu todas as diretivas de pré-processador do fluxo de entrada do compilador, com exceção das ocorrências da diretiva de linha necessária para indicar o local de origem nas mensagens do compilador. Ao indicar um pré-processador diferente do pré-processador do Microsoft C/C++, ou ao especificar opções de pré-processador com a opção [**/cpp \_ opt**](-cpp-opt.md) , a especificação de uma opção de pré-processador apropriada que coloca as diretivas de linha no fluxo de entrada do compilador é necessária. Por exemplo, para o pré-processador do Microsoft C/C++, a opção **/e** teria que ser usada:

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

A diretiva de **\# linha** é aceita pelo MIDL em um dos seguintes formatos:

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

Para obter uma descrição completa da diretiva de linha e outras diretivas de pré-processador, consulte a documentação do compilador C que está sendo usado.

MIDL aceita apenas a diretiva de pré-processador de linha. Portanto, se a opção de [**\_ cpp de///**](-no-cpp-nocpp.md) não tiver sido usada, o arquivo de entrada não deverá ter outras diretivas de pré-processador ou o arquivo de entrada deverá ter sido processado antes de invocar MIDL.

Para obter mais informações, consulte [lidando com as \# definições em arquivos IDL](dealing-with-defines-in-idl-files-2.md).

 

 




