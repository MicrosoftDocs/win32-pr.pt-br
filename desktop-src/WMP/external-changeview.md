---
title: Método External.changeView
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método changeView altera a exibição Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- Método changeView Windows Media Player
- Método changeView Windows Media Player , classe externa
- Classe externa Windows Media Player , método changeView
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
ms.openlocfilehash: fa982e87e0a25fa8ae6cc80b428524844f60e2ec76f50d246e7b2a76b3ca942a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649366"
---
# <a name="externalchangeview-method"></a>Método External.changeView

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **método changeView** altera a exibição Windows Media Player.

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

*LibraryLocationType* \[ Em\]
</dt> <dd>

Uma [constante de local da](library-location-constants.md) biblioteca que especifica o tipo da nova exibição. Por exemplo, a CONSTANTE CPGenreID especifica que a nova exibição mostrará um gênero específico.

</dd> <dt>

*LibraryLocationID* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém a ID do item específico a ser mostrada na nova exibição. Por exemplo, se *LibraryLocationType* for CPGenreID, esse parâmetro especificará a ID do gênero a ser mostrada na nova exibição. Essa cadeia de caracteres pode estar vazia. Consulte Observações.

</dd> <dt>

*Filtro* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o filtro para a nova exibição. A exibição será filtrada como se o usuário tivesse inserido esse texto no controle de roda de palavras do Player. Essa cadeia de caracteres pode estar vazia.

</dd> <dt>

*ViewParams* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém parâmetros Windows Media Player disponibiliza para a nova página de descoberta que é exibida com a nova exibição. Esses parâmetros não são interpretados por Windows Media Player. Eles são criados pela loja online e têm significado apenas para a loja online.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Em alguns casos, faz sentido definir o parâmetro *LibraryLocationID* como a cadeia de caracteres vazia. Por exemplo, se você definir o parâmetro *LibraryLocationType* como AllCPAlbumIDs, a nova exibição representará todos os álbums. Nenhum álbum individual será o foco da nova exibição, portanto, não há necessidade de fornecer uma ID de álbum no parâmetro *LibraryLocationID.*

O *parâmetro ViewParams* fornece uma maneira de uma página de descoberta se comunicar com outra página de descoberta. Quando o script em uma página de descoberta chama **changeView,** Windows Media Player ajusta sua interface do usuário. Esse ajuste faz com que o Player chame o método [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) do plug-in para obter a URL de uma nova página de descoberta. A cadeia de caracteres que a página de descoberta original passa no *parâmetro ViewParams* não é passada para **GetTemplate.** No entanto, a nova página de descoberta pode recuperar a cadeia de *caracteres ViewParams* chamando [External.viewParameters.](external-viewparameters.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External.viewParameters**](external-viewparameters.md)
</dt> </dl>

 

 





