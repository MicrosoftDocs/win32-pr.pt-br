---
title: Enumeração de MSDRM_STATUS (wmdrmsdk. h)
description: O \_ tipo de enumeração status Msdrm define as condições de status para o subsistema DRM.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- Formato de mídia do Windows de enumeração de MSDRM_STATUS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4c1f9b37f237b1ae2399849ef3100e3d6fdbc12c7ee3bc1d169420e38bb85a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654570"
---
# <a name="msdrm_status-enumeration"></a>\_Enumeração de status Msdrm

O tipo de enumeração **\_ status Msdrm** define as condições de status para o subsistema DRM.

## <a name="syntax"></a>Syntax


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DRM_ERROR"></span><span id="drm_error"></span>**erro de DRM \_**
</dt> <dd>

Especifica que ocorreu um erro.

</dd> <dt>

<span id="DRM_INFORMATION"></span><span id="drm_information"></span>**informações de DRM \_**
</dt> <dd>

Especifica que há informações de status adicionais.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**\_início de BACKUPRESTORE DRM \_**
</dt> <dd>

Especifica que uma operação de backup ou restauração de licença foi iniciada.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**fim do DRM \_ BACKUPRESTORE \_**
</dt> <dd>

Especifica que uma operação de backup ou restauração de licença terminou.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**\_conexão BACKUPRESTORE \_ DRM**
</dt> <dd>

Especifica que uma operação de backup ou restauração de licença está em andamento e que o computador cliente está se conectando ao servidor de backup.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**desconexão de \_ BACKUPRESTORE DRM \_**
</dt> <dd>

Especifica que uma operação de backup ou restauração de licença está em andamento e que o computador cliente está desconectando do servidor de backup.

</dd> <dt>

<span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**erro de DRM \_ \_ WITHURL**
</dt> <dd>

Especifica que a operação de DRM encontrou uma URL inadequada.

</dd> <dt>

<span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_licença restrita de DRM \_**
</dt> <dd>

Especifica que a operação DRM não pode continuar porque nenhuma licença que concede o direito necessário existe no computador cliente.

</dd> <dt>

<span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ precisa de \_ individualização**
</dt> <dd>

Especifica que a operação DRM não pode continuar porque o subsistema DRM precisa ser individualizado.

</dd> <dt>

<span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**\_notificação de \_ OPL de reprodução de DRM \_**
</dt> <dd>

Especifica que uma operação de reprodução não pode ser concluída porque um requisito de nível de proteção de saída não foi atendido.

</dd> <dt>

<span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**\_notificação de \_ OPL de cópia de DRM \_**
</dt> <dd>

Especifica que uma operação de cópia não pode ser concluída porque um requisito de nível de proteção de saída não foi atendido.

</dd> <dt>

<span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**\_REFRESHCRL DRM \_ concluído**
</dt> <dd>

Especifica que uma chamada para [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) concluiu a atualização de uma lista de revogação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> </dl>

 

 





