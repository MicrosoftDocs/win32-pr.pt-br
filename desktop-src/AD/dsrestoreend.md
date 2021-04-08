---
title: Função DsRestoreEnd (Ntdsbcli. h)
description: Chamado para encerrar uma operação de restauração.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Função DsRestoreEnd Active Directory
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009275"
---
# <a name="dsrestoreend-function"></a>Função DsRestoreEnd

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use o [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

A função **DsRestoreEnd** é chamada para encerrar uma operação de restauração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HBC* \[ no\]
</dt> <dd>

Contém o identificador de contexto de restauração obtido com a função [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC. A lista a seguir lista os possíveis códigos de erro.

<dl> <dt>

**\_parâmetro inválido de erro \_**
</dt> <dd>

*HBC* não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

A função **DsRestoreEnd** fecha identificadores de associação pendentes e executa uma operação de limpeza após uma tentativa de restauração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                                                               |
| Fim do suporte do servidor<br/>    | Nenhum compatível<br/>                                                               |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[Restaurando um servidor de Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

