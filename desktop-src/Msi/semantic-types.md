---
description: As entradas a seguir nas colunas Format, Type e ContextData da Tabela ModuleConfiguration especificam o tipo semântico de informações que estão sendo substituídas no item configurável especificado na coluna Name desta tabela.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Tipos semânticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01845bd7790f618794816182bb4b11fc0d13baf9216d17bbd15c63a390a52a90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040296"
---
# <a name="semantic-types"></a>Tipos semânticos

As entradas a seguir nas colunas Format, Type e ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md) especificam o tipo semântico de informações que estão sendo substituídas no item configurável especificado na coluna Name desta tabela.

[Tipos de formato de texto](text-format-types.md)



| Formatar | Tipo       | ContextData                                                 | Descrição                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Texto   |            |                                                             | Texto arbitrário. Consulte [tipo de texto arbitrário](arbitrary-text-type.md).                                        |
| Texto   | Enumeração       | <A>=<a>;<B>=<b>;<C>=<c> | Valor selecionado de um conjunto. Consulte [tipo de enumeração](enum-type.md).                                                 |
| Texto   | Formatado  |                                                             | Valor que atende à definição do texto formatado no instalador. Consulte [tipo formatado](formatted-type.md). |
| Texto   | RTF        |                                                             | Uma cadeia de texto RTF. Consulte [tipo de RTF](rtf-type.md).                                                          |
| Texto   | Identificador |                                                             | uma cadeia de texto em conformidade com um [identificador](identifier.md)de Windows Installer.                              |



 

[Tipos de formato de inteiro](integer-format-types.md)



| Formatar  | Tipo | ContextData | Descrição                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Integer |      |             | Qualquer valor inteiro. Consulte [tipo de inteiro arbitrário](arbitrary-integer-type.md). |



 

[Tipos de formato de chave](key-format-types.md)



| Formatar | Tipo      | ContextData      | Descrição                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Chave    | Arquivo      | AssemblyContext  | Permitir que os usuários configurem chaves estrangeiras para assemblies Win32 ou Common Language Runtime. Consulte [tipo de arquivo](file-type.md). |
| Chave    | Binário    | Bitmap           | Chave estrangeira para uma linha de tabela binária que contém um bitmap para uso na interface do usuário. Consulte [tipo de binário](binary-type.md).                  |
| Chave    | Binário    | ícone             | Chave estrangeira para uma linha de tabela binária que contém um ícone para uso na interface do usuário. Consulte [tipo de binário](binary-type.md).                   |
| Chave    | Binário    | EXE              | Chave estrangeira para uma linha de tabela binária que contém um EXE de 32 bits. Consulte [tipo de binário](binary-type.md).                             |
| Chave    | Binário    | EXE64            | Chave estrangeira para uma linha de tabela binária que contém um EXE de 32 ou de 64 bits. Consulte [tipo de binário](binary-type.md).                       |
| Chave    | ícone      | ShortcutIcon     | Chave estrangeira para uma linha de tabela de ícones que contém um ícone para uso por um atalho. Consulte o [tipo de ícone](icon-type.md).                |
| Chave    | caixa de diálogo    | DialogNext       | Chave estrangeira para uma linha da tabela de caixa de diálogo. Consulte [tipo de caixa de diálogo](dialog-type.md).                                                 |
| Chave    | caixa de diálogo    | DialogPrev       | Chave estrangeira para uma linha da tabela de caixa de diálogo. Consulte [tipo de caixa de diálogo](dialog-type.md).                                                 |
| Chave    | Diretório | IsolationDir     | Chave estrangeira para uma linha de tabela de diretório na qual os arquivos isolados pertencem. Consulte [tipo de diretório](directory-type.md).            |
| Chave    | Diretório | ShortcutLocation | Chave estrangeira para uma linha de tabela de diretório na qual um atalho deve ser instalado. Consulte [tipo de diretório](directory-type.md).   |
| Chave    | Propriedade  |                  | Chave estrangeira para uma linha de propriedade. Consulte [tipo de propriedade](property-type.md).                                                 |
| Chave    | Propriedade  | Públicos           | Chave estrangeira para uma linha de propriedade. Consulte [tipo de propriedade](property-type.md).                                                 |
| Chave    | Propriedade  | Privados          | Chave estrangeira para uma linha de propriedade. Consulte [tipo de propriedade](property-type.md).                                                 |



 

[Tipos de formato de campo de bits](bitfield-format-types.md)



| Formatar   | Tipo | ContextData                                  | Descrição                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Indevida |      | <mask>;<A>=<a>;<B> = b | Altera um subconjunto de bits em uma coluna. Consulte [tipo](arbitrary-bitfield-type.md)de campo de bits arbitrário. |



 

 

 



