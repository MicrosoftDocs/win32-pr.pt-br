---
title: Constantes de WINBIO_REJECT_DETAIL (WinBio \_ Types. h)
description: Especifique o motivo pelo qual um procedimento de identificação ou captura de impressão digital biométrica não teve sucesso.
ms.assetid: b1ae4e65-9e53-42dd-99ba-1910b72688dd
topic_type:
- apiref
api_name:
- WINBIO_FP_TOO_HIGH
- WINBIO_FP_TOO_LOW
- WINBIO_FP_TOO_LEFT
- WINBIO_FP_TOO_RIGHT
- WINBIO_FP_TOO_FAST
- WINBIO_FP_TOO_SLOW
- WINBIO_FP_POOR_QUALITY
- WINBIO_FP_TOO_SKEWED
- WINBIO_FP_TOO_SHORT
- WINBIO_FP_MERGE_FAILURE
- WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK
- WINBIO_REJECT_DETAIL_POSITION_MASK
- WINBIO_REJECT_DETAIL_REASON_MASK
- WINBIO_IRIS_POOR_QUALITY
- WINBIO_IRIS_TOO_BRIGHT
- WINBIO_IRIS_TOO_DARK
- WINBIO_IRIS_SPOOF_DETECTED
- WINBIO_IRIS_TOO_SKEWED
- WINBIO_IRIS_TOO_CLOSED
- WINBIO_IRIS_GLARE
- WINBIO_IRIS_DIRTY_LENS
- WINBIO_IRIS_POOR_FOCUS
- WINBIO_IRIS_WRONG_ORIENTATION
- WINBIO_IRIS_TOO_HIGH
- WINBIO_IRIS_TOO_LOW
- WINBIO_IRIS_TOO_LEFT
- WINBIO_IRIS_TOO_RIGHT
- WINBIO_IRIS_TOO_NEAR
- WINBIO_IRIS_TOO_FAR
- WINBIO_FACE_POOR_QUALITY
- WINBIO_FACE_TOO_BRIGHT
- WINBIO_FACE_TOO_DARK
- WINBIO_FACE_SPOOF_DETECTED
- WINBIO_FACE_AMBIGUOUS_TARGET
- WINBIO_FACE_EYES_OCCLUDED
- WINBIO_FACE_WRONG_ORIENTATION
- WINBIO_FACE_TOO_HIGH
- WINBIO_FACE_TOO_LOW
- WINBIO_FACE_TOO_LEFT
- WINBIO_FACE_TOO_RIGHT
- WINBIO_FACE_TOO_NEAR
- WINBIO_FACE_TOO_FAR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d23dcf568e5ed25fb5081283a421b1c0dbb07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645240"
---
# <a name="winbio_reject_detail-constants"></a>\_Constantes de detalhes de rejeição WINBIO \_

As constantes a seguir podem ser usadas para especificar o motivo pelo qual um procedimento de identificação ou captura de impressão digital biométrica não teve sucesso.



