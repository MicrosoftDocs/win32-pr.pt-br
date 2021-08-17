---
description: Empacota o tipo de objeto, a versão e as informações de tamanho necessárias em muitas estruturas do NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: Estrutura de NDIS_OBJECT_HEADER (Ntddndis. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: f9f4a4ef2a833081cde0c3c7ca4d395e59743944291a95d7680c241191988b35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065045"
---
# <a name="ndis_object_header-structure"></a>Estrutura de cabeçalho de \_ objeto NDIS \_

A estrutura de **\_ \_ cabeçalho do objeto NDIS** empacota o tipo de objeto, a versão e as informações de tamanho necessárias em muitas estruturas do NDIS 6,0.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

Especifica o tipo de objeto NDIS que uma estrutura descreve.

</dd> <dt>

**Revisão**
</dt> <dd>

Especifica o número de revisão dessa estrutura.

</dd> <dt>

**Tamanho**
</dt> <dd>

Especifica o tamanho total, em bytes, da estrutura NDIS que contém o **cabeçalho do \_ objeto \_ NDIS**. Esse tamanho inclui o tamanho do membro **do \_ \_ cabeçalho do objeto NDIS** e todos os outros membros da estrutura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, somente Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                       |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Ntddndis. h (incluir Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de DOT11 \_ BSSID \_**](dot11-bssid-list.md)
</dt> </dl>

 

 




