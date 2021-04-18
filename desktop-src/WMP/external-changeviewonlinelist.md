---
title: Método external. changeViewOnlineList
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. changeViewOnlineList
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- método changeViewOnlineList Windows Media Player
- método changeViewOnlineList Windows Media Player, classe externa
- Classe externa Windows Media Player, método changeViewOnlineList
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810553"
---
# <a name="externalchangeviewonlinelist-method"></a>Método external. changeViewOnlineList

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **changeViewOnlineList** altera a exibição no Windows Media Player para exibir uma lista gerada dinamicamente pela loja online.

## <a name="syntax"></a>Sintaxe


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
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

**Cadeia de caracteres** que contém a ID do item específico a ser mostrado na nova exibição. Por exemplo, se *LibraryLocationType* for CPGenreID, esse parâmetro especificará a ID do gênero a ser mostrado na nova exibição. Esta cadeia de caracteres pode estar vazia.

</dd> <dt>

*Parâmetros* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém parâmetros que o Windows Media Player passa para o plug-in do loja online chamando [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate). Esses parâmetros não são interpretados pelo Windows Media Player. Eles são criados pela loja online e têm significado apenas para a loja online. Esta cadeia de caracteres pode estar vazia

</dd> <dt>

*FriendlyName* \[ no\]
</dt> <dd>

A **cadeia de caracteres** que contém um nome amigável, a ser exibida pelo Windows Media Player, para a lista dinâmica.

</dd> <dt>

*ListType* \[ no\]
</dt> <dd>

Uma constante de local de biblioteca que especifica o tipo dos itens na lista gerada dinamicamente. Por exemplo, se o valor desse parâmetro for CPTrackID, a lista dinâmica conterá faixas.

</dd> <dt>

*Modo de exibição* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o modo que o Windows Media Player usará para exibir a lista dinâmica. O chamador deve definir esse parâmetro como um dos valores a seguir, que são definidos em contentpartner. h:

ViewModeReport

ViewModeDetails

ViewModeIcon

ViewModeTile

ViewModeOrderedList

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando o script em uma página de descoberta chama **changeViewOnlineList**, o Windows Media Player passa alguns dos parâmetros para os métodos [IWMPContentPartner:: GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) e [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , que são implementados pelo plug-in da loja online. A tabela a seguir mostra a correspondência entre os parâmetros dos três métodos.



| parâmetro changeViewOnlineList | Parâmetro GetListContents | Parâmetro GetTemplate |
|--------------------------------|---------------------------|-----------------------|
| *LocalType*                 | *local*                | *local*            |
| *LocationID*                   | *pContext*                | *pContext*            |
| *Params*                       | *bstrParams*              | *bstrViewParams*      |
| *ListType*                     | *bstrListType*            | não aplicável        |



 

Como todos os três métodos mostrados na tabela anterior são implementados pela loja online, você tem alguma flexibilidade em como usar os parâmetros. A ideia é que você forneça informações suficientes para **GetListContents** para determinar qual lista deve ser recuperada e para **GetTemplate** para determinar qual página de descoberta deve ser exibida em seguida. Os exemplos a seguir ilustram duas possibilidades.

**Exemplo 1: uma lista dinâmica que está no catálogo da loja online**

Suponha que você queira que o plug-in obtenha o conteúdo da lista dinâmica que tem uma ID de 6 no catálogo da loja online. Suponha que a lista 6 seja uma lista de faixas. Você pode fornecer o plug-in com informações suficientes fazendo a seguinte chamada.


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



Observe que o parâmetro *params* está vazio; o plug-in tem informações suficientes nos outros parâmetros.

**Exemplo 2: uma lista dinâmica que não está no catálogo da loja online**

Suponha que você deseja que o plug-in obtenha o conteúdo de uma lista dinâmica que não esteja no catálogo da loja online. Talvez você tenha decidido ter uma lista dinâmica que inclui as músicas escolhidas por um determinado artista. Suponha que o artista tenha uma ID de 2 no catálogo da loja online. Você pode fazer a chamada a seguir.


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



Observe que os parâmetros *LocationType* e *LocationID* não especificam a lista. Em vez disso, o parâmetro *params* especifica a lista. Os parâmetros *LocationType* e *LocationID* são passados para **IWMPContentPartner:: GetListContents**, mas, nesse caso, **GetListContents** podem ignorá-los. Os parâmetros *LocationType* e *LocationID* também são passados para **IWMPContentPartner:: GetTemplate**, que podem usá-los para determinar qual página de descoberta deve ser exibida com a lista dinâmica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartnerCallback::AddListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[**IWMPContentPartner:: GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**Local e item selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 





