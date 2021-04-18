---
title: Estrutura de WMDRM_ENCRYPT_SCATTER_INFO (wmdrmsdk. h)
description: A \_ estrutura de informações de dispersão do WMDRM Encrypt \_ \_ contém as informações necessárias para configurar a interface IWMDRMEncryptScatter para uso.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_ENCRYPT_SCATTER_INFO
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793998"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>\_Estrutura de \_ informações de dispersão do WMDRM Encrypt \_

A estrutura de **\_ \_ \_ informações de dispersão do WMDRM Encrypt** contém as informações necessárias para configurar a interface [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) para uso.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwStreamID**
</dt> <dd>

Identificador do fluxo a ser criptografado.

</dd> <dt>

**dwSampleProtectionVersion**
</dt> <dd>

Versão de proteção de exemplo a ser usada para codificar dados do fluxo especificado.

</dd> <dt>

**cbProtectionInfo**
</dt> <dd>

Tamanho do buffer **pbProtectionInfo** em bytes.

</dd> <dt>

**pbProtectionInfo**
</dt> <dd>

Buffer que contém informações adicionais de proteção.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada pelo método [**IWMDRMEncryptScatter:: InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





