---
title: Método DownloadItem. getItemInfo
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método getItemInfo recupera o valor de um atributo para o item de download.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, classe DownloadItem
- Classe DownloadItem Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783614"
---
# <a name="downloaditemgetiteminfo-method"></a>Método DownloadItem. getItemInfo

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **getItemInfo** recupera o valor de um atributo para o item de download.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ItemName* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo. Os valores com suporte são AlbumArtist, álbum, Duration, WM/provedor, title, userrating e WM/TrackNumber.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres** que contém o valor do atributo especificado por *ItemName*.

## <a name="remarks"></a>Comentários

Esse método recupera atributos especificados usando a cadeia de caracteres de descrição BITS. Consulte a [Convenção de trabalho bits do Windows Media Player](windows-media-player-bits-job-convention.md).

Esse método tem suporte para download em segundo plano. Seu código não deve chamar esse método ao usar o download em tempo real.

Esse método pode recuperar informações para trabalhos BITS adicionados somente durante a sessão atual do Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DownloadItem. Type**](downloaditem-type.md)
</dt> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





