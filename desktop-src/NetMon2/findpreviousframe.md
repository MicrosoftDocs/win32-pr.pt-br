---
description: A função FindPreviousFrame localiza o quadro anterior no contexto de captura atual que corresponde ao filtro.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Função FindPreviousFrame (Netmon.h)
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
ms.openlocfilehash: a3bd6378691b63fc7f4db2455f713ffd0cf2a0281da2411dc494244ad3f00ba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982523"
---
# <a name="findpreviousframe-function"></a>Função FindPreviousFrame

A **função FindPreviousFrame** localiza o quadro anterior no contexto de captura atual que corresponde ao filtro.

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

Lidar com o quadro.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Nome do protocolo, como TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Endereço de destino do quadro que é pesquisado.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Endereço de origem do quadro que é pesquisado.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Ponteiro para um **WORD** que recebe o deslocamento de protocolo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Ponto de partida da pesquisa. Por padrão, essa função pesquisa 1.000 quadros para trás do ponto de partida *OriginalFrameNumber.* Você pode alterar a distância de retorno de pesquisa adicionando essa linha ao arquivo Nmapi.ini, que está localizado no \\ Monitor de Rede diretório.

MAXLOOKBACK=<new lookback distance>

</dd> <dt>

*LowestFrame* 
</dt> <dd>

Número de quadro mais baixo na captura pesquisada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um alçamento para o quadro anterior.

Se a função não for bem-sucedida, o valor de retorno será **NULL.**

## <a name="remarks"></a>Comentários

O filtro de captura é definido principalmente por *ProtocolName,* que é a única entrada de filtro necessária; você pode adicionar *informações de DestinationAddress* *e SourceAddress* para aumentar a velocidade de captura.

*ProtocolOffset* é retornado ao analisador de chamada, que adiciona esse **DWORD** ao ponteiro retornado ao bloquear o quadro (com [ParserTemporaryLockFrame](parsertemporarylockframe.md)) para obter o LPBYTE do protocolo que está sendo pesquisado. No retorno, o HFRAME que passou o filtro é dado ao analisador. Se o analisador descobrir que o quadro não é aquele que está sendo procurado, o analisador poderá entregar esse HFRAME de volta para a função **FindPreviousFrame** para recuperar o próximo quadro. Os endereços de origem e de destino, que não são necessários, podem ser passados como **NULL.** Quando usados, esses endereços podem ser do tipo IP DE TIPO DE ENDEREÇO e assim por \_ \_ diante, não apenas tipos MAC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




