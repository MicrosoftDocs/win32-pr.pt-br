---
description: A estrutura de eventos de atualização \_ atualiza eventos. Essa estrutura é passada de volta para o aplicativo de chamada por meio do procedimento de retorno de chamada de status do evento pelo NPP.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Estrutura de UPDATE_EVENT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812757"
---
# <a name="update_event-structure"></a>ATUALIZAR \_ estrutura de eventos

A estrutura de **\_ eventos de atualização** atualiza eventos. Essa estrutura é passada de volta para o aplicativo de chamada por meio do procedimento de retorno de chamada de status do evento pelo NPP.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Evento**
</dt> <dd>

Evento real que está sendo registrado.

</dd> <dt>

**Ação**
</dt> <dd>

A ação executada.

</dd> <dt>

**Status**
</dt> <dd>

Indicação de status de rede.

</dd> <dt>

**Valor**
</dt> <dd>

Variável de contador auxiliar.

</dd> <dt>

**Estampa**
</dt> <dd>

Os eventos marcados, em microssegundos.

</dd> <dt>

**lpUserContext**
</dt> <dd>

Contexto de usuário fornecido pelo aplicativo.

</dd> <dt>

**lpReserved**
</dt> <dd>

Uso de driver ou NAL.

</dd> <dt>

**FramesDropped**
</dt> <dd>

Quadros RTF descartados no buffer especificado.

</dd> <dt>

**Reserved**
</dt> <dd>

Nenhum dado é retornado com essa opção de opção.

</dd> <dt>

**lpFrameTable**
</dt> <dd>

Somente RTF.

</dd> <dt>

**lpPacketQueue**
</dt> <dd>

Para transmissões.

</dd> <dt>

**SecurityResponse**
</dt> <dd>

Resposta do monitor de segurança remota.

</dd> <dt>

**lpFinalStats**
</dt> <dd>

Isso só é preenchido em paradas não relacionadas à segurança (por exemplo, gatilhos).

</dd> </dl>

## <a name="remarks"></a>Comentários

Os usuários do C++ devem observar que a declaração desse retorno de chamada deve estar na parte pública do arquivo de cabeçalho:

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

A implementação deve estar na seção protegida do arquivo. cpp:

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




