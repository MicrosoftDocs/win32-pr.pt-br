---
title: /cpp_opt switch
description: A opção /cpp \_ opt especifica opções para passar para o pré-processador C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt com a opção MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3b7845feb36cd09d96fc64cb7397e4daf001957f6ce7a6f5e797707caafd32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105646"
---
# <a name="cpp_opt-switch"></a>/cpp \_ opt switch

A **opção /cpp \_ opt** especifica opções para passar para o pré-processador C/C++.

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*Opção \_ de pré-processador \_ C* 
</dt> <dd>

Especifica a opção de linha de comando associada ao pré-processador invocado. 

**Observação:** para os pré-processadores do Microsoft C/C++, você deve fornecer a opção como parte da cadeia de caracteres de opção do `/E` *\_ pré-processador \_ C.* 

Aspas são necessárias quando mais de uma opção é usada e para espaços.

</dd> </dl>

## <a name="remarks"></a>Comentários

Não use essa opção, a menos que haja um motivo específico para fazer isso. Consulte [Requisitos do pré-processador C para MIDL](c-preprocessor-requirements-for-midl.md) para obter informações importantes sobre pré-processamento.

A **opção /cpp \_ opt** pode ser usada com ou sem a opção [**/cpp \_ cmd.**](-cpp-cmd.md) Consulte **/cpp \_ cmd para** obter detalhes de como a linha de comando do pré-processador é construída em ambos os casos.

A **opção /cpp \_ opt,** se especificada, sempre deve incluir `/E` para funcionar corretamente.

## <a name="examples"></a>Exemplos

**midl /cpp \_ cmd d: \\ nt \\ tools \\ ia64 \\cl.exe /DFLAG=TRUE /Ic: \\ inc filename.idl**

**midl /cpp \_ cmd "mycpp" /DFLAG=TRUE /Ic: \\ inc filename.idl**

**midl /cpp \_ opt "/E /DFLAG=TRUE /Ic: \\ inc" filename.idl**

**midl /cpp \_ cmd "cl" /cpp \_ opt "/E /DFLAG=TRUE /Ic: \\ inc" filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[Requisitos do pré-processador C para MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




