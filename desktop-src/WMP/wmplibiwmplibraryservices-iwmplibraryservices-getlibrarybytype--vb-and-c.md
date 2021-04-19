---
title: Método IWMPLibraryServices getLibraryByType
description: O método getLibraryByType retorna uma interface IWMPLibrary que representa a biblioteca que tem o tipo e o índice especificados.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- método getLibraryByType Windows Media Player
- método getLibraryByType Windows Media Player, interface IWMPLibraryServices
- Interface IWMPLibraryServices Windows Media Player, método getLibraryByType
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
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811781"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>Método IWMPLibraryServices:: getLibraryByType

O método **getLibraryByType** retorna uma interface **IWMPLibrary** que representa a biblioteca que tem o tipo e o índice especificados.

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

*wmplt* \[ no\]
</dt> <dd>

Um valor da enumeração **WMPLib. WMPLibraryType** que especifica o tipo de biblioteca a ser recuperada.

</dd> <dt>

*Lindex* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice da biblioteca a ser recuperada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib. IWMPLibrary** para a biblioteca que é retornada.

## <a name="remarks"></a>Comentários

Há apenas uma biblioteca local, e as bibliotecas de discos estão disponíveis somente em CDs de dados e DVDs que contêm conteúdo de mídia.

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

 

 





