---
title: Função DsRestoreRegister (Ntdsbcli. h)
description: Registra uma operação de restauração.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Função DsRestoreRegister Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e878a5d2b9567ae7a483344a2240d3480620ea00706db1ed0c834fd2c5553a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962455"
---
# <a name="dsrestoreregister-function"></a>Função DsRestoreRegister

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. a partir do Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsRestoreRegister** registra uma operação de restauração. Essa função interbloqueia todas as operações de restauração subsequentes e impede que o destino de restauração seja iniciado até que a função [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) seja chamada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HBC* \[ no\]
</dt> <dd>

Contém o identificador de contexto de restauração obtido com a função [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*szCheckPointFilePath* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho para o arquivo de ponto de verificação. Esse caminho é fornecido pela função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e tem um valor **BFT** de **BFT de \_ ponto \_ de verificação**. Normalmente, isso é o mesmo que o caminho do banco de dados do sistema. Esse caminho é necessário para a função de restauração de backup apropriada. Este parâmetro não pode ser **nulo**. A passagem de **NULL** nesse parâmetro causará um erro durante o processo de restauração.

</dd> <dt>

*szLogPath* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho onde os arquivos de log serão restaurados. Esse caminho é fornecido pela função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e tem um valor **BFT** de **BFT \_ log \_ dir**. Se o caminho apontar para um diretório vazio, novos arquivos de log serão criados lá. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*rgrstmap* \[ no\]
</dt> <dd>

Uma matriz de [**estruturas \_ RSTMAP EDB**](edb-rstmap.md) que contém os caminhos novos e antigos para cada banco de dados. Há uma estrutura para cada banco de dados. Para o diretório, há uma estrutura para o banco de dados do sistema e outra estrutura para o banco de dados de diretório. A ordem dos elementos na matriz não importa. O parâmetro *crstmap* contém o número de elementos na matriz.

</dd> <dt>

*crstmap* \[ no\]
</dt> <dd>

Contém o número de elementos na matriz *rgrstmap* .

</dd> <dt>

*szBackupLogPath* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho onde os arquivos de log de backup residem atualmente. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*genLow* \[ no\]
</dt> <dd>

Contém o número de log mais baixo a ser restaurado nesta sessão de restauração. Este é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF.

</dd> <dt>

*genHigh* \[ no\]
</dt> <dd>

Contém o número de log mais alto a ser restaurado nesta sessão de restauração. Este é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC. A lista a seguir lista os possíveis códigos de erro.

<dl> <dt>

**ERRO de \_ acesso \_ negado**
</dt> <dd>

O chamador não tem os privilégios de acesso apropriados para chamar essa função. A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> <dt>

**\_parâmetro inválido de erro \_**
</dt> <dd>

Um ou mais parâmetros são inválidos.

</dd> <dt>

**hrMissingExpiryToken**
</dt> <dd>

O token de expiração fornecido a [**DsRestorePrepare**](dsrestoreprepare.md) era inválido. Esse valor é definido em Ntdsbmsg. h.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DsRestoreRegisterW** (Unicode) e **DsRestoreRegisterA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> <dt>

[**\_RSTMAP EDB**](edb-rstmap.md)
</dt> <dt>

[Restaurando o Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

