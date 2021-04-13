---
title: Constantes de WINBIO_IRIS (WinBio \_ Types. h)
description: Especifique os tipos para reconhecimento de íris.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455404"
---
# <a name="winbio_iris-constants"></a>Constantes da íris de WINBIO \_

As seguintes constantes são valores de **\_ \_ subtipo biométrico WINBIO** que podem ser usados para especificar os tipos de reconhecimento de íris além do ANSI INCITS 379-2004: "formato de intercâmbio de imagem íris", que não define nenhum valor de olho à esquerda/direita:



| Constante/valor                                                                                                                                                                                                                                                                   | Descrição                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **\_ Tipo de íris WINBIO \_ \_ desconhecido**</dt> <dt>0</dt> </dl>                       | O tipo de íris é desconhecido. <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **\_ \_ \_ Olho esquerdo WINBIO íris**</dt> <dt>0xF5</dt> </dl>                               | O tipo íris é o olho à esquerda. <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **\_ \_ \_ Olho direito de WINBIO íris**</dt> <dt>0xF6</dt> </dl>                            | O tipo íris é o olho certo. <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**WINBIO \_ \_ \_ Pos \_ 01 não especificado pela íris**</dt> <dt>0xF7</dt> </dl>    | Subtipo associado com o primeiro modelo de um usuário quando apenas um olho é o quadro de câmera e não pode ser determinado se é o olho do usuário para a esquerda ou para a direita.<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **WINBIO \_ do \_ PDV não \_ especificado \_ na íris, 02**</dt> <dt>0xF8</dt> </dl> | Subtipo associado a um modelo do usuário s segundo quando apenas um olho é o quadro da câmera e não pode ser determinado se é o olho do usuário para a esquerda ou para a direita.<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **WINBIO \_ íris \_ 0xF9 \_ Eyes**</dt> <dt></dt> </dl>                             | O tipo íris é ambos os olhos. <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **WINBIO \_ íris \_ \_ olho**</dt> <dt>0xFA</dt> </dl>                          | O tipo de íris é olho. <br/>                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



 

 





