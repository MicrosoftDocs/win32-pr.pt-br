---
title: Evento DomainChange do objeto AxWindowsMediaPlayer
description: O evento DomainChange ocorre quando o domínio do DVD é alterado. | Evento DomainChange do objeto AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Evento DomainChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784918"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>Evento DomainChange do objeto AxWindowsMediaPlayer

O evento DomainChange ocorre quando o domínio do DVD é alterado.

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade  | Descrição                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| strDomain | System. StringIndicates o novo domínio. Para obter os valores possíveis, consulte a seção comentários.<br/> |



 

## <a name="remarks"></a>Comentários

A tabela a seguir mostra os valores possíveis para a propriedade strDomain.



| String            | Descrição                                                          |
|-------------------|----------------------------------------------------------------------|
| firstPlay         | Executando a inicialização padrão de um disco de DVD.                     |
| videoManagerMenu  | Exibindo menus para o disco inteiro. Também conhecido como menu raiz ou topMenu. |
| videoTitleSetMenu | Exibindo menus para o conjunto de títulos atual. Também conhecido como titleMenu.     |
| título             | Exibindo o título atual.                                        |
| parar              | O navegador de DVD está no domínio de parada de DVD.                         |



 

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

[**Interface IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





