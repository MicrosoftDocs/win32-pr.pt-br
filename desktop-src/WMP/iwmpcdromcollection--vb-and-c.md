---
title: Interface IWMPCdromCollection (VB e C) (WMP. h)
description: Fornece uma maneira de organizar e acessar uma coleção de unidades de CD ou DVD. A interface IWMPCdromCollection expõe a propriedade a seguir.
ms.assetid: 60874603-d9c8-4ed1-a92a-bd069bd0c253
keywords:
- IWMPCdromCollection (VB e C) interface do Windows Media Player
- IWMPCdromCollection (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPCdromCollection (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fbc9c053c186b6d542e201f7bee5d2331b649
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788155"
---
# <a name="iwmpcdromcollection-vb-and-c-interface"></a>Interface IWMPCdromCollection (VB e C#)

Fornece uma maneira de organizar e acessar uma coleção de unidades de CD ou DVD.

A interface **IWMPCdromCollection** expõe a propriedade a seguir.

## <a name="members"></a>Membros

A interface **IWMPCdromCollection (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPCdromCollection (VB e C#)** tem esses métodos.



| Método                                                                                                     | Descrição                                                                              |
|:-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**getByDriveSpecifier**](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md) | Retorna uma interface **IWMPCdrom** associada a uma letra de unidade específica.<br/> |
| [**Item**](wmplibiwmpcdromcollection-iwmpcdromcollection-item--vb-and-c.md)                               | Retorna uma interface **IWMPCdrom** no índice fornecido.<br/>                        |



 

### <a name="properties"></a>Propriedades

A interface **IWMPCdromCollection (VB e C#)** tem essas propriedades.



| Propriedade                                                                                  | Tipo de acesso          | Descrição                                                              |
|:------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------|
| [**count**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)<br/> | Somente leitura<br/> | Obtém o número de unidades de CD e DVD disponíveis no sistema.<br/> |



 

Obtenha uma interface **IWMPCdromCollection** usando a propriedade a seguir.



| Objeto                                                                   | Propriedade                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**cdromCollection**](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> </dl>

 

 





