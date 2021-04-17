---
title: Enumeração de WMDM_STORAGE_ENUM_MODE
description: O \_ tipo de enumeração do modo enum de armazenamento do WMDM \_ \_ define como o conteúdo no armazenamento deve ser enumerado. Essa enumeração é usada por IWMDMStorage3 SetEnumPreference.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- WMDM_STORAGE_ENUM_MODE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789589"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a>\_Enumeração do \_ modo de enumeração de armazenamento WMDM \_

O tipo de enumeração do **\_ \_ \_ modo enum de armazenamento do WMDM** define como o conteúdo no armazenamento deve ser enumerado. Essa enumeração é usada por [**IWMDMStorage3:: SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**modo de enumeração \_ \_ bruto**
</dt> <dd>

Enumera o conteúdo no armazenamento da mesma forma que ele é organizado no sistema de arquivos do armazenamento.

**o \_ modo de enumeração \_ usa o \_ dispositivo \_ pref**

Enumera o conteúdo no armazenamento com base na preferência do dispositivo, conforme indicado pelo parâmetro do dispositivo *UseMetadataViews* .

**\_modos de \_ exibição de metadados do modo de enumeração \_**

Enumera o conteúdo no armazenamento organizando o conteúdo com base em uma exibição de metadados.

</dd> <dt>

<span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**o \_ modo de enumeração \_ usa o \_ dispositivo \_ pref**
</dt> <dd>

Enumera o conteúdo no armazenamento com base na preferência do dispositivo, conforme indicado pelo parâmetro do dispositivo *UseMetadataViews* .

**\_modos de \_ exibição de metadados do modo de enumeração \_**

Enumera o conteúdo no armazenamento organizando o conteúdo com base em uma exibição de metadados.

</dd> <dt>

<span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**\_modos de \_ exibição de metadados do modo de enumeração \_**
</dt> <dd>

Enumera o conteúdo no armazenamento organizando o conteúdo com base em uma exibição de metadados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





