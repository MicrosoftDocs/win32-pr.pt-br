---
description: O método GetLocalOffsetForDate retorna o deslocamento em minutos (+ ou &\# 8211;) entre GMT e hora local para o tempo fornecido no argumento.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Métodos WBEMTime:: GetLocalOffsetForDate (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829260"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a>Métodos WBEMTime:: GetLocalOffsetForDate

\[A classe [**WBEMTime**](wbemtime.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O método **GetLocalOffsetForDate** retorna o deslocamento em minutos (+ ou) entre GMT e hora local para o tempo fornecido no argumento.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                           | Descrição                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| [**GetLocalOffsetForDate (tempo \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))         | O argumento é uma referência a uma **hora \_ t**.<br/>  |
| [**GetLocalOffsetForDate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))     | O argumento é um ponteiro para um **FILETIME**.<br/>   |
| [**GetLocalOffsetForDate (struct tm \* )**](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | O argumento é uma estrutura de ponteiro para **TM** .<br/> |
| [**GetLocalOffsetForDate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime)) | O argumento é um ponteiro para um **SYSTEMTIME**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
