---
description: O método InsertAt insere um elemento (ou várias cópias de um elemento) ou todos os elementos de outra matriz em um índice especificado.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: Métodos CHStringArray::InsertAt (ChStrArr.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 75332e300987233c0a6f3d6755d27fd7c305a7d86fb6cd9a6143c417222c0dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097246"
---
# <a name="chstringarrayinsertat-methods"></a>Métodos CHStringArray::InsertAt

\[A [**classe CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) faz parte do WMI Provider Framework, que agora é considerado no estado final e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estará disponível para problemas não relacionados à segurança que afetam essas bibliotecas. As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O **método InsertAt** insere um elemento (ou várias cópias de um elemento) ou todos os elementos de outra matriz em um índice especificado.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                               | Descrição                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))       | Insere um ou mais elementos em um índice especificado em uma matriz.<br/>                                               |
| [**InsertAt(int,CHStringArray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray)) | Insere todos os elementos de [**outro CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) em um índice especificado em uma matriz.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2008<br/>                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>ChStrArr.h (inclua FwCommon.h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

�

�
