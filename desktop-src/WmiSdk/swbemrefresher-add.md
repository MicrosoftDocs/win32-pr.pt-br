---
description: O método SWbemRefresher. add adiciona um novo objeto SWbemRefreshableItem à coleção no objeto SWbemRefresher. Objeto SWbemRefreshableItem para a coleção no objeto SWbemRefresher.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Método SWbemRefresher. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782507"
---
# <a name="swbemrefresheradd-method"></a>Método SWbemRefresher. Add

O método **SWbemRefresher. Add** adiciona um novo objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) à coleção no objeto [**SWbemRefresher**](swbemrefresher.md) .

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemService* 
</dt> <dd>

Obrigatórios. Um objeto [**SWbemServices**](swbemservices.md) que representa uma conexão com o namespace no qual o objeto que está sendo adicionado ao atualizador reside.

</dd> <dt>

*strInstancePath* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o caminho relativo do objeto no namespace. O caminho deve conter uma instância. A propriedade [**index**](swbemrefreshableitem-index.md) do [**SWbemRefreshableItem**](swbemrefreshableitem.md) retornado representa o índice do objeto na coleção de atualizadores.

</dd> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém o caminho do objeto do objeto para o qual o método é executado.

</dd> <dt>

*objWbemNamedvalueSet* \[ adicional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a chamada for bem-sucedida, um objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) que contém um único objeto atualizável será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHER CLSID<br/>                                                        |
| IID<br/>                      | ISWbemRefresher de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




