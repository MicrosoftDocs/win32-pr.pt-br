---
title: explicit_handle atributo
description: O atributo \ \_ identificador \ explícito \ ACF especifica que cada procedimento tem, como seu primeiro parâmetro, um identificador primitivo, como um tipo de manipulador \_ t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle do atributo MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105748171"
---
# <a name="explicit_handle-attribute"></a>\_atributo de identificador explícito

O \[ atributo de ACF **\_ identificador explícito** \] especifica que cada procedimento tem, como seu primeiro parâmetro, um identificador primitivo, como um tipo de [**manipulador \_ t**](handle-t.md) .

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando você usa o atributo **\[ \_ identificador \] explícito** , cada procedimento tem um identificador primitivo como seu primeiro parâmetro, mesmo que o arquivo IDL não contenha esse identificador em sua lista de parâmetros. Os protótipos emitidos para o arquivo de cabeçalho e rotinas de stub contêm o parâmetro adicional, e esse parâmetro é usado como o identificador para direcionar a chamada remota.

O atributo **\[ \_ identificador \] explícito** afeta os procedimentos remotos e os procedimentos de serialização. Para a serialização de tipo, as rotinas de suporte são geradas com o parâmetro inicial como um identificador explícito (serialização). Se o atributo **\[ \_ identificador \] explícito** não for usado, o aplicativo ainda poderá especificar que uma operação tenha um identificador explícito (associação ou serialização) direcionando a chamada. Para fazer isso, um protótipo com um argumento contendo um tipo de identificador é fornecido para o arquivo IDL. Observe que, no modo padrão, um argumento que não aparece primeiro também pode ser usado como um identificador que direciona a chamada.

Portanto, embora o atributo **\[ \_ identificador \] explícito** seja uma maneira de dar ao protótipo IDL um atributo de **\[ \_ identificador \] explícito** primitivo, ele não requer necessariamente uma alteração no arquivo IDL. No modo [**/OSF**](-osf.md) , somente o primeiro argumento pode ser usado como um tipo de identificador explícito.

O atributo **\[ \_ identificador \] explícito** pode ser usado como um atributo de interface ou um atributo de operação. Como um atributo de interface, ele afeta todas as operações na interface e todos os tipos que exigem suporte de serialização. No entanto, se ele for usado como um atributo de operação, ele afetará apenas essa operação específica. Se um método contiver um ou \[ mais \] identificadores de contexto, o mais à esquerda \[ no \] identificador de contexto será usado como o identificador de associação e nenhum identificador explícito adicional será criado.

## <a name="examples"></a>Exemplos

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




