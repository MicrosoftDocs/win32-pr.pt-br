---
title: Constantes de serviço de texto de TSF diversas (Ctffunc. h)
description: Os valores a seguir são usados com os serviços de texto.
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd4d9cdd73cd42512fe667b84867328c65f13fafa7281341eca7ba6379eef7d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476766"
---
# <a name="miscellaneous-tsf-text-service-constants"></a>Constantes de serviço de texto de TSF diversas

Os valores a seguir são usados com os serviços de texto.



| Constante/valor                                                                                                                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <dt>**TF \_ MENUREADY**</dt> <dt>0x00000001</dt> </dl>                                                | Não usado no momento.<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <dt>**TF \_ PROPUI \_ status \_ SAVETOFILE**</dt> <dt>0x00000001</dt> </dl> | A propriedade pode ser serializada. Se esse valor não estiver presente, a propriedade não poderá ser serializada. Esse valor é usado com [ITfFnPropertyUIStatus:: GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) e [ITfFnPropertyUIStatus:: SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 em Windows 2000 Professional<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Ctffunc. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Ctffunc. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITfFnPropertyUIStatus:: GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[ITfFnPropertyUIStatus:: SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





