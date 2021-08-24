---
description: O método FormatMessageW sobrecarregado formatará uma cadeia de caracteres de mensagem.
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: Métodos CHString::FormatMessageW (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 53f8a9663994ffbc6b50aebddc7d9877c17c1067a074bcdddbe2fc79bc525e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050934"
---
# <a name="chstringformatmessagew-methods"></a>Métodos CHString::FormatMessageW

\[A [**classe CHString**](chstring.md) faz parte do WMI Provider Framework, que agora é considerado no estado final e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estará disponível para problemas não relacionados à segurança que afetam essas bibliotecas. As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O método **FormatMessageW sobrecarregado formatará** uma cadeia de caracteres de mensagem.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                              | Descrição                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**FormatMessageW(UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))       | Formatar essa mensagem de acordo com o identificador de recurso especificado pelo **UINT.**<br/> |
| [**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---)) | Formatar essa cadeia de caracteres de mensagem de acordo com o formato especificado pelo **LPCWSTR.**<br/>    |



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
