---
description: O método Mid extrai uma substring de caracteres nCount de comprimento de uma cadeia de caracteres CHString, começando na posição nFirst (com base em zero). O método retorna uma cópia da substring extraída.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: Métodos CHString::Mid (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cbe5b7fc6e3f0d4130e106217c46c82202c230f180dd4c90d09f90073dee08ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319838"
---
# <a name="chstringmid-methods"></a>Métodos CHString::Mid

\[A [**classe CHString**](chstring.md) faz parte do WMI Provider Framework, que agora é considerado no estado final e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estará disponível para problemas não relacionados à segurança que afetam essas bibliotecas. As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O **método Mid** extrai uma substring de caracteres *nCount* de comprimento de uma cadeia [**de caracteres CHString,**](chstring.md) começando na posição *nFirst* (com base em zero). O método retorna uma cópia da substring extraída.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                        | Descrição                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int)) | Extrai uma substring de comprimento e ponto de início especificados.<br/> |
| [**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))         | Extrai uma substring começando em int.<br/>                        |



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
