---
description: O método LogError registra um erro. Os aplicativos não precisam chamar esse método. Ele é chamado internamente em resposta a erros de renderização.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'Método IAMErrorLog:: LogError (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750275"
---
# <a name="iamerrorloglogerror-method"></a>Método IAMErrorLog:: LogError

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método **LogError** registra um erro. Os aplicativos não precisam chamar esse método. Ele é chamado internamente em resposta a erros de renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Gravidade* 
</dt> <dd>

Reservado. Não use.

</dd> <dt>

*ErrorString* 
</dt> <dd>

Valor da cadeia de caracteres que contém o texto do erro.

</dd> <dt>

*ErrorCode* 
</dt> <dd>

Código do erro.

</dd> <dt>

*resultado* 
</dt> <dd>

O valor HRESULT retornado pela chamada de método que causou o erro.

</dd> <dt>

*pExtraInfo* \[ no\]
</dt> <dd>

Ponteiro para uma variante que contém informações adicionais sobre o erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar o valor do parâmetro *HRESULT* .

## <a name="remarks"></a>Comentários

Dentro desse método, não libere a **variante** apontada por *pExtraInfo*. Além disso, a **variante** torna-se inválida depois que o método retorna, portanto, não tente fazer referência posteriormente.

Implemente esse método para retornar o mais rápido possível. Não faça chamadas de função de dentro desse método que possam bloquear a execução do programa. Por exemplo, não chame funções que enviam mensagens de janela, bloqueiem eventos ou, de outra forma, podem bloquear a execução. Isso pode fazer com que o computador pare de responder.

Para obter uma lista de erros definidos pelo DES, juntamente com o significado e o tipo de dados da **variante** apontada por *PExtraInfo*, consulte [erros de renderização](rendering-errors.md).

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMErrorLog**](iamerrorlog.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




