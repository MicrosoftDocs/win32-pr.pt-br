---
description: Recupera o status do cache Arquivos Offline.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: Função CSCQueryDatabaseStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748909"
---
# <a name="cscquerydatabasestatus-function"></a>Função CSCQueryDatabaseStatus

\[Essa função não tem suporte e não deve ser usada.\]

Recupera o status do cache Arquivos Offline.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulStatus* 
</dt> <dd>

O status. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                               | Significado                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <dt>**Sinalizador \_ DATABASESTATUS \_ criptografado**</dt> , <dt>0x00000002</dt> </dl>                                      | O cache é marcado para criptografia e todos os arquivos no cache são criptografados.<br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <dt>**Sinalizador \_ DATABASESTATUS \_ 0x00000004 parcialmente \_ criptografado**</dt> <dt></dt> </dl>       | O cache é marcado para criptografia, mas alguns arquivos no cache não são criptografados.<br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <dt>**Sinalizador \_ DATABASESTATUS \_ 0x00000004 parcialmente não \_ criptografado**</dt> <dt></dt> </dl> | O cache não está marcado para criptografia, mas nem todos os arquivos no cache foram descriptografados.<br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <dt>**Sinalizador \_ DATABASESTATUS não \_ criptografado**</dt> <dt>0x00000000</dt> </dl>                                | O cache não está marcado para criptografia e todos os arquivos no cache foram descriptografados.<br/>      |



 

</dd> <dt>

*pulErrors* 
</dt> <dd>

Esse parâmetro é um valor diferente de zero se houver um erro de banco de dados interno ou 0 caso contrário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CSCIsCSCEnabled**](csciscscenabled.md)
</dt> </dl>

 

 
