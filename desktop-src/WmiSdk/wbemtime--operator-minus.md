---
description: 'O operador de subtração de classe WBEMTime (&\# 8211;) foi sobrecarregado para:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'Operadores WBEMTime:: Operator (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771276"
---
# <a name="wbemtimeoperator--operators"></a>Operadores WBEMTime:: Operator

\[A classe [**WBEMTime**](wbemtime.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O operador de subtração da classe [**WBEMTime**](wbemtime.md) () foi sobrecarregado para:

-   Subtraia um período de tempo do tempo de um objeto para produzir um novo objeto de hora que contenha o tempo resultante.
-   Subtraia uma hora do tempo do objeto para produzir um novo objeto de intervalo de tempo que contenha a diferença entre as duas horas.

### <a name="overload-list"></a>Lista de sobrecargas



| Operador                                                                         | Descrição                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**Operator-(WBEMTime&)**](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | Subtrai um **WBEMTime** de um **WBEMTime**.<br/>                         |
| [**Operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_)) | Subtrai um [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) de um **WBEMTime**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
