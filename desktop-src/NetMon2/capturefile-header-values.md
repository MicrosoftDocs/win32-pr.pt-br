---
description: Define a estrutura do arquivo de cabeçalho de Monitor de Rede.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Estrutura de CAPTUREFILE_HEADER_VALUES (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 29ee0ab0a9a927b3860760877457735198465b7c28789a542c040fc9e9e788a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367412"
---
# <a name="capturefile_header_values-structure"></a>Estrutura de \_ valores de cabeçalho de captura \_

A estrutura de **\_ \_ valores de cabeçalho** do arquivo de captura define a estrutura do arquivo de cabeçalho monitor de rede.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a>Membros

<dl> <dt>

**Signature**
</dt> <dd>

Identificador exclusivo: ' GMBU.

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Binary, decimal codificado (secundário). O valor desse membro deve ser zero (0).

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Decimal codificado em binário (principal). Esse valor deve ser 2.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo de topologia.

</dd> <dt>

**Estampa**
</dt> <dd>

Hora da captura.

</dd> <dt>

**FrameTableOffset**
</dt> <dd>

Tabela de índice de quadro.

</dd> <dt>

**FrameTableLength**
</dt> <dd>

Tamanho da tabela do índice do quadro.

</dd> <dt>

**UserDataOffset**
</dt> <dd>

Deslocamento de dados do usuário.

</dd> <dt>

**UserDataLength**
</dt> <dd>

Comprimento dos dados do usuário.

</dd> <dt>

**CommentDataOffset**
</dt> <dd>

Deslocamento de dados de comentário.

</dd> <dt>

**CommentDataLength**
</dt> <dd>

Comprimento dos dados do comentário.

</dd> <dt>

**StatisticsOffset**
</dt> <dd>

Deslocamento para a estrutura de **estatísticas** .

</dd> <dt>

**StatisticsLength**
</dt> <dd>

Comprimento da estrutura de **estatísticas** .

</dd> <dt>

**NetworkInfoOffset**
</dt> <dd>

Deslocamento para a estrutura **NETWORKINFO** .

</dd> <dt>

**NetworkInfoLength**
</dt> <dd>

Comprimento da estrutura **NETWORKINFO** .

</dd> <dt>

**ConversationStatsOffset**
</dt> <dd>

Este membro não é usado.

</dd> <dt>

**ConversationStatsLength**
</dt> <dd>

Este membro não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




