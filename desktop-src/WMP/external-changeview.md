---
title: Método external. changeView
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método changeView altera a exibição no Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- método changeView Windows Media Player
- método changeView Windows Media Player, classe externa
- Classe externa Windows Media Player, método changeView
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800133"
---
# <a name="externalchangeview-method"></a>Método external. changeView

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **changeView** altera a exibição no Windows Media Player.

## <a name="syntax"></a>Sintaxe


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LibraryLocationType* \[ no\]
</dt> <dd>

Uma [constante de local de biblioteca](library-location-constants.md) que especifica o tipo da nova exibição. Por exemplo, a constante CPGenreID especifica que a nova exibição mostrará um gênero específico.

</dd> <dt>

*LibraryLocationID* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém a ID do item específico a ser mostrado na nova exibição. Por exemplo, se *LibraryLocationType* for CPGenreID, esse parâmetro especificará a ID do gênero a ser mostrado na nova exibição. Esta cadeia de caracteres pode estar vazia. Consulte Observações.

</dd> <dt>

*Filtrar* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o filtro para a nova exibição. O modo de exibição será filtrado como se o usuário tivesse inserido esse texto no controle de roda de palavras do jogador. Esta cadeia de caracteres pode estar vazia.

</dd> <dt>

*ViewParams* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém parâmetros que o Windows Media Player disponibiliza para a nova página de descoberta exibida com a nova exibição. Esses parâmetros não são interpretados pelo Windows Media Player. Eles são criados pela loja online e têm significado apenas para a loja online.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Em alguns casos, faz sentido definir o parâmetro *LibraryLocationID* para a cadeia de caracteres vazia. Por exemplo, se você definir o parâmetro *LibraryLocationType* como AllCPAlbumIDs, o novo modo de exibição representará todos os álbuns. Nenhum álbum individual será o foco da nova exibição, portanto, não há necessidade de fornecer uma ID de álbum no parâmetro *LibraryLocationID* .

O parâmetro *ViewParams* fornece uma maneira para uma página de descoberta se comunicar com outra página de descoberta. Quando o script em uma página de descoberta chama **changeView**, o Windows Media Player ajusta sua interface do usuário. Esse ajuste faz com que o Player chame o método [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) do plug-in para obter a URL de uma nova página de descoberta. A cadeia de caracteres que a página de descoberta original passa no parâmetro *ViewParams* não é passada para **GetTemplate**. No entanto, a página nova descoberta pode recuperar a cadeia de caracteres *ViewParams* chamando [external. viewparameters](external-viewparameters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External. viewparameters**](external-viewparameters.md)
</dt> </dl>

 

 





