---
description: Contém dados que descrevem um especialista quando ele é iniciado.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Estrutura EXPERTSTARTUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f49fcf3c87795dbd7c9e65745e1b5560331c96c471d8ff7b2c8a24560b143cb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911046"
---
# <a name="expertstartupinfo-structure"></a>Estrutura EXPERTSTARTUPINFO

A estrutura **EXPERTSTARTUPINFO** contém dados que descrevem um especialista quando ele é iniciado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Sinalizadores**
</dt> <dd>

Sinalizadores que descrevem o especialista.

</dd> <dt>

**hCapture**
</dt> <dd>

Identificador para uma captura.

</dd> <dt>

**szCaptureFile**
</dt> <dd>

Nome do arquivo de captura.

</dd> <dt>

**dwFrameNumber**
</dt> <dd>

Número do quadro.

</dd> <dt>

**hProtocol**
</dt> <dd>

Identificador para o protocolo.

</dd> <dt>

**lpPropertyInst**
</dt> <dd>

Ponteiro para uma estrutura [**PROPERTYINST**](propertyinst.md) .

</dd> <dt>

**sBitfield**
</dt> <dd> <dl> <dt>

**BitNumber**
</dt> <dd>

Usado somente se o membro **Dataqualificador** da estrutura [**PROPERTYINST**](propertyinst.md) estiver definido para os \_ sinalizadores prop igual \_ .

</dd> <dt>

**Bno**
</dt> <dd>

Usado somente se o membro **Dataqualificador** da estrutura [**PROPERTYINST**](propertyinst.md) estiver definido para os \_ sinalizadores prop igual \_ .

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




