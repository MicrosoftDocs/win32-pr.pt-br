---
title: WMDRM_LICENSE_FILTER estrutura (Wmdrmsdk.h)
description: A estrutura FILTRO DE LICENÇA WMDRM define parâmetros de filtragem para uso \_ \_ ao criar uma enumeração de licença.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER formato de mídia do Windows
- formato de mídia de janelas de estrutura
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
ms.openlocfilehash: 94dc65758c7c5a25d31dd9fdb2d0fcd5cfa65debfff3defab4b88280a5ff3b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698132"
---
# <a name="wmdrm_license_filter-structure"></a>Estrutura DE FILTRO \_ DE LICENÇA \_ WMDRM

A **estrutura FILTRO DE LICENÇA \_ \_ WMDRM** define parâmetros de filtragem para uso ao criar uma enumeração de licença.

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

**Dwversion**
</dt> <dd>

Especifica um número de versão mínimo para as licenças retornadas.

</dd> <dt>

**bstrKID**
</dt> <dd>

Especifica uma ID de chave para a que filtrar licenças. Somente as licenças com a ID de chave especificada serão incluídas na enumeração .

</dd> <dt>

**bstrRights**
</dt> <dd>

Especifica um conjunto de direitos para o que filtrar licenças. Somente as licenças que fornecem todos os direitos especificados serão incluídas na enumeração .

</dd> <dt>

**bstrAllowedSourceIDs**
</dt> <dd>

Especifica as fontes de conteúdo protegido a incluir na pesquisa de licença.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada pelo [**método IWMDRMLicenseManagement::CreateLicenseEnumeration.**](iwmdrmlicensemanagement-createlicenseenumeration.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





