---
title: Constantes de WINBIO_POOL (WinBio \_ Types. h)
description: Especifique o tipo de pool de unidades biométricas a ser usado na sessão.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fefc43bb9dc4cefbde1ce5622853a3ba2cfae498ff2f8f81e97417e306641db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909793"
---
# <a name="winbio_pool-constants"></a>\_Constantes do pool WINBIO

As constantes a seguir podem ser usadas na função [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar o tipo de pool de unidades biométricas a ser usado na sessão.



| Constante                                                                                                                                                                                  | Descrição                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**\_pool WINBIO \_ desconhecido**</dt> </dl>          | O tipo de pool é desconhecido.<br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_sistema de pool WINBIO \_**</dt> </dl>             | Especifica uma coleção compartilhada de unidades biométricas gerenciadas pelo provedor de serviços.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**WINBIO \_ pool \_ privado**</dt> </dl>          | Especifica uma coleção de unidades biométricas que são gerenciadas pelo chamador.<br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <dt>**POOL WINBIO não \_ \_ atribuído**</dt> </dl> | Reservado.<br/>                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