| Constante                                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**\_FP WINBIO \_ muito \_ alto**</dt> </dl>                                                                  | A varredura de dedo começou muito alto no dedo.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**\_FP WINBIO \_ muito \_ baixo**</dt> </dl>                                                                     | A varredura de dedo começou muito baixa no dedo.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**\_FP WINBIO \_ muito \_ à esquerda**</dt> </dl>                                                                  | O dedo foi muito distante durante a verificação.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**\_FP WINBIO \_ muito \_ à direita**</dt> </dl>                                                               | O dedo foi muito muito certo durante a verificação.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**\_FP WINBIO \_ muito \_ rápido**</dt> </dl>                                                                  | O dedo foi esdedodo muito rapidamente no sensor.<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**\_FP WINBIO \_ muito \_ lento**</dt> </dl>                                                                  | O dedo estava passando muito lentamente no sensor.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**\_ \_ qualidade ruim de FP WINBIO \_**</dt> </dl>                                                      | A qualidade da verificação era muito ruim.<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**\_FP WINBIO \_ muito \_ distorcido**</dt> </dl>                                                            | O dedo não passou diretamente pelo sensor.<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**\_FP WINBIO \_ muito \_ curto**</dt> </dl>                                                               | Não foi verificada um número suficiente do dedo.<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**\_ \_ falha na mesclagem de FP WINBIO \_**</dt> </dl>                                                   | Não foi possível combinar as capturas de impressão digital.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**WINBIO \_ REJEITAR \_ \_ \_ \_ máscara antifalsificação de detalhes**</dt> </dl> | Essa máscara cobre os 8 bits superiores do valor de detalhe de rejeição em que estão localizados os comportamentos de verificação de tempo de vida. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**WINBIO \_ REJEITAR \_ \_ \_ máscara de posição de detalhes**</dt> </dl>    | Essa máscara cobre o intervalo de bits dedicado a erros de posição. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**\_máscara do \_ motivo do detalhe de REjeição WINBIO \_ \_**</dt> </dl>                       | Essa máscara cobre os 16 bits inferiores em que o motivo enumerado para a rejeição está localizado. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**\_ \_ qualidade insuficiente da íris WINBIO \_**</dt> </dl>                                                | As condições fizeram com que a câmera capturasse uma imagem ruim. Instrua o usuário a limpar o sensor e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**\_íris WINBIO \_ muito \_ brilhante**</dt> </dl>                                                      | A imagem inclui muita luz ambiente para obter uma boa correspondência. Instrua o usuário a garantir que eles não estejam enfrentando outra fonte de luz brilhante. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**\_íris WINBIO \_ muito \_ escuro**</dt> </dl>                                                            | A imagem é muito escura para obter uma boa correspondência. Instrua o usuário a garantir que a íris não fique obscurecida por itens como um vela, óculos escuros ou contatos coloridos. Esse valor tem suporte a partir do Windows 10.<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**\_falsificação de íris WINBIO \_ \_ detectada**</dt> </dl>                                          | O componente de reconhecimento acredita que a íris não está ativa, mas vem de um feed de vídeo reproduzido, uma foto ou um Sculpture 3-D. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**\_íris WINBIO \_ muito \_ distorcido**</dt> </dl>                                                      | O usuário não está olhando diretamente para a câmera. Instrua o usuário a olhar diretamente na câmera e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**\_íris WINBIO \_ muito \_ fechado**</dt> </dl>                                                      | Os eyelids do usuário estão obscurecendo a íris. Instrua o usuário a abrir seus olhos um pouco mais e examinar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**WINBIO \_ íris \_ anti-reflexo**</dt> </dl>                                                                      | A imagem inclui a lente anti-reflexo. Instrua o usuário a remover seus óculos e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**\_ \_ lentes sujas de WINBIO íris \_**</dt> </dl>                                                      | A lente da câmera estava suja. Instrua o usuário a limpar a lente e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**\_ \_ foco insatisfatório WINBIO íris \_**</dt> </dl>                                                      | Esta íris está desfocada. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**\_ \_ orientação incorreta do WINBIO íris \_**</dt> </dl>                                 | A orientação da câmera não corresponde à orientação obrigatória que a estrutura de [**\_ \_ \_ informações do sensor estendido WINBIO**](winbio-extended-sensor-info.md) especifica. Instrua o usuário a alterar a orientação da câmera e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**\_íris WINBIO \_ muito \_ alto**</dt> </dl>                                                            | A íris está voltada para cima. Instrua o usuário a procurar um pouco e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**\_íris WINBIO \_ muito \_ baixo**</dt> </dl>                                                               | A íris está voltada para baixo. Instrua o usuário a procurar um pouco e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**\_íris WINBIO \_ muito \_ à esquerda**</dt> </dl>                                                            | A íris está muito longe à esquerda. Instrua o usuário a procurar um pouco mais à direita e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**\_íris WINBIO \_ muito \_ à direita**</dt> </dl>                                                         | A íris está muito longe à direita. Instrua o usuário a olhar um pouco mais para a esquerda e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**WINBIO \_ íris \_ muito \_ próximo**</dt> </dl>                                                            | A íris está muito perto da câmera. Instrua o usuário a se afastar um pouco mais e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**\_íris WINBIO \_ muito \_ distante**</dt> </dl>                                                               | A íris está muito longe da câmera. Instrua o usuário a mudar um pouco mais de perto e examinar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**WINBIO \_ face \_ baixa \_ qualidade**</dt> </dl>                                                | As condições fizeram com que a câmera capturasse uma imagem ruim. Instrua o usuário a limpar o sensor e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**WINBIO \_ face \_ muito \_ brilhante**</dt> </dl>                                                      | A imagem inclui muita luz ambiente para obter uma boa correspondência. Instrua o usuário a garantir que eles não estejam enfrentando outra fonte de luz brilhante. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**WINBIO \_ facial \_ muito \_ escuro**</dt> </dl>                                                            | A imagem é muito escura para obter uma boa correspondência. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**\_falsificação de face WINBIO \_ \_ detectada**</dt> </dl>                                          | O componente de reconhecimento acredita que a face não está ativa, mas vem de um feed de vídeo reproduzido, uma foto ou uma Sculpture 3D. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**\_ \_ destino ambíguo de WINBIO face \_**</dt> </dl>                                    | Duas ou mais faces estão sobrepostas no quadro da câmera. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**WINBIO \_ facial \_ \_ obstruído**</dt> </dl>                                             | Os olhos do usuário são obstruído. Instrua o usuário a garantir que seus olhos não sejam obscurecidos por itens como um meio, óculos escuros ou contatos coloridos. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**WINBIO \_ face \_ de \_ orientação errada**</dt> </dl>                                 | A orientação da câmera não corresponde à orientação obrigatória que a estrutura de [**\_ \_ \_ informações do sensor estendido WINBIO**](winbio-extended-sensor-info.md) especifica. Instrua o usuário a alterar a orientação da câmera e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**WINBIO \_ facial \_ muito \_ alto**</dt> </dl>                                                            | A face está voltada para cima. Instrua o usuário a procurar um pouco e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**WINBIO \_ facial \_ muito \_ baixo**</dt> </dl>                                                               | A face está voltada para baixo. Instrua o usuário a procurar um pouco e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**WINBIO \_ face para a \_ \_ esquerda**</dt> </dl>                                                            | A face está até a esquerda. Instrua o usuário a mover um pouco mais para a direita e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**WINBIO \_ face para a \_ \_ direita**</dt> </dl>                                                         | A face está para a direita. Instrua o usuário a mover um pouco mais para a esquerda e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**WINBIO \_ rosto \_ muito \_ próximo**</dt> </dl>                                                            | A face está muito próxima da câmera. Instrua o usuário a se afastar um pouco mais e verificar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**WINBIO \_ facial \_ muito \_ longe**</dt> </dl>                                                               | A face está muito longe da câmera. Instrua o usuário a mudar um pouco mais de perto e examinar novamente. Esse valor tem suporte a partir do Windows 10.<br/>                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                                                                                  |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





