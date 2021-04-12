---
title: Constantes de WINBIO_BIR_FIELD (WinBio \_ Types. h)
description: Especifique um bitmask.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295794"
---
# <a name="winbio_bir_field-constants"></a>\_Constantes do \_ campo WINBIO Bir

As constantes a seguir são usadas para criar um bitmask para o membro **ValidFields** da estrutura de [**\_ \_ cabeçalho WINBIO Bir**](winbio-bir-header.md) .



| Constante/valor                                                                                                                                                                                                                                                                                           | Descrição                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**WINBIO \_ 0x0001 \_ de \_ \_ contagem de subtítulos de campo Bir**</dt> <dt></dt> </dl>                          | Fornecido para conformidade com o NISTIR 6529-a, o formato de Patron da estrutura de formatos de intercâmbio biométrico comum (CBEFF), mas não é usado.<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**WINBIO \_ \_ID de \_ produto \_ do campo Bir**</dt> <dt>0x0002</dt> </dl>                                   | O membro **ProductID** é válido.<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**WINBIO \_ BIR \_ campo \_ Patron \_ ID**</dt> <dt>0x0004</dt> </dl>                                      | Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**WINBIO \_ \_ \_ Índice de campo Bir**</dt> <dt>0x0008</dt> </dl>                                                   | Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**WINBIO \_ 0x0010 \_ de \_ \_ data de criação do campo Bir**</dt> <dt></dt> </dl>                          | O membro **CreationDate** é válido.<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**WINBIO \_ \_Período de \_ validade \_ do campo Bir**</dt> <dt>0x0020</dt> </dl>                    | O membro **ValidityPeriod** é válido.<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**WINBIO \_ BIR \_ de \_ \_ tipo biométrico de campo**</dt> <dt>0x0040</dt> </dl>                       | O membro de **tipo** é válido.<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**WINBIO \_ BIR \_ de \_ \_ subtipo de campo biométrico**</dt> <dt>0x0080</dt> </dl>              | O membro do **subtipo** é válido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**WINBIO \_ BIR \_ Field \_ CBEFF \_ header \_ versão**</dt> <dt>0x0100</dt> </dl>    | O membro **HeaderVersion** é válido.<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**WINBIO \_ BIR \_ Field \_ Patron \_ header \_ versão**</dt> <dt>0x0200</dt> </dl> | O membro **PatronHeaderVersion** é válido.<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**WINBIO \_ BIR \_ de \_ \_ finalidade biométrica**</dt> <dt>0x0400</dt> do campo </dl>              | O membro de **finalidade** é válido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**WINBIO \_ BIR \_ \_ \_ condição biométrica do campo**</dt> <dt>0x0800</dt> </dl>        | Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**WINBIO \_ BIR \_ \_ qualidade do campo**</dt> <dt>0x1000</dt> </dl>                                             | O membro **dataquality** é válido.<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**WINBIO \_ 0x2000 do BIR \_ Field \_ Creator**</dt> <dt></dt> </dl>                                             | Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**WINBIO \_ BIR \_ \_ desafio de campo**</dt> <dt>0x4000</dt> </dl>                                       | Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**WINBIO \_ BIR \_ de \_ carga de campo**</dt> <dt>0x8000</dt> </dl>                                             | Fornecido para conformidade com NISTIR 6529-A, CBEFF Patron Format A, mas não usado.<br/>                                                   |



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

 

 





