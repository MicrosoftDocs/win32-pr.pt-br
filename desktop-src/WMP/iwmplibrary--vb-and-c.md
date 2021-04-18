---
title: Interface IWMPLibrary (VB e C) (WMP. h)
description: Representa uma biblioteca. A interface IWMPLibrary expõe as propriedades a seguir.
ms.assetid: 956b2da1-5f01-48d6-8faa-e360c225afda
keywords:
- IWMPLibrary (VB e C) interface do Windows Media Player
- IWMPLibrary (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPLibrary (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9749d3a2363c3863180639f249d7261ec1b9694
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758195"
---
# <a name="iwmplibrary-vb-and-c-interface"></a>Interface IWMPLibrary (VB e C#)

Representa uma biblioteca.

A interface **IWMPLibrary** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPLibrary (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPLibrary (VB e C#)** tem esses métodos.



| Método                                                                     | Descrição                                                                                           |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**isidêntico**](wmplibiwmplibrary-iwmplibrary-isidentical--vb-and-c.md) | Retorna um valor que indica se o objeto fornecido é o mesmo que o atual.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IWMPLibrary (VB e C#)** tem essas propriedades.



| Propriedade                                                                                      | Tipo de acesso          | Descrição                                                                   |
|:----------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)<br/> | Somente leitura<br/> | Obtém uma interface **IWMPMediaCollection** para a biblioteca atual.<br/> |
| [**nomes**](wmplibiwmplibrary-iwmplibrary-name--vb-and-c.md)<br/>                       | Somente leitura<br/> | Obtém o nome de exibição da biblioteca atual.<br/>                      |
| [**Escreva**](wmplibiwmplibrary-iwmplibrary-type--vb-and-c.md)<br/>                       | Somente leitura<br/> | Obtém um valor que indica o tipo de biblioteca.<br/>                      |



 

Obtenha uma interface **IWMPLibrary** usando o método a seguir.



| Objeto                                                   | Propriedade                                                         |
|----------------------------------------------------------|------------------------------------------------------------------|
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md) | [**getLibraryByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPLibraryServices. getLibraryByType (VB e C#)**](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md)
</dt> </dl>

 

 





