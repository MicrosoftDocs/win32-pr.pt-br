---
description: Abre o banco de dados Shim.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: Função SdbInitDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0504b12254658250820cb3ecac3e9e47ee2a6ca242b15600fa69241b597bb0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666376"
---
# <a name="sdbinitdatabase-function"></a>Função SdbInitDatabase

Abre o banco de dados Shim.

## <a name="syntax"></a>Sintaxe


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro especifica o formato do caminho no parâmetro *pszDatabasePath* . Pode ser um dos seguintes valores.



| Valor                                                                                                                                                                                                                                                      | Significado                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <dt>**HID \_ \_Caminhos dos**</dt> <dt>0x00000001</dt> </dl>                             | Um caminho de estilo MS-DOS.<br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <dt>**HID \_ \_FULLPATH do banco de dados**</dt> <dt>0x00000002</dt> </dl>     | Um caminho completo.<br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <dt>**HID \_ NENHUM \_ banco de dados**</dt> <dt>0x00000004</dt> </dl>                       | O parâmetro *pszDatabasePath* é ignorado e nenhum banco de dados é aberto.<br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <dt>**HID \_ \_ \_ Máscara de tipo de banco de dados**</dt> <dt>0xF00F0000</dt> </dl> | Esse parâmetro especifica um banco de dados predefinido. O parâmetro *pszDatabasePath* é ignorado.<br/> |



 

Se *dwFlags* contiver a **\_ máscara de \_ tipo \_ de dados HID**, esse parâmetro também poderá incluir um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                               | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**Sdb \_ 0x80030000 \_ de \_ Shim principal do banco de dados**</dt> <dt></dt> </dl>          | Banco de dados de correção de aplicativo.<br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**Sdb \_ 0x80020000 \_ principal \_ MSI do banco de dados**</dt> <dt></dt> </dl>             | Banco de dados MSI.<br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**Sdb \_ \_Principais \_ drivers de banco de dados**</dt> <dt>0x80040000</dt> </dl> | Banco de dados de drivers a serem bloqueados.<br/> |



 

</dd> <dt>

*pszDatabasePath* \[ no\]
</dt> <dd>

O caminho para o banco de dados. Esse parâmetro poderá ser **nulo** se o parâmetro *dwFlags* especificar um banco de dados predefinido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna um identificador para o banco de dados aberto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
</dt> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




