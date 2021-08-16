---
title: Função DsBackupRead (Ntdsbcli. h)
description: Lê um bloco de dados do arquivo aberto atual em um buffer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Função DsBackupRead Active Directory
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b5ea4da5b004bb4584eb119419b8c89658f36fed7e8c47514bae47d44e31b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429998"
---
# <a name="dsbackupread-function"></a>Função DsBackupRead

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. a partir do Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsBackupRead** lê um bloco de dados do arquivo aberto atual em um buffer. O aplicativo cliente deve chamar essa função repetidamente até que todo o arquivo de backup tenha sido recebido. A função [**DsBackupOpenFile**](dsbackupopenfile.md) fornece todo o tamanho do arquivo de backup.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HBC* \[ no\]
</dt> <dd>

Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pvBuffer* \[ no\]
</dt> <dd>

Ponteiro para um buffer que recebe os dados. Esse buffer deve ter pelo menos *cbBuffer* bytes de tamanho.

</dd> <dt>

*cbBuffer* \[ no\]
</dt> <dd>

Contém o tamanho, em bytes, do buffer em *pvBuffer*. Esse valor deve ser um múltiplo de 8192 e deve ser maior ou igual a 24576.

</dd> <dt>

*pcbRead* \[ fora\]
</dt> <dd>

Ponteiro para um valor **DWORD** que recebe o número real de bytes lidos. Isso pode ser menor que o número de bytes solicitados porque alguns transportes fragmentam o buffer que está sendo transmitido em vez de preencher todo o buffer com os dados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC. Os códigos de erro possíveis incluem o seguinte.

<dl> <dt>

**\_parâmetro inválido de erro \_**
</dt> <dd>

Um ou mais parâmetros não são válidos.

</dd> <dt>

**identificador de erro \_ \_ EOF**
</dt> <dd>

O fim do arquivo de backup foi atingido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Fazendo backup de um servidor de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

