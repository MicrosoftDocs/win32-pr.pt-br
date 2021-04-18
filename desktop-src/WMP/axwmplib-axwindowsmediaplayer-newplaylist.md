---
title: Método AxWindowsMediaPlayer. newPlaylist
description: O método newPlaylist retorna uma interface IWMPPlaylist para uma nova lista de reprodução.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- método newPlaylist Windows Media Player
- método newPlaylist Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, método newPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760467"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a>Método AxWindowsMediaPlayer. newPlaylist

O método newPlaylist retorna uma interface IWMPPlaylist para uma nova lista de reprodução.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrName* 
</dt> <dd>

O **System. String** que é o nome da nova lista de reprodução.

</dd> <dt>

*bstrURL* 
</dt> <dd>

O **System. String** que é a URL da playlist do metarquivo do Windows Media que é usada para inicializar a nova lista de reprodução.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface WMPLib. IWMPPlaylist que representa a lista de reprodução recém-criada.

## <a name="remarks"></a>Comentários

Se o parâmetro *bstrURL* for uma cadeia de caracteres nula ou de comprimento zero (""), esse método criará uma **lista de reprodução** vazia. Se o parâmetro *bstrname* for uma cadeia de caracteres de comprimento zero (""), esse método aplicará o nome do metarquivo atual.

A nova lista de reprodução criada com esse método não é adicionada à biblioteca. Para adicionar uma nova lista de reprodução à biblioteca, use IWMPPlaylistCollection. **importPlaylist** ou IWMPPlaylistCollection. **newPlaylist**. Os espaços à esquerda ou à direita no nome da playlist são removidos automaticamente quando adicionados à biblioteca.

Como a biblioteca permite várias listas de reprodução com o mesmo nome, talvez você queira verificar a presença de uma lista de reprodução com um nome específico antes de adicionar uma nova.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. newPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





