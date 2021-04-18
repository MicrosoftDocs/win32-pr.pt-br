---
description: A interface IAMTimelineTrack fornece métodos para manipular objetos Track em serviços de edição do DirectShow (DES). Uma faixa contém uma lista de fontes que são processadas na saída final.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interface IAMTimelineTrack (QEdit. h)
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
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767675"
---
# <a name="iamtimelinetrack-interface"></a>Interface IAMTimelineTrack

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineTrack` interface fornece métodos para manipular objetos *Track* nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).

Uma faixa contém uma lista de fontes que são processadas na saída final. As fontes dentro da mesma faixa não podem se sobrepor. As faixas de vídeo podem ter efeitos e transições. O mecanismo de renderização aplica efeitos antes de aplicar transições. As faixas de áudio podem ter efeitos, mas não transições. Para obter mais informações, consulte [o modelo de linha do tempo](the-timeline-model.md).

Para criar um objeto Track, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha do tempo \_ Major \_ tipo \_ Track. Você pode consultar o ponteiro **IAMTimelineObj** retornado para a `IAMTimelineTrack` interface.

## <a name="members"></a>Membros

A interface **IAMTimelineTrack** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTrack** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineTrack** tem esses métodos.



| Método                                                          | Descrição                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AreYouBlank**](iamtimelinetrack-areyoublank.md)             | Determina se a faixa está em branco (não contém nenhum objeto de origem).<br/>                                                                       |
| [**GetNextSrc**](iamtimelinetrack-getnextsrc.md)               | Pesquisa o roteiro da próxima fonte que aparece na hora especificada ou posteriormente.<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | Pesquisa o roteiro da próxima fonte que aparece na hora especificada ou posteriormente, com o fornecido como um valor de [**REFTIME**](reftime.md) .<br/> |
| [**GetNextSrcEx**](iamtimelinetrack-getnextsrcex.md)           | Recupera a próxima fonte após a origem especificada.<br/>                                                                                     |
| [**GetSourcesCount**](iamtimelinetrack-getsourcescount.md)     | Recupera o número de fontes no roteiro.<br/>                                                                                             |
| [**GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)           | Recupera o objeto de origem mais próximo ao horário especificado, de acordo com as condições de limite especificadas.<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | Recupera o objeto de origem mais próximo ao tempo especificado, dado como um valor [**REFTIME**](reftime.md) .<br/>                                   |
| [**InsertSpace**](iamtimelinetrack-insertspace.md)             | Divide todos os objetos existentes na hora especificada e insere o espaço entre eles.<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | Divide todos os objetos existentes na hora especificada e insere o espaço entre eles, usando valores de [**REFTIME**](reftime.md) .<br/>              |
| [**MoveEverythingBy**](iamtimelinetrack-moveeverythingby.md)   | Não há suporte.<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | Não há suporte.<br/>                                                                                                                            |
| [**SrcAdd**](iamtimelinetrack-srcadd.md)                       | Adiciona uma origem à faixa.<br/>                                                                                                               |
| [**ZeroBetween**](iamtimelinetrack-zerobetween.md)             | Remove tudo da faixa entre os horários especificados.<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | Remove tudo da faixa entre os horários especificados, fornecidos como valores de [**REFTIME**](reftime.md) .<br/>                                |



 

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



 

 
