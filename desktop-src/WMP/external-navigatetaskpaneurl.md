---
title: Método external. NavigateTaskPaneURL
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. NavigateTaskPaneURL
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Windows Media Player do método NavigateTaskPaneURL
- método NavigateTaskPaneURL Windows Media Player, classe externa
- classe externa Windows Media Player, método NavigateTaskPaneURL
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebcf8d799452a9966355f644f00ac5c4aecc4c066374254e8e580431b756b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649026"
---
# <a name="externalnavigatetaskpaneurl-method"></a>Método external. NavigateTaskPaneURL

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **NavigateTaskPaneURL** abre uma página da Web no painel de tarefas especificado e altera o foco para o painel especificado.

## <a name="syntax"></a>Sintaxe


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrKeyName* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome da chave para a loja online. (obrigatório)

</dd> <dt>

*bstrTaskPane* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do painel de tarefas no qual a página da Web é aberta. (obrigatório)

</dd> <dt>

*bstrParams* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém os parâmetros da cadeia de caracteres de consulta a serem acrescentados à URL especificada pelo elemento **Navigate** do documento serviceInfo. (opcional)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Navegar para um painel que sua loja online não suporta pode fazer com que o repositório online atual seja alterado.

O valor especificado para *bstrParams* é válido somente quando **NavigateTaskPaneURL** é chamado a partir de páginas da Web fornecidas pela loja online.

A tabela a seguir lista os valores válidos para *bstrTaskPane* e o painel de tarefas associado para cada um.



| Valor            | Painel de Tarefas                      |
|------------------|--------------------------------|
| **ServiceTask1** | Primeiro painel de tarefas da loja online.  |
| **ServiceTask2** | Segundo painel de tarefas da loja online. |
| **ServiceTask3** | Terceiro painel de tarefas da loja online.  |



 

O código da página da Web deve especificar um valor para [external. SelectedTaskPane](external-selectedtaskpane.md) ao carregar para garantir que o botão correto do painel de tarefas seja realçado após a conclusão da navegação.

## <a name="examples"></a>Exemplos

O código de exemplo a seguir mostra como o **NavigateTaskPaneURL** cria a URL da página da Web a ser exibida para **ServiceTask1**.

Exemplo do elemento **Navigate** :


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



Exemplo de chamada para o método **NavigateTaskPaneURL** :


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



Exemplo de URL resultante usada para a página da Web exibida em **ServiceTask1**:


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External. SelectedTaskPane**](external-selectedtaskpane.md)
</dt> </dl>

 

 





