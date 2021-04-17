---
description: O método Merge do objeto Database mescla o banco de dados de referência com o banco de dados base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Método Database. Merge
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748597"
---
# <a name="databasemerge-method"></a>Método Database. Merge

O método **Merge** do objeto [**Database**](database-object.md) mescla o banco de dados de referência com o banco de dados base.

## <a name="syntax"></a>Sintaxe


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*reference* 
</dt> <dd>

O objeto de [**banco de dados**](database-object.md) necessário a ser mesclado no banco de dados.

</dd> <dt>

*errotable* 
</dt> <dd>

Um nome opcional de uma tabela para conter os nomes das tabelas que contêm conflitos de mesclagem, o número de linhas conflitantes dentro da tabela e uma referência à tabela com o conflito de mesclagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A função [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) e o método **Merge** do objeto [**Database**](database-object.md) não podem ser usados para mesclar um módulo incluído em um pacote de instalação. Eles não devem ser usados para mesclar [módulos de mesclagem](merge-modules.md) em um pacote Windows Installer. Para incluir um módulo de mesclagem em um pacote de instalação, os autores de pacotes de instalação devem seguir as diretrizes descritas no tópico [aplicando módulos de mesclagem](applying-merge-modules.md) .

O método **Merge** não copia [arquivos de gabinete](cabinet-files.md) inseridos ou [transformações incorporadas](embedded-transforms.md) do banco de dados de referência para o banco de dados de destino. Os fluxos de dados inseridos que estão listados na tabela [binária](binary-table.md) ou na [tabela de ícones](icon-table.md) são copiados do banco de dado de referência para o banco de dados de destino. Os armazenamentos inseridos no banco de dados de referência não são copiados para o banco de dados de destino.

Se nenhuma tabela for fornecida, a mensagem de erro geral fornecerá o número de tabelas que contêm conflitos de mesclagem. Qualquer tabela pode ser passada, mas todas as outras colunas devem ser anuláveis porque a operação para atualizar a [tabela de erros](error-table.md) falhará se uma coluna não for anulável. Uma tabela recém-criada também pode ser passada porque o método **Merge** cria automaticamente as colunas que ele usa se forem encontrados conflitos de mesclagem. Duas colunas são usadas para apresentar conflitos de mesclagem. A primeira coluna é o nome da tabela e a coluna de chave primária. A segunda coluna é o número de linhas dessa tabela que têm falhas de mesclagem.

Se as tabelas com o mesmo nome em ambos os bancos de dados não corresponderem no número de chaves primárias, nos tipos de coluna, no número de colunas ou nos nomes de coluna, o método de **mesclagem** falhará e lançará uma mensagem de erro informando o que ocorreu.

Para que a tabela de erros permaneça, o manipulador de erros deve confirmar o banco de dados ao qual a tabela de erro pertence. No entanto, essa confirmação deve ser feita depois de usar a terceira coluna para obter as referências a essas tabelas em que ocorreram conflitos de mesclagem.

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




