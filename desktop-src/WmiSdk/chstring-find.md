---
description: O método Find pesquisa uma cadeia de caracteres para a primeira combinação de uma substring.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: Métodos CHString::Find (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a7f326b202d107dc192683517508446b3c785266c675e5cf27d92577311d453a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319990"
---
# <a name="chstringfind-methods"></a>Métodos CHString::Find

\[A [**classe CHString**](chstring.md) faz parte do WMI Provider Framework, que agora é considerado no estado final e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estará disponível para problemas não relacionados à segurança que afetam essas bibliotecas. As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O **método Find** pesquisa uma cadeia de caracteres para a primeira combinação de uma substring.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                          | Descrição                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| [**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))     | Pesquisa o **WSTR** nessa cadeia de caracteres.<br/>    |
| [**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr)) | Pesquisa o **LPCWSTR** nessa cadeia de caracteres.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2008<br/>                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>ChString.h (inclua FwCommon.h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
