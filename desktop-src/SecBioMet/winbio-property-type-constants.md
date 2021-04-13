---
title: Constantes de WINBIO_PROPERTY_TYPE (WinBio. h)
description: Especifique a origem das informações de propriedade na função WinBioGetProperty.
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4a1420af18bfa4d2ba5d0457b22cd5f77e7b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455991"
---
# <a name="winbio_property_type-constants"></a>Constantes do tipo de \_ Propriedade WINBIO \_

As constantes **de \_ \_ tipo de propriedade WINBIO** a seguir podem ser usadas para especificar a origem das informações de propriedade na função [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) .

<dl> <dt>

<span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**\_sessão do \_ tipo de propriedade WINBIO \_**
</dt> <dd> <dl> <dt>



A propriedade se aplica a uma sessão biométrica específica.


</dt> </dl> </dd> <dt>

<span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**\_modelo de \_ tipo de propriedade WINBIO \_**
</dt> <dd> <dl> <dt>



A propriedade se aplica a um modelo biométrico específico.


</dt> </dl> </dd> <dt>

<span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**\_unidade de \_ tipo de propriedade WINBIO \_**
</dt> <dd> <dl> <dt>



A propriedade se aplica a uma unidade biométrica específica.


</dt> </dl> </dd> <dt>

<span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**\_conta do \_ tipo de propriedade WINBIO \_**
</dt> <dd> <dl> <dt>



A propriedade se aplica a uma conta de usuário específica que tenha um registro biométrico. Esse valor tem suporte a partir do Windows 10.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>WinBio. h (incluir WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 





