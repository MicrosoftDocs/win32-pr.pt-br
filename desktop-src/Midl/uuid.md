---
title: atributo uuid
description: O atributo \ UUID \ interface designa um UUID (identificador universal exclusivo) que é atribuído à interface e que o distingue de outras interfaces.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- MIDL de atributo uuid
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638580"
---
# <a name="uuid-attribute"></a>atributo uuid

O atributo interface **\[ UUID \]** designa um UUID (identificador universal exclusivo) que é atribuído à interface e que o distingue de outras interfaces.

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cadeia de caracteres-UUID* 
</dt> <dd>

Especifica uma cadeia de caracteres que consiste em 8 dígitos hexadecimais seguidos por um hífen, em seguida, três grupos de quatro dígitos hexadecimais, cada um seguido por um hífen e 12 dígitos hexadecimais. Você pode colocar a cadeia de caracteres UUID entre aspas, exceto quando você usar o [**/OSF**](-osf.md)do compilador MIDL switch.

</dd> </dl>

## <a name="remarks"></a>Comentários

A biblioteca de tempo de execução usa o UUID de interface que o atributo **\[ UUID \]** designa para ajudar a estabelecer a comunicação entre os aplicativos cliente e servidor. O atributo **\[ UUID \]** pode aparecer na lista de atributos de interface para uma interface RPC ou uma interface com.

Para uma interface RPC, a lista de atributos de interface deve incluir o atributo **\[ UUID \]** ou o **\[** [](local.md) **\]** atributo local, e aquele que você escolher deve ocorrer exatamente uma vez. Se a lista incluir o atributo **\[ UUID \]** , ela também poderá incluir o **\[** atributo [**version**](version.md) **\]** .

Para uma interface COM (identificada pelo **\[** atributo de interface de [**objeto**](object.md) **\]** ), a lista de atributos de interface deve incluir o atributo **\[ UUID \]** , mas não pode incluir o atributo **\[ version \]** . A lista de uma interface COM pode incluir o atributo **\[ local \]** , embora o atributo **\[ UUID \]** esteja presente.

O Microsoft RPC dá suporte a uma extensão para o DCE IDL que permite que o UUID seja colocado entre aspas duplas ("" ""). O formulário entre aspas é necessário para os pré-processadores do compilador C que interpretam números UUID como números de ponto flutuante.

Todos os valores UUID devem ser gerados por computador para garantir a exclusividade. Use o utilitário Uuidgen para gerar valores exclusivos de UUID.

O UUID e os números de versão da interface são usados para determinar se o cliente pode se associar ao servidor. Para que o cliente seja associado ao servidor, o UUID especificado nas interfaces do cliente e do servidor deve ser o mesmo.

Observe que uma interface sem atributos pode ser importada para um arquivo IDL base. No entanto, a interface deve conter apenas tipos de texto sem procedimentos. Se até um procedimento estiver contido na interface, um atributo local ou UUID deverá ser especificado.

## <a name="examples"></a>Exemplos

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 




