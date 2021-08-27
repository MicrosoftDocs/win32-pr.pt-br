---
title: Interfaces de persistência
description: Interfaces de persistência
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4894ccb1cc5d17747739e78918da9a5b48e2cca13a9f36078d752fceeaef011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120416"
---
# <a name="persistence-interfaces"></a>Interfaces de persistência

Os objetos que têm um estado persistente de qualquer tipo devem implementar pelo menos uma \* interface IPersist e, preferencialmente, várias interfaces, a fim de fornecer ao contêiner a opção mais flexível de como deseja salvar o estado de um controle.

Se um controle tiver qualquer estado persistente, ele deverá, no mínimo, implementar o [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ou o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) (os dois são mutuamente exclusivos e não devem ser implementados juntos na maior parte). O último é usado quando um controle deseja saber quando ele é criado novo em vez de ser recarregado a partir de um estado persistente existente (**IPersistStream** não tem o novo recurso criado). A existência de qualquer interface indica que o controle pode salvar e carregar seu estado persistente em um fluxo, ou seja, uma instância de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Além dessas duas interfaces baseadas em fluxo, as \* interfaces IPersist listadas na tabela a seguir podem ser fornecidas opcionalmente para dar suporte à persistência a locais diferentes de um [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)expansível.

Um conjunto de categorias de componentes é identificado para cobrir o suporte para interfaces persistências consulte [categorias de componentes](component-categories.md).



| Interface                                                              | Uso                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | O objeto pode salvar e carregar seu estado em uma matriz de bytes sequenciais de comprimento fixo (na memória).<br/>                                                                                                                                                                                                                                                    |
| [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | O objeto pode salvar e carregar seu estado em uma instância de [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) . Os controles que desejam ser marcados como Insertáveis como outros objetos de documento compostos (para inserção em contêineres com reconhecimento de não controle) devem dar suporte a essa interface.<br/>                                                                                               |
| [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)<br/> | O objeto pode salvar e carregar seu estado como propriedades individuais gravadas em IPropertyBag que o contêiner implementa. Isso é usado para a funcionalidade de salvar como texto em alguns contêineres.<br/>                                                                                                                                                          |
| [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | O objeto pode salvar e carregar seu estado em um local nomeado por um moniker. O controle chama [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) para recuperar a interface de armazenamento necessária, como [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/objidl/nn-objidl-ilockbytes), [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), etc.<br/> |



 

Embora o suporte para [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) seja opcional, é altamente recomendável como uma otimização para contêineres com recursos de salvar como texto, como Visual Basic.

Com exceção de [**IPersistStream:: GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax), [**IPersistStreamInit:: GetSizeMax**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)e [**IPersistMemory:: GetSizeMax**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85)), todos os métodos de cada interface devem ser totalmente implementados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

