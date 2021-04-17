---
description: A interface IAMTimelineSrc fornece métodos para manipular e definir propriedades em objetos de origem nos serviços de edição do DirectShow (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interface IAMTimelineSrc (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812827"
---
# <a name="iamtimelinesrc-interface"></a>Interface IAMTimelineSrc

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineSrc` interface fornece métodos para manipular e definir propriedades em objetos de origem nos [serviços de edição do DirectShow](directshow-editing-services.md) (des). Um objeto de origem representa um fluxo de uma fonte de mídia.

Você pode usar uma parte dos dados em um arquivo de origem definindo as horas de início e de parada de mídia. Esses valores especificam o início e o fim do objeto de origem, em relação à origem da mídia original. As horas de mídia podem diferir das horas de início e parada do objeto na linha do tempo, permitindo a reprodução de movimento rápido ou lento. (Com fontes de áudio, ocorre a mudança de densidade.)

Para criar um objeto de origem, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha de tempo \_ principal \_ tipo \_ Source. Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a interface **IAMTimelineSrc** . Para obter mais informações, consulte [construindo uma linha do tempo](constructing-a-timeline.md) e [trabalhando com fontes](working-with-sources.md).

## <a name="members"></a>Membros

A interface **IAMTimelineSrc** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineSrc** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineSrc** tem esses métodos.



| Método                                                    | Descrição                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**FixMediaTimes**](iamtimelinesrc-fixmediatimes.md)     | Arredonda os valores de tempo especificados para o limite de quadro mais próximo.<br/>                               |
| [**FixMediaTimes2**](iamtimelinesrc-fixmediatimes2.md)   | Arredonda os valores de tempo especificados, fornecidos como valores de **REFTIME** , para o limite de quadro mais próximo.<br/> |
| [**GetDefaultFPS**](iamtimelinesrc-getdefaultfps.md)     | Recupera a taxa de quadros padrão do objeto de origem.<br/>                                             |
| [**GetMediaLength**](iamtimelinesrc-getmedialength.md)   | Recupera o tamanho da mídia deste objeto de origem.<br/>                                             |
| [**GetMediaLength2**](iamtimelinesrc-getmedialength2.md) | Recupera o tamanho da mídia desse objeto de origem, como um valor de **REFTIME** .<br/>                     |
| [**Getmedianame**](iamtimelinesrc-getmedianame.md)       | Recupera o nome do arquivo de origem representado por esse objeto de origem.<br/>                      |
| [**GetMediaTimes**](iamtimelinesrc-getmediatimes.md)     | Recupera os horários de início e de término da mídia.<br/>                                                     |
| [**GetMediaTimes2**](iamtimelinesrc-getmediatimes2.md)   | Recupera os horários de início e de parada da mídia, como valores de **REFTIME** .<br/>                              |
| [**GetStreamNumber**](iamtimelinesrc-getstreamnumber.md) | Recupera o número de fluxo atual para o objeto de origem.<br/>                                    |
| [**Getalongamode**](iamtimelinesrc-getstretchmode.md)   | Recupera o modo de ampliação de uma fonte de vídeo.<br/>                                                 |
| [**IsNormalRate**](iamtimelinesrc-isnormalrate.md)       | Indica se o clipe será reproduzido na taxa de reprodução normal.<br/>                             |
| [**ModifyStopTime**](iamtimelinesrc-modifystoptime.md)   | Define a hora de parada, em relação à linha do tempo.<br/>                                                 |
| [**ModifyStopTime2**](iamtimelinesrc-modifystoptime2.md) | Define a hora de parada, como um valor de **REFTIME** .<br/>                                                   |
| [**SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)     | Define a taxa de quadros padrão do objeto de origem.<br/>                                                  |
| [**SetMediaLength**](iamtimelinesrc-setmedialength.md)   | Especifica a duração do arquivo de origem.<br/>                                                    |
| [**SetMediaLength2**](iamtimelinesrc-setmedialength2.md) | Especifica a duração do arquivo de origem, como um valor **REFTIME** .<br/>                            |
| [**Setmedianame**](iamtimelinesrc-setmedianame.md)       | Especifica o nome do arquivo de origem representado por esse objeto de origem.<br/>                      |
| [**SetMediaTimes**](iamtimelinesrc-setmediatimes.md)     | Define as horas de início e de término da mídia.<br/>                                                          |
| [**SetMediaTimes2**](iamtimelinesrc-setmediatimes2.md)   | Define as horas de parada e de início da mídia, como valores de **REFTIME** .<br/>                                   |
| [**SetStreamNumber**](iamtimelinesrc-setstreamnumber.md) | Especifica qual fluxo deve ser lido do arquivo de origem associado a este objeto de origem.<br/>       |
| [**Setstretchmode**](iamtimelinesrc-setstretchmode.md)   | Define o modo de ampliação de uma fonte de vídeo.<br/>                                                      |
| [**SpliceWithNext**](iamtimelinesrc-splicewithnext.md)   | Une esse objeto de origem a outro objeto de origem.<br/>                                            |



 

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



 

 
