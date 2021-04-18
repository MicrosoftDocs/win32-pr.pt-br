---
title: Constantes de WINBIO_BIOMETRIC_TYPE (WinBio \_ Types. h)
description: Tipos biométricos padrão definidos pelo National Institute of Standards and Technology Information (NISTIR) 6529-A, também conhecido como o formato de Patron da CBEFF (Biometric Exchange formatings Framework).
ms.assetid: DCBDB5F9-FF81-44C1-B439-2B8C02483212
topic_type:
- apiref
api_name:
- WINBIO_STANDARD_TYPE_MASK
- WINBIO_NO_TYPE_AVAILABLE
- WINBIO_TYPE_MULTIPLE
- WINBIO_TYPE_FACIAL_FEATURES
- WINBIO_TYPE_VOICE
- WINBIO_TYPE_FINGERPRINT
- WINBIO_TYPE_IRIS
- WINBIO_TYPE_RETINA
- WINBIO_TYPE_HAND_GEOMETRY
- WINBIO_TYPE_SIGNATURE_DYNAMICS
- WINBIO_TYPE_KEYSTROKE_DYNAMICS
- WINBIO_TYPE_LIP_MOVEMENT
- WINBIO_TYPE_THERMAL_FACE_IMAGE
- WINBIO_TYPE_THERMAL_HAND_IMAGE
- WINBIO_TYPE_GAIT
- WINBIO_TYPE_SCENT
- WINBIO_TYPE_DNA
- WINBIO_TYPE_EAR_SHAPE
- WINBIO_TYPE_FINGER_GEOMETRY
- WINBIO_TYPE_PALM_PRINT
- WINBIO_TYPE_VEIN_PATTERN
- WINBIO_TYPE_FOOT_PRINT
- WINBIO_TYPE_OTHER
- WINBIO_TYPE_PASSWORD
- WINBIO_TYPE_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d2ab5c41a3c2af26312c97a67d1179b50fd759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800095"
---
# <a name="winbio_biometric_type-constants"></a>\_Constantes de tipo BIOMÉTRICO WINBIO \_

As constantes a seguir representam os tipos biométricos padrão definidos pelo National Institute of Standards and Technology Information (NISTIR) 6529-A, também conhecido como o formato de Patron do CBEFF (Biometric Exchange formating Framework). No momento, somente a **\_ \_ impressão digital do tipo WINBIO** é suportada.



| Constante                                                                                                                                                                                                            | Descrição                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**\_máscara de \_ tipo \_ padrão WINBIO**</dt> </dl>                 | Bitmask que especifica o conjunto com suporte de fatores biométricos.<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**WINBIO \_ nenhum \_ tipo \_ disponível**</dt> </dl>                    | Nenhum tipo biométrico está disponível.<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**WINBIO \_ tipo \_ múltiplo**</dt> </dl>                                 | Vários tipos são especificados.<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**\_ \_ recursos facial do tipo WINBIO \_**</dt> </dl>           | Os recursos faciais são usados para determinar a identidade de um indivíduo.<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**WINBIO \_ tipo \_ voz**</dt> </dl>                                          | Padrões de frequência e volume na voz de um indivíduo são usados para determinar a identidade de um indivíduo.<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**\_impressão digital do tipo WINBIO \_**</dt> </dl>                        | Padrões de impressão digital são usados para determinar a identidade de um indivíduo.<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**WINBIO \_ tipo \_ íris**</dt> </dl>                                             | Padrões de íris são usados para determinar a identidade de um indivíduo. Esse valor tem suporte a partir do Windows 10.<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**WINBIO \_ tipo \_ retina**</dt> </dl>                                       | Os padrões de sentido na retina são usados para determinar a identidade de um indivíduo.<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**\_geometria do tipo WINBIO \_ \_**</dt> </dl>                 | A forma de uma pessoa de um indivíduo é usada para determinar a identidade de um indivíduo.<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**WINBIO \_ de \_ assinatura do tipo \_ dinâmica**</dt> </dl>  | Os padrões de força que o indivíduo usa quando assinam seu nome são usados para determinar a identidade de um indivíduo.<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**WINBIO \_ de \_ pressionamento de teclas do tipo \_ Dynamics**</dt> </dl>  | Os padrões de velocidade e erro na digitação por um indivíduo são usados para determinar a identidade de um indivíduo.<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**\_movimentação de \_ LIP do tipo WINBIO \_**</dt> </dl>                    | As alterações nos Lips de um indivíduo que ocorrem quando falam são usadas para determinar a identidade de um indivíduo.<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**\_imagem de \_ \_ face térmica do tipo \_ WINBIO**</dt> </dl> | Os padrões de temperatura na face de um indivíduo são usados para determinar a identidade de um indivíduo.<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**\_imagem da \_ \_ mão térmica do tipo \_ WINBIO**</dt> </dl> | Os padrões de temperatura à mão de um indivíduo são usados para determinar a identidade de um indivíduo.<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**WINBIO \_ tipo \_ da**</dt> </dl>                                             | Os padrões de movimento que ocorrem quando as movimentações individuais são usadas para determinar a identidade de um indivíduo.<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**WINBIO \_ tipo \_ odor**</dt> </dl>                                          | O odor de um indivíduo é usado para determinar a identidade de um indivíduo.<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**WINBIO \_ tipo \_ DNA**</dt> </dl>                                                | As sequências do Deoxyribonucleic Acid (DNA) são usadas para determinar a identidade de um indivíduo.<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**\_ \_ forma Ear de tipo WINBIO \_**</dt> </dl>                             | A forma de uma Ear da pessoa é usada para determinar a identidade de um indivíduo.<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**WINBIO \_ tipo \_ de \_ geometria de dedo**</dt> </dl>           | As formas dos dedos de um indivíduo são usadas para determinar a identidade de um indivíduo.<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**WINBIO \_ tipo \_ de \_ impressão Palm**</dt> </dl>                          | A forma do Palm é usada para determinar a identidade de um indivíduo.<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**WINBIO \_ tipo de \_ sentido \_ padrão**</dt> </dl>                    | Os padrões no Veins sob a capa da mão de um indivíduo são usados para determinar a identidade de um indivíduo.<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**\_impressão de \_ pé do tipo WINBIO \_**</dt> </dl>                          | A forma do pé é usada para determinar a identidade de um indivíduo.<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**WINBIO \_ tipo \_ outro**</dt> </dl>                                          | Os dados biométricos com suporte não são definidos pelas constantes atuais.<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**\_senha do tipo WINBIO \_**</dt> </dl>                                 | Os dados de senha são usados para determinar a identidade de um indivíduo.<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**WINBIO \_ tipo \_ any**</dt> </dl>                                                | Qualquer tipo de dados é usado para determinar a identidade de um indivíduo.<br/>                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                                                                                  |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





