---
title: Função DsSetCurrentBackupLog (Ntdsbcli. h)
description: Define o número do log de backup atual após uma restauração bem-sucedida.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Função DsSetCurrentBackupLog Active Directory
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10ac21d1a3cb2501a809b938252414c756bdfbd62f1e142ba3b902cde8c291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191775"
---
# <a name="dssetcurrentbackuplog-function"></a>Função DsSetCurrentBackupLog

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. a partir do Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsSetCurrentBackupLog** define o número do log de backup atual após uma restauração bem-sucedida. Como Active Directory Domain Services dá suporte apenas ao registro em log circular, essa função não é usada normalmente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szServerName* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor para o qual definir o número de log de backup. Barras invertidas precedentes são opcionais. O servidor deve ser o mesmo computador do qual essa função é chamada. O nome do servidor não pode conter nenhum caractere de sublinhado ( \_ ). Um exemplo de um nome de servidor é " \\ \\ Server1".

</dd> <dt>

*dwCurrentLog* \[ no\]
</dt> <dd>

Contém o número do log de backup a ser definido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC. A lista a seguir lista os possíveis códigos de erro.

<dl> <dt>

**\_parâmetro inválido de erro \_**
</dt> <dd>

Um ou mais parâmetros são inválidos.

</dd> <dt>

**ERRO \_ de \_ memória insuficiente \_**
</dt> <dd>

Ocorreu uma falha de alocação de memória.

</dd> </dl>

## <a name="remarks"></a>Comentários

Normalmente, não é necessário chamar a função **DsSetCurrentBackupLog** . As funções de backup determinam e definem automaticamente o backup do último número de log. Use **DsSetCurrentBackupLog** para impedir que outro backup incremental seja realizado com sucesso até que um backup completo seja executado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DsSetCurrentBackupLogW** (Unicode) e **DsSetCurrentBackupLogA** (ANSI)<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fazendo backup e restaurando um servidor de Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

