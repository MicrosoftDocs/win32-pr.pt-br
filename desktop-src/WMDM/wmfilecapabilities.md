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
ms.openlocfilehash: a4f4852eeb7142b92c2c1a4c2073dfc70e5f6a6d74c727a7ab9e63c285796846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903766"
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

 

 





