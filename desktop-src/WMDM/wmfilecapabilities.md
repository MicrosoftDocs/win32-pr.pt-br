---
title: Estrutura WMFILECAPABILITIES
description: A estrutura WMFILECAPABILITIES descreve o tipo MIME.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Estrutura WMFILECAPABILITIES Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781290"
---
# <a name="wmfilecapabilities-structure"></a>Estrutura WMFILECAPABILITIES

A estrutura **WMFILECAPABILITIES** descreve o tipo MIME.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a>Membros

<dl> <dt>

**pwszMimeType**
</dt> <dd>

Tipo MIME.

</dd> <dt>

**dwReserved**
</dt> <dd>

**DWORD** reservado para uso futuro. Defina como zero (0).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDMDevice2::GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





