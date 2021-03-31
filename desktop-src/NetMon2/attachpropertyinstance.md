---
description: A função AttachPropertyInstance mapeia uma propriedade existente para um local específico nos dados reconhecidos.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: Função AttachPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829345"
---
# <a name="attachpropertyinstance-function"></a>Função AttachPropertyInstance

A função **AttachPropertyInstance** mapeia uma propriedade existente para um local específico nos dados reconhecidos.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro que está sendo analisado. Use o identificador passado para a DLL do analisador no parâmetro *hFrame* da função [**attachproperties**](attachproperties.md) .

</dd> <dt>

*hProperty* \[ no\]
</dt> <dd>

Identificador para uma estrutura de [**PROPERTYINFO**](propertyinfo.md) que define a propriedade. Ao implementar a função de exportação de [**registro**](register-parser.md) , você especifica a estrutura **PROPERTYINFO** que define a propriedade.

</dd> <dt>

*Comprimento* \[ no\]
</dt> <dd>

Comprimento dos dados para esta instância da propriedade.

</dd> <dt>

*lpData* \[ no\]
</dt> <dd>

Ponteiro para o local nos dados reconhecidos nos quais o valor da propriedade está localizado. Use o ponteiro passado para a DLL do analisador no parâmetro *lpProtocol* da função [**attachproperties**](attachproperties.md) .

</dd> <dt>

*HelpID* \[ no\]
</dt> <dd>

Identificador (de 0 a 2047) usado para definir a ajuda contextual para a propriedade.

O número do identificador é relativo ao arquivo de ajuda associado ao [*banco de dados de propriedades*](p.md)de protocolo.

</dd> <dt>

*IndentLevel* \[ no\]
</dt> <dd>

Nível de recuo (de 0 a 15) usado para exibir uma propriedade hierarquicamente.

Monitor de Rede usa os níveis de 0 a 14 para recuar Propriedades. O nível 15 é um valor especial que permite que um analisador anexe uma propriedade oculta que não está visível.

</dd> <dt>

*IFlags* \[ no\]
</dt> <dd>

Um valor de campo de bits que indica a ordem dos BITs dentro de uma propriedade. Os analisadores anteriores que definem o *referenciador* como 0 ou 1, agora devem definir o *referenciador* como \_ erro IFLAG. Defina esse parâmetro como um dos valores a seguir.



| Valor                                                                                                                                                         | Significado                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**erro de IFLAG \_**</dt> </dl>       | Os dados no quadro têm um erro.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ permutado**</dt> </dl> | No momento da anexação, o byte de **palavra** é um formato não-Intel.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ Unicode**</dt> </dl> | No momento da anexação, a **cadeia de caracteres** é Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

A função **AttachPropertyInstance** é chamada durante a implementação da função de exportação [**attachproperties**](attachproperties.md) . Quando uma propriedade é anexada aos dados, Monitor de Rede cria uma estrutura [**PROPERTYINST**](propertyinst.md) que define a instância da propriedade anexada.

Durante a implementação de [**attachproperties**](attachproperties.md), chame **AttachPropertyInstance** para usar os dados como eles existem na captura. Você também pode chamar a função [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) para modificar os dados de propriedade. No entanto, é recomendável que você use os dados como eles existem na captura.



| Para obter informações sobre                                        | Consulte                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede. | [**Analisadores**](parsers.md)                                         |
| Como chamar **AttachPropertyInstance**.                   | [Implementando Anexaproperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Anexarproperties**](attachproperties.md)
</dt> <dt>

[**AttachPropertyInstanceEx**](attachpropertyinstanceex.md)
</dt> <dt>

[**PROPERTYINST**](propertyinst.md)
</dt> </dl>

 

 




