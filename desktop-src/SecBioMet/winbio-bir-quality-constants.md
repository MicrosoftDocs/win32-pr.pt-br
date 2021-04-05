---
title: Constantes de WINBIO_BIR_QUALITY (WinBio \_ Types. h)
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
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086393"
---
# <a name="winbio_bir_quality-constants"></a>WINBIO \_ \_ constantes de qualidade Bir

Os sinalizadores a seguir são usados pelo membro **dataquality** da estrutura [**de \_ \_ cabeçalho WINBIO Bir**](winbio-bir-header.md) para especificar a qualidade relativa dos dados biométricos no Bir se um valor inteiro de 0 a 100 não tiver sido especificado.



| Constante/valor                                                                                                                                                                                                                                                                       | Descrição                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ Qualidade de dados \_ \_ não \_ definida**</dt> <dt> 1</dt> </dl>                   | As medições de qualidade são suportadas pelo criador do BIR, mas nenhum valor é definido no BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ Qualidade de dados \_ \_ não \_ suportada**</dt> <dt> 2</dt> </dl> | As medições de qualidade não são suportadas pelo criador do BIR.<br/>                             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





