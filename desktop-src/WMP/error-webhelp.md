---
title: Erro. método Webhelp
description: O método WebHelp inicia a página de ajuda da Web do Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero). | Erro. método Webhelp
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- método WebHelp do Windows Media Player
- método WebHelp do Windows Media Player, classe de erro
- Classe de erro Windows Media Player, método Webhelp
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
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763351"
---
# <a name="errorwebhelp-method"></a>Erro. método Webhelp

O método **WebHelp** inicia a página de ajuda da Web do Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero).

## <a name="syntax"></a>Sintaxe


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

As páginas de ajuda da Web sempre contêm as informações mais recentes e mais detalhadas sobre erros do Windows Media Player. Esse método transfere automaticamente as outras informações necessárias pela ajuda da Web, como a versão do sistema operacional que está sendo usada.

Para acessar as páginas de ajuda da Web diretamente, use o seguinte código de erro e links do centro de suporte.

-   [Informações de código de erro do Windows Media Player](https://support.microsoft.com/kb/886273)
-   [Centro de soluções do Windows Media Player](https://support.microsoft.com/ph/7763#tab0)

**Windows Media Player 10 Mobile:** Esse método sempre tem sucesso, mas não executa a operação pretendida.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que inicia a página de ajuda da Web do Microsoft Windows Media Player. O objeto de **jogador** foi criado com ID = "Player".


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

 

 





