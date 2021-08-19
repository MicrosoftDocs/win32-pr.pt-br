---
title: Função DsBackupOpenFile (Ntdsbcli.h)
description: Abre o arquivo especificado e executa as operações de cliente e servidor necessárias para preparar o arquivo para backup.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Função DsBackupOpenFile Active Directory
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6331dc79a93e515d49c688bc8c5dd3b9e747cfbac91ace9c7685a219ae21e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430008"
---
# <a name="dsbackupopenfile-function"></a>Função DsBackupOpenFile

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Começando com Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A **função DsBackupOpenFile** abre o arquivo especificado e executa as operações de cliente e servidor necessárias para preparar o arquivo para backup.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hbc* \[ Em\]
</dt> <dd>

Contém o alça de contexto de backup obtido com a [**função DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*szAttachmentName* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do arquivo de backup a ser aberto.

</dd> <dt>

*cbReadHintSize* \[ Em\]
</dt> <dd>

Contém o tamanho possível, em bytes, do buffer passado como o argumento *pvBuffer* na [**função DsBackupRead.**](dsbackupread.md) As funções de backup usam esse valor como uma dica para otimizar o tráfego de rede. Esse valor deve ser um múltiplo de 8192 e deve ser maior ou igual a 24576.

</dd> <dt>

*widgetFileSize* \[ out\]
</dt> <dd>

Ponteiro para um **valor \_ INTEIRO** GRANDE que recebe o tamanho, em bytes, do arquivo de backup aberto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro Win32 ou RPC caso contrário. A lista a seguir lista outros códigos de erro possíveis.

<dl> <dt>

**ACESSO \_ DE ERRO \_ NEGADO**
</dt> <dd>

O chamador não tem os privilégios de acesso adequados para chamar essa função. A [**função DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> <dt>

**ERRO \_ PARÂMETRO \_ INVÁLIDO**
</dt> <dd>

*hbc*, *szAttachmentName* ou *widgetFileSize* são inválidos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DsBackupOpenFileW** (Unicode) e **DsBackupOpenFileA** (ANSI)<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsBackupRead**](dsbackupread.md)
</dt> <dt>

[Fazer o back-up de um servidor do Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

