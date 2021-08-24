---
description: o construtor da classe WBEMTime facilita as conversões entre vários formatos de tempo de execução de Windows e ANSI C.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'Construtores WBEMTime:: WBEMTime (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ac02e3ee2a7a77ed1cc2cc9157b0d6c191563f234bf594cb53029a76e76f0137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757616"
---
# <a name="wbemtimewbemtime-constructors"></a>Construtores WBEMTime:: WBEMTime

\[A classe [**WBEMTime**](wbemtime.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

o construtor da classe **WBEMTime** facilita as conversões entre vários formatos de tempo de execução de Windows e ANSI C.

### <a name="overload-list"></a>Lista de sobrecargas



| Construtor                                                                 | Descrição                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                                   | Cria um objeto de tempo não inicializado.<br/>                          |
| [**WBEMTime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                           | Inicializa o novo objeto de hora para o valor no parâmetro.<br/> |
| [**WBEMTime (constante de tempo \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))        | Inicializa o novo objeto de hora para o valor no parâmetro.<br/> |
| [**WBEMTime (const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))    | Inicializa o novo objeto de hora para o valor no parâmetro.<br/> |
| [**WBEMTime (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))     | Inicializa o novo objeto de hora para o valor no parâmetro.<br/> |
| [**WBEMTime (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_)) | Inicializa o novo objeto de hora para o valor no parâmetro.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2008<br/>                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
