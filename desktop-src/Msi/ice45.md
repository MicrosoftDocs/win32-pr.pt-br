---
description: ICE45 valida que as colunas de campo de bits no banco de dados não definem nenhum bit reservado como 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169191"
---
# <a name="ice45"></a>ICE45

ICE45 valida que as colunas de campo de bits no banco de dados não definem nenhum bit reservado como 1.

Os bits reservados não fornecem nenhuma funcionalidade nas versões atuais do instalador, mas podem estar em versões futuras. Eles devem ser definidos como 0 para serem compatíveis com as versões futuras do Windows Installer.

## <a name="result"></a>Resultado

ICE45 posta uma mensagem de erro se qualquer uma das tabelas a seguir contiver um campo de bits com um bit reservado definido como um valor de 1.

-   [Tabela BBControl](bbcontrol-table.md)
-   [Tabela de diálogo](dialog-table.md)
-   [Tabela de recursos](feature-table.md)
-   [Tabela de arquivos](file-table.md)
-   [Tabela MoveFile](movefile-table.md)
-   [Tabela ModuleConfiguration](moduleconfiguration-table.md)
-   [Tabela ODBCDataSource](odbcdatasource-table.md)
-   [Tabela de patches](patch-table.md)
-   [Remover tabelafile](removefile-table.md)
-   [Tabela de UserControl](servicecontrol-table.md)
-   [Tabela de desinstalação](serviceinstall-table.md)
-   [Tabela TextStyle](textstyle-table.md)

ICE45 posta uma das duas mensagens de aviso se a [tabela de controle](control-table.md) contiver um campo de bits com um bit reservado definido como um valor de 1.

## <a name="example"></a>Exemplo

ICE45 relata o seguinte erro para o exemplo mostrado.

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

ICE45 relata o seguinte aviso para o exemplo mostrado.

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Atributos |
|-------|------------|
| Arquivo1 | 128        |



 

[Tabela de controle](control-table.md) (parcial)



| caixa de diálogo  | Control | Atributos |
|---------|---------|------------|
| Dialog1 | Edit1   | 2097152    |
| Dialog1 | Edit2   | 1048576    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



