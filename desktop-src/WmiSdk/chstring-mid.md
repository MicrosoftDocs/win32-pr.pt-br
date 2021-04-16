---
description: O método mid extrai uma subcadeia de caracteres nCount de comprimento de uma cadeia de caracteres CHString, começando na posição nPrimeiro (baseada em zero). O método retorna uma cópia da subcadeia de caracteres extraída.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'Métodos CHString:: mid (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772588"
---
# <a name="chstringmid-methods"></a>Métodos CHString:: mid

\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O método **mid** extrai uma subcadeia de caracteres *nCount* de comprimento de uma cadeia de caracteres [**CHString**](chstring.md) , começando na posição *nPrimeiro* (baseada em zero). O método retorna uma cópia da subcadeia de caracteres extraída.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                        | Descrição                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**Mid (int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int)) | Extrai uma subcadeia de caracteres de comprimento e ponto inicial especificados.<br/> |
| [**Mid (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))         | Extrai uma subcadeia de caracteres começando em int.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>ChString. h (incluir FwCommon. h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
