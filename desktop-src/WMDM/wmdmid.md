---
title: Estrutura WMDMID
description: A estrutura WMDMID descreve os números de série e as IDs de grupo.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Estrutura WMDMID Windows Media Gerenciador de Dispositivos
- Ponteiro de estrutura PWMDMID Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781469"
---
# <a name="wmdmid-structure"></a>Estrutura WMDMID

A estrutura **WMDMID** descreve os números de série e as IDs de grupo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamanho da estrutura **WMDMID** , em bytes.

</dd> <dt>

**dwVendorID**
</dt> <dd>

**DWORD** que contém o número de ID registrado do fornecedor. Contém zero se não estiver em uso.

</dd> <dt>

**\[comprimento de WMDMID pID \_\]**
</dt> <dd>

Ponteiro para uma matriz de bytes que contém o número de série. O número de série é uma cadeia de caracteres de valores de bytes que não têm nenhum formato padrão. Observe que esse não é um valor de caractere largo. **WMDMID \_ LENGTH** é um valor constante definido em mswmdm. h.

</dd> <dt>

**SerialNumberLength**
</dt> <dd>

Comprimento real do número de série retornado, em bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMDSPDevice:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**IMDSPStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**IWMDMDevice:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**IWMDMStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





