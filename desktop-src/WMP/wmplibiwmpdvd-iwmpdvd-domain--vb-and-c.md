---
title: Propriedade de domínio IWMPDVD
description: A propriedade Domain Obtém o domínio atual do DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Propriedade de domínio Windows Media Player
- Propriedade de domínio Windows Media Player, interface IWMPDVD
- Interface IWMPDVD do Windows Media Player, propriedade de domínio
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749553"
---
# <a name="iwmpdvddomain-property"></a>IWMPDVD: Propriedade omain de:d

A propriedade **Domain** Obtém o domínio atual do DVD.

## <a name="syntax"></a>Syntax


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System. String** que é um dos valores a seguir.



| Valor                                                                                        | Significado                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>firstPlay</dt> </dl>         | Executando a inicialização padrão de um disco de DVD.<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | Exibindo menus para todo o disco. Também conhecido como topMenu para o Windows Media Player. Normalmente chamado de menu de título ou do menu superior.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Exibindo menus para o conjunto de títulos atual. Também conhecido como titleMenu para o Windows Media Player. Normalmente chamado de menu raiz.<br/>          |
| <dl> <dt>title</dt> </dl>             | Normalmente, exibindo o título atual.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | O navegador de DVD está no domínio de parada de DVD.<br/>                                                                                          |
| <dl> <dt>indefinido</dt> </dl>         | O Windows Media Player não está em nenhum domínio de DVD.<br/>                                                                                        |



 

## <a name="remarks"></a>Comentários

Cada DVD é criado de maneira diferente. Alguns DVDs não contêm os domínios firstPlay, videoManagerMenu ou videoTitleSetMenu.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





