---
description: Localiza o próximo quadro no contexto de captura atual que corresponde ao filtro.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Função FindNextFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501355"
---
# <a name="findnextframe-function"></a>Função FindNextFrame

A função **FindNextFrame** localiza o próximo quadro no contexto de captura atual que corresponde ao filtro.

## <a name="syntax"></a>Sintaxe


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCurrentFrame* 
</dt> <dd>

Um identificador para o quadro.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

O nome do protocolo, como TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

O endereço de destino.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

O endereço de origem.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Um ponteiro para uma **palavra** que receberá o deslocamento do protocolo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

O ponto de partida da pesquisa. Por padrão, essa função pesquisa em frente a 1.000 quadros do ponto de partida *OriginalFrameNumber* . Para alterar a distância de encaminhamento da pesquisa, adicione essa linha ao arquivo de Nmapi.ini, localizado no \\ diretório monitor de rede.

MAXLOOKBACK =<new lookforward distance>

</dd> <dt>

*HighestFrame* 
</dt> <dd>

O número de quadro mais alto na captura que é pesquisada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um identificador para o próximo quadro.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

O filtro de captura é definido principalmente pelo parâmetro *ProtocolName* , que é a única entrada de filtro necessária; Você pode adicionar dados *DestinationAddress* e *SourceAddress* para aumentar a velocidade de captura.

O ponteiro *ProtocolOffset* é retornado para o analisador de chamada, que adiciona a **palavra** ao ponteiro retornado bloqueando o quadro (com [ParserTemporaryLockFrame](parsertemporarylockframe.md)) para obter o **LPBYTE** do protocolo procurado. No retorno, o HFRAME que passou pelo filtro é fornecido ao analisador. Se o analisador descobrir que esse quadro não é o procurado, o analisador poderá entregar o HFRAME de volta à função **FindNextFrame** para obter o próximo quadro. Os endereços de origem e destino não são necessários e podem ser passados como **nulos**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




