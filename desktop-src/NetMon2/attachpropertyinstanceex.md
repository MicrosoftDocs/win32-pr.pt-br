---
description: A função AttachPropertyInstanceEx mapeia uma propriedade existente para um local específico nos dados reconhecidos e modifica o valor dos dados da propriedade.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Função AttachPropertyInstanceEx (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ec0b874d55d149c9d049b8c6b2cafd716fe82c66410e2d3e1550b397c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911276"
---
# <a name="attachpropertyinstanceex-function"></a>Função AttachPropertyInstanceEx

A **função AttachPropertyInstanceEx** mapeia uma propriedade existente para um local específico nos dados reconhecidos e modifica o valor dos dados da propriedade.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ Em\]
</dt> <dd>

Lidar com o quadro que está sendo analisado. Use o handle passado para a DLL do analisador no *parâmetro hFrame* da [**função AttachProperties.**](attachproperties.md)

</dd> <dt>

*hProperty* \[ Em\]
</dt> <dd>

Lidar com uma [**estrutura PROPERTYINFO**](propertyinfo.md) que define a propriedade . Quando você implementa a [**função Registrar**](register-parser.md) exportação, especifica a estrutura **PROPERTYINFO** que define a propriedade .

</dd> <dt>

*Comprimento* \[ Em\]
</dt> <dd>

Comprimento dos dados para esta instância da propriedade.

</dd> <dt>

*lpData* \[ Em\]
</dt> <dd>

Ponteiro para o local nos dados reconhecidos em que o valor da propriedade está localizado. Use o ponteiro passado para a DLL do analisador no *parâmetro lpProtocol* da [**função AttachProperties.**](attachproperties.md)

</dd> <dt>

*LengthEx* \[ Em\]
</dt> <dd>

Comprimento do comprimento de dados estendido em bytes.

</dd> <dt>

*lpDataEx* \[ Em\]
</dt> <dd>

Ponteiro para os dados estendidos, que normalmente é uma variável de pilha que contém os dados estendidos.

</dd> <dt>

*HelpID* \[ Em\]
</dt> <dd>

Identificador (de 0 a 2047) usado para definir a Ajuda contextista para uma propriedade.

O *número helpID* é relativo ao arquivo de Ajuda associado ao banco de dados de [*propriedade do protocolo*](p.md).

</dd> <dt>

*IndentLevel* \[ Em\]
</dt> <dd>

Nível de recuo (de 0 a 15) usado para exibir uma propriedade hierarquicamente.

Monitor de Rede usa níveis de 0 a 9. O nível 15 é um valor especial que permite que o analisador anexe uma propriedade oculta que não está visível.

</dd> <dt>

*IFlags* \[ Em\]
</dt> <dd>

Um valor de campo BIT que indica a ordem dos BITs dentro de uma propriedade. Os analisadores anteriores que definiam *fError* como 0 ou 1 agora devem definir *fError* como IFLAG \_ ERROR. De definir esse parâmetro como um dos valores a seguir.



| Valor                                                                                                                                                         | Significado                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**ERRO \_ IFLAG**</dt> </dl>       | Os dados no quadro têm um erro.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ TROCADO**</dt> </dl> | No momento da anexação, o byte **WORD** é um formato não Intel.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ UNICODE**</dt> </dl> | No momento da anexação, **STRING** é Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será **TRUE.**

Se a função não for bem-sucedida, o valor de retorno será **FALSE.**

## <a name="remarks"></a>Comentários

A **função AttachPropertyInstanceEx** é chamada durante a implementação da função de exportação [**AttachProperties.**](attachproperties.md) Quando uma propriedade é anexada aos dados usando AttachPropertyInstanceEx, o Monitor de Rede cria uma estrutura [**PROPERTYINST**](propertyinst.md) que define a instância da propriedade anexada e uma estrutura [**PROPERTYINSTEX**](propertyinstex.md) que define os dados estendidos.

Se **AttachPropertyInstanceEx** for chamado e nenhum dado estendido for fornecido, o parâmetro *lpDataEx* for **NULL** ou o parâmetro *LengthEx* for 0, a chamada **AttachPropertyInstanceEx** será funcionalmente equivalente a [**uma chamada AttachPropertyInstance.**](attachpropertyinstance.md)

Durante a implementação de [**AttachProperties**](attachproperties.md), chame [**AttachPropertyInstance**](attachpropertyinstance.md) para usar os dados como eles existem na captura. Você também pode chamar **a função AttachPropertyInstanceEx** para modificar os dados da propriedade. No entanto, é aconselhável que você use os dados como eles existem na captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




