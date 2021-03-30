---
title: opção/cpp_cmd
description: A \_ opção cmd/cpp especifica o pré-processador que o compilador MIDL usa para pré-processar arquivos de entrada.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd MIDL do comutador
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638634"
---
# <a name="cpp_cmd-switch"></a>\_opção/cpp cmd

A **opção \_ cmd/cpp** especifica o pré-processador que o compilador MIDL usa para pré-processar arquivos de entrada.

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*\_Binário de pré-processador C \_* 
</dt> <dd>

Especifica o comando que invoca o pré-processador. Esse comando permite que os desenvolvedores substituam o pré-processador padrão. Por padrão, o MIDL invoca o compilador C/C++ da Microsoft do ambiente de compilação da máquina de compilação.

</dd> </dl>

## <a name="remarks"></a>Comentários

O *argumento \_ \_ binário de pré-processador C* para a opção pode especificar o caminho completo; o sufixo exe e as aspas são opcionais. Normalmente, os desenvolvedores usam a opção para escolher uma versão específica do pré-processador do Microsoft C/C++ ou equivalente no ambiente de compilação. Nesse caso, não é necessário usar a opção [**/cpp \_ opt**](-cpp-opt.md) com **/cpp \_ cmd**.

Ao usar um pré-processador que não seja da Microsoft, especialmente quando o pré-processador especificado não direciona sua saída para stdout, a opção de compilador C que redireciona a saída para stdout como parte da opção [**/cpp \_ opt**](-cpp-opt.md) do compilador MIDL deve ser especificada. Consulte [requisitos do pré-processador do C para MIDL](c-preprocessor-requirements-for-midl.md) para obter detalhes

O pré-processador é invocado por uma cadeia de caracteres de comando que é formada pelas informações fornecidas ao compilador MIDL **por/cpp \_ cmd**, [**/cpp \_ opt**](-cpp-opt.md), [**/d**](-d.md), [**/i**](-i.md)e [**/u**](-u.md) opções. A tabela a seguir resume como a cadeia de caracteres de comando é construída para cada combinação de **/cpp \_ cmd** e **/cpp \_ opt** switches.

Quando a opção **/cpp \_ cmd** não é especificada, o compilador MIDL invoca o compilador do Microsoft C/C++. MIDL usa um binário Cl.exe encontrado no ambiente de compilação.

Quando a opção [**/cpp \_ opt**](-cpp-opt.md) não está presente, o compilador MIDL concatena a cadeia de caracteres especificada pela **opção/cpp \_ cmd** com as informações especificadas pelas opções MIDL [**/i**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) . A cadeia de caracteres/E também é concatenada à cadeia de caracteres de invocação do compilador C para indicar que o compilador C/C++ deve executar o pré-processamento apenas. A opção [**/nologo**](-nologo.md) é adicionada para suprimir a faixa do compilador C/C++. O compilador MIDL usa a cadeia de caracteres concatenada para invocar o pré-processador C para IDL de nível superior, bem como arquivos IDL importados, e também para quaisquer arquivos ACF presentes correspondentes.

Quando a opção [**/cpp \_ opt**](-cpp-opt.md) está presente, o que deve ser um caso raro para as plataformas atuais de 32 bits e 64 bits, o compilador MIDL concatena a cadeia de caracteres especificada pela **opção \_ cmd/cpp** com a cadeia de caracteres especificada pela opção **\_ opcional/cpp** . O compilador MIDL usa a cadeia de caracteres concatenada para invocar o binário do pré-processador indicado no lugar do pré-processador padrão. Quando a **opção/cpp \_ opt** está presente, nem as opções do compilador MIDL especificadas pelas comutações [**/I**](-i.md), [**/d**](-d.md)e [**/u**](-u.md) nem o switch do compilador C/e são concatenados com a cadeia de caracteres. Você deve fornecer a opção/E, ou equivalente, como parte da cadeia de caracteres.



| /cpp \_ cmd presente? | a \_ opção/cpp está presente? | Description                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Não (padrão)       | Não (padrão)       | Invoca o compilador padrão do Microsoft C/C++ com as configurações obtidas nas opções MIDL [**/i**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) . Adiciona os comutadores de pré-processador/E e [**/nologo**](-nologo.md). |
| Sim                | Não                 | Invoca o binário de pré-processador indicado com os mesmos comutadores acima.                                                                                                                                        |
| Não                 | Sim                | Invoca o compilador C da Microsoft com opções especificadas. Não usa MIDL [**/i**](-i.md), [**/d**](-d.md), [**/u**](-u.md) opções. Você deve fornecer/E como parte da [**/cpp \_ opt**](-cpp-opt.md).             |
| Sim                | Sim                | Invoca o binário do pré-processador especificado somente com as opções especificadas. Você deve usar aspas.                                                                                                                       |



 

## <a name="examples"></a>Exemplos

**MIDL/cpp \_ cmd d: \\ NT \\ Tools \\ IA64 \\cl.exe/DFLAG = true/IC: \\ Inc filename. idl**

**MIDL/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc filename. idl**

**MIDL/cpp \_ opt "/E/DFLAG = true/IC: \\ Inc" filename. idl**

**MIDL/cpp \_ cmd "CL"/cpp \_ opt "/e/DFLAG = true/IC: \\ Inc" filename. idl**

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ aceitar**](-cpp-opt.md)
</dt> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**///// \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[Requisitos de pré-processador do C para MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




