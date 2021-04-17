---
description: O método Modify do objeto View modifica uma linha de banco de dados com um objeto de registro modificado obtido pelo método Fetch.
ms.assetid: c3c500aa-070f-41d7-90f7-db979452d24f
title: Método View. Modify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Modify
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b4dc97f2e3b5f85d472cfcbfad6017ce4e051e4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748562"
---
# <a name="viewmodify-method"></a>Método View. Modify

O método **Modify** do objeto [**View**](view-object.md) modifica uma linha de banco de dados com um objeto de [**registro**](record-object.md) modificado obtido pelo método [**Fetch**](view-fetch.md) .

## <a name="syntax"></a>Sintaxe


```JScript
View.Modify(
  action,
  record
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*action* 
</dt> <dd>

Ação necessária a ser executada na linha do banco de dados. Essa ação é uma das mostradas na tabela a seguir.



| Nome da ação                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiViewModifySeek"></span><span id="msiviewmodifyseek"></span><span id="MSIVIEWMODIFYSEEK"></span><dl> <dt>**msiViewModifySeek**</dt> <dt>– 1</dt> </dl>                                            | Atualiza as informações no registro fornecido sem alterar a posição no conjunto de resultados e sem afetar as operações de busca subsequentes. O registro pode então ser usado para atualizar, excluir e atualizar subsequentemente. Todas as colunas de chave primária da tabela devem estar na consulta e o registro deve ter pelo menos quantos campos forem a consulta. A busca não pode ser usada com consultas multitabela. Consulte os comentários. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                             |
| <span id="msiViewModifyRefresh"></span><span id="msiviewmodifyrefresh"></span><span id="MSIVIEWMODIFYREFRESH"></span><dl> <dt>**msiViewModifyRefresh**</dt> <dt>0</dt> </dl>                                 | Atualiza as informações no registro. É necessário primeiro chamar o método [**Fetch**](view-fetch.md) com o mesmo registro. Falha para uma linha excluída. Funciona com registros de leitura e gravação e somente leitura.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyInsert"></span><span id="msiviewmodifyinsert"></span><span id="MSIVIEWMODIFYINSERT"></span><dl> <dt>**msiViewModifyInsert**</dt> <dt>1</dt> </dl>                                     | Insere um registro. Falha se existir uma linha com as mesmas chaves primárias. Falha com um banco de dados somente leitura. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="msiViewModifyUpdate"></span><span id="msiviewmodifyupdate"></span><span id="MSIVIEWMODIFYUPDATE"></span><dl> <dt>**msiViewModifyUpdate**</dt> <dt>2</dt> </dl>                                     | Atualiza um registro existente. Somente chaves não primárias. É necessário primeiro chamar o método [**Fetch**](view-fetch.md) com o mesmo registro. Falha com um registro excluído. Funciona somente com registros de leitura/gravação.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyAssign"></span><span id="msiviewmodifyassign"></span><span id="MSIVIEWMODIFYASSIGN"></span><dl> <dt>**msiViewModifyAssign**</dt> <dt>3</dt> </dl>                                     | Grava dados atuais no cursor em uma linha de tabela. Atualiza o registro se as chaves primárias corresponderem a uma linha existente e inserirem se não corresponderem. Falha com um banco de dados somente leitura. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiViewModifyReplace"></span><span id="msiviewmodifyreplace"></span><span id="MSIVIEWMODIFYREPLACE"></span><dl> <dt>**msiViewModifyReplace**</dt> <dt>4</dt> </dl>                                 | Atualiza ou exclui e insere um registro em uma tabela. É necessário primeiro chamar o método [**Fetch**](view-fetch.md) com o mesmo registro. Atualiza o registro se as chaves primárias estiverem inalteradas. Exclui a linha antiga e insere novas se as chaves primárias foram alteradas. Falha com um banco de dados somente leitura. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                                                                                                                                                           |
| <span id="msiViewModifyMerge"></span><span id="msiviewmodifymerge"></span><span id="MSIVIEWMODIFYMERGE"></span><dl> <dt>**msiViewModifyMerge**</dt> <dt>5</dt> </dl>                                         | Insere ou valida um registro em uma tabela. Insere se as chaves primárias não correspondem a nenhuma linha e validam se há uma correspondência. Falha se o registro não corresponder aos dados na tabela. Falha se houver um registro com uma chave duplicada que não seja idêntica. Funciona somente com registros de leitura/gravação. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                                                                                                                                                |
| <span id="msiViewModifyDelete"></span><span id="msiviewmodifydelete"></span><span id="MSIVIEWMODIFYDELETE"></span><dl> <dt>**msiViewModifyDelete**</dt> <dt>6</dt> </dl>                                     | Remove uma linha da tabela. É necessário primeiro chamar o método [**Fetch**](view-fetch.md) com o mesmo registro. Falhará se a linha tiver sido excluída. Funciona somente com registros de leitura/gravação. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyInsertTemporary"></span><span id="msiviewmodifyinserttemporary"></span><span id="MSIVIEWMODIFYINSERTTEMPORARY"></span><dl> <dt>**msiViewModifyInsertTemporary**</dt> <dt>7</dt> </dl> | Insere um registro temporário. As informações não são persistentes. Falha se existir uma linha com a mesma chave primária. Funciona somente com registros de leitura/gravação. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                                                                                                                                                                                                                                                                                           |
| <span id="msiViewModifyValidate"></span><span id="msiviewmodifyvalidate"></span><span id="MSIVIEWMODIFYVALIDATE"></span><dl> <dt>**msiViewModifyValidate**</dt> <dt>8</dt> </dl>                             | Valida um registro. Não valida entre junções. É necessário primeiro chamar o método [**Fetch**](view-fetch.md) com o mesmo registro. Obter erros de validação com o método [**GetError**](view-geterror.md) . Funciona com registros de leitura/gravação e somente leitura. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                                                                                                                                                                                         |
| <span id="msiViewModifyValidateNew"></span><span id="msiviewmodifyvalidatenew"></span><span id="MSIVIEWMODIFYVALIDATENEW"></span><dl> <dt>**msiViewModifyValidateNew**</dt> <dt>9</dt> </dl>                 | Valida um novo registro. Não valida entre junções. Verifica se há chaves duplicadas. Obtém erros de validação chamando o método [**GetError**](view-geterror.md) . Requer a chamada do método [**MsiDatabase. OpenView**](database-openview.md) com um valor de modificação. Funciona com registros de leitura/gravação e somente leitura. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                                                                                                                                 |
| <span id="msiViewModifyValidateField"></span><span id="msiviewmodifyvalidatefield"></span><span id="MSIVIEWMODIFYVALIDATEFIELD"></span><dl> <dt>**msiViewModifyValidateField**</dt> <dt>10</dt> </dl>        | Valida os campos de um registro novo ou buscado. Pode validar um ou mais campos de um registro incompleto. Obtém erros de validação chamando o método [**GetError**](view-geterror.md) . Funciona com registros de leitura/gravação e somente leitura. Esse modo não pode ser usado com uma exibição contendo junções.<br/>                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyValidateDelete"></span><span id="msiviewmodifyvalidatedelete"></span><span id="MSIVIEWMODIFYVALIDATEDELETE"></span><dl> <dt>**msiViewModifyValidateDelete**</dt> <dt>11</dt> </dl>    | Valida um registro que será excluído mais tarde. É necessário primeiro chamar o método [**Fetch**](view-fetch.md) com o mesmo registro. Falha se outra linha se referir às chaves primárias desta linha. A validação não verifica a existência das chaves primárias dessa linha em Propriedades ou cadeias de caracteres. Não verifica se uma coluna é uma chave estrangeira para várias tabelas. Obtenha erros de validação chamando o método [**GetError**](view-geterror.md) . Funciona com registros de leitura/gravação e somente leitura. Esse modo não pode ser usado com uma exibição contendo junções.<br/> |



 

</dd> <dt>

*gravável* 
</dt> <dd>

Obrigatórios. Objeto de [**registro**](record-object.md) obtido pelo método [**Fetch**](view-fetch.md) com dados de campo modificados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método deve ser chamado após o método [**Execute**](view-execute.md) .

Para executar qualquer instrução SQL, é necessário criar uma exibição. No entanto, uma exibição que não cria um conjunto de resultados, como CREATE TABLE ou INSERT INTO, não pode ser usada com o método **Modify** para atualizar tabelas por meio da exibição.

Os valores msiViewModifyValidate, msiViewModifyValidateNew, msiViewModifyValidateField e msiViewModifyValidateDelete do método **Modify** não executam atualizações reais; Eles garantem que os dados no registro sejam válidos. O uso dessas ações requer que o banco de dados contenha uma [ \_ tabela de validação](-validation-table.md) .

Você não pode buscar um registro que contém dados binários de um banco de dado e, em seguida, usar esse registro para inserir os dados em um banco de dado completamente diferente. Você deve exportar os dados para um arquivo e, em seguida, importá-los para o novo banco de dados usando o método [**SetStream**](record-setstream.md) do objeto [**Record**](record-object.md) . Isso garante que cada banco de dados tenha sua própria cópia dos dados binários.

> [!Note]  
> As ações personalizadas só podem adicionar, modificar ou remover linhas, colunas ou tabelas temporárias de um banco de dados. As ações personalizadas não podem modificar dados persistentes em um banco de dados, como os que fazem parte do banco de dado armazenado em disco. Para obter mais informações, consulte [acessando a sessão do instalador atual de dentro de uma ação personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md).

 

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




