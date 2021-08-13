---
description: A interface IAMTimelineObj fornece métodos para manipular objetos de linha do tempo DirectShow DeS (Serviços de Edição).
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: Interface IAMTimelineObj (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4a987cfd0f08311a0e7a233ab479e5cdbe2fc649fd521ad4f4ed1b37b6df6d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428156"
---
# <a name="iamtimelineobj-interface"></a>Interface IAMTimelineObj

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A interface fornece métodos para manipular objetos de linha do `IAMTimelineObj` tempo [DirectShow DES (Serviços](directshow-editing-services.md) de Edição). Todos os objetos de linha do tempo implementam esse método, incluindo objetos de origem, efeito, transição, faixa, grupo e composição. Crie um objeto de linha do tempo chamando [**o método IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md)

## <a name="members"></a>Membros

A interface **IAMTimelineObj** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineObj** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineObj** tem esses métodos.



| Método                                                          | Descrição                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearDirty**](iamtimelineobj-cleardirty.md)                 | Sem suporte.<br/>                                                                                                              |
| [**FixTimes**](iamtimelineobj-fixtimes.md)                     | Eleva os horários de início e parada especificados para os limites de quadro mais próximos.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Eleva os horários de início e de parada especificados como [**valores REFTIME**](reftime.md) para os limites de quadro mais próximos.<br/> |
| [**GetDirtyRange**](iamtimelineobj-getdirtyrange.md)           | Sem suporte.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | Sem suporte.<br/>                                                                                                              |
| [**GetEmbedDepth**](iamtimelineobj-getembeddepth.md)           | Sem suporte.<br/>                                                                                                              |
| [**GetGenID**](iamtimelineobj-getgenid.md)                     | Recupera o identificador gerado do objeto.<br/>                                                                                |
| [**GetGroupIBelongTo**](iamtimelineobj-getgroupibelongto.md)   | Sem suporte.<br/>                                                                                                              |
| [**GetLocked**](iamtimelineobj-getlocked.md)                   | Recupera o estado de edição do objeto (bloqueado ou desbloqueado).<br/>                                                                  |
| [**GetMuted**](iamtimelineobj-getmuted.md)                     | Recupera o estado de mute do objeto.<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | Recupera o setter de propriedade do objeto.<br/>                                                                                     |
| [**GetStartStop**](iamtimelineobj-getstartstop.md)             | Recupera os horários de início e parada do objeto, em relação ao pai do objeto.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Recupera os horários de início e de parada do objeto, como [**valores REFTIME.**](reftime.md)<br/>                                          |
| [**GetSubObject**](iamtimelineobj-getsubobject.md)             | Recupera o subobjeto associado a este objeto .<br/>                                                                        |
| [**GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)     | Recupera o GUID do subobjeto associado a este objeto de linha do tempo.<br/>                                                   |
| [**GetSubObjectGUIDB**](iamtimelineobj-getsubobjectguidb.md)   | Recupera o GUID do subobjeto como um **valor BSTR.**<br/>                                                                    |
| [**GetSubObjectLoaded**](iamtimelineobj-getsubobjectloaded.md) | Determina se o ponteiro de subobjeto do objeto foi definido.<br/>                                                             |
| [**GetTimelineNoRef**](iamtimelineobj-gettimelinenoref.md)     | Sem suporte.<br/>                                                                                                              |
| [**GetTimelineType**](iamtimelineobj-gettimelinetype.md)       | Recupera o tipo do objeto.<br/>                                                                                                |
| [**GetUserData**](iamtimelineobj-getuserdata.md)               | Recupera os dados persistentes definidos pelo aplicativo.<br/>                                                                          |
| [**Getuserid**](iamtimelineobj-getuserid.md)                   | Recupera o identificador definido pelo aplicativo do objeto.<br/>                                                                      |
| [**Getusername**](iamtimelineobj-getusername.md)               | Recupera o nome definido pelo aplicativo do objeto.<br/>                                                                            |
| [**Remover**](iamtimelineobj-remove.md)                         | Remove esse objeto da linha do tempo, para reinserção em outro lugar.<br/>                                                           |
| [**Removeall**](iamtimelineobj-removeall.md)                   | Remove permanentemente esse objeto da linha do tempo, incluindo subobjetos e filhos.<br/>                                       |
| [**SetDirtyRange**](iamtimelineobj-setdirtyrange.md)           | Não implementado.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Não implementado.<br/>                                                                                                            |
| [**SetLocked**](iamtimelineobj-setlocked.md)                   | Define o estado de edição do objeto como bloqueado ou desbloqueado.<br/>                                                                      |
| [**SetMuted**](iamtimelineobj-setmuted.md)                     | Define o estado de muted do objeto.<br/>                                                                                              |
| [**SetPropertySetter**](iamtimelineobj-setpropertysetter.md)   | Define o setter de propriedade do objeto.<br/>                                                                                          |
| [**SetStartStop**](iamtimelineobj-setstartstop.md)             | Define os horários de início e parada do objeto em relação à linha do tempo.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Define os horários de início e de parada do objeto, como **valores REFTIME.**<br/>                                                              |
| [**SetSubObject**](iamtimelineobj-setsubobject.md)             | Sem suporte.<br/>                                                                                                              |
| [**SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md)     | Especifica o GUID (identificador global exclusivo) do subobjeto associado a este objeto.<br/>                               |
| [**SetSubObjectGUIDB**](iamtimelineobj-setsubobjectguidb.md)   | Especifica o GUID do subobjeto como um **valor BSTR.**<br/>                                                                    |
| [**SetTimelineType**](iamtimelineobj-settimelinetype.md)       | Sem suporte.<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | Define dados persistentes definidos pelo aplicativo.<br/>                                                                                   |
| [**SetUserID**](iamtimelineobj-setuserid.md)                   | Define um identificador definido pelo aplicativo para o objeto .<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | Define um nome definido pelo aplicativo para o objeto .<br/>                                                                            |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
