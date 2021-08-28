---
title: Constantes de WINBIO_ENG_CAP (WinBio \_ Types. h)
description: Especifique os recursos do mecanismo genérico.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5be1099b6ad555b0547dc975c1446740f43359792c1643d155322095ad26dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867946"
---
# <a name="winbio_eng_cap-constants"></a>\_Constantes do \_ Cap WINBIO ENG

As constantes a seguir são valores de **\_ recursos WINBIO** que podem ser usados para especificar recursos genéricos do componente do mecanismo que está conectado a uma unidade biométrica específica. Você especifica esses recursos no membro **GenericEngineCapabilities** da estrutura [**de \_ \_ \_ informações do mecanismo estendido WINBIO**](winbio-extended-engine-info.md) .



| Constante/valor                                                                                                                                                                                                                                                                                        | Descrição                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Aperfeiçoamento interativo do Cap de ENG**</dt> <dt>0x00000001</dt> </dl> | O componente de mecanismo biométrico pode executar melhorias iterativas.<br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <dt>**WINBIO \_ \_Detecção de \_ spoof \_ de capacidade de ENG**</dt> <dt>0x00000002</dt> </dl>                   | O componente de mecanismo biométrico pode executar a detecção de falsificação.<br/>       |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



 

 





