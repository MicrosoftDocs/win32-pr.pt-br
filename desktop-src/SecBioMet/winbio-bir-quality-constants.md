---
title: WINBIO_BIR_QUALITY constantes (tipos \_ Winbio.h)
description: Especifique a qualidade relativa dos dados biométricos no BIR se um valor inteiro de 0 a 100 não tiver sido especificado.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5139b1420ea3dbfbc9e37a9dc07421788bb051acb40449e9c0117031320e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911042"
---
# <a name="winbio_bir_quality-constants"></a>Constantes \_ WINBIO BIR \_ QUALITY

Os sinalizadores a seguir são usados pelo membro **DataQuality** da estrutura [**WINBIO \_ BIR \_ HEADER**](winbio-bir-header.md) para especificar a qualidade relativa dos dados biométricos no BIR se um valor inteiro de 0 a 100 não tiver sido especificado.



| Constante/valor                                                                                                                                                                                                                                                                       | Descrição                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ QUALIDADE \_ DE DADOS NÃO \_ \_ DEFINIDA**</dt> <dt> 1</dt> </dl>                   | As medidas de qualidade são suportadas pelo criador do BIR, mas nenhum valor é definido no BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ QUALIDADE \_ DE DADOS SEM \_ \_ SUPORTE**</dt> <dt> 2</dt> </dl> | Não há suporte para medidas de qualidade pelo criador do BIR.<br/>                             |



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

 

 





