---
title: opção/cpp_opt
description: A \_ opção/cpp opt especifica opções a serem passadas para o pré-processador do C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt MIDL do comutador
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104368989"
---
# <a name="cpp_opt-switch"></a>\_comutador opcional/cpp

A opção **/cpp \_ opt** especifica opções a serem passadas para o pré-processador do C/C++.

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*\_Opção de pré-processador C \_* 
</dt> <dd>

Especifica a opção de linha de comando associada ao pré-processador invocado. 

**Observação**: para os pré-processadores Microsoft c/C++, você deve fornecer o `/E` comutador como parte da cadeia de caracteres da *\_ \_ opção de pré-processador C* . 

As aspas são necessárias quando mais de uma opção é usada e para espaços.

</dd> </dl>

## <a name="remarks"></a>Comentários

Não use essa opção, a menos que haja um motivo específico para isso. Consulte [requisitos de pré-processador do C para MIDL](c-preprocessor-requirements-for-midl.md) para obter informações importantes sobre o pré-processamento.

A opção **/cpp \_ opt** pode ser usada com ou sem a opção [**\_ cmd do/CPP**](-cpp-cmd.md) . Consulte **/cpp \_ cmd** para obter detalhes de como a linha de comando do pré-processador é construída em ambos os casos.

A opção **/cpp \_ opt** , se especificada, deve sempre incluir `/E` para funcionar corretamente.

## <a name="examples"></a>Exemplos

**MIDL/cpp \_ cmd d: \\ NT \\ Tools \\ IA64 \\cl.exe/DFLAG = true/IC: \\ Inc filename. idl**

**MIDL/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc filename. idl**

**MIDL/cpp \_ opt "/E/DFLAG = true/IC: \\ Inc" filename. idl**

**MIDL/cpp \_ cmd "CL"/cpp \_ opt "/e/DFLAG = true/IC: \\ Inc" filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**///// \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[Requisitos de pré-processador do C para MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




