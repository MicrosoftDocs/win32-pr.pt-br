---
title: Propriedade de domínio IWMPDVD
description: A propriedade de domínio obtém o domínio atual do DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- propriedade de domínio Windows Media Player
- propriedade de Windows Media Player , interface IWMPDVD
- Interface IWMPDVD Windows Media Player , propriedade de domínio
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
ms.openlocfilehash: b5b5f382d7c1db820905b45b924105225c0c5b55a569f85707e4e9f729e59596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000466"
---
# <a name="iwmpdvddomain-property"></a>Propriedade IWMPDVD::d omain

A **propriedade** de domínio obtém o domínio atual do DVD.

## <a name="syntax"></a>Syntax


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System.String** que é um dos valores a seguir.



| Valor                                                                                        | Significado                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>firstPlay</dt> </dl>         | Executando a inicialização padrão de um disco de DVD.<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | Exibindo menus para todo o disco. Também conhecido como topMenu para Windows Media Player. Normalmente chamado de menu de título ou o menu superior.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Exibindo menus para o conjunto de título atual. Também conhecido como titleMenu para Windows Media Player. Normalmente chamado de menu raiz.<br/>          |
| <dl> <dt>title</dt> </dl>             | Normalmente, exibindo o título atual.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | O Navegador de DVD está no domínio parar DVD.<br/>                                                                                          |
| <dl> <dt>Indefinido</dt> </dl>         | Windows Media Player não está em nenhum domínio de DVD.<br/>                                                                                        |



 

## <a name="remarks"></a>Comentários

Cada DVD é gravado de forma diferente. Alguns DVDs não contêm os domínios firstPlay, videoManagerMenu ou videoTitleSetMenu.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





