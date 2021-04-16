---
description: A função de exportação Attachproperties mapeia as propriedades para um local dentro de um pedaço de dados reconhecidos. Anexarproperties deve ser implementado para cada analisador compatível com a DLL do analisador.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Função de retorno de chamada attachproperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757758"
---
# <a name="attachproperties-callback-function"></a>Função de retorno de chamada attachproperties

A função de exportação **attachproperties** mapeia as propriedades para um local dentro de um pedaço de dados reconhecidos. **Anexarproperties** deve ser implementado para cada analisador compatível com a DLL do analisador.

## <a name="syntax"></a>Sintaxe


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador do quadro que está sendo analisado.

</dd> <dt>

*lpFrame* \[ no\]
</dt> <dd>

Ponteiro para o primeiro byte em um quadro.

</dd> <dt>

*lpProtocol* \[ no\]
</dt> <dd>

Ponteiro para o início dos dados reconhecidos.

</dd> <dt>

*MacType* \[ no\]
</dt> <dd>

Valor MAC do primeiro protocolo em um quadro. O *MacType* pode ser um dos seguintes:



| Valor                                                                                                                                                                         | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**tipo de MAC \_ \_ Ethernet**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**tipo de MAC \_ \_ TOKENRING**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**tipo de MAC \_ \_ FDDI**</dt> </dl>                | ANSI X3T 9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ no\]
</dt> <dd>

O número restante de bytes em um quadro que começa no início dos dados reconhecidos.

</dd> <dt>

*hPreviousProtocol* \[ no\]
</dt> <dd>

Identificador do protocolo anterior.

</dd> <dt>

*nPreviousProtocolOffset* \[ no\]
</dt> <dd>

Deslocamento do protocolo anterior começando no início do quadro.

</dd> <dt>

*lpInstData* \[ no\]
</dt> <dd>

Ponteiro para os dados de instância fornecidos pelo protocolo anterior. Os dados da instância não podem ter mais de um \_ PTR de comprimento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um ponteiro para o primeiro byte após os dados reconhecidos em um quadro ou **nulo** se os dados reconhecidos forem a última parte dos dados em um quadro.

Se a função não for bem-sucedida, o valor de retorno será um ponteiro para os dados reconhecidos. O parâmetro *lpProtocol* passa o ponteiro para a DLL do analisador.

## <a name="remarks"></a>Comentários

Monitor de Rede chama a função **attachproperties** para cada analisador que reconhece uma parte dos dados em um quadro. Observe que o analisador determina quais propriedades existem nos dados reconhecidos e onde cada propriedade está localizada.

Durante a implementação de **attachproperties**, chame [AttachPropertyInstance](attachpropertyinstance.md) para usar os dados como eles existem na captura. Você também pode chamar a função [AttachPropertyInstanceEx](attachpropertyinstanceex.md) para modificar os dados de propriedade. No entanto, é recomendável que você use os dados como eles existem na captura.

As funções **AttachPropertyInstanceEx** e **AttachPropertyInstance** são chamadas apenas para as propriedades que existem nos dados reconhecidos. Observe que Monitor de Rede tem um [*banco de dados de propriedade*](p.md) para o analisador que contém uma descrição de todas as propriedades que o analisador suporta.

**Dados de instância**

Os dados da instância são informações passadas de um analisador para outro. Os dados da instância podem ser quaisquer dados que sejam menores ou iguais a um \_ PTR de comprimento, ou um ponteiro para dados, como dados de quadro brutos, que não precisam ser alocados pelo analisador ou liberados pelo parser. No parâmetro *lpInstData* das funções **attachproperties** e [RecognizeFrame](recognizeframe.md) , monitor de rede fornece um ponteiro para os dados da instância do protocolo anterior. Você pode definir os dados da instância para o analisador durante a implementação de **RecognizeFrame**.



| Para obter informações sobre                                          | Consulte                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede.   | [Analisadores](parsers.md)                                             |
| Quais pontos de entrada são incluídos na DLL do analisador.           | [Arquitetura de DLL do analisador](parser-dll-architecture.md)             |
| Como reconhecer dados.                                      | [Implementando RecognizeFrame](implementing-recognizeframe.md)     |
| Como criar um banco de dados de propriedade.                          | [Implementando o registro](implementing-register.md)                 |
| Como implementar **anexaproperties**  inclui um exemplo. | [Implementando Anexaproperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




