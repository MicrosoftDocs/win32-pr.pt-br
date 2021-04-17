---
description: Os GUIDs a seguir dão suporte a implementações de CDM (módulo de descriptografia de conteúdo).
title: GUIDs do CDM (Módulo de Descriptografia de Conteúdo)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105808391"
---
# <a name="content-decryption-module-cdm-guids"></a>GUIDs do CDM (Módulo de Descriptografia de Conteúdo)

Os GUIDs a seguir dão suporte a implementações de CDM (módulo de descriptografia de conteúdo).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

GUID de serviço usado para obter interfaces de uma implementação de [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , como a interface [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) do WinRT. Uma implementação de **IMFContentDecryptionModule** deve implementar o [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) e dar suporte a esse GUID de serviço.


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Confira também



- [Media Foundation constantes](media-foundation-constants.md)
- [IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule
- [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




