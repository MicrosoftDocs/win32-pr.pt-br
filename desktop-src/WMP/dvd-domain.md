---
title: DVD. Domain
description: A propriedade Domain recupera o domínio atual do DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. Domain do Windows Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295767"
---
# <a name="dvddomain"></a>DVD. Domain

A propriedade **Domain** recupera o domínio atual do DVD.

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** somente leitura que contém um dos valores a seguir.



| String            | Descrição                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| firstPlay         | Executando a inicialização padrão de um disco de DVD.                                                                                      |
| videoManagerMenu  | Exibindo menus para todo o disco. Também conhecido como topMenu para o Windows Media Player. Normalmente chamado de menu de título ou do menu superior. |
| videoTitleSetMenu | Exibindo menus para o conjunto de títulos atual. Também conhecido como titleMenu para o Windows Media Player. Normalmente chamado de menu raiz.              |
| título             | Geralmente exibindo o título atual.                                                                                                 |
| parar              | O navegador de DVD está no domínio de parada de DVD.                                                                                          |
| não definido         | O Player não está em nenhum domínio de DVD.                                                                                                      |



 

## <a name="remarks"></a>Comentários

Cada DVD é criado de maneira diferente. Alguns DVDs não contêm os domínios firstPlay, videoManagerMenu ou videoTitleSetMenu.

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna uma cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Versão<br/>                  | Windows Media Player para Windows XP ou posterior<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> </dl>

 

 





