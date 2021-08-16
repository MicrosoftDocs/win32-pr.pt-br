---
description: A \_ estrutura do descritor de quadros fornece informações descritivas sobre quadros brutos.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Estrutura de FRAME_DESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1e675c07eae46096878e7c0aa71b53ba5bf22194e82ad8cc5aa5b6070d7e27e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938567"
---
# <a name="frame_descriptor-structure"></a>\_Estrutura do descritor de quadros

A estrutura do **\_ descritor de quadros** fornece informações descritivas sobre quadros brutos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a>Membros

<dl> <dt>

**FramePointer**
</dt> <dd>

Ponteiro para dados de quadro.

</dd> <dt>

**Estampa**
</dt> <dd>

Hora do sistema, em microssegundos, quando o quadro foi capturado. Esse tempo normalmente é usado para determinar o intervalo entre os tempos em que dois quadros foram capturados.

</dd> <dt>

**FrameLength**
</dt> <dd>

Comprimento do quadro.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Tamanho de quadro real copiado.

</dd> <dt>

**ETYPE**
</dt> <dd>

Nome do ETYPE.

</dd> <dt>

**SAP**
</dt> <dd>

Valor SAP.

</dd> <dt>

**LowProtocol**
</dt> <dd>

Índice do protocolo encontrado.

</dd> <dt>

**LowProtocolOffset**
</dt> <dd>

Deslocamento para os dados de protocolo obtidos de **LowProtocol**.

</dd> <dt>

**HighPort**
</dt> <dd>

Porta de protocolo alto identificado em **LowProtocol**.

</dd> <dt>

**HighProtocolOffset**
</dt> <dd>

Deslocamento para os dados de protocolo obtidos de **HighPort**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




