---
description: Recupera o nome do usuário em cujo nome o registro de certificado é pretendido.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'Método ISCrdEnr:: GetUserName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297350"
---
# <a name="iscrdenrgetusername-method"></a>Método ISCrdEnr:: GetUserName

O método **GetUserName** recupera o nome do usuário em cujo nome o registro de certificado é pretendido.

Antes de chamar esse método, você deve especificar o nome de usuário em uma chamada para [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md) ou [**ISCrdEnr:: SetUserName**](iscrdenr-setusername.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse valor deve ser zero (0), SCARTAR \_ \_ \_ nome UPN de registro ou scartar \_ registrar \_ \_ nome compatível com Sam \_ .

Se esse valor for SCARTAR \_ registrar \_ \_ nome UPN, **GetUserName** retornará o nome UPN (Universal principal Name) do usuário, como " someone@example.com ".

Se esse valor for SCARTAR \_ registrar \_ \_ nome compatível com Sam \_ , o método retornará o nome Sam (Security Access Manager) do usuário no formato "domínio \\ usuário".

Se esse valor for zero, o método retornará o nome UPN do usuário, se ele existir. Se o usuário não tiver um nome UPN, o método retornará o nome SAM do usuário.

</dd> <dt>

*pbstrUserName* \[ fora\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que retorna o nome do usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="c"></a>C++

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Cadeia de caracteres que representa o nome do usuário.

## <a name="remarks"></a>Comentários

Você pode especificar o nome do usuário para o qual o [*cartão inteligente*](../secgloss/s-gly.md) é emitido chamando [**ISCrdEnr:: SetUserName**](iscrdenr-setusername.md) ou [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md). Depois que um nome de usuário tiver sido especificado, seu valor poderá ser recuperado chamando **GetUserName**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr:: SetUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 
