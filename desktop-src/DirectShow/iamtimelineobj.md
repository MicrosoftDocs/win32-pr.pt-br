---
description: A interface IAMTimelineObj fornece métodos para manipular objetos de linha do tempo em DES (serviços de edição do DirectShow).
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: Interface IAMTimelineObj (QEdit. h)
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
ms.openlocfilehash: e968ec01d937aeac9a5838b75462a6d23a632512
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759443"
---
# <a name="iamtimelineobj-interface"></a>Interface IAMTimelineObj

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineObj` interface fornece métodos para manipular objetos de linha do tempo nos [serviços de edição do DirectShow](directshow-editing-services.md) (des). Todos os objetos de linha do tempo implementam esse método, incluindo objetos de origem, efeito, transição, faixa, grupo e composição. Crie um objeto de linha do tempo chamando o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .

## <a name="members"></a>Membros

A interface **IAMTimelineObj** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineObj** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineObj** tem esses métodos.



| Método                                                          | Descrição                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearDirty**](iamtimelineobj-cleardirty.md)                 | Não há suporte.<br/>                                                                                                              |
| [**FixTimes**](iamtimelineobj-fixtimes.md)                     | Arredonda as horas de início e de término especificadas para os limites de quadro mais próximos.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Arredonda os horários de início e de término especificados, especificados como valores de [**REFTIME**](reftime.md) , para os limites de quadro mais próximos.<br/> |
| [**GetDirtyRange**](iamtimelineobj-getdirtyrange.md)           | Não há suporte.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | Não há suporte.<br/>                                                                                                              |
| [**GetEmbedDepth**](iamtimelineobj-getembeddepth.md)           | Não há suporte.<br/>                                                                                                              |
| [**GetGenID**](iamtimelineobj-getgenid.md)                     | Recupera o identificador gerado do objeto.<br/>                                                                                |
| [**GetGroupIBelongTo**](iamtimelineobj-getgroupibelongto.md)   | Não há suporte.<br/>                                                                                                              |
| [**Getlocked**](iamtimelineobj-getlocked.md)                   | Recupera o estado de edição do objeto (bloqueado ou desbloqueado).<br/>                                                                  |
| [**Sem mudo**](iamtimelineobj-getmuted.md)                     | Recupera o estado mudo do objeto.<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | Recupera o setter da Propriedade do objeto.<br/>                                                                                     |
| [**GetStartStop**](iamtimelineobj-getstartstop.md)             | Recupera as horas de início e de parada do objeto, em relação ao pai do objeto.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Recupera os horários de início e de parada do objeto, como valores de [**REFTIME**](reftime.md) .<br/>                                          |
| [**GetSubObject**](iamtimelineobj-getsubobject.md)             | Recupera o subobjeto associado a este objeto.<br/>                                                                        |
| [**GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)     | Recupera o GUID do subobjeto associado a este objeto Timeline.<br/>                                                   |
| [**GetSubObjectGUIDB**](iamtimelineobj-getsubobjectguidb.md)   | Recupera o GUID do subobjeto como um valor **BSTR** .<br/>                                                                    |
| [**GetSubObjectLoaded**](iamtimelineobj-getsubobjectloaded.md) | Determina se o ponteiro do subobjeto do objeto foi definido.<br/>                                                             |
| [**GetTimelineNoRef**](iamtimelineobj-gettimelinenoref.md)     | Não há suporte.<br/>                                                                                                              |
| [**Gettimelinetype**](iamtimelineobj-gettimelinetype.md)       | Recupera o tipo do objeto.<br/>                                                                                                |
| [**Getuserdata**](iamtimelineobj-getuserdata.md)               | Recupera os dados persistentes definidos pelo aplicativo.<br/>                                                                          |
| [**GetUserID**](iamtimelineobj-getuserid.md)                   | Recupera o identificador definido pelo aplicativo do objeto.<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | Recupera o nome definido pelo aplicativo do objeto.<br/>                                                                            |
| [**Remover**](iamtimelineobj-remove.md)                         | Remove este objeto da linha do tempo, para reinserção em outro lugar.<br/>                                                           |
| [**RemoveAll**](iamtimelineobj-removeall.md)                   | Remove permanentemente esse objeto da linha do tempo, incluindo subobjetos e filhos.<br/>                                       |
| [**SetDirtyRange**](iamtimelineobj-setdirtyrange.md)           | Não implementado.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Não implementado.<br/>                                                                                                            |
| [**Desbloqueado**](iamtimelineobj-setlocked.md)                   | Define o estado de edição do objeto como bloqueado ou desbloqueado.<br/>                                                                      |
| [**Com mudo**](iamtimelineobj-setmuted.md)                     | Define o estado mudo do objeto.<br/>                                                                                              |
| [**SetPropertySetter**](iamtimelineobj-setpropertysetter.md)   | Define o setter da Propriedade do objeto.<br/>                                                                                          |
| [**SetStartStop**](iamtimelineobj-setstartstop.md)             | Define os horários de início e de término do objeto, em relação à linha do tempo.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Define os horários de início e de parada do objeto, como valores de **REFTIME** .<br/>                                                              |
| [**SetSubObject**](iamtimelineobj-setsubobject.md)             | Não há suporte.<br/>                                                                                                              |
| [**SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md)     | Especifica o GUID (identificador global exclusivo) do subobjeto associado a esse objeto.<br/>                               |
| [**SetSubObjectGUIDB**](iamtimelineobj-setsubobjectguidb.md)   | Especifica o GUID do subobjeto como um valor **BSTR** .<br/>                                                                    |
| [**Settimelinetype**](iamtimelineobj-settimelinetype.md)       | Não há suporte.<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | Define dados persistentes definidos pelo aplicativo.<br/>                                                                                   |
| [**SetUserID**](iamtimelineobj-setuserid.md)                   | Define um identificador definido pelo aplicativo para o objeto.<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | Define um nome definido pelo aplicativo para o objeto.<br/>                                                                            |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
