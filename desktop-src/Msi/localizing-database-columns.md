---
description: modifique qualquer uma das outras colunas localizáveis no banco de dados MNPFren.msi usando um editor de tabela como o Orca ou SQL consultas.
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: Localizando colunas de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72d4d4d82f45be66f41710dea7294a63051d69750ade49ae3b66761964b579f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629451"
---
# <a name="localizing-database-columns"></a>Localizando colunas de banco de dados

modifique qualquer uma das outras colunas localizáveis no banco de dados MNPFren.msi usando um editor de tabela como o Orca ou SQL consultas. Para determinar quais colunas de uma determinada tabela podem ser localizadas em outro idioma, consulte o tópico de referência para essa tabela de banco de dados. Consulte [tabelas de banco de dados](database-tables.md) para obter uma lista de todas as tabelas de banco de dados.

Por exemplo, o campo de texto de alguns registros na [tabela de controle](control-table.md) pode precisar ser localizado em francês. A cadeia de caracteres "tem certeza de que deseja cancelar a \[ instalação do ProductName \] ?" na [caixa de diálogo cancelar](cancel-dialog.md) , pode ser modificado nesta tabela para ser exibido em francês. O registro original no arquivo de .msi aparece da seguinte maneira.

[Tabela de controle](control-table.md) (parcial) do arquivo de .msi original



| caixa de diálogo\_  | Control | Type | X   | Y   | Largura | Altura | Atributos | Propriedade | Texto                                                          | \_Próximo controle | Ajuda |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| CancelDlg | Texto    | Texto | 48  | 15  | 194   | 30     | 3          |          | Tem certeza de que deseja cancelar a \[ instalação do ProductName \] ? |               |      |



 

você pode usar um editor de tabela para modificar o campo de texto, como o editor de tabela Orca fornecido com o SDK ou outro editor de tabela, ou usar uma consulta SQL para alterar o campo de texto do registro da tabela de controle. um exemplo que demonstra consultas de banco de dados controladas por script é fornecido no SDK do Windows Installer como o WiRunSQL.vbs do utilitário. Use a linha de comando a seguir para modificar o campo com WiRunSQL.vbs e o Host de Script Windows. consulte também [exemplos de consultas de banco de dados usando SQL e Script](examples-of-database-queries-using-sql-and-script.md).

**Cscript WiRunSQL.vbs MNPFren.msi "controle de conjunto de controle de atualização. Text = ' ETEs-vous sur de vouloir annuler l'installation de \[ ProductName \] ? ' EM que Control. Dialog \_ = ' CancelDlg ' e Control. Control = ' Text ' "**

[Tabela de controle](control-table.md) (parcial) no MNPFren.msi



| caixa de diálogo\_  | Control | Type | X   | Y   | Largura | Altura | Atributos | Propriedade | Texto                                                                | \_Próximo controle | Ajuda |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| CancelDlg | Texto    | Texto | 48  | 15  | 194   | 30     | 3          |          | Êtes-vous sûr de vouloir annuler l'installation de \[ ProductName \] ? |               |      |



 

Se a instalação do MNPFren.msi for cancelada pelo usuário, a **caixa de diálogo de cancelamento** aparecerá exibindo o texto: "Êtes-vous sûr de vouloir annuler L'INSTALLATION de MNP2000?"

Ao usar esse método para localizar o texto da interface do usuário em um idioma diferente, a interface do usuário localizada deve ser testada para garantir que o tamanho dos controles seja grande o suficiente para exibir o texto localizado inteiro. Isso deve ser testado usando todas as configurações de tamanho de fonte que estão disponíveis para exibição. O texto localizado pode exigir mais espaço do que o texto original e pode ser truncado se for exibido em um controle muito pequeno.

[Continuar](updating-productlanguage-and-productcode-properties.md)

 

 



