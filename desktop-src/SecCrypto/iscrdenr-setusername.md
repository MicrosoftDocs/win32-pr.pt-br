---
description: Especifica o nome do usuário em cujo nome o registro de certificado é pretendido.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'Método ISCrdEnr:: SetUserName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758010"
---
# <a name="iscrdenrsetusername-method"></a>Método ISCrdEnr:: SetUserName

O método **SetUserName** especifica o nome do usuário em cujo nome o registro de certificado é pretendido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse valor deve ser SCARTAR \_ \_ \_ nome UPN de registro (definido como 1) ou scartar \_ registrar \_ \_ nome compatível com Sam \_ (definido como 2).

Defina esse valor como SCARTAR \_ registrar \_ \_ nome UPN, se o nome especificado em *bstrUserName* for o nome da entidade universal do usuário, como " someone@example.com ". O nome UPN do usuário deve corresponder a um nome de SAM (Gerenciador de acesso de segurança) existente.

Defina esse valor como SCARTAR \_ registrar \_ \_ nome compatível com Sam \_ , se o nome especificado em *bstrUserName* for o nome Sam do usuário no formato "domínio \\ usuário".

</dd> <dt>

*bstrUserName* \[ no\]
</dt> <dd>

Nome do usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="vb"></a>VB

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="remarks"></a>Comentários

Chame esse método para especificar o nome de usuário a ser emitido pelo [*cartão inteligente*](../secgloss/s-gly.md). Uma alternativa para **SetUserName** é [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md).

Depois que um nome de usuário tiver sido especificado, seu valor poderá ser recuperado chamando [**GetUserName**](iscrdenr-getusername.md).

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

[**ISCrdEnr:: GetUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> </dl>

 

 
