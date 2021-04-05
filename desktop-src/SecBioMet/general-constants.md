---
title: Constantes gerais (WinBio \_ Types. h)
description: Especifique o comprimento máximo do SID, identificadores, IDs, comprimento máximo da cadeia de caracteres e tamanho máximo do buffer de exemplo.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918446"
---
# <a name="general-constants-winbio_typesh"></a>Constantes gerais (WinBio \_ Types. h)

As constantes a seguir são usadas em todo o Windows Biometric Framework.



| Constante/valor                                                                                                                                                                                                                                                                   | Descrição                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**\_tamanho máximo de \_ SID \_ de segurança**</dt> </dl>                                                                                          | O comprimento máximo de um valor de SID (identificador de segurança). Atualmente, isso é 68.<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**\_ID da unidade WINBIO \_**</dt> </dl>                                                                                                                | Número de identificação de uma unidade biométrica.<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**\_identificador de sessão WINBIO \_**</dt> </dl>                                                                                           | Um inteiro longo sem sinal que contém o identificador para uma sessão biométrica aberta.<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**\_identificador de estrutura WINBIO \_**</dt> </dl>                                                                                     | Um inteiro longo sem sinal que contém o identificador para uma sessão aberta do Framework.<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**UUID de WINBIO \_**</dt> </dl>                                                                                                                          | Uma GUID.<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**\_cadeia de caracteres WINBIO**</dt> </dl>                                                                                                                    | Uma matriz de bytes que contém uma cadeia de caracteres Unicode terminada em nulo.<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**WINBIO \_ \_ \_ comp. máximo de cadeia de caracteres**</dt> </dl>                                                                                       | O comprimento máximo de um valor de **\_ cadeia de caracteres WINBIO** . Atualmente, isso é 256.<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Tamanho máximo do buffer de exemplo**</dt> <dt>0x7FFFFFFF</dt> </dl> | O número máximo de bytes em uma única captura de dados biométricas.<br/>                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





