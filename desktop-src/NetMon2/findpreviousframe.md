---
description: A função FindPreviousFrame localiza o quadro anterior no contexto de captura atual que corresponde ao filtro.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Função FindPreviousFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920706"
---
# <a name="findpreviousframe-function"></a>Função FindPreviousFrame

A função **FindPreviousFrame** localiza o quadro anterior no contexto de captura atual que corresponde ao filtro.

## <a name="syntax"></a>Sintaxe


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCurrentFrame* 
</dt> <dd>

Identificador para o quadro.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Nome do protocolo, como TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Endereço de destino do quadro procurado.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Endereço de origem do quadro procurado.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Ponteiro para uma **palavra** que recebe o deslocamento do protocolo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Ponto de partida da pesquisa. Por padrão, essa função pesquisa quadros de 1.000 anteriores do ponto de partida *OriginalFrameNumber* . Você pode alterar a distância de pesquisa adicionando essa linha ao arquivo de Nmapi.ini, que está localizado no \\ diretório monitor de rede.

MAXLOOKBACK =<new lookback distance>

</dd> <dt>

*LowestFrame* 
</dt> <dd>

O número de quadro mais baixo na captura que é pesquisada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um identificador para o quadro anterior.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

O filtro de captura é definido principalmente por *ProtocolName*, que é a única entrada de filtro necessária; Você pode adicionar informações de *DestinationAddress* e *SourceAddress* para aumentar a velocidade de captura.

*ProtocolOffset* é retornado para o analisador de chamada, que adiciona esse **DWORD** ao ponteiro retornado bloqueando o quadro (com [PARSERTEMPORARYLOCKFRAME](parsertemporarylockframe.md)) para obter o LPBYTE do protocolo que está sendo pesquisado. No retorno, o HFRAME que passou pelo filtro é fornecido ao analisador. Se o analisador descobrir que o quadro não é aquele que está sendo procurado, o analisador poderá entregar esse HFRAME de volta à função **FindPreviousFrame** para recuperar o próximo quadro. Os endereços de origem e de destino, que não são necessários, podem ser passados como **NULL**. Quando usado, esses endereços podem ser do tipo endereço \_ \_ IP, e assim por diante, não apenas tipos de Mac.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




