---
title: Método getLibraryServices de IWMPLibraryByType
description: O método getLibraryByType retorna uma interface IWMPLibrary que representa a biblioteca que tem o tipo e o índice especificados.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- Método getLibraryByType Windows Media Player
- Método getLibraryByType Windows Media Player interface , IWMPLibraryServices
- Interface IWMPLibraryServices Windows Media Player , método getLibraryByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f83d74c8c03f8b08936c3693c77e211cd87a8b42c2d020c26ee5133406a2a042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746204"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>Método IWMPLibraryServices::getLibraryByType

O **método getLibraryByType** retorna uma interface **IWMPLibrary** que representa a biblioteca que tem o tipo e o índice especificados.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wmplt* \[ Em\]
</dt> <dd>

Um valor da **enumeração WMPLib.WMPLibraryType** que especifica o tipo de biblioteca a ser recuperado.

</dd> <dt>

*lIndex* \[ Em\]
</dt> <dd>

Um **System.Int32** que é o índice da biblioteca a ser recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma interface **WMPLib.IWMPLibrary** para a biblioteca retornada.

## <a name="remarks"></a>Comentários

Há apenas uma biblioteca local e as bibliotecas de disco estão disponíveis apenas em CDs de dados e DVDs que contêm conteúdo de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Interface IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





