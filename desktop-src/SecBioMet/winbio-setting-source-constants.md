---
title: WINBIO_SETTING_SOURCE constantes (tipos \_ Winbio.h)
description: Determine se a Windows Biométrica está habilitada no momento.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f02a5edc80d00d098a592626ad4d9f0e1030f9f6eee119bf615375680d11842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909314"
---
# <a name="winbio_setting_source-constants"></a>Constantes WINBIO \_ SETTING \_ SOURCE

As constantes a seguir são usadas pela [**função WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) para determinar se o Windows Biometric Framework está habilitado no momento. As constantes especificam de onde a configuração foi originada.



| Constante                                                                                                                                                                                                        | Descrição                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <dt>**FONTE DE CONFIGURAÇÃO DO WINBIO \_ \_ \_ INVÁLIDA**</dt> </dl> | A configuração não é válida.<br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <dt>**PADRÃO DE \_ ORIGEM DE \_ CONFIGURAÇÃO DO WINBIO \_**</dt> </dl> | A configuração originou-se da política interna.<br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <dt>**POLÍTICA DE \_ ORIGEM DE \_ CONFIGURAÇÃO DO WINBIO \_**</dt> </dl>    | A configuração foi originada no registro do computador local.<br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <dt>**LOCAL DE \_ ORIGEM DA \_ CONFIGURAÇÃO DO WINBIO \_**</dt> </dl>       | A configuração foi criada por Política de Grupo<br/>                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





