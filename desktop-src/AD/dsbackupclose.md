---
title: Função DsBackupClose (Ntdsbcli.h)
description: Fecha um arquivo de backup aberto com a função DsBackupOpenFile.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Função DsBackupClose Active Directory
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c9c8931d67b33fdad1f9e3605ee6efe801dac988d3931d96d1417561c093b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192184"
---
# <a name="dsbackupclose-function"></a>Função DsBackupClose

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Começando com Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A **função DsBackupClose** fecha um arquivo de backup aberto com a [**função DsBackupOpenFile.**](dsbackupopenfile.md) Para cada alça de backup, apenas um arquivo pode ser aberto por vez, portanto, essa função fecha o arquivo aberto no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hbc* \[ Em\]
</dt> <dd>

Contém o alça de contexto de backup obtido com a [**função DsBackupPrepare.**](dsbackupprepare.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro Win32 ou RPC caso contrário. A lista a seguir lista outros códigos de erro possíveis.

<dl> <dt>

**ERRO \_ PARÂMETRO \_ INVÁLIDO**
</dt> <dd>

*hbc* não é válido.

</dd> <dt>

**hrInvalidHandle**
</dt> <dd>

Nenhum arquivo está aberto no momento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[Fazer o back-up de um servidor do Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

