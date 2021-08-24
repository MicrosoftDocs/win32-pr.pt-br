---
description: O método OpenDatabase do objeto instalador abre um banco de dados existente ou cria um novo, retornando um objeto de banco de dados. Ele gera um erro se o objeto de banco de dados não puder ser criado e aberto com êxito.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Método Installer. OpenDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: aab1e66dd4208817f854db88c57db5b6269a7a0b912242da649dffcf24cabab3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821366"
---
# <a name="installeropendatabase-method"></a>Método Installer. OpenDatabase

O método **OpenDatabase** do objeto [**instalador**](installer-object.md) abre um banco de dados existente ou cria um novo, retornando um objeto de [**banco de dados**](database-object.md) . Ele gera um erro se o objeto de **banco de dados** não puder ser criado e aberto com êxito.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*name* 
</dt> <dd>

Cadeia de caracteres necessária que contém o nome do caminho do banco de dados. Se uma cadeia de caracteres vazia for fornecida, um banco de dados temporário será criado e não persistirá.

</dd> <dt>

*OpenMode* 
</dt> <dd>

Um parâmetro da lista a seguir ou uma cadeia de caracteres que contém o nome do caminho do novo arquivo de banco de dados de saída que deve ser gravado após a confirmação.



| Parâmetro                                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt> </dl>                 | Abre um banco de dados somente leitura, sem alterações persistentes.<br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt> </dl>                 | Abre um banco de dados de leitura/gravação no modo de transação.<br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt> </dl>                         | Abre uma leitura/gravação direta de banco de dados sem transação.<br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt> </dl>                         | Cria um novo banco de dados, leitura/gravação de modo Transact.<br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt> </dl> | Cria um novo banco de dados, modo direto de leitura/gravação.<br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt> </dl>         | Abre um banco de dados para exibir arquivos de script de notificação, como os arquivos gerados pelo método [**CreateAdvertiseScript**](installer-createadvertisescript.md) .<br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt> </dl>            | Adiciona esse sinalizador para indicar um arquivo de patch.<br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um objeto de [**banco de dados**](database-object.md) que representa o banco de dados do instalador novo ou existente que foi aberto.

## <a name="remarks"></a>Comentários

Quando um banco de dados é aberto como a saída de outro banco de dados, o fluxo de informações de resumo do banco de dados de saída é, na verdade, um espelho somente leitura do banco de dados original e, portanto, não pode ser alterado. Além disso, ele não é persistido com o banco de dados. Para criar ou modificar as informações de resumo do banco de dados de saída, ele deve ser fechado e reaberto.

Para fazer e salvar alterações em um banco de dados, primeiro abra o banco de dados na transação (msiOpenDatabaseModeTransact), crie (msiOpenDatabaseModeCreate ou msiOpenDatabaseModeCreateDirect) ou o modo direto (msiOpenDatabaseModeDirect). Depois de fazer as alterações, chame sempre o método [**Commit**](database-commit.md) antes de fechar o identificador do banco de dados. O método **Commit** libera todos os buffers.

Sempre chame o método [**Commit**](database-commit.md) em um banco de dados que tenha sido aberto no modo direto (MsiOpenDatabaseModeDirect ou msiOpenDatabaseModeCreateDirect) antes de fechar o banco de dados. A falha em fazer isso pode corromper o banco de dados.

Como o método **OpenDatabase** inicia o acesso ao banco de dados, ele não pode ser usado com uma instalação em execução.

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




