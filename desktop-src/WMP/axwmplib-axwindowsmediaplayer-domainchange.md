---
title: Evento DomainChange do objeto AxWindowsMediaPlayer
description: O evento DomainChange ocorre quando o domínio de DVD muda. | Evento DomainChange do objeto AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Evento DomainChange do objeto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: a37f10679225fb893fad8bcf6fc6687021256e305e8c5a08e6ebe96d16b74e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136119"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>Evento DomainChange do objeto AxWindowsMediaPlayer

O evento DomainChange ocorre quando o domínio de DVD muda.

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

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, que contém a propriedade a seguir relacionada a esse evento.



| Propriedade  | Descrição                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| strDomain | System.StringIndica o novo domínio. Para valores possíveis, consulte a seção Comentários.<br/> |



 

## <a name="remarks"></a>Comentários

A tabela a seguir mostra os valores possíveis para a propriedade strDomain.



| String            | Descrição                                                          |
|-------------------|----------------------------------------------------------------------|
| firstPlay         | Executando a inicialização padrão de um disco de DVD.                     |
| videoManagerMenu  | Exibindo menus para o disco inteiro. Também conhecido como Menu Raiz ou topMenu. |
| videoTitleSetMenu | Exibindo menus para o conjunto de título atual. Também conhecido como titleMenu.     |
| título             | Exibindo o título atual.                                        |
| parar              | O Navegador de DVD está no domínio parar DVD.                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





