---
title: Estrutura de WMDRM_LICENSE_FILTER (wmdrmsdk. h)
description: A estrutura do filtro de licença do WMDRM \_ define os \_ parâmetros de filtragem para uso ao criar uma enumeração de licenças.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_LICENSE_FILTER
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763891"
---
# <a name="wmdrm_license_filter-structure"></a>Estrutura de filtro de \_ licença WMDRM \_

A estrutura do **\_ \_ filtro de licença do WMDRM** define os parâmetros de filtragem para uso ao criar uma enumeração de licenças.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**DW**
</dt> <dd>

Especifica um número de versão mínimo para as licenças retornadas.

</dd> <dt>

**bstrKID**
</dt> <dd>

Especifica uma ID de chave para filtrar licenças. Somente as licenças com a ID de chave especificada serão incluídas na enumeração.

</dd> <dt>

**bstrRights**
</dt> <dd>

Especifica um conjunto de direitos para filtrar licenças para. Somente as licenças que fornecem todos os direitos especificados serão incluídas na enumeração.

</dd> <dt>

**bstrAllowedSourceIDs**
</dt> <dd>

Especifica as fontes de conteúdo protegido a serem incluídas na pesquisa de licença.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada pelo método [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





