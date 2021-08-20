---
description: O construtor de classe WBEMTimeSpan cria um objeto de intervalo de tempo. O construtor está sobrecarregado.
audience: developer
ms.assetid: 337dc247-9904-457a-a1f3-e1cf29b61126
ms.tgt_platform: multiple
title: Construtores WBEMTimeSpan::WbemTimeSpan (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cedd30f887b7cb789f44f06ab2c6d6b93e3d7c4723c7e0189764164bdbb43d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107267"
---
# <a name="wbemtimespanwbemtimespan-constructors"></a>Construtores WBEMTimeSpan::WbemTimeSpan

\[A [**classe WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) faz parte do WMI Provider Framework que agora é considerado no estado final e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estará disponível para problemas não relacionados à segurança que afetam essas bibliotecas. As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O **construtor de classe WBEMTimeSpan** cria um objeto de intervalo de tempo. O construtor está sobrecarregado.

### <a name="overload-list"></a>Lista de sobrecargas



| Construtor                                                                                                 | Descrição                                                                  |
|:------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))                                                      | Cria um objeto de período de tempo não reinicializado.<br/>                        |
| [**WBEMTimeSpan(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))                                               | Inicializa o novo objeto de intervalo de tempo para valor no parâmetro .<br/>   |
| [**WBEMTimeSpan(int,int,int,int,int,int,int,int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int)) | Inicializa o novo objeto de intervalo de tempo para valores nos parâmetros.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2008<br/>                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
