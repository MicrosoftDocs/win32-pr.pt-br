---
title: Enumeração de DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
description: O \_ tipo de enumeração status de individualização de DRM \_ define os Estados válidos para individualização de DRM. | Enumeração de DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- Formato de mídia do Windows de enumeração de DRM_INDIVIDUALIZATION_STATUS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 081a8714d29cb48236bdb9191c15e92db96b18a9f8c1d9c2388c5baee7783296
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705646"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>Enumeração de DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)

O tipo de enumeração **\_ \_ status de individualização de DRM** define os Estados válidos para [*individualização*](wmformat-glossary.md)de DRM. Quando um aplicativo inicia a individualização com uma chamada para [**IWMDRMReader:: individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), o progresso da solicitação de individualização é transmitido para o aplicativo por meio de chamadas para o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . As mensagens de status de individualização usarão o \_ membro WMT individualize do tipo de enumeração [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) como o parâmetro *status* . O status da individualização é passado para **OnStatus** *no parâmetro de* física.

## <a name="syntax"></a>Syntax


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**i \_ INdefinido**
</dt> <dd>

Este valor está reservado para uso futuro.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**início do i \_**
</dt> <dd>

Indica o início do processo de individualização.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**i com \_ sucesso**
</dt> <dd>

Indica que o processo de individualização foi concluído.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**falha de i \_**
</dt> <dd>

Indica que o processo de individualização falhou.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**i \_ cancelar**
</dt> <dd>

Indica que o processo de individualização foi cancelado como resultado de uma chamada para [**IWMDRMReader:: CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Download do i \_**
</dt> <dd>

Indica que a atualização de segurança está sendo baixada.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**i \_ instalar**
</dt> <dd>

Indica que a atualização de segurança está sendo instalada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela estrutura [**de \_ \_ status individual do WM**](wm-individualize-status.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Versão<br/>                  | Windows SDK do Media Format 7 ou versões posteriores do SDK<br/>                       |
| Cabeçalho<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_status do http DRM \_**](drm-http-status.md)
</dt> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





