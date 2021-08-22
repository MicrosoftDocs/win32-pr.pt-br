---
description: os operadores de atribuição de classe WBEMTime estão sobrecarregados para facilitar conversões entre vários formatos de tempo de execução de Windows e ANSI C. As várias assinaturas sobrecarregadas são listadas abaixo.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'Operadores WBEMTime:: Operator = (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 321ca0ba75d40389fbd6eb2ba70dc67a9b8e16afd3b5390bbc9ec61bd875c79a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502896"
---
# <a name="wbemtimeoperator-operators"></a>Operadores WBEMTime:: Operator =

\[A classe [**WBEMTime**](wbemtime.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

os operadores de atribuição de classe [**WBEMTime**](wbemtime.md) estão sobrecarregados para facilitar conversões entre vários formatos de tempo de execução de Windows e ANSI C. As várias assinaturas sobrecarregadas são listadas abaixo.

### <a name="overload-list"></a>Lista de sobrecargas



| Operador                                                                     | Descrição                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**operador = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Converte um **BSTR** em formato **WBEMTime** .<br/>         |
| [**Operator = (tempo \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Converte o **tempo \_ t** em formato **WBEMTime** .<br/>        |
| [**Operator = (& FILETIME)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Converte **FILETIME** em formato **WBEMTime** .<br/>       |
| [**Operator = (struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Converte uma estrutura **TM** em formato **WBEMTime** .<br/> |
| [**Operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Converte **SYSTEMTIME** em formato **WBEMTime** .<br/>     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2008<br/>                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
