---
description: O modelo de classe IMediaObjectImpl fornece uma implementação base para a interface IMediaObject. Para obter mais informações sobre como usar esse modelo, consulte usando o modelo de classe DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Modelo de classe IMediaObjectImpl (Dmoimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759497"
---
# <a name="imediaobjectimpl-class-template"></a>Modelo de classe IMediaObjectImpl

O `IMediaObjectImpl` modelo de classe fornece uma implementação base para a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . Para obter mais informações sobre como usar esse modelo, consulte [usando o modelo de classe DMO](using-the-dmo-class-template.md).

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
| [**Bloquear**](/previous-versions/ms809100(v=msdn.10))                                       | Bloqueia o DMO                                                        |
| [**OutputType**](/previous-versions/ms807644(v=msdn.10))                           | Recupera o tipo de mídia atual para um fluxo de saída especificado.      |
| [**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))                     | Consulta se o tipo de mídia foi definido em um fluxo de saída.          |
| [**Unlock**](/previous-versions/ms809101(v=msdn.10))                                   | Desbloqueia o DMO                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dmoimpl. h</dt> </dl>                                                                     |
| Biblioteca<br/> | <dl> <dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de DMO](dmo-reference.md)
</dt> <dt>

[Usando o modelo de classe DMO](using-the-dmo-class-template.md)
</dt> </dl>

 

 
