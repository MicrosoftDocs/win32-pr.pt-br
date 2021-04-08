---
title: Constantes de WINBIO_PRESENCE_CHANGE (WinBio \_ Types. h)
description: Descreve os tipos de alterações que podem ocorrer quando o Windows Biometric Framework monitora a presença de indivíduos.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008968"
---
# <a name="winbio_presence_change-constants"></a>Constantes de alteração de \_ presença de WINBIO \_

Descreve os tipos de alterações que podem ocorrer quando o Windows Biometric Framework monitora a presença de indivíduos.



| Constante/valor                                                                                                                                                                                                                                                                                      | Descrição                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ desconhecido**</dt> <dt>0</dt> </dl>           | O tipo de evento é desconhecido. Esse valor é usado para a estrutura não inicializada.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ Atualizar \_ tudo**</dt> <dt>1</dt> </dl> | Fornece informações sobre todas as faces atuais no quadro da câmera.<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**WINBIO \_ \_Chegada do \_ tipo \_ de alteração de presença**</dt> <dt>2</dt> </dl>              | Uma nova face entrou no quadro da câmera.<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ Recognize**</dt> . <dt>3</dt> </dl>     | Uma face foi correspondida a um usuário registrado.<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ parte**</dt> <dt>4</dt> </dl>              | Uma face detectada anteriormente esteve fora do quadro da câmera por um período de tempo.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ Track**</dt> <dt>5</dt> </dl>                 | Fornece informações de atualizações sobre a caixa delimitadora e rejeição de valores de detalhes para um subconjunto das faces que estão atualmente no quadro da câmera.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



 

 





