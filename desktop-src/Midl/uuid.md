---
title: atributo uuid
description: O atributo de interface \ uuid\ designa um UUID (identificador universal exclusivo) atribuído à interface e que o distingue de outras interfaces.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- Atributo uuid MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce85ad2014e1f0563e2c20af7abec3cc476fab330b38340162f28fd390a5f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066636"
---
# <a name="uuid-attribute"></a>atributo uuid

O atributo de interface **\[ uuid \]** designa um UUID (identificador universal exclusivo) atribuído à interface e que o distingue de outras interfaces.

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*string-uuid* 
</dt> <dd>

Especifica uma cadeia de caracteres que consiste em 8 dígitos hexadecimais seguidos por um hífen e, em seguida, três grupos de quatro dígitos hexadecimais, cada um seguido por um hífen e, em seguida, 12 dígitos hexadecimais. Você pode colocar a cadeia de caracteres UUID entre aspas, exceto quando usar a opção do compilador MIDL [**/osf**](-osf.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A biblioteca em tempo de executar usa a interface UUID que o **\[ atributo uuid \]** designa para ajudar a estabelecer a comunicação entre os aplicativos cliente e servidor. O **\[ atributo \] uuid** pode aparecer na lista de atributos de interface para uma interface RPC ou uma interface COM.

Para uma interface RPC, a lista de atributos de interface deve incluir o atributo **\[ uuid \]** ou o atributo local, e aquele escolhido deve **\[** [](local.md) **\]** ocorrer exatamente uma vez. Se a lista incluir o **\[ atributo uuid, \]** ela também poderá incluir o atributo **\[** [**de**](version.md) **\]** versão.

Para uma interface COM (identificada pelo atributo de interface de objeto), a lista de atributos da interface deve incluir o **\[** [](object.md) **\]** **\[ atributo uuid, \]** **\[ \]** mas não pode incluir o atributo de versão. A lista de uma interface COM pode incluir o **\[ atributo local, \]** mesmo que o atributo **\[ uuid \]** está presente.

O Microsoft RPC dá suporte a uma extensão para ADL de DCE que permite que o UUID seja entre aspas duplas ("" ""). O formulário entre aspas é necessário para pré-processadores do compilador C que interpretam números UUID como números de ponto flutuante.

Todos os valores UUID devem ser gerados pelo computador para garantir a exclusividade. Use o utilitário Uuidgen para gerar valores UUID exclusivos.

O UUID e os números de versão da interface são usados para determinar se o cliente pode se vincular ao servidor. Para o cliente se vincular ao servidor, o UUID especificado nas interfaces do cliente e do servidor deve ser o mesmo.

Observe que uma interface sem atributos pode ser importada para um arquivo IDL base. No entanto, a interface deve conter apenas tipos de dados sem procedimentos. Se até mesmo um procedimento estiver contido na interface, um atributo local ou UUID deverá ser especificado.

## <a name="examples"></a>Exemplos

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Interface**](interface.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**Objeto**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 




