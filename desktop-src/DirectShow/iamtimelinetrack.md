---
description: A interface IAMTimelineTrack fornece métodos para manipular objetos de controle DirectShow DeS (Serviços de Edição). Uma faixa contém uma lista de fontes renderizadas na saída final.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interface IAMTimelineTrack (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cc33facc22023d6e93c8dcfa3804d111d9c99f49be16d8271b09a7bf938b49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965076"
---
# <a name="iamtimelinetrack-interface"></a>Interface IAMTimelineTrack

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineTrack` interface fornece métodos para manipular objetos *track* [DirectShow DES (Serviços](directshow-editing-services.md) de Edição).

Uma faixa contém uma lista de fontes renderizadas na saída final. As fontes dentro da mesma faixa podem não se sobrepor. As faixas de vídeo podem ter efeitos e transições. O mecanismo de renderização aplica efeitos antes de aplicar transições. As faixas de áudio podem ter efeitos, mas não transições. Para obter mais informações, consulte [O modelo de linha do tempo](the-timeline-model.md).

Para criar um objeto track, chame [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor TIMELINE \_ MAJOR TYPE \_ \_ TRACK. Você pode consultar o ponteiro **IAMTimelineObj** retornado para a `IAMTimelineTrack` interface.

## <a name="members"></a>Membros

A interface **IAMTimelineTrack** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTrack** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineTrack** tem esses métodos.



| Método                                                          | Descrição                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AreYouBlank**](iamtimelinetrack-areyoublank.md)             | Determina se a faixa está em branco (não contém objetos de origem).<br/>                                                                       |
| [**GetNextSrc**](iamtimelinetrack-getnextsrc.md)               | Pesquisa a faixa para a próxima fonte que aparece na hora especificada ou posterior.<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | Pesquisa a faixa para a próxima origem que aparece na hora especificada ou posterior, com o especificado como um [**valor REFTIME.**](reftime.md)<br/> |
| [**GetNextSrcEx**](iamtimelinetrack-getnextsrcex.md)           | Recupera a próxima origem após a origem especificada.<br/>                                                                                     |
| [**GetSourcesCount**](iamtimelinetrack-getsourcescount.md)     | Recupera o número de fontes na faixa.<br/>                                                                                             |
| [**GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)           | Recupera o objeto de origem mais próximo ao tempo especificado, de acordo com as condições de limite especificadas.<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | Recupera o objeto de origem mais próximo ao tempo especificado, dado como um [**valor REFTIME.**](reftime.md)<br/>                                   |
| [**InsertSpace**](iamtimelinetrack-insertspace.md)             | Divide todos os objetos que existem no momento especificado e insere espaço entre eles.<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | Divide todos os objetos que existem no momento especificado e insere espaço entre eles, usando [**valores REFTIME.**](reftime.md)<br/>              |
| [**MoveEverythingBy**](iamtimelinetrack-moveeverythingby.md)   | Sem suporte.<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | Sem suporte.<br/>                                                                                                                            |
| [**SrcAdd**](iamtimelinetrack-srcadd.md)                       | Adiciona uma origem à faixa.<br/>                                                                                                               |
| [**ZeroBetween**](iamtimelinetrack-zerobetween.md)             | Remove tudo da faixa entre os horários especificados.<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | Remove tudo da faixa entre os horários especificados, dados como [**valores REFTIME.**](reftime.md)<br/>                                |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
