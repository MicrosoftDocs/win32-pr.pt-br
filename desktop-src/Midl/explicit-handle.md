---
title: explicit_handle atributo
description: O atributo \ explicit handle\ ACF especifica que cada procedimento tem, como seu primeiro parâmetro, um identificador primitivo, como \_ um tipo t de \_ identificador.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle atributo MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b50aa69c43e27b4797f6619b4efa14b90f16dd2b4bee45df2db6b708e58f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013914"
---
# <a name="explicit_handle-attribute"></a>atributo \_ de alça explícita

O atributo ACF de identificador explícito especifica que cada procedimento tem, como seu primeiro parâmetro, um identificador primitivo, como um tipo \[ **\_** \] t [**\_ de**](handle-t.md) identificador.

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

*interface-name* 
</dt> <dd>

Especifica o nome da interface.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando você usa o atributo **\[ \_ de alça \]** explícita, cada procedimento tem um handle primitivo como seu primeiro parâmetro, mesmo que o arquivo IDL não contenha esse alça em sua lista de parâmetros. Os protótipos emitidos para o arquivo de header e as rotinas de stub contêm o parâmetro adicional e esse parâmetro é usado como o handle para direcionar a chamada remota.

O **\[ atributo de \_ alça \]** explícita afeta procedimentos remotos e procedimentos de serialização. Para serialização de tipo, as rotinas de suporte são geradas com o parâmetro inicial como um identificador explícito (serialização). Se o **\[ atributo de \_ alça \]** explícito não for usado, o aplicativo ainda poderá especificar que uma operação tenha um alçado explícito (associação ou serialização) que direciona a chamada. Para fazer isso, um protótipo com um argumento que contém um tipo de identificador é fornecido para o arquivo IDL. Observe que, no modo padrão, um argumento que não aparece primeiro também pode ser usado como um handle que direciona a chamada.

Portanto, embora o atributo **\[ de \_ handle \]** explícito seja uma maneira de dar ao protótipo de IDL **\[ \_ \]** um atributo de alça explícita primitivo, ele não requer necessariamente uma alteração no arquivo IDL. No [**modo /osf,**](-osf.md) somente o primeiro argumento pode ser usado como um tipo de identificador explícito.

O **\[ atributo de \_ alça \]** explícita pode ser usado como um atributo de interface ou um atributo de operação. Como um atributo de interface, ele afeta todas as operações na interface e todos os tipos que exigem suporte à serialização. No entanto, se for usado como um atributo de operação, isso afetará apenas essa operação específica. Se um método contiver um ou mais em alças de contexto, o mais à esquerda no alça de contexto será usado como o alçamento de associação e nenhum handle \[ \] explícito adicional será \[ \] criado.

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

[**auto \_ handle**](auto-handle.md)
</dt> <dt>

[**alça \_ implícita**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




