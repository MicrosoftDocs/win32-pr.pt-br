---
description: Exibe uma interface do usuário selecionada, permitindo que um nome de usuário seja selecionado.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'Método ISCrdEnr:: selectUserName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755044"
---
# <a name="iscrdenrselectusername-method"></a>Método ISCrdEnr:: selectUserName

O método **selectUserName** exibe uma interface do **usuário** selecionada, permitindo que um nome de usuário seja selecionado.

O nome de usuário se aplica ao usuário em cujo nome o registro de certificado é pretendido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado para uso futuro. Defina esse valor como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="vb"></a>VB

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="remarks"></a>Comentários

Use esse método para selecionar o nome do usuário. Depois que um nome de usuário tiver sido selecionado, seu valor poderá ser recuperado chamando o método [**ISCrdEnr:: GetUserName**](iscrdenr-getusername.md) .

Uma alternativa ao uso da interface ' Selecionar usuário ' é especificar um usuário chamando o método [**ISCrdEnr:: SetUserName**](iscrdenr-setusername.md) .

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

[**ISCrdEnr:: SetUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




