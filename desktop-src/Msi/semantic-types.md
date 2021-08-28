---
description: As entradas a seguir nas colunas Format, Type e ContextData da tabela ModuleConfiguration especificam o tipo semântico de informações que estão sendo substituídas no item configurável especificado na coluna Nome desta tabela.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Tipos semânticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234e5dd929991c2ec5fecbc1d2d1bda72f4fbe52
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882649"
---
# <a name="semantic-types"></a>Tipos semânticos

As entradas a seguir nas colunas Format, Type e ContextData da tabela [ModuleConfiguration](moduleconfiguration-table.md) especificam o tipo semântico de informações que estão sendo substituídas no item configurável especificado na coluna Nome desta tabela.

[Tipos de formato de texto](text-format-types.md)



| Formatar | Type       | ContextData                                                 | Descrição                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Texto   |            |                                                             | Texto arbitrário. Consulte [Tipo de texto arbitrário](arbitrary-text-type.md).                                        |
| Texto   | Enumeração       | <A>=<a>;<B>=<b>;&lt; C &gt; = &lt; c&gt; | Valor selecionado em um conjunto. Consulte [Tipo de enum](enum-type.md).                                                 |
| Texto   | Formatado  |                                                             | Valor que atender à definição de Texto Formatado no instalador. Consulte [Tipo formatado](formatted-type.md). |
| Texto   | RTF        |                                                             | Uma cadeia de caracteres de texto RTF. Consulte [Tipo RTF](rtf-type.md).                                                          |
| Texto   | Identificador |                                                             | Uma cadeia de caracteres de texto em conformidade com Windows [identificador do instalador.](identifier.md)                              |



 

[Tipos de formato de inteiro](integer-format-types.md)



| Formatar  | Type | ContextData | Description                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Integer |      |             | Qualquer valor inteiro. Consulte [Tipo de inteiro arbitrário](arbitrary-integer-type.md). |



 

[Tipos de formato de chave](key-format-types.md)



| Formatar | Type      | ContextData      | Descrição                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Chave    | Arquivo      | AssemblyContext  | Permitir que os usuários configurem chaves estrangeiras para assemblies win32 ou common language runtime. Consulte [Tipo de arquivo](file-type.md). |
| Chave    | Binário    | Bitmap           | Chave estrangeira para uma linha de tabela binária que mantém um bitmap para uso na interface do usuário. Consulte [Tipo binário](binary-type.md).                  |
| Chave    | Binário    | ícone             | Chave estrangeira para uma linha de tabela binária que mantém um Ícone para uso na interface do usuário. Consulte [Tipo binário](binary-type.md).                   |
| Chave    | Binário    | EXE              | Chave estrangeira para uma linha de tabela binária que mantém um EXE de 32bits. Consulte [Tipo binário](binary-type.md).                             |
| Chave    | Binário    | EXE64            | Chave estrangeira para uma linha de tabela binária que mantém um EXE de 32 ou 64bits. Consulte [Tipo binário](binary-type.md).                       |
| Chave    | ícone      | ShortcutIcon     | Chave estrangeira para uma linha da tabela Ícone que mantém um Ícone para uso por um atalho. Consulte [Tipo de ícone](icon-type.md).                |
| Chave    | caixa de diálogo    | Caixa de diálogoNext       | Chave estrangeira para uma linha da tabela Dialog. Consulte [Tipo de caixa de diálogo](dialog-type.md).                                                 |
| Chave    | caixa de diálogo    | DialogPrev       | Chave estrangeira para uma linha da tabela Dialog. Consulte [Tipo de caixa de diálogo](dialog-type.md).                                                 |
| Chave    | Diretório | IsolationDir     | Chave estrangeira para uma linha da tabela Directory em que os arquivos isolados pertencem. Consulte [Tipo de diretório](directory-type.md).            |
| Chave    | Diretório | ShortcutLocation | Chave estrangeira para uma linha de tabela do Diretório em que um atalho deve ser instalado. Consulte [Tipo de diretório](directory-type.md).   |
| Chave    | Propriedade  |                  | Chave estrangeira para uma linha de propriedade. Consulte [Tipo de propriedade](property-type.md).                                                 |
| Chave    | Propriedade  | Público           | Chave estrangeira para uma linha de propriedade. Consulte [Tipo de propriedade](property-type.md).                                                 |
| Chave    | Propriedade  | Privado          | Chave estrangeira para uma linha de propriedade. Consulte [Tipo de propriedade](property-type.md).                                                 |



 

[Tipos de formato bitfield](bitfield-format-types.md)



| Formatar   | Type | ContextData                                  | Description                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Bitfield |      | &lt;mask &gt; ; <A> = <a> ; <B> =b | Altera um subconjunto de bits em uma coluna. Consulte [Tipo de bitfield arbitrário](arbitrary-bitfield-type.md). |



 

 

 



