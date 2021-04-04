---
title: Função DsBackupFree (Ntdsbcli. h)
description: Libera a memória alocada pelas funções de backup e restauração Active Directory Domain Services.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Função DsBackupFree Active Directory
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824346"
---
# <a name="dsbackupfree-function"></a>Função DsBackupFree

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsBackupFree** libera a memória alocada pelas funções de backup e restauração de Active Directory Domain Services. As funções a seguir alocam memória que deve ser liberada com a função **DsBackupFree** .

-   [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
-   [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
-   [**DsBackupPrepare**](dsbackupprepare.md)
-   [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a>Sintaxe


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pvBuffer* \[ no\]
</dt> <dd>

Ponteiro para o buffer de memória a ser liberado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[Fazendo backup de um servidor de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

