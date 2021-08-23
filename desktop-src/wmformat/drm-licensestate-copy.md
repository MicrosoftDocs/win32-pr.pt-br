---
title: DRM_LicenseState_Copy
description: A propriedade Copy LicenseState do DRM contém uma estrutura WM LICENSE STATE DATA que contém detalhes sobre como esse \_ direito foi aplicado ao \_ \_ \_ \_ conteúdo.
ms.assetid: 97a79e35-6533-4781-b368-ffe8d81956ec
keywords:
- DRM_LicenseState_Copy formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_LicenseState_Copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245c200651e191d79bd2d33ef469487b26d490549bdef85db92c0f6c58b10caa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658846"
---
# <a name="drm_licensestate_copy"></a>Cópia de LicenseState do DRM \_ \_

A **propriedade \_ Copy LicenseState \_ do DRM** contém uma estrutura [**WM LICENSE STATE \_ \_ \_ DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) que contém detalhes sobre como esse direito foi aplicado ao conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LicenseState \_ Copy

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BINARY**

## <a name="remarks"></a>Comentários

Essa é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do DRM**](drm-properties.md)
</dt> </dl>

 

 