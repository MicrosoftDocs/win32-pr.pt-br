---
description: O modelo de classe IMediaObjectImpl fornece uma implementação base para a interface IMediaObject. para obter mais informações sobre como usar esse modelo, consulte usando o modelo de classe DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Modelo de classe IMediaObjectImpl (Dmoimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b166836ff4da6100f61fca5d3a0c2887462b37adcbdd2ec61abeb919553a59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015574"
---
# <a name="imediaobjectimpl-class-template"></a>Modelo de classe IMediaObjectImpl

O `IMediaObjectImpl` modelo de classe fornece uma implementação base para a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . para obter mais informações sobre como usar esse modelo, consulte [usando o modelo de classe DMO](using-the-dmo-class-template.md).

Este `IMediaObjectImpl` modelo expõe os membros a seguir.



| Classe aninhada                              | Descrição                                  |
|-------------------------------------------|----------------------------------------------|
| [**LockIt**](imediaobjectimpl-lockit.md) | Classe auxiliar que bloqueia e desbloqueia o DMO. |



 



| Método                                                                      | Descrição                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))                     | Determina se todos os fluxos não opcionais têm tipos de mídia. |
| [**InputType**](/previous-versions/ms807633(v=msdn.10))                             | Recupera o tipo de mídia atual para um fluxo de entrada especificado.       |
| [**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))                       | Consulta se o tipo de mídia foi definido em um fluxo de entrada.           |
| [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))   | Consulta se um fluxo de entrada pode aceitar mais entradas.               |
| [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))   | Consulta se um fluxo de entrada pode aceitar um determinado tipo de mídia.       |
| [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10)) | Consulta se um fluxo de saída pode aceitar um determinado tipo de mídia.      |
| [**Bloqueio**](/previous-versions/ms809100(v=msdn.10))                                       | Bloqueia o DMO                                                        |
| [**OutputType**](/previous-versions/ms807644(v=msdn.10))                           | Recupera o tipo de mídia atual para um fluxo de saída especificado.      |
| [**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))                     | Consulta se o tipo de mídia foi definido em um fluxo de saída.          |
| [**Automático**](/previous-versions/ms809101(v=msdn.10))                                   | Desbloqueia o DMO                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dmoimpl. h</dt> </dl>                                                                     |
| Biblioteca<br/> | <dl> <dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DMO Referência](dmo-reference.md)
</dt> <dt>

[usando o modelo de classe DMO](using-the-dmo-class-template.md)
</dt> </dl>

 

 
