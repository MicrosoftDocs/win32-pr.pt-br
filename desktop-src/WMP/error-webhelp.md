---
title: Erro. método Webhelp
description: o método webhelp inicia a página de ajuda da Web Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero). | Erro. método Webhelp
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- Windows Media Player do método Webhelp
- método webhelp Windows Media Player, classe Error
- classe Error Windows Media Player, método webhelp
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fee647d8f3ddca89ed36c224caab05543715864347700d35ae8e80ee45078cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577870"
---
# <a name="errorwebhelp-method"></a>Erro. método Webhelp

o método **webhelp** inicia a página de ajuda da Web Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero).

## <a name="syntax"></a>Sintaxe


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

as páginas de ajuda da Web sempre contêm as informações mais recentes e mais detalhadas sobre Windows Media Player erros. Esse método transfere automaticamente as outras informações necessárias pela ajuda da Web, como a versão do sistema operacional que está sendo usada.

Para acessar as páginas de ajuda da Web diretamente, use o seguinte código de erro e links do centro de suporte.

-   [Windows Media Player Informações do código de erro](https://support.microsoft.com/kb/886273)
-   [Windows Media Player Centro de soluções](https://support.microsoft.com/ph/7763#tab0)

**Windows Media Player 10 Mobile:** Esse método sempre tem sucesso, mas não executa a operação pretendida.

## <a name="examples"></a>Exemplos

o exemplo a seguir cria um elemento de botão HTML que inicia a página de ajuda da Web do Microsoft Windows Media Player. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Error**](error-object.md)
</dt> </dl>

 

 





